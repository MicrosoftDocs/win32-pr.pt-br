---
title: Propriedade pluginname do ItsPubPlugin
description: Recupera o nome do plug-in.
ms.assetid: c1ea46b6-fac6-4140-a278-cb04ee9af739
ms.tgt_platform: multiple
keywords:
- Propriedade pluginname Serviços de Área de Trabalho Remota
- Propriedade pluginname Serviços de Área de Trabalho Remota, interface ItsPubPlugin
- Serviços de Área de Trabalho Remota de interface ItsPubPlugin, Propriedade pluginname
topic_type:
- apiref
api_name:
- ItsPubPlugin.pluginName
- ItsPubPlugin.get_pluginName
api_location:
- Cpubplugin.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa1cd3103e901255a6226db3e128e81bb17c02e6b586a48ca434ed44932861c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128635"
---
# <a name="itspubpluginpluginname-property"></a>ItsPubPlugin: Propriedade luginName de:p

Recupera o nome do plug-in.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_pluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para uma variável **BSTR** para receber o nome do plug-in.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                         |
| INSERI<br/>                      | <dl> <dt>Cpubplugin. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ItsPubPlugin**](/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin)
</dt> </dl>

 

 





