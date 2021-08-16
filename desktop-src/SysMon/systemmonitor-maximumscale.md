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
ms.openlocfilehash: 176ebab3b2879b3d158310ec61fa9e65df45f8b502029ede1c58c2c1dd33f225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882025"
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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.MinimumScale**](systemmonitor-minimumscale.md)
</dt> <dt>

[**SystemMonitor.ShowScaleLabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





