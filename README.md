@model AdmissionCollege.Models.PayMent

@{
    ViewBag.Title = "Create";
    Layout = null;
}

<h2>Create</h2>


@using (Html.BeginForm())
{
    @Html.AntiForgeryToken()

<div class="form-horizontal">
    <h4>PayMent</h4>
    <hr />
    @Html.ValidationSummary(true, "", new { @class = "text-danger" })
<form id="pdfForm">
    <div class="form-group">
        @Html.LabelFor(model => model.BillingID, htmlAttributes: new { @class = "control-label col-md-2" })
        <div class="col-md-10">
            @Html.EditorFor(model => model.BillingID, new { htmlAttributes = new { @class = "form-control" } })
            @Html.ValidationMessageFor(model => model.BillingID, "", new { @class = "text-danger" })
        </div>
    </div>

    <div class="form-group">
        @Html.LabelFor(model => model.FullName, htmlAttributes: new { @class = "control-label col-md-2" })
        <div class="col-md-10">
            @Html.EditorFor(model => model.FullName, new { htmlAttributes = new { @class = "form-control" } })
            @Html.ValidationMessageFor(model => model.FullName, "", new { @class = "text-danger" })
        </div>
    </div>

    <div class="form-group">
        @Html.LabelFor(model => model.Email, htmlAttributes: new { @class = "control-label col-md-2" })
        <div class="col-md-10">
            @Html.EditorFor(model => model.Email, new { htmlAttributes = new { @class = "form-control" } })
            @Html.ValidationMessageFor(model => model.Email, "", new { @class = "text-danger" })
        </div>
    </div>

    <div class="form-group">
        @Html.LabelFor(model => model.Address, htmlAttributes: new { @class = "control-label col-md-2" })
        <div class="col-md-10">
            @Html.EditorFor(model => model.Address, new { htmlAttributes = new { @class = "form-control" } })
            @Html.ValidationMessageFor(model => model.Address, "", new { @class = "text-danger" })
        </div>
    </div>

    <div class="form-group">
        @Html.LabelFor(model => model.City, htmlAttributes: new { @class = "control-label col-md-2" })
        <div class="col-md-10">
            @Html.EditorFor(model => model.City, new { htmlAttributes = new { @class = "form-control" } })
            @Html.ValidationMessageFor(model => model.City, "", new { @class = "text-danger" })
        </div>
    </div>

    <div class="form-group">
        @Html.LabelFor(model => model.State, htmlAttributes: new { @class = "control-label col-md-2" })
        <div class="col-md-10">
            @Html.EditorFor(model => model.State, new { htmlAttributes = new { @class = "form-control" } })
            @Html.ValidationMessageFor(model => model.State, "", new { @class = "text-danger" })
        </div>
    </div>

    <div class="form-group">
        @Html.LabelFor(model => model.ZipCode, htmlAttributes: new { @class = "control-label col-md-2" })
        <div class="col-md-10">
            @Html.EditorFor(model => model.ZipCode, new { htmlAttributes = new { @class = "form-control" } })
            @Html.ValidationMessageFor(model => model.ZipCode, "", new { @class = "text-danger" })
        </div>
    </div>

    <div class="form-group">
        @Html.LabelFor(model => model.Cardaccepted, htmlAttributes: new { @class = "control-label col-md-2" })
        <div class="col-md-10">
            @Html.EditorFor(model => model.Cardaccepted, new { htmlAttributes = new { @class = "form-control" } })
            @Html.ValidationMessageFor(model => model.Cardaccepted, "", new { @class = "text-danger" })
        </div>
    </div>

    <div class="form-group">
        @Html.LabelFor(model => model.Nameoncard, htmlAttributes: new { @class = "control-label col-md-2" })
        <div class="col-md-10">
            @Html.EditorFor(model => model.Nameoncard, new { htmlAttributes = new { @class = "form-control" } })
            @Html.ValidationMessageFor(model => model.Nameoncard, "", new { @class = "text-danger" })
        </div>
    </div>

    <div class="form-group">
        @Html.LabelFor(model => model.CreditCardNumber, htmlAttributes: new { @class = "control-label col-md-2" })
        <div class="col-md-10">
            @Html.EditorFor(model => model.CreditCardNumber, new { htmlAttributes = new { @class = "form-control" } })
            @Html.ValidationMessageFor(model => model.CreditCardNumber, "", new { @class = "text-danger" })
        </div>
    </div>

    <div class="form-group">
        @Html.LabelFor(model => model.ExpMonth, htmlAttributes: new { @class = "control-label col-md-2" })
        <div class="col-md-10">
            @Html.EditorFor(model => model.ExpMonth, new { htmlAttributes = new { @class = "form-control" } })
            @Html.ValidationMessageFor(model => model.ExpMonth, "", new { @class = "text-danger" })
        </div>
    </div>

    <div class="form-group">
        @Html.LabelFor(model => model.ExpYear, htmlAttributes: new { @class = "control-label col-md-2" })
        <div class="col-md-10">
            @Html.EditorFor(model => model.ExpYear, new { htmlAttributes = new { @class = "form-control" } })
            @Html.ValidationMessageFor(model => model.ExpYear, "", new { @class = "text-danger" })
        </div>
    </div>

    <div class="form-group">
        @Html.LabelFor(model => model.CVV, htmlAttributes: new { @class = "control-label col-md-2" })
        <div class="col-md-10">
            @Html.EditorFor(model => model.CVV, new { htmlAttributes = new { @class = "form-control" } })
            @Html.ValidationMessageFor(model => model.CVV, "", new { @class = "text-danger" })
        </div>
    </div>
</form>

        <div class="form-group">
            <div class="col-md-offset-2 col-md-10">
                <button><a href="@Url.Action(/*method*/"Index", /*controller*/"PayMentpdf")" class="btn btn-default">Pay</a> </button>
                @* <input type="submit" value="Pay" class="btn btn-default" />*@
            </div>
            @*<div class="form-group">
                    <button><a href="@Url.Action(/*method*/"Create", /*controller*/"PayMentpdf")" class="login-btn">Pay</a> </button>
                </div>*@
        </div>
</div>
   

     
            <script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
       
       
        <input type="button"
               value="Generate PDF"
               onclick="generatePdf()">


        <script>
            function generatePdf() {
                let formElement = document.getElementById('pdfForm');
                html2pdf().from(formElement).save();
            }
        </script>
  
}

<div>
    @Html.ActionLink("Back to List", "Index")
</div>

@section Scripts {
    @Scripts.Render("~/bundles/jqueryval")
}
