---
title: Método onterminado IRDVTaskPluginNotifySink (Sbtsv. h)
description: Chamado pelo agente de tarefa para solicitar que o agente de tarefa seja desligado.
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- Método onterminado Serviços de Área de Trabalho Remota
- Método onterminado Serviços de Área de Trabalho Remota, interface IRDVTaskPluginNotifySink
- Serviços de Área de Trabalho Remota de interface IRDVTaskPluginNotifySink, método onterminado
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
ms.openlocfilehash: 0b261437425b0b4dce4b2c2e17c52b6e24ea3e0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499760"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a>Método IRDVTaskPluginNotifySink:: onterminable

Chamado pelo agente de tarefa para solicitar que o agente de tarefa seja desligado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HR* \[ no\]
</dt> <dd>

Indica se o desligamento é devido a um desligamento normal ou uma falha. Se o desligamento for normal, isso conterá **S \_ OK**. Caso contrário, ele contém um código de erro **HRESULT** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 Enterprise<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                  |
| parâmetro<br/>                   | <dl> <dt>Sbtsv. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





