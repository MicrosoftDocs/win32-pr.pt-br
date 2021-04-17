---
title: Player. windowlessVideo
description: A propriedade windowlessVideo especifica ou recupera um valor que indica se o controle do Windows Media Player renderiza o vídeo no modo sem janela.
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- Player. windowlessVideo Windows Media Player
topic_type:
- apiref
api_name:
- Player.windowlessVideo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93f4a8a2b70a42cd0893d463eccca0427dde6c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772981"
---
# <a name="playerwindowlessvideo"></a><span data-ttu-id="dbff0-104">Player. windowlessVideo</span><span class="sxs-lookup"><span data-stu-id="dbff0-104">Player.windowlessVideo</span></span>

<span data-ttu-id="dbff0-105">A propriedade **windowlessVideo** especifica ou recupera um valor que indica se o controle do Windows Media Player renderiza o vídeo no modo sem janela.</span><span class="sxs-lookup"><span data-stu-id="dbff0-105">The **windowlessVideo** property specifies or retrieves a value indicating whether the Windows Media Player control renders video in windowless mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbff0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbff0-106">Syntax</span></span>

<span data-ttu-id="dbff0-107">*Player*. **windowlessVideo**</span><span class="sxs-lookup"><span data-stu-id="dbff0-107">*player*.**windowlessVideo**</span></span>

## <a name="possible-values"></a><span data-ttu-id="dbff0-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="dbff0-108">Possible Values</span></span>

<span data-ttu-id="dbff0-109">Essa propriedade é um **booliano** que é especificado em tempo de design e é somente leitura daí em diante.</span><span class="sxs-lookup"><span data-stu-id="dbff0-109">This property is a **Boolean** that is specified at design time and is read-only thereafter.</span></span>



| <span data-ttu-id="dbff0-110">Valor</span><span class="sxs-lookup"><span data-stu-id="dbff0-110">Value</span></span> | <span data-ttu-id="dbff0-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="dbff0-111">Description</span></span>                                      |
|-------|--------------------------------------------------|
| <span data-ttu-id="dbff0-112">true</span><span class="sxs-lookup"><span data-stu-id="dbff0-112">true</span></span>  | <span data-ttu-id="dbff0-113">O vídeo é renderizado no modo sem janela.</span><span class="sxs-lookup"><span data-stu-id="dbff0-113">The video is rendered in windowless mode.</span></span>        |
| <span data-ttu-id="dbff0-114">false</span><span class="sxs-lookup"><span data-stu-id="dbff0-114">false</span></span> | <span data-ttu-id="dbff0-115">Padrão.</span><span class="sxs-lookup"><span data-stu-id="dbff0-115">Default.</span></span> <span data-ttu-id="dbff0-116">O vídeo é renderizado no modo de janela.</span><span class="sxs-lookup"><span data-stu-id="dbff0-116">The video is rendered in windowed mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="dbff0-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbff0-117">Remarks</span></span>

<span data-ttu-id="dbff0-118">Por padrão, um controle do Windows Media Player inserido renderiza o vídeo em sua própria janela dentro da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="dbff0-118">By default, an embedded Windows Media Player control renders video in its own window within the client area.</span></span> <span data-ttu-id="dbff0-119">Quando **windowlessVideo** é definido como true, o controle de jogador renderiza o vídeo diretamente na área do cliente, para que você possa aplicar efeitos especiais ou colocar o vídeo em camadas com texto.</span><span class="sxs-lookup"><span data-stu-id="dbff0-119">When **windowlessVideo** is set to true, the Player control renders video directly in the client area, so you can apply special effects or layer the video with text.</span></span>

<span data-ttu-id="dbff0-120">No Windows Vista, o vídeo de renderização no modo sem janela pode prejudicar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="dbff0-120">In Windows Vista, rendering video in windowless mode can degrade performance.</span></span>

<span data-ttu-id="dbff0-121">Não há suporte para a propriedade **windowlessVideo** no Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="dbff0-121">The **windowlessVideo** property is not supported for Netscape Navigator.</span></span> <span data-ttu-id="dbff0-122">Definir um valor para essa propriedade no navegador pode gerar resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="dbff0-122">Setting a value for this property in Navigator may yield unexpected results.</span></span>

<span data-ttu-id="dbff0-123">**Windows Media Player 10 Mobile:** Não há suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="dbff0-123">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbff0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbff0-124">Requirements</span></span>



| <span data-ttu-id="dbff0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbff0-125">Requirement</span></span> | <span data-ttu-id="dbff0-126">Valor</span><span class="sxs-lookup"><span data-stu-id="dbff0-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dbff0-127">Versão</span><span class="sxs-lookup"><span data-stu-id="dbff0-127">Version</span></span><br/> | <span data-ttu-id="dbff0-128">Windows Media Player para Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="dbff0-128">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="dbff0-129">DLL</span><span class="sxs-lookup"><span data-stu-id="dbff0-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="dbff0-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbff0-130"><dt>Wmp.dll</dt></span></span> </dl> |



 

 





