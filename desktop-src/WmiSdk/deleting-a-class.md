---
description: Ao contrário da exclusão de uma instância dinâmica, a exclusão de uma classe é um procedimento simples.
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: Excluindo uma classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad3e44292aa1ca6b534151a82f36df50802e04db788d8cfb8aaeb477c23164f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412086"
---
# <a name="deleting-a-class"></a>Excluindo uma classe

Ao contrário da exclusão de uma instância dinâmica, a exclusão de uma classe é um procedimento simples. No entanto, conforme discutido anteriormente, as classes base ou derivada raramente são excluídas. Em vez disso, uma instância é mais comumente excluída. A [API de Script para WMI](scripting-api-for-wmi.md) usa os mesmos métodos para excluir um objeto de classe ou uma instância. Para obter mais informações, consulte [Excluindo uma instância](deleting-an-instance.md). Para obter informações sobre como remover classes e instâncias do repositório WMI, consulte o [**comando pragma deleteclass**](pragma-deleteclass.md) preprocessor.

A [API COM para WMI](com-api-for-wmi.md) tem métodos diferentes para excluir uma instância e excluir um objeto .

O procedimento a seguir descreve como excluir uma classe base ou classe derivada.

**Para excluir uma classe base ou classe derivada**

-   Chame o [**método IWbemServices::D eleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) ou [**IWbemServices::D eleteClassAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync)

    Como o nome sugere, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) exclui uma instância de forma assíncrona, enquanto [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) exclui uma instância de forma síncrona. Para usar **DeleteClassAsync**, você também deve implementar um [**objeto IWbemObjectSink.**](iwbemobjectsink.md)

> [!Note]  
> Como o retorno de chamada para o sink pode não ser retornado no mesmo nível de autenticação que o cliente exige, é recomendável que você use a comunicação síncrona em vez de assíncrona. Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

 

 

 



