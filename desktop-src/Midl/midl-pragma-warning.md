---
title: midl_pragma atributo de aviso
description: Use a opção de aviso de pragma de MIDL \_ para substituir temporariamente o comportamento de mensagem de aviso do MIDL no momento da compilação.
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- midl_pragma o atributo de aviso MIDL
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b7e1e2c2a1d818216245e45a9129018a3ba2e1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823172"
---
# <a name="midl_pragma-warning-attribute"></a>atributo de aviso de pragma de MIDL \_

Use a opção de **\_ aviso de pragma de MIDL** para substituir temporariamente o comportamento de mensagem de aviso do MIDL no momento da compilação.

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*opção de aviso \_* 
</dt> <dd>

A opção de aviso pode ser uma das seguintes opções: desabilitar, habilitar, padrão.

</dd> <dt>

*lista de mensagens \_* 
</dt> <dd>

Uma lista de números de mensagem separados por espaços.

</dd> </dl>

## <a name="remarks"></a>Comentários

O pragma pode ser usado como um pragma do C-Compiler. Ou seja, ele desabilita, habilita ou retorna para o comportamento padrão de um determinado aviso de MIDL.

## <a name="examples"></a>Exemplos

``` syntax
#if (__midl >= 501)
midl_pragma warning( disable: 2007 )   // file already imported midl_pragma warning( disable: 2209 )   // ignored redundant attr
#endif
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**pragma**](pragma.md)
</dt> </dl>

 

 




