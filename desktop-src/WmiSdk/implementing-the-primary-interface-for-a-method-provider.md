---
description: Um provedor de métodos deve implementar IWbemServices como a interface primária. No entanto, um provedor de método puro requer apenas que você implemente o método IWbemServices::ExecMethodAsync.
ms.assetid: 39466513-48f3-4bf6-a3ab-e9d2c387480c
ms.tgt_platform: multiple
title: Implementando a interface primária para um provedor de método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fcc698155ad0a9e786636045654b08d1cd2b7dfabd946b2d3ee9e8192485
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244226"
---
# <a name="implementing-the-primary-interface-for-a-method-provider"></a>Implementando a interface primária para um provedor de método

Um provedor de métodos deve implementar [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) como a interface primária. No entanto, um provedor de método puro requer apenas que você implemente o [**método IWbemServices::ExecMethodAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)

Como outros provedores usam [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), a interface contém muitos métodos irrelevantes para um provedor de método puro. Seu provedor de método puro deve fornecer uma implementação de stub que retorna WBEM E PROVIDER NOT CAPABLE para todos os outros métodos \_ \_ \_ \_ **IWbemServices** além [**de ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync). No entanto, muitos provedores de método também servem como provedores de instância ou classe. O método de combinação e os provedores de instância devem dar suporte a mais **dos métodos IWbemServices.**

 

 



