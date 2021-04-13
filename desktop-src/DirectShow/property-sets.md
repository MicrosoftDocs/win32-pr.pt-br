---
description: Conjuntos de propriedades
ms.assetid: 4b8a917f-7a6c-4433-83f4-b83ef6d26115
title: Conjuntos de Propriedades (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdc65efbc99eeed3a5f94ab33ce5ec982975852
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370171"
---
# <a name="property-sets-directshow"></a>Conjuntos de Propriedades (DirectShow)

O Microsoft DirectShow usa conjuntos de propriedades para dar suporte a serviços estendidos oferecidos por hardware e seus drivers e filtros associados. Fornecedores de hardware e filtro podem definir novos recursos como propriedades, organizá-los em conjuntos de propriedades e publicar a especificação para esses conjuntos de propriedades. Como desenvolvedor do aplicativo, você pode usar os métodos da interface [**IKsPropertySet**](ikspropertyset.md) para determinar se um driver ou filtro dá suporte a um determinado conjunto de propriedades e recuperar ou definir essas propriedades.

Todos os métodos expostos por **IKsPropertySet** exigem um **GUID** que identifica o conjunto de Propriedades (o parâmetro *guidPropSet* ) e um **DWORD** que identifica a propriedade dentro do conjunto de Propriedades (o parâmetro *dwPropId* ). O parâmetro *dwPropId* normalmente é um membro de um tipo de dados enumerado.

As propriedades individuais podem ter dados associados que você especifica no parâmetro *pPropData* nos métodos [**IKsPropertySet:: Set**](ikspropertyset-set.md) e [**IKsPropertySet:: Get**](ikspropertyset-get.md) . Nesses métodos, os dados de propriedade são digitados como um ponteiro para `void` . O tipo de dados e o significado dos dados são especificados na definição do conjunto de propriedades.

As seções a seguir fornecem informações sobre os conjuntos de propriedades com suporte no DirectShow:

-   [**Conjunto de propriedades da proteção contra cópia de DVD**](dvd-copy-protection-property-set.md)
-   [**Conjunto de propriedades de karaokê de DVD**](dvd-karaoke-property-set.md)
-   [**Conjunto de propriedades de subimagem de DVD**](dvd-subpicture-property-set.md)
-   [Conjunto de propriedades de transporte de dispositivo externo](external-device-transport-property-set.md)
-   [Conjunto de propriedades de revisão do quadro](frame-stepping-property-set.md)
-   [Conjunto de propriedades de PIN](pin-property-set.md)
-   [**Conjunto de propriedades de alteração de taxa**](rate-change-property-set.md)

 

 



