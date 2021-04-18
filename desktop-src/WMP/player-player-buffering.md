---
title: Evento Player. buffering
description: O evento de buffer ocorre quando o controle do Windows Media Player começa ou termina o armazenamento em buffer ou o download. | Evento Player. buffering
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Evento de buffer do Windows Media Player
- Evento de buffer do Windows Media Player, classe de Player
- Classe de Player Windows Media Player, evento de buffer
topic_type:
- apiref
api_name:
- Player.Buffering
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a73ac77f9b8e81162a6cc0f9220562caba26eae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793259"
---
# <a name="playerbuffering-event"></a><span data-ttu-id="4972e-107">Evento Player. buffering</span><span class="sxs-lookup"><span data-stu-id="4972e-107">Player.Buffering event</span></span>

<span data-ttu-id="4972e-108">O evento de **buffer** ocorre quando o controle do Windows Media Player começa ou termina o armazenamento em buffer ou o download.</span><span class="sxs-lookup"><span data-stu-id="4972e-108">The **Buffering** event occurs when the Windows Media Player control begins or ends buffering or downloading.</span></span>

## <a name="syntax"></a><span data-ttu-id="4972e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4972e-109">Syntax</span></span>


```JScript
Player.Buffering(
  Start
)
```



## <a name="parameters"></a><span data-ttu-id="4972e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4972e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4972e-111">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="4972e-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="4972e-112">**Booliano** que contém um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4972e-112">**Boolean** containing one of the following values.</span></span>



| <span data-ttu-id="4972e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4972e-113">Value</span></span> | <span data-ttu-id="4972e-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="4972e-114">Description</span></span>            |
|-------|------------------------|
| <span data-ttu-id="4972e-115">true</span><span class="sxs-lookup"><span data-stu-id="4972e-115">true</span></span>  | <span data-ttu-id="4972e-116">O buffer foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="4972e-116">Buffering has started.</span></span> |
| <span data-ttu-id="4972e-117">false</span><span class="sxs-lookup"><span data-stu-id="4972e-117">false</span></span> | <span data-ttu-id="4972e-118">O buffer foi encerrado.</span><span class="sxs-lookup"><span data-stu-id="4972e-118">Buffering has ended.</span></span>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4972e-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4972e-119">Return value</span></span>

<span data-ttu-id="4972e-120">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4972e-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4972e-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="4972e-121">Remarks</span></span>

<span data-ttu-id="4972e-122">Use esse evento para determinar quando o buffer ou o download é iniciado ou interrompido.</span><span class="sxs-lookup"><span data-stu-id="4972e-122">Use this event to determine when buffering or downloading starts or stops.</span></span> <span data-ttu-id="4972e-123">Você pode usar o mesmo bloco de eventos para ambos os casos e para testar a *rede*. **bufferingProgress** e *rede*. **downloadProgress** para determinar se o Windows Media Player está atualmente armazenando em buffer ou baixando conteúdo.</span><span class="sxs-lookup"><span data-stu-id="4972e-123">You can use the same event block for both cases and test *Network*.**bufferingProgress** and *Network*.**downloadProgress** to determine whether Windows Media Player is currently buffering or downloading content.</span></span>

<span data-ttu-id="4972e-124">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="4972e-124">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file by using the parameter name given.</span></span> <span data-ttu-id="4972e-125">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="4972e-125">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="4972e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4972e-126">Requirements</span></span>



| <span data-ttu-id="4972e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4972e-127">Requirement</span></span> | <span data-ttu-id="4972e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="4972e-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4972e-129">Versão</span><span class="sxs-lookup"><span data-stu-id="4972e-129">Version</span></span><br/> | <span data-ttu-id="4972e-130">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="4972e-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4972e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4972e-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="4972e-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4972e-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4972e-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="4972e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4972e-134">**Network. bufferingProgress**</span><span class="sxs-lookup"><span data-stu-id="4972e-134">**Network.bufferingProgress**</span></span>](network-bufferingprogress.md)
</dt> <dt>

[<span data-ttu-id="4972e-135">**Network. downloadProgress**</span><span class="sxs-lookup"><span data-stu-id="4972e-135">**Network.downloadProgress**</span></span>](network-downloadprogress.md)
</dt> <dt>

[<span data-ttu-id="4972e-136">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="4972e-136">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





