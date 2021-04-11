---
description: O tipo de dados Language é uma cadeia de texto que contém uma ou mais IDs de idioma numérico válidas. Se houver duas ou mais IDs de idioma, elas deverão ser separadas por vírgulas.
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: Idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87cb8b88dc3a693eee6890276adb67ad359e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164507"
---
# <a name="language"></a><span data-ttu-id="a5554-104">Idioma</span><span class="sxs-lookup"><span data-stu-id="a5554-104">Language</span></span>

<span data-ttu-id="a5554-105">O tipo de dados Language é uma cadeia de texto que contém uma ou mais IDs de idioma numérico válidas.</span><span class="sxs-lookup"><span data-stu-id="a5554-105">The Language data type is a text string containing one or more valid numeric language IDs.</span></span> <span data-ttu-id="a5554-106">Se houver duas ou mais IDs de idioma, elas deverão ser separadas por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="a5554-106">If there are two or more language IDs, they must be separated by commas.</span></span>

<span data-ttu-id="a5554-107">O tipo de dados Language é um valor de 16 bits que é a combinação de IDs numéricas primárias e subidiomas.</span><span class="sxs-lookup"><span data-stu-id="a5554-107">The Language data type is a 16-bit value that is the combination of a primary and sublanguage numeric IDs.</span></span> <span data-ttu-id="a5554-108">O LANGid primário inclui bits 0 a 9, enquanto a ID do subidioma é de 10 a 15.</span><span class="sxs-lookup"><span data-stu-id="a5554-108">The Primary LANGID comprises bits 0 through 9 while the subLanguage ID is bits 10 through 15.</span></span> <span data-ttu-id="a5554-109">Para obter uma lista dos identificadores numéricos primário e de subidioma, consulte o tópico [constantes e cadeias de caracteres do identificador de linguagem](../intl/language-identifier-constants-and-strings.md) .</span><span class="sxs-lookup"><span data-stu-id="a5554-109">For a list of primary and sub language numeric identifiers, see the [Language Identifier Constants and Strings](../intl/language-identifier-constants-and-strings.md) topic.</span></span>

<span data-ttu-id="a5554-110">Para IDs de idioma primário, o intervalo 0x200 a 0x3FF é definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a5554-110">For primary language IDs, the range 0x200 to 0x3ff is user definable.</span></span> <span data-ttu-id="a5554-111">O intervalo de 0x000 a 0x1ff é reservado para uso do sistema.</span><span class="sxs-lookup"><span data-stu-id="a5554-111">The range 0x000 to 0x1ff is reserved for system use.</span></span> <span data-ttu-id="a5554-112">Para IDs de subidioma, o intervalo de 0x20 a 0x3F é definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a5554-112">For sublanguage IDs, the range 0x20 to 0x3f is user definable.</span></span> <span data-ttu-id="a5554-113">O intervalo 0x00 a 0x1F é reservado para uso do sistema.</span><span class="sxs-lookup"><span data-stu-id="a5554-113">The range 0x00 to 0x1f is reserved for system use.</span></span>

 

 
