---
title: Método OnTerminated IRDVTaskPluginNotifySink (Sbtsv.h)
description: Chamado pelo agente de tarefa para solicitar que o agente de tarefa seja desligado.
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- Método OnTerminated Serviços de Área de Trabalho Remota
- Método OnTerminated Serviços de Área de Trabalho Remota , interface IRDVTaskPluginNotifySink
- Interface IRDVTaskPluginNotifySink Serviços de Área de Trabalho Remota , método OnTerminated
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTerminated
api_location:
- sbtsv.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29ab2a3e8ddea5999b6d63322dbeb9fca07983e591e849f22a3e98e27c67609a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129128"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a>Método IRDVTaskPluginNotifySink::OnTerminated

Chamado pelo agente de tarefa para solicitar que o agente de tarefa seja desligado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hr* \[ Em\]
</dt> <dd>

Indica se o desligar é devido a um desligado normal ou uma falha. Se o desligado for normal, ele conterá **S \_ OK.** Caso contrário, ele conterá um **código de erro HRESULT.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 Enterprise<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                  |
| Cabeçalho<br/>                   | <dl> <dt>Sbtsv.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





