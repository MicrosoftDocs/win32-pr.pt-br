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
# <a name="providing-display-attributes"></a>Fornecendo atributos de exibição

Estrutura de Serviços de Texto (TSF) permite que um serviço de texto forneça atributos de exibição para texto. Isso permite que comentários visuais adicionais sejam fornecidos ao usuário. Por exemplo, um serviço de texto do verificador de ortografia pode realçar uma palavra com um sublinhado vermelho. Os atributos de exibição fornecidos são definidos pela estrutura [TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) e incluem cor do texto, cor da tela de fundo do texto, estilo sublinhado, cor sublinhada e peso sublinhado.

Os clientes que usam essas informações de atributo de exibição geralmente serão aplicativos, mas também podem incluir serviços de texto. O gerenciador TSF media entre o provedor de atributo de exibição e o cliente e rastreia o provedor de atributo de exibição dos atributos de exibição específicos.

Para fornecer atributos de exibição, um serviço de texto deve fazer o seguinte.

1.  Registre o serviço de texto como um provedor de atributo de exibição chamando [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) com o identificador de classe do serviço de texto para o primeiro parâmetro, GUID \_ TFCAT DISPLAYATTRIBUTEPROVIDER para o segundo parâmetro e o identificador de classe do serviço de texto novamente para o \_ terceiro parâmetro.
2.  Implemente [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) e disponibiliza-o na fábrica de classes.
3.  Implemente [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) e disponibiliza-o em [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).
4.  Implemente [um objeto ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) para cada tipo de atributo de exibição que o serviço de texto fornece.

## <a name="applying-the-display-attributes"></a>Aplicando os atributos de exibição

O serviço de texto deve aplicar o atributo de exibição a um intervalo de texto. Um serviço de texto só pode modificar o valor da propriedade durante uma sessão de edição de leitura/gravação.

Supondo que isso está dentro de uma sessão de edição de leitura/gravação, um atributo de exibição é aplicado da seguinte maneira.

1.  Obtenha um [objeto ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) que abrange o texto ao que o atributo de exibição será aplicado.
2.  Obtenha um [objeto ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) para os atributos de texto chamando [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) com GUID \_ PROP \_ ATTRIBUTE.
3.  Crie um [TfGuidAtom](tfguidatom.md) do **GUID** do identificador de atributo de exibição definido pelo serviço de texto chamando [ITfCategoryMgr::RegisterGUID.](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
4.  Inicializar uma variável VARIANT como VT I4 e definir o membro \_ **lVal** como **o TfGuidAtom** criado na etapa anterior.
5.  Aplique o atributo de exibição ao intervalo chamando [ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) com o cookie de edição de leitura/gravação, o intervalo e a VARIANT inicializados na etapa anterior.


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



## <a name="supplying-the-display-attribute-information-object"></a>Fornecendo o objeto de informações de atributo de exibição

Um cliente obtém um **objeto ITfDisplayAttributeInfo** de duas maneiras.

1.  O cliente chama [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) com o **identificador GUID** do atributo de exibição. Na primeira vez que o cliente chamar **ITfDisplayAttributeMgr::GetDisplayAttributeInfo**, o gerente do TSF criará uma instância do provedor de atributo de exibição chamando CoCreateInstance com o identificador de classe passado como o primeiro parâmetro para **ITfCategoryMgr::RegisterCategory**. Chamadas subsequentes **para ITfDisplayAttributeMgr::GetDisplayAttributeInfo** reutilizarão o objeto de provedor de atributo de exibição.

    Em seguida, o gerente do TSF chama [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) com o **GUID** do atributo de exibição para obter o objeto **ITfDisplayAttributeInfo.**

    Em seguida, o gerenciador do TSF passa o objeto **ITfDisplayAttributeInfo** de volta para o cliente.

2.  O cliente chama [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) para obter um objeto **IEnumTfDisplayAttributeInfo** que contém todos os atributos de exibição fornecidos por todos os provedores de atributo de exibição. O gerenciador TSF enumera cada provedor de atributo de exibição e cria uma instância de cada provedor chamando CoCreateInstance com o identificador de classe passado como o terceiro parâmetro para **ITfCategoryMgr::RegisterCategory**.

    Em seguida, o gerente do TSF chama o **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** de cada provedor para obter um **objeto IEnumTfDisplayAttributeInfo** que contém todos os atributos de exibição fornecidos pelo provedor.

    Em seguida, o gerente do TSF chama o método [IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) do provedor, adicionando cada objeto **ITfDisplayAttributeInfo** obtido ao enumerador do próprio gerenciador, até que o final da enumeração do provedor seja atingido.

    Quando todos os objetos **ITfDisplayAttributeInfo** de todos os provedores de atributo de exibição são adicionados ao enumerador do gerenciador TSF, o gerenciador retorna seu enumerador ao cliente. Em seguida, o cliente chama **IEnumTfDisplayAttributeInfo::Next** uma ou mais vezes para obter os **objetos ITfDisplayAttributeInfo.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 IEnumTfDisplayAttributeInfo 
</dt> <dt>

 ITfDisplayAttributeProvider::EnumDisplayAttributeInfo 
</dt> <dt>

[IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




