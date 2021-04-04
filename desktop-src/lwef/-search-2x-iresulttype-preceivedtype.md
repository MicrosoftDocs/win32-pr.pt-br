---
title: Propriedade IResultType PreceivedType (WdsSharedIDL. h)
description: Essa propriedade contém a cadeia de caracteres usada para identificar o tipo no índice.
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- Recursos do ambiente Windows herdado da propriedade PreceivedType
- Propriedade PreceivedType recursos de ambiente do Windows herdados, interface IResultType
- Recursos do ambiente Windows herdado da interface IResultType, Propriedade PreceivedType
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b058105af254403c3b733f484d7c49a9ac5a0da3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824308"
---
# <a name="iresulttypepreceivedtype-property"></a>IResultType::P Propriedade ReceivedType

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Essa propriedade contém a cadeia de caracteres usada para identificar o tipo no índice.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valor da propriedade

Retorna o endereço da cadeia de caracteres identifyint o tipo no índice.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| parâmetro<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





