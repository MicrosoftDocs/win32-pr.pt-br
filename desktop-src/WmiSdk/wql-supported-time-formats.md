---
description: Descreve os formatos de tempo com suporte para uso na cláusula WHERE do WQL.
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: Formatos de hora WQL-Supported
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b84d9e37de3529060dc3da6277b2cfb40f7cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812035"
---
# <a name="wql-supported-time-formats"></a>Formatos de hora WQL-Supported

Além do formato de data e hora do WMI, os seguintes formatos de datas têm suporte para uso na cláusula WHERE do WQL.



| Formatar                                    | Descrição                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HH \[ \] {AP} M<br/>                   | Hora, conforme mostrado em um relógio de doze horas e na designação AM ou PM.<br/> 4 PM<br/>                                                                                                             |
| hh:mm<br/>                          | Hora e minutos delimitados por dois-pontos. Nenhuma designação AM ou PM.<br/> 3:23<br/>                                                                                                                  |
| hh: mm \[ \] {AP} M<br/>                | Hora e minutos delimitados por dois-pontos, espaço opcional e designação AM ou PM.<br/> 3:23 AM<br/>                                                                                              |
| hh:mm:ss<br/>                       | Hora delimitada por dois-pontos, minutos e segundos. Nenhuma designação AM/PM.<br/> 3:23:00<br/>                                                                                                         |
| hh: mm: SS \[ \] {AP} M<br/>             | Hora delimitada por dois-pontos, minutos e segundos, espaço opcional e designação AM/PM.<br/> 3:23:13H<br/>                                                                                      |
| hh: mm: SS: uuu<br/>                   | Hora delimitada por dois-pontos, minutos e segundos e deslocamento de três dígitos que indica o número de minutos que o fuso horário de origem desvia do UTC.<br/>                                    |
| hh: mm: SS: u \[ \[ \] u \] u<br/>           | Hora delimitada por dois-pontos, minutos e segundos; e um deslocamento de um, dois ou três dígitos que indica o número de minutos que o fuso horário de origem desvia do UTC.<br/>                       |
| hh: mm: SS: uuu \[ \] {AP} M<br/>         | Hora delimitada por dois-pontos, minutos e segundos, deslocamento de três dígitos que indica o número de minutos que o fuso horário de origem desvia do UTC e a designação AM ou PM.<br/>              |
| hh: mm: SS: u u u \[ \[ \] \] \[ \] {AP} M<br/> | Hora delimitada por dois-pontos, minutos e segundos; um deslocamento de um, dois ou três dígitos que indica o número de minutos que o fuso horário de origem desvia do UTC; e a designação AM ou PM.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cláusula WHERE](where-clause.md)
</dt> </dl>

 

 




