---
title: WM/WMADRCAverageTarget
description: O atributo WM/WMADRCAverageTarget contém o nível médio de volume solicitado pelo usuário. Esse valor é usado pelo Windows Media Player para controle de intervalo dinâmico.
ms.assetid: 8173b5ab-27e4-4af9-aea8-6c1310f065f5
keywords:
- Formato de mídia do Windows do WM/WMADRCAverageTarget
topic_type:
- apiref
api_name:
- WM/WMADRCAverageTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 387eed9112e8e0d79943b99bf326b07f42f425d1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105797589"
---
# <a name="wmwmadrcaveragetarget"></a><span data-ttu-id="3b023-105">WM/WMADRCAverageTarget</span><span class="sxs-lookup"><span data-stu-id="3b023-105">WM/WMADRCAverageTarget</span></span>

<span data-ttu-id="3b023-106">O atributo **WM/WMADRCAverageTarget** contém o nível médio de volume solicitado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3b023-106">The **WM/WMADRCAverageTarget** attribute contains the average volume level requested by the user.</span></span> <span data-ttu-id="3b023-107">Esse valor é usado pelo Windows Media Player para controle de intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="3b023-107">This value is used by Windows Media Player for dynamic range control.</span></span>

## <a name="global-constant"></a><span data-ttu-id="3b023-108">Constante global</span><span class="sxs-lookup"><span data-stu-id="3b023-108">Global Constant</span></span>

<span data-ttu-id="3b023-109">g \_ wszWMWMADRCAverageTarget</span><span class="sxs-lookup"><span data-stu-id="3b023-109">g\_wszWMWMADRCAverageTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="3b023-110">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="3b023-110">Data Type</span></span>

<span data-ttu-id="3b023-111">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3b023-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="3b023-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b023-112">Remarks</span></span>

<span data-ttu-id="3b023-113">Há quatro atributos usados pelo Windows Media Player para o controle de intervalo dinâmico: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** e **WM/WMADRCPeakTarget**.</span><span class="sxs-lookup"><span data-stu-id="3b023-113">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="3b023-114">Todos esses valores são definidos pelo gravador com base nas informações do codec ao gravar fluxos com o codec do Windows Media Audio 9 ou o Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="3b023-114">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="3b023-115">Os valores médios são definidos como o nível médio de volume do fluxo e os valores de pico são definidos para o nível máximo do volume no fluxo.</span><span class="sxs-lookup"><span data-stu-id="3b023-115">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="3b023-116">Os valores de referência são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3b023-116">The reference values are read-only.</span></span> <span data-ttu-id="3b023-117">Os valores de destino são definidos pelo Windows Media Player quando o arquivo está sendo reproduzido para registrar as preferências de controle de intervalo dinâmico do usuário.</span><span class="sxs-lookup"><span data-stu-id="3b023-117">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b023-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b023-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b023-119">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="3b023-119">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="3b023-120">**WM/WMADRCAverageReference**</span><span class="sxs-lookup"><span data-stu-id="3b023-120">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="3b023-121">**WM/WMADRCPeakReference**</span><span class="sxs-lookup"><span data-stu-id="3b023-121">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> <dt>

[<span data-ttu-id="3b023-122">**WM/WMADRCPeakTarget**</span><span class="sxs-lookup"><span data-stu-id="3b023-122">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




