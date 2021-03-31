---
title: Propriedade DisplayName IResultProperty (WdsSharedIDL. h)
description: Nome de exibição localizado da propriedade.
ms.assetid: 8f9e118a-9e92-4919-afe1-735c61af38f7
keywords:
- Propriedade DisplayName recursos de ambiente do Windows herdados
- Propriedade DisplayName recursos de ambiente do Windows herdados, interface IResultProperty
- Recursos do ambiente Windows herdado da interface IResultProperty, Propriedade DisplayName
topic_type:
- apiref
api_name:
- IResultProperty.DisplayName
- IResultProperty.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f36aa934d2ddf31d841478cef1cb9a33b0531224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085847"
---
# <a name="iresultpropertydisplayname-property"></a>IResultProperty::D Propriedade isplayname

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Nome de exibição localizado da propriedade.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valor da propriedade

Retorna um ponteiro para o nome de exibição localizado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| parâmetro<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





