---
description: '\_Descrição da constante ICONSTRUCTEDLOCALE de localidade'
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 26d54ce55393f54d56f521231e257a8b0692758f8e6c830a890d81c8f82e8422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809634"
---
# <a name="locale_iconstructedlocale"></a>ICONSTRUCTEDLOCALE de localidade \_

Identificador a ser solicitado se a localidade for uma localidade "construída". O uso desse LCTYPE não é recomendado.

isso identifica uma localidade para a qual Windows muitos não têm informações completas e tem de "construir" informações em tempo de execução. normalmente, as informações fornecidas pelo LOCALE_ICONSTRUCTEDLOCALE são de uso limitado, já que Windows fornecerá tantos dados quantos estiverem disponíveis para cada localidade. Portanto, o uso desse LCTYPE não é recomendado.


| Valor | Significado                 |
|-------|-------------------------|
| 0     | Não construído         |
| 1     | É uma localidade construída |


Um exemplo seria uma solicitação para "de-US" ou para o alemão na Estados Unidos. O NLS usará os dados do idioma alemão que ele pode encontrar e os Estados Unidos dados de região que ele pode encontrar. 

Isso pode não ser perfeito, como, por exemplo, o sistema provavelmente não terá informações sobre o nome de Estados Unidos em alemão. No entanto, se o aplicativo ou o usuário desejar um contexto "de-US", os dados retornados serão os melhores disponíveis. 

Os aplicativos que usam LOCALE_ICONSTRUCTEDLOCALE para rejeitar as localidades e fazer fallback para uma localidade diferente normalmente acabam com uma experiência pior, como a aterrissagem em de-DE-ou en-US neste exemplo. Nenhuma delas está perto da solicitação original para o idioma alemão com uma região Estados Unidos.

