---
description: A API de localização define os tipos de enumeração a seguir.
ms.assetid: a1d9d274-2861-4818-8fa1-d8d66edf27b3
title: Estruturas e tipos de enumeração (API de localização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a73c27cb2ad6dc0dcd0c2b92f4e9ba52e98fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766255"
---
# <a name="structures-and-enumeration-types-location-api"></a>Estruturas e tipos de enumeração (API de localização)

\[A API de localização Win32 está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) . \]

A API de localização define os tipos de enumeração a seguir.



| Enumeração                                                                       | Descrição                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**\_precisão desejada do local \_**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))                  | Define os tipos de precisão desejados possíveis.                         |
| [**\_status do relatório de localização \_**](/windows/win32/api/locationapi/ne-locationapi-location_report_status) | Define o status possível para novos relatórios de um determinado tipo de relatório. |



 

## <a name="location-constants-from-the-sensor-api"></a>Constantes de localização da API do sensor

A API do sensor também define as chaves de propriedade e constantes relacionadas à localização. As chaves de propriedade definidas em sensores. h podem ser usadas para recuperar dados de localização de um relatório chamando [**ILocationReport:: GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).

 

 
