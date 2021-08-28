---
title: Visualizadores e ferramentas de conversão da biblioteca de tipos
description: Visualizadores e ferramentas de conversão da biblioteca de tipos
ms.assetid: 35c29e2c-3ee3-4e73-b925-6aa0ccb50a00
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1b0687769367edad4fd1c7325be943dfae74aae643789791396089cd6c6ea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309002"
---
# <a name="type-library-viewers-and-conversion-tools"></a>Visualizadores e ferramentas de conversão da biblioteca de tipos

As bibliotecas de tipos contêm a especificação de um ou mais elementos COM, incluindo classes, interfaces, enumerações e muito mais. Esses arquivos são armazenados em um formato binário padrão. Uma biblioteca de tipos pode ser um arquivo autônomo com a extensão de nome de arquivo .tlb ou pode ser armazenada como um recurso em um arquivo executável, que pode ter uma extensão de nome de arquivo .ocx, .dll ou .exe. Os visualizadores de biblioteca de tipos e as ferramentas de conversão descritos a seguir leem esse formato para obter informações sobre os elementos COM na biblioteca.

Antes de programar um objeto em uma linguagem de programação específica, você deve ser capaz de exibir sua biblioteca de tipos nessa linguagem. Isso fornece a sintaxe adequada para as classes, interfaces, métodos, propriedades e eventos do objeto COM.

Os produtos de desenvolvimento da Microsoft fornecem as seguintes ferramentas que você pode usar para gerar, extrair e exibir informações da biblioteca de tipos.

## <a name="c"></a>C++

-   [Visualizador de Objetos OLE-COM](ole-com-object-viewer.md)
-   [Compilador MIDL](midl-compiler.md)
-   [Mktyplib](mktyplib-command-line-tool.md)

## <a name="visual-basic"></a>Visual Basic

-   [Visual Basic Pesquisador de Objetos](visual-basic-object-browser.md)

## <a name="java"></a>Java

-   [Jactivex](jactivex-command-line-tool.md)
-   [Assistente de Biblioteca de Tipos Java](java-type-library-wizard.md)
-   [JavaTLB](javatlb-command-line-tool.md)

Para ter uma visão geral de como essas ferramentas interagem com bibliotecas de tipos, consulte [Como Ferramentas para Desenvolvedores usar bibliotecas de tipos](how-developer-tools-use-type-libraries.md).

 

 




