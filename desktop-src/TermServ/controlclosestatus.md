---
title: Enumeração ControlCloseStatus
description: Indica se o aplicativo que contém o controle pode fechar o controle imediatamente.
ms.assetid: ac2e1c68-81b1-4b51-aa7e-0ff703e619a2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de enumeração ControlCloseStatus
topic_type:
- apiref
api_name:
- ControlCloseStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b94e0ce5cd040a2ade970f566897d2eac339dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918082"
---
# <a name="controlclosestatus-enumeration"></a>Enumeração ControlCloseStatus

Indica se o aplicativo que contém o controle pode fechar o controle imediatamente.

## <a name="syntax"></a>Syntax


```C++
enum ControlCloseStatus {
  controlCloseCanProceed     = 0x0000, 
  controlCloseWaitForEvents  = 0x0001 

};
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed**
</dt> <dd>

O contêiner pode prosseguir com o próximo imediatamente. Isso pode acontecer se o controle não estiver conectado.

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**
</dt> <dd>

O contêiner deve aguardar eventos [**IMsTscAxEvents:: OnDisconnect**](imstscaxevents-ondisconnected.md) ou [**IMsTscAxEvents:: OnConfirmClose**](imstscaxevents-onconfirmclose.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                      |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md)
</dt> <dt>

[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[**IMsTscAxEvents:: ondisconnectd**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





