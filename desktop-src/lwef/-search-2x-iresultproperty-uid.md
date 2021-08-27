---
title: Propriedade UID IResultProperty (WdsSharedIDL. h)
description: Identificador exclusivo da propriedade.
ms.assetid: b5cee5b3-78b4-4d2a-b442-f6624497ef71
keywords:
- recursos de ambiente herdado de Windows da propriedade UID
- propriedade UID recursos herdados de Windows ambiente, interface IResultProperty
- IResultProperty interface herdada Windows recursos de ambiente, propriedade UID
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
ms.openlocfilehash: d413a81d6b18091d2e21b4572f5f8e01693829c17942d3e395e2c03a71d467d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754707"
---
# <a name="iresultpropertyuid-property"></a>Propriedade IResultProperty:: UID

> [!NOTE]
> Windows o Desktop Search 2. x é uma tecnologia obsoleta que estava originalmente disponível como um suplemento para o Windows XP e o Windows Server 2003. em versões posteriores, use a [API de pesquisa Windows](../search/-search-reference-entry-page.md) em vez disso. 

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
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos de área de trabalho do SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com \[ aplicativos de área de trabalho do SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Pesquisador de desktops (WDS) 2.6.5<br/>                                             |
| Cabeçalho<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





