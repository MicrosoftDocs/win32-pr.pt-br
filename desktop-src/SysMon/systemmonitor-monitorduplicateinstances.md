---
title: Propriedade SystemMonitor. MonitorDuplicateInstances
description: Recupera ou define um valor que determina se várias instâncias de um contador podem ser monitoradas.
ms.assetid: fe8d6074-eb29-4093-9f79-39e6171a3a3f
keywords:
- Propriedade MonitorDuplicateInstances SysMon
- Propriedade MonitorDuplicateInstances SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade MonitorDuplicateInstances
topic_type:
- apiref
api_name:
- SystemMonitor.MonitorDuplicateInstances
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6ae53d0a1dcf3f67a43dab7959bb42619ace6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369514"
---
# <a name="systemmonitormonitorduplicateinstances-property"></a>Propriedade SystemMonitor. MonitorDuplicateInstances

Recupera ou define um valor que determina se várias instâncias de um contador podem ser monitoradas.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property MonitorDuplicateInstances As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Verdadeiro indica que várias instâncias de um contador podem ser monitoradas (true é o padrão). False indica que apenas uma instância de um contador pode ser monitorada.

## <a name="remarks"></a>Comentários

O monitor do sistema acrescenta \# n a cada nome de instância, exceto o primeiro, se houver várias instâncias. O número de série, n, começa com um e é incrementado em um para cada nova instância. Por exemplo, se você especificar " \\ processo ( \* ) \\ % tempo do processador", a coleção do contador deverá conter várias instâncias de svchost. A primeira ocorrência será svchost, a próxima ocorrência será svchost \# 1 e assim por diante.

As instâncias duplicadas serão monitoradas apenas se você usar o caractere curinga ( \* ) para o nome da instância. Se você especificou " \\ processo (svchost) \\ % tempo do processador", somente a primeira instância encontrada de svchost será monitorada, nem todas as instâncias do svchost.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





