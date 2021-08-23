---
description: Descreve os dados de objeto do coletor de exibição incluídos em uma notificação ou resultado da notificação.
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: Estrutura de WFD_DISPLAY_SINK_OBJECT_HEADER (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: e4c9e4d83fbac1cccb2dbc0643acc707176be433dfca7854395a0f97c9c36435
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800466"
---
# <a name="wfd_display_sink_object_header-structure"></a>\_Estrutura de \_ cabeçalho de objeto do coletor de vídeo WFD \_ \_

A estrutura do **cabeçalho do objeto do \_ coletor de vídeo \_ \_ \_ WFD** descreve os dados do objeto do coletor de vídeo incluídos em uma notificação ou resultado da notificação.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WFD_DISPLAY_SINK_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Length;
} WFD_DISPLAY_SINK_OBJECT_HEADER, *PWFD_DISPLAY_SINK_OBJECT_HEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tipo**
</dt> <dd>

O tipo do objeto do coletor de vídeo. Você pode usar o **tipo de objeto do coletor de vídeo WFD do identificador \_ \_ \_ \_ \_ padrão** que é definido como o valor 1.

</dd> <dt>

**Revisão**
</dt> <dd>

A versão de revisão do objeto do coletor de vídeo. Você pode usar a **revisão de objeto do coletor de exibição WFD do identificador \_ \_ \_ \_ \_ versão \_ 1** , que é definida como o valor 1.

</dd> <dt>

**Comprimento**
</dt> <dd>

O comprimento dos dados no resultado da notificação ou da notificação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




