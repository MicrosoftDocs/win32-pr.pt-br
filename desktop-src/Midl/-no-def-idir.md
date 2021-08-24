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
ms.openlocfilehash: 8c93d61bff28ad0aa4306047755c88419d0b925431f9b3ea476ec957dcd62b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811296"
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

 

 




