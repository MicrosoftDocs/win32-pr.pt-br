---
description: '\_Descrição da constante ICONSTRUCTEDLOCALE de localidade'
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 120c206a14030a182378977c9e68fb7dcd77200d
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/30/2021
ms.locfileid: "105995141"
---
# <a name="locale_iconstructedlocale"></a>ICONSTRUCTEDLOCALE de localidade \_

Identificador a ser solicitado se a localidade for uma localidade "construída". O uso desse LCTYPE não é recomendado.

Isso identifica uma localidade para a qual o Windows não tem informações completas e tem de "construir" informações em tempo de execução. Normalmente, as informações fornecidas pelo LOCALE_ICONSTRUCTEDLOCALE são de uso limitado, pois o Windows fornecerá tantos dados quantos estiverem disponíveis para cada localidade. Portanto, o uso desse LCTYPE não é recomendado.


| Valor | Significado                 |
|-------|-------------------------|
| 0     | Não construído         |
| 1     | É uma localidade construída |


Um exemplo seria uma solicitação para "de-US" ou para o alemão na Estados Unidos. O NLS usará os dados do idioma alemão que ele pode encontrar e os Estados Unidos dados de região que ele pode encontrar. 

Isso pode não ser perfeito, como, por exemplo, o sistema provavelmente não terá informações sobre o nome de Estados Unidos em alemão. No entanto, se o aplicativo ou o usuário desejar um contexto "de-US", os dados retornados serão os melhores disponíveis. 

Os aplicativos que usam LOCALE_ICONSTRUCTEDLOCALE para rejeitar as localidades e fazer fallback para uma localidade diferente normalmente acabam com uma experiência pior, como a aterrissagem em de-DE-ou en-US neste exemplo. Nenhuma delas está perto da solicitação original para o idioma alemão com uma região Estados Unidos.

