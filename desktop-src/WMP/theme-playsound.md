---
title: THEME. playSound
description: O método playSound reproduz o arquivo de som especificado.
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- TEMA. playSound Windows Media Player
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ceb30e5c47632a1358262019124fceae056294d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758090"
---
# <a name="themeplaysound"></a><span data-ttu-id="b3737-104">THEME. playSound</span><span class="sxs-lookup"><span data-stu-id="b3737-104">THEME.playSound</span></span>

<span data-ttu-id="b3737-105">O método **PlaySound** reproduz o arquivo de som especificado.</span><span class="sxs-lookup"><span data-stu-id="b3737-105">The **playSound** method plays the specified sound file.</span></span>

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a><span data-ttu-id="b3737-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3737-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3737-107"><span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*</span><span class="sxs-lookup"><span data-stu-id="b3737-107"><span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*</span></span>
</dt> <dd>

<span data-ttu-id="b3737-108">Uma **cadeia de caracteres** que especifica o nome do arquivo de som a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="b3737-108">A **String** specifying the name of the sound file to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3737-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b3737-109">Return Value</span></span>

<span data-ttu-id="b3737-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b3737-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3737-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3737-111">Remarks</span></span>

<span data-ttu-id="b3737-112">Esse método permite que você adicione efeitos sonoros a uma capa, por exemplo, quando os botões são clicados.</span><span class="sxs-lookup"><span data-stu-id="b3737-112">This method allows you to add sound effects to a skin for example, when buttons are clicked.</span></span> <span data-ttu-id="b3737-113">O som é reproduzido pelo sistema operacional diretamente e não pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b3737-113">The sound is played by the operating system directly and not by Windows Media Player.</span></span> <span data-ttu-id="b3737-114">Isso significa que o som não pode ser controlado com as configurações e métodos do Windows Media Player, mas pode ser reproduzido enquanto o Windows Media Player está reproduzindo outro arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="b3737-114">This means that the sound cannot be controlled with Windows Media Player settings and methods, but it can be played while Windows Media Player is playing another digital media file.</span></span>

<span data-ttu-id="b3737-115">Esse método oferece suporte apenas a arquivos WAV.</span><span class="sxs-lookup"><span data-stu-id="b3737-115">This method supports WAV files only.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3737-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3737-116">Requirements</span></span>



| <span data-ttu-id="b3737-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3737-117">Requirement</span></span> | <span data-ttu-id="b3737-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b3737-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b3737-119">Versão</span><span class="sxs-lookup"><span data-stu-id="b3737-119">Version</span></span><br/> | <span data-ttu-id="b3737-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="b3737-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3737-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3737-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3737-122">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="b3737-122">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





