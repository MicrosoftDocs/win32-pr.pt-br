---
title: Método IRDVTaskPlugin Initialize
description: Chamado para inicializar o agente de tarefa.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Inicializar o método Serviços de Área de Trabalho Remota
- Inicializar a interface Serviços de Área de Trabalho Remota , IRDVTaskPlugin
- Interface IRDVTaskPlugin Serviços de Área de Trabalho Remota , método Initialize
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14f4a002a0b33e403c02dba74385edd21e211fb27bcfb144c7a9ddc080a40fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606099"
---
# <a name="irdvtaskplugininitialize-method"></a>Método IRDVTaskPlugin::Initialize

Chamado para inicializar o agente de tarefa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNotifySink* \[ Em\]
</dt> <dd>

Tipo: **[ **IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)\***

Um ponteiro para uma interface [**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md) que o agente de tarefa usa para se comunicar com o agente de gatilho. Você deve liberar essa interface quando ela não for mais necessária.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





