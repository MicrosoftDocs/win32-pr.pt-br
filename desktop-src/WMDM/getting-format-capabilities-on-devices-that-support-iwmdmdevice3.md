---
title: Obtendo recursos de formato por meio de IWMDMDevice3
description: Obtendo recursos de formato em dispositivos que dão suporte a IWMDMDevice3
ms.assetid: a431c3cb-e722-4d68-a82d-385fff067ea6
keywords:
- Windows Media Gerenciador de Dispositivos, recursos do dispositivo
- Gerenciador de Dispositivos, recursos do dispositivo
- Guia de programação, recursos do dispositivo
- aplicativos de desktop, recursos de dispositivo
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, recursos do dispositivo
- gravando arquivos em dispositivos, recursos do dispositivo
- Método IWMDMDevice3
- Windows Media Gerenciador de Dispositivos, método IWMDMDevice3
- Gerenciador de Dispositivos, método IWMDMDevice3
- Guia de programação, método IWMDMDevice3
- aplicativos de área de trabalho, método IWMDMDevice3
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, método IWMDMDevice3
- gravando arquivos em dispositivos, método IWMDMDevice3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734f674a5fc54aaec0df10d4db613fa067f9b505
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2019
ms.locfileid: "104006962"
---
# <a name="getting-format-capabilities-through-iwmdmdevice3"></a><span data-ttu-id="5f0e1-116">Obtendo recursos de formato por meio de IWMDMDevice3</span><span class="sxs-lookup"><span data-stu-id="5f0e1-116">Getting format capabilities through IWMDMDevice3</span></span>

<span data-ttu-id="5f0e1-117">[**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) é o método preferencial para solicitar a um dispositivo quais formatos ele dá suporte.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-117">[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) is the preferred method for asking a device what formats it supports.</span></span> <span data-ttu-id="5f0e1-118">As etapas a seguir mostram como usar esse método para consultar um dispositivo em busca de seus recursos de formato:</span><span class="sxs-lookup"><span data-stu-id="5f0e1-118">The following steps show how to use this method to query a device for its format capabilities:</span></span>

1.  <span data-ttu-id="5f0e1-119">O aplicativo deve determinar a quais formatos um dispositivo dá suporte e quais são de interesse.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-119">The application must determine which formats a device supports and which are of interest.</span></span> <span data-ttu-id="5f0e1-120">Para fazer isso, o aplicativo pode solicitar uma lista de formatos com suporte pelo dispositivo chamando [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).</span><span class="sxs-lookup"><span data-stu-id="5f0e1-120">To do this, the application can request a list of formats supported by the device by calling [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).</span></span>
2.  <span data-ttu-id="5f0e1-121">O aplicativo executa um loop em todos os formatos com suporte e solicita os recursos de formato de um dispositivo para um formato específico (como WMA ou WMV) chamando **IWMDMDevice3:: GetFormatCapability** e especificando um formato usando a enumeração [**WMDM \_ FORMATCODE**](wmdm-formatcode.md) .</span><span class="sxs-lookup"><span data-stu-id="5f0e1-121">The application loops through all of the supported formats and requests a device's format capabilities for a specific format (such as WMA or WMV) by calling **IWMDMDevice3::GetFormatCapability** and specifying a format using the [**WMDM\_FORMATCODE**](wmdm-formatcode.md) enumeration.</span></span> <span data-ttu-id="5f0e1-122">Esse método recupera uma estrutura de [**\_ \_ recursos de formato do WMDM**](wmdm-format-capability.md) .</span><span class="sxs-lookup"><span data-stu-id="5f0e1-122">This method retrieves a [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md) structure.</span></span>
3.  <span data-ttu-id="5f0e1-123">Execute o loop através de todas as estruturas de [**\_ \_ configuração do WMDM prop**](wmdm-prop-config.md) na estrutura de **\_ \_ recursos do formato WMDM** recuperada.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-123">Loop through all the [**WMDM\_PROP\_CONFIG**](wmdm-prop-config.md) structures in the retrieved **WMDM\_FORMAT\_CAPABILITY** structure.</span></span> <span data-ttu-id="5f0e1-124">Cada estrutura de **\_ \_ configuração do WMDM prop** contém um grupo de propriedades com valores com suporte, representando uma configuração para esse formato.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-124">Each **WMDM\_PROP\_CONFIG** structure holds a group of properties with supported values, representing one configuration for that format.</span></span> <span data-ttu-id="5f0e1-125">Cada configuração tem um número de preferência, em que um número mais baixo indica uma preferência maior pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-125">Each configuration has a preference number, where a lower number indicates a greater preference by the device.</span></span>
4.  <span data-ttu-id="5f0e1-126">Execute o loop através de todas as estruturas [**\_ \_ desc prop do WMDM**](wmdm-prop-desc.md) na **configuração de \_ prop \_ do WMDM** recuperada.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-126">Loop through all the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures in the retrieved **WMDM\_PROP\_CONFIG**.</span></span> <span data-ttu-id="5f0e1-127">Cada **WMDM \_ prop \_ desc** contém uma lista de pares de propriedade/valor com suporte.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-127">Each **WMDM\_PROP\_DESC** contains a list of supported property/value pairs.</span></span>
5.  <span data-ttu-id="5f0e1-128">Recupere os nomes de propriedade e os valores da estrutura de **\_ \_ desc prop do WMDM** .</span><span class="sxs-lookup"><span data-stu-id="5f0e1-128">Retrieve the property names and values from the **WMDM\_PROP\_DESC** structure.</span></span> <span data-ttu-id="5f0e1-129">As propriedades incluem taxa de bits, codec e tamanho do quadro.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-129">Properties include bit rate, codec, and frame size.</span></span> <span data-ttu-id="5f0e1-130">Os nomes de propriedade são definidos no arquivo de cabeçalho mswmdm. h; uma lista da maioria dessas constantes é fornecida nas [constantes de metadados](metadata-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5f0e1-130">Property names are defined in the mswmdm.h header file; a list of most of these constants is given in [Metadata Constants](metadata-constants.md).</span></span> <span data-ttu-id="5f0e1-131">Três tipos de valores de propriedade são possíveis:</span><span class="sxs-lookup"><span data-stu-id="5f0e1-131">Three types of property values are possible:</span></span>
    -   <span data-ttu-id="5f0e1-132">Um único valor, WMDM \_ enum \_ prop \_ \_ valores válidos \_ , indicando suporte para quaisquer valores dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-132">A single value, WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY, indicating support for any values for this property.</span></span>
    -   <span data-ttu-id="5f0e1-133">Um intervalo de valores, definido por um valor máximo, valor mínimo e intervalo.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-133">A range of values, defined by a maximum value, minimum value, and interval.</span></span>
    -   <span data-ttu-id="5f0e1-134">Uma lista de valores discretos.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-134">A list of discrete values.</span></span>
6.  <span data-ttu-id="5f0e1-135">Limpe os valores armazenados.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-135">Clear the stored values.</span></span> <span data-ttu-id="5f0e1-136">A memória para esses valores é alocada pelo Windows Media Gerenciador de Dispositivos; seu dispositivo é responsável por liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-136">Memory for these values is allocated by Windows Media Device Manager; your device is responsible for freeing the memory.</span></span> <span data-ttu-id="5f0e1-137">Como fazer isso é descrito no final deste tópico.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-137">How to do this is described at the end of this topic.</span></span>

<span data-ttu-id="5f0e1-138">Ao responder a **GetFormatCapability**, um dispositivo pode reportar \_ \_ \_ valores válidos de prop Enumerate para o \_ \_ **recurso de \_ formato WMDM \_ . configuração de prop do WMDM \_ \_ . WMDM \_ prop \_ desc. ValidValuesForm** para solicitar suporte para quaisquer valores de taxa de bits, canais e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-138">When responding to **GetFormatCapability**, a device can report WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY for **WMDM\_FORMAT\_CAPABILITY.WMDM\_PROP\_CONFIG.WMDM\_PROP\_DESC.ValidValuesForm** to claim support for any values for bit rate, channels, and so on.</span></span> <span data-ttu-id="5f0e1-139">No entanto, você deve tratar essa declaração com cautela, pois os dispositivos podem, às vezes, relatar suporte para quaisquer valores quando, na verdade, não dão suporte a todas as taxas de bits ou tamanhos de imagem.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-139">However, you should treat this claim with caution, because devices can sometimes report support for any values when in fact they do not support all bit rates or image sizes.</span></span> <span data-ttu-id="5f0e1-140">Você pode considerar que o aplicativo transcodificará arquivos extremamente grandes ou de alta taxa de bits para versões menores ou para versões com uso intensivo de CPU e uso intensivo de memória ao enviá-los para dispositivos que se destinam a reproduzir esses arquivos.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-140">You might consider having your application transcode extremely large or high-bit-rate files to smaller versions or less memory-intensive and CPU-intensive versions when sending them to devices that are intended to play these files.</span></span>

<span data-ttu-id="5f0e1-141">A função C++ a seguir mostra como solicitar suporte a formato de dispositivo para um formato específico.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-141">The following C++ function shows how to request device format support for a specific format.</span></span>


```C++
HRESULT GetFormatCaps(WMDM_FORMATCODE formatCode, IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Get a list of supported configurations for the format.
    WMDM_FORMAT_CAPABILITY formatCapList;
    hr = pDevice->GetFormatCapability(formatCode, &formatCapList);
    if (FAILED(hr)) return E_FAIL;

    // TODO: Display the format name.
    // Loop through the configurations and examine each one.
    for (UINT iConfig = 0; iConfig < formatCapList.nPropConfig; iConfig++)
    {
        WMDM_PROP_CONFIG formatConfig = formatCapList.pConfigs[iConfig];

        // Preference level for this configuration (lower number means more preferred).
        // TODO: Display the preference level for this format configuration.

        // Loop through all properties for this configuration and get supported
        // values for the property. Values can be a single value, a range, 
        // or a list of enumerated values.
        for (UINT iDesc = 0; iDesc < formatConfig.nPropDesc; iDesc++)
        {
            WMDM_PROP_DESC propDesc = formatConfig.pPropDesc[iDesc];
            // TODO: Display the property name.

            // Three ways a value can be represented: any, a range, or a list.
            switch (propDesc.ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // TODO: Display a message indicating that all values are valid.
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    {
                        // List these in the docs as the propvariants set.
                        WMDM_PROP_VALUES_RANGE rng = 
                            propDesc.ValidValues.ValidValuesRange;
                        // TODO: Display the min, max, and step values.
                    }
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    {
                        // TODO: Display a banner for the list of valid values.
                        WMDM_PROP_VALUES_ENUM list = propDesc.ValidValues.EnumeratedValidValues;
                        PROPVARIANT pVal;
                        for (UINT iValue = 0; iValue < list.cEnumValues; iValue++)
                        {
                            pVal = list.pValues[iValue];
                            // TODO: Display each valid value.
                            PropVariantClear(&pVal);
                            PropVariantInit(&pVal);
                        }
                    }

                    break;
                default:
                    return E_FAIL,
                    break;
            }
        }
    }
    // Now clear the memory used by WMDM_FORMAT_CAPABILITY.
    FreeFormatCapability(formatCapList);
    return hr;
}
```



<span data-ttu-id="5f0e1-142">**Limpando a memória alocada**</span><span class="sxs-lookup"><span data-stu-id="5f0e1-142">**Clearing allocated memory**</span></span>

<span data-ttu-id="5f0e1-143">Depois de recuperar os recursos de formato de um dispositivo, o aplicativo deve liberar a memória alocada para manter a descrição.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-143">After retrieving format capabilities from a device, the application must free the memory allocated to hold the description.</span></span> <span data-ttu-id="5f0e1-144">[**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) e [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) têm matrizes de estruturas simples que podem ser limpas simplesmente chamando **CoTaskMemFree** com a matriz.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-144">[**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) and [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) have arrays of simple structures that can be cleared by simply calling **CoTaskMemFree** with the array.</span></span> <span data-ttu-id="5f0e1-145">No entanto, o **GetFormatCapability** tem uma estrutura de dados mais complexa com memória alocada dinamicamente que deve ser limpa por meio de um loop por todos os elementos e liberando-os individualmente.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-145">However, **GetFormatCapability** has a more complex data structure with dynamically allocated memory that must be cleared by looping through all the elements and freeing them individually.</span></span>

<span data-ttu-id="5f0e1-146">O código C++ a seguir mostra como um aplicativo pode liberar a memória alocada para uma estrutura de **\_ \_ recursos de formato do WMDM** .</span><span class="sxs-lookup"><span data-stu-id="5f0e1-146">The following C++ code shows how an application can free the memory allocated for a **WMDM\_FORMAT\_CAPABILITY** structure.</span></span>


```C++
void CWMDMController::FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i = 0; i < formatCap.nPropConfig; i++) 
    {
        // Loop through all descriptions of a configuration and delete
        // the values particular to that description type.
        for (UINT j=0; j < formatCap.pConfigs[i].nPropDesc; j++) 
        {
            switch (formatCap.pConfigs[i].pPropDesc[j].ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    for (UINT k=0; k < formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.cEnumValues; k++)
                    {
                        PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues[k]));
                    }
                    CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues);
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMin));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMax));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeStep));
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // No dynamically allocated memory for this value.
                default:
                    break;
            }

            // Free the memory for the description name.
            CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].pwszPropName);
        }
        // Free the memory holding the array of description items for this configuration.
        CoTaskMemFree(formatCap.pConfigs[i].pPropDesc);
    }

    // Free the memory pointing to the array of configurations.
    CoTaskMemFree(formatCap.pConfigs);
    formatCap.nPropConfig = 0;
}
```



<span data-ttu-id="5f0e1-147">**Consultando todos os formatos com suporte**</span><span class="sxs-lookup"><span data-stu-id="5f0e1-147">**Querying for all supported formats**</span></span>

<span data-ttu-id="5f0e1-148">Normalmente, um aplicativo consulta um dispositivo em busca de um formato específico, pois ele está interessado em enviar um arquivo específico para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-148">Typically, an application queries a device for a specific format, because it is interested in sending a specific file to the device.</span></span> <span data-ttu-id="5f0e1-149">No entanto, se você quiser consultar um aplicativo para todos os seus formatos com suporte, você pode chamar [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) e passar g \_ wszWMDMFormatsSupported para recuperar uma lista completa.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-149">However, if you want to query an application for all its supported formats, you can call [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) and pass in g\_wszWMDMFormatsSupported to retrieve a full list.</span></span>

<span data-ttu-id="5f0e1-150">Se um dispositivo retornar apenas um elemento, WMDM \_ FORMATCODE \_ indefinido, isso geralmente significa que o dispositivo não oferece suporte a códigos de formato.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-150">If a device only returns one element, WMDM\_FORMATCODE\_UNDEFINED, this usually means that the device does not support format codes.</span></span> <span data-ttu-id="5f0e1-151">Chamar **GetFormatCapability** com WMDM \_ FORMATCODE \_ indefinido pode recuperar recursos, mas essas propriedades podem ser razoavelmente genéricas (como nome, tamanho do arquivo, data da última modificação e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="5f0e1-151">Calling **GetFormatCapability** with WMDM\_FORMATCODE\_UNDEFINED might retrieve capabilities, but these properties might be fairly generic (such as name, file size, last modified date, and so on).</span></span>

<span data-ttu-id="5f0e1-152">As etapas a seguir mostram como consultar uma lista de todos os formatos com suporte:</span><span class="sxs-lookup"><span data-stu-id="5f0e1-152">The following steps show how to query for a list of all supported formats:</span></span>

1.  <span data-ttu-id="5f0e1-153">Solicite uma lista de todos os códigos de formatação com suporte chamando **IWMDMDevice3:: GetProperty** e passando em g \_ wszWMDMFormatsSupported.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-153">Request a list of all format codes supported by calling **IWMDMDevice3::GetProperty** and passing in g\_wszWMDMFormatsSupported.</span></span> <span data-ttu-id="5f0e1-154">Isso retorna um **PROPVARIANT** contendo uma **SafeArray** de formatos com suporte.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-154">This returns a **PROPVARIANT** containing a **SAFEARRAY** of supported formats.</span></span>
2.  <span data-ttu-id="5f0e1-155">Faça um loop pelos elementos chamando **SafeArrayGetElement**.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-155">Loop through the elements by calling **SafeArrayGetElement**.</span></span> <span data-ttu-id="5f0e1-156">Cada elemento é uma enumeração **WMDM \_ FORMATCODE** .</span><span class="sxs-lookup"><span data-stu-id="5f0e1-156">Each element is a **WMDM\_FORMATCODE** enumeration.</span></span>
3.  <span data-ttu-id="5f0e1-157">Solicite os recursos para cada formato, liberando a memória para cada elemento de **\_ \_ capacidade de formato do WMDM** depois de feito com ele.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-157">Request the capabilities for each format, freeing the memory for each **WMDM\_FORMAT\_CAPABILITY** element once done with it.</span></span>
4.  <span data-ttu-id="5f0e1-158">Desmarque o **PROPVARIANT** recuperado na etapa 1 chamando **PropVariantClear**.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-158">Clear the **PROPVARIANT** retrieved in step 1 by calling **PropVariantClear**.</span></span>

<span data-ttu-id="5f0e1-159">O seguinte código de exemplo C++ recupera uma lista de formatos com suporte para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-159">The following C++ example code retrieves a list of supported formats for a device.</span></span>


```C++
// Query a device for supported configurations for each media or format type. 
HRESULT CWMDMController::GetCaps(IWMDMDevice3* pDevice)
{
    HRESULT hr = S_OK;

    // Request the "formats supported" property to get a list of supported formats.
    PROPVARIANT pvFormatsSupported;
    PropVariantInit(&pvFormatsSupported);
    hr = pDevice->GetProperty(g_wszWMDMFormatsSupported, &pvFormatsSupported);
    HANDLE_HR(hr, "Got a property list in GetCaps", "Couldn't get a property list in GetCaps.");

    // Loop through the retrieved format list.
    // For each format, get a list of format configurations.
    SAFEARRAY* formatList = pvFormatsSupported.parray;
    WMDM_FORMATCODE formatCode = WMDM_FORMATCODE_NOTUSED;
    for (LONG iCap = 0; iCap < formatList->rgsabound[0].cElements; iCap++)
    { 
        // Get a format from the SAFEARRAY of retrieved formats.
        SafeArrayGetElement(formatList, &iCap, &formatCode);

        // Call a custom function to request the format capabilities.
        if (formatCode != WMDM_FORMATCODE_NOTUSED)
            myGetFormatCaps(formatCode, pDevice);
    }

e_Exit:
    // Clear out the memory we used.
    PropVariantClear(&pvFormatsSupported);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="5f0e1-160">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f0e1-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f0e1-161">**Descobrindo recursos de formato de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="5f0e1-161">**Discovering Device Format Capabilities**</span></span>](discovering-device-format-capabilities.md)
</dt> </dl>

 

 




