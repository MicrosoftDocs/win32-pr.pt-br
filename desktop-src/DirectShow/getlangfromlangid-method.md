---
description: O método GetLangFromLangID recupera uma cadeia de caracteres legível ao receber uma ID de idioma principal.
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: Método GetLangFromLangID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23afddf746852028c26732eb658e786588f7e9ec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825779"
---
# <a name="getlangfromlangid-method"></a><span data-ttu-id="cfe99-103">Método GetLangFromLangID</span><span class="sxs-lookup"><span data-stu-id="cfe99-103">GetLangFromLangID Method</span></span>

> [!Note]  
> <span data-ttu-id="cfe99-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cfe99-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="cfe99-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="cfe99-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="cfe99-106">O `GetLangFromLangID` método recupera uma cadeia de caracteres legível ao receber uma ID de idioma principal.</span><span class="sxs-lookup"><span data-stu-id="cfe99-106">The `GetLangFromLangID` method retrieves a human-readable string when given a primary language ID.</span></span>

``` syntax
[ sLanguage = ] MSWebDVD.GetLangFromLangID(iPrimaryLangID)
```

## <a name="parameters"></a><span data-ttu-id="cfe99-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cfe99-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfe99-108"><span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*</span><span class="sxs-lookup"><span data-stu-id="cfe99-108"><span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*</span></span>
</dt> <dd>

<span data-ttu-id="cfe99-109">Especifica a ID do idioma principal como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="cfe99-109">Specifies the primary language ID as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfe99-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="cfe99-110">Return Value</span></span>

<span data-ttu-id="cfe99-111">Retorna uma representação de cadeia de caracteres do idioma que pode ser exibido na interface do usuário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cfe99-111">Returns a String representation of the language that can be displayed in the application's user interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfe99-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfe99-112">Remarks</span></span>

<span data-ttu-id="cfe99-113">Embora esse método seja nomeado `GetLangFromLangID` , o parâmetro que você passa é, na verdade, a ID do idioma principal, não a ID do idioma.</span><span class="sxs-lookup"><span data-stu-id="cfe99-113">Although this method is named `GetLangFromLangID`, the parameter that you pass is actually the primary language ID, not the language ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="cfe99-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfe99-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe99-115">**GetAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="cfe99-115">**GetAudioLanguage**</span></span>](getaudiolanguage-method.md)
</dt> <dt>

[<span data-ttu-id="cfe99-116">**GetDVDTextLanguageLCID**</span><span class="sxs-lookup"><span data-stu-id="cfe99-116">**GetDVDTextLanguageLCID**</span></span>](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



