---
title: Co-Branding Online Stores
description: Co-Branding Online Stores
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Windows Media Player online, co-identidade visual
- lojas online, co-identidade visual
- tipo 1 lojas online, co-identidade visual
- tipo 2 lojas online, co-identidade visual
- lojas online de co-identidade visual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db3ca69c377a7aedeb71f05008d707fab955f02bf0e02d7b0ca35861105aade1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342127"
---
# <a name="co-branding-online-stores"></a>Co-Branding Online Stores

Os OEMs de computador pessoal que não operam uma loja de música podem fazer a identidade visual com provedores de lojas online. Windows Media Player configuração dá suporte ao parâmetro de linha de comando ServiceExtra para habilitar os OEMs de hardware para definir um atributo personalizado que o armazenamento online pode usar para identificar qual OEM instalou o armazenamento online inicial.

Por exemplo, se um criador de computadores chamado Fabrikam quiser definir a loja online inicial para a loja de música Proseware, ele poderá usar a seguinte linha de comando para instalar o Windows Media Player 10:


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



Quando Windows Media Player é instalado dessa maneira, o Player anexa a cadeia de caracteres ServiceExtra sempre que abre o serviço Proseware. O exemplo a seguir mostra a URL que Windows Media Player enviaria ao serviço Proseware para recuperar o documento ServiceInfo:


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



Em seguida, o proseware online store pode usar a cadeia de caracteres de consulta para determinar qual OEM instalou o Windows Media Player e retornar um documento ServiceInfo gerado dinamicamente que aponta para a versão da marca da loja online.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Informações comuns às lojas online do tipo 1 e do tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Configurar parâmetros de linha de comando para lojas online**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




