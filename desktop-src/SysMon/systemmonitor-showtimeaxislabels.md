---
title: Propriedade SystemMonitor. ShowTimeAxisLabels
description: Recupera ou define um valor que determina se o eixo horizontal (X) da exibição de gráfico contém rótulos.
ms.assetid: 9e9d2d2c-f053-4afe-85de-25242842498f
keywords:
- Propriedade ShowTimeAxisLabels SysMon
- Propriedade ShowTimeAxisLabels SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, Propriedade ShowTimeAxisLabels
topic_type:
- apiref
api_name:
- SystemMonitor.ShowTimeAxisLabels
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06569dcd4702ae687b09bfae88c84482a49afb71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749185"
---
# <a name="systemmonitorshowtimeaxislabels-property"></a>Propriedade SystemMonitor. ShowTimeAxisLabels

Recupera ou define um valor que determina se o eixo horizontal (X) da exibição de gráfico contém rótulos.

## <a name="syntax"></a>Syntax


```VB
Property ShowTimeAxisLabels As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Um valor true aplicará rótulos ao eixo x. Um valor false não será. O padrão é False.

## <a name="remarks"></a>Comentários

O SYSMON ignora essa propriedade para gráficos de barras, relatórios e histogramas.

Para grafos de linha, o SYSMON usa a hora em que o valor do contador foi amostrado como o rótulo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





