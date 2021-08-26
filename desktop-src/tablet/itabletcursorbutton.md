---
description: Representa informações gerais sobre um botão em um dispositivo de caneta.
ms.assetid: 20c9f8bb-8f8d-4469-baff-b9001c8adb3b
title: Interface ITabletCursorButton
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 76f5e581a4db81d9e260b388cc129d915121a69f3b360441e4220fd58aa0e623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938596"
---
# <a name="itabletcursorbutton-interface"></a>Interface ITabletCursorButton

Representa informações gerais sobre um botão em um dispositivo de caneta.

## <a name="members"></a>Membros

A interface **ITabletCursorButton** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITabletCursorButton** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITabletCursorButton** tem esses métodos.



| Método                                         | Descrição                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [**GetGuid**](itabletcursorbutton-getguid.md) | Recupera o identificador exclusivo do botão da caneta.<br/> |
| [**GetName**](itabletcursorbutton-getname.md) | Recupera o nome do botão da caneta.<br/>              |



 

## <a name="remarks"></a>Comentários

Os desenvolvedores não devem usar essa interface.

O código a seguir mostra como a interface **ITabletCursorButton** é definida.

``` syntax
[
    object,
    uuid(997A992E-8B6C-4945-BC17-A1EE563B3AB7),
    pointer_default(unique)
]
interface ITabletCursorButton : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetGuid(
        [out] GUID *pguidBtn);
};
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITabletCursorButton**](itabletcursorbutton.md)
</dt> </dl>

 

