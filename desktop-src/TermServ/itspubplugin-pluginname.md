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
ms.openlocfilehash: 97f5aa6ff6659047e9be48fd7b7a41f652c5cfd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757932"
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

 

 





