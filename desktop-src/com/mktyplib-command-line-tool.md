---
title: Ferramenta de Command-Line de MkTypLib
description: MkTypLib é um aplicativo de linha de comando que processa um arquivo IDL para produzir uma biblioteca de tipos. Ele também pode ser usado para gerar um arquivo de cabeçalho C ou C++.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc392351327124777c2d52d0bbe0653853dcb52
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641934"
---
# <a name="mktyplib-command-line-tool"></a>Ferramenta de Command-Line de MkTypLib

\[A ferramenta de Mktyplib.exe está obsoleta. Em vez disso, use o compilador MIDL. Se precisar de compatibilidade com versões anteriores com programas de automação antigos, use o compilador MIDL com a opção **/mktyplib203** .\]

MkTypLib é um aplicativo de linha de comando que processa um arquivo IDL para produzir uma biblioteca de tipos. Ele também pode ser usado para gerar um arquivo de cabeçalho C ou C++.

Para gerar uma biblioteca de tipos a partir de um arquivo ODL:

-   No prompt de comando, execute o seguinte comando:

    **mktyplibÂ * * * nome de arquivo*

    em que *filename* é o nome do arquivo ODL.

O MkTypLib também dá suporte a vários parâmetros opcionais. Para obter uma lista completa, execute a seguinte linha de comando:

**MkTypLib/?**

Como MkTypLib é um aplicativo obsoleto, ele não pode analisar arquivos IDL ou arquivos com interfaces definidas fora de uma instrução de [**biblioteca**](/windows/desktop/Midl/library) . Para obter mais informações, consulte [diferenças entre MIDL e MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Convertendo para C++](translating-to-c--.md)
</dt> </dl>

 

 