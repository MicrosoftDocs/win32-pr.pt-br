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
ms.openlocfilehash: 078934c8f19085bf233df78501798a8416ceadf7ba6a0b663cb14b8a8c46b223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129327"
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
| Cabeçalho<br/>                   | <dl> <dt>Tspubplugincom. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





