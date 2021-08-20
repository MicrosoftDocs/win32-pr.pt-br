---
title: Método SystemMonitor. SetLogViewRange
description: Define a data de início usada para recuperar valores de contadores dos arquivos de log.
ms.assetid: ced641d0-cf71-4826-8ff0-c05f20a71aaa
keywords:
- Método SetLogViewRange SysMon
- Método SetLogViewRange SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método SetLogViewRange
topic_type:
- apiref
api_name:
- SystemMonitor.SetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e851b32f505905309a0aaf2ed1108c16db8267d8f648a73d8b5221733f04b32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954990"
---
# <a name="systemmonitorsetlogviewrange-method"></a>Método SystemMonitor. SetLogViewRange

Define a data de início usada para recuperar valores de contadores dos arquivos de log.

## <a name="syntax"></a>Sintaxe


```VB
SystemMonitor.SetLogViewRange( _
  ByVal StartTime As Date, _
  ByVal StopTime As Date _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartTime* \[ no\]
</dt> <dd>

Data de início usada para recuperar valores de contadores dos arquivos de log.

</dd> <dt>

*StopTime* \[ no\]
</dt> <dd>

Data de término usada para recuperar valores de contadores dos arquivos de log.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O SYSMON recupera valores de contadores dos arquivos de log que se enquadram nas datas de início e parada, inclusive.

Se você não especificar uma data de início ou se definir a data de início como um valor de data que está fora do intervalo de valores de data encontrado nos arquivos de log, o SYSMON alterará o valor para o valor de data mais antigo encontrado nos arquivos de log. Se o valor inicial for maior que o valor de parada, o SYSMON alterará o valor inicial para que seja o mesmo valor que o valor de parada.

Se você não especificar um valor de parada ou definir o valor de parada como um valor de data posterior à última data contida no arquivo de log, o SYSMON alterará o valor para o valor de data mais recente encontrado nos arquivos de log. Se o valor de parada for menor que o valor de parada, o SYSMON alterará o valor de parada para o mesmo valor que o valor inicial.

Se você especificar uma data de início e de parada, deverá especificar as datas antes de definir [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md). Se você definir as datas após a definição de **SystemMonitor. DataSourceType**, somente o primeiro valor do contador será recuperado do arquivo de log.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.GetLogViewRange**](systemmonitor-getlogviewrange.md)
</dt> </dl>

 

 





