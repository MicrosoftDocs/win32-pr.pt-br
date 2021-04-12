---
title: Propriedade SystemMonitor. MinimumScale
description: Recupera ou define o valor mínimo do eixo vertical (Y) do grafo.
ms.assetid: 22dacfbf-27bb-48fe-b646-4cf17645a131
keywords:
- Propriedade MinimumScale SysMon
- Propriedade MinimumScale SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade MinimumScale
topic_type:
- apiref
api_name:
- SystemMonitor.MinimumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f675e96ecdd4e547ca4a93b248556fd8c0539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455099"
---
# <a name="systemmonitorminimumscale-property"></a>Propriedade SystemMonitor. MinimumScale

Recupera ou define o valor mínimo do eixo vertical (Y) do grafo.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property MinimumScale As Long
```



## <a name="property-value"></a>Valor da propriedade

Valor mínimo positivo do eixo vertical do grafo. O valor mínimo padrão da escala vertical é 0. O valor mais alto para o qual você pode definir o valor mínimo é um valor menor que [**MaximumScale**](systemmonitor-maximumscale.md) .

## <a name="remarks"></a>Comentários

O controle ajusta automaticamente a posição dos números de escala exibidos na escala vertical de acordo com o tamanho do controle exibido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.MaximumScale**](systemmonitor-maximumscale.md)
</dt> <dt>

[**SystemMonitor.ShowScaleLabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





