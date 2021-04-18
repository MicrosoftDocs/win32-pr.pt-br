---
description: A exclusão de uma instância é o comando de exclusão mais comum que você provavelmente executará no WMI.
ms.assetid: 95ba3e9c-1397-41fe-a080-c03a98aafd42
ms.tgt_platform: multiple
title: Excluindo uma instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2229889ec4bc21ad234eb1636f264977bb3e25e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789321"
---
# <a name="deleting-an-instance"></a>Excluindo uma instância

A exclusão de uma instância é o comando de exclusão mais comum que você provavelmente executará no WMI. Como excluir uma classe, o comando real é bem simples. No entanto, o WMI é executado de forma muito diferente, dependendo do tipo de instância que você está excluindo. Se a instância for estática, o WMI simplesmente excluirá a instância do repositório do WMI. Para obter informações sobre como remover classes e instâncias do repositório do WMI, consulte o comando de pré-processador do [**pragma DeleteClass**](pragma-deleteclass.md) .

Se a instância for dinâmica, o WMI deverá chamar [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) nos provedores responsáveis pelas seguintes classes:

-   A classe que possui a instância.
-   Todas as classes pai da classe que possui a instância.
-   Todas as subclasses da classe que possui a instância.

O sucesso da exclusão depende da classe não abstrata mais alta para a instância original. Se o provedor de qualquer classe não abstrata mais alta for concluído com sucesso ao concluir a exclusão, a operação terá sucesso. Para obter mais informações, consulte a seção comentários de [**IWbemServices::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).

A [API com para WMI](com-api-for-wmi.md) tem métodos diferentes para excluir uma instância e excluir um objeto.

O procedimento a seguir descreve como usar o C++ para excluir uma instância de uma classe base ou classe derivada.

**Para excluir uma instância de uma classe base ou classe derivada usando C++**

-   Chame os métodos [**IWbemServices::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) ou [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) .

    Como o nome sugere, [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) exclui uma instância assincronamente enquanto [**deleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) exclui uma instância de forma síncrona. Para usar o **DeleteInstanceAsync**, você também deve implementar um objeto [**IWbemObjectSink**](iwbemobjectsink.md) .

> [!Note]  
> Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

 

A [API de script para WMI](scripting-api-for-wmi.md) usa os mesmos métodos para excluir um objeto de classe ou uma instância.

O procedimento a seguir descreve como usar o VBScript para excluir uma instância de uma classe base ou classe derivada.

**Para excluir uma instância de uma classe base ou classe derivada usando o VBScript**

-   Chame os métodos [**SWbemObject. Delete \_**](swbemobject-delete-.md) ou [**SWbemObject. DeleteAsync \_**](swbemobject-deleteasync-.md) .

    Como o nome sugere, [**delete \_**](swbemobject-delete-.md) exclui uma instância de forma síncrona enquanto [**DeleteAsync \_**](swbemobject-deleteasync-.md) exclui uma instância de maneira assíncrona. Para obter mais informações sobre como excluir uma instância de forma assíncrona, consulte [chamando um método](calling-a-method.md).

    O exemplo a seguir descreve como excluir uma instância usando o VBScript.

    ```VB
    Dim service

    Set service = GetObject("winmgmts:{impersonationLevel=impersonate}") 

    Set objwbemobject= service.get("")

    objwbemobject.Path_.Class = "MyNewClass" 
    objwbemobject.put_
    service.delete  "MyNewClass"
    ```

    

> [!Note]  
> Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

 

 

 



