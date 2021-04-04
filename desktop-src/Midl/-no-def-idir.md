---
title: opção/no_def_idir
description: Quando os diretórios são especificados com a opção/I, a \_ \_ opção de Idir de alteração de mudança instrui o compilador MIDL a pesquisar somente os diretórios especificados com a opção/i.
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /no_def_idir MIDL do comutador
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62ed845c73c36fbbfe4ea7dea952ee4541b043a7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823352"
---
# <a name="no_def_idir-switch"></a>\_opção de \_ Idir def de alteração

Quando os diretórios são especificados com a opção [**/i**](-i.md) , a opção de **\_ \_ Idir de////** opções de alteração instrui o compilador MIDL a pesquisar somente os diretórios especificados com a opção **/i** , ignorando o diretório atual, bem como os diretórios especificados pela variável de ambiente INCLUDE.

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Quando nenhum diretório é especificado com a opção [**/i**](-i.md) , a opção de **\_ \_ Idir de//** chave de alteração instrui o compilador MIDL a pesquisar somente o diretório atual.

## <a name="examples"></a>Exemplos

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**/I**](-i.md)
</dt> </dl>

 

 




