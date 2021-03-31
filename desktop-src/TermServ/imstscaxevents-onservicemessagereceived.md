---
title: Método IMsTscAxEvents OnServiceMessageReceived
description: Chamado quando o cliente recebe uma mensagem do sistema.
ms.assetid: 9D230AA3-30F8-4BDF-89D6-D33AF42D0E85
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnServiceMessageReceived
- Método OnServiceMessageReceived Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnServiceMessageReceived
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnServiceMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a26b78fa31667fb550848d4edd7918aa2bde3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644797"
---
# <a name="imstscaxeventsonservicemessagereceived-method"></a>Método IMsTscAxEvents:: OnServiceMessageReceived

Chamado quando o cliente recebe uma mensagem do sistema.

## <a name="syntax"></a>Sintaxe


```C++
void OnServiceMessageReceived(
  [in] BSTR serviceMessage
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mensagens* \[ no\]
</dt> <dd>

Especifica a mensagem do sistema.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre mensagens do sistema, consulte [Configurar mensagens para um servidor Gateway área de trabalho remota](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                      |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

