---
title: Criando o documento ServiceInfo dinamicamente
description: Criando o documento ServiceInfo dinamicamente
ms.assetid: 96937b04-f705-49f6-8ddf-25c98a51dc9a
keywords:
- Windows Media Player online, criando o documento ServiceInfo
- lojas online, criando o documento ServiceInfo
- type 1 online stores,creating ServiceInfo document
- type 2 online stores,creating ServiceInfo document
- Windows Media Player online, criando dinamicamente o documento ServiceInfo
- lojas online, criando dinamicamente o documento ServiceInfo
- tipo 1 lojas online, criando dinamicamente o documento ServiceInfo
- tipo 2 lojas online, criando dinamicamente o documento ServiceInfo
- Windows Media Player online, documento ServiceInfo
- lojas online, documento ServiceInfo
- type 1 online stores,ServiceInfo document
- type 2 online stores,ServiceInfo document
- criando dinamicamente o documento ServiceInfo
- criando o documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3883487d072af57174a1f40f2fcef05d3290917b473a95bf723c34d793c5ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340986"
---
# <a name="creating-the-serviceinfo-document-dynamically"></a>Criando o documento ServiceInfo dinamicamente

Você pode usar o ASP para criar o documento ServiceInfo. Isso pode lhe dar maior flexibilidade em sua loja online usando as seguintes técnicas:

-   Gerando dinamicamente o nome do host para URLs.
-   Alterando URLs para localização com base em parâmetros de localidade e geoid.
-   A adoção dinâmica de parâmetros de cadeia de caracteres de consulta da URL do ServiceInfo para outras URLs, como a URL da página de navegação.

O código de exemplo a seguir mostra uma página ASP simples que cria dinamicamente um documento ServiceInfo:


```C++
<%
    Dim sHost
    Dim sLocale

    sHost = Request.ServerVariables("HTTP_HOST")
    sLocale = Request.QueryString("locale")
%>

<?xml version="1.0" encoding="utf-8"?>
<ServiceInfo Version="1.00" Key="MyCommerceService">
    <FriendlyName>My Online Store</FriendlyName>
    <ServiceTask1
        URL = "https://<%= sHost %>/service/html/Music.asp">
    </ServiceTask1>
    <ServiceTask2
        URL = "https://<%= sHost %>/service/html/Video.asp">
    </ServiceTask2>
    <ServiceTask3
        URL = "https://<%= sHost %>/service/html/Radio.asp">
    </ServiceTask3>
    <Navigate
        BaseURL = "https://<%= sHost %>/service/html/navigate.asp?myloc<%= sLocale %>">
    </Navigate>
</ServiceInfo>
```



O código de exemplo anterior usa o ASP para recuperar o nome do host do servidor Web e criar dinamicamente as URLs no documento. O código também recupera o parâmetro *de* cadeia de caracteres de consulta de localidade da solicitação ServiceInfo e o anexa à URL da página de navegação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Informações comuns às lojas online do tipo 1 e do tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Navegação para lojas online do tipo 2**](navigation-for-type-2-online-stores.md)
</dt> <dt>

[**Documento ServiceInfo para um armazenamento online do tipo 1**](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo para uma loja online do tipo 2**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




