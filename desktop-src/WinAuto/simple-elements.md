---
title: Elementos simples
description: Um elemento simples é um elemento de interface do usuário que compartilha um objeto IAccessible com outros elementos e se baseia nesse objeto IAccessible (normalmente seu pai) para expor suas propriedades.
ms.assetid: 3f6bd992-4e0a-4dba-b6e9-e70dca77c880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9676b8bf4198f8be753b3788fcc6defdec2d6a1d8ad3ff3fed2f41da4f256554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133639"
---
# <a name="simple-elements"></a>Elementos simples

Um *elemento simples* é um elemento de interface do usuário que compartilha um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) com outros elementos e se baseia nesse objeto **IAccessible** (normalmente seu pai) para expor suas propriedades. Para diferenciar entre os elementos que compartilham um objeto **IAccessible** , o servidor atribui um identificador filho positivo exclusivo a cada elemento simples. Essa atribuição é feita em uma base por instância de interface, portanto, as IDs devem ser exclusivas dentro desse contexto. Muitas implementações atribuem essas IDs sequencialmente, começando com 1. Esse esquema não permite que elementos simples tenham filhos próprios. Elementos simples também são conhecidos como *filhos*.

Para ser identificado e exposto exclusivamente, um elemento simples requer um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e uma ID filho. Portanto, ao se comunicar com um objeto **IAccessible** , os clientes devem fornecer a ID filho apropriada. Um identificador especial, **childID \_** próprio, pode ser usado para fazer referência ao próprio objeto acessível, em vez de um de seus filhos.

O objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) compartilhado entre elementos simples geralmente corresponde a um objeto pai comum na interface do usuário. Por exemplo, as caixas de listagem do sistema expõem um objeto acessível para a caixa de listagem geral e elementos simples para cada item da caixa de listagem. Nesse caso, o objeto **IAccessible** da caixa de listagem também é o pai ou o contêiner dos itens da lista.

Para obter mais informações sobre objetos acessíveis, consulte [objetos acessíveis](accessible-objects.md).

 

 




