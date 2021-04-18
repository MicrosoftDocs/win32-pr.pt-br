---
description: Ao contrário da exclusão de uma instância dinâmica, a exclusão de uma classe é um procedimento simples.
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: Excluindo uma classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3d9ce149b5eff0f5202cb25c5f7d16fdf44291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798378"
---
# <a name="deleting-a-class"></a>Excluindo uma classe

Ao contrário da exclusão de uma instância dinâmica, a exclusão de uma classe é um procedimento simples. No entanto, conforme discutido anteriormente, as classes base ou derivadas raramente são excluídas. Em vez disso, uma instância é mais comumente excluída. A [API de script para WMI](scripting-api-for-wmi.md) usa os mesmos métodos para excluir um objeto de classe ou uma instância. Para obter mais informações, consulte [excluindo uma instância](deleting-an-instance.md). Para obter informações sobre como remover classes e instâncias do repositório do WMI, consulte o comando de pré-processador do [**pragma DeleteClass**](pragma-deleteclass.md) .

A [API com para WMI](com-api-for-wmi.md) tem métodos diferentes para excluir uma instância e excluir um objeto.

O procedimento a seguir descreve como excluir uma classe base ou classe derivada.

**Para excluir uma classe base ou classe derivada**

-   Chame o método [**IWbemServices::D eleteclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) ou [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) .

    Como o nome sugere, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) exclui uma instância assincronamente enquanto [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) exclui uma instância de forma síncrona. Para usar o **DeleteClassAsync**, você também deve implementar um objeto [**IWbemObjectSink**](iwbemobjectsink.md) .

> [!Note]  
> Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

 

 

 



