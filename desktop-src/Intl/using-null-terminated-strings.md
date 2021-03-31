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
# <a name="using-null-terminated-strings"></a><span data-ttu-id="6042d-103">Usando cadeias de caracteres terminadas em nulo</span><span class="sxs-lookup"><span data-stu-id="6042d-103">Using Null-terminated Strings</span></span>

<span data-ttu-id="6042d-104">Os aplicativos Unicode sempre devem converter zero em TCHAR ao usar cadeias de caracteres terminadas em nulo.</span><span class="sxs-lookup"><span data-stu-id="6042d-104">Your Unicode applications should always cast zero to TCHAR when using null-terminated strings.</span></span> <span data-ttu-id="6042d-105">O código 0x0000 é o terminador de cadeia de caracteres Unicode para uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="6042d-105">The code 0x0000 is the Unicode string terminator for a null-terminated string.</span></span> <span data-ttu-id="6042d-106">Um único byte nulo não é suficiente para este código, porque muitos caracteres Unicode contêm bytes nulos como o byte alto ou baixo.</span><span class="sxs-lookup"><span data-stu-id="6042d-106">A single null byte is not sufficient for this code, because many Unicode characters contain null bytes as either the high or the low byte.</span></span> <span data-ttu-id="6042d-107">Um exemplo é a letra a, para a qual o código de caractere é 0x0041.</span><span class="sxs-lookup"><span data-stu-id="6042d-107">An example is the letter A, for which the character code is 0x0041.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6042d-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6042d-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6042d-109">Usando caracteres especiais em Unicode</span><span class="sxs-lookup"><span data-stu-id="6042d-109">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



