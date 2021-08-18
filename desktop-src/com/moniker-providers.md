---
title: Provedores de moniker
description: Provedores de moniker
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8fab6c5a84d7020b8bcb02979471cb2fbd76df7e66fc9909eec2121926827df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130098"
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

 

 




