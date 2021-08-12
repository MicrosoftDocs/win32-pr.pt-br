---
description: A interface ITablet3 habilita a consulta multitoque para entrada.
ms.assetid: 949f2d83-7761-4d60-b8fe-5a9ac7567238
title: Interface ITablet3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b774ab5626d1eab5d8f4179b27924686fed56661fb776039a65ff40b3b64ebba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449839"
---
# <a name="itablet3-interface"></a>Interface ITablet3

A interface ITablet3 habilita a consulta multitoque para entrada.

## <a name="members"></a>Membros

A interface **ITablet3** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITablet3** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **interface ITablet3** tem esses métodos.



| Método                                                  | Descrição                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetMaximumCursors**](itablet3-getmaximumcursors.md) | Recupera o número máximo de entradas com suporte.<br/>        |
| [**isMultiTouch**](itablet3-ismultitouch.md)           | Indica se o multitouch está habilitado para este objeto.<br/> |



 

## <a name="remarks"></a>Comentários

Os desenvolvedores não devem usar essa interface

O código a seguir descreve como a interface **ITablet3** é definida.

``` syntax
[
  object,
  uuid(AC0E3951-0A2F-448E-88D0-49DA0C453460)
  pointer_default(unique)
]
interface ITablet3 : IUnknown
{
    HRESULT IsMultiTouch([out] BOOL *pIsMultiTouch);

    HRESULT GetMaximumCursors([out] ULONG *pMaximumCursors);
};
  
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

