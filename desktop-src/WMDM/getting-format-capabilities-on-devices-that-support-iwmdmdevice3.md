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
# <a name="getting-format-capabilities-through-iwmdmdevice3"></a>Obtendo recursos de formato por meio de IWMDMDevice3

[**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) é o método preferencial para solicitar a um dispositivo quais formatos ele dá suporte. As etapas a seguir mostram como usar esse método para consultar um dispositivo em busca de seus recursos de formato:

1.  O aplicativo deve determinar a quais formatos um dispositivo dá suporte e quais são de interesse. Para fazer isso, o aplicativo pode solicitar uma lista de formatos com suporte pelo dispositivo chamando [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty).
2.  O aplicativo executa um loop em todos os formatos com suporte e solicita os recursos de formato de um dispositivo para um formato específico (como WMA ou WMV) chamando **IWMDMDevice3:: GetFormatCapability** e especificando um formato usando a enumeração [**WMDM \_ FORMATCODE**](wmdm-formatcode.md) . Esse método recupera uma estrutura de [**\_ \_ recursos de formato do WMDM**](wmdm-format-capability.md) .
3.  Execute o loop através de todas as estruturas de [**\_ \_ configuração do WMDM prop**](wmdm-prop-config.md) na estrutura de **\_ \_ recursos do formato WMDM** recuperada. Cada estrutura de **\_ \_ configuração do WMDM prop** contém um grupo de propriedades com valores com suporte, representando uma configuração para esse formato. Cada configuração tem um número de preferência, em que um número mais baixo indica uma preferência maior pelo dispositivo.
4.  Execute o loop através de todas as estruturas [**\_ \_ desc prop do WMDM**](wmdm-prop-desc.md) na **configuração de \_ prop \_ do WMDM** recuperada. Cada **WMDM \_ prop \_ desc** contém uma lista de pares de propriedade/valor com suporte.
5.  Recupere os nomes de propriedade e os valores da estrutura de **\_ \_ desc prop do WMDM** . As propriedades incluem taxa de bits, codec e tamanho do quadro. Os nomes de propriedade são definidos no arquivo de cabeçalho mswmdm. h; uma lista da maioria dessas constantes é fornecida nas [constantes de metadados](metadata-constants.md). Três tipos de valores de propriedade são possíveis:
    -   Um único valor, WMDM \_ enum \_ prop \_ \_ valores válidos \_ , indicando suporte para quaisquer valores dessa propriedade.
    -   Um intervalo de valores, definido por um valor máximo, valor mínimo e intervalo.
    -   Uma lista de valores discretos.
6.  Limpe os valores armazenados. A memória para esses valores é alocada pelo Windows Media Gerenciador de Dispositivos; seu dispositivo é responsável por liberar a memória. Como fazer isso é descrito no final deste tópico.

Ao responder a **GetFormatCapability**, um dispositivo pode reportar \_ \_ \_ valores válidos de prop Enumerate para o \_ \_ **recurso de \_ formato WMDM \_ . configuração de prop do WMDM \_ \_ . WMDM \_ prop \_ desc. ValidValuesForm** para solicitar suporte para quaisquer valores de taxa de bits, canais e assim por diante. No entanto, você deve tratar essa declaração com cautela, pois os dispositivos podem, às vezes, relatar suporte para quaisquer valores quando, na verdade, não dão suporte a todas as taxas de bits ou tamanhos de imagem. Você pode considerar que o aplicativo transcodificará arquivos extremamente grandes ou de alta taxa de bits para versões menores ou para versões com uso intensivo de CPU e uso intensivo de memória ao enviá-los para dispositivos que se destinam a reproduzir esses arquivos.

A função C++ a seguir mostra como solicitar suporte a formato de dispositivo para um formato específico.


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



**Limpando a memória alocada**

Depois de recuperar os recursos de formato de um dispositivo, o aplicativo deve liberar a memória alocada para manter a descrição. [**GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) e [**GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2) têm matrizes de estruturas simples que podem ser limpas simplesmente chamando **CoTaskMemFree** com a matriz. No entanto, o **GetFormatCapability** tem uma estrutura de dados mais complexa com memória alocada dinamicamente que deve ser limpa por meio de um loop por todos os elementos e liberando-os individualmente.

O código C++ a seguir mostra como um aplicativo pode liberar a memória alocada para uma estrutura de **\_ \_ recursos de formato do WMDM** .


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



**Consultando todos os formatos com suporte**

Normalmente, um aplicativo consulta um dispositivo em busca de um formato específico, pois ele está interessado em enviar um arquivo específico para o dispositivo. No entanto, se você quiser consultar um aplicativo para todos os seus formatos com suporte, você pode chamar [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) e passar g \_ wszWMDMFormatsSupported para recuperar uma lista completa.

Se um dispositivo retornar apenas um elemento, WMDM \_ FORMATCODE \_ indefinido, isso geralmente significa que o dispositivo não oferece suporte a códigos de formato. Chamar **GetFormatCapability** com WMDM \_ FORMATCODE \_ indefinido pode recuperar recursos, mas essas propriedades podem ser razoavelmente genéricas (como nome, tamanho do arquivo, data da última modificação e assim por diante).

As etapas a seguir mostram como consultar uma lista de todos os formatos com suporte:

1.  Solicite uma lista de todos os códigos de formatação com suporte chamando **IWMDMDevice3:: GetProperty** e passando em g \_ wszWMDMFormatsSupported. Isso retorna um **PROPVARIANT** contendo uma **SafeArray** de formatos com suporte.
2.  Faça um loop pelos elementos chamando **SafeArrayGetElement**. Cada elemento é uma enumeração **WMDM \_ FORMATCODE** .
3.  Solicite os recursos para cada formato, liberando a memória para cada elemento de **\_ \_ capacidade de formato do WMDM** depois de feito com ele.
4.  Desmarque o **PROPVARIANT** recuperado na etapa 1 chamando **PropVariantClear**.

O seguinte código de exemplo C++ recupera uma lista de formatos com suporte para um dispositivo.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Descobrindo recursos de formato de dispositivo**](discovering-device-format-capabilities.md)
</dt> </dl>

 

 




