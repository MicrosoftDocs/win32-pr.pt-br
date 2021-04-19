---
title: DVD. IsAvailable
description: A propriedade IsAvailable indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada. | DVD. IsAvailable
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- DVD. isdisponível Windows Media Player
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
ms.openlocfilehash: 5088b4b6365dd60d859fda8ec563cc9c8ff8a4c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105796432"
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

Os recursos de DVD do Windows Media Player não funcionarão em computadores que não têm decodificadores de DVD de terceiros instalados. Você pode determinar se um decodificador está disponível chamando **IsAvailable**("dvdDecoder").

Cada DVD é criado de maneira diferente. Os métodos disponíveis durante a reprodução e navegação em DVD dependem de como o DVD é criado.

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| Versão<br/>                  | Windows Media Player para Windows XP ou posterior<br/>                            |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de DVD**](dvd-object.md)
</dt> </dl>

 

 





