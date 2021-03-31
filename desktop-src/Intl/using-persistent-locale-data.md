---
description: Usando dados de localidade persistente
ms.assetid: f62402d6-31de-4ff7-9538-7925a007a089
title: Usando dados de localidade persistente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4fe4990da53e4db9f71b2feffbd9eb40aedee9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837418"
---
# <a name="using-persistent-locale-data"></a>Usando dados de localidade persistente

Um aplicativo globalizado geralmente mantém ou transmite dados, por exemplo, data e hora. Ao decidir como seu aplicativo deve lidar com a persistência de dados, lembre-se de que não há garantia de que os dados sejam os mesmos do computador para o computador ou entre as execuções do aplicativo. Isso é verdadeiro para as [localidades](locales-and-languages.md) fornecidas com o Windows e as [localidades personalizadas](custom-locales.md).

O design do aplicativo deve levar em conta uma variedade de alterações de dados relacionadas à localidade que podem ocorrer. Por exemplo:

-   Os símbolos de moeda podem mudar conforme os países adotam o euro.
-   As preferências regionais podem ser alteradas. Por exemplo, o formato d/m/y pode mudar para o formato m/d/y de uma localidade específica.
-   A ortografia dos nomes de dias pode mudar devido à reforms de ortografia. Além disso, a capitalização pode mudar para os nomes de mês ou dia.

## <a name="use-locale-independent-formats-for-storage-and-data-interchange"></a>Usar formatos de Locale-Independent para armazenamento e troca de dados

Um aplicativo que persiste dados deve usar formatos independentes de localidade para armazenamento e troca de dados. Os exemplos são formatos embutidos em código ou padrão; o nome da localidade de localidade invariável invariável e formatos de armazenamento binários. [ \_ \_ ](locale-name-constants.md)

Se a classificação persistente de dados for necessária, o aplicativo deverá usar a função [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) . Lembre-se de que um formato invariável não permanece invariável para [classificação](sorting.md), somente para dados de localidade e calendário.

## <a name="use-the-user-default-locale-for-data-presentation"></a>Usar a localidade padrão do usuário para a apresentação de dados

Para apresentar dados persistentes, é melhor para o aplicativo reformatar os dados usando a localidade padrão do usuário. O uso dessa localidade permite substituições do usuário. Para obter mais informações, consulte [local \_ user \_ Default](locale-user-default.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o suporte ao idioma nacional](using-national-language-support.md)
</dt> <dt>

[Localidades personalizadas](custom-locales.md)
</dt> <dt>

[Classificação](sorting.md)
</dt> </dl>

 

 



