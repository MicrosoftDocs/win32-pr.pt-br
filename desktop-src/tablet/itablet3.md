---
description: A interface ITablet3 permite a consulta multitoque para entrada.
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
ms.openlocfilehash: f37d70888ccedf0fe941f0387c064aba37dc287e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766503"
---
# <a name="itablet3-interface"></a>Interface ITablet3

A interface ITablet3 permite a consulta multitoque para entrada.

## <a name="members"></a>Membros

A interface **ITablet3** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITablet3** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITablet3** tem esses métodos.



| Método                                                  | Descrição                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetMaximumCursors**](itablet3-getmaximumcursors.md) | Recupera o número máximo de entradas com suporte.<br/>        |
| [**isMultiTouch**](itablet3-ismultitouch.md)           | Indica se o multitoque está habilitado para este objeto.<br/> |



 

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

