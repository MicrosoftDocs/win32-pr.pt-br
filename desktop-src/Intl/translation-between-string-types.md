---
description: As funções listadas na tabela a seguir convertem cadeias de caracteres de um tipo de cadeia de caracteres para outro.
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: Conversão entre tipos de cadeia de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877721f2d8ce3852011786e487598e3fd068c9eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761371"
---
# <a name="translation-between-string-types"></a><span data-ttu-id="03fd4-103">Conversão entre tipos de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="03fd4-103">Translation Between String Types</span></span>

<span data-ttu-id="03fd4-104">As funções listadas na tabela a seguir convertem cadeias de caracteres de um tipo de cadeia de caracteres para outro.</span><span class="sxs-lookup"><span data-stu-id="03fd4-104">The functions listed in the following table translate character strings from one string type to another.</span></span>



| <span data-ttu-id="03fd4-105">Função</span><span class="sxs-lookup"><span data-stu-id="03fd4-105">Function</span></span>                                           | <span data-ttu-id="03fd4-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="03fd4-106">Description</span></span>                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="03fd4-107">**FoldString**</span><span class="sxs-lookup"><span data-stu-id="03fd4-107">**FoldString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | <span data-ttu-id="03fd4-108">Traduz uma cadeia de caracteres para outra.</span><span class="sxs-lookup"><span data-stu-id="03fd4-108">Translates one character string to another.</span></span>             |
| [<span data-ttu-id="03fd4-109">**LCMapString**</span><span class="sxs-lookup"><span data-stu-id="03fd4-109">**LCMapString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | <span data-ttu-id="03fd4-110">Mapeia uma cadeia de caracteres por localidade.</span><span class="sxs-lookup"><span data-stu-id="03fd4-110">Maps a character string by locale.</span></span>                      |
| [<span data-ttu-id="03fd4-111">**Tounicode**</span><span class="sxs-lookup"><span data-stu-id="03fd4-111">**ToUnicode**</span></span>](/windows/win32/api/winuser/nf-winuser-tounicode)              | <span data-ttu-id="03fd4-112">Traduz um código de chave virtual em um caractere Unicode.</span><span class="sxs-lookup"><span data-stu-id="03fd4-112">Translates a virtual key code into a Unicode character.</span></span> |
| [<span data-ttu-id="03fd4-113">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="03fd4-113">**MultiByteToWideChar**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | <span data-ttu-id="03fd4-114">Mapeia uma cadeia de caracteres multibyte para uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="03fd4-114">Maps a multibyte string to a Unicode string.</span></span>            |
| [<span data-ttu-id="03fd4-115">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="03fd4-115">**WideCharToMultiByte**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | <span data-ttu-id="03fd4-116">Mapeia uma cadeia de caracteres Unicode para uma cadeia de caracteres multibyte.</span><span class="sxs-lookup"><span data-stu-id="03fd4-116">Maps a Unicode string to a multibyte string.</span></span>            |



 

<span data-ttu-id="03fd4-117">As funções [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) e [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) são particularmente úteis para aplicativos que dão suporte a vários tipos de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="03fd4-117">The [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) and [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) functions are particularly useful for applications that support several string types.</span></span> <span data-ttu-id="03fd4-118">ANSI C também define as funções de conversão **wcstombs** e **mbstowcs**, mas elas só podem converter de e para o conjunto de caracteres com suporte na biblioteca C padrão.</span><span class="sxs-lookup"><span data-stu-id="03fd4-118">ANSI C also defines the conversion functions **wcstombs** and **mbstowcs**, but they can only convert to and from the character set supported by the standard C library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03fd4-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03fd4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03fd4-120">Unicode na API do Windows</span><span class="sxs-lookup"><span data-stu-id="03fd4-120">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
