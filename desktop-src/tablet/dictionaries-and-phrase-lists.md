---
description: O léxico ou a lista de palavras possíveis usadas pelo modelo de linguagem de um reconhecedor específico está contido em um ou mais dicionários.
ms.assetid: e975a75f-ab88-4164-afc8-3b817988504d
title: Listas de dicionários e de frases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f88dc2f6b05eea322b6e88dda1f986b3c54b7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781613"
---
# <a name="dictionaries-and-phrase-lists"></a>Listas de dicionários e de frases

O léxico ou a lista de palavras possíveis usadas pelo modelo de linguagem de um reconhecedor específico está contido em um ou mais dicionários. O reconhecedor pesquisa todos os dicionários disponíveis no sistema durante a compilação de correspondências de reconhecimento. Você pode usar o SAPI (Microsoft Speech APIs) para modificar alguns desses dicionários.

Uma lista de frases fornece outro meio de modificar o vocabulário do reconhecedor. A adição de palavras a uma lista de frases estende o vocabulário; adicionar palavras e, em seguida, restringir o reconhecedor para usar apenas a lista de frases (ao contrário da lista de frases e dos dicionários) restringe o vocabulário.

Versões anteriores das APIs de tecnologia do Tablet PC contavam com o conceito de listas de palavras. As listas de palavras são quase idênticas às listas de frases e são usadas para a mesma finalidade ao trabalhar diretamente com um objeto [**RecognizerContext**](inkrecognizercontext-class.md) em um aplicativo habilitado para tinta. Para obter mais detalhes sobre onde e quando usar listas de palavras, consulte [Configurando contexto para controles de Ink-Enabled](setting-context-for-ink-enabled-controls.md).

Quando o tamanho da lista com o qual você deseja estender o léxico excede 100.000 palavras, recomendamos que você use um dicionário em vez de uma lista de palavras ou de expressões.

 

 



