---
description: Outra maneira de criar um namespace é usar a API do WMI para criar o namespace de forma programática.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Criando um namespace com a API do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53054837157df5edea90657f8b68c87b394b6d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105815471"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a>Criando um namespace com a API do WMI

Outra maneira de criar um namespace é usar a API do WMI para criar o namespace de forma programática. A vantagem de criar um namespace de forma programática é que você pode criar o namespace de dentro de um aplicativo. No entanto, o uso da API do WMI é mais complexo do que usar o código formato MOF (MOF) e não é possível compartilhar facilmente seus namespaces com outros desenvolvedores.

O procedimento a seguir descreve como criar um namespace usando a API do WMI.

**Para criar um namespace usando a API do WMI**

1.  Use [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) para recuperar um ponteiro para um objeto [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que aponta para a classe de sistema de [**\_ \_ namespace**](--namespace.md) .
2.  Defina uma instância da classe de sistema de [**\_ \_ namespace**](--namespace.md) com uma chamada para [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).
3.  Defina a propriedade **Name** da instância do [**\_ \_ namespace**](--namespace.md) com uma chamada para [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).
4.  Crie o namespace com uma chamada para [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).

    O parâmetro *Pins* de [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) deve apontar para a nova instância.

 

 



