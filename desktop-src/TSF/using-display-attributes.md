---
title: Usando atributos de exibição
description: Veja como usar atributos de exibição. Estrutura de Serviços de Texto (TSF) permite que um serviço de texto forneça atributos de exibição para texto.
ms.assetid: b0f6e8e8-586a-4b51-a498-fb22bd36161f
keywords:
- Estrutura de Serviços de Texto (TSF), atributos de exibição
- TSF (Estrutura de Serviços de Texto), atributos de exibição
- Aplicativos habilitados para TSF, atributos de exibição
- atributos de exibição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3c576064ab22571b5a7822f5e6ff143add55d03
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406129"
---
# <a name="using-display-attributes"></a><span data-ttu-id="aff84-108">Usando atributos de exibição</span><span class="sxs-lookup"><span data-stu-id="aff84-108">Using Display Attributes</span></span>

<span data-ttu-id="aff84-109">Estrutura de Serviços de Texto (TSF) permite que um serviço de texto forneça atributos de exibição para texto.</span><span class="sxs-lookup"><span data-stu-id="aff84-109">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="aff84-110">Isso permite que um aplicativo exibe comentários visuais adicionais.</span><span class="sxs-lookup"><span data-stu-id="aff84-110">This enables an application to display additional visual feedback.</span></span> <span data-ttu-id="aff84-111">Por exemplo, um serviço de texto do verificador de ortografia pode realçar uma palavra com um sublinhado vermelho.</span><span class="sxs-lookup"><span data-stu-id="aff84-111">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="aff84-112">Os atributos de exibição que podem ser fornecidos são definidos pela estrutura [TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) e incluem cor do texto, cor da tela de fundo do texto, estilo sublinhado, cor sublinhada e peso sublinhado.</span><span class="sxs-lookup"><span data-stu-id="aff84-112">The display attributes that can be provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="aff84-113">Ao renderizar texto, um aplicativo deve obter os atributos de exibição para o texto desenhado e usar os atributos para modificar como o texto é desenhado.</span><span class="sxs-lookup"><span data-stu-id="aff84-113">When rendering text, an application should obtain the display attributes for the text drawn and use the attributes to modify how the text is drawn.</span></span> <span data-ttu-id="aff84-114">Conclua as etapas a seguir para obter atributos de exibição.</span><span class="sxs-lookup"><span data-stu-id="aff84-114">Complete the following steps to obtain display attributes.</span></span>

1.  <span data-ttu-id="aff84-115">Obtenha um objeto de propriedade para GUID \_ PROP \_ ATTRIBUTE chamando [ITfContext::GetProperty.](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)</span><span class="sxs-lookup"><span data-stu-id="aff84-115">Obtain a property object for GUID\_PROP\_ATTRIBUTE by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).</span></span>
2.  <span data-ttu-id="aff84-116">Obtenha o valor de GUID PROP ATTRIBUTE para o intervalo especificado chamando \_ \_ [ITfReadOnlyProperty::GetValue.](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)</span><span class="sxs-lookup"><span data-stu-id="aff84-116">Obtain the value of the GUID\_PROP\_ATTRIBUTE for the specified range by calling [ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span></span> <span data-ttu-id="aff84-117">Isso fornece um [valor TfGuidAtom.](tfguidatom.md)</span><span class="sxs-lookup"><span data-stu-id="aff84-117">This supplies a [TfGuidAtom](tfguidatom.md) value.</span></span>
3.  <span data-ttu-id="aff84-118">Converta [o valor TfGuidAtom](tfguidatom.md) em um GUID chamando [ITfCategoryMgr::GetGUID.](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)</span><span class="sxs-lookup"><span data-stu-id="aff84-118">Convert the [TfGuidAtom](tfguidatom.md) value into a GUID by calling [ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span></span>
4.  <span data-ttu-id="aff84-119">Crie um [objeto ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) para o atributo de exibição chamando [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="aff84-119">Create an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for the display attribute by calling [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>
5.  <span data-ttu-id="aff84-120">Obtenha as informações de atributo de exibição chamando [ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="aff84-120">Obtain the display attribute information by calling [ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>

<span data-ttu-id="aff84-121">O exemplo de código a seguir demonstra uma função que obtém os atributos de exibição de um contexto, intervalo e cookie de edição fornecidos.</span><span class="sxs-lookup"><span data-stu-id="aff84-121">The following code example demonstrates a function that obtains the display attributes from a supplied context, range, and edit cookie.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="aff84-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aff84-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aff84-123">TF \_ DISPLAYATTRIBUTE</span><span class="sxs-lookup"><span data-stu-id="aff84-123">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="aff84-124">ITfContext::GetProperty</span><span class="sxs-lookup"><span data-stu-id="aff84-124">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="aff84-125">ITfReadOnlyProperty::GetValue</span><span class="sxs-lookup"><span data-stu-id="aff84-125">ITfReadOnlyProperty::GetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[<span data-ttu-id="aff84-126">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="aff84-126">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="aff84-127">ITfCategoryMgr::GetGUID</span><span class="sxs-lookup"><span data-stu-id="aff84-127">ITfCategoryMgr::GetGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="aff84-128">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="aff84-128">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="aff84-129">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="aff84-129">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="aff84-130">ITfDisplayAttributeInfo::GetAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="aff84-130">ITfDisplayAttributeInfo::GetAttributeInfo</span></span> 
</dt> </dl>

 

 




