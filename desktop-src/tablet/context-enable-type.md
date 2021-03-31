---
description: Indica se as mensagens de contexto devem ser enviadas para o procedimento de janela da janela de propriedade.
ms.assetid: 57ecf10a-8a02-4353-b916-9080ebc0b270
title: Enumeração de CONTEXT_ENABLE_TYPE
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
ms.openlocfilehash: cd741eeff1cc3e2ce055a84dd646c3aa2563f217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662940"
---
# <a name="context_enable_type-enumeration"></a>\_Enumeração de tipo de habilitação de contexto \_

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

<span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**\_habilitação de contexto**
</dt> <dd>

O contexto do Tablet deve ser habilitado, o que resulta em mensagens de contexto sendo enviadas para o procedimento de janela da janela de propriedade.

</dd> <dt>

<span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**\_desabilitar contexto**
</dt> <dd>

O contexto do Tablet deve ser desabilitado, impedindo que outras mensagens de contexto sejam enviadas para o procedimento de janela da janela de propriedade ou coletor de eventos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método ITablet:: CreateContext**](itablet-createcontext.md)
</dt> </dl>

 

 




