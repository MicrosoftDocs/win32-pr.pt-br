---
description: A classe FOURCCMap fornece conversão entre subtipos de mídia GUID e marcas de mídia de 32 bits FOURCC de estilo antigo.
ms.assetid: f77f1da9-34f6-44a0-9f1a-7db2e5a26268
title: Classe FOURCCMap
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap
api_type:
- COM
api_location: ''
ms.openlocfilehash: b9254986bebadeffafaa832817f59194bfc58e12
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908854"
---
# <a name="fourccmap-class"></a><span data-ttu-id="fb3fa-103">Classe FOURCCMap</span><span class="sxs-lookup"><span data-stu-id="fb3fa-103">FOURCCMap class</span></span>

![hierarquia de classe FOURCCMap](images/fourcc01.png)

<span data-ttu-id="fb3fa-105">A classe **FOURCCMap** fornece conversão entre subtipos de mídia **GUID** e marcas de mídia de 32 bits **FOURCC** de estilo antigo.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-105">The **FOURCCMap** class provides conversion between **GUID** media subtypes and old-style **FOURCC** 32-bit media tags.</span></span> <span data-ttu-id="fb3fa-106">Nas APIs de multimídia originais do Windows, os tipos de mídia foram marcados com valores de 32 bits criados a partir de caracteres de 4 8 bits e eram conhecidos como s **FOURCC**.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-106">In the original Windows multimedia APIs, media types were tagged with 32-bit values created from four 8-bit characters and were known as **FOURCC** s.</span></span> <span data-ttu-id="fb3fa-107">Os tipos de mídia do DirectShow têm **GUID** s para o subtipo, parcialmente porque são mais simples de criar (a criação de um novo **FOURCC** requer seu registro com a Microsoft).</span><span class="sxs-lookup"><span data-stu-id="fb3fa-107">DirectShow media types have **GUID** s for the subtype, partly because these are simpler to create (creation of a new **FOURCC** requires its registration with Microsoft).</span></span> <span data-ttu-id="fb3fa-108">Como os s **FOURCC** são exclusivos, um mapeamento um-para-um tornou-se possível alocando um intervalo de 4.000.000.000 **GUID** s representando os s **FOURCC**.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-108">Because **FOURCC** s are unique, a one-to-one mapping has been made possible by allocating a range of 4,000 million **GUID** s representing **FOURCC** s.</span></span> <span data-ttu-id="fb3fa-109">Esse intervalo é todos os **GUIDs** do formulário:</span><span class="sxs-lookup"><span data-stu-id="fb3fa-109">This range is all **GUID** s of the form:</span></span>

`XXXXXXXX-0000-0010-8000-00AA00389B71`

<span data-ttu-id="fb3fa-110">Essa classe simplifica a conversão entre o **GUID** s e os s **FOURCC**.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-110">This class simplifies conversion between **GUID** s and **FOURCC** s.</span></span> <span data-ttu-id="fb3fa-111">Isso é apenas para fins de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-111">This is for compatibility only.</span></span> <span data-ttu-id="fb3fa-112">É recomendável que todos os novos subtipos de mídia sejam representados por **GUID** s criados por Guidgen.exe ou por uma ferramenta semelhante, e não pelo mapeamento de s **FOURCC**.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-112">It is recommended that all new media subtypes be represented by **GUID** s created by Guidgen.exe or a similar tool, and not by mapping **FOURCC** s.</span></span>

<span data-ttu-id="fb3fa-113">O objeto é derivado de um **GUID**, sem membros de dados adicionais e pode ser convertido em um **GUID**.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-113">The object is derived from a **GUID**, with no extra data members, and can be cast to a **GUID**.</span></span> <span data-ttu-id="fb3fa-114">O objeto pode ser passado como um **FOURCC** no momento da construção.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-114">The object can be passed a **FOURCC** at construction time.</span></span> <span data-ttu-id="fb3fa-115">O construtor padrão inicializará o **FOURCC** como zero.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-115">The default constructor will initialize the **FOURCC** to zero.</span></span>

<span data-ttu-id="fb3fa-116">Os métodos [**GetFOURCC**](fourccmap-getfourcc.md) e [**SetFOURCC**](fourccmap-setfourcc.md) não verificam se as partes fixas do **GUID** correspondem ao intervalo **FOURCC** .</span><span class="sxs-lookup"><span data-stu-id="fb3fa-116">The [**GetFOURCC**](fourccmap-getfourcc.md) and [**SetFOURCC**](fourccmap-setfourcc.md) methods do not check that the fixed portions of the **GUID** correspond to the **FOURCC** range.</span></span> <span data-ttu-id="fb3fa-117">Portanto, se você converter um ponteiro para um **GUID** em um ponteiro para um **FOURCC** e, em seguida, definir ou obter o campo **FOURCC** , também precisará verificar separadamente se o **GUID** está dentro do intervalo **FOURCC** .</span><span class="sxs-lookup"><span data-stu-id="fb3fa-117">Thus, if you cast a pointer to a **GUID** into a pointer to a **FOURCC** and then set or get the **FOURCC** field, you also need to check separately that the **GUID** is within the **FOURCC** range.</span></span>

## <a name="member-functions"></a><span data-ttu-id="fb3fa-118">Funções de membro</span><span class="sxs-lookup"><span data-stu-id="fb3fa-118">Member Functions</span></span>



| <span data-ttu-id="fb3fa-119">Label</span><span class="sxs-lookup"><span data-stu-id="fb3fa-119">Label</span></span> | <span data-ttu-id="fb3fa-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fb3fa-120">Value</span></span> |
|------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="fb3fa-121">**FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="fb3fa-121">**FOURCCMap**</span></span>](fourccmap-fourccmap.md) | <span data-ttu-id="fb3fa-122">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="fb3fa-122">Constructor method.</span></span>                                      |
| [<span data-ttu-id="fb3fa-123">**GetFOURCC**</span><span class="sxs-lookup"><span data-stu-id="fb3fa-123">**GetFOURCC**</span></span>](fourccmap-getfourcc.md) | <span data-ttu-id="fb3fa-124">Recupera o **FOURCC** de um objeto **FOURCCMap** .</span><span class="sxs-lookup"><span data-stu-id="fb3fa-124">Retrieves the **FOURCC** from a **FOURCCMap** object.</span></span>    |
| [<span data-ttu-id="fb3fa-125">**SetFOURCC**</span><span class="sxs-lookup"><span data-stu-id="fb3fa-125">**SetFOURCC**</span></span>](fourccmap-setfourcc.md) | <span data-ttu-id="fb3fa-126">Define a parte **FOURCC** do objeto **FOURCCMap** .</span><span class="sxs-lookup"><span data-stu-id="fb3fa-126">Sets the **FOURCC** portion of the **FOURCCMap** object.</span></span> |



 

 

 



