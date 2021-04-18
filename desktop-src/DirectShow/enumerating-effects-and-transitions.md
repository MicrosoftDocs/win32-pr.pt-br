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
# <a name="enumerating-effects-and-transitions"></a><span data-ttu-id="dd90f-103">Enumerando efeitos e transições</span><span class="sxs-lookup"><span data-stu-id="dd90f-103">Enumerating Effects and Transitions</span></span>

<span data-ttu-id="dd90f-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="dd90f-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="dd90f-105">O DirectShow fornece um objeto [enumerador de dispositivo do sistema](system-device-enumerator.md) para enumerar dispositivos.</span><span class="sxs-lookup"><span data-stu-id="dd90f-105">DirectShow provides a [System Device Enumerator](system-device-enumerator.md) object for enumerating devices.</span></span> <span data-ttu-id="dd90f-106">Você pode usá-lo para recuperar os monikers para efeitos ou transições instalados no sistema do usuário.</span><span class="sxs-lookup"><span data-stu-id="dd90f-106">You can use it to retrieve monikers for effects or transitions installed on the user's system.</span></span>

<span data-ttu-id="dd90f-107">O enumerador de dispositivo do sistema expõe a interface [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .</span><span class="sxs-lookup"><span data-stu-id="dd90f-107">The system device enumerator exposes the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span> <span data-ttu-id="dd90f-108">Ele retorna enumeradores de categoria para categorias de dispositivo especificadas.</span><span class="sxs-lookup"><span data-stu-id="dd90f-108">It returns category enumerators for specified device categories.</span></span> <span data-ttu-id="dd90f-109">Um enumerador de categoria, por sua vez, expõe a interface [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) e retorna monikers para cada dispositivo na categoria.</span><span class="sxs-lookup"><span data-stu-id="dd90f-109">A category enumerator, in turn, exposes the [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) interface and returns monikers for each device in the category.</span></span> <span data-ttu-id="dd90f-110">Para obter uma discussão detalhada sobre como usar o **ICreateDevEnum**, consulte [enumerando dispositivos e filtros](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="dd90f-110">For a detailed discussion of using **ICreateDevEnum**, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span> <span data-ttu-id="dd90f-111">Veja a seguir um breve resumo, específico dos serviços de edição do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dd90f-111">The following is a brief summary, specific to DirectShow Editing Services.</span></span>

<span data-ttu-id="dd90f-112">Para enumerar efeitos ou transições, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="dd90f-112">To enumerate effects or transitions, perform the following steps.</span></span>

1.  <span data-ttu-id="dd90f-113">Crie uma instância do enumerador de dispositivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="dd90f-113">Create an instance of the system device enumerator.</span></span>
2.  <span data-ttu-id="dd90f-114">Chame o método [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) para recuperar um enumerador de categoria.</span><span class="sxs-lookup"><span data-stu-id="dd90f-114">Call the [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method to retrieve a category enumerator.</span></span> <span data-ttu-id="dd90f-115">As categorias são definidas por identificadores de classe (CLSIDs).</span><span class="sxs-lookup"><span data-stu-id="dd90f-115">Categories are defined by class identifiers (CLSIDs).</span></span> <span data-ttu-id="dd90f-116">Use CLSID \_ VideoEffects1Category para efeitos ou \_ VideoEffects2Category CLSID para transições.</span><span class="sxs-lookup"><span data-stu-id="dd90f-116">Use CLSID\_VideoEffects1Category for effects or CLSID\_VideoEffects2Category for transitions.</span></span>
3.  <span data-ttu-id="dd90f-117">Chame **IEnumMoniker:: Next** para recuperar cada moniker na enumeração.</span><span class="sxs-lookup"><span data-stu-id="dd90f-117">Call **IEnumMoniker::Next** to retrieve each moniker in the enumeration.</span></span>
4.  <span data-ttu-id="dd90f-118">Para cada moniker, chame **IMoniker:: BindToStorage** para recuperar seu recipiente de propriedades associado.</span><span class="sxs-lookup"><span data-stu-id="dd90f-118">For each moniker, call **IMoniker::BindToStorage** to retrieve its associated property bag.</span></span>

<span data-ttu-id="dd90f-119">O recipiente de propriedades contém o nome amigável e o GUID (identificador global exclusivo) para o efeito ou a transição.</span><span class="sxs-lookup"><span data-stu-id="dd90f-119">The property bag contains the friendly name and the globally unique identifier (GUID) for the effect or transition.</span></span> <span data-ttu-id="dd90f-120">Um aplicativo pode exibir uma lista de nomes amigáveis e, em seguida, obter o GUID correspondente.</span><span class="sxs-lookup"><span data-stu-id="dd90f-120">An application can display a list of friendly names and then obtain the corresponding GUID.</span></span>

<span data-ttu-id="dd90f-121">O exemplo de código a seguir ilustra essas etapas.</span><span class="sxs-lookup"><span data-stu-id="dd90f-121">The following code example illustrates these steps.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="dd90f-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd90f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd90f-123">Trabalhando com efeitos e transições</span><span class="sxs-lookup"><span data-stu-id="dd90f-123">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
