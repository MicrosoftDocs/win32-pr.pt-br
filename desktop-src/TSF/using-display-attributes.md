---
title: Usando atributos de exibição
description: A TSF (estrutura de serviços de texto) permite que um serviço de texto forneça atributos de exibição para texto.
ms.assetid: b0f6e8e8-586a-4b51-a498-fb22bd36161f
keywords:
- TSF (estrutura de serviços de texto), atributos de exibição
- TSF (estrutura de serviços de texto), atributos de exibição
- Aplicativos habilitados para TSF, atributos de exibição
- atributos de exibição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc725f67fab904db23f6232ac5efb5d63c62c26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635183"
---
# <a name="using-display-attributes"></a><span data-ttu-id="3965b-107">Usando atributos de exibição</span><span class="sxs-lookup"><span data-stu-id="3965b-107">Using Display Attributes</span></span>

<span data-ttu-id="3965b-108">A TSF (estrutura de serviços de texto) permite que um serviço de texto forneça atributos de exibição para texto.</span><span class="sxs-lookup"><span data-stu-id="3965b-108">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="3965b-109">Isso permite que um aplicativo exiba comentários visuais adicionais.</span><span class="sxs-lookup"><span data-stu-id="3965b-109">This enables an application to display additional visual feedback.</span></span> <span data-ttu-id="3965b-110">Por exemplo, um serviço de texto de verificador ortográfico pode realçar uma palavra incorreta com um sublinhado vermelho.</span><span class="sxs-lookup"><span data-stu-id="3965b-110">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="3965b-111">Os atributos de exibição que podem ser fornecidos são definidos pela estrutura [TF \_ DisplayAttribute](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) e incluem cor do texto, cor do plano de fundo do texto, estilo de sublinhado, cor de sublinhado e peso de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="3965b-111">The display attributes that can be provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="3965b-112">Ao renderizar o texto, um aplicativo deve obter os atributos de exibição do texto desenhado e usar os atributos para modificar a forma como o texto é desenhado.</span><span class="sxs-lookup"><span data-stu-id="3965b-112">When rendering text, an application should obtain the display attributes for the text drawn and use the attributes to modify how the text is drawn.</span></span> <span data-ttu-id="3965b-113">Conclua as etapas a seguir para obter os atributos de exibição.</span><span class="sxs-lookup"><span data-stu-id="3965b-113">Complete the following steps to obtain display attributes.</span></span>

1.  <span data-ttu-id="3965b-114">Obtenha um objeto de propriedade para o \_ atributo prop do GUID \_ chamando [ITfContext:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).</span><span class="sxs-lookup"><span data-stu-id="3965b-114">Obtain a property object for GUID\_PROP\_ATTRIBUTE by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).</span></span>
2.  <span data-ttu-id="3965b-115">Obtenha o valor do \_ atributo prop do GUID \_ para o intervalo especificado chamando [ITfReadOnlyProperty:: GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span><span class="sxs-lookup"><span data-stu-id="3965b-115">Obtain the value of the GUID\_PROP\_ATTRIBUTE for the specified range by calling [ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span></span> <span data-ttu-id="3965b-116">Isso fornece um valor de [TfGuidAtom](tfguidatom.md) .</span><span class="sxs-lookup"><span data-stu-id="3965b-116">This supplies a [TfGuidAtom](tfguidatom.md) value.</span></span>
3.  <span data-ttu-id="3965b-117">Converta o valor [TfGuidAtom](tfguidatom.md) em um GUID chamando [ITfCategoryMgr:: GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span><span class="sxs-lookup"><span data-stu-id="3965b-117">Convert the [TfGuidAtom](tfguidatom.md) value into a GUID by calling [ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span></span>
4.  <span data-ttu-id="3965b-118">Crie um objeto [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) para o atributo de exibição chamando [ITfDisplayAttributeMgr:: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="3965b-118">Create an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for the display attribute by calling [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>
5.  <span data-ttu-id="3965b-119">Obtenha as informações do atributo de exibição chamando [ITfDisplayAttributeInfo:: GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="3965b-119">Obtain the display attribute information by calling [ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>

<span data-ttu-id="3965b-120">O exemplo de código a seguir demonstra uma função que obtém os atributos de exibição de um contexto fornecido, um intervalo e um cookie de edição.</span><span class="sxs-lookup"><span data-stu-id="3965b-120">The following code example demonstrates a function that obtains the display attributes from a supplied context, range, and edit cookie.</span></span>


```C++
HRESULT GetDispAttrFromRange(   ITfContext *pContext, 
                                ITfRange *pRange, 
                                TfEditCookie ec, 
                                TF_DISPLAYATTRIBUTE *pDispAttr)
{
    HRESULT     hr;
    
    //Create the category manager. 
    ITfCategoryMgr  *pCategoryMgr;
    hr = CoCreateInstance(  CLSID_TF_CategoryMgr,
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_ITfCategoryMgr, 
                            (LPVOID*)&pCategoryMgr);
    if(FAILED(hr))
    {
        return hr;
    }

    //Create the display attribute manager. 
    ITfDisplayAttributeMgr  *pDispMgr;
    hr = CoCreateInstance(  CLSID_TF_DisplayAttributeMgr,
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_ITfDisplayAttributeMgr, 
                            (LPVOID*)&pDispMgr);
    if(FAILED(hr))
    {
        pCategoryMgr->Release();
        return hr;
    }
    
    //Get the display attribute property. 
    ITfProperty *pProp;
    hr = pContext->GetProperty(GUID_PROP_ATTRIBUTE, &pProp);
    if(SUCCEEDED(hr))
    {
        VARIANT var;

        VariantInit(&var);
        hr = pProp->GetValue(ec, pRange, &var);
        if(S_OK == hr)  //Returns S_FALSE if the range is not completely covered by the property.  
        {
            if(VT_I4 == var.vt)
            {
                //The property is a guidatom. 
                GUID    guid;

                //Convert the guidatom into a GUID. 
                hr = pCategoryMgr->GetGUID((TfGuidAtom)var.lVal, &guid);
                if(SUCCEEDED(hr))
                {
                    ITfDisplayAttributeInfo *pDispInfo;

                    //Get the display attribute info object for this attribute. 
                    hr = pDispMgr->GetDisplayAttributeInfo(guid, &pDispInfo, NULL);
                    if(SUCCEEDED(hr))
                    {
                        //Get the display attribute info. 
                        hr = pDispInfo->GetAttributeInfo(pDispAttr);

                        pDispInfo->Release();
                    }
                }
            }
            else
            {
                //An error occurred; GUID_PROP_ATTRIBUTE must always be VT_I4. 
                hr = E_FAIL;
            }
            VariantClear(&var);
        }
    pProp->Release();
    }

    pCategoryMgr->Release();
    pDispMgr->Release();

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="3965b-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3965b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3965b-122">TF \_ TipoDeExibição</span><span class="sxs-lookup"><span data-stu-id="3965b-122">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="3965b-123">ITfContext:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="3965b-123">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="3965b-124">ITfReadOnlyProperty:: GetValue</span><span class="sxs-lookup"><span data-stu-id="3965b-124">ITfReadOnlyProperty::GetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[<span data-ttu-id="3965b-125">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="3965b-125">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="3965b-126">ITfCategoryMgr:: GetGuid</span><span class="sxs-lookup"><span data-stu-id="3965b-126">ITfCategoryMgr::GetGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="3965b-127">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="3965b-127">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="3965b-128">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="3965b-128">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="3965b-129">ITfDisplayAttributeInfo::GetAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="3965b-129">ITfDisplayAttributeInfo::GetAttributeInfo</span></span> 
</dt> </dl>

 

 




