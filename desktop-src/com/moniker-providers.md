---
title: Provedores de moniker
description: Provedores de moniker
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde584e12daddacbc940b23b21a0386aa37de2c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635852"
---
# <a name="moniker-providers"></a>Provedores de moniker

Em geral, um componente deve ser um provedor de moniker quando ele permite acesso a um de seus objetos, enquanto ainda controla o armazenamento do objeto. Se um componente vai distribuir os identificadores de recurso que identificam seus objetos, ele deve ser capaz de executar as seguintes tarefas:

-   Quando solicitado, crie um moniker que identifique um objeto.
-   Habilite o moniker a ser associado quando um cliente chama [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) .

Um provedor de moniker deve criar um moniker de uma *classe de moniker* apropriada para identificar um objeto. A classe moniker refere-se a uma implementação específica da interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) que define o tipo de moniker criado. Embora você possa implementar **IMoniker** para criar uma nova classe de moniker, ela é frequentemente desnecessária porque o OLE fornece implementações de várias classes de moniker diferentes, cada uma com seu próprio CLSID. Consulte [implementações de moniker OLE](ole-moniker-implementations.md) para obter descrições das classes moniker que o OLE fornece.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Clientes de moniker](moniker-clients.md)
</dt> <dt>

[Implementações de moniker OLE](ole-moniker-implementations.md)
</dt> </dl>

 

 




