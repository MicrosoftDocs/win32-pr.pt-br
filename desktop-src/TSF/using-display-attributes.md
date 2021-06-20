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
# <a name="using-display-attributes"></a>Usando atributos de exibição

Estrutura de Serviços de Texto (TSF) permite que um serviço de texto forneça atributos de exibição para texto. Isso permite que um aplicativo exibe comentários visuais adicionais. Por exemplo, um serviço de texto do verificador de ortografia pode realçar uma palavra com um sublinhado vermelho. Os atributos de exibição que podem ser fornecidos são definidos pela estrutura [TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) e incluem cor do texto, cor da tela de fundo do texto, estilo sublinhado, cor sublinhada e peso sublinhado.

Ao renderizar texto, um aplicativo deve obter os atributos de exibição para o texto desenhado e usar os atributos para modificar como o texto é desenhado. Conclua as etapas a seguir para obter atributos de exibição.

1.  Obtenha um objeto de propriedade para GUID \_ PROP \_ ATTRIBUTE chamando [ITfContext::GetProperty.](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
2.  Obtenha o valor de GUID PROP ATTRIBUTE para o intervalo especificado chamando \_ \_ [ITfReadOnlyProperty::GetValue.](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue) Isso fornece um [valor TfGuidAtom.](tfguidatom.md)
3.  Converta [o valor TfGuidAtom](tfguidatom.md) em um GUID chamando [ITfCategoryMgr::GetGUID.](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
4.  Crie um [objeto ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) para o atributo de exibição chamando [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).
5.  Obtenha as informações de atributo de exibição chamando [ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).

O exemplo de código a seguir demonstra uma função que obtém os atributos de exibição de um contexto, intervalo e cookie de edição fornecidos.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 ITfDisplayAttributeInfo::GetAttributeInfo 
</dt> </dl>

 

 




