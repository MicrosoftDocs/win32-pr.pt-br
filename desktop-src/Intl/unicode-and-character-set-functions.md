---
description: As funções a seguir são usadas com conjuntos de caracteres.
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Funções de conjunto de caracteres e Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6996139d8a9bb426c21a460ac2bcb1358e6c8e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011563"
---
# <a name="unicode-and-character-set-functions"></a><span data-ttu-id="ad47f-103">Funções de conjunto de caracteres e Unicode</span><span class="sxs-lookup"><span data-stu-id="ad47f-103">Unicode and Character Set Functions</span></span>

<span data-ttu-id="ad47f-104">As funções a seguir são usadas com conjuntos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ad47f-104">The following functions are used with character sets.</span></span>



| <span data-ttu-id="ad47f-105">Função</span><span class="sxs-lookup"><span data-stu-id="ad47f-105">Function</span></span>                                                       | <span data-ttu-id="ad47f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad47f-106">Description</span></span>                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad47f-107">**GetTextCharset**</span><span class="sxs-lookup"><span data-stu-id="ad47f-107">**GetTextCharset**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | <span data-ttu-id="ad47f-108">Recupera um identificador de conjunto de caracteres para a fonte selecionada no momento em um contexto de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="ad47f-108">Retrieves a character set identifier for the font that is currently selected into a specified device context.</span></span>         |
| [<span data-ttu-id="ad47f-109">**GetTextCharsetInfo**</span><span class="sxs-lookup"><span data-stu-id="ad47f-109">**GetTextCharsetInfo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | <span data-ttu-id="ad47f-110">Recupera informações sobre o conjunto de caracteres da fonte selecionada no momento em um contexto de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="ad47f-110">Retrieves information about the character set of the font that is currently selected into a specified device context.</span></span> |
| [<span data-ttu-id="ad47f-111">**IsDBCSLeadByte**</span><span class="sxs-lookup"><span data-stu-id="ad47f-111">**IsDBCSLeadByte**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | <span data-ttu-id="ad47f-112">Determina se um caractere especificado é um byte de Lead para a página de código ANSI padrão do sistema (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="ad47f-112">Determines if a specified character is a lead byte for the system default Windows ANSI code page (CP\_ACP).</span></span>           |
| [<span data-ttu-id="ad47f-113">**IsDBCSLeadByteEx**</span><span class="sxs-lookup"><span data-stu-id="ad47f-113">**IsDBCSLeadByteEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | <span data-ttu-id="ad47f-114">Determina se um caractere especificado é potencialmente um byte de Lead.</span><span class="sxs-lookup"><span data-stu-id="ad47f-114">Determines if a specified character is potentially a lead byte.</span></span>                                                       |
| [<span data-ttu-id="ad47f-115">**IsTextUnicode**</span><span class="sxs-lookup"><span data-stu-id="ad47f-115">**IsTextUnicode**</span></span>](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | <span data-ttu-id="ad47f-116">Determina se é provável que um buffer contenha uma forma de texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="ad47f-116">Determines if a buffer is likely to contain a form of Unicode text.</span></span>                                                   |
| [<span data-ttu-id="ad47f-117">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="ad47f-117">**MultiByteToWideChar**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | <span data-ttu-id="ad47f-118">Mapeia uma cadeia de caracteres para uma cadeia de caracteres UTF-16 (caracteres largos).</span><span class="sxs-lookup"><span data-stu-id="ad47f-118">Maps a character string to a UTF-16 (wide character) string.</span></span>                                                          |
| [<span data-ttu-id="ad47f-119">**TranslateCharsetInfo**</span><span class="sxs-lookup"><span data-stu-id="ad47f-119">**TranslateCharsetInfo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | <span data-ttu-id="ad47f-120">Traduz informações de conjunto de caracteres e define todos os membros de uma estrutura de destino com os valores apropriados.</span><span class="sxs-lookup"><span data-stu-id="ad47f-120">Translates character set information and sets all members of a destination structure to appropriate values.</span></span>           |
| [<span data-ttu-id="ad47f-121">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="ad47f-121">**WideCharToMultiByte**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | <span data-ttu-id="ad47f-122">Mapeia uma cadeia de caracteres UTF-16 (caracteres largos) para uma nova cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ad47f-122">Maps a UTF-16 (wide character) string to a new character string.</span></span>                                                      |
| <span data-ttu-id="ad47f-123">[**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ad47f-123">[**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))</span></span>                       | <span data-ttu-id="ad47f-124">Não use.</span><span class="sxs-lookup"><span data-stu-id="ad47f-124">Do not use.</span></span>                                                                                                           |
| [<span data-ttu-id="ad47f-125">**NlsDllCodePageTranslation**</span><span class="sxs-lookup"><span data-stu-id="ad47f-125">**NlsDllCodePageTranslation**</span></span>](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | <span data-ttu-id="ad47f-126">Não use.</span><span class="sxs-lookup"><span data-stu-id="ad47f-126">Do not use.</span></span>                                                                                                           |
| <span data-ttu-id="ad47f-127">[**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ad47f-127">[**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))</span></span>                       | <span data-ttu-id="ad47f-128">Não use.</span><span class="sxs-lookup"><span data-stu-id="ad47f-128">Do not use.</span></span>                                                                                                           |



 

 

 
