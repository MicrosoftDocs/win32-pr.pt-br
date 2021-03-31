---
title: Método SystemMonitor. ScaleToFit
description: Dimensionar valores do contador para caber no grafo.
ms.assetid: 8e58e51a-4767-40da-836a-e49d34dec195
keywords:
- Método ScaleToFit SysMon
- Método ScaleToFit SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método ScaleToFit
topic_type:
- apiref
api_name:
- SystemMonitor.ScaleToFit
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1e481dd44c441ea9e2dd44f2e63a06539da74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644552"
---
# <a name="systemmonitorscaletofit-method"></a>Método SystemMonitor. ScaleToFit

Dimensionar valores do contador para caber no grafo.

## <a name="syntax"></a>Sintaxe


```VB
SystemMonitor.ScaleToFit( _
  ByVal selectedCountersOnly As Boolean _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*selectedCountersOnly* \[ no\]
</dt> <dd>

True para dimensionar apenas os contadores selecionados; caso contrário, false para dimensionar todos os contadores.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método limpará o modo de exibição de gráfico. O SYSMON usa o fator de escala especificado para cada contador para redesenhar o grafo se a fonte de dados for um arquivo de log ou começar a grafar novos valores de contador se a fonte de dados for uma atividade em tempo real.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**MYITEM. ScaleFactor**](counteritem-scalefactor.md)
</dt> <dt>

[**Coitem. selecionado**](counteritem-selected.md)
</dt> </dl>

 

 





