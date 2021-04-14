---
description: Além de classes e instâncias, o WMI permite que você modifique um método. O principal motivo para você querer modificar um método é se você alterou a implementação de um método em um provedor. Para obter mais informações, consulte escrevendo um provedor de método.
ms.assetid: 239a994f-ecaf-4558-9626-8f5e60dd350c
ms.tgt_platform: multiple
title: Modificando um método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93009891deec8651599f73f14a73f83bba8ffd4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370555"
---
# <a name="modifying-a-method"></a>Modificando um método

Além de classes e instâncias, o WMI permite que você modifique um método. O principal motivo para você querer modificar um método é se você alterou a implementação de um método em um provedor. Para obter mais informações, consulte [escrevendo um provedor de método](writing-a-method-provider.md).

Modificar um método não é uma operação que possa ser feita no script.

O procedimento a seguir descreve como modificar um método programaticamente.

**Para modificar um método programaticamente**

1.  Recupere a definição de classe com uma chamada para [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).

    Os dois parâmetros de saída, *ppInSignature* e *ppOutSignature*, contêm a classe in-Parameter e a classe out-Parameter, respectivamente. O valor de retorno é agrupado na classe out-Parameter como uma propriedade e deve ser chamado **ReturnValue**.

2.  Recupere e modifique os parâmetros com chamadas para [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)ou [**IWbemClassObject::D xcluir**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).
3.  Coloque a nova versão do método novamente na classe pai com uma chamada para [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).

 

 



