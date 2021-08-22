---
description: Os aplicativos Unicode sempre devem converter zero em TCHAR ao usar cadeias de caracteres terminadas em nulo.
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: Usando cadeias de caracteres terminadas em nulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0a5f27048bde2af75eca28626a562473ceffcc66f3f2f23509beca4fba06ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631776"
---
# <a name="using-null-terminated-strings"></a>Usando cadeias de caracteres terminadas em nulo

Os aplicativos Unicode sempre devem converter zero em TCHAR ao usar cadeias de caracteres terminadas em nulo. O código 0x0000 é o terminador de cadeia de caracteres Unicode para uma cadeia de caracteres terminada em nulo. Um único byte nulo não é suficiente para este código, porque muitos caracteres Unicode contêm bytes nulos como o byte alto ou baixo. Um exemplo é a letra a, para a qual o código de caractere é 0x0041.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando caracteres especiais em Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



