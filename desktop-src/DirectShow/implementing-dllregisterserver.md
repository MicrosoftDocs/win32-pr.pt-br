---
description: Implementando DllRegisterServer
ms.assetid: aaa4069e-0b6a-4a76-b950-1a85a9ed969d
title: Implementando DllRegisterServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39d55b73dd70a21c10df26a100f964917a57dd9f036ebd5c2708359bca1dd50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998087"
---
# <a name="implementing-dllregisterserver"></a>Implementando DllRegisterServer

A etapa final é implementar a função **DllRegisterServer** . A DLL que contém o componente deve exportar essa função. A função será chamada por um aplicativo de configuração ou quando o usuário executar a ferramenta de Regsvr32.exe.

O exemplo a seguir mostra uma implementação mínima de **DlLRegisterServer**:


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



A função [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) cria entradas de registro para cada componente no


```
g_Templates
```



matriz. No entanto, essa função tem algumas limitações. primeiro, ele atribui todos os filtros à categoria "filtros de DirectShow" (CLSID \_ LegacyAmFilterCategory), mas nem todos os filtros pertencem a essa categoria. Filtros de captura e filtros de compactação, por exemplo, têm suas próprias categorias. Em segundo lugar, se o filtro der suporte a um dispositivo de hardware, talvez seja necessário registrar duas partes adicionais de informações que o **AMovieDLLRegisterServer2** não manipula: a *média* e a *categoria do PIN*. Um meio define um método de comunicação em um dispositivo de hardware, como um barramento. A categoria de PIN define a função de um PIN. para obter informações sobre médias, consulte "KSPIN \_ medium" no Microsoft Windows Driver Development Kit (DDK). Para obter uma lista de categorias de PIN, consulte [Pin Property Set](pin-property-set.md).

Se você quiser especificar uma categoria de filtro, uma média ou uma categoria de PIN, chame o método [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) de em **DllRegisterServer**. Esse método usa um ponteiro para uma estrutura [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) , que especifica informações sobre o filtro.

Para complicar as questões, a estrutura **REGFILTER2** dá suporte a dois formatos diferentes para o registro de Pins. O membro **DW** especifica o formato:

-   Se **DW** for 1, o formato do PIN será **AMOVIESETUP \_ PIN** (descrito anteriormente).
-   Se **DW** for 2, o formato do PIN será [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).

A estrutura **REGFILTERPINS2** inclui entradas para médias de PIN e categorias de PIN. Além disso, ele usa sinalizadores de bit para alguns itens que **AMOVIESETUP \_ PIN** declara como valores Boolianos.

O exemplo a seguir mostra como chamar **IFilterMapper2:: RegisterFilter** de dentro de **DllRegisterServer**:


```C++
REGFILTER2 rf2FilterReg = {
    1,              // Version 1 (no pin mediums or pin category).
    MERIT_NORMAL,   // Merit.
    1,              // Number of pins.
    &sudPins        // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
        return hr;

    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->RegisterFilter(
        CLSID_SomeFilter,                // Filter CLSID. 
        g_wszName,                       // Filter name.
        NULL,                            // Device moniker. 
        &CLSID_VideoCompressorCategory,  // Video compressor category.
        g_wszName,                       // Instance data.
        &rf2FilterReg                    // Pointer to filter information.
    );
    pFM2->Release();
    return hr;
}
```



 

 



