---
title: Propriedade habilitada para IRemoteDesktopClientTouchPointer
description: Se o recurso de ponteiro de toque está habilitado no controle de cliente do contêiner de aplicativo RDP.
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Propriedade habilitada Serviços de Área de Trabalho Remota
- Propriedade Enabled Serviços de Área de Trabalho Remota, interface IRemoteDesktopClientTouchPointer
- Serviços de Área de Trabalho Remota de interface IRemoteDesktopClientTouchPointer, Propriedade Enabled
topic_type:
- apiref
api_name:
- IRemoteDesktopClientTouchPointer.Enabled
- IRemoteDesktopClientTouchPointer.get_Enabled
- IRemoteDesktopClientTouchPointer.put_Enabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd534a9f8ec77903f196bbdfa10e1823a18dff4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760310"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a>Propriedade IRemoteDesktopClientTouchPointer:: Enabled

Se o recurso de ponteiro de toque está habilitado no controle de cliente do contêiner de aplicativo RDP.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Enabled(
  [in]          VARIANT_BOOL Enabled
);

HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *Enabled
);
```



## <a name="property-value"></a>Valor da propriedade

**true** se o recurso de ponteiro de toque estiver habilitado; caso contrário, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                      |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>              |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>              |
| IID<br/>                      | IID \_ IRemoteDesktopClientTouchPointer é definido como 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRemoteDesktopClientTouchPointer**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer)
</dt> </dl>

 

