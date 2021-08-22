---
title: DVD. IsAvailable
description: A propriedade IsAvailable indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada. | DVD. IsAvailable
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- Windows Media Player de DVD. IsAvailable
topic_type:
- apiref
api_name:
- DVD.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efb1a240c8df072d0770521f70c526f4e096c26385df85cff7acf0d229fdc252
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996916"
---
# <a name="dvdisavailable"></a>DVD. IsAvailable

A propriedade **IsAvailable** indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada.

``` syntax
player.dvd.isAvailable(
        name
        )
```

## <a name="parameters"></a>Parâmetros

*name*

**Cadeia de caracteres** que contém um dos valores a seguir.



| String     | Descrição                                                                            |
|------------|----------------------------------------------------------------------------------------|
| voltar       | Determina se o método **back** está disponível.                                   |
| DVD        | Determina se o DVD está carregado.                                                  |
| dvdDecoder | Determina se o decodificador de DVD está instalado no sistema.                             |
| resume     | Determina se o método **resume** está disponível.                                 |
| titleMenu  | Determina se o método **titleMenu** está disponível.                              |
| topMenu    | Determina se o método **topMenu** está disponível. Normalmente chamado de menu raiz. |



 

## <a name="return-values"></a>Valores de retorno

Esse método retorna um **valor booleano** somente leitura que indica se o parâmetro especificado está disponível.

## <a name="remarks"></a>Comentários

os recursos de dvd do Windows Media Player não funcionarão em computadores que não têm decodificadores de DVD de terceiros instalados. Você pode determinar se um decodificador está disponível chamando **IsAvailable**("dvdDecoder").

Cada DVD é criado de maneira diferente. Os métodos disponíveis durante a reprodução e navegação em DVD dependem de como o DVD é criado.

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                               |
| Versão<br/>                  | Windows Media Player para Windows XP ou posterior<br/>                            |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de DVD**](dvd-object.md)
</dt> </dl>

 

 





