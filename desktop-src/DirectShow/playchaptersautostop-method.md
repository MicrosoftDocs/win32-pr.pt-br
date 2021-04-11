---
description: O método PlayChaptersAutoStop inicia a reprodução no capítulo especificado no título especificado e o número de capítulos especificado.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: Método PlayChaptersAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f542f890a54c755c9ea041c46f7cef3b4b7fd9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163763"
---
# <a name="playchaptersautostop-method"></a><span data-ttu-id="bc578-103">Método PlayChaptersAutoStop</span><span class="sxs-lookup"><span data-stu-id="bc578-103">PlayChaptersAutoStop Method</span></span>

> [!Note]  
> <span data-ttu-id="bc578-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bc578-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="bc578-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="bc578-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="bc578-106">O `PlayChaptersAutoStop` método inicia a reprodução no capítulo especificado no título especificado e o número de capítulos especificado.</span><span class="sxs-lookup"><span data-stu-id="bc578-106">The `PlayChaptersAutoStop` method starts playback at the specified chapter in the specified title and for the number of chapters specified.</span></span>

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a><span data-ttu-id="bc578-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc578-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc578-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="bc578-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="bc578-109">Especifica o título como um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="bc578-109">Specifies the title as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="bc578-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span><span class="sxs-lookup"><span data-stu-id="bc578-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="bc578-111">Especifica o capítulo inicial como um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="bc578-111">Specifies the start chapter as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="bc578-112"><span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*</span><span class="sxs-lookup"><span data-stu-id="bc578-112"><span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*</span></span>
</dt> <dd>

<span data-ttu-id="bc578-113">Especifica o número de capítulos a serem reproduzidos como um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="bc578-113">Specifies the number of chapters to play as an Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc578-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="bc578-114">Return Value</span></span>

<span data-ttu-id="bc578-115">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="bc578-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc578-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc578-116">Remarks</span></span>

<span data-ttu-id="bc578-117">Quando o último capítulo foi reproduzido, esse método faz com que uma notificação de evento do [**\_ \_ capítulo \_ autostop**](ec-dvd-chapter-autostop.md) de um DVD do EC seja enviada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bc578-117">When the last chapter has played, this method causes an [**EC\_DVD\_CHAPTER\_AUTOSTOP**](ec-dvd-chapter-autostop.md) event notification to be sent to the application.</span></span>

 

 



