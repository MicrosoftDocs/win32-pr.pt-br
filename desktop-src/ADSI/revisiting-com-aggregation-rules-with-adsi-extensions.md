---
title: Revisitando regras de agregação com com extensões ADSI
description: Veja a seguir uma breve revisão das regras de agregação COM e de extensão de ADSI.
ms.assetid: 3efcdfcf-4965-4436-90b2-dc0f627c71b4
ms.tgt_platform: multiple
keywords:
- Extensões ADSI, regras de agregação COM
- ADSI de agregação COM
- Revisitando regras de agregação com com extensões ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9b3e3614c4adc225883f120f8fbf362df3e646
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641839"
---
# <a name="revisiting-com-aggregation-rules-with-adsi-extensions"></a><span data-ttu-id="2e4b4-106">Revisitando regras de agregação com com extensões ADSI</span><span class="sxs-lookup"><span data-stu-id="2e4b4-106">Revisiting COM Aggregation Rules with ADSI Extensions</span></span>

<span data-ttu-id="2e4b4-107">Veja a seguir uma breve revisão das regras de agregação COM e de extensão de ADSI.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-107">The following is a brief review of COM aggregation and ADSI extension rules.</span></span>

-   <span data-ttu-id="2e4b4-108">O método **CreateInstance** retorna um ponteiro para uma interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , como a seguir, que não Delega nenhuma chamada de função para o agregador.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-108">The **CreateInstance** method returns a pointer to an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface, as follows, that does not delegate any function calls to the aggregator.</span></span>

    <span data-ttu-id="2e4b4-109">O método [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) retorna ponteiros para as interfaces às quais ele dá suporte e erros de interfaces para as quais não dá suporte.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-109">The [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method returns pointers to the interfaces that it supports, and errors for interfaces it does not support.</span></span>

    <span data-ttu-id="2e4b4-110">O método [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrementa a contagem de referência no próprio objeto de extensão agregado.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-110">The [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method increments the reference count on the aggregated extension object itself.</span></span>

    <span data-ttu-id="2e4b4-111">O método [**IUnkown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) decrementa a contagem de referência no próprio objeto de extensão agregado e se destrói quando a contagem de referência é 0.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-111">The [**IUnkown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method decrements the reference count on the aggregated extension object itself and destroys itself when the reference count is 0.</span></span>

-   <span data-ttu-id="2e4b4-112">O objeto de extensão deve armazenar o ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do agregador, como m \_ pOuterUnknown, durante a implementação do método **CreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="2e4b4-112">The extension object should store the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer of the aggregator, such as m\_pOuterUnknown, during the implementation of the **CreateInstance** method.</span></span>
-   <span data-ttu-id="2e4b4-113">Todas as interfaces às quais o objeto de extensão dá suporte, incluindo [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension), devem herdar de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), o que delega todas as chamadas de função de volta para o agregador.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-113">All interfaces that the extension object supports, including [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension), should inherit from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), which delegates all function calls back to the aggregator.</span></span>
    -   <span data-ttu-id="2e4b4-114">[**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) chama "m \_ POuterUnknown->QueryInterface"</span><span class="sxs-lookup"><span data-stu-id="2e4b4-114">[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) calls "m\_pOuterUnknown->QueryInterface"</span></span>
    -   <span data-ttu-id="2e4b4-115">[**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) chama "m \_ POuterUnknown->AddRef"</span><span class="sxs-lookup"><span data-stu-id="2e4b4-115">[**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) calls "m\_pOuterUnknown->AddRef"</span></span>
    -   <span data-ttu-id="2e4b4-116">[**IUnkown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) chama "m \_ pOuterUnknown-versão de >"</span><span class="sxs-lookup"><span data-stu-id="2e4b4-116">[**IUnkown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) calls "m\_pOuterUnknown->Release"</span></span>

<span data-ttu-id="2e4b4-117">Os gravadores de extensão podem escolher qualquer implementação interna que prefiram, desde que obedeçam às regras padrão de agregação COM.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-117">Extension writers can choose any internal implementation they prefer as long as they obey standard COM aggregation rules.</span></span> <span data-ttu-id="2e4b4-118">Lembre-se de que um objeto de extensão não precisa funcionar como um objeto autônomo.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-118">Be aware that an extension object does not have to work as a standalone object.</span></span> <span data-ttu-id="2e4b4-119">As extensões são projetadas para funcionar como agregações.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-119">Extensions are designed to work as aggregates.</span></span> <span data-ttu-id="2e4b4-120">No entanto, uma extensão pode ser gravada para funcionar como um objeto autônomo e como uma agregação.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-120">However, an extension can be written to work as both a standalone object and as an aggregate.</span></span>

<span data-ttu-id="2e4b4-121">Além do suporte à agregação Standard COM, um objeto de extensão pode dar suporte a [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para recursos mais avançados.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-121">In addition to standard COM aggregation support, an extension object may support [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) for more advanced features.</span></span> <span data-ttu-id="2e4b4-122">Se a associação tardia tiver suporte, a extensão deverá:</span><span class="sxs-lookup"><span data-stu-id="2e4b4-122">If late binding is supported, the extension should:</span></span>

-   <span data-ttu-id="2e4b4-123">Delega funções para [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) de volta para o agregador.</span><span class="sxs-lookup"><span data-stu-id="2e4b4-123">Delegate functions for [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) back to the aggregator.</span></span>
-   <span data-ttu-id="2e4b4-124">Implemente a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) em [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span><span class="sxs-lookup"><span data-stu-id="2e4b4-124">Implement the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface in [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>

 

 