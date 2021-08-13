---
description: Representa um objeto de caneta.
ms.assetid: c55945b7-59df-49b5-b25f-fa96056889fc
title: Interface ITabletCursor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 83a24329b318ec2bb542a3bbb63a28d4db9fce877b99f75aa7091670825fa439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716934"
---
# <a name="itabletcursor-interface"></a>Interface ITabletCursor

Representa um objeto de caneta.

## <a name="members"></a>Membros

A interface **ITabletCursor** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITabletCursor** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITabletCursor** tem esses métodos.



| Método                                                 | Descrição                                                            |
|:-------------------------------------------------------|:-----------------------------------------------------------------------|
| [**Getbutton**](itabletcursor-getbutton.md)           | Recupera o objeto de botão especificado de uma caneta digitalizadora.<br/> |
| [**GetButtonCount**](itabletcursor-getbuttoncount.md) | Recupera o número de botões na caneta digitalizadora.<br/>       |
| [**GetId**](itabletcursor-getid.md)                   | Recupera o identificador da caneta.<br/>                            |
| [**GetName**](itabletcursor-getname.md)               | Recupera o nome da caneta digitalizadora.<br/>                    |
| [**Isverted**](itabletcursor-isinverted.md)         | Indica se a caneta está de cabeça para baixo.<br/>                     |



 

## <a name="remarks"></a>Comentários

Não use essa interface.

O código a seguir descreve como a interface **ITabletCursor** é definida.

``` syntax
[
    object,
    uuid(EF9953C6-B472-4B02-9D22-D0E247ADE0E8,
    pointer_default(unique)
]
interface ITabletCursor : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT IsInverted();

    HRESULT GetId(
        [out] CURSOR_ID *pCid);

    HRESULT GetTablet(
        [out] ITablet **ppTablet);

    HRESULT GetButtonCount(
        [out] ULONG *pcButtons);

    HRESULT GetButton(
        [in] ULONG iButton,
        [out] ITabletCursorButton **ppButton);
};

     
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

