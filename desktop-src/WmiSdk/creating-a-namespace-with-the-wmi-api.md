---
description: Outra maneira de criar um namespace é usar a API WMI para criar o namespace programaticamente.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Criando um namespace com a API WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8192bb38b60c3d0ddefb8cc1e5cb7b5f78cb0f5ba7937d39784729e0f61f70b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612536"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a>Criando um namespace com a API WMI

Outra maneira de criar um namespace é usar a API WMI para criar o namespace programaticamente. A vantagem de criar um namespace programaticamente é que você pode criar o namespace de dentro de um aplicativo. No entanto, o uso da API WMI é mais complexo do que usar um código MOF (Managed Object Format) e você não pode compartilhar seus namespaces com outros desenvolvedores com facilidade.

O procedimento a seguir descreve como criar um namespace usando a API WMI.

**Para criar um namespace usando a API WMI**

1.  Use [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) para recuperar um ponteiro para um objeto [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que aponta para a [**\_ \_ classe do sistema namespace.**](--namespace.md)
2.  Defina uma instância da [**\_ \_ classe de sistema Namespace**](--namespace.md) com uma chamada para [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).
3.  De **definir** a propriedade Name da [**\_ \_ instância do Namespace**](--namespace.md) com uma chamada para [**IWbemClassObject::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).
4.  Crie o namespace com uma chamada para [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).

    O *parâmetro pInst* de [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) deve apontar para a nova instância.

 

 



