---
description: Esta seção descreve a estrutura de QOS (qualidade de serviço) específica do protocolo para ATM, que está contida no campo ProviderSpecific da estrutura de QOS.
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Extensão de QoS de ATM do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075c9dcbd8b9148f41d39c99e2118ed638a577ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090349"
---
# <a name="winsock-atm-qos-extension"></a>Extensão de QoS de ATM do Winsock

Esta seção descreve a estrutura de [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos)(qualidade de serviço) específica do protocolo para ATM, que está contida no campo [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) da estrutura de **QoS** . Observe que o uso dessa estrutura **QoS** específica de ATM é opcional pelos clientes do Windows Sockets 2, e o provedor de serviços ATM é necessário para mapear a estrutura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) genérica para os elementos de informações de Q. 2931 apropriados. No entanto, se a estrutura **FLOWSPEC** genérica e a estrutura **QoS** específica do ATM forem especificadas, o valor especificado na estrutura **QoS** específica do ATM deverá ter precedência caso haja conflitos. Consulte a seção especificação da API do Windows Sockets 2 2,7 para obter mais informações sobre as provisões de QoS e a estrutura **FLOWSPEC** .

A estrutura de [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) específica de protocolo para ATM é uma concatenação das estruturas do elemento de informações 2931 (IE), que são definidas no texto a seguir. Se um aplicativo omitir um IE que exige 3. x, o provedor de serviços deverá inserir um valor padrão razoável, colocando as informações na estrutura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) em conta, se aplicável.

A manipulação de s repetidas depende do próprio IE. Se um IE for repetido e for um que pode ser repetido de acordo com a especificação UNI do fórum ATM, o provedor deverá tratá-lo corretamente. Nesse caso, Order na lista determina a ordem de preferência, com elementos que aparecem anteriormente na lista sendo mais preferenciais. Se um IE for repetido e isso não for permitido por uma especificação UNI do fórum ATM, o provedor poderá falhar a solicitação do cliente (a opção preferencial) ou usar o último IE desse tipo encontrado.

Cada estrutura individual do IE é formatada da seguinte maneira e identificada pelo campo **IEType** :

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

Os valores válidos para o campo **IEType** são definidos como:

``` syntax
typedef enum {
    IE_AALParameters,
    IE_TrafficDescriptor,
    IE_BroadbandBearerCapability,
    IE_BHLI,
    IE_BLLI,
    IE_CalledPartyNumber,
    IE_CalledPartySubaddress,
    IE_CallingPartyNumber,
    IE_CallingPartySubaddress,
    IE_Cause,
    IE_QOSClass,
    IE_TransitNetworkSelection,
} Q2931_IE_TYPE;
```

O campo do **IE** é sobreposto por uma estrutura específica do IE e o campo **IELength** é o comprimento total em bytes da estrutura do IE, incluindo os campos **IEType** e **IELength** . A semântica e os valores válidos para cada elemento dessas estruturas do IE são por especificação UNI 3. x de ATM. \_O campo SAP \_ ausente pode ser usado para esses elementos opcionais para uma determinada estrutura do IE, por especificação uni 3. x de ATM.

 

 
