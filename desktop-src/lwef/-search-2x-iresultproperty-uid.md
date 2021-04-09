---
title: Propriedade UID IResultProperty (WdsSharedIDL. h)
description: Identificador exclusivo da propriedade.
ms.assetid: b5cee5b3-78b4-4d2a-b442-f6624497ef71
keywords:
- Propriedade UID recursos de ambiente herdados do Windows
- Propriedade UID recursos de ambiente herdados do Windows, interface IResultProperty
- Recursos do ambiente Windows herdado da interface IResultProperty, Propriedade UID
topic_type:
- apiref
api_name:
- IResultProperty.UID
- IResultProperty.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08921e366cca2be40a8a79fe43d7a15cec54f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009223"
---
# <a name="iresultpropertyuid-property"></a>Propriedade IResultProperty:: UID

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Identificador exclusivo da propriedade.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a>Valor da propriedade

Retorna um ponteiro para o identificador de propriedade exclusivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| parâmetro<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





