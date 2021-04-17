---
description: Salvando e restaurando objetos DvdState
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: Salvando e restaurando objetos DvdState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9640b20bc8d763054c15331017da343ef45f3c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757245"
---
# <a name="saving-and-restoring-dvdstate-objects"></a><span data-ttu-id="6502e-103">Salvando e restaurando objetos DvdState</span><span class="sxs-lookup"><span data-stu-id="6502e-103">Saving and Restoring DvdState Objects</span></span>

<span data-ttu-id="6502e-104">Os objetos [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) permitem que os aplicativos salvem um instantâneo da sessão do usuário, incluindo informações como o local atual no disco, o nível pai da pessoa que está exibindo, os fluxos de áudio e subimagem selecionados e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6502e-104">[**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) objects enable applications to save a snapshot of the user session, including information such as the current location on the disc, the parental level of the person who is viewing, the selected audio and subpicture streams, and so on.</span></span> <span data-ttu-id="6502e-105">Isso significa que os usuários podem salvar seu lugar em um disco DVD-Video e observá-lo em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="6502e-105">This means that users can save their place on a DVD-Video disc and watch it at a later time.</span></span>

<span data-ttu-id="6502e-106">Os aplicativos não podem criar objetos DvdState.</span><span class="sxs-lookup"><span data-stu-id="6502e-106">Applications cannot create DvdState objects.</span></span> <span data-ttu-id="6502e-107">Esses objetos são criados internamente pelo navegador de DVD quando um aplicativo chama [**IDvdInfo2:: GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate).</span><span class="sxs-lookup"><span data-stu-id="6502e-107">These objects are created internally by the DVD Navigator when an application calls [**IDvdInfo2::GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate).</span></span> <span data-ttu-id="6502e-108">Os objetos DvdState expõem a interface [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) para permitir que os aplicativos consultem determinadas informações.</span><span class="sxs-lookup"><span data-stu-id="6502e-108">DvdState objects expose the [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) interface to allow applications to query for certain information.</span></span>

<span data-ttu-id="6502e-109">No aplicativo de exemplo de DVD, as funções **CDvdCore:: RestoreBookmark** e **CDvdCore:: SaveBookmark** mostram como salvar e recuperar objetos DvdState.</span><span class="sxs-lookup"><span data-stu-id="6502e-109">In the DVD sample application, the **CDvdCore::RestoreBookmark** and **CDvdCore::SaveBookmark** functions show how to save and retrieve DvdState objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6502e-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6502e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6502e-111">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="6502e-111">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



