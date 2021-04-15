---
title: Usando páginas ASP para criar dinamicamente listas de reprodução do metarquivo do Windows Media
description: Usando páginas ASP para criar dinamicamente listas de reprodução do metarquivo do Windows Media
ms.assetid: 9abf04a4-33b9-4502-aaf3-e40de06c7b41
keywords:
- Playlists do metarquivo do Windows Media, criando
- listas de reprodução de metarquivo, criando
- listas de reprodução, criando
- Playlists do metarquivo do Windows Media, criando dinamicamente
- listas de reprodução de metarquivo, criando dinamicamente
- listas de reprodução, criando dinamicamente
- Playlists do metarquivo do Windows Media, páginas ASP
- listas de reprodução de metarquivo, páginas ASP
- listas de reprodução, páginas ASP
- Criando listas de reprodução do metarquivo do Windows Media
- Criando dinamicamente playlists de metarquivo do Windows Media
- Páginas ASP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ea3cef88d86078aa95785163d7c2f4b0e57e975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498677"
---
# <a name="using-asp-pages-to-dynamically-create-windows-media-metafile-playlists"></a>Usando páginas ASP para criar dinamicamente listas de reprodução do metarquivo do Windows Media

Você pode usar Active Server páginas (arquivos ASP ou. asp) para gerar listas de reprodução dinamicamente com base nas informações fornecidas pelos usuários. Uma página ASP é uma página da Web dinâmica usada em conjunto com o Microsoft Serviços de Informações da Internet (IIS). O ASP é um ambiente no qual você pode combinar HTML, scripts e componentes de servidor ActiveX reutilizáveis para criar soluções de negócios baseadas na Web, dinâmicas e poderosas. As páginas ASP permitem o script do lado do servidor para o IIS com suporte nativo para o Microsoft Visual Basic Scripting Edition (VBScript) e o Microsoft JScript. Essa discussão pressupõe que você esteja familiarizado com o ASP e Definindo variáveis.

Todas as informações de cabeçalho devem estar contidas na primeira linha da cadeia de caracteres da página ASP retornada ao Windows Media Player.

Ao usar páginas ASP para gerar listas de reprodução, você deve especificar valores para o **ContentType** do objeto de **resposta** e **expirar** as propriedades na página ASP devido a problemas de latência com o Windows Media Player. O valor **Response. ContentType** deve ser uma extensão de nome de arquivo válida para os metaarquivos do Windows Media. Os valores aceitáveis incluem WMA, Wax, WMV, WVX, ASF e ASX.

A propriedade **Response. Expires** especifica o período de tempo, em segundos, que o Windows Media Player armazena em cache o arquivo de lista de reprodução. Especificar um valor de zero resulta no Windows Media Player solicitando uma nova lista de reprodução a partir do servidor sempre que o usuário atualizar a página.

Consulte o SDK da plataforma para obter detalhes sobre como usar o objeto de **resposta** em páginas Active Server.

O código a seguir é um exemplo de uma página ASP usada para gerar uma lista de reprodução do metarquivo do Windows Media.


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

 

 




