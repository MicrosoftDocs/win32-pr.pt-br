---
title: usando páginas ASP para criar dinamicamente Windows listas de reprodução do metarquivo de mídia
description: usando páginas ASP para criar dinamicamente Windows listas de reprodução do metarquivo de mídia
ms.assetid: 9abf04a4-33b9-4502-aaf3-e40de06c7b41
keywords:
- Windows Playlists de metarquivo de mídia, criando
- listas de reprodução de metarquivo, criando
- listas de reprodução, criando
- Windows Playlists de metarquivo de mídia, criando dinamicamente
- listas de reprodução de metarquivo, criando dinamicamente
- listas de reprodução, criando dinamicamente
- Windows Playlists de metarquivo de mídia, páginas ASP
- listas de reprodução de metarquivo, páginas ASP
- listas de reprodução, páginas ASP
- criando listas de reprodução do metarquivo de mídia Windows
- criando dinamicamente Windows playlists de metarquivo de mídia
- Páginas ASP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 096a71a5ffedb353cbfd75fb1b5c23b97065ca96c0d75ac30588c44e7720f779
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762066"
---
# <a name="using-asp-pages-to-dynamically-create-windows-media-metafile-playlists"></a>usando páginas ASP para criar dinamicamente Windows listas de reprodução do metarquivo de mídia

Você pode usar Active Server páginas (arquivos ASP ou. asp) para gerar listas de reprodução dinamicamente com base nas informações fornecidas pelos usuários. uma página ASP é uma página da web dinâmica usada em conjunto com Serviços de Informações da Internet da Microsoft (IIS). o ASP é um ambiente no qual você pode combinar os componentes HTML, scripts e reutilizáveis do ActiveX server para criar soluções comerciais baseadas na Web, dinâmicas e poderosas. as páginas ASP permitem o script do lado do servidor para o IIS com suporte nativo para o microsoft Visual Basic scripting Edition (VBScript) e o microsoft JScript. Essa discussão pressupõe que você esteja familiarizado com o ASP e Definindo variáveis.

Todas as informações de cabeçalho devem estar contidas na primeira linha da cadeia de caracteres da página ASP retornada para Windows Media Player.

Ao usar páginas ASP para gerar listas de reprodução, você deve especificar valores para o **ContentType** do objeto de **resposta** e **expirar** as propriedades na página ASP devido a problemas de latência com Windows Media Player. o valor **Response. ContentType** deve ser uma extensão de nome de arquivo válida para os metaarquivos de mídia Windows. Os valores aceitáveis incluem WMA, Wax, WMV, WVX, ASF e ASX.

a propriedade **Response. expires** especifica o período de tempo, em segundos, que Windows Media Player armazena em cache o arquivo de lista de reprodução. especificar um valor de zero resulta em Windows Media Player solicitando uma nova lista de reprodução a partir do servidor sempre que o usuário atualizar a página.

Consulte o SDK da plataforma para obter detalhes sobre como usar o objeto de **resposta** em páginas Active Server.

o código a seguir é um exemplo de uma página ASP usada para gerar uma lista de reprodução de metarquivo de mídia Windows.


```XML
<%Response.ContentType = "video/x-ms-wma"%><%Response.expires=0 %>
<ASX VERSION="3.0">
    <TITLE>Your title here</TITLE>
    <ENTRY>
        <REF HREF ="mms://adventure-works.com/pubpt/filename.wma" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando listas de reprodução de metarquivo**](creating-metafile-playlists.md)
</dt> </dl>

 

 




