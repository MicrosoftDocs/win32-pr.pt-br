---
description: Enumerando efeitos e transições
ms.assetid: 364b7bfb-5d6e-4ca6-b0c8-7a0180c3f61a
title: Enumerando efeitos e transições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e533f36501ac8da6015cc31eea6c2c111bf6a208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105759556"
---
# <a name="enumerating-effects-and-transitions"></a>Enumerando efeitos e transições

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

O DirectShow fornece um objeto [enumerador de dispositivo do sistema](system-device-enumerator.md) para enumerar dispositivos. Você pode usá-lo para recuperar os monikers para efeitos ou transições instalados no sistema do usuário.

O enumerador de dispositivo do sistema expõe a interface [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) . Ele retorna enumeradores de categoria para categorias de dispositivo especificadas. Um enumerador de categoria, por sua vez, expõe a interface [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) e retorna monikers para cada dispositivo na categoria. Para obter uma discussão detalhada sobre como usar o **ICreateDevEnum**, consulte [enumerando dispositivos e filtros](enumerating-devices-and-filters.md). Veja a seguir um breve resumo, específico dos serviços de edição do DirectShow.

Para enumerar efeitos ou transições, execute as etapas a seguir.

1.  Crie uma instância do enumerador de dispositivo do sistema.
2.  Chame o método [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) para recuperar um enumerador de categoria. As categorias são definidas por identificadores de classe (CLSIDs). Use CLSID \_ VideoEffects1Category para efeitos ou \_ VideoEffects2Category CLSID para transições.
3.  Chame **IEnumMoniker:: Next** para recuperar cada moniker na enumeração.
4.  Para cada moniker, chame **IMoniker:: BindToStorage** para recuperar seu recipiente de propriedades associado.

O recipiente de propriedades contém o nome amigável e o GUID (identificador global exclusivo) para o efeito ou a transição. Um aplicativo pode exibir uma lista de nomes amigáveis e, em seguida, obter o GUID correspondente.

O exemplo de código a seguir ilustra essas etapas.


```C++
ICreateDevEnum *pCreateDevEnum = NULL;
IEnumMoniker *pEnumMoniker = NULL;

// Create the System Device Enumerator.
HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
    CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, (void**)&pCreateDevEnum);
if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

// Create an enumerator for the video effects category.
hr = pCreateDevEnum->CreateClassEnumerator(
    CLSID_VideoEffects1Category,  // Video effects category. 
    &pEnumMoniker, 0);               

// Note: Use CLSID_VideoEffects2Category for video transitions.

if (hr == S_OK)  // S_FALSE means the category is empty.
{
    // Enumerate each video effect.
    IMoniker *pMoniker;
    while (S_OK == pEnumMoniker->Next(1, &pMoniker, NULL))
    {
        IPropertyBag *pBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pBag);
        if(FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(OLESTR("FriendlyName"), &var, NULL);
        if (SUCCEEDED(hr))
        {
            if ( ... )  // Check if var.bstrVal is the name you want.
            {
                VARIANT var2;
                GUID guid;
                var2.vt = VT_BSTR;
                pBag->Read(OLESTR("guid"), &var2, NULL);
                CLSIDFromString(var2.bstrVal, &guid);
                VariantClear(&var2);
                // GUID is now the CLSID for the effect.
            }
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnumMoniker->Release();
}
pCreateDevEnum->Release();
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com efeitos e transições](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
