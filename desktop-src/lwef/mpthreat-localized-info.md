---
title: estrutura MPTHREAT_LOCALIZED_INFO (MpClient.h)
description: Informações localizadas para uma ameaça.
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- MPTHREAT_LOCALIZED_INFO estrutura herdada Windows recursos de ambiente
- PMPTHREAT_LOCALIZED_INFO de estrutura herdada Windows recursos de ambiente
topic_type:
- apiref
api_name:
- MPTHREAT_LOCALIZED_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff28c77c60421fcaabe31580400ad87823ad3edf3536d96ba3ba5eec177ad94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555946"
---
# <a name="mpthreat_localized_info-structure"></a>Estrutura MPTHREAT \_ LOCALIZED \_ INFO

Informações localizadas para uma ameaça.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPTHREAT_LOCALIZED_INFO {
  MPTHREAT_ID           ThreatID;
  MP_MIDL_STRING LPWSTR CategoryName;
  MP_MIDL_STRING LPWSTR CategoryDescription;
  MP_MIDL_STRING LPWSTR SeverityName;
  MP_MIDL_STRING LPWSTR SeverityDescription;
  MP_MIDL_STRING LPWSTR ShortDescription;
  MP_MIDL_STRING LPWSTR DefaultActionName;;
  MP_MIDL_STRING LPWSTR Advice;
  MP_MIDL_STRING LPWSTR ThreatUrl;
} MPTHREAT_LOCALIZED_INFO, *PMPTHREAT_LOCALIZED_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**ThreatID**
</dt> <dd>

Tipo: **\_ ID MPTHREAT**

</dd> <dd>

Identificador de ameaça. O bit superior é definido para identificar ameaças relacionadas ao antivírus.

</dd> <dt>

**Categoryname**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Classificação de ameaças, como um troia ou um keylogger.

</dd> <dt>

**CategoryDescription**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Descrição da categoria de ameaça.

</dd> <dt>

**SeverityName**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Nível de gravidade da ameaça, como grave ou moderado.

</dd> <dt>

**SeverityDescription**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Descrição do nível de gravidade da ameaça.

</dd> <dt>

**Shortdescription**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Breve descrição da ameaça.

</dd> <dt>

**DefaultActionName;**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Nome da ação padrão, como remover ou colocar em quarentena, sugerido pelo mecanismo.

</dd> <dt>

**Conselho**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Conselhos para a ameaça específica.

</dd> <dt>

**ThreatUrl**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Uma URL para uma página da Web que contém informações sobre a ameaça.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





