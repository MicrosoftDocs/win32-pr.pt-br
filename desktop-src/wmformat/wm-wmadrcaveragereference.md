---
title: WM/WMADRCAverageReference
description: O atributo WM/WMADRCAverageReference contém o nível médio de volume do arquivo como codificado.
ms.assetid: 994614e3-06e2-48f0-bdac-6de5ab0c0eff
keywords:
- Formato de mídia do Windows do WM/WMADRCAverageReference
topic_type:
- apiref
api_name:
- WM/WMADRCAverageReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7059b68658d070ca71a738a5e20658474139558
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105763077"
---
# <a name="wmwmadrcaveragereference"></a><span data-ttu-id="1e6d8-104">WM/WMADRCAverageReference</span><span class="sxs-lookup"><span data-stu-id="1e6d8-104">WM/WMADRCAverageReference</span></span>

<span data-ttu-id="1e6d8-105">O atributo **WM/WMADRCAverageReference** contém o nível médio de volume do arquivo como codificado.</span><span class="sxs-lookup"><span data-stu-id="1e6d8-105">The **WM/WMADRCAverageReference** attribute contains the average volume level of the file as encoded.</span></span>

## <a name="global-constant"></a><span data-ttu-id="1e6d8-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="1e6d8-106">Global Constant</span></span>

<span data-ttu-id="1e6d8-107">g \_ wszWMWMADRCAverageReference</span><span class="sxs-lookup"><span data-stu-id="1e6d8-107">g\_wszWMWMADRCAverageReference</span></span>

## <a name="data-type"></a><span data-ttu-id="1e6d8-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="1e6d8-108">Data Type</span></span>

<span data-ttu-id="1e6d8-109">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1e6d8-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="1e6d8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e6d8-110">Remarks</span></span>

<span data-ttu-id="1e6d8-111">Há quatro atributos usados pelo Windows Media Player para o controle de intervalo dinâmico: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** e **WM/WMADRCPeakTarget**.</span><span class="sxs-lookup"><span data-stu-id="1e6d8-111">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="1e6d8-112">Todos esses valores são definidos pelo gravador com base nas informações do codec ao gravar fluxos com o codec do Windows Media Audio 9 ou o Windows Media Audio 9 Professional.</span><span class="sxs-lookup"><span data-stu-id="1e6d8-112">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="1e6d8-113">Os valores médios são definidos como o nível médio de volume do fluxo e os valores de pico são definidos para o nível máximo do volume no fluxo.</span><span class="sxs-lookup"><span data-stu-id="1e6d8-113">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="1e6d8-114">Os valores de referência são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="1e6d8-114">The reference values are read-only.</span></span> <span data-ttu-id="1e6d8-115">Os valores de destino são definidos pelo Windows Media Player quando o arquivo está sendo reproduzido para registrar as preferências de controle de intervalo dinâmico do usuário.</span><span class="sxs-lookup"><span data-stu-id="1e6d8-115">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e6d8-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e6d8-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e6d8-117">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="1e6d8-117">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="1e6d8-118">**WM/WMADRCAverageTarget**</span><span class="sxs-lookup"><span data-stu-id="1e6d8-118">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="1e6d8-119">**WM/WMADRCPeakReference**</span><span class="sxs-lookup"><span data-stu-id="1e6d8-119">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> <dt>

[<span data-ttu-id="1e6d8-120">**WM/WMADRCPeakTarget**</span><span class="sxs-lookup"><span data-stu-id="1e6d8-120">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




