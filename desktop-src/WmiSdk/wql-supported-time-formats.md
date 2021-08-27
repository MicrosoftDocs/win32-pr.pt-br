---
description: Descreve os formatos de hora com suporte para uso na cláusula WHERE do WQL.
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: WQL-Supported de tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 627b46ef7d01a2eb3e8e40484b37822c9ebca55a9487b1ffb0e1a138ab7378d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049734"
---
# <a name="wql-supported-time-formats"></a>WQL-Supported de tempo

Além do formato DATETIME do WMI, há suporte para os formatos de data a seguir para uso na cláusula WHERE do WQL.



| Formatar                                    | Descrição                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| hh \[ \] {AP}M<br/>                   | Hora, conforme mostrado em um relógio de doze horas, e designação AM ou PM.<br/> 4 PM<br/>                                                                                                             |
| hh:mm<br/>                          | Hora e minutos delimitados por dois-pontos. Nenhuma designação AM ou PM.<br/> 3:23<br/>                                                                                                                  |
| hh:mm \[ \] {AP}M<br/>                | Hora e minutos delimitados por dois-pontos, espaço opcional e designação AM ou PM.<br/> 3h23<br/>                                                                                              |
| hh:mm:ss<br/>                       | Hora, minutos e segundos delimitados por dois-pontos. Nenhuma designação AM/PM.<br/> 3:23:00<br/>                                                                                                         |
| hh:mm:ss \[ \] {AP}M<br/>             | Hora delimitada por dois-pontos, minutos e segundos, espaço opcional e designação AM/PM.<br/> 15:23:00<br/>                                                                                      |
| hh:mm:ss:uuu<br/>                   | Hora delimitada por dois-pontos, minutos e segundos e deslocamento de três dígitos que indica o número de minutos que o fuso horário de origem desvia de UTC.<br/>                                    |
| hh:mm:ss: \[ \[ u u u \] \] u<br/>           | Hora, minutos e segundos delimitados por dois-pontos; e um, dois ou três dígitos de deslocamento que indica o número de minutos que o fuso horário de origem desvia de UTC.<br/>                       |
| hh:mm:ss:uuu \[ \] {AP}M<br/>         | Hora delimitada por dois-pontos, minutos e segundos, deslocamento de três dígitos que indica o número de minutos que o fuso horário de origem desvia de UTC e designação AM ou PM.<br/>              |
| hh:mm:ss: \[ \[ u u u \] \] \[ \] {AP}M<br/> | Hora, minutos e segundos delimitados por dois-pontos; deslocamento de um, dois ou três dígitos que indica o número de minutos que o fuso horário de origem desvia de UTC; e designação AM ou PM.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cláusula WHERE](where-clause.md)
</dt> </dl>

 

 




