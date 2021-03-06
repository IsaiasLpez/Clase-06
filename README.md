<!DOCTYPE html>
<html lang="es">

    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous" />
        <title>Inmigrantes internacionales</title>
        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;600&display=swap" rel="stylesheet">
        <style>
            :root { --bs-font-sans-serif: 'Roboto', sans-serif; }
            h1{font-size: calc(2rem + 2vw)}
            em{
              font-weight: 600;
              font-style: normal;
              text-decoration: underline;
            }
            @media (min-width: 992px) { header p{ text-align: justify; text-justify: inter-word; } }
            g#grafico g:nth-child(odd) rect {fill: url(#my-cool-gradient) #447799;}
            g#grafico g:nth-child(even) rect {fill: url(#my-cool-gradient2) #F16B0F;}
        </style>
    </head>

    <body>

        <header class="container">
            <div class="row py-4">
                <div class="col-11 col-sm-10 col-md-9 col-lg-8 col-xl-7 col-xxl-6 mx-auto">
                    <h1 class="mb-3 mt-5 text-center">Cantidad de inmigrantes internacionales
                      </h1>
                      <h1 class="mb-3 mt-3 text-center">
                        (censo 2017)</h1>

                    <h2 class="fs-6 mb-5 text-center text-uppercase">Dúo dinámico</h2>

                    <p class="lead">En 2017 se censaron <em>746.465 personas</em> nacidas en el extranjero que residen en Chile, las que representan <em>4,35%</em> de la población total que vive en el país. Dicho porcentaje en 2002 era <em>1,27%</em>

</p>

                    <p>La mayor parte de la población inmigrante internacional nació en Perú, Colombia y Venezuela.

</p>
                </div>
            </div>
        </header>
        <div>
        <svg style="width:0;height:0;position:absolute;" aria-hidden="true" focusable="false">
          <linearGradient id="my-cool-gradient" x2="1" y2="1">
            <stop offset="0%" stop-color="#447799" />
            <stop offset="50%" stop-color="#224488" />
            <stop offset="100%" stop-color="#112266" />
          </linearGradient>
        </svg>
      </div>
      <div>
      <svg style="width:0;height:0;position:absolute;" aria-hidden="true" focusable="false">
        <linearGradient id="my-cool-gradient2" x2="1" y2="1">
          <stop offset="0%" stop-color="#F16B0F" />
          <stop offset="50%" stop-color="#F1460F" />
          <stop offset="100%" stop-color="#F10F0F" />
        </linearGradient>
      </svg>
    </div>
        <main class="container pb-5">
            <div class="row">
                <div class="col-sm-11 col-md-10 col-lg-9 col-xl-8 col-xxl-7 mx-auto">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 400 200" class="bg-light my-3">
                        <g id="grafico"></g>
                    </svg>
                </div>
                <div class="col-11 col-sm-10 col-md-9 col-lg-8 col-xl-7 col-xxl-6 mx-auto mb-5">
                    <p>El 81% de los inmigrantes internacionales que declararon residir en Chile al momento del Censo nacieron en los siguientes siete países:

</p>
<ul>
  <li>Perú (25,2%)</li>
  <li>Colombia (14,1%)</li>
  <li>Venezuela (11,1%)</li>
  <li>Bolivia (9,9%)</li>
  <li>Argentina (8,9%)</li>
  <li>Haití (8,4%)</li>
  <li>Ecuador (3,7%)</li>
</ul>
                </div>
            </div>
        </main>
        <footer class="bg-black text-black-50">
            <div class="container">
                <div class="row py-3">
                    <div class="col-12">
                        <p class="d-flex justify-content-between small p-1 m-0">
                            <!--reemplaza el # que sigue con la URL de tu cuenta en GitHub-->
                            <a href="https://github.com/IsaiasLpez" class="link-light">Isaías López</a>
                            <a href="https://github.com/NicoGaona" class="link-light">Nicolás Gaona</a>
                            <a href="https://github.com/profesorfaco/dno075-2022-1/" class="link-light">Infografía Digital</a>
                            <a href="https://github.com/profesorfaco/dno075-2022-1/tree/main/clase-06" class="d-none d-lg-inline link-light">Lunes 11 de abril, 2022</a>
                        </p>
                    </div>
                </div>
            </div>
        </footer>
        <script>
            var censo = [
                { pais: "Perú", inmigracion: 187757 },
                { pais: "Colombia", inmigracion: 105445 },
                { pais: "Venezuela", inmigracion: 83045 },
                { pais: "Bolivia", inmigracion: 73796 },
                { pais: "Argentina", inmigracion: 66491 },
                { pais: "Haití", inmigracion: 62683 },
                { pais: "Ecuador", inmigracion: 27692 },
                { pais: "Otro país", inmigracion: 136075 },
                { pais: "País ignorado", inmigracion: 3482 },
            ];
            censo.forEach(function (dato, i) {
                document.querySelector("#grafico").innerHTML += '<g transform="translate(10, '+ 17 * (i + 1) +')"><rect x="0" y="0" width="'+ (dato.inmigracion/1000) +'" height="10"></rect><text x="'+((dato.inmigracion/1000)+5)+'" y="8" font-size="8">'+dato.pais+'</text></g>';
            });
        </script>
    </body>
</html>
