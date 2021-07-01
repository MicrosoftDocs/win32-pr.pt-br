---
title: Registro em log do W3C
description: O registro em log estendido do W3C é o tipo de log do lado do servidor que pode ser habilitado na sessão do servidor ou no grupo de URL.
ms.assetid: a08b8f9e-2247-43c6-b253-81f72001d8d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb53ccf3b6bf5383a0a4da62538b6fa516c500f8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119941"
---
# <a name="w3c-logging"></a>Registro em log do W3C

O registro em log estendido do W3C é o tipo de log do lado do servidor que pode ser habilitado na sessão do servidor ou no grupo de URL. Quando o registro em log do W3C está habilitado em um grupo de URL, o registro em log é executado somente em solicitações roteados para o Grupo de URL. Um arquivo de log separado é criado para cada grupo de URL configurado para habilitar o registro em log do W3C.

Quando o registro em log do W3C está habilitado na sessão do servidor, ele funciona como forma centralizada de registro em log para todos os grupos de URL na sessão do servidor. Um único arquivo de log é mantido para todos os grupos de URL na sessão do servidor.

A tabela a seguir lista os campos que podem ser registrados pela API do Servidor HTTP. A tabela contém um subconjunto das constantes [**\_ HTTP LOG \_ FIELD.**](http-log-field--constants.md) Alguns dos campos listados abaixo são gerados automaticamente pela API do Servidor HTTP internamente e, portanto, não estão contidos na estrutura DE DADOS [**\_ CAMPOS \_ \_ DE LOG HTTP.**](/windows/desktop/api/Http/ns-http-http_log_fields_data) A coluna "Aparece como" contém o texto que aparece no arquivo de log. Os dados na tabela estão na ordem de ocorrência no registro de arquivo de log.

Os campos que não estão marcados como "API do Servidor HTTP gerada" devem ser passados dentro da estrutura DE DADOS [**\_ CAMPOS \_ \_ DE LOG HTTP**](/windows/desktop/api/Http/ns-http-http_log_fields_data) por aplicativo. O aplicativo pode gerar esses campos da estrutura [**\_ SOLICITAÇÃO HTTP**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) passada para ele.



| Campo                            | Aparece como      | Descrição                                                                                                                                | Membro DE \_ \_ DADOS DE CAMPOS DE LOG HTTP \_ | Constantes \_ HTTP LOG \_ FIELDS      |
|----------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|----------------------------------|
| Data                             | data            | A data em que a atividade ocorreu.                                                                                                   | API do Servidor HTTP gerada.     | DATA DO \_ CAMPO DE LOG \_ \_ HTTP           |
| Hora                             | time            | A hora, em UTC (tempo universal coordenado), em que a atividade ocorreu.                                                             | API do Servidor HTTP gerada.     | HORA DO \_ CAMPO DE LOG \_ \_ HTTP           |
| Nome do Serviço e Número da Instância | s-sitename      | O nome do serviço de Internet e o número da instância que estava em execução no cliente.                                                              | ServiceName                    | NOME \_ DO SITE DO CAMPO \_ \_ DE LOG \_ HTTP     |
| Nome do Servidor                      | s-computername  | O nome do servidor no qual a entrada do arquivo de log foi gerada.                                                                          | ServerName                     | NOME \_ DO COMPUTADOR DO CAMPO \_ \_ DE LOG \_ HTTP |
| Endereço IP do servidor                | s-ip            | O endereço IP do servidor no qual a entrada do arquivo de log foi gerada.                                                                    | ServerIp                       | IP \_ DO SERVIDOR DE CAMPO DE LOG \_ \_ \_ HTTP     |
| Método                           | cs-method       | O verbo solicitado, por exemplo, um método GET.                                                                                             | Método                         | MÉTODO DE \_ CAMPO DE LOG \_ \_ HTTP         |
| Tronco de URI                         | cs-uri-stem     | O destino do verbo, por exemplo, Default.htm.                                                                                          | UriStem                        | STEM \_ DO \_ URI DO CAMPO \_ DE LOG \_ HTTP      |
| Consulta de URI                        | cs-uri-query    | A consulta, se alguma, que o cliente estava tentando executar. Um URI (Resource Identifier Universal) consulta é necessário apenas para páginas dinâmico. | UriQuery                       | CONSULTA \_ DE \_ URI DO \_ CAMPO \_ DE LOG HTTP     |
| Porta do servidor                      | s-port          | O número da porta do servidor configurado para o serviço.                                                                                 | ServerPort                     | PORTA \_ DO SERVIDOR DE CAMPO \_ \_ DE LOG \_ HTTP   |
| Nome do Usuário                        | cs-username     | O nome do usuário autenticado que acessou o servidor. Os usuários anônimos são indicados por um hífen.                                    | UserName                       | NOME \_ DE USUÁRIO DO CAMPO \_ \_ DE LOG \_ HTTP     |
| Endereço IP do Cliente                | c-ip            | Endereço IP do cliente que fez a solicitação.                                                                                        | ClientIp                       | IP \_ DO CLIENTE DO CAMPO DE LOG \_ \_ \_ HTTP     |
| Versão do protocolo                 | cs-version      | A versão do protocolo HTTP que o cliente usou.                                                                                            | API do Servidor HTTP gerada.     | VERSÃO \_ DO CAMPO DE LOG \_ \_ HTTP        |
| Agente do usuário                       | cs(User-Agent)  | O tipo de navegador que o cliente usou.                                                                                                     | UserAgent                      | AGENTE DE \_ USUÁRIO DO CAMPO DE LOG \_ \_ \_ HTTP    |
| Cookie                           | cs(Cookie)      | O conteúdo do cookie enviado ou recebido, se for o caso.                                                                                        | Cookie                         | COOKIE DE \_ CAMPO DE LOG \_ \_ HTTP         |
| Referenciador                         | cs(Referrer)    | O site que o usuário visitou pela última vez. Esse site fornece um link para o site atual.                                                        | Referenciador                       | REFERÊNCIA \_ DE CAMPO DE LOG \_ \_ HTTP       |
| Host                             | cs-host         | O nome do cabeçalho de host, se houver.                                                                                                              | Host                           | \_host de \_ campo de log http \_           |
| Status HTTP                      | sc-status       | O código de status HTTP.                                                                                                                      | ProtocolStatus                 | \_status do \_ campo de log http \_         |
| Substatus do protocolo               | SC-substatus    | O código de erro de substatus.                                                                                                                  | SubStatus                      | substatus de \_ campo de log http \_ \_ \_    |
| Status do Win32                     | SC-Win32-status | O código de status do Windows.                                                                                                                   | Win32Status                    | \_Status do \_ Win32 do campo de log http \_ \_  |
| Bytes Enviados                       | SC-bytes        | O número de bytes enviados pelo servidor.                                                                                                    | API do servidor HTTP gerada.     | \_bytes de campo de log http \_ \_ \_ enviados    |
| Bytes Recebidos                   | cs-bytes        | O número de bytes recebidos e processados pelo servidor.                                                                                  | API do servidor HTTP gerada.     | \_bytes de campo de log http \_ \_ \_ recv    |
| Tempo decorrido                       | tempo decorrido      | O período de tempo que a ação tomou em milissegundos.                                                                                  | API do servidor HTTP gerada.     | \_tempo de campo de log http \_ \_ \_ retirado    |
| ID do fluxo                      | streamid          | A ID do fluxo.                                                                                  | API do servidor HTTP gerada.     | \_ID do \_ fluxo do campo de log http \_ \_       |



 

O arquivo de log é um formato baseado em texto ASCII personalizável. Os prefixos de campo no arquivo são definidos da seguinte maneira:

| Prefixo    | Descrição                          |
|-----|---------------------------|
| s   | Ações do servidor.           |
| c   | Ações do cliente.           |
| SC  | Ações de servidor para cliente. |
| cs  | Ações de cliente para servidor. |



 

No entanto, o aplicativo pode selecionar um ou mais campos do arquivo de log estendido do W3C, nem todos os campos conterão informações. Para campos que são selecionados, mas para os quais não há informações, um hífen (-) aparece como um espaço reservado. Se um campo contiver um caractere não imprimível, a API do servidor HTTP o substituirá por um sinal de adição (+) para preservar o formato do arquivo de log. Isso normalmente ocorre com ataques de vírus, quando, por exemplo, um usuário mal-intencionado envia retornos de carro e feeds de linha que, se não forem substituídos pelo sinal de adição (+), quebraria o formato do arquivo de log. Os campos são separados por espaços.

Se um campo for habilitado pelo grupo de URLs ou pela sessão de servidor, mas não for selecionado para a solicitação, ele aparecerá no arquivo de log com um hífen (-) como um espaço reservado.

Os arquivos de log são criados quando a primeira solicitação chega no grupo de URLs ou na sessão de servidor, eles não são criados quando o log é configurado. O exemplo a seguir mostra a primeira entrada do arquivo de log para um arquivo de log do W3C com os campos IP do cliente, nome de usuário, IP do servidor, porta do servidor, método, tronco URI, consulta de URI, status e agente do usuário habilitado:

``` syntax
#Software: Microsoft HTTP Server API 2.0  
#Version: 1.0   // the log file version as it's described by "https://www.w3.org/TR/WD-logfile".
#Date: 2002-05-02 17:42:15  // when the first log file entry was recorded, which is when the entire log file was created.
#Fields: date time c-ip cs-username s-ip s-port cs-method cs-uri-stem cs-uri-query sc-status cs(User-Agent)
2002-05-02 17:42:15 172.22.255.255 - 172.30.255.255 80 GET /images/picture.jpg - 200 Mozilla/4.0+(compatible;MSIE+5.5;+Windows+2000+Server)
```

O campo time-taked é inicializado quando a API do servidor HTTP recebe o primeiro byte, antes de a solicitação ser analisada. O carimbo de data/hora decorrido é interrompido quando ocorre a última conclusão de envio. O tempo decorrido não reflete o tempo na rede. A primeira solicitação para o site mostra um tempo um pouco mais longo do que outras solicitações semelhantes, pois a API do servidor HTTP abre o arquivo de log com a primeira solicitação.

 

 