---
description: Para NLS, classificação (também conhecido como &\# 0034; agrupamento&\# 0034;) é a organização de cadeias de caracteres.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Classificação (internacionalização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49a5abb8371a00ad9ee63f929b4aaf4b18b11be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172033"
---
# <a name="sorting"></a><span data-ttu-id="45f98-103">Classificação</span><span class="sxs-lookup"><span data-stu-id="45f98-103">Sorting</span></span>

<span data-ttu-id="45f98-104">Para NLS, a classificação (também conhecida como "Agrupamento") é a organização das cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="45f98-104">For NLS, sorting (also known as "collation") is the arrangement of strings.</span></span> <span data-ttu-id="45f98-105">Há dois tipos de classificação:</span><span class="sxs-lookup"><span data-stu-id="45f98-105">There are two types of sorting:</span></span>

-   <span data-ttu-id="45f98-106">Classificação linguística.</span><span class="sxs-lookup"><span data-stu-id="45f98-106">Linguistic sorting.</span></span> <span data-ttu-id="45f98-107">Organiza cadeias de caracteres com características linguísticas semelhantes em grupos (por classificação).</span><span class="sxs-lookup"><span data-stu-id="45f98-107">Arranges strings with similar linguistic characteristics into groups (by sorts).</span></span>
-   <span data-ttu-id="45f98-108">Classificação Ordinal (não lingüística).</span><span class="sxs-lookup"><span data-stu-id="45f98-108">Ordinal (non-linguistic) sorting.</span></span> <span data-ttu-id="45f98-109">Organiza as cadeias de caracteres em uma sequência ordenada.</span><span class="sxs-lookup"><span data-stu-id="45f98-109">Arranges the strings in an ordered sequence.</span></span>

<span data-ttu-id="45f98-110">A classificação usa as funções de comparação de cadeia de caracteres NLS, como [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), ou funções de API "wrapper", como [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), que chamam internamente as funções de comparação de cadeia de caracteres NLS.</span><span class="sxs-lookup"><span data-stu-id="45f98-110">Sorting uses the NLS string comparison functions, such as [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) and [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), or "wrapper" API functions, such as [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), that internally call the NLS string comparison functions.</span></span>

<span data-ttu-id="45f98-111">Para obter detalhes sobre como implementar a classificação em seus aplicativos, consulte [lidando com a classificação em seus aplicativos](handling-sorting-in-your-applications.md).</span><span class="sxs-lookup"><span data-stu-id="45f98-111">For details about implementing sorting in your applications, see [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="45f98-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45f98-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45f98-113">Sobre o suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="45f98-113">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="45f98-114">Lidando com a classificação em seus aplicativos</span><span class="sxs-lookup"><span data-stu-id="45f98-114">Handling Sorting in Your Applications</span></span>](handling-sorting-in-your-applications.md)
</dt> <dt>

[<span data-ttu-id="45f98-115">**CompareString**</span><span class="sxs-lookup"><span data-stu-id="45f98-115">**CompareString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[<span data-ttu-id="45f98-116">LCMapString</span><span class="sxs-lookup"><span data-stu-id="45f98-116">LCMapString</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
