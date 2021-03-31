---
title: Propriedade SystemMonitor. MaximumScale
description: Recupera ou define o valor máximo do eixo vertical (Y) do grafo.
ms.assetid: 305886e3-2586-47c7-a888-6e393580c456
keywords:
- Propriedade MaximumScale SysMon
- Propriedade MaximumScale SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriedade MaximumScale
topic_type:
- apiref
api_name:
- SystemMonitor.MaximumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37740802fac4d89bbcbe9d5c105e357b55ab481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918316"
---
# <a name="systemmonitormaximumscale-property"></a>Propriedade SystemMonitor. MaximumScale

Recupera ou define o valor máximo do eixo vertical (Y) do grafo.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property MaximumScale As Long
```



## <a name="property-value"></a>Valor da propriedade

Valor máximo positivo do eixo vertical do grafo. O valor máximo padrão da escala vertical é 100. O menor valor para o qual você pode definir o valor máximo é mais do que o valor de [**MinimumScale**](systemmonitor-minimumscale.md) . O valor mais alto para o qual você pode definir o valor máximo é 999.999.999.

## <a name="remarks"></a>Comentários

O controle ajusta automaticamente a posição dos números de escala exibidos na escala vertical de acordo com o tamanho do controle exibido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.MinimumScale**](systemmonitor-minimumscale.md)
</dt> <dt>

[**SystemMonitor.ShowScaleLabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





