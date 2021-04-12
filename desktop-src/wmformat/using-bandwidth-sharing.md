---
title: Usando o compartilhamento de largura de banda
description: Usando o compartilhamento de largura de banda
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- SDK do Windows Media Format, compartilhamento de largura de banda
- compartilhamento de largura de banda, sobre
- perfis, compartilhamento de largura de banda
- fluxos, compartilhamento de largura de banda
- compartilhamento de largura de banda, interface IWMProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298c690b484a8b4b5990aacd5d525867da8923c0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104365757"
---
# <a name="using-bandwidth-sharing"></a><span data-ttu-id="24192-108">Usando o compartilhamento de largura de banda</span><span class="sxs-lookup"><span data-stu-id="24192-108">Using Bandwidth Sharing</span></span>

<span data-ttu-id="24192-109">Você pode usar objetos de compartilhamento de largura de banda para especificar que determinados fluxos, quando combinados, não usarão mais largura de banda do que o especificado.</span><span class="sxs-lookup"><span data-stu-id="24192-109">You can use bandwidth sharing objects to specify that certain streams, when combined, will not use more bandwidth than specified.</span></span> <span data-ttu-id="24192-110">As informações em um objeto de compartilhamento de largura de banda não são geradas nem verificadas pelo gravador nem usadas pelo leitor para qualquer coisa.</span><span class="sxs-lookup"><span data-stu-id="24192-110">The information in a bandwidth sharing object is not generated or verified by the writer nor used by the reader for anything.</span></span>

<span data-ttu-id="24192-111">Quando um arquivo é gravado com informações de compartilhamento de largura de banda em seu perfil, os dados são armazenados em sua seção de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="24192-111">When a file is written that has bandwidth sharing information in its profile, the data is stored in its header section.</span></span> <span data-ttu-id="24192-112">Você pode usar a interface [**IWMProfile**](iwmprofile.md) no leitor para verificar se há informações de compartilhamento de largura de banda quando o arquivo é reproduzido.</span><span class="sxs-lookup"><span data-stu-id="24192-112">You can use the [**IWMProfile**](iwmprofile.md) interface in the reader to check for bandwidth sharing information when the file is played.</span></span>

<span data-ttu-id="24192-113">Cada objeto de compartilhamento de largura de banda é definido por duas configurações.</span><span class="sxs-lookup"><span data-stu-id="24192-113">Each bandwidth sharing object is defined by two settings.</span></span> <span data-ttu-id="24192-114">A primeira é a largura de banda, conforme definido por uma largura de banda e uma janela de buffer.</span><span class="sxs-lookup"><span data-stu-id="24192-114">First is the bandwidth, as defined by a bandwidth and a buffer window.</span></span> <span data-ttu-id="24192-115">A segunda configuração é um tipo de compartilhamento de largura de banda, que pode ser exclusivo ou parcial.</span><span class="sxs-lookup"><span data-stu-id="24192-115">The second setting is a bandwidth sharing type, which can be either exclusive or partial.</span></span> <span data-ttu-id="24192-116">O compartilhamento de largura de banda exclusivo significa que os fluxos constituintes são reproduzidos um de cada vez, enquanto os fluxos parciais são entregues simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="24192-116">Exclusive bandwidth sharing means that the constituent streams are played back one at a time, while partial means the streams are delivered concurrently.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24192-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24192-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24192-118">**Interface IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="24192-118">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="24192-119">**IWMProfile3::AddBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="24192-119">**IWMProfile3::AddBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="24192-120">**IWMProfile3::CreateNewBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="24192-120">**IWMProfile3::CreateNewBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="24192-121">**IWMProfile3::GetBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="24192-121">**IWMProfile3::GetBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="24192-122">**IWMProfile3::GetBandwidthSharingCount**</span><span class="sxs-lookup"><span data-stu-id="24192-122">**IWMProfile3::GetBandwidthSharingCount**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount)
</dt> <dt>

[<span data-ttu-id="24192-123">**Trabalhando com perfis**</span><span class="sxs-lookup"><span data-stu-id="24192-123">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




