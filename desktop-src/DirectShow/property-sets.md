---
description: Conjuntos de propriedades
ms.assetid: 4b8a917f-7a6c-4433-83f4-b83ef6d26115
title: Conjuntos de propriedades (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c26bef876e0bde559ac506963f86a485a302a9ce6faf6c2699c62dabac3f72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747946"
---
# <a name="property-sets-directshow"></a>Conjuntos de propriedades (DirectShow)

O Microsoft DirectShow usa conjuntos de propriedades para dar suporte a serviços estendidos oferecidos pelo hardware e seus drivers e filtros associados. Fornecedores de hardware e filtro podem definir novos recursos como propriedades, organizá-los em conjuntos de propriedades e publicar a especificação desses conjuntos de propriedades. Como desenvolvedor de aplicativos, você pode usar os métodos da interface [**IKsPropertySet**](ikspropertyset.md) para determinar se um driver ou filtro dá suporte a um conjunto específico de propriedades e recuperar ou definir essas propriedades.

Todos os métodos expostos por **IKsPropertySet** exigem um **GUID** que identifica o conjunto de propriedades (o *parâmetro guidPropSet)* e um **DWORD** que identifica a propriedade dentro do conjunto de propriedades (o *parâmetro dwPropID).* O *parâmetro dwPropID* normalmente é um membro de um tipo de dados enumerado.

As propriedades individuais podem ter dados associados que você especifica no parâmetro *pPropData* nos métodos [**IKsPropertySet::Set**](ikspropertyset-set.md) e [**IKsPropertySet::Get.**](ikspropertyset-get.md) Nesses métodos, os dados da propriedade são digitados como um ponteiro para `void` . O tipo de dados e o significado dos dados são especificados na definição do conjunto de propriedades.

As seções a seguir fornecem informações sobre os conjuntos de propriedades com suporte DirectShow:

-   [**Conjunto de propriedades de proteção de cópia de DVD**](dvd-copy-protection-property-set.md)
-   [**Conjunto de propriedades De DVD**](dvd-karaoke-property-set.md)
-   [**Conjunto de propriedades da Subpicture de DVD**](dvd-subpicture-property-set.md)
-   [Conjunto de propriedades de transporte de dispositivo externo](external-device-transport-property-set.md)
-   [Conjunto de propriedades de passo a passo de quadro](frame-stepping-property-set.md)
-   [Fixar conjunto de propriedades](pin-property-set.md)
-   [**Conjunto de propriedades de alteração de taxa**](rate-change-property-set.md)

 

 



