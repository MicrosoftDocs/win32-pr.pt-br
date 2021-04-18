---
title: Evento Player. CurrentMediaItemAvailable
description: O evento CurrentMediaItemAvailable ocorre quando um item de metadados gráfico no item de mídia atual fica disponível. | Evento Player. CurrentMediaItemAvailable
ms.assetid: dc692b14-67d3-4867-8f99-ddfcf7d1610c
keywords:
- Evento CurrentMediaItemAvailable do Windows Media Player
- Evento CurrentMediaItemAvailable Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento CurrentMediaItemAvailable
topic_type:
- apiref
api_name:
- Player.CurrentMediaItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f25d085c354cf18966ec37f822a080db56cf16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760630"
---
# <a name="playercurrentmediaitemavailable-event"></a><span data-ttu-id="0361a-107">Evento Player. CurrentMediaItemAvailable</span><span class="sxs-lookup"><span data-stu-id="0361a-107">Player.CurrentMediaItemAvailable event</span></span>

<span data-ttu-id="0361a-108">O evento **CurrentMediaItemAvailable** ocorre quando um item de metadados gráfico no item de mídia atual fica disponível.</span><span class="sxs-lookup"><span data-stu-id="0361a-108">The **CurrentMediaItemAvailable** event occurs when a graphic metadata item in the current media item becomes available.</span></span>

## <a name="syntax"></a><span data-ttu-id="0361a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0361a-109">Syntax</span></span>


```JScript
Player.CurrentMediaItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a><span data-ttu-id="0361a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0361a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0361a-111">*bstrItemName*</span><span class="sxs-lookup"><span data-stu-id="0361a-111">*bstrItemName*</span></span> 
</dt> <dd>

<span data-ttu-id="0361a-112">**Cadeia de caracteres** que contém o nome do item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="0361a-112">**String** containing the name of the current media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0361a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0361a-113">Return value</span></span>

<span data-ttu-id="0361a-114">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0361a-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0361a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0361a-115">Remarks</span></span>

<span data-ttu-id="0361a-116">Como a reprodução pode começar antes que um item de mídia seja totalmente baixado, todos os gráficos de metadados contidos no item de mídia (como arte de capa do álbum) podem não estar disponíveis quando começam a ser reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="0361a-116">Because playback can begin before a media item is fully downloaded, any metadata graphics contained in the media item (such as album cover art) may not be available when it starts to play.</span></span> <span data-ttu-id="0361a-117">Esse evento alerta quando um item gráfico de metadados termina o download.</span><span class="sxs-lookup"><span data-stu-id="0361a-117">This event alerts you when a metadata graphic item is finished downloading.</span></span> <span data-ttu-id="0361a-118">Em seguida, você pode recuperar o objeto de **mídia** passando o valor de *BstrItemName* para a *mediacollection*. método **getByName** , depois do qual você pode acessar o item gráfico de metadados usando *mídia*. **getItemInfoByType** e especificando o **WM/Picture** para o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="0361a-118">You can then retrieve the **Media** object by passing the value of *bstrItemName* to the *MediaCollection*.**getByName** method, after which you can access the metadata graphic item by using *Media*.**getItemInfoByType** and specifying **WM/Picture** for the attribute name.</span></span>

<span data-ttu-id="0361a-119">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="0361a-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="0361a-120">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="0361a-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="0361a-121">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="0361a-121">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="0361a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0361a-122">Requirements</span></span>



| <span data-ttu-id="0361a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0361a-123">Requirement</span></span> | <span data-ttu-id="0361a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0361a-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0361a-125">Versão</span><span class="sxs-lookup"><span data-stu-id="0361a-125">Version</span></span><br/> | <span data-ttu-id="0361a-126">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0361a-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0361a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0361a-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="0361a-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0361a-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0361a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0361a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0361a-130">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="0361a-130">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="0361a-131">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="0361a-131">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="0361a-132">**Mediacollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="0361a-132">**MediaCollection.getByName**</span></span>](mediacollection-getbyname.md)
</dt> <dt>

[<span data-ttu-id="0361a-133">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="0361a-133">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





