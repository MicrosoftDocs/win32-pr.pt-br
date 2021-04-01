---
title: Monikers
description: Um moniker no COM não é apenas uma maneira de identificar um objeto \ 8212; um moniker também é implementado como um objeto.
ms.assetid: ae0cd2f3-8ac0-4388-8781-e86fc4a26b3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf148d63611b5252eec9f5f5f69eacbcece8c65f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004951"
---
# <a name="monikers"></a>Monikers

Um moniker no COM não é apenas uma maneira de identificar um objeto — um moniker também é implementado como um objeto. Esse objeto fornece serviços que permitem que um componente obtenha um ponteiro para o objeto identificado pelo moniker. Esse processo é conhecido como *Associação*.

Os monikers são objetos que implementam a interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) e geralmente são implementados em DLLs como objetos de componente. Há duas maneiras de exibir o uso de monikers: como um cliente moniker, um componente que usa um moniker para obter um ponteiro para outro objeto; e como um provedor de moniker, um componente que fornece monikers que identificam seus objetos para clientes de moniker.

O OLE usa monikers para se conectar e ativar objetos, estejam eles no mesmo computador ou em uma rede. Um uso muito importante é para conexões de rede. Eles também são usados para identificar, conectar e executar objetos de link de documento OLE composto. Nesse caso, a origem do link atua como o provedor do moniker e o contêiner que contém o objeto de link atua como o cliente do moniker.

Para mais informações, consulte os seguintes tópicos:

-   [Clientes de moniker](moniker-clients.md)
-   [Provedores de moniker](moniker-providers.md)
-   [Implementações de moniker OLE](ole-moniker-implementations.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O Component Object Model](the-component-object-model.md)
</dt> </dl>

 

 




