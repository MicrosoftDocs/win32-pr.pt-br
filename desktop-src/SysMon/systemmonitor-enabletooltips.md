---
title: Propriedade SystemMonitor. EnableToolTips
description: Recupera ou define um valor que determina se uma dica de ferramenta é mostrada quando o mouse passa sobre um contador em uma das exibições de gráfico (sem suporte para a exibição de relatório).
ms.assetid: af9a78ea-a9de-4343-8978-4316769a5f30
keywords:
- Propriedade EnableToolTips SysMon
- Propriedade EnableToolTips SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, Propriedade EnableToolTips
topic_type:
- apiref
api_name:
- SystemMonitor.EnableToolTips
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 757cdd8a54bf6e5ae6e70b82dfc30865c796f944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756531"
---
# <a name="systemmonitorenabletooltips-property"></a>Propriedade SystemMonitor. EnableToolTips

Recupera ou define um valor que determina se uma dica de ferramenta é mostrada quando o mouse passa sobre um contador em uma das exibições de gráfico (sem suporte para a exibição de relatório).

## <a name="syntax"></a>Syntax


```VB
Property EnableToolTips As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Verdadeiro exibe uma dica de ferramenta com as informações do contador; caso contrário, false.

## <a name="remarks"></a>Comentários

Para grafos de linha, a dica de ferramenta é ancorada ao ponto de dados mais próximo do mouse. Para gráficos de barras e histogramas, a dica de ferramenta representa o valor total de dados da barra, não um ponto dentro da barra.

A dica de ferramenta contém informações diferentes com base na fonte de dados. Para arquivos de log, a dica de ferramenta contém o caminho do contador, o valor do contador, o carimbo de data/hora, o número de amostras de dados incluídas no ponto de dados e os valores mínimo e máximo de dados.

Para a atividade em tempo real, a dica de ferramenta contém o caminho do contador, o valor do contador e o carimbo de data/hora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





