---
title: Settings. invokeURLs
description: A propriedade invokeURLs especifica ou recupera um valor que indica se os eventos de URL devem iniciar um navegador da Web.
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- Settings. invokeURLs Windows Media Player
topic_type:
- apiref
api_name:
- Settings.invokeURLs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb55bb61243e6905a51a943a26adc120511335c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747481"
---
# <a name="settingsinvokeurls"></a><span data-ttu-id="e4506-104">Settings. invokeURLs</span><span class="sxs-lookup"><span data-stu-id="e4506-104">Settings.invokeURLs</span></span>

<span data-ttu-id="e4506-105">A propriedade **invokeURLs** especifica ou recupera um valor que indica se os eventos de URL devem iniciar um navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="e4506-105">The **invokeURLs** property specifies or retrieves a value indicating whether URL events should launch a Web browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4506-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4506-106">Syntax</span></span>

<span data-ttu-id="e4506-107">Player. Settings. invokeURLs</span><span class="sxs-lookup"><span data-stu-id="e4506-107">player.settings.invokeURLs</span></span>

## <a name="possible-values"></a><span data-ttu-id="e4506-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="e4506-108">Possible Values</span></span>

<span data-ttu-id="e4506-109">Esta propriedade é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e4506-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="e4506-110">Valor</span><span class="sxs-lookup"><span data-stu-id="e4506-110">Value</span></span> | <span data-ttu-id="e4506-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4506-111">Description</span></span>                                  |
|-------|----------------------------------------------|
| <span data-ttu-id="e4506-112">true</span><span class="sxs-lookup"><span data-stu-id="e4506-112">true</span></span>  | <span data-ttu-id="e4506-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="e4506-113">Default.</span></span> <span data-ttu-id="e4506-114">Os eventos de URL devem iniciar um navegador.</span><span class="sxs-lookup"><span data-stu-id="e4506-114">URL events should launch a browser.</span></span> |
| <span data-ttu-id="e4506-115">false</span><span class="sxs-lookup"><span data-stu-id="e4506-115">false</span></span> | <span data-ttu-id="e4506-116">Os eventos de URL não devem iniciar um navegador.</span><span class="sxs-lookup"><span data-stu-id="e4506-116">URL events should not launch a browser.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="e4506-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4506-117">Remarks</span></span>

<span data-ttu-id="e4506-118">Os arquivos de mídia podem conter URLs.</span><span class="sxs-lookup"><span data-stu-id="e4506-118">Media files can contain URLs.</span></span> <span data-ttu-id="e4506-119">Quando uma URL é enviada ao controle do Windows Media Player, ela é passada primeiro para o manipulador de eventos **ScriptCommand** , independentemente do valor em **invokeURLs**.</span><span class="sxs-lookup"><span data-stu-id="e4506-119">When a URL is sent to the Windows Media Player control, it is passed first to the **ScriptCommand** event handler regardless of the value in **invokeURLs**.</span></span> <span data-ttu-id="e4506-120">Após o **ScriptCommand** sair, o Windows Media Player verifica o **invokeURLs** para determinar se o navegador da Internet padrão deve ser iniciado com a URL.</span><span class="sxs-lookup"><span data-stu-id="e4506-120">After **ScriptCommand** exits, Windows Media Player checks **invokeURLs** to determine whether to launch the default Internet browser with the URL.</span></span> <span data-ttu-id="e4506-121">Você pode exibir URLs seletivamente, verificando-as em **ScriptCommand** e configurando **invokeURLs** conforme desejado.</span><span class="sxs-lookup"><span data-stu-id="e4506-121">You can selectively display URLs by checking them in **ScriptCommand** and setting **invokeURLs** as desired.</span></span>

<span data-ttu-id="e4506-122">**Windows Media Player 10 Mobile**: essa propriedade só aceita ou retorna false.</span><span class="sxs-lookup"><span data-stu-id="e4506-122">**Windows Media Player 10 Mobile**: This property only accepts or returns false.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4506-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4506-123">Requirements</span></span>



| <span data-ttu-id="e4506-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4506-124">Requirement</span></span> | <span data-ttu-id="e4506-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e4506-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e4506-126">Versão</span><span class="sxs-lookup"><span data-stu-id="e4506-126">Version</span></span><br/> | <span data-ttu-id="e4506-127">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e4506-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e4506-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e4506-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="e4506-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4506-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4506-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4506-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4506-131">**Evento Player. ScriptCommand**</span><span class="sxs-lookup"><span data-stu-id="e4506-131">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="e4506-132">**Objeto de configurações**</span><span class="sxs-lookup"><span data-stu-id="e4506-132">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





