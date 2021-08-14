---
title: Propriedade IsUpdateNeeded de IResultsViewer (WdsView.h)
description: Isso retornará TRUE se a consulta de exibições tiver sido modificada e precisar de atualização.
ms.assetid: 68ae1f68-0585-4bc5-bea4-eb55f3626093
keywords:
- Propriedade IsUpdateNeeded herdada Windows recursos de ambiente
- Propriedade IsUpdateNeeded Legacy Windows Environment Features , interface IResultsViewer
- Interface IResultsViewer Recursos Windows ambiente herdados, propriedade IsUpdateNeeded
topic_type:
- apiref
api_name:
- IResultsViewer.IsUpdateNeeded
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c013692509ddebe5c0f6530e9abf4b17aa2c356c6eade829bdc2dbad52465f27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753877"
---
# <a name="iresultsviewerisupdateneeded-property"></a>Propriedade IResultsViewer::IsUpdateNeeded

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use a [API Windows Search.](../search/-search-reference-entry-page.md) 

Isso retornará TRUE se a consulta de exibições tiver sido modificada e precisar de atualização.

## <a name="syntax"></a>Syntax

## <a name="property-value"></a>Valor da propriedade

Quando chamado, isso retornará um ponteiro para o sinalizador de notação se a consulta tiver sido alterada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/>                                 |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com aplicativos da área de trabalho SP1 \[\]<br/>                        |
| Redistribuível<br/>          | Windows Pesquisa de Área de Trabalho (WDS) 2.6.5<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





