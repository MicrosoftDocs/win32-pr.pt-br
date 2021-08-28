---
title: Propriedade IRemoteDesktopClientTouchPointer Enabled
description: Se o recurso de ponteiro de toque está habilitado no controle de cliente do contêiner do aplicativo RDP.
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Propriedades habilitadas Serviços de Área de Trabalho Remota
- Propriedade habilitada Serviços de Área de Trabalho Remota , interface IRemoteDesktopClientTouchPointer
- Interface IRemoteDesktopClientTouchPointer Serviços de Área de Trabalho Remota , propriedade Enabled
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
ms.openlocfilehash: d7ce04e38b41fce462973606f40f0099f010e6f4ab785900039e6771b0a9aaf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124846"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a>Propriedade IRemoteDesktopClientTouchPointer::Enabled

Se o recurso de ponteiro de toque está habilitado no controle de cliente do contêiner do aplicativo RDP.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Enabled(
  [in]          VARIANT_BOOL Enabled
);

HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *Enabled
);
```



## <a name="property-value"></a>Valor da propriedade

**true** se o recurso de ponteiro de toque estiver habilitado; caso contrário, **false.**

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

 

