---
title: Co-Branding lojas online
description: Co-Branding lojas online
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Windows Media Player lojas online, co-marca
- lojas online, co-marca
- Digite 1 lojas online, co-marca
- Digite 2 lojas online, co-marca
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
# <a name="co-branding-online-stores"></a>Co-Branding lojas online

Os OEMs de computadores pessoais que não operam uma loja de música podem comarcações com provedores de loja online. Windows Media Player instalação dá suporte ao parâmetro de linha de comando do imextra para permitir que os OEMs de hardware definam um atributo personalizado que pode ser usado pelo armazenamento online para identificar qual OEM instalou o armazenamento online inicial.

por exemplo, se um criador de computadores chamado Fabrikam quiser definir a loja online inicial para a loja de músicas da proseware, ele poderá usar a seguinte linha de comando para instalar o Windows Media Player 10:


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



quando Windows Media Player é instalado dessa maneira, o Player acrescenta a cadeia de caracteres de todos os minutos sempre que abre o serviço de proseware. o exemplo a seguir mostra a URL que Windows Media Player enviaria ao serviço de proseware para recuperar o documento do serviceinfo:


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



a loja online da proseware pode usar a cadeia de caracteres de consulta para determinar qual OEM instalado Windows Media Player e retornar um documento do serviceinfo gerado dinamicamente que aponta para a versão de marca da loja online.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Parâmetros de linha de comando de instalação para lojas online**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




