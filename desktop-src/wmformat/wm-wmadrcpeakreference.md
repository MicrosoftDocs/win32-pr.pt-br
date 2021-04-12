---
title: WM/WMADRCPeakReference
description: O atributo WM/WMADRCPeakReference contém o nível máximo de volume do arquivo como codificado. Esse valor é usado pelo Windows Media Player para controle de intervalo dinâmico. Esse valor é definido pelo codec e é somente leitura.
ms.assetid: c732ee88-437b-4970-8f17-61aed2d91022
keywords:
- Formato de mídia do Windows do WM/WMADRCPeakReference
topic_type:
- apiref
api_name:
- WM/WMADRCPeakReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59660f950c748c45a1affccee10ae86e38998f23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364906"
---
# <a name="wmwmadrcpeakreference"></a><span data-ttu-id="82593-106">WM/WMADRCPeakReference</span><span class="sxs-lookup"><span data-stu-id="82593-106">WM/WMADRCPeakReference</span></span>

<span data-ttu-id="82593-107">O atributo **WM/WMADRCPeakReference** contém o nível máximo de volume do arquivo como codificado.</span><span class="sxs-lookup"><span data-stu-id="82593-107">The **WM/WMADRCPeakReference** attribute contains the maximum volume level of the file as encoded.</span></span> <span data-ttu-id="82593-108">Esse valor é usado pelo Windows Media Player para controle de intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="82593-108">This value is used by Windows Media Player for dynamic range control.</span></span> <span data-ttu-id="82593-109">Esse valor é definido pelo codec e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="82593-109">This value is set by the codec and is read-only.</span></span>

## <a name="global-constant"></a><span data-ttu-id="82593-110">Constante global</span><span class="sxs-lookup"><span data-stu-id="82593-110">Global Constant</span></span>

<span data-ttu-id="82593-111">g \_ wszWMWMADRCPeakReference</span><span class="sxs-lookup"><span data-stu-id="82593-111">g\_wszWMWMADRCPeakReference</span></span>

## <a name="data-type"></a><span data-ttu-id="82593-112">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="82593-112">Data Type</span></span>

<span data-ttu-id="82593-113">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="82593-113">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="82593-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="82593-114">Remarks</span></span>

<span data-ttu-id="82593-115">Há quatro atributos usados pelo Windows Media Player para o controle de intervalo dinâmico: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** e **WM/WMADRCPeakTarget**.</span><span class="sxs-lookup"><span data-stu-id="82593-115">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="82593-116">Todos esses valores são definidos pelo gravador com base nas informações do codec ao gravar fluxos com o codec do Windows Media Audio 9 ou o Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="82593-116">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="82593-117">Os valores médios são definidos como o nível médio de volume do fluxo e os valores de pico são definidos para o nível máximo do volume no fluxo.</span><span class="sxs-lookup"><span data-stu-id="82593-117">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="82593-118">Os valores de referência são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="82593-118">The reference values are read-only.</span></span> <span data-ttu-id="82593-119">Os valores de destino são definidos pelo Windows Media Player quando o arquivo está sendo reproduzido para registrar as preferências de controle de intervalo dinâmico do usuário.</span><span class="sxs-lookup"><span data-stu-id="82593-119">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="82593-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="82593-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82593-121">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="82593-121">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="82593-122">**WM/WMADRCAverageReference**</span><span class="sxs-lookup"><span data-stu-id="82593-122">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="82593-123">**WM/WMADRCAverageTarget**</span><span class="sxs-lookup"><span data-stu-id="82593-123">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="82593-124">**WM/WMADRCPeakTarget**</span><span class="sxs-lookup"><span data-stu-id="82593-124">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




