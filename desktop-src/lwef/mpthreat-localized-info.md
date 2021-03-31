---
title: Estrutura de MPTHREAT_LOCALIZED_INFO (MpClient. h)
description: Informações localizadas para uma ameaça.
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPTHREAT_LOCALIZED_INFO
- Ponteiro de estrutura de PMPTHREAT_LOCALIZED_INFO recursos de ambiente herdados do Windows
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
ms.openlocfilehash: 87ea0bee7c8cae15389b40b64038aad92a56dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369587"
---
# <a name="mpthreat_localized_info-structure"></a>\_Estrutura de informações localizadas do MPTHREAT \_

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

**Threatid**
</dt> <dd>

Tipo: **\_ ID de MPTHREAT**

</dd> <dd>

Identificador de ameaça. O bit superior é definido para identificar ameaças relacionadas ao antivírus.

</dd> <dt>

**CategoryName**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Classificação de ameaças, como um cavalo de Troia ou um keylogger.

</dd> <dt>

**CategoryDescription**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Descrição da categoria de ameaça.

</dd> <dt>

**Gravidadename**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Nível de severidade da ameaça, como grave ou moderado.

</dd> <dt>

**SeverityDescription**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Descrição do nível de severidade da ameaça.

</dd> <dt>

**ShortDescription**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Breve descrição da ameaça.

</dd> <dt>

**Defaultactionname;**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Nome da ação padrão, como remover ou colocar em quarentena, sugerido pelo mecanismo.

</dd> <dt>

**Aconselhamento**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Conselhos para a ameaça específica.

</dd> <dt>

**ThreatUrl**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Uma URL para uma página da Web que contém informações sobre a ameaça.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





