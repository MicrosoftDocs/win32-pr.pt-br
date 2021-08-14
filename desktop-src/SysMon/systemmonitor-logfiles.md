---
title: Propriedade SystemMonitor. LogFiles
description: Coleção de um ou mais arquivos de log a serem usados como a origem dos valores do contador exibidos no monitor do sistema.
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- Propriedade LogFiles SysMon
- Propriedade LogFiles SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, Propriedade LogFiles
topic_type:
- apiref
api_name:
- SystemMonitor.LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed0ea39809d3dfe40ebcedf2fbf2105833af836c12b95ffdfe442d3956d52a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882176"
---
# <a name="systemmonitorlogfiles-property"></a>Propriedade SystemMonitor. LogFiles

Coleção de um ou mais arquivos de log a serem usados como a origem dos valores do contador exibidos no monitor do sistema.

## <a name="syntax"></a>Syntax


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a>Valor da propriedade

Coleção de objetos [**LogFileItem**](logfileitem.md) que especificam os arquivos de log usados como a fonte de dados para o grafo.

## <a name="remarks"></a>Comentários

Para adicionar ou remover um arquivo de log da coleção de arquivos de log, o valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) não deve ser definido como sysmonLogFiles.

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

[**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)
</dt> <dt>

[**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md)
</dt> <dt>

[**SystemMonitor.SqlLogSetName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





