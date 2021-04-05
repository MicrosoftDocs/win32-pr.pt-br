---
title: Exibindo caixas de diálogo
description: Exibindo caixas de diálogo
ms.assetid: 637555af-0a36-4aee-908f-496b52f7bd78
keywords:
- Lojas online do Windows Media Player, exibindo caixas de diálogo
- lojas online, exibindo caixas de diálogo
- tipo 1 lojas online, exibindo caixas de diálogo
- Lojas online do Windows Media Player, caixas de diálogo
- lojas online, caixas de diálogo
- tipos 1 lojas online, caixas de diálogo
- exibindo caixas de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebe008a6c3eac872edea497dc9d50da408aa7eb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640149"
---
# <a name="displaying-dialog-boxes"></a><span data-ttu-id="08442-110">Exibindo caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="08442-110">Displaying Dialog Boxes</span></span>

<span data-ttu-id="08442-111">A loja online pode invocar caixas de diálogo por meio do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="08442-111">The online store can invoke dialog boxes through Windows Media Player.</span></span> <span data-ttu-id="08442-112">Para fazer isso, chame [external. ShowPopup](external-showpopup.md) do código de script da página de descoberta, fornecendo um valor de índice personalizado que representa a caixa de diálogo a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="08442-112">To do this, call [External.showPopup](external-showpopup.md) from the discovery page script code, providing a custom index value that represents the dialog box to display.</span></span> <span data-ttu-id="08442-113">Esse valor de índice tem significado apenas para o código da loja online; O Windows Media Player não interpreta esse valor.</span><span class="sxs-lookup"><span data-stu-id="08442-113">This index value has meaning only to the online store code; Windows Media Player does not interpret this value.</span></span> <span data-ttu-id="08442-114">Em seguida, o Windows Media Player chama [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passando g \_ szItemInfo \_ PopupURL para o parâmetro *bstrInfoName* e o número de índice para o parâmetro *pContext* .</span><span class="sxs-lookup"><span data-stu-id="08442-114">Windows Media Player then calls [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passing g\_szItemInfo\_PopupURL for the *bstrInfoName* parameter and the index number for the *pContext* parameter.</span></span> <span data-ttu-id="08442-115">Em seguida, o plug-in retorna um **BSTR** contendo a URL da página da Web a ser exibida na caixa de diálogo e o Player mostra a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="08442-115">The plug-in then returns a **BSTR** containing the URL of the webpage to display in the dialog box and the Player shows the dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08442-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08442-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08442-117">**Guia de programação para lojas online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="08442-117">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




