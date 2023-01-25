---
layout: default
title: AIOTI Ontology Landscape Portfolio
---

<head>
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/bulma@0.8.2/css/bulma.min.css"
    />
    <link rel="stylesheet" href="{{ '/assets/css/main.css' | relative_url }}" />
    <script
      src="https://code.jquery.com/jquery-3.5.0.min.js"
      integrity="sha256-xNzN2a4ltkB44Mc/Jz3pT4iU1cmeR0FkXs4pru/JxaQ="
      crossorigin="anonymous">
    </script>
    <script
      src="https://cdnjs.cloudflare.com/ajax/libs/datatables/1.10.20/js/jquery.dataTables.min.js"
      integrity="sha256-L4cf7m/cgC51e7BFPxQcKZcXryzSju7VYBKJLOKPHvQ="
      crossorigin="anonymous">
      </script>
  </head>

Browse the solutions provided by AIOTI members in the table below.
<br/>Follow [**this link**](./index.html) to return to the main page.

<div class= "container" >
  <table id="catalogue" class="display" style="width: 100%">
      <tbody>
        <td colspan="12" bgcolor=gray></td>  
        <!--For loop that iterates over markdown frontmatter in _solutions folder-->
        {% for solution in site.solutions %}
	<tr>
    	   <td colspan="12" class="divider" bgcolor=grey></td>
    	</tr>
        <tr>
	  <td colspan="2"><b>Acronym</b></td>
          <td colspan="4"><b>Name</b></td>
          <td colspan="5"><b>Main Areas</b></td>
          <td colspan="1"><b><a href="https://enspire.science/trl-scale-horizon-europe-erc-explained/">TRL</a></b></td>
        </tr>
        <tr>
          <td colspan="2">
            <strong>
         	{{ solution.acronym }}
            </strong>
            <br><br>
	  	<img src="{{ solution.logo }}" alt="   " width=100/>
          </td>
          <td colspan="4">
          	{{ solution.name }}
          </td>
          <td colspan="5">
		  {{ solution.main_areas }}
	  </td>
	  <td colspan="1"  bgcolor="{{ solution.hexcolor }}">
          	  {{ solution.trl }}
          </td>
        </tr>
	<tr>
	  <td colspan="12">
		<strong>Description:</strong>
            	{{ solution.description | markdownify }}
	  </td>
	</tr>
	<tr>
	  <td colspan="12">
		<strong>Technical Specification:</strong>
            	{{ solution.specification | markdownify }}
	  </td>
	</tr>
	<tr>
	    <td colspan="12">
		<strong>Ontology URI:</strong>
                <a href="{{ solution.ontology_uri }}">{{ solution.ontology_uri }}</a>
	    </td>
        </tr>
	<tr>
	   <td colspan="6">
		<strong>Maintainer:</strong>
            	{{ solution.maintainer | markdownify}}
	   </td>
	   <td colspan="6">
		<strong>License:</strong>
            	{{ solution.license | markdownify }}
	   </td>
        </tr>
	<tr>
	   <td colspan="12">
		<strong>Complete Survey Information:</strong>
               	<a href="{{ solution.complete_survey_uri }}">{{ solution.acronym }}</a>
	   </td>
        </tr>
	{% endfor %}
	<td colspan="12" bgcolor=gray></td>  
      </tbody>
    </table>
  </div>

## Contribute your own ontology to the next version of the Ontology Landscape

Please fill out our [Survey](https://ec.europa.eu/eusurvey/runner/OntologyLandscapeTemplate)
