We sometimes need to be able to obtain XML from an interactive report with column names. For example, for creating a report in BI Publisher, this code helps generate XML dynamically.


Step 1.
Create package PKG_GENERATE_REPORT

Step2.
Create button in Apex page.

Step 3.
Create Process:
declare
    v_report_xml    clob;
begin
   pkg_generate_report.sql2xml(in_app_id  => :APP_ID,
                               in_page_id => :APP_PAGE_ID,
                               out_clob   => v_report_xml);
end;


v_report_sql is xml for your query
