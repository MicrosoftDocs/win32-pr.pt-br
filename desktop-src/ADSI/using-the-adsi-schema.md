---
title: Usando o esquema ADSI
description: Um esquema define o universo de objetos armazenados em um diretório.
ms.assetid: 140a5dd0-6f50-4f84-8708-45c0f1c6bdc4
ms.tgt_platform: multiple
keywords:
- Usando o esquema ADSI
- ADSI, ADSI, usando, esquema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478104a24d850f79cc52473f3d9e546936c56650
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103823988"
---
# <a name="using-the-adsi-schema"></a>Usando o esquema ADSI

Um esquema define o universo de objetos armazenados em um diretório. No Active Directory, o esquema especifica quais atributos um objeto de serviço de diretório pode ou deve ter. Ele também especifica o intervalo de valores e a sintaxe dos atributos e se eles dão suporte a valores únicos ou múltiplos. Em suma, o esquema é organizado por definições de classe, definições de atributo e sintaxe de atributo. A ADSI fornece três interfaces para ler dados de atributo, classe e sintaxe de um esquema: [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)e [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax).

Active Directory usa um conjunto de objetos de esquema para fornecer gerenciamento de esquema extensível dinamicamente. Para obter mais informações sobre um objeto desconhecido, pesquise seus objetos de esquema associados. Para criar uma nova definição de classe ou estender uma definição de classe existente, você pode criar ou estender os objetos de esquema apropriados. Os objetos de esquema são organizados no contêiner de esquema de um determinado diretório. Para acessar uma classe de esquema de objeto, use a propriedade [**IADs. Schema**](iads-property-methods.md) do objeto para obter a cadeia de caracteres ADsPath e use essa cadeia de caracteres para associar a uma interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) na classe de esquema de objeto.

Para determinar as definições de atributo, ou seja, o intervalo de valores, a sintaxe e assim por diante, inspecione os objetos de atributo de esquema para cada propriedade com suporte no objeto de serviço de diretório. Para obter mais informações sobre como acessar os objetos de atributo de esquema, consulte [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty).

A ADSI abstrai os dados de sintaxe conforme necessário e permite que você use [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) para identificar a sintaxe necessária para representar dados de objeto.

Para obter mais informações sobre o esquema de Active Directory, consulte [Active Directory esquema](/windows/desktop/AD/active-directory-schema). Para obter exemplos de código a serem usados para ler o contêiner de esquema, consulte [lendo o esquema](reading-the-schema.md).

 

 