---
description: Um provedor de alto desempenho WMI aumenta muito a velocidade com que um cliente WMI pode obter informações de um provedor de instância WMI.
ms.assetid: 767a16bb-44b6-4c56-b79b-23241fcc216e
ms.tgt_platform: multiple
title: Melhorando a eficiência de um provedor de instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55d166cdc4817068363eec899a010c778b4fa125fbfb4eda11b2745558886be4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318810"
---
# <a name="improving-the-efficiency-of-an-instance-provider"></a>Melhorando a eficiência de um provedor de instância

Um provedor de alto desempenho WMI aumenta muito a velocidade com que um cliente WMI pode obter informações de um provedor de instância WMI. A principal alteração é que um provedor de alto desempenho é executado como um servidor em processo para o aplicativo cliente ou para o WMI. Ao colocar o provedor dentro do processo do cliente, você pode acelerar a interação entre os dois.

Para obter mais informações sobre como tornar seu provedor de instâncias um provedor de alto desempenho, consulte Making [an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md).

 

 



