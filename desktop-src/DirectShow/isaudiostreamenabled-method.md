---
description: O método IsAudioStreamEnabled recupera um valor que indica se o fluxo de áudio especificado está habilitado no título atual.
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: Método IsAudioStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92df59479e5729c392eb25b6c6c075a52b4835b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500136"
---
# <a name="isaudiostreamenabled-method"></a><span data-ttu-id="9c734-103">Método IsAudioStreamEnabled</span><span class="sxs-lookup"><span data-stu-id="9c734-103">IsAudioStreamEnabled Method</span></span>

> [!Note]  
> <span data-ttu-id="9c734-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9c734-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9c734-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="9c734-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9c734-106">O `IsAudioStreamEnabled` método recupera um valor que indica se o fluxo de áudio especificado está habilitado no título atual.</span><span class="sxs-lookup"><span data-stu-id="9c734-106">The `IsAudioStreamEnabled` method retrieves a value indicating whether the specified audio stream is enabled in the current title.</span></span>

``` syntax
[bEnabled = ] MSWebDVD.IsAudioStreamEnabled(iStream)
```

## <a name="parameters"></a><span data-ttu-id="9c734-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c734-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c734-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="9c734-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="9c734-109">Especifica o fluxo de áudio como um valor inteiro de 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="9c734-109">Specifies the audio stream as an Integer value from 0 through 7.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c734-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9c734-110">Return Value</span></span>

<span data-ttu-id="9c734-111">Retorna um valor booliano que indica se o fluxo de áudio especificado está disponível para o título atual.</span><span class="sxs-lookup"><span data-stu-id="9c734-111">Returns a Boolean value indicating whether the specified audio stream is available for the current title.</span></span> <span data-ttu-id="9c734-112">Verdadeiro significa que está disponível.</span><span class="sxs-lookup"><span data-stu-id="9c734-112">True means it is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c734-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c734-113">Remarks</span></span>

<span data-ttu-id="9c734-114">Embora um disco possa conter até oito fluxos de áudio independentes, cada fluxo não está necessariamente disponível para cada título.</span><span class="sxs-lookup"><span data-stu-id="9c734-114">Although a disc can contain up to eight independent audio streams, each stream is not necessarily available for each title.</span></span> <span data-ttu-id="9c734-115">Por exemplo, um título de filme principal pode ter três fluxos de áudio para inglês, espanhol e japonês, mas o título "chegando Attractions" pode ter apenas um fluxo de áudio em inglês.</span><span class="sxs-lookup"><span data-stu-id="9c734-115">For example, a main movie title might have three audio streams for English, Spanish, and Japanese, but the "Coming Attractions" title might have only one audio stream in English.</span></span> <span data-ttu-id="9c734-116">Sempre verifique se um fluxo está disponível para um título antes de definir a propriedade [**CurrentAudioStream**](currentaudiostream-property.md) .</span><span class="sxs-lookup"><span data-stu-id="9c734-116">Always verify that a stream is available for a title before setting the [**CurrentAudioStream**](currentaudiostream-property.md) property.</span></span>

 

 



