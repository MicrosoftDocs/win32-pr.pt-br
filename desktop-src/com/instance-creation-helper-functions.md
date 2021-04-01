---
title: Funções auxiliares de criação de instância
description: Funções auxiliares de criação de instância
ms.assetid: 0b9b7bcf-f0f0-42c4-945e-63a532640d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84956f6040aaba13b46dea92bea611a49d5d8de3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008411"
---
# <a name="instance-creation-helper-functions"></a>Funções auxiliares de criação de instância

Nas versões anteriores do COM, o mecanismo primário usado para criar uma instância de objeto era a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) . Essa função encapsula o processo de criação de um objeto de classe, usando-o para criar uma nova instância e liberar o objeto de classe. Outra função desse tipo é o [**OleCreate**](/windows/desktop/api/ole/nf-ole-olecreate)mais específico, o auxiliar de documento OLE composto que cria um objeto de classe e recupera um ponteiro para um objeto solicitado.

Para suavizar o processo de criação de instâncias em sistemas distribuídos, o COM introduziu quatro novos mecanismos importantes de criação de instância:

-   Monikers de classe e [ **IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator)
-   [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)

Um moniker de classe permite que você identifique a classe de um objeto e normalmente é usado com outro moniker, como um moniker de arquivo, para indicar o local do objeto. Isso permite que você se vincule a um objeto e especifique o servidor que deve ser iniciado para esse objeto. Os monikers de classe também podem ser compostos à direita dos monikers que dão suporte à associação à interface [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) . Para obter mais informações, consulte [moniker de classe](class-monikers.md).

[**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) estende [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para tornar possível criar um único objeto não inicializado associado ao CLSID fornecido em um computador remoto especificado. Além disso, em vez de solicitar uma única interface e obter um único ponteiro para essa interface, o **CoCreateInstanceEx** torna possível consultar várias interfaces e (se disponível) receber ponteiros para elas em uma única viagem de ida e volta, permitindo, portanto, menos viagens de ida e volta entre as máquinas. Isso pode tornar a interação do objeto remoto muito mais eficiente. Para fazer isso, a função usa uma matriz de [**várias estruturas \_ QI**](/windows/win32/api/objidlbase/ns-objidlbase-multi_qi) .

A criação de um objeto por meio de [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) ainda requer que o objeto seja inicializado por meio de uma chamada para uma das interfaces de inicialização (como [**IPersistStorage:: Load**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-load)). As funções auxiliares [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) e [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) encapsulam a potência de criação de instância do **CoCreateInstanceEx** e a inicialização, a antiga de um arquivo e a última de um armazenamento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um objeto por meio de um objeto de classe](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 