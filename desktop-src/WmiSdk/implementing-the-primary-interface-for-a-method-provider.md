---
description: 'Um provedor de métodos deve implementar IWbemServices como a interface primária. No entanto, um provedor de método puro requer apenas que você implemente o método IWbemServices:: ExecMethodAsync.'
ms.assetid: 39466513-48f3-4bf6-a3ab-e9d2c387480c
ms.tgt_platform: multiple
title: Implementando a interface primária para um provedor de métodos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 196f87a6520d92bf18362be88f8cc40e5133dabe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764458"
---
# <a name="implementing-the-primary-interface-for-a-method-provider"></a>Implementando a interface primária para um provedor de métodos

Um provedor de métodos deve implementar [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) como a interface primária. No entanto, um provedor de método puro requer apenas que você implemente o método [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) .

Como outros provedores usam [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), a interface contém muitos métodos que são irrelevantes para um provedor de método puro. Seu provedor de método puro deve fornecer uma implementação de stub que retorne o \_ provedor WBEM E \_ \_ não \_ compatível com todos os outros métodos de **IWbemServices** além de [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync). No entanto, muitos provedores de método também servem como provedores de instância ou classe. Os provedores de método e instância de combinação devem dar suporte a mais dos métodos de **IWbemServices** .

 

 



