---
description: O método PlayChapterInTitle reproduz o capítulo especificado no título especificado.
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: Método PlayChapterInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381a63c36c61a8853dcba6a587adb1f078b8cfaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825460"
---
# <a name="playchapterintitle-method"></a><span data-ttu-id="f5d87-103">Método PlayChapterInTitle</span><span class="sxs-lookup"><span data-stu-id="f5d87-103">PlayChapterInTitle Method</span></span>

> [!Note]  
> <span data-ttu-id="f5d87-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f5d87-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f5d87-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f5d87-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f5d87-106">O `PlayChapterInTitle` método reproduz o capítulo especificado no título especificado.</span><span class="sxs-lookup"><span data-stu-id="f5d87-106">The `PlayChapterInTitle` method plays the specified chapter in the specified title.</span></span>

``` syntax
MSWebDVD.PlayChapterInTitle(iTitle, iChapter)
```

## <a name="parameters"></a><span data-ttu-id="f5d87-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5d87-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5d87-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="f5d87-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="f5d87-109">Especifica o título como um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="f5d87-109">Specifies the title as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="f5d87-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span><span class="sxs-lookup"><span data-stu-id="f5d87-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="f5d87-111">Especifica o capítulo como um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="f5d87-111">Specifies the chapter as an Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5d87-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f5d87-112">Return Value</span></span>

<span data-ttu-id="f5d87-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="f5d87-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5d87-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5d87-114">Remarks</span></span>

<span data-ttu-id="f5d87-115">Esse método inicia a reprodução no capítulo especificado e, em seguida, continua sendo executado indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="f5d87-115">This method starts playback at the specified chapter and then continues playing indefinitely.</span></span> <span data-ttu-id="f5d87-116">Se você quiser reproduzir apenas um capítulo específico, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span><span class="sxs-lookup"><span data-stu-id="f5d87-116">If you want to play only a particular chapter, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span></span>

 

 



