---
description: O método GetDVDTextNumberOfStrings recupera o número de cadeias de caracteres de texto disponíveis para o idioma especificado.
ms.assetid: 84d2b5b7-b474-48a4-9058-ea9da8109398
title: Método GetDVDTextNumberOfStrings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c9c4fadfd28d6cddc8b9013a6e426aebe9f816
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105786977"
---
# <a name="getdvdtextnumberofstrings-method"></a><span data-ttu-id="1a169-103">Método GetDVDTextNumberOfStrings</span><span class="sxs-lookup"><span data-stu-id="1a169-103">GetDVDTextNumberOfStrings Method</span></span>

> [!Note]  
> <span data-ttu-id="1a169-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1a169-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1a169-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="1a169-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="1a169-106">O `GetDVDTextNumberOfStrings` método recupera o número de cadeias de caracteres de texto disponíveis para o idioma especificado.</span><span class="sxs-lookup"><span data-stu-id="1a169-106">The `GetDVDTextNumberOfStrings` method retrieves the number of text strings available for the specified language.</span></span>

``` syntax
[ iStrings = ] MSWebDVD.GetDVDTextNumberOfStrings(iLangIndex)
```

## <a name="parameters"></a><span data-ttu-id="1a169-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a169-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a169-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span><span class="sxs-lookup"><span data-stu-id="1a169-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span></span>
</dt> <dd>

<span data-ttu-id="1a169-109">Especifica o idioma como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="1a169-109">Specifies the language as an Integer.</span></span> <span data-ttu-id="1a169-110">O valor deve variar de zero a um menor que o valor retornado por [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span><span class="sxs-lookup"><span data-stu-id="1a169-110">The value must range from zero through one less than the value returned by [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a169-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1a169-111">Return Value</span></span>

<span data-ttu-id="1a169-112">Retorna um valor inteiro especificando quantas cadeias de caracteres o disco contém no idioma especificado.</span><span class="sxs-lookup"><span data-stu-id="1a169-112">Returns an integer value specifying how many strings the disc contains in the specified language.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a169-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a169-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a169-114">Objeto MSWebDVD</span><span class="sxs-lookup"><span data-stu-id="1a169-114">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> </dl>

 

 



