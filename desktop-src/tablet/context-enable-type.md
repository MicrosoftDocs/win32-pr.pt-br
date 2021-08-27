---
description: Indica se as mensagens de contexto devem ser enviadas para o procedimento de janela da janela de propriedade.
ms.assetid: 57ecf10a-8a02-4353-b916-9080ebc0b270
title: CONTEXT_ENABLE_TYPE enumeração
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONTEXT_ENABLE_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 94bffba211f75416ccae5e9a55342441b7b11b41b1a9f1f4b085ec190f991645
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110966"
---
# <a name="context_enable_type-enumeration"></a>\_ENUMERAÇÃO CONTEXT ENABLE \_ TYPE

Indica se as mensagens de contexto devem ser enviadas para o procedimento de janela da janela de propriedade.

## <a name="syntax"></a>Syntax


```C++
typedef enum _CONTEXT_ENABLE_TYPE { 
  CONTEXT_ENABLE   = 1,
  CONTEXT_DISABLE  = 2
} CONTEXT_ENABLE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**CONTEXT \_ ENABLE**
</dt> <dd>

O contexto do tablet deve ser habilitado, resultando em mensagens de contexto enviadas para o procedimento de janela da janela de propriedade.

</dd> <dt>

<span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**CONTEXT \_ DISABLE**
</dt> <dd>

O contexto do tablet deve ser desabilitado, impedindo que outras mensagens de contexto sejam enviadas para o procedimento de janela ou o sink de eventos da janela de propriedade.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método ITablet::CreateContext**](itablet-createcontext.md)
</dt> </dl>

 

 




