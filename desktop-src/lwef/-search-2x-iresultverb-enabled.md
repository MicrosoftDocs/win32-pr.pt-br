---
title: Propriedade habilitada para IResultVerb (WdsSharedIDL. h)
description: Essa propriedade retornará TRUE se o verbo estiver habilitado.
ms.assetid: 27e3dbb8-678e-46c7-82e5-40b86cb157a7
keywords:
- recursos de ambiente herdado de Windows de propriedade habilitada
- propriedade habilitada Windows recursos de ambiente, interface IResultVerb
- IResultVerb interface herdada Windows recursos de ambiente, propriedade Enabled
topic_type:
- apiref
api_name:
- IResultVerb.Enabled
- IResultVerb.get_Enabled
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c96a4c40252bf6b5ab74d3d4ec96e2568dffeed624ae2b5126059192dd72d9e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014316"
---
# <a name="iresultverbenabled-property"></a>Propriedade IResultVerb:: Enabled

> [!NOTE]
> Windows o Desktop Search 2. x é uma tecnologia obsoleta que estava originalmente disponível como um suplemento para o Windows XP e o Windows Server 2003. em versões posteriores, use a [API de pesquisa Windows](../search/-search-reference-entry-page.md) em vez disso. 

Essa propriedade retornará TRUE se o verbo estiver habilitado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *flag
);
```



## <a name="property-value"></a>Valor da propriedade

Essa propriedade retornará true se o verbo estiver habilitado ou false se não.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos de área de trabalho do SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com \[ aplicativos de área de trabalho do SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Pesquisador de desktops (WDS) 2.6.5<br/>                                             |
| Cabeçalho<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





