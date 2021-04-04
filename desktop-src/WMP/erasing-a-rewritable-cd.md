---
title: Apagando um CD regravável
description: Apagando um CD regravável
ms.assetid: 272fdd2b-c174-4bde-b05e-839d547532a6
keywords:
- Windows Media Player, gravação de CD
- Modelo de objeto do Windows Media Player, gravação de CD
- modelo de objeto, gravação de CD
- Controle ActiveX do Windows Media Player, gravação de CD
- Controle ActiveX, gravação de CD
- Controle ActiveX móvel do Windows Media Player, gravação de CD
- Windows Media Player Mobile, gravação de CD
- Gravação de CD, apagando CDs regraváveis
- gravando CDs, apagando CDs regraváveis
- apagando CDs regraváveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7025b7cd70c86c0b832aa792e50a8a2c64e7f45
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007112"
---
# <a name="erasing-a-rewritable-cd"></a><span data-ttu-id="3aef0-113">Apagando um CD regravável</span><span class="sxs-lookup"><span data-stu-id="3aef0-113">Erasing a Rewritable CD</span></span>

<span data-ttu-id="3aef0-114">A interface [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) fornece um método para apagar discos CD-RW.</span><span class="sxs-lookup"><span data-stu-id="3aef0-114">The [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface provides a method for erasing CD-RW discs.</span></span> <span data-ttu-id="3aef0-115">Antes de apagar um CD, você deve primeiro verificar se a operação tem suporte.</span><span class="sxs-lookup"><span data-stu-id="3aef0-115">Before erasing a CD, you must first ensure that the operation is supported.</span></span> <span data-ttu-id="3aef0-116">Para obter mais informações, consulte [recuperando a unidade e o status do disco](retrieving-the-drive-and-disc-status.md).</span><span class="sxs-lookup"><span data-stu-id="3aef0-116">For more information, see [Retrieving the Drive and Disc Status](retrieving-the-drive-and-disc-status.md).</span></span>

<span data-ttu-id="3aef0-117">Para começar a apagar o conteúdo de um CD regravável, chame [IWMPCdromBurn:: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span><span class="sxs-lookup"><span data-stu-id="3aef0-117">To begin erasing the contents of a rewritable CD, call [IWMPCdromBurn::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span></span>


```C++

    HRESULT hr = m_spCdromBurn->erase();
    

```



## <a name="related-topics"></a><span data-ttu-id="3aef0-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3aef0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3aef0-119">**Gravando um CD**</span><span class="sxs-lookup"><span data-stu-id="3aef0-119">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="3aef0-120">**Recuperar a interface de gravação de CD**</span><span class="sxs-lookup"><span data-stu-id="3aef0-120">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="3aef0-121">**Iniciando o processo de gravação**</span><span class="sxs-lookup"><span data-stu-id="3aef0-121">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="3aef0-122">**Recuperando a unidade e o status do disco**</span><span class="sxs-lookup"><span data-stu-id="3aef0-122">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="3aef0-123">**Recuperando o status da gravação**</span><span class="sxs-lookup"><span data-stu-id="3aef0-123">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




