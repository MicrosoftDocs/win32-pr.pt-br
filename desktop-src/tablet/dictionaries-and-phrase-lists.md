---
description: O léxico ou a lista de palavras possíveis usadas pelo modelo de linguagem de um reconhecedor específico está contido em um ou mais dicionários.
ms.assetid: e975a75f-ab88-4164-afc8-3b817988504d
title: Dicionários e listas de frases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0cc5b97918e1fed384494e887b604f1d08856e27232ed82f09bceff3ce14fe2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110956"
---
# <a name="dictionaries-and-phrase-lists"></a>Dicionários e listas de frases

O léxico ou a lista de palavras possíveis usadas pelo modelo de linguagem de um reconhecedor específico está contido em um ou mais dicionários. O reconhecedor pesquisa todos os dicionários disponíveis no sistema ao compilar as correspondeções de reconhecimento. Você pode usar as SAPI (APIs de Fala da Microsoft) para modificar alguns desses dicionários.

Uma lista de frases fornece outro meio de modificar o vocabulário do reconhecedor. Adicionar palavras a uma lista de frases estende o vocabulário; adicionar palavras e restringir o reconhecedor para usar apenas a lista de frases (em oposição à lista de frases e aos dicionários) restringe o vocabulário.

Versões anteriores das APIs de Tecnologia de Tablet PC dependia do conceito de listas de palavras. As listas de palavras são quase idênticas às listas de frases e são usadas para a mesma finalidade ao trabalhar diretamente com um objeto [**RecognizerContext**](inkrecognizercontext-class.md) em um aplicativo habilitado para tinta. Para obter mais detalhes sobre onde e quando usar listas de palavras, consulte [Setting Context for Ink-Enabled Controls](setting-context-for-ink-enabled-controls.md).

Quando o tamanho da lista com a qual você deseja estender o léxico excede 100.000 palavras, recomendamos que você use um dicionário em vez de uma lista de palavras ou lista de frases.

 

 



