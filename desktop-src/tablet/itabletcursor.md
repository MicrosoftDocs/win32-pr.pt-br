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
ms.openlocfilehash: eecbebc7090fb57d3794f3d056c24fba61fa5c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837221"
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
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

