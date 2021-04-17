---
title: Player. stretchToFit
description: A propriedade stretchToFit especifica ou recupera um valor que indica se o vídeo exibido pelo controle do Windows Media Player é dimensionado automaticamente para se ajustar à janela de vídeo, quando a janela de vídeo é maior do que as dimensões da imagem de vídeo.
ms.assetid: 9ea02959-602e-4bac-a8aa-dce502d1bb54
keywords:
- Player. stretchToFit Windows Media Player
topic_type:
- apiref
api_name:
- Player.stretchToFit
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7b68042cf2a5bd0e7f718d1e19641edecdf548
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797641"
---
# <a name="playerstretchtofit"></a><span data-ttu-id="8e1f8-104">Player. stretchToFit</span><span class="sxs-lookup"><span data-stu-id="8e1f8-104">Player.stretchToFit</span></span>

<span data-ttu-id="8e1f8-105">A propriedade **stretchToFit** especifica ou recupera um valor que indica se o vídeo exibido pelo controle do Windows Media Player é dimensionado automaticamente para se ajustar à janela de vídeo, quando a janela de vídeo é maior do que as dimensões da imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-105">The **stretchToFit** property specifies or retrieves a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window, when the video window is larger than the dimensions of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e1f8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e1f8-106">Syntax</span></span>

<span data-ttu-id="8e1f8-107">*Player*. **stretchToFit**</span><span class="sxs-lookup"><span data-stu-id="8e1f8-107">*player*.**stretchToFit**</span></span>

## <a name="possible-values"></a><span data-ttu-id="8e1f8-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="8e1f8-108">Possible Values</span></span>

<span data-ttu-id="8e1f8-109">Esta propriedade é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="8e1f8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="8e1f8-110">Value</span></span> | <span data-ttu-id="8e1f8-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e1f8-111">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="8e1f8-112">true</span><span class="sxs-lookup"><span data-stu-id="8e1f8-112">true</span></span>  | <span data-ttu-id="8e1f8-113">O vídeo será alongado para se ajustar à janela.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-113">The video will stretch to fit the window.</span></span>              |
| <span data-ttu-id="8e1f8-114">false</span><span class="sxs-lookup"><span data-stu-id="8e1f8-114">false</span></span> | <span data-ttu-id="8e1f8-115">Padrão.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-115">Default.</span></span> <span data-ttu-id="8e1f8-116">O vídeo não será ampliado para se ajustar à janela.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-116">The video will not stretch to fit the window.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8e1f8-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e1f8-117">Remarks</span></span>

<span data-ttu-id="8e1f8-118">Quando **stretchToFit** é definido como true, o controle do Windows Media Player mantém a taxa de proporção original do vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-118">When **stretchToFit** is set to true, the Windows Media Player control maintains the original aspect ratio of the video.</span></span> <span data-ttu-id="8e1f8-119">Se a taxa de proporção do vídeo não corresponder à taxa de proporção da janela de vídeo, as áreas de máscara preta poderão aparecer na parte superior e inferior, ou à esquerda e à direita da imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-119">If the aspect ratio of the video does not match the aspect ratio of the video window, black mask areas may appear on either the top and the bottom, or left and right, of the video image.</span></span>

<span data-ttu-id="8e1f8-120">Essa propriedade se aplica ao controle do Windows Media Player somente quando inserida em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-120">This property applies to the Windows Media Player control only when embedded in a webpage.</span></span>

<span data-ttu-id="8e1f8-121">**Windows Media Player 10 Mobile:** Não há suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-121">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e1f8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e1f8-122">Requirements</span></span>



| <span data-ttu-id="8e1f8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e1f8-123">Requirement</span></span> | <span data-ttu-id="8e1f8-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8e1f8-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e1f8-125">Versão</span><span class="sxs-lookup"><span data-stu-id="8e1f8-125">Version</span></span><br/> | <span data-ttu-id="8e1f8-126">Windows Media Player versão 7,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="8e1f8-126">Windows Media Player version 7.1 or later.</span></span><br/>                              |
| <span data-ttu-id="8e1f8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8e1f8-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="8e1f8-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e1f8-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e1f8-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e1f8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e1f8-130">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="8e1f8-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





