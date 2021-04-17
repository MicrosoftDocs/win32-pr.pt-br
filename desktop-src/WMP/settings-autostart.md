---
title: Settings. AutoStart
description: A propriedade AutoStart especifica ou recupera um valor que indica se o item de mídia atual começa a ser reproduzido automaticamente.
ms.assetid: 553f8534-9e3e-4fdc-bfc1-551939969289
keywords:
- Settings. AutoStart Windows Media Player
topic_type:
- apiref
api_name:
- Settings.autoStart
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d08b8f84f4a0b51225ed5692a25fa41cab809ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747699"
---
# <a name="settingsautostart"></a><span data-ttu-id="0c388-104">Settings. AutoStart</span><span class="sxs-lookup"><span data-stu-id="0c388-104">Settings.autoStart</span></span>

<span data-ttu-id="0c388-105">A propriedade **AutoStart** especifica ou recupera um valor que indica se o item de mídia atual começa a ser reproduzido automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0c388-105">The **autoStart** property specifies or retrieves a value indicating whether the current media item begins playing automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c388-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c388-106">Syntax</span></span>

<span data-ttu-id="0c388-107">Player. Settings. AutoStart</span><span class="sxs-lookup"><span data-stu-id="0c388-107">player.settings.autoStart</span></span>

## <a name="possible-values"></a><span data-ttu-id="0c388-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="0c388-108">Possible Values</span></span>

<span data-ttu-id="0c388-109">Esta propriedade é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0c388-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="0c388-110">Valor</span><span class="sxs-lookup"><span data-stu-id="0c388-110">Value</span></span> | <span data-ttu-id="0c388-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c388-111">Description</span></span>                                                         |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="0c388-112">true</span><span class="sxs-lookup"><span data-stu-id="0c388-112">true</span></span>  | <span data-ttu-id="0c388-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="0c388-113">Default.</span></span> <span data-ttu-id="0c388-114">O item de mídia começa a ser reproduzido automaticamente (consulte comentários).</span><span class="sxs-lookup"><span data-stu-id="0c388-114">The media item begins playing automatically (see Remarks).</span></span> |
| <span data-ttu-id="0c388-115">false</span><span class="sxs-lookup"><span data-stu-id="0c388-115">false</span></span> | <span data-ttu-id="0c388-116">O item de mídia não começa a ser reproduzido automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0c388-116">The media item does not begin playing automatically.</span></span>                |



 

## <a name="remarks"></a><span data-ttu-id="0c388-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c388-117">Remarks</span></span>

<span data-ttu-id="0c388-118">Se **AutoStart** for definido como true, o item de mídia começará a ser reproduzido quando o *Player*. **URL**, *Player*. **currentPlaylist** ou *Player*. **currentMedia** está definido.</span><span class="sxs-lookup"><span data-stu-id="0c388-118">If **autoStart** is set to true, the media item will begin playing when *Player*.**URL**, *Player*.**currentPlaylist**, or *Player*.**currentMedia** is set.</span></span> <span data-ttu-id="0c388-119">Caso contrário, ele não começará a ser reproduzido até os *controles*. o método **Play** é chamado.</span><span class="sxs-lookup"><span data-stu-id="0c388-119">Otherwise, it will not start playing until the *Controls*.**play** method is called.</span></span>

<span data-ttu-id="0c388-120">Como a propriedade **AutoStart** para o modo completo do Windows Media Player pode ser definida globalmente por eventos externos (como carregar um CD), não há nenhum valor padrão confiável para capas e controles de Player remotos.</span><span class="sxs-lookup"><span data-stu-id="0c388-120">Because the **autoStart** property for the full mode of Windows Media Player can be set globally by external events (such as loading a CD), there is no reliable default value for skins and remoted Player controls.</span></span> <span data-ttu-id="0c388-121">Isso ocorre porque o mecanismo de reprodução do player de modo completo é usado em ambos os casos.</span><span class="sxs-lookup"><span data-stu-id="0c388-121">This is because the playback engine of the full mode Player is used in both cases.</span></span>

<span data-ttu-id="0c388-122">Você deve definir **AutoStart** como false imediatamente antes de definir o *Player*. **URL**, *Player*. **currentPlaylist** ou *Player*. **currentMedia** em capas e controles remotos do Windows Media Player se você quiser garantir que o item de mídia não comece a ser reproduzido imediatamente.</span><span class="sxs-lookup"><span data-stu-id="0c388-122">You should set **autoStart** to false immediately before you set *Player*.**URL**, *Player*.**currentPlaylist**, or *Player*.**currentMedia** in skins and remoted Windows Media Player controls if you want to ensure that the media item does not start playing immediately.</span></span> <span data-ttu-id="0c388-123">Além disso, a menos que você defina **AutoStart** como true imediatamente antes de especificar um item de mídia, você não deve confiar nessa configuração como um substituto para usar os *controles*. método **Play** .</span><span class="sxs-lookup"><span data-stu-id="0c388-123">Also, unless you set **autostart** to true immediately before specifying a media item, you should not rely on this setting as a substitute for using the *Controls*.**play** method.</span></span>

## <a name="examples"></a><span data-ttu-id="0c388-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0c388-124">Examples</span></span>

<span data-ttu-id="0c388-125">O exemplo a seguir cria um elemento de caixa de seleção HTML que permite ao usuário especificar se o controle de jogador reproduz o item de mídia atual automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0c388-125">The following example creates an HTML CHECKBOX element that allows the user to specify whether the Player control plays the current media item automatically.</span></span> <span data-ttu-id="0c388-126">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="0c388-126">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX" ID = AS
              onClick = "
    /* Use the CHECKBOX state to specify the value 
       of the autoStart property. */
    Player.settings.autoStart = AS.checked;
"> 

```



## <a name="requirements"></a><span data-ttu-id="0c388-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c388-127">Requirements</span></span>



| <span data-ttu-id="0c388-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c388-128">Requirement</span></span> | <span data-ttu-id="0c388-129">Valor</span><span class="sxs-lookup"><span data-stu-id="0c388-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0c388-130">Versão</span><span class="sxs-lookup"><span data-stu-id="0c388-130">Version</span></span><br/> | <span data-ttu-id="0c388-131">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0c388-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0c388-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0c388-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="0c388-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c388-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c388-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c388-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c388-135">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="0c388-135">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="0c388-136">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="0c388-136">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="0c388-137">**Objeto de configurações**</span><span class="sxs-lookup"><span data-stu-id="0c388-137">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





