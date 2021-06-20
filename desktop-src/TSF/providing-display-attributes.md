---
title: Fornecendo atributos de exibição
description: Saiba como fornecer atributos de exibição. Estrutura de Serviços de Texto (TSF) permite que um serviço de texto forneça atributos de exibição para texto.
ms.assetid: 5809f5b8-0396-4abd-b5fe-61ecc8cd0914
keywords:
- Estrutura de Serviços de Texto (TSF), atributos de exibição
- TSF (Estrutura de Serviços de Texto), atributos de exibição
- serviços de texto, atributos de exibição
- atributos de exibição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780cc191e39d5b1d0c3329bab87af5267e4a6c73
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406109"
---
# <a name="providing-display-attributes"></a><span data-ttu-id="53187-108">Fornecendo atributos de exibição</span><span class="sxs-lookup"><span data-stu-id="53187-108">Providing Display Attributes</span></span>

<span data-ttu-id="53187-109">Estrutura de Serviços de Texto (TSF) permite que um serviço de texto forneça atributos de exibição para texto.</span><span class="sxs-lookup"><span data-stu-id="53187-109">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="53187-110">Isso permite que comentários visuais adicionais sejam fornecidos ao usuário.</span><span class="sxs-lookup"><span data-stu-id="53187-110">This enables additional visual feedback to be supplied to the user.</span></span> <span data-ttu-id="53187-111">Por exemplo, um serviço de texto do verificador de ortografia pode realçar uma palavra com um sublinhado vermelho.</span><span class="sxs-lookup"><span data-stu-id="53187-111">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="53187-112">Os atributos de exibição fornecidos são definidos pela estrutura [TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) e incluem cor do texto, cor da tela de fundo do texto, estilo sublinhado, cor sublinhada e peso sublinhado.</span><span class="sxs-lookup"><span data-stu-id="53187-112">The display attributes provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="53187-113">Os clientes que usam essas informações de atributo de exibição geralmente serão aplicativos, mas também podem incluir serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="53187-113">Clients that use this display attribute information will most often be applications, but can also include text services.</span></span> <span data-ttu-id="53187-114">O gerenciador TSF media entre o provedor de atributo de exibição e o cliente e rastreia o provedor de atributo de exibição dos atributos de exibição específicos.</span><span class="sxs-lookup"><span data-stu-id="53187-114">The TSF manager mediates between the display attribute provider and the client and tracks the display attribute provider of the specific display attributes.</span></span>

<span data-ttu-id="53187-115">Para fornecer atributos de exibição, um serviço de texto deve fazer o seguinte.</span><span class="sxs-lookup"><span data-stu-id="53187-115">To provide display attributes, a text service must do the following.</span></span>

1.  <span data-ttu-id="53187-116">Registre o serviço de texto como um provedor de atributo de exibição chamando [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) com o identificador de classe do serviço de texto para o primeiro parâmetro, GUID \_ TFCAT DISPLAYATTRIBUTEPROVIDER para o segundo parâmetro e o identificador de classe do serviço de texto novamente para o \_ terceiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="53187-116">Register the text service as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span>
2.  <span data-ttu-id="53187-117">Implemente [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) e disponibiliza-o na fábrica de classes.</span><span class="sxs-lookup"><span data-stu-id="53187-117">Implement [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) and make it available from the class factory.</span></span>
3.  <span data-ttu-id="53187-118">Implemente [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) e disponibiliza-o em [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="53187-118">Implement [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) and make it available from [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span></span>
4.  <span data-ttu-id="53187-119">Implemente [um objeto ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) para cada tipo de atributo de exibição que o serviço de texto fornece.</span><span class="sxs-lookup"><span data-stu-id="53187-119">Implement an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for each type of display attribute that the text service provides.</span></span>

## <a name="applying-the-display-attributes"></a><span data-ttu-id="53187-120">Aplicando os atributos de exibição</span><span class="sxs-lookup"><span data-stu-id="53187-120">Applying the Display Attributes</span></span>

<span data-ttu-id="53187-121">O serviço de texto deve aplicar o atributo de exibição a um intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="53187-121">The text service must apply the display attribute to a range of text.</span></span> <span data-ttu-id="53187-122">Um serviço de texto só pode modificar o valor da propriedade durante uma sessão de edição de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="53187-122">A text service can only modify the property value during a read/write edit session.</span></span>

<span data-ttu-id="53187-123">Supondo que isso está dentro de uma sessão de edição de leitura/gravação, um atributo de exibição é aplicado da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="53187-123">Assuming this is within a read/write edit session, a display attribute is applied in the following manner.</span></span>

1.  <span data-ttu-id="53187-124">Obtenha um [objeto ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) que abrange o texto ao que o atributo de exibição será aplicado.</span><span class="sxs-lookup"><span data-stu-id="53187-124">Obtain an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) object that covers the text that the display attribute will be applied to.</span></span>
2.  <span data-ttu-id="53187-125">Obtenha um [objeto ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) para os atributos de texto chamando [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) com GUID \_ PROP \_ ATTRIBUTE.</span><span class="sxs-lookup"><span data-stu-id="53187-125">Obtain an [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) object for the text attributes by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) with GUID\_PROP\_ATTRIBUTE.</span></span>
3.  <span data-ttu-id="53187-126">Crie um [TfGuidAtom](tfguidatom.md) do **GUID** do identificador de atributo de exibição definido pelo serviço de texto chamando [ITfCategoryMgr::RegisterGUID.](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)</span><span class="sxs-lookup"><span data-stu-id="53187-126">Create a [TfGuidAtom](tfguidatom.md) from the text service-defined display attribute identifier **GUID** by calling [ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>
4.  <span data-ttu-id="53187-127">Inicializar uma variável VARIANT como VT I4 e definir o membro \_ **lVal** como **o TfGuidAtom** criado na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="53187-127">Initialize a VARIANT variable to VT\_I4 and set the **lVal** member to the **TfGuidAtom** created in the previous step.</span></span>
5.  <span data-ttu-id="53187-128">Aplique o atributo de exibição ao intervalo chamando [ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) com o cookie de edição de leitura/gravação, o intervalo e a VARIANT inicializados na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="53187-128">Apply the display attribute to the range by calling [ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) with the read/write edit cookie, the range and the VARIANT initialized in the previous step.</span></span>


```C++
STDAPI CEditSession::DoEditSession(TfEditCookie ec)
{
    HRESULT hr;
    ITfCategoryMgr *pCategoryMgr;
    TfGuidAtom  gaDisplayAttribute = TF_INVALID_GUIDATOM;

    //Create a TfGuidAtom for the display attribute identifier. 
    hr = CoCreateInstance(CLSID_TF_CategoryMgr,
                         NULL, 
                         CLSCTX_INPROC_SERVER, 
                         IID_ITfCategoryMgr, 
                         (void**)&pCategoryMgr);
    
    if(SUCCEEDED(hr))
    {
        hr = pCategoryMgr->RegisterGUID(guidDisplayAttribute, &gaDisplayAttribute);

        pCategoryMgr->Release();
    }
    
    //Apply the display attribute to the selected text. 
    if(TF_INVALID_GUIDATOM != gaDisplayAttribute)
    {
        TF_SELECTION tfSel;
        ULONG cFetched;

        //Get the selection. 
        hr = m_pContext->GetSelection(ec, TF_DEFAULT_SELECTION, 1, &tfSel, &cFetched);
        if(SUCCEEDED(hr) && cFetched)
        {
            ITfProperty *pDisplayAttributeProperty;

            //Get the display attribute property. 
            hr = m_pContext->GetProperty(GUID_PROP_ATTRIBUTE, &pDisplayAttributeProperty);
            if(SUCCEEDED(hr))
            {
                VARIANT var;

                VariantInit(&var);

                //All display attributes are TfGuidAtoms and TfGuidAtoms are VT_I4. 
                var.vt = VT_I4; 
                var.lVal = gaDisplayAttribute;

                //Set the display attribute value over the range. 
                hr = pDisplayAttributeProperty->SetValue(ec, tfSel.range, &var);

                pDisplayAttributeProperty->Release();
            }

            tfSel.range->Release();
        }
    }

    return S_OK;
}
```



## <a name="supplying-the-display-attribute-information-object"></a><span data-ttu-id="53187-129">Fornecendo o objeto de informações de atributo de exibição</span><span class="sxs-lookup"><span data-stu-id="53187-129">Supplying the Display Attribute Information Object</span></span>

<span data-ttu-id="53187-130">Um cliente obtém um **objeto ITfDisplayAttributeInfo** de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="53187-130">A client obtains an **ITfDisplayAttributeInfo** object in one of two ways.</span></span>

1.  <span data-ttu-id="53187-131">O cliente chama [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) com o **identificador GUID** do atributo de exibição.</span><span class="sxs-lookup"><span data-stu-id="53187-131">The client calls [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) with the **GUID** identifier of the display attribute.</span></span> <span data-ttu-id="53187-132">Na primeira vez que o cliente chamar **ITfDisplayAttributeMgr::GetDisplayAttributeInfo**, o gerente do TSF criará uma instância do provedor de atributo de exibição chamando CoCreateInstance com o identificador de classe passado como o primeiro parâmetro para **ITfCategoryMgr::RegisterCategory**.</span><span class="sxs-lookup"><span data-stu-id="53187-132">The first time the client calls **ITfDisplayAttributeMgr::GetDisplayAttributeInfo**, the TSF manager will create an instance of the display attribute provider by calling CoCreateInstance with the class identifier passed as the first parameter to **ITfCategoryMgr::RegisterCategory**.</span></span> <span data-ttu-id="53187-133">Chamadas subsequentes **para ITfDisplayAttributeMgr::GetDisplayAttributeInfo** reutilizarão o objeto de provedor de atributo de exibição.</span><span class="sxs-lookup"><span data-stu-id="53187-133">Subsequent calls to **ITfDisplayAttributeMgr::GetDisplayAttributeInfo** will reuse the display attribute provider object.</span></span>

    <span data-ttu-id="53187-134">Em seguida, o gerente do TSF chama [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) com o **GUID** do atributo de exibição para obter o objeto **ITfDisplayAttributeInfo.**</span><span class="sxs-lookup"><span data-stu-id="53187-134">The TSF manager then calls [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) with the display attribute **GUID** to obtain the **ITfDisplayAttributeInfo** object.</span></span>

    <span data-ttu-id="53187-135">Em seguida, o gerenciador do TSF passa o objeto **ITfDisplayAttributeInfo** de volta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="53187-135">The TSF manager then passes the **ITfDisplayAttributeInfo** object back to the client.</span></span>

2.  <span data-ttu-id="53187-136">O cliente chama [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) para obter um objeto **IEnumTfDisplayAttributeInfo** que contém todos os atributos de exibição fornecidos por todos os provedores de atributo de exibição.</span><span class="sxs-lookup"><span data-stu-id="53187-136">The client calls [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by all of the display attribute providers.</span></span> <span data-ttu-id="53187-137">O gerenciador TSF enumera cada provedor de atributo de exibição e cria uma instância de cada provedor chamando CoCreateInstance com o identificador de classe passado como o terceiro parâmetro para **ITfCategoryMgr::RegisterCategory**.</span><span class="sxs-lookup"><span data-stu-id="53187-137">The TSF manager enumerates each display attribute provider and creates an instance of each provider by calling CoCreateInstance with the class identifier passed as the third parameter to **ITfCategoryMgr::RegisterCategory**.</span></span>

    <span data-ttu-id="53187-138">Em seguida, o gerente do TSF chama o **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** de cada provedor para obter um **objeto IEnumTfDisplayAttributeInfo** que contém todos os atributos de exibição fornecidos pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="53187-138">The TSF manager then calls each provider's **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by the provider.</span></span>

    <span data-ttu-id="53187-139">Em seguida, o gerente do TSF chama o método [IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) do provedor, adicionando cada objeto **ITfDisplayAttributeInfo** obtido ao enumerador do próprio gerenciador, até que o final da enumeração do provedor seja atingido.</span><span class="sxs-lookup"><span data-stu-id="53187-139">The TSF manager then calls the provider's [IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) method, adding each **ITfDisplayAttributeInfo** object obtained to the manager's own enumerator, until the end of the provider's enumeration is reached.</span></span>

    <span data-ttu-id="53187-140">Quando todos os objetos **ITfDisplayAttributeInfo** de todos os provedores de atributo de exibição são adicionados ao enumerador do gerenciador TSF, o gerenciador retorna seu enumerador ao cliente.</span><span class="sxs-lookup"><span data-stu-id="53187-140">When all of the **ITfDisplayAttributeInfo** objects for all of the display attribute providers are added to the TSF manager's enumerator, the manager returns its enumerator to the client.</span></span> <span data-ttu-id="53187-141">Em seguida, o cliente chama **IEnumTfDisplayAttributeInfo::Next** uma ou mais vezes para obter os **objetos ITfDisplayAttributeInfo.**</span><span class="sxs-lookup"><span data-stu-id="53187-141">The client then calls **IEnumTfDisplayAttributeInfo::Next** one or more times to obtain the **ITfDisplayAttributeInfo** objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53187-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53187-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53187-143">TF \_ DISPLAYATTRIBUTE</span><span class="sxs-lookup"><span data-stu-id="53187-143">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="53187-144">ITfCategoryMgr::RegisterCategory</span><span class="sxs-lookup"><span data-stu-id="53187-144">ITfCategoryMgr::RegisterCategory</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[<span data-ttu-id="53187-145">ITfDisplayAttributeProvider</span><span class="sxs-lookup"><span data-stu-id="53187-145">ITfDisplayAttributeProvider</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[<span data-ttu-id="53187-146">IEnumTfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="53187-146">IEnumTfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="53187-147">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="53187-147">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="53187-148">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="53187-148">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="53187-149">ITfRange</span><span class="sxs-lookup"><span data-stu-id="53187-149">ITfRange</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[<span data-ttu-id="53187-150">ITfProperty</span><span class="sxs-lookup"><span data-stu-id="53187-150">ITfProperty</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[<span data-ttu-id="53187-151">ITfContext::GetProperty</span><span class="sxs-lookup"><span data-stu-id="53187-151">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="53187-152">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="53187-152">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="53187-153">ITfCategoryMgr::RegisterGUID</span><span class="sxs-lookup"><span data-stu-id="53187-153">ITfCategoryMgr::RegisterGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[<span data-ttu-id="53187-154">ITfProperty::SetValue</span><span class="sxs-lookup"><span data-stu-id="53187-154">ITfProperty::SetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[<span data-ttu-id="53187-155">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="53187-155">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="53187-156">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="53187-156">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="53187-157">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="53187-157">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="53187-158">IEnumTfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="53187-158">IEnumTfDisplayAttributeInfo</span></span> 
</dt> <dt>

 <span data-ttu-id="53187-159">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="53187-159">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span> 
</dt> <dt>

[<span data-ttu-id="53187-160">IEnumTfDisplayAttributeInfo::Next</span><span class="sxs-lookup"><span data-stu-id="53187-160">IEnumTfDisplayAttributeInfo::Next</span></span>](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




