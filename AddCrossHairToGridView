protected void Page_Load(object sender, EventArgs e)
{
   DBLoadGridView(); // You write this!
   AddCrossHairToGridView(gvExample,1,0,0,0);
}

public void AddCrossHairToGridView(GridView gv, int top, int right, int bottom, int left)
{
   System.Text.StringBuilder js = new StringBuilder();
   js.Append("<script type=\"text/javascript\" language=\"javascript\">");
   js.Append("initCrossHairsTable(\"" + gv.ClientID.ToString() + "\",");
   js.Append(top + "," + right + "," + bottom + "," + left + ");");
   js.Append("<");
   js.Append("/script>");

   Type t = this.GetType();
   if (!ClientScript.IsClientScriptIncludeRegistered(t, "CrossHairJS"))
       ClientScript.RegisterClientScriptInclude("CrossHairJS", "crosshairs0.3.js");

   if (!ClientScript.IsClientScriptBlockRegistered(t, "HighlightScript"))
       ClientScript.RegisterStartupScript(t, "HighlightScript", js.ToString());
}
