---
title: Documento do serviceInfo para uma loja online tipo 1
description: Documento do serviceInfo para uma loja online tipo 1
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Windows Media Player repositórios online, documento do serviceinfo
- repositórios online, documento do serviceInfo
- Digite 1 lojas online, documento do serviceInfo
- Documento do serviceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893cb3c849e062147d0f6bc80f3f9c1bd56a3457b60dfe30ce837820091e9710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995436"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a>Documento do serviceInfo para uma loja online tipo 1

As lojas online do tipo 1 devem fornecer à Microsoft a URL de um documento XML que descreve a loja online. o Windows Media Player 11 usa este documento para determinar como configurar a interface do usuário para hospedar o repositório online.

O documento do serviceInfo para um repositório tipo 1 fornece as seguintes informações para Windows Media Player:

-   Informações usadas para configurar o botão **lojas online** (também chamado de guia), como o texto do botão, a cor do botão e a dica de ferramenta do botão.
-   URLs para imagens que Windows Media Player exibe para identificar a loja online.
-   URLs de páginas da web, fornecidas pela loja online, que Windows Media Player hospeda em sua interface do usuário.
-   URL em que Windows Media Player pode recuperar o plug-in do repositório online para que o plug-in possa ser instalado no computador do usuário.

quando Windows Media Player recupera o documento serviceinfo da Web, ele anexa uma cadeia de caracteres de consulta à URL. A cadeia de caracteres de consulta contém parâmetros que fornecem informações sobre a localidade e a localização geográfica do usuário e a versão do Windows Media Player.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o tipo 1 lojas online**](about-type-1-online-stores.md)
</dt> <dt>

[**Criando o documento do serviceInfo dinamicamente**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Documento de informações de exemplo para uma loja online tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento do serviceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




