var mymap;

var Escolas = [
			{nome:"Colégio Adventista de Campinas",latitude:-22.912305, longitude:-47.054025, 
				descricao:"Escola particular de Campinas, São Paulo <br>Endereço: R. Oscár Leite, 55 - Pte. Preta, <br>Campinas - SP, 13041-620 <br>Telefone: (19) 3519-3800"},
			{nome:"Colégio Lyon Campinas",latitude:-22.910657, longitude:-47.047660, 
				descricao:"Escola particular de Campinas, São Paulo <br>Endereço: R. Proença, 1141 - Jardim Proença, <br>Campinas - SP, 13026-121 <br>Telefone: (19) 3252-7400"},
			{nome:"Escola Futura Campinas",latitude:-22.915070, longitude:-47.042107, 
				descricao:"Escola particular de Campinas, São Paulo <br>Endereço: Av. Guarani, 405 - Jardim Guarani, <br>Campinas - SP, 13100-211 <br>Telefone: (19) 3253-0346"},
			{nome:"Colégio Pio XII",latitude:-22.909890, longitude:-47.052169, 
				descricao:"Escola católica em Campinas, São Paulo <br>Endereço: R. Boaventura do Amaral, 354 - Bosque, <br>Campinas - SP, 13026-908 <br>Telefone: (19) 3341-3170"},
			{nome:"Colégio Franciscano Ave Maria",latitude:-22.9121953, longitude:-47.0568606, 
				descricao:"Escola católica em Campinas, São Paulo <br>Endereço: Rua Barão de Jaguara, 190 - Bosque, <br>Campinas - SP, 13026-099 <br>Telefone: (19) 2136-9933"},
			{nome:"Colégio Sagrado Coração de Jesus",latitude:-22.907055, longitude:-47.037794, 
				descricao:"Escola em Campinas, São Paulo <br>Endereço: Av. Dr. Manoel Afonso Ferreira, 245 - Jardim Paraíso, <br>Campinas - SP, 13100-029 <br>Telefone: (19) 3753-2400"},
			{nome:"Colégio Asther",latitude:-22.918105, longitude:-47.043423, 
				descricao:"Escola em Campinas, São Paulo<br>Endereço: Av. Princesa D'Oeste, 556 - Jardim Paraíso, <br>Campinas - SP, 13100-040<br>Telefone: (19) 3753-6300"},
			{nome:"Colégio Presbiteriano Eduardo Lane",latitude:-22.906127, longitude:-47.056444, 
				descricao:"Escola em Campinas, São Paulo<br>Endereço: R. Luzitana, 824 - Centro, <br>Campinas - SP, 13015-121<br>Telefone: (19) 3231-9236"},
			{nome:"Batista Agape Colegio",latitude:-22.919667, longitude:-47.057373, 
				descricao:"Escola particular de Campinas, São Paulo<br>Endereço: R. Sandoval Meireles, 135 - Pte. Preta, <br>Campinas - SP, 13041-315<br>Telefone: (19) 2127-4200"},
			{nome:"Colegio Anglo Center Ville",latitude:-22.917983, longitude:-47.087338, 
				descricao:"Escola particular de Campinas, São Paulo<br>Endereço: Av. João Batista Morato do Canto, 1695 -<br>Parque Industrial, Campinas - SP, 13031-800<br>Telefone: (19) 2515-2353"},
			{nome:"Colégio Novo Anglo",latitude:-22.804745, longitude:-47.076722, 
				descricao:"Colégio de ensino médio, Campinas, São Paulo<br>Endereço: R. Dr. Sérgio Almeida Prado, 210 - <br>Cidade Universitária, Campinas - SP, 13083-750<br>Telefone: (19) 3287-6613"},
			{nome:"Anglo Tamandaré Campinas",latitude:-22.895486, longitude:-47.052208, 
				descricao:"Escola em Campinas, São Paulo<br>Endereço: R. Maria Monteiro, 1016 -<br> Cambuí, Campinas - SP, 13025-151<br>Telefone: (19) 3252-8082"},
			{nome:"Colégio Novo Anglo - Unidade Taquaral",latitude:-22.866564, longitude:-47.049107, 
				descricao:"Escola particular de Campinas, São Paulo<br>Endereço: R. Jorge de Figueiredo Corrêa, 545 - <br>Parque Taquaral, Campinas - SP, 13087-261<br>Telefone: (19) 3256-6828"},
			{nome:"Novo Anglo Barão Geraldo",latitude:-22.824502, longitude:-47.079759, 
				descricao:"Escola em Campinas, São Paulo<br>Endereço: Av. Albino J. B. de Oliveira, 1600 - <br>Jardim Afife, Campinas - SP<br>Telefone: (19) 3289-1051"},
			{nome:"Colégio Integral",latitude:-22.901176, longitude:-47.029873, 
				descricao:"Escola em Campinas, São Paulo<br>Endereço: Avenida José Araújo Cunha, 71 - <br>Paineiras, Campinas - SP, 13094-530<br>Telefone: (19) 3794-4444"},
			{nome:"Colégio Integral AlphaVille",latitude:-22.820719, longitude:-47.036072, 
				descricao:"Escola em Campinas, São Paulo<br>Endereço: R. Embiruçu, 43 - <br>Lot a Campinas, Campinas - SP, 13098-320<br>Telefone: (19) 3796-9400"},
			{nome:"Colégio Dom Barreto",latitude:-22.919701, longitude:-47.053470, 
				descricao:"Escola particular de Campinas, São Paulo<br>Endereço: Av. da Saudade, 705 - <br>Pte. Preta, Campinas - SP, 13041-670<br>Telefone: (19) 3232-4366"},
			{nome:"Colégio Poli-Bentinho",latitude:-22.910078, longitude:-47.059588, 
				descricao:"Centro educacional em Campinas, São Paulo<br>Endereço: R. José de Alencar, 430 - <br>Centro, Campinas - SP, 13013-040<br>Telefone: (19) 3737-3270"},
			{nome:"Etec Bento Quirino",latitude:-22.890915, longitude:-47.058381, 
				descricao:"Escola técnica em Campinas, São Paulo<br>Endereço: Av. Orosimbo Maia, 2600 - <br>Cambuí, Campinas - SP, 13024-045<br>Telefone: (19) 3252-3596"},
			{nome:"Oficina do Estudante",latitude:-22.889761, longitude:-47.064651, 
				descricao:"Escola particular de Campinas, São Paulo<br>Endereço: Av. Brasil, 601 - <br>Jardim Guanabara, Campinas - SP, 13073-012<br>Telefone: (19) 3241-6688"},
			{nome:"Objetivo Campinas unidade Barão Geraldo",latitude:-22.819855, longitude:-47.085948, 
				descricao:"Escola particular de Campinas, São Paulo<br>Endereço: R. João Pedroso, 265 - <br>Barão Geraldo, Campinas - SP, 13083-584<br>Telefone: (19) 3249-2710"},
			{nome:"Centro Educacional Objetivo Cambuí",latitude:-22.890160, longitude:-47.047569, 
				descricao:"Escola particular de Campinas, São Paulo<br>Endereço: R. Cap Francisco de Paula, 333 - <br>Cambuí, Campinas - SP, 13024-450<br>Telefone: (19) 3254-6333"},
			{nome:"Centro Educacional Objetivo Centro",latitude:-22.900866, longitude:-47.062581, 
				descricao:"Colégio de ensino médio, Campinas, São Paulo<br>Endereço: R. Dr. Delfino Cintra, 100 - <br>Centro, Campinas - SP, 13020-100<br>Telefone: (19) 3234-3130"},
			{nome:"Colégio Notre Dame",latitude:-22.895330, longitude:-47.002749, 
				descricao:"Escola em Campinas, São Paulo<br>Endereço: R. Egberto Ferreira de Arruda Camargo, 151 <br>Notre Dame, Campinas - SP, 13092-621<br>Telefone: (19) 2138-8300"}
	];

function start(){
		
		mymap = L.map('mapid').setView([-22.909931, -47.062635], 15);

		L.tileLayer('https://api.tiles.mapbox.com/v4/{id}/{z}/{x}/{y}.png?access_token=pk.eyJ1IjoibWFwYm94IiwiYSI6ImNpejY4NXVycTA2emYycXBndHRqcmZ3N3gifQ.rJcFIG214AriISLbB6B5aw', {
			maxZoom: 18,
			attribution: 'Map data &copy; <a href="http://openstreetmap.org">OpenStreetMap</a> contributors, ' +
				'<a href="http://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>, ' +
				'Imagery © <a href="http://mapbox.com">Mapbox</a>',
			id: 'mapbox.streets'
		}).addTo(mymap);

		var selectString= "";

		for(i=0;i<Escolas.length;i++){
			L.marker([Escolas[i].latitude, Escolas[i].longitude]).addTo(mymap)
				.bindPopup("<b>"+Escolas[i].nome+"</b><br /> "+Escolas[i].descricao).openPopup();
			/*var popup = L.popup()
    			.setLatLng([Escolas[i].latitude, Escolas[i].longitude])
    			.setContent(Escolas[i].nome)
    			.openOn(mymap);
    		*/
    		selectString = selectString + "<option value='" + i + "'>" + Escolas[i].nome + "</option>";
		}

		document.getElementById("selectEscolas").innerHTML = selectString;



	}

	function select(index){
		mymap.setView([Escolas[index].latitude, Escolas[index].longitude], 15);
	}