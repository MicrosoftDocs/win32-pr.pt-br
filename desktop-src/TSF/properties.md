---
title: Propriedades (elementos comuns)
description: A TSF (estrutura de serviços de texto) fornece propriedades que associam metadados a um intervalo de texto.
ms.assetid: d1d0dd99-f303-4355-9835-917de9491a0b
keywords:
- TSF (estrutura de serviços de texto), propriedades
- TSF (estrutura de serviços de texto), propriedades
- serviços de texto, propriedades
- Aplicativos habilitados para TSF, propriedades
- properties
- TSF (estrutura de serviços de texto), tipos de propriedade
- TSF (estrutura de serviços de texto), tipos de propriedade
- serviços de texto, tipos de propriedade
- Aplicativos habilitados para TSF, tipos de propriedade
- tipos de propriedade
- TSF (estrutura de serviços de texto), armazenamento persistente de propriedades
- TSF (estrutura de serviços de texto), armazenamento persistente de propriedades
- serviços de texto, armazenamento persistente de propriedades
- Aplicativos habilitados para TSF, armazenamento persistente de propriedades
- armazenamento persistente de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff852bccfb7d9b6c94e57a2fa0cf8eef6fbdf18
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105782921"
---
# <a name="properties-common-elements"></a>Propriedades (elementos comuns)

A TSF (estrutura de serviços de texto) fornece propriedades que associam metadados a um intervalo de texto. Essas propriedades incluem, mas não se limitam a, atributos de exibição, como texto em negrito, identificador de idioma do texto e dados brutos fornecidos por um serviço de texto, como os dados de áudio associados ao texto do serviço de texto de fala.

O exemplo a seguir demonstra como uma propriedade de cor de texto hipotética com os valores possíveis de vermelho (R), verde (G) ou azul (B) pode ser exibida.


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



As propriedades de tipos diferentes podem se sobrepor. Por exemplo, use o exemplo anterior e adicione um atributo de texto que possa ser negrito (B) ou itálico (I).


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



O texto "This" seria negrito, "is" seria negrito e vermelho, "alguns" seria exibido normalmente, "colorida" seria verde e em itálico e "texto" seria em itálico.

As propriedades do mesmo tipo não podem se sobrepor. Por exemplo, a situação a seguir não é permitida porque "is" e "colorida" têm valores sobrepostos dos mesmos tipos.


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a>Tipos de propriedade

O TSF define três tipos diferentes de propriedades.



|                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Estático         | Um objeto de propriedade estática armazena os dados de propriedade com texto. Ele também armazena o intervalo de informações de texto para cada intervalo ao qual a propriedade se aplica. ITfReadOnlyProperty:: GetType retorna a \_ \_ categoria estática TFCAT propstyle do GUID \_ .                                                                                                                                                                                                                      |
| Static-Compact | Um objeto de propriedade estática-Compact é idêntico a um objeto de propriedade estática, exceto que uma propriedade estática-Compact não armazena dados de intervalo. Quando o intervalo coberto por uma propriedade estática-Compact é solicitado, um intervalo é criado para cada grupo de propriedades adjacentes. As propriedades de compactação estática são a maneira mais eficiente de armazenar propriedades por caractere. ITfReadOnlyProperty:: GetType retorna a \_ categoria STATICCOMPACT do GUID TFCAT \_ propstyle \_ . |
| Personalizado         | Um objeto de propriedade personalizada armazena as informações de intervalo para cada intervalo ao qual a propriedade se aplica. No entanto, ele não armazena os dados reais da propriedade. Em vez disso, uma propriedade personalizada armazena um objeto ITfPropertyStore. O Gerenciador de TSF usa esse objeto para acessar e manter os dados de propriedade. ITfReadOnlyProperty:: GetType retorna a \_ \_ categoria personalizada TFCAT propstyle do GUID \_ .                                                                    |



 

## <a name="working-with-properties"></a>Trabalhando com propriedades

O valor e os atributos da propriedade são obtidos usando a interface [ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) e modificados usando a interface [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) .

Se um tipo de propriedade específico for necessário, [ITfContext:: GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) será usado. **ITfContext:: GetProperty** requer um **GUID** que identifique a propriedade a ser obtida. O TSF define um conjunto de [identificadores de propriedade predefinidos](predefined-properties.md) usados ou um serviço de texto pode definir seus próprios identificadores de propriedade. Se uma propriedade personalizada for usada, o provedor de propriedades deverá publicar o **GUID** da propriedade e o formato dos dados obtidos.

Por exemplo, para obter o **CLSID** para o proprietário de um intervalo de texto, chame **ITfContext:: GetProperty** para obter o objeto Property, chame [ITfProperty:: FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) para obter o intervalo que cobre totalmente a propriedade e, em seguida, chame [ITfReadOnlyProperty:: GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) para obter um [TfGuidAtom](/windows/desktop/TSF/tfguidatom) que representa o **CLSID** do serviço de texto que possui o texto. O exemplo a seguir mostra uma função que, dado um contexto, um intervalo e um cookie de edição, obterá o **CLSID** do serviço de texto que possui o texto.


```C++
HRESULT GetTextOwner(   ITfContext *pContext, 
                        ITfRange *pRange, 
                        TfEditCookie ec, 
                        CLSID *pclsidOwner)
{
    HRESULT     hr;
    ITfProperty *pProp;

    *pclsidOwner = GUID_NULL;

    hr = pContext->GetProperty(GUID_PROP_TEXTOWNER, &pProp);
    if(S_OK == hr)
    {
        ITfRange    *pPropRange;

        hr = pProp->FindRange(ec, pRange, &pPropRange, TF_ANCHOR_START);
        if(S_OK == hr)
        {
            VARIANT var;

            VariantInit(&var);
            hr = pProp->GetValue(ec, pPropRange, &var);
            if(S_OK == hr)
            {
                if(VT_I4 == var.vt)
                {
                    /*
                    var.lVal is a TfGuidAtom that represents the CLSID of the 
                    text owner. Use ITfCategoryMgr to obtain the CLSID from 
                    the TfGuidAtom.
                    */
                    ITfCategoryMgr  *pCatMgr;

                    hr = CoCreateInstance(  CLSID_TF_CategoryMgr,
                                            NULL, 
                                            CLSCTX_INPROC_SERVER, 
                                            IID_ITfCategoryMgr, 
                                            (LPVOID*)&pCatMgr);
                    if(SUCCEEDED(hr))
                    {
                        hr = pCatMgr->GetGUID((TfGuidAtom)var.lVal, pclsidOwner);
                        if(SUCCEEDED(hr))
                        {
                            /*
                            *pclsidOwner now contains the CLSID of the text 
                            service that owns the text at the selection.
                            */
                        }

                        pCatMgr->Release();
                    }
                }
                else
                {
                    //Unrecognized VARIANT type 
                    hr = E_FAIL;
                }
                
                VariantClear(&var);
            }
            
            pPropRange->Release();
        }
        
        pProp->Release();
    }

    return hr;
}

```



As propriedades também podem ser enumeradas obtendo uma interface [IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) de [ITfContext:: EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).

## <a name="persistent-storage-of-properties"></a>Armazenamento persistente de propriedades

Geralmente, as propriedades são transparentes para um aplicativo e são usadas por um ou mais serviços de texto. Para preservar os dados de propriedade, como ao salvar em um arquivo, um aplicativo deve serializar os dados de propriedade quando eles são armazenados e desserializar os dados de propriedade quando os dados são restaurados. Nesse caso, o aplicativo não deve estar interessado em propriedades individuais, mas deve enumerar todas as propriedades no contexto e armazená-las.

Ao armazenar dados de propriedade, um aplicativo deve executar as etapas a seguir.

1.  Obtenha um enumerador de propriedade chamando **ITfContext:: EnumProperties**.
2.  Enumere cada propriedade chamando [IEnumTfProperties:: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).
3.  Para cada propriedade, obtenha um enumerador de intervalo chamando [ITfReadOnlyProperty:: EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).
4.  Enumere cada intervalo na propriedade chamando [IEnumTfRanges:: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).
5.  Para cada intervalo na propriedade, chame [ITextStoreACPServices:: Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) com a propriedade, intervalo, uma estrutura [de \_ \_ ACP de \_ cabeçalho \_ de propriedade persistente de TF](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) e um objeto de fluxo implementado pelo aplicativo.
6.  Grave o conteúdo da estrutura **\_ ACP do \_ \_ cabeçalho \_ de propriedade persistente TF** na memória persistente.
7.  Grave o conteúdo do objeto de fluxo em memória persistente.
8.  Continue as etapas anteriores para todos os intervalos em todas as propriedades.
9.  O aplicativo deve gravar algum tipo de terminiator no fluxo para que, quando os dados forem restaurados, um ponto de interrupção possa ser identificado.


```C++
HRESULT SaveProperties( ITfContext *pContext, 
                        ITextStoreACPServices *pServices, 
                        TfEditCookie ec, 
                        IStream *pStream)
{
    HRESULT             hr;
    IEnumTfProperties   *pEnumProps;
    TF_PERSISTENT_PROPERTY_HEADER_ACP PropHeader;
    ULONG uWritten;
    
    //Enumerate the properties in the context. 
    hr = pContext->EnumProperties(&pEnumProps);
    if(SUCCEEDED(hr))
    {
        ITfProperty *pProp;
        ULONG       uFetched;

        while(SUCCEEDED(pEnumProps->Next(1, &pProp, &uFetched)) && uFetched)
        {
            //Enumerate all the ranges that contain the property. 
            IEnumTfRanges   *pEnumRanges;
            hr = pProp->EnumRanges(ec, &pEnumRanges, NULL);
            if(SUCCEEDED(hr))
            {
                IStream *pTempStream;

                //Create a temporary stream to write the property data to. 
                hr = CreateStreamOnHGlobal(NULL, TRUE, &pTempStream);
                if(SUCCEEDED(hr))
                {
                    ITfRange    *pRange;

                    while(SUCCEEDED(pEnumRanges->Next(1, &pRange, &uFetched)) && uFetched)
                    {
                        LARGE_INTEGER li;

                        //Reset the temporary stream pointer. 
                        li.QuadPart = 0;
                        pTempStream->Seek(li, STREAM_SEEK_SET, NULL);
                        
                        //Get the property header and data for the range. 
                        hr = pServices->Serialize(pProp, pRange, &PropHeader, pTempStream);

                        /*
                        Write the property header into the primary stream. 
                        The header also contains the size of the property 
                        data.
                        */
                        hr = pStream->Write(&PropHeader, sizeof(PropHeader), &uWritten);

                        //Reset the temporary stream pointer. 
                        li.QuadPart = 0;
                        pTempStream->Seek(li, STREAM_SEEK_SET, NULL);

                        //Copy the property data from the temporary stream into the primary stream. 
                        ULARGE_INTEGER  uli;
                        uli.QuadPart = PropHeader.cb;

                        hr = pTempStream->CopyTo(pStream, uli, NULL, NULL);

                        pRange->Release();
                    }
                    
                    pTempStream->Release();
                }
                
                pEnumRanges->Release();
            }
            
            pProp->Release();
        }
        
        pEnumProps->Release();
    }

    //Write a property header with zero size and guid into the stream as a terminator 
    ZeroMemory(&PropHeader, sizeof(PropHeader));
    hr = pStream->Write(&PropHeader, sizeof(PropHeader), &uWritten);

    return hr;
}

```



**ITextStoreACPServices:: serializar**[ITfPropertyStore:: Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)

Ao restaurar dados de propriedade, um aplicativo deve executar as etapas a seguir.

1.  Defina o ponteiro de fluxo para o início da primeira estrutura de **\_ ACP de \_ \_ cabeçalho \_ de propriedade persistente de TF** .
2.  Leia a estrutura de **\_ ACP do \_ \_ cabeçalho \_ de propriedade persistente TF** .
3.  Chame **ITfContext:: GetProperty** com o membro **guidtype** da estrutura **de \_ \_ ACP de \_ cabeçalho \_ de propriedade persistente TF** .
4.  O aplicativo pode fazer uma das duas coisas neste ponto.
    1.  Crie uma instância de um objeto [ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) que o aplicativo deve implementar. Em seguida, chame [ITextStoreACPServices:: unserializate](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) com **NULL** para *pStream* e o ponteiro **ITfPersistentPropertyLoaderACP** .
    2.  Passe o fluxo de entrada para **ITextStoreACPServices:: unserializeize** e **NULL** para *pLoader*.

    O primeiro método é preferencial, pois é o mais eficiente. A implementação do segundo método faz com que todos os dados de propriedade sejam lidos do fluxo durante a chamada **ITextStoreACPServices:: unserializate** . O primeiro método faz com que os dados de propriedade sejam lidos sob demanda em um momento posterior.
5.  Repita as etapas anteriores até que todos os blocos de propriedade sejam desserializados.


```C++
HRESULT LoadProperties( ITfContext *pContext, 
                        ITextStoreACPServices *pServices, 
                        IStream *pStream)
{
    HRESULT hr;
    ULONG   uRead;
    TF_PERSISTENT_PROPERTY_HEADER_ACP PropHeader;

    /*
    Read each property header and property data from the stream. The 
    list of properties is terminated by a TF_PERSISTENT_PROPERTY_HEADER_ACP 
    structure with a cb member of zero.
    */
    hr = pStream->Read(&PropHeader, sizeof(PropHeader), &uRead);
    while(  SUCCEEDED(hr) && 
            (sizeof(PropHeader) == uRead) && 
            (0 != PropHeader.cb))
    {
        ITfProperty *pProp;

        hr = pContext->GetProperty(PropHeader.guidType, &pProp);
        if(SUCCEEDED(hr))
        {
            /*
            Have TSF read the property data from the stream. This call 
            requests a read-only lock, so be sure it can be granted 
            or else this method will fail.
            */
            CTSFPersistentPropertyLoader *pLoader = new CTSFPersistentPropertyLoader(&PropHeader, pStream);
            hr = pServices->Unserialize(pProp, &PropHeader, NULL, pLoader);

            pProp->Release();
        }

        //Read the next header. 
        hr = pStream->Read(&PropHeader, sizeof(PropHeader), &uRead);
    }

    return hr;
}

```



 

 
