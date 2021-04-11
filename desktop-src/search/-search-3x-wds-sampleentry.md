---
description: Este tópico descreve as tecnologias relacionadas ao Windows Search.
ms.assetid: 76b39ea6-2aaf-40e0-aa56-2165e188244d
title: Tecnologias de pesquisa relacionadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f8a03738958e19712ff8cc4566e4b7f7396ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090090"
---
# <a name="related-search-technologies"></a>Tecnologias de pesquisa relacionadas

Este tópico descreve as tecnologias relacionadas ao [Windows Search](-search-3x-wds-overview.md).

Este tópico é organizado da seguinte maneira:

-   [Pesquisa empresarial](#enterprise-search)
    -   [Pesquisa do SharePoint Enterprise](#sharepoint-enterprise-search)
-   [Windows Desktop Search 2. x](#windows-desktop-search-2x)
-   [Platform SDK: serviço de indexação](#platform-sdk-indexing-service)
-   [Tópicos relacionados](#related-topics)

## <a name="enterprise-search"></a>Pesquisa empresarial

Para obter uma visão geral dos recursos técnicos do [Enterprise Search da Microsoft](https://www.microsoft.com/enterprisesearch/en/us/default.aspx), consulte:

-   [Centro de recursos de pesquisa empresarial](https://developer.microsoft.com/office/docs)
-   [Blog do Microsoft Enterprise Search](https://blogs.msdn.com/b/enterprisesearch/rss.aspx)

### <a name="sharepoint-enterprise-search"></a>Pesquisa do SharePoint Enterprise

O SharePoint Foundation 2010 fornece a [consulta do código do lado do servidor e a](/previous-versions/office/developer/sharepoint-2010/ee536691(v=office.14)) [consulta do código do lado do cliente](/previous-versions/office/developer/sharepoint-2010/ee539764(v=office.14)). Para obter mais informações sobre como consultar, Pesquisar novo conteúdo e melhorar a relevância com o SharePoint Server 2010 Enterprise Search, consulte [conceitos básicos do Enterprise Search](/previous-versions/office/ee554857(v=office.14)).

A pesquisa do Windows 7 dá suporte à Federação de pesquisa para armazenamentos de dados remotos usando as tecnologias OpenSearch, que permitem aos usuários acessar e interagir com seus dados remotos no Windows Explorer. O SharePoint Search Server 2008 e o MOSS 2007 SP2 também dão suporte à pesquisa federada de servidores remotos usando o OpenSearch. Para obter informações sobre a implantação do servidor de pesquisa 2008 com o Office SharePoint Server 2007, consulte [servidor de pesquisa de pesquisa federada \[ 2008 \] ](/previous-versions/office/bb931109(v=office.14)). Para obter informações sobre a pesquisa facetada do MOSS, na qual os resultados da pesquisa são relocalizados por categoria, consulte [codeplex](https://www.codeplex.com/FacetedSearch).

Os manipuladores de protocolo de pesquisa do Windows usam especificações de design semelhantes ao SharePoint Server e, em geral, podem ser usados de maneira intercambiável. Portanto, quando os usuários precisam Pesquisar bancos de dados herdados, armazenamentos de email ou outras estruturas que não têm suporte do Windows Search, primeiro você deve determinar se um manipulador de protocolo já existe para esse armazenamento de dados, talvez para uso com outro aplicativo, como o SharePoint Server. Nesse caso, você pode instalar esse manipulador de protocolo no sistema.

## <a name="windows-desktop-search-2x"></a>Windows Desktop Search 2. x

O uso do e do desenvolvimento para as versões 2. x do Microsoft Windows Desktop Search (WDS) é altamente desencorajado. Em vez de usar o [Windows Desktop Search 2. x](../lwef/-search-2x-wds-overview.md), use o [Windows Search](-search-3x-wds-overview.md) e a [API de pesquisa do Windows](-search-reference-entry-page.md).

## <a name="platform-sdk-indexing-service"></a>Platform SDK: serviço de indexação

[Platform SDK: o serviço de indexação](/previous-versions/windows/desktop/indexsrv/indexsrv-portal) é obsoleto a partir do Windows XP. Em vez disso, use o [Windows Search](-search-3x-wds-overview.md) e a [API de pesquisa do Windows](-search-reference-entry-page.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Guia do desenvolvedor do Windows Search](-search-developers-guide-entry-page.md)
</dt> <dt>

[Referência do Windows Search](-search-reference-entry-page.md)
</dt> <dt>

[Exemplos de código do Windows Search](-search-samples-ovw.md)
</dt> <dt>

[Pesquisa federada no Windows](-search-federated-search-overview.md)
</dt> <dt>

[Glossário do Windows Search](search-glossary.md)
</dt> </dl>

 

 
