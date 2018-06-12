# test3

                var xmlhttp = new XMLHttpRequest();
                var url = "/app/create";

                xmlhttp.onreadystatechange = function() {
                                if (this.readyState == 4 && this.status == 200) {
                                                var result = JSON.parse(this.responseText);
                                                console.log(this.responseText);
                                                console.log(result.identity);
                                                identity = result.identity;
                                                var config = {
                                                                host: window.location.hostname,
                                                                prefix: "/saml/",
                                                                port: window.location.port,
                                                                isSecure: window.location.protocol === "https:",
                                                                identity: result.identity,
                                                };

                                                var app = qlik.sessionAppFromApp("f964b975-b69a-4812-8683-b5a0df29f3e3", config);
                                                //app.doReload().then((result) => {
                                                                app.getObject('QV01','zswLzs');
                                                                app.getObject('QV02','RYMj');
                                                                app.getObject('QV04','MRmuW');
                                                                app.getObject('QV03','PyQXKt');
                                                                new AppUi( app );
                                                //});
                                }
                };
                xmlhttp.open("GET", url, true);
                xmlhttp.send();
