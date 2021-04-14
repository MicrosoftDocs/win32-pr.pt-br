---
title: Método de inicialização IRDVTaskPlugin
description: Chamado para inicializar o agente de tarefa.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método Initialize
- Método Initialize Serviços de Área de Trabalho Remota, interface IRDVTaskPlugin
- Serviços de Área de Trabalho Remota de interface IRDVTaskPlugin, método Initialize
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9530be7334e1f3fefa7f73007334e448362a95ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369365"
---
# <a name="irdvtaskplugininitialize-method"></a>Método IRDVTaskPlugin:: Initialize

Chamado para inicializar o agente de tarefa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNotifySink* \[ no\]
</dt> <dd>

Tipo: **[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md) \** _

Um ponteiro para uma interface [_ *IRDVTaskPluginNotifySink* *](irdvtaskpluginnotifysink.md) que o agente de tarefa usa para se comunicar com o agente de gatilho. Você deve liberar essa interface quando ela não for mais necessária.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





