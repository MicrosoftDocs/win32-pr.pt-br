---
description: Esta seção lista os parâmetros usados para QoS (qualidade de serviço).
ms.assetid: befbcf01-ecd2-4316-8e5e-889e918272cc
title: Parâmetro de qualidade de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700b44f054f8a23631ac51fe96b06eff21645101
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811698"
---
# <a name="quality-of-service-parameter"></a><span data-ttu-id="51d09-103">Parâmetro de qualidade de serviço</span><span class="sxs-lookup"><span data-stu-id="51d09-103">Quality of Service Parameter</span></span>

<span data-ttu-id="51d09-104">Esta seção lista os parâmetros usados para QoS (qualidade de serviço).</span><span class="sxs-lookup"><span data-stu-id="51d09-104">This section lists the parameters used for quality of service (QoS).</span></span>

``` syntax
#include <windows.h>
/* 
 *  values used for the QOSClassForward and QOSClassBackward
 *  field in struct ATM_QOS_CLASS_IE
 */
#define QOS_CLASS0                  0x00
#define QOS_CLASS1                  0x01
#define QOS_CLASS2                  0x02
#define QOS_CLASS3                  0x03
#define QOS_CLASS4                  0x04

typedef struct {
    UCHAR QOSClassForward;
    UCHAR QOSClassBackward;
} ATM_QOS_CLASS_IE;
```

 

 



