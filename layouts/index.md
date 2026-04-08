{{ define "main" }}
    <header class="major">
        <h2>{{ .Title }}</h2>
    </header>

    {{ .Content }}

    <div class="row">
        {{ range first 3 (where .Site.RegularPages "Section" "posts") }}
        <section class="col-4 col-12-narrower">
            <div class="box post">
                <h3>{{ .Title }}</h3>
                <p>{{ .Summary }}</p>
                <a href="{{ .Permalink }}" class="button alt">閱讀全文</a>
            </div>
        </section>
        {{ end }}
    </div>
{{ end }}