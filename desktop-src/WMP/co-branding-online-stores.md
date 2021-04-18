---
title: Co-Branding lojas online
description: Co-Branding lojas online
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Lojas online do Windows Media Player, co-marca
- lojas online, co-marca
- Digite 1 lojas online, co-marca
- Digite 2 lojas online, co-marca
- lojas online de co-identidade visual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cae110d3ed04e864f1b617cb4fd6fcdee3b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788183"
---
# <a name="co-branding-online-stores"></a>Co-Branding lojas online

Os OEMs de computadores pessoais que não operam uma loja de música podem comarcações com provedores de loja online. A instalação do Windows Media Player dá suporte ao parâmetro de linha de comando do netextra para permitir que os OEMs de hardware definam um atributo personalizado que pode ser usado pela loja online para identificar qual OEM instalou o armazenamento online inicial.

Por exemplo, se um criador de computadores chamado Fabrikam quiser definir a loja online inicial para a loja de músicas da Proseware, ele poderá usar a seguinte linha de comando para instalar o Windows Media Player 10:


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



Quando o Windows Media Player é instalado dessa maneira, o Player acrescenta a cadeia de caracteres de todos os minutos sempre que abre o serviço de Proseware. O exemplo a seguir mostra a URL que o Windows Media Player enviaria ao serviço de Proseware para recuperar o documento do ServiceInfo:


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



A loja online da Proseware pode usar a cadeia de caracteres de consulta para determinar qual OEM instalou o Windows Media Player e retornar um documento do serviceInfo gerado dinamicamente que aponta para a versão de marca da loja online.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Parâmetros de linha de comando de instalação para lojas online**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




