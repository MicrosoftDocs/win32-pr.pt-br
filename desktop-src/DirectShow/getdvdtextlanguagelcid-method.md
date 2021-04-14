---
description: O método GetDVDTextLanguageLCID recupera o LCID (identificador de localidade) para o bloco de cadeia de caracteres de texto especificado.
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: Método GetDVDTextLanguageLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66d21b9870982b605d9deeb1e22882a525c5616
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500195"
---
# <a name="getdvdtextlanguagelcid-method"></a><span data-ttu-id="7adf2-103">Método GetDVDTextLanguageLCID</span><span class="sxs-lookup"><span data-stu-id="7adf2-103">GetDVDTextLanguageLCID Method</span></span>

> [!Note]  
> <span data-ttu-id="7adf2-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7adf2-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7adf2-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="7adf2-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7adf2-106">O `GetDVDTextLanguageLCID` método recupera o LCID (identificador de localidade) para o bloco de cadeia de caracteres de texto especificado.</span><span class="sxs-lookup"><span data-stu-id="7adf2-106">The `GetDVDTextLanguageLCID` method retrieves the locale identifier (LCID) for the specified text string block.</span></span>

``` syntax
[ iLCID = ] MSWebDVD.GetDVDTextLanguageLCID(iLangIndex)
```

## <a name="parameters"></a><span data-ttu-id="7adf2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7adf2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7adf2-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span><span class="sxs-lookup"><span data-stu-id="7adf2-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span></span>
</dt> <dd>

<span data-ttu-id="7adf2-109">Especifica o bloco de linguagem de texto no disco como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="7adf2-109">Specifies the text language block on the disc as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7adf2-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7adf2-110">Return Value</span></span>

<span data-ttu-id="7adf2-111">Retorna um valor LCID que contém informações que especificam o idioma em que as cadeias de caracteres são gravadas.</span><span class="sxs-lookup"><span data-stu-id="7adf2-111">Returns an LCID value that contains information specifying the language the strings are written in.</span></span>

## <a name="remarks"></a><span data-ttu-id="7adf2-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="7adf2-112">Remarks</span></span>

<span data-ttu-id="7adf2-113">As cadeias de caracteres de texto complementares são armazenadas em blocos contíguos no disco. Cada idioma tem um bloco de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7adf2-113">Supplemental text strings are stored in contiguous blocks on the disc. Each language has one block of strings.</span></span> <span data-ttu-id="7adf2-114">Um aplicativo especifica esses blocos por um índice, que deve ser menor que o valor retornado por [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span><span class="sxs-lookup"><span data-stu-id="7adf2-114">An application specifies these blocks by an index, which must be less than the value returned by [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7adf2-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="7adf2-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7adf2-116">Objeto MSWebDVD</span><span class="sxs-lookup"><span data-stu-id="7adf2-116">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> <dt>

[<span data-ttu-id="7adf2-117">**GetLangFromLangID**</span><span class="sxs-lookup"><span data-stu-id="7adf2-117">**GetLangFromLangID**</span></span>](getlangfromlangid-method.md)
</dt> </dl>

 

 



