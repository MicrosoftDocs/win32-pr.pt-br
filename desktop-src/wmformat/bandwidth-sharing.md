---
title: Compartilhamento de largura de banda
description: Compartilhamento de largura de banda
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- SDK do Windows Media Format, compartilhamento de largura de banda
- ASF (Advanced Systems Format), compartilhamento de largura de banda
- ASF (formato de sistemas avançados), compartilhamento de largura de banda
- SDK do Windows Media Format, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- compartilhamento de largura de banda, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2221d2fbc44654af7f12acf6e45fb85ca32b7d2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007132"
---
# <a name="bandwidth-sharing"></a><span data-ttu-id="38ca6-110">Compartilhamento de largura de banda</span><span class="sxs-lookup"><span data-stu-id="38ca6-110">Bandwidth Sharing</span></span>

<span data-ttu-id="38ca6-111">Você pode especificar fluxos em um arquivo que, quando agrupados, usem menos largura de banda do que a soma das taxas de bits declaradas combinadas.</span><span class="sxs-lookup"><span data-stu-id="38ca6-111">You can specify streams in a file that, when taken together, use less bandwidth than the sum of their stated bit rates combined.</span></span> <span data-ttu-id="38ca6-112">Ao especificar o compartilhamento de largura de banda no perfil, você esclarece a leitura de aplicativos de que a largura de banda disponível necessária para transmitir o arquivo não é o que ele poderia parecer.</span><span class="sxs-lookup"><span data-stu-id="38ca6-112">By specifying bandwidth sharing in the profile, you clarify to reading applications that the available bandwidth needed to stream the file is not what it might otherwise seem.</span></span>

<span data-ttu-id="38ca6-113">Nenhum dos objetos do Windows Media Format SDK alteram seu comportamento em resposta a informações de compartilhamento de largura de banda, que é fornecida exclusivamente para que a leitura de aplicativos possa levá-lo ao determinar se um arquivo pode ser reproduzido com entrega de largura de banda restrita.</span><span class="sxs-lookup"><span data-stu-id="38ca6-113">None of the objects of the Windows Media Format SDK change their behavior in response to bandwidth sharing information, which is provided solely so that reading applications can take it into account when determining whether a file can be played with restricted bandwidth delivery.</span></span>

<span data-ttu-id="38ca6-114">O compartilhamento de largura de banda é configurado com um objeto de compartilhamento de largura de banda e é adicionado a um perfil antes de começar a gravar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="38ca6-114">Bandwidth sharing is configured with a bandwidth sharing object and is added to a profile before beginning to write a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38ca6-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="38ca6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38ca6-116">**Recursos de arquivo ASF**</span><span class="sxs-lookup"><span data-stu-id="38ca6-116">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="38ca6-117">**Objeto de compartilhamento de largura de banda**</span><span class="sxs-lookup"><span data-stu-id="38ca6-117">**Bandwidth Sharing Object**</span></span>](bandwidth-sharing-object.md)
</dt> <dt>

[<span data-ttu-id="38ca6-118">**Interface IWMBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="38ca6-118">**IWMBandwidthSharing Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="38ca6-119">**Interface IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="38ca6-119">**IWMProfile3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)
</dt> <dt>

[<span data-ttu-id="38ca6-120">**Usando o compartilhamento de largura de banda**</span><span class="sxs-lookup"><span data-stu-id="38ca6-120">**Using Bandwidth Sharing**</span></span>](using-bandwidth-sharing.md)
</dt> </dl>

 

 




