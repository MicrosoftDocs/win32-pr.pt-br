---
title: Ferramenta de Command-Line de MkTypLib
description: MkTypLib é um aplicativo de linha de comando que processa um arquivo IDL para produzir uma biblioteca de tipos. Ele também pode ser usado para gerar um arquivo de cabeçalho C ou C++.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b712ed8220dd609dd3ba189bdac6b5ee11d2805f26ff5a1f146c20f17c1f8ab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047934"
---
# <a name="mktyplib-command-line-tool"></a>Ferramenta de Command-Line de MkTypLib

\[A ferramenta de Mktyplib.exe está obsoleta. Em vez disso, use o compilador MIDL. Se precisar de compatibilidade com versões anteriores com programas de automação antigos, use o compilador MIDL com a opção **/mktyplib203** .\]

MkTypLib é um aplicativo de linha de comando que processa um arquivo IDL para produzir uma biblioteca de tipos. Ele também pode ser usado para gerar um arquivo de cabeçalho C ou C++.

Para gerar uma biblioteca de tipos a partir de um arquivo ODL:

-   No prompt de comando, execute o seguinte comando:

    * * mktyplibÂ * *_nome do arquivo_

    em que *filename* é o nome do arquivo ODL.

O MkTypLib também dá suporte a vários parâmetros opcionais. Para obter uma lista completa, execute a seguinte linha de comando:

**MkTypLib/?**

Como MkTypLib é um aplicativo obsoleto, ele não pode analisar arquivos IDL ou arquivos com interfaces definidas fora de uma instrução de [**biblioteca**](/windows/desktop/Midl/library) . Para obter mais informações, consulte [diferenças entre MIDL e MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Convertendo para C++](translating-to-c--.md)
</dt> </dl>

 

 