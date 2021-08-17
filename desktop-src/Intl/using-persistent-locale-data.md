---
description: Usando dados de localidade persistentes
ms.assetid: f62402d6-31de-4ff7-9538-7925a007a089
title: Usando dados de localidade persistentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28f1545284f6bebc0d903f8f5fc3fdd3b74ea29730dc64f52c1ed384ae2a7c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383326"
---
# <a name="using-persistent-locale-data"></a>Usando dados de localidade persistentes

Um aplicativo globalizado geralmente persiste ou transmite dados, por exemplo, hora e data. Ao decidir como seu aplicativo deve lidar com a persistência de dados, lembre-se de que não há garantia de que os dados sejam os mesmos do computador para o computador ou entre as executações do aplicativo. Isso é verdadeiro para ambas [as localidades](locales-and-languages.md) que são Windows [e localidades personalizadas.](custom-locales.md)

O design do aplicativo deve levar em conta uma variedade de alterações de dados relacionadas à localidade que podem ocorrer. Por exemplo:

-   Conversor de Moedas símbolos podem mudar à medida que os países adotam o Euro.
-   As preferências regionais podem mudar. Por exemplo, o formato d/m/y pode mudar para o formato m/d/y para uma localidade específica.
-   A ortografia de nomes de dia pode mudar devido a reforma ortográfica. Além disso, a caixa de dados pode mudar para nomes de mês ou dia.

## <a name="use-locale-independent-formats-for-storage-and-data-interchange"></a>Usar Locale-Independent formatos para Armazenamento e intercâmbio de dados

Um aplicativo que persiste dados deve usar formatos independentes de localidade para armazenamento e intercâmbio de dados. Exemplos são formatos em código ou padrão; a localidade invariável [LOCALE \_ NAME \_ INVARIANT](locale-name-constants.md); e formatos de armazenamento binário.

Se dados de classificação persistentes são necessários, o aplicativo deve usar a [**função CompareStringOrdinal.**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) Lembre-se de que um formato invariável não permanece invariável para [classificação](sorting.md), somente para dados de localidade e calendário.

## <a name="use-the-user-default-locale-for-data-presentation"></a>Usar a localidade padrão do usuário para apresentação de dados

Para apresentar dados persistentes, é melhor que o aplicativo reformate os dados usando a localidade padrão do usuário. O uso dessa localidade permite substituições de usuário. Para obter mais informações, consulte [LOCALE \_ USER \_ DEFAULT](locale-user-default.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o suporte a idiomas nacionais](using-national-language-support.md)
</dt> <dt>

[Localidades personalizadas](custom-locales.md)
</dt> <dt>

[Classificação](sorting.md)
</dt> </dl>

 

 



