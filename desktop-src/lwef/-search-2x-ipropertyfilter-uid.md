---
title: Propriedade UID IPropertyFilter (WdsSharedIDL. h)
description: UID da propriedade a ser filtrada.
ms.assetid: a9dfb34c-a161-4d5f-8d01-695b2f9346e6
keywords:
- Propriedade UID recursos de ambiente herdados do Windows
- Propriedade UID recursos de ambiente herdados do Windows, interface IPropertyFilter
- Recursos do ambiente Windows herdado da interface IPropertyFilter, Propriedade UID
topic_type:
- apiref
api_name:
- IPropertyFilter.UID
- IPropertyFilter.get_UID
- IPropertyFilter.put_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529f3f9142345705b9e14cabd2a46200d62fe2ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295828"
---
# <a name="ipropertyfilteruid-property"></a>Propriedade IPropertyFilter:: UID

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

UID da propriedade a ser filtrada.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_UID(
  [in]          long uid
);

HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a>Valor da propriedade

Define a propriedade UID.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| parâmetro<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





