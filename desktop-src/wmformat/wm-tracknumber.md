---
title: WM/TrackNumber
description: O atributo WM/TrackNumber contém o número de faixa do conteúdo. Esse atributo é baseado em 1.
ms.assetid: cd338cd9-a5de-4311-8089-1d5d90570f69
keywords:
- Formato de mídia do Windows do WM/TrackNumber
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55691335faaf835b270013c6499197c0e3f7bee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105772591"
---
# <a name="wmtracknumber"></a><span data-ttu-id="5abfe-105">WM/TrackNumber</span><span class="sxs-lookup"><span data-stu-id="5abfe-105">WM/TrackNumber</span></span>

<span data-ttu-id="5abfe-106">O atributo **WM/TrackNumber** contém o número de faixa do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5abfe-106">The **WM/TrackNumber** attribute contains the track number of the content.</span></span> <span data-ttu-id="5abfe-107">Esse atributo é baseado em 1.</span><span class="sxs-lookup"><span data-stu-id="5abfe-107">This attribute is 1-based.</span></span>

## <a name="global-constant"></a><span data-ttu-id="5abfe-108">Constante global</span><span class="sxs-lookup"><span data-stu-id="5abfe-108">Global Constant</span></span>

<span data-ttu-id="5abfe-109">g \_ wszWMTrackNumber</span><span class="sxs-lookup"><span data-stu-id="5abfe-109">g\_wszWMTrackNumber</span></span>

## <a name="data-type"></a><span data-ttu-id="5abfe-110">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="5abfe-110">Data Type</span></span>

<span data-ttu-id="5abfe-111">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="5abfe-111">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="5abfe-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5abfe-112">Remarks</span></span>

<span data-ttu-id="5abfe-113">Muitos aplicativos existentes gravam o valor para o **WM/TrackNumber** como um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="5abfe-113">Many existing applications write the value for **WM/TrackNumber** as a **DWORD**.</span></span> <span data-ttu-id="5abfe-114">Se você criar um aplicativo que reproduza arquivos de fontes desconhecidas, deverá incluir o código para lidar com valores de cadeia de caracteres e **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="5abfe-114">If you create an application that plays files from unknown sources, you should include code to handle both string and **DWORD** values.</span></span>

## <a name="see-also"></a><span data-ttu-id="5abfe-115">Veja também</span><span class="sxs-lookup"><span data-stu-id="5abfe-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5abfe-116">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="5abfe-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




