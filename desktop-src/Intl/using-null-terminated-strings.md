---
description: Os aplicativos Unicode sempre devem converter zero em TCHAR ao usar cadeias de caracteres terminadas em nulo.
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: Usando cadeias de caracteres terminadas em nulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce12079fa3d0c5a88af369a347f1cd655136ee09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172175"
---
# <a name="using-null-terminated-strings"></a>Usando cadeias de caracteres terminadas em nulo

Os aplicativos Unicode sempre devem converter zero em TCHAR ao usar cadeias de caracteres terminadas em nulo. O código 0x0000 é o terminador de cadeia de caracteres Unicode para uma cadeia de caracteres terminada em nulo. Um único byte nulo não é suficiente para este código, porque muitos caracteres Unicode contêm bytes nulos como o byte alto ou baixo. Um exemplo é a letra a, para a qual o código de caractere é 0x0041.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando caracteres especiais em Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



