---
description: O método PlayChapter inicia a reprodução do capítulo especificado dentro do título atual.
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: Método PlayChapter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab4600d8d4fc09c4b63fa423c66823e92e95a2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105789825"
---
# <a name="playchapter-method"></a><span data-ttu-id="7f4b7-103">Método PlayChapter</span><span class="sxs-lookup"><span data-stu-id="7f4b7-103">PlayChapter Method</span></span>

> [!Note]  
> <span data-ttu-id="7f4b7-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7f4b7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7f4b7-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="7f4b7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7f4b7-106">O `PlayChapter` método inicia a reprodução do capítulo especificado dentro do título atual.</span><span class="sxs-lookup"><span data-stu-id="7f4b7-106">The `PlayChapter` method starts playback from the specified chapter within the current title.</span></span>

``` syntax
MSWebDVD.PlayChapter(iChapter)
```

## <a name="parameters"></a><span data-ttu-id="7f4b7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f4b7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f4b7-108"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span><span class="sxs-lookup"><span data-stu-id="7f4b7-108"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="7f4b7-109">Especifica o índice do capítulo no título atual como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="7f4b7-109">Specifies the chapter index in the current title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f4b7-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7f4b7-110">Return Value</span></span>

<span data-ttu-id="7f4b7-111">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="7f4b7-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f4b7-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f4b7-112">Remarks</span></span>

<span data-ttu-id="7f4b7-113">Quando o final do capítulo especificado for atingido, esse método continuará a reproduzir os capítulos subsequentes, se existirem.</span><span class="sxs-lookup"><span data-stu-id="7f4b7-113">When the end of the specified chapter is reached, this method continues playing subsequent chapters, if any exist.</span></span> <span data-ttu-id="7f4b7-114">Se você quiser reproduzir apenas um capítulo especificado, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span><span class="sxs-lookup"><span data-stu-id="7f4b7-114">If you want to play only a specified chapter, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7f4b7-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f4b7-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f4b7-116">**PlayChapterInTitle**</span><span class="sxs-lookup"><span data-stu-id="7f4b7-116">**PlayChapterInTitle**</span></span>](playchapterintitle-method.md)
</dt> </dl>

 

 



