---
description: Define métodos que manipulam os eventos da interface ITablet.
ms.assetid: 9acf32fa-b33f-4b9a-be73-804b7d5434e8
title: Interface ITabletEventSink
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: a1a773f7b4e08a718c419de2d51c0ff3bd9bba551267188b12889b9ec99d4ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716452"
---
# <a name="itableteventsink-interface"></a>Interface ITabletEventSink

Define métodos que manipulam os eventos da [**interface ITablet**](itablet.md) .

## <a name="members"></a>Membros

A interface **ITabletEventSink** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITabletEventSink** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITabletEventSink** tem esses métodos.



| Método                                                        | Descrição                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**ContextCreate**](itableteventsink-contextcreate.md)       | Ocorre quando um novo contexto do Tablet é criado.<br/>                                          |
| [**ContextDestroy**](itableteventsink-contextdestroy.md)     | Ocorre quando um contexto do Tablet está sendo destruído.<br/>                                      |
| [**CursorDown**](itableteventsink-cursordown.md)             | Ocorre quando a dica da caneta entra em contato com a superfície do Tablet de digitalização.<br/>                    |
| [**CursorInRange**](itableteventsink-cursorinrange.md)       | Ocorre quando uma caneta entra dentro do intervalo de detecção do digitalizador.<br/>                 |
| [**CursorMove**](itableteventsink-cursormove.md)             | Ocorre quando o cursor se move sobre o digitalizador digitalizador.<br/>                               |
| [**CursorNew**](itableteventsink-cursornew.md)               | Ocorre quando uma nova caneta é adicionada ao sistema.<br/>                                      |
| [**CursorOutOfRange**](itableteventsink-cursoroutofrange.md) | Ocorre quando a caneta deixa o intervalo de detecção física (proximidade) do Tablet.<br/> |
| [**CursorUp**](itableteventsink-cursorup.md)                 | Ocorre quando o usuário dispara a caneta da superfície digitalizadora do Tablet.<br/>         |
| [**Pacotes**](itableteventsink-packets.md)                   | Ocorre quando a caneta está sendo movida no digitalizador.<br/>                                    |
| [**SystemEvent**](itableteventsink-systemevent.md)           | Ocorre quando um evento do sistema está disponível.<br/>                                              |



 

## <a name="remarks"></a>Comentários

Os desenvolvedores não devem usar essa interface.

O código a seguir mostra como a interface **ITabletEventSink** é definida.

``` syntax
[
    object,
    uuid(788459C8-26C8-4666-BF57-04AD3A0A5EB5),
    pointer_default(unique)
]
interface ITabletEventSink: IUnknown
{

    HRESULT ContextCreate(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT ContextDestroy(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT CursorNew(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorInRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorOutOfRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorDown(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT CursorUp(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT Packets(
        [in] TABLET_CONTEXT_ID tcid,
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE * pbPkts,
        [in, unique, size_is(cPkts)
#ifndef NT_TARGET_XP
         ,disable_consistency_check
#endif
        ] ULONG *pnSerialNumbers,
        [in] CURSOR_ID cid
    );

    HRESULT SystemEvent(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] SYSTEM_EVENT event,
        [in] SYSTEM_EVENT_DATA eventdata
    );
};

     
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

