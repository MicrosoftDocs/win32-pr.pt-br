---
description: Estende a interface ITablet.
ms.assetid: dd4f3b2e-7f63-4d5b-b50e-64458719c17a
title: Interface ITablet2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b402695aa278105ad57209f3ff33e66ccaf8c746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780717"
---
# <a name="itablet2-interface"></a>Interface ITablet2

Estende a [**interface ITablet**](itablet.md).

## <a name="members"></a>Membros

A interface **ITablet2** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITablet2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITablet2** tem esses métodos.



| Método                                          | Descrição                                                                                              |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**GetDeviceKind**](itablet2-getdevicekind.md) | Retorna o tipo de dispositivo de hardware que o objeto do Tablet representa, como mouse, caneta ou toque.<br/> |



 

## <a name="remarks"></a>Comentários

Essa interface foi introduzida no Windows Vista.

Os desenvolvedores não devem usar essa interface.

O código a seguir descreve como a interface **ITablet2** é definida.

``` syntax
[
    object,
    uuid(C247F616-BBEB-406A-AED3-F75E656599AE),
    pointer_default(unique)
]
interface ITablet2 : IUnknown
{
    HRESULT GetDeviceKind([out] TABLET_DEVICE_KIND *pKind);

    HRESULT GetMatchingScreenRect([out] RECT *prcInput);
};
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

