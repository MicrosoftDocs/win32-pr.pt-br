---
title: Propriedade pluginname do IRDVTaskPlugin (Tspubplugincom. h)
description: Contém o nome de exibição do agente de tarefa.
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- Propriedade pluginname Serviços de Área de Trabalho Remota
- Propriedade pluginname Serviços de Área de Trabalho Remota, interface IRDVTaskPlugin
- Serviços de Área de Trabalho Remota de interface IRDVTaskPlugin, Propriedade pluginname
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.PluginName
- IRDVTaskPlugin.get_PluginName
api_location:
- tspubplugincom.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0262472e37a8ff3e5b9bb153d2e94f4e52029b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644793"
---
# <a name="irdvtaskpluginpluginname-property"></a>IRDVTaskPlugin: Propriedade luginName de:P

Contém o nome de exibição do agente de tarefa. Esse nome é usado apenas para fins de log.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_PluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor da propriedade

O nome de exibição do agente de tarefa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 Enterprise<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                           |
| parâmetro<br/>                   | <dl> <dt>Tspubplugincom. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





