---
description: O tipo de dados Language é uma cadeia de texto que contém uma ou mais IDs de idioma numérico válidas. Se houver duas ou mais IDs de idioma, elas deverão ser separadas por vírgulas.
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: Idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b98e24ec0ad4d4b42dfcba02374792e10ea117db474a973eae06336a55834538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013124"
---
# <a name="language"></a>Idioma

O tipo de dados Language é uma cadeia de texto que contém uma ou mais IDs de idioma numérico válidas. Se houver duas ou mais IDs de idioma, elas deverão ser separadas por vírgulas.

O tipo de dados Language é um valor de 16 bits que é a combinação de IDs numéricas primárias e subidiomas. O LANGid primário inclui bits 0 a 9, enquanto a ID do subidioma é de 10 a 15. Para obter uma lista dos identificadores numéricos primário e de subidioma, consulte o tópico [constantes e cadeias de caracteres do identificador de linguagem](../intl/language-identifier-constants-and-strings.md) .

Para IDs de idioma primário, o intervalo 0x200 a 0x3FF é definido pelo usuário. O intervalo de 0x000 a 0x1ff é reservado para uso do sistema. Para IDs de subidioma, o intervalo de 0x20 a 0x3F é definido pelo usuário. O intervalo 0x00 a 0x1F é reservado para uso do sistema.

 

 
