---
title: opção/sal_local
description: O \_ comutador local/sal DIRECIONA MIDL para gerar também anotações sal para parâmetros de métodos de interface marcados como \ local \. A opção/sal também deve estar presente.
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- /sal_local MIDL do comutador
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03263b94b809407d1c3e55c2f3dacc5e10684bc1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105759065"
---
# <a name="sal_local-switch"></a>\_comutador local/sal

O comutador **\_ local/sal** direciona MIDL para gerar também anotações sal para parâmetros de métodos de interface marcados como [**\[ \] local**](local.md). A opção [**/sal**](-sal.md) também deve estar presente.

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Modifica o comportamento da opção [**/sal**](-sal.md) para também fornecer anotações sobre os parâmetros dos métodos de interface marcados com o atributo [**\[ local \]**](local.md) . Use o atributo [**\[ anotar \]**](annotate.md)para substituir a anotação gerada por MIDL por uma cadeia de caracteres de anotação diferente.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal**](-sal.md)
</dt> <dt>

[**\[anotar\]**](annotate.md)
</dt> </dl>

 

 




