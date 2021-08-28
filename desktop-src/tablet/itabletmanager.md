---
description: Fornece acesso a todos os tablets anexados ao computador.
ms.assetid: d0fd9a6f-93fe-43d6-97fd-fee45854dfa1
title: Interface ITabletManager
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: ae4a12964ff900d8a30c0f59d2210c82007995337a2661a6fbd29a6acdfccdf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820516"
---
# <a name="itabletmanager-interface"></a>Interface ITabletManager

Fornece acesso a todos os tablets anexados ao computador.

## <a name="members"></a>Membros

A interface **ITabletManager** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITabletManager** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITabletManager** tem esses métodos.



| Método                                                  | Descrição                                                        |
|:--------------------------------------------------------|:-------------------------------------------------------------------|
| [**GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))           | Recupera o objeto de tablet especificado.<br/>                  |
| [**GetTabletCount**](itabletmanager-gettabletcount.md) | Recupera o número de tablets anexados ao sistema.<br/> |



 

## <a name="remarks"></a>Comentários

Os desenvolvedores não devem usar essa interface.

O código a seguir mostra como a interface **ITabletManager** é implementada.

``` syntax
[
    object,
    uuid(764DE8AA-1867-47C1-8F6A-122445ABD89A),
    pointer_default(unique)
]
interface ITabletManager : IUnknown
{
    HRESULT GetDefaultTablet(
        [out] ITablet **ppTablet);

    HRESULT GetTabletCount(
        [out] ULONG *pcTablets);

    HRESULT GetTablet(
        [in] ULONG iTablet,
        [out] ITablet **ppTablet);

    HRESULT GetTabletContextById(
        [in] TABLET_CONTEXT_ID tcid,
        [out] ITabletContext **ppContext);

    HRESULT GetCursorById(
        [in] CURSOR_ID cid,
        [out] ITabletCursor **ppCursor);
};
        
        
```

Chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) com uma ID de classe de CLSID TabletManagerS e, em seguida, chame QueryInterface para obter um ponteiro para \_ a **interface ITabletManager**. [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) O GUID do \_ TabletManagerS clSID é definido da seguinte forma:

``` syntax
#define CLSID_TabletManagerS uuid(A5B020FD-E04B-4e67-B65A-E7DEED25B2CF)
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

