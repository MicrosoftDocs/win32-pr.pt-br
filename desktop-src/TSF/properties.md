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
# <a name="properties-common-elements"></a><span data-ttu-id="fc762-118">Propriedades (elementos comuns)</span><span class="sxs-lookup"><span data-stu-id="fc762-118">Properties (Common Elements)</span></span>

<span data-ttu-id="fc762-119">A TSF (estrutura de serviços de texto) fornece propriedades que associam metadados a um intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="fc762-119">Text Services Framework (TSF) provides properties that associate metadata with a range of text.</span></span> <span data-ttu-id="fc762-120">Essas propriedades incluem, mas não se limitam a, atributos de exibição, como texto em negrito, identificador de idioma do texto e dados brutos fornecidos por um serviço de texto, como os dados de áudio associados ao texto do serviço de texto de fala.</span><span class="sxs-lookup"><span data-stu-id="fc762-120">These properties include, but are not limited to, display attributes such as bold text, the language identifier of the text, and raw data provided by a text service such as the audio data associated with text from the speech text service.</span></span>

<span data-ttu-id="fc762-121">O exemplo a seguir demonstra como uma propriedade de cor de texto hipotética com os valores possíveis de vermelho (R), verde (G) ou azul (B) pode ser exibida.</span><span class="sxs-lookup"><span data-stu-id="fc762-121">The following example demonstrates how a hypothetical text color property with possible values of red (R), green (G), or blue (B) can be viewed.</span></span>


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="fc762-122">As propriedades de tipos diferentes podem se sobrepor.</span><span class="sxs-lookup"><span data-stu-id="fc762-122">Properties of different types can overlap.</span></span> <span data-ttu-id="fc762-123">Por exemplo, use o exemplo anterior e adicione um atributo de texto que possa ser negrito (B) ou itálico (I).</span><span class="sxs-lookup"><span data-stu-id="fc762-123">For example, take the previous example and add a text attribute that can be either bold (B) or italic (I).</span></span>


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="fc762-124">O texto "This" seria negrito, "is" seria negrito e vermelho, "alguns" seria exibido normalmente, "colorida" seria verde e em itálico e "texto" seria em itálico.</span><span class="sxs-lookup"><span data-stu-id="fc762-124">The text "this" would be bold, "is" would be both bold and red, "some" would be displayed normally, "colored" would be green and italicized and "text" would be italicized.</span></span>

<span data-ttu-id="fc762-125">As propriedades do mesmo tipo não podem se sobrepor.</span><span class="sxs-lookup"><span data-stu-id="fc762-125">Properties of the same type cannot overlap.</span></span> <span data-ttu-id="fc762-126">Por exemplo, a situação a seguir não é permitida porque "is" e "colorida" têm valores sobrepostos dos mesmos tipos.</span><span class="sxs-lookup"><span data-stu-id="fc762-126">For example, the following situation is not allowed because "is" and "colored" have overlapping values of the same types.</span></span>


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a><span data-ttu-id="fc762-127">Tipos de propriedade</span><span class="sxs-lookup"><span data-stu-id="fc762-127">Property Types</span></span>

<span data-ttu-id="fc762-128">O TSF define três tipos diferentes de propriedades.</span><span class="sxs-lookup"><span data-stu-id="fc762-128">TSF defines three different types of properties.</span></span>



|                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc762-129">Estático</span><span class="sxs-lookup"><span data-stu-id="fc762-129">Static</span></span>         | <span data-ttu-id="fc762-130">Um objeto de propriedade estática armazena os dados de propriedade com texto.</span><span class="sxs-lookup"><span data-stu-id="fc762-130">A static property object stores the property data with text.</span></span> <span data-ttu-id="fc762-131">Ele também armazena o intervalo de informações de texto para cada intervalo ao qual a propriedade se aplica.</span><span class="sxs-lookup"><span data-stu-id="fc762-131">It also stores the range of text information for each range that the property applies to.</span></span> <span data-ttu-id="fc762-132">ITfReadOnlyProperty:: GetType retorna a \_ \_ categoria estática TFCAT propstyle do GUID \_ .</span><span class="sxs-lookup"><span data-stu-id="fc762-132">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATIC category.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="fc762-133">Static-Compact</span><span class="sxs-lookup"><span data-stu-id="fc762-133">Static-Compact</span></span> | <span data-ttu-id="fc762-134">Um objeto de propriedade estática-Compact é idêntico a um objeto de propriedade estática, exceto que uma propriedade estática-Compact não armazena dados de intervalo.</span><span class="sxs-lookup"><span data-stu-id="fc762-134">A static-compact property object is identical to a static property object except a static-compact property does not store range data.</span></span> <span data-ttu-id="fc762-135">Quando o intervalo coberto por uma propriedade estática-Compact é solicitado, um intervalo é criado para cada grupo de propriedades adjacentes.</span><span class="sxs-lookup"><span data-stu-id="fc762-135">When the range covered by a static-compact property is requested, a range is created for each group of adjacent properties.</span></span> <span data-ttu-id="fc762-136">As propriedades de compactação estática são a maneira mais eficiente de armazenar propriedades por caractere.</span><span class="sxs-lookup"><span data-stu-id="fc762-136">Static-compact properties are the most efficient way to store properties on a per-character basis.</span></span> <span data-ttu-id="fc762-137">ITfReadOnlyProperty:: GetType retorna a \_ categoria STATICCOMPACT do GUID TFCAT \_ propstyle \_ .</span><span class="sxs-lookup"><span data-stu-id="fc762-137">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATICCOMPACT category.</span></span> |
| <span data-ttu-id="fc762-138">Personalizado</span><span class="sxs-lookup"><span data-stu-id="fc762-138">Custom</span></span>         | <span data-ttu-id="fc762-139">Um objeto de propriedade personalizada armazena as informações de intervalo para cada intervalo ao qual a propriedade se aplica.</span><span class="sxs-lookup"><span data-stu-id="fc762-139">A custom property object stores the range information for each range that the property applies to.</span></span> <span data-ttu-id="fc762-140">No entanto, ele não armazena os dados reais da propriedade.</span><span class="sxs-lookup"><span data-stu-id="fc762-140">It does not, however, store the actual data for the property.</span></span> <span data-ttu-id="fc762-141">Em vez disso, uma propriedade personalizada armazena um objeto ITfPropertyStore.</span><span class="sxs-lookup"><span data-stu-id="fc762-141">Instead, a custom property stores an ITfPropertyStore object.</span></span> <span data-ttu-id="fc762-142">O Gerenciador de TSF usa esse objeto para acessar e manter os dados de propriedade. ITfReadOnlyProperty:: GetType retorna a \_ \_ categoria personalizada TFCAT propstyle do GUID \_ .</span><span class="sxs-lookup"><span data-stu-id="fc762-142">The TSF manager uses this object to access and maintain the property data.ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_CUSTOM category.</span></span>                                                                    |



 

## <a name="working-with-properties"></a><span data-ttu-id="fc762-143">Trabalhando com propriedades</span><span class="sxs-lookup"><span data-stu-id="fc762-143">Working with Properties</span></span>

<span data-ttu-id="fc762-144">O valor e os atributos da propriedade são obtidos usando a interface [ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) e modificados usando a interface [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) .</span><span class="sxs-lookup"><span data-stu-id="fc762-144">The property value and attributes are obtained using the [ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) interface and modified using the [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) interface.</span></span>

<span data-ttu-id="fc762-145">Se um tipo de propriedade específico for necessário, [ITfContext:: GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) será usado.</span><span class="sxs-lookup"><span data-stu-id="fc762-145">If a specific property type is required, then [ITfContext::GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) is used.</span></span> <span data-ttu-id="fc762-146">**ITfContext:: GetProperty** requer um **GUID** que identifique a propriedade a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="fc762-146">**ITfContext::GetProperty** requires a **GUID** that identifies the property to obtain.</span></span> <span data-ttu-id="fc762-147">O TSF define um conjunto de [identificadores de propriedade predefinidos](predefined-properties.md) usados ou um serviço de texto pode definir seus próprios identificadores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="fc762-147">TSF defines a set of [predefined property identifiers](predefined-properties.md) used or a text service can define its own property identifiers.</span></span> <span data-ttu-id="fc762-148">Se uma propriedade personalizada for usada, o provedor de propriedades deverá publicar o **GUID** da propriedade e o formato dos dados obtidos.</span><span class="sxs-lookup"><span data-stu-id="fc762-148">If a custom property is used, the property provider must publish the property **GUID** and the format of the data obtained.</span></span>

<span data-ttu-id="fc762-149">Por exemplo, para obter o **CLSID** para o proprietário de um intervalo de texto, chame **ITfContext:: GetProperty** para obter o objeto Property, chame [ITfProperty:: FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) para obter o intervalo que cobre totalmente a propriedade e, em seguida, chame [ITfReadOnlyProperty:: GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) para obter um [TfGuidAtom](/windows/desktop/TSF/tfguidatom) que representa o **CLSID** do serviço de texto que possui o texto.</span><span class="sxs-lookup"><span data-stu-id="fc762-149">For example, to obtain the **CLSID** for the owner of a range of text, call **ITfContext::GetProperty** to obtain the property object, call [ITfProperty::FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) to obtain the range that entirely covers the property, then call [ITfReadOnlyProperty::GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) to get a [TfGuidAtom](/windows/desktop/TSF/tfguidatom) that represents the **CLSID** of the text service that owns the text.</span></span> <span data-ttu-id="fc762-150">O exemplo a seguir mostra uma função que, dado um contexto, um intervalo e um cookie de edição, obterá o **CLSID** do serviço de texto que possui o texto.</span><span class="sxs-lookup"><span data-stu-id="fc762-150">The following example shows a function that, given a context, range and an edit cookie, will obtain the **CLSID** of the text service that owns the text.</span></span>


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



<span data-ttu-id="fc762-151">As propriedades também podem ser enumeradas obtendo uma interface [IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) de [ITfContext:: EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).</span><span class="sxs-lookup"><span data-stu-id="fc762-151">Properties can also be enumerated by obtaining an [IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) interface from [ITfContext::EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).</span></span>

## <a name="persistent-storage-of-properties"></a><span data-ttu-id="fc762-152">Armazenamento persistente de propriedades</span><span class="sxs-lookup"><span data-stu-id="fc762-152">Persistent Storage of Properties</span></span>

<span data-ttu-id="fc762-153">Geralmente, as propriedades são transparentes para um aplicativo e são usadas por um ou mais serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="fc762-153">Often, properties are transparent to an application and are used by one or more text services.</span></span> <span data-ttu-id="fc762-154">Para preservar os dados de propriedade, como ao salvar em um arquivo, um aplicativo deve serializar os dados de propriedade quando eles são armazenados e desserializar os dados de propriedade quando os dados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="fc762-154">In order to preserve the property data, such as when saving to a file, an application must serialize the property data when it is stored and unserialize the property data when the data is restored.</span></span> <span data-ttu-id="fc762-155">Nesse caso, o aplicativo não deve estar interessado em propriedades individuais, mas deve enumerar todas as propriedades no contexto e armazená-las.</span><span class="sxs-lookup"><span data-stu-id="fc762-155">In this case, the application should not be interested in individual properties, but should enumerate all properties in the context and store them.</span></span>

<span data-ttu-id="fc762-156">Ao armazenar dados de propriedade, um aplicativo deve executar as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc762-156">When storing property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="fc762-157">Obtenha um enumerador de propriedade chamando **ITfContext:: EnumProperties**.</span><span class="sxs-lookup"><span data-stu-id="fc762-157">Obtain a property enumerator by calling **ITfContext::EnumProperties**.</span></span>
2.  <span data-ttu-id="fc762-158">Enumere cada propriedade chamando [IEnumTfProperties:: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).</span><span class="sxs-lookup"><span data-stu-id="fc762-158">Enumerate each property by calling [IEnumTfProperties::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).</span></span>
3.  <span data-ttu-id="fc762-159">Para cada propriedade, obtenha um enumerador de intervalo chamando [ITfReadOnlyProperty:: EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).</span><span class="sxs-lookup"><span data-stu-id="fc762-159">For each property, obtain a range enumerator by calling [ITfReadOnlyProperty::EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).</span></span>
4.  <span data-ttu-id="fc762-160">Enumere cada intervalo na propriedade chamando [IEnumTfRanges:: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).</span><span class="sxs-lookup"><span data-stu-id="fc762-160">Enumerate each range in the property by calling [IEnumTfRanges::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).</span></span>
5.  <span data-ttu-id="fc762-161">Para cada intervalo na propriedade, chame [ITextStoreACPServices:: Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) com a propriedade, intervalo, uma estrutura [de \_ \_ ACP de \_ cabeçalho \_ de propriedade persistente de TF](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) e um objeto de fluxo implementado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc762-161">For each range in the property, call [ITextStoreACPServices::Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) with the property, range, a [TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) structure, and a stream object implemented by the application.</span></span>
6.  <span data-ttu-id="fc762-162">Grave o conteúdo da estrutura **\_ ACP do \_ \_ cabeçalho \_ de propriedade persistente TF** na memória persistente.</span><span class="sxs-lookup"><span data-stu-id="fc762-162">Write the contents of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure into persistent memory.</span></span>
7.  <span data-ttu-id="fc762-163">Grave o conteúdo do objeto de fluxo em memória persistente.</span><span class="sxs-lookup"><span data-stu-id="fc762-163">Write the contents of the stream object into persistent memory.</span></span>
8.  <span data-ttu-id="fc762-164">Continue as etapas anteriores para todos os intervalos em todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="fc762-164">Continue the previous steps for all of the ranges in all of the properties.</span></span>
9.  <span data-ttu-id="fc762-165">O aplicativo deve gravar algum tipo de terminiator no fluxo para que, quando os dados forem restaurados, um ponto de interrupção possa ser identificado.</span><span class="sxs-lookup"><span data-stu-id="fc762-165">The application should write some type of terminiator into the stream so that, when the data is restored, a stopping point can be identified.</span></span>


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



<span data-ttu-id="fc762-166">**ITextStoreACPServices:: serializar**[ITfPropertyStore:: Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span><span class="sxs-lookup"><span data-stu-id="fc762-166">**ITextStoreACPServices::Serialize**[ITfPropertyStore::Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span></span>

<span data-ttu-id="fc762-167">Ao restaurar dados de propriedade, um aplicativo deve executar as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc762-167">When restoring property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="fc762-168">Defina o ponteiro de fluxo para o início da primeira estrutura de **\_ ACP de \_ \_ cabeçalho \_ de propriedade persistente de TF** .</span><span class="sxs-lookup"><span data-stu-id="fc762-168">Set the stream pointer to the start of the first **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
2.  <span data-ttu-id="fc762-169">Leia a estrutura de **\_ ACP do \_ \_ cabeçalho \_ de propriedade persistente TF** .</span><span class="sxs-lookup"><span data-stu-id="fc762-169">Read the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
3.  <span data-ttu-id="fc762-170">Chame **ITfContext:: GetProperty** com o membro **guidtype** da estrutura **de \_ \_ ACP de \_ cabeçalho \_ de propriedade persistente TF** .</span><span class="sxs-lookup"><span data-stu-id="fc762-170">Call **ITfContext::GetProperty** with the **guidType** member of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
4.  <span data-ttu-id="fc762-171">O aplicativo pode fazer uma das duas coisas neste ponto.</span><span class="sxs-lookup"><span data-stu-id="fc762-171">The application can do one of two things at this point.</span></span>
    1.  <span data-ttu-id="fc762-172">Crie uma instância de um objeto [ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) que o aplicativo deve implementar.</span><span class="sxs-lookup"><span data-stu-id="fc762-172">Create an instance of an [ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) object that the application must implement.</span></span> <span data-ttu-id="fc762-173">Em seguida, chame [ITextStoreACPServices:: unserializate](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) com **NULL** para *pStream* e o ponteiro **ITfPersistentPropertyLoaderACP** .</span><span class="sxs-lookup"><span data-stu-id="fc762-173">Then call [ITextStoreACPServices::Unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) with **NULL** for *pStream* and the **ITfPersistentPropertyLoaderACP** pointer.</span></span>
    2.  <span data-ttu-id="fc762-174">Passe o fluxo de entrada para **ITextStoreACPServices:: unserializeize** e **NULL** para *pLoader*.</span><span class="sxs-lookup"><span data-stu-id="fc762-174">Pass the input stream to **ITextStoreACPServices::Unserialize** and **NULL** for *pLoader*.</span></span>

    <span data-ttu-id="fc762-175">O primeiro método é preferencial, pois é o mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="fc762-175">The first method is preferred as it is the most efficient.</span></span> <span data-ttu-id="fc762-176">A implementação do segundo método faz com que todos os dados de propriedade sejam lidos do fluxo durante a chamada **ITextStoreACPServices:: unserializate** .</span><span class="sxs-lookup"><span data-stu-id="fc762-176">Implementing the second method causes all of the property data to be read from the stream during the **ITextStoreACPServices::Unserialize** call.</span></span> <span data-ttu-id="fc762-177">O primeiro método faz com que os dados de propriedade sejam lidos sob demanda em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="fc762-177">The first method causes the property data to be read on demand at a later time.</span></span>
5.  <span data-ttu-id="fc762-178">Repita as etapas anteriores até que todos os blocos de propriedade sejam desserializados.</span><span class="sxs-lookup"><span data-stu-id="fc762-178">Repeat the previous steps until all property blocks are unserialized.</span></span>


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



 

 
