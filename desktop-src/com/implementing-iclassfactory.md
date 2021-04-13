---
title: Implementando IClassFactory
description: Implementando IClassFactory
ms.assetid: 96466756-c135-4ee5-a48c-f31129878473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b057657508b3060506c15c68308ea6a5332e5099
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366741"
---
# <a name="implementing-iclassfactory"></a>Implementando IClassFactory

Quando um cliente usa um CLSID para solicitar a criação de uma instância de objeto, a primeira etapa é a criação de um objeto de classe, um objeto intermediário que contém uma implementação dos métodos da interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) . Embora o COM forneça várias funções de criação de instância, a primeira etapa na implementação dessas funções é a criação de um objeto de classe.

Como resultado, todos os servidores devem implementar os métodos da interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , que contém dois métodos:

-   [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance). Esse método deve criar uma instância não inicializada do objeto e retornar um ponteiro para uma interface solicitada no objeto.
-   [**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver). Esse método apenas incrementa a contagem de referência no objeto de classe para garantir que o servidor permaneça na memória e não seja desligado antes que o cliente esteja pronto para fazê-lo.

Para permitir que um servidor seja responsável por seu próprio licenciamento, COM define [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), que herda sua definição de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Assim, um servidor que implementa **IClassFactory2** deve, por definição, implementar os métodos de **IClassFactory**.

O COM também fornece funções auxiliares para a implementação de servidores fora do processo. Para obter mais informações, consulte [auxiliares de implementação do servidor fora do processo](out-of-process-server-implementation-helpers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Responsabilidades do servidor COM](com-server-responsibilities.md)
</dt> <dt>

[Licenciamento e IClassFactory2](licensing-and-iclassfactory2.md)
</dt> </dl>

 

 