---
title: Atributos de sincronização
description: Os atributos Sync01 por meio de Sync16 são representações de cadeia de caracteres de valores de 32 bits que o Windows Media Player usa quando sincroniza as listas de reprodução com um de até 16 dispositivos portáteis.
ms.assetid: b9ae3420-aa09-4969-8637-f16d438942f3
keywords:
- Atributos de sincronização Windows Media Player
topic_type:
- apiref
api_name:
- Sync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af26ae563a38efcc40b0bcd319c5fc62b4776dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787612"
---
# <a name="sync-attributes"></a><span data-ttu-id="3e82c-104">Atributos de sincronização</span><span class="sxs-lookup"><span data-stu-id="3e82c-104">Sync Attributes</span></span>

<span data-ttu-id="3e82c-105">Os atributos **Sync01** por meio de **Sync16** são representações de cadeia de caracteres de valores de 32 bits que o Windows Media Player usa quando sincroniza as listas de reprodução com um de até 16 dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="3e82c-105">The **Sync01** through **Sync16** attributes are string representations of 32-bit values that Windows Media Player uses when it synchronizes playlists with one of up to 16 portable devices.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3e82c-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="3e82c-106">Applies To</span></span>

-   [<span data-ttu-id="3e82c-107">Playlists</span><span class="sxs-lookup"><span data-stu-id="3e82c-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="3e82c-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e82c-108">Remarks</span></span>

<span data-ttu-id="3e82c-109">Esses são atributos de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3e82c-109">These are read/write attributes.</span></span> <span data-ttu-id="3e82c-110">Um valor de zero indica que o Windows Media Player não deve sincronizar a lista de reprodução com o dispositivo associado.</span><span class="sxs-lookup"><span data-stu-id="3e82c-110">A value of zero indicates that Windows Media Player should not synchronize the playlist with the associated device.</span></span> <span data-ttu-id="3e82c-111">Um valor maior que zero indica uma prioridade de sincronização para a lista de reprodução fornecida.</span><span class="sxs-lookup"><span data-stu-id="3e82c-111">A value greater than zero indicates a synchronization priority for the given playlist.</span></span>

<span data-ttu-id="3e82c-112">Com base na entrada do usuário, o Windows Media Player define esse atributo para cada uma das listas de reprodução na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3e82c-112">Based on user input, Windows Media Player sets this attribute for each of the playlists in the library.</span></span> <span data-ttu-id="3e82c-113">Quando o Windows Media Player tenta sincronizar uma lista de reprodução com um dispositivo portátil, ele examina cada playlist para comparar os valores dos atributos **Sync**_XX_ que representam a parceria do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e82c-113">When Windows Media Player attempts to synchronize a playlist with a portable device, it examines each playlist to compare the values for the **Sync**_XX_ attributes that represent the device partnership.</span></span> <span data-ttu-id="3e82c-114">As listas de reprodução que têm valores menores de **sincronização**_XX_ recebem prioridade de sincronização maior.</span><span class="sxs-lookup"><span data-stu-id="3e82c-114">Playlists that have lower **Sync**_XX_ values receive higher synchronization priority.</span></span>

<span data-ttu-id="3e82c-115">Por exemplo, a biblioteca pode conter as quatro listas de reprodução a seguir e os respectivos valores de **sincronização**_XX_ :</span><span class="sxs-lookup"><span data-stu-id="3e82c-115">For example, the library might contain the following four playlists and respective **Sync**_XX_ values:</span></span>



| <span data-ttu-id="3e82c-116">Nome da playlist</span><span class="sxs-lookup"><span data-stu-id="3e82c-116">Playlist Name</span></span> | <span data-ttu-id="3e82c-117">Valor de Sync01</span><span class="sxs-lookup"><span data-stu-id="3e82c-117">Sync01 Value</span></span> |
|---------------|--------------|
| <span data-ttu-id="3e82c-118">GymMusic. WPL</span><span class="sxs-lookup"><span data-stu-id="3e82c-118">GymMusic.WPL</span></span>  | <span data-ttu-id="3e82c-119">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="3e82c-119">0x0000000D</span></span>   |
| <span data-ttu-id="3e82c-120">Relaxar. WPL</span><span class="sxs-lookup"><span data-stu-id="3e82c-120">Relax.WPL</span></span>     | <span data-ttu-id="3e82c-121">0x00000020</span><span class="sxs-lookup"><span data-stu-id="3e82c-121">0x00000020</span></span>   |
| <span data-ttu-id="3e82c-122">DriveHome. WPL</span><span class="sxs-lookup"><span data-stu-id="3e82c-122">DriveHome.WPL</span></span> | <span data-ttu-id="3e82c-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3e82c-123">0x00000001</span></span>   |
| <span data-ttu-id="3e82c-124">NoGo. WPL</span><span class="sxs-lookup"><span data-stu-id="3e82c-124">NoGo.WPL</span></span>      | <span data-ttu-id="3e82c-125">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e82c-125">0x00000000</span></span>   |



 

<span data-ttu-id="3e82c-126">Quando o Windows Media Player sincroniza o dispositivo associado ao atributo, ele sincronizará as listas de reprodução na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="3e82c-126">When Windows Media Player synchronizes the device associated with the attribute, it will synchronize the playlists in the following order:</span></span>

1.  <span data-ttu-id="3e82c-127">DriveHome. WPL</span><span class="sxs-lookup"><span data-stu-id="3e82c-127">DriveHome.WPL</span></span>
2.  <span data-ttu-id="3e82c-128">GymMusic. WPL</span><span class="sxs-lookup"><span data-stu-id="3e82c-128">GymMusic.WPL</span></span>
3.  <span data-ttu-id="3e82c-129">Relaxar. WPL</span><span class="sxs-lookup"><span data-stu-id="3e82c-129">Relax.WPL</span></span>

<span data-ttu-id="3e82c-130">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="3e82c-130">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e82c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e82c-131">Requirements</span></span>



| <span data-ttu-id="3e82c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e82c-132">Requirement</span></span> | <span data-ttu-id="3e82c-133">Valor</span><span class="sxs-lookup"><span data-stu-id="3e82c-133">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="3e82c-134">Versão</span><span class="sxs-lookup"><span data-stu-id="3e82c-134">Version</span></span><br/> | <span data-ttu-id="3e82c-135">Windows Media Player 10 ou posterior</span><span class="sxs-lookup"><span data-stu-id="3e82c-135">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3e82c-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e82c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e82c-137">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="3e82c-137">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="3e82c-138">**Enumerando listas de reprodução de sincronização**</span><span class="sxs-lookup"><span data-stu-id="3e82c-138">**Enumerating Synchronization Playlists**</span></span>](enumerating-synchronization-playlists.md)
</dt> </dl>

 

 





