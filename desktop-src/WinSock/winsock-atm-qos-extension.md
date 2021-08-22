---
description: Esta seção descreve a estrutura QOS (Qualidade de Serviço) específica do protocolo para ATM, que está contida no campo ProviderSpecific da estrutura QOS.
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Extensão de QoS do Winsock ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422db2df8e4f845086120814f6cf4e6288dcc00c42693eac8da21c466448aaa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612816"
---
# <a name="winsock-atm-qos-extension"></a>Extensão de QoS do Winsock ATM

Esta seção descreve a estrutura [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)(Qualidade de Serviço) específica do protocolo para o ATM, que está contida no campo [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) da estrutura **QOS.** Observe que o uso dessa estrutura **QOS** específica do ATM é opcional pelos clientes do Windows Sockets 2 e o provedor de serviços do ATM é necessário para mapear a estrutura [**genérica FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) para os elementos de informações Q.2931 apropriados. No entanto, se a estrutura **genérica FLOWSPEC** e a estrutura QOS específica do **ATM** são especificadas, o valor especificado na estrutura QOS específica do **ATM** deve ter precedência caso haja conflitos. Consulte Windows especificação da API sockets 2 seção 2.7 para obter mais informações sobre provisionamentos de QoS e **estrutura FLOWSPEC.**

A estrutura [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) específica do protocolo para ATM é uma concatenação de estruturas de IE (elemento de informações) Q.2931, que são definidas no texto a seguir. Se um aplicativo omitir um IE que o UNI 3.x ordena, o provedor de serviços deverá inserir um valor padrão razoável, levando em conta as informações na estrutura [**FLOWSPEC,**](/windows/win32/api/qos/ns-qos-flowspec) se aplicável.

A manipulação de E/S repetidas depende do próprio IE. Se um IE for repetido e tiver permissão para ser repetido de acordo com a especificação UNI do Fórum do ATM, o provedor deverá lidar com ele corretamente. Nesse caso, a ordem na lista determina a ordem de preferência, com elementos que aparecem anteriormente na lista sendo mais preferenciais. Se um IE for repetido e isso não for permitido por especificação UNI do Fórum do ATM, o provedor poderá falhar na solicitação do cliente (a opção preferencial) ou usar o último IE desse tipo encontrado.

Cada estrutura de IE individual é formatada da seguinte maneira e identificada pelo **campo IEType:**

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

Os valores legais para **o campo IEType** são definidos como:

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

O campo **IE** é sobreposição por uma estrutura de IE específica e o campo **IELength** é o comprimento total em bytes da estrutura do IE, incluindo os campos **IEType** e **IELength.** A semântica e os valores legais para cada elemento dessas estruturas de IE são por especificação UNI 3.x do ATM. SAP FIELD ABSENT pode ser usado para os elementos que são opcionais para uma determinada estrutura \_ \_ de IE, de acordo com a especificação UNI 3.x do ATM.

 

 
