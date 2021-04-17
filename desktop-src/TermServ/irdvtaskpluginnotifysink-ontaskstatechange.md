---
title: Método IRDVTaskPluginNotifySink OnTaskStateChange
description: Usado para notificar o agente de disparo de que o estado de uma tarefa foi alterado.
ms.assetid: 3021ea7a-2627-48d1-8df5-c40e7a9b51c5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnTaskStateChange
- Método OnTaskStateChange Serviços de Área de Trabalho Remota, interface IRDVTaskPluginNotifySink
- Serviços de Área de Trabalho Remota de interface IRDVTaskPluginNotifySink, método OnTaskStateChange
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTaskStateChange
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3e3acf1a2d47b1721ef90554f7a11714c02e6df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811908"
---
# <a name="irdvtaskpluginnotifysinkontaskstatechange-method"></a>Método IRDVTaskPluginNotifySink:: OnTaskStateChange

Usado para notificar o agente de disparo de que o estado de uma tarefa foi alterado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnTaskStateChange(
  [in] BSTR            bstrIdentifier,
  [in] RDV_TASK_STATUS status
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrIdentifier* \[ no\]
</dt> <dd>

Tipo: **BSTR**

O identificador da tarefa. Este é o identificador passado para o método [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> <dt>

*status* \[ do no\]
</dt> <dd>

Tipo: **[ **RDV \_ \_ status da tarefa**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**

Um valor da enumeração [**de \_ \_ status da tarefa RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que especifica o novo estado da tarefa.

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

[**\_status da tarefa RDV \_**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)
</dt> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





