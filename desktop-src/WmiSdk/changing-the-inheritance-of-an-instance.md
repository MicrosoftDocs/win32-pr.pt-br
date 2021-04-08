---
description: Você pode encontrar uma situação em que uma instância que foi criada como um filho de uma classe pai deve alterar as classes pai e se tornar o filho de uma classe pai diferente.
ms.assetid: 6d0fd456-81ab-4665-bb88-f9fb29fbbd39
ms.tgt_platform: multiple
title: Alterando a herança de uma instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a35de3dcc37d91b318ab60fb5a520cb4da10e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828668"
---
# <a name="changing-the-inheritance-of-an-instance"></a>Alterando a herança de uma instância

Você pode encontrar uma situação em que uma instância que foi criada como um filho de uma classe pai deve alterar as classes pai e se tornar o filho de uma classe pai diferente. Por exemplo, você pode ter uma classe derivada, **ManualService**, descrevendo um serviço manual e uma classe derivada, **autoatendimento**, descrevendo um serviço automático. Ambas as classes têm um grande número de propriedades. Nem todas as propriedades são idênticas. Para alterar um serviço de manual para automático, você também deve alterar a instância que representa o serviço de **ManualService** para **autoatendimento**. Na versão atual do WMI, você não pode chamar o método [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) com o parâmetro *Pins* apontando para uma instância do **autoatendimento** e as propriedades de chave que descrevem a instância **ManualService** . Se você fizer isso, você excluirá implicitamente a instância **ManualService** original. Em essência, depois de estabelecer a classe de uma instância, você só pode alterar a classe pai de uma instância excluindo a instância e recriando a instância como uma instância da nova classe pai.

O procedimento a seguir descreve como mover uma instância de uma classe para outra classe.

**Para mover uma instância de uma classe para outra classe**

1.  Exclua a instância da classe original.
2.  Crie a instância na nova classe.

    O WMI não permite que os aplicativos movam uma instância criando-a na nova classe e, em seguida, atualizando-a com a chave da instância original.

Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).

 

 



