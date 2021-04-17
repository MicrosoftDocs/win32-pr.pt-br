---
title: Atributo SyncState
description: O atributo SyncState é uma representação de cadeia de caracteres de um valor de 32 bits que o Windows Media Player usa quando sincroniza as listas de reprodução com dispositivos portáteis.
ms.assetid: affc3d1c-7fe6-4811-acfc-57285cb181ca
keywords:
- Atributo SyncState Windows Media Player
topic_type:
- apiref
api_name:
- SyncState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a948f6c649d548b375ccb676134177b0273c85c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761581"
---
# <a name="syncstate-attribute"></a><span data-ttu-id="5f047-104">Atributo SyncState</span><span class="sxs-lookup"><span data-stu-id="5f047-104">SyncState Attribute</span></span>

<span data-ttu-id="5f047-105">O atributo **SyncState** é uma representação de cadeia de caracteres de um valor de 32 bits que o Windows Media Player usa quando sincroniza as listas de reprodução com dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="5f047-105">The **SyncState** attribute is a string representation of a 32-bit value that Windows Media Player uses when it synchronizes playlists with portable devices.</span></span>

## <a name="applies-to"></a><span data-ttu-id="5f047-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="5f047-106">Applies To</span></span>

-   [<span data-ttu-id="5f047-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="5f047-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="5f047-108">Outros itens</span><span class="sxs-lookup"><span data-stu-id="5f047-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="5f047-109">Itens de foto</span><span class="sxs-lookup"><span data-stu-id="5f047-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="5f047-110">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="5f047-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="5f047-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f047-111">Remarks</span></span>

<span data-ttu-id="5f047-112">Esse atributo consiste em valores de 16 2 bits, cada um dos quais Especifica o estado de sincronização de um dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="5f047-112">This attribute consists of sixteen 2-bit values, each of which specifies the synchronization state of a portable device.</span></span> <span data-ttu-id="5f047-113">O bit mais significativo (MSB) desse valor de 32 bits corresponde ao dispositivo 16.</span><span class="sxs-lookup"><span data-stu-id="5f047-113">The most significant bit (MSB) of this 32-bit value corresponds to device 16.</span></span> <span data-ttu-id="5f047-114">O bit menos significativo (LSB) corresponde ao dispositivo 1.</span><span class="sxs-lookup"><span data-stu-id="5f047-114">The least significant bit (LSB) corresponds to device 1.</span></span>

<span data-ttu-id="5f047-115">O MSB de cada valor de 2 bits indica se o Windows Media Player sincronizou o conteúdo com o dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="5f047-115">The MSB of each 2-bit value indicates whether Windows Media Player synchronized the content with the corresponding device.</span></span> <span data-ttu-id="5f047-116">Um valor de 1 indica que ele fez.</span><span class="sxs-lookup"><span data-stu-id="5f047-116">A value of 1 indicates that it did.</span></span> <span data-ttu-id="5f047-117">Um valor de 0 indica que ele não foi.</span><span class="sxs-lookup"><span data-stu-id="5f047-117">A value of 0 indicates that it did not.</span></span>

<span data-ttu-id="5f047-118">Se o MSB for 0, o LSB especificará por que a sincronização falhou.</span><span class="sxs-lookup"><span data-stu-id="5f047-118">If the MSB is 0, the LSB specifies why the synchronization failed.</span></span> <span data-ttu-id="5f047-119">Um valor de 1 no LSB indica que não havia espaço livre suficiente para o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5f047-119">A value of 1 in the LSB indicates that there was not enough free space for the content.</span></span> <span data-ttu-id="5f047-120">Um valor de 0 no LSB indica algum outro motivo que impediu a sincronização.</span><span class="sxs-lookup"><span data-stu-id="5f047-120">A value of 0 in the LSB indicates some other reason prevented synchronization.</span></span>

<span data-ttu-id="5f047-121">Para recuperar o estado de sincronização de um determinado dispositivo, você deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5f047-121">To retrieve the synchronization state of a given device, you should do the following:</span></span>

1.  <span data-ttu-id="5f047-122">Invocar **IWMPSyncDevice:: get \_ status** para determinar se um determinado dispositivo está sincronizado.</span><span class="sxs-lookup"><span data-stu-id="5f047-122">Invoke **IWMPSyncDevice::get\_status** to determine whether a given device is synchronized.</span></span>
2.  <span data-ttu-id="5f047-123">Se estiver sincronizada, invoque **IWMPSyncDevice:: get \_ partnershipIndex** para recuperar o índice do par de bits do dispositivo no atributo **SyncState** .</span><span class="sxs-lookup"><span data-stu-id="5f047-123">If it is synchronized, invoke **IWMPSyncDevice::get\_partnershipIndex** to retrieve the index of the device's bit pair in the **SyncState** attribute.</span></span>
3.  <span data-ttu-id="5f047-124">Usando esse índice, mascara o par de bits correspondente do atributo **SyncState** e examine o resultado para determinar o estado de sincronização da lista de reprodução com o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f047-124">Using this index, mask the corresponding bit pair of the **SyncState** attribute and examine the result to determine the synchronization state of the playlist with the device.</span></span>

<span data-ttu-id="5f047-125">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="5f047-125">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f047-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f047-126">Requirements</span></span>



| <span data-ttu-id="5f047-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f047-127">Requirement</span></span> | <span data-ttu-id="5f047-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5f047-128">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="5f047-129">Versão</span><span class="sxs-lookup"><span data-stu-id="5f047-129">Version</span></span><br/> | <span data-ttu-id="5f047-130">Windows Media Player 10 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5f047-130">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f047-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f047-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f047-132">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="5f047-132">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="5f047-133">**Determinando o estado de sincronização da playlist**</span><span class="sxs-lookup"><span data-stu-id="5f047-133">**Determining Playlist Synchronization State**</span></span>](determining-playlist-synchronization-state.md)
</dt> <dt>

[<span data-ttu-id="5f047-134">**IWMPSyncDevice:: obter \_ partnershipIndex**</span><span class="sxs-lookup"><span data-stu-id="5f047-134">**IWMPSyncDevice::get\_partnershipIndex**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[<span data-ttu-id="5f047-135">**IWMPSyncDevice:: obter \_ status**</span><span class="sxs-lookup"><span data-stu-id="5f047-135">**IWMPSyncDevice::get\_status**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 





