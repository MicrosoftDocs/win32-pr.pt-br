---
title: WM/Track
description: O atributo WM/Track contém o número de faixa do conteúdo. Esse atributo é baseado em zero e tem suporte para compatibilidade com versões anteriores. Em vez disso, o novo conteúdo deve usar o atributo WM/TrackNumber.
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- Formato de mídia do WM/Track Windows
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 244426175ea74bc0281f8822964c2fc0bfa37aa7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364591"
---
# <a name="wmtrack"></a><span data-ttu-id="c4302-106">WM/Track</span><span class="sxs-lookup"><span data-stu-id="c4302-106">WM/Track</span></span>

<span data-ttu-id="c4302-107">O atributo **WM/Track** contém o número de faixa do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c4302-107">The **WM/Track** attribute contains the track number of the content.</span></span> <span data-ttu-id="c4302-108">Esse atributo é baseado em zero e tem suporte para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="c4302-108">This attribute is zero-based and is supported for backward compatibility.</span></span> <span data-ttu-id="c4302-109">Em vez disso, o novo conteúdo deve usar o atributo [**WM/TrackNumber**](wm-tracknumber.md) .</span><span class="sxs-lookup"><span data-stu-id="c4302-109">New content should use the [**WM/TrackNumber**](wm-tracknumber.md) attribute instead.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c4302-110">Constante global</span><span class="sxs-lookup"><span data-stu-id="c4302-110">Global Constant</span></span>

<span data-ttu-id="c4302-111">g \_ wszWMTrack</span><span class="sxs-lookup"><span data-stu-id="c4302-111">g\_wszWMTrack</span></span>

## <a name="data-type"></a><span data-ttu-id="c4302-112">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="c4302-112">Data Type</span></span>

<span data-ttu-id="c4302-113">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="c4302-113">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="c4302-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4302-114">Remarks</span></span>

<span data-ttu-id="c4302-115">Muitos aplicativos existentes gravam o valor do **WM/Track** como um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="c4302-115">Many existing applications write the value for **WM/Track** as a **DWORD**.</span></span> <span data-ttu-id="c4302-116">Se você criar um aplicativo que reproduza arquivos de fontes desconhecidas, deverá incluir o código para lidar com valores de cadeia de caracteres e **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c4302-116">If you create an application that plays files from unknown sources, you should include code to handle both string and **DWORD** values.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4302-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4302-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4302-118">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="c4302-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




