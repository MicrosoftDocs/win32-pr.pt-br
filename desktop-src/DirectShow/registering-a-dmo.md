---
description: Registrando um DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: Registrando um DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c5364304fd5f6a9557c84a4b27c86d29fa4e84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757871"
---
# <a name="registering-a-dmo"></a><span data-ttu-id="885e8-103">Registrando um DMO</span><span class="sxs-lookup"><span data-stu-id="885e8-103">Registering a DMO</span></span>

<span data-ttu-id="885e8-104">Para que os clientes usem o DMO, o CLSID deve ser registrado no sistema do usuário.</span><span class="sxs-lookup"><span data-stu-id="885e8-104">In order for clients to use your DMO, the CLSID must be registered on the user's system.</span></span> <span data-ttu-id="885e8-105">Isso é feito por meio da função **DllRegisterServer** da dll.</span><span class="sxs-lookup"><span data-stu-id="885e8-105">This is done through the DLL's **DllRegisterServer** function.</span></span> <span data-ttu-id="885e8-106">Se você estiver usando o Active Template Library (ATL), o assistente ATL gerará automaticamente essa função.</span><span class="sxs-lookup"><span data-stu-id="885e8-106">If you are using the Active Template Library (ATL), the ATL wizard automatically generates this function.</span></span>

<span data-ttu-id="885e8-107">Você também pode registrar o DMO em uma ou mais categorias de DMO padrão.</span><span class="sxs-lookup"><span data-stu-id="885e8-107">You can also register your DMO under one or more standard DMO categories.</span></span> <span data-ttu-id="885e8-108">Isso permite que os clientes descubram o DMO usando a função [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) .</span><span class="sxs-lookup"><span data-stu-id="885e8-108">This enables clients to discover your DMO using the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function.</span></span> <span data-ttu-id="885e8-109">As categorias são definidas por GUID e são listadas na seção [GUIDs de DMO](dmo-guids.md).</span><span class="sxs-lookup"><span data-stu-id="885e8-109">The categories are defined by GUID, and are listed in the section [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="885e8-110">O registro de um DMO em uma categoria é opcional.</span><span class="sxs-lookup"><span data-stu-id="885e8-110">Registering a DMO under a category is optional.</span></span> <span data-ttu-id="885e8-111">Para fazer isso, chame a função [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) e especifique o nome amigável do DMO, CLSID e a categoria.</span><span class="sxs-lookup"><span data-stu-id="885e8-111">To do so, call the [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) function and specify the friendly name of the DMO, the CLSID, and the category.</span></span> <span data-ttu-id="885e8-112">Opcionalmente, você também pode registrar um conjunto de tipos de mídia aos quais seu DMOs dá suporte.</span><span class="sxs-lookup"><span data-stu-id="885e8-112">Optionally, you can also register a set of media types that your DMOs supports.</span></span> <span data-ttu-id="885e8-113">Para obter mais informações, consulte [tipos de mídia DMO](dmo-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="885e8-113">For more information, see [DMO Media Types](dmo-media-types.md).</span></span>

<span data-ttu-id="885e8-114">O exemplo a seguir mostra como registrar um efeito de áudio DMO que dá suporte a entrada e saída de áudio PCM.</span><span class="sxs-lookup"><span data-stu-id="885e8-114">The following example shows how to register an audio effect DMO that supports PCM audio input and output.</span></span> <span data-ttu-id="885e8-115">Nesse caso, os tipos de entrada e os tipos de saída são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="885e8-115">In this case the input types and output types are the same.</span></span>


```C++
STDAPI DllRegisterServer(void)
{
    // Register the DMO as a PCM audio effect DMO
    DMO_PARTIAL_MEDIATYPE mt;
    mt.type    = MEDIATYPE_Audio;
    mt.subtype = MEDIASUBTYPE_PCM;
    HRESULT hr = DMORegister(
        L"MyDMO",                  // Friendly name
        CLSID_MyDMO,               // CLSID
        DMOCATEGORY_AUDIO_EFFECT,  // Category
        0,                         // Flags 
        1,                         // Number of input types
        &mt,                       // Array of input types
        1,                         // Number of output types
        &mt);                      // Array of output types

    if (FAILED(hr)) return hr;

    // Registers the object, with no typelib.
    return _Module.RegisterServer(FALSE);
}
```



<span data-ttu-id="885e8-116">Este exemplo supõe que a ATL foi usada para criar o projeto; a última linha da função chama o método ATL padrão para registrar o servidor COM.</span><span class="sxs-lookup"><span data-stu-id="885e8-116">This example assumes that ATL was used to create the project; the last line of the function calls the standard ATL method to register the COM server.</span></span> <span data-ttu-id="885e8-117">Se você não estiver usando a ATL, sua função terá uma aparência diferente.</span><span class="sxs-lookup"><span data-stu-id="885e8-117">If you are not using ATL, your function will look different.</span></span>

<span data-ttu-id="885e8-118">**Cancelando o registro de um DMO**</span><span class="sxs-lookup"><span data-stu-id="885e8-118">**Unregistering a DMO**</span></span>

<span data-ttu-id="885e8-119">Sua função **DllUnregisterServer** deve remover todas as entradas do registro que a função **DllRegisterServer** cria.</span><span class="sxs-lookup"><span data-stu-id="885e8-119">Your **DllUnregisterServer** function must remove any registry entries that the **DllRegisterServer** function creates.</span></span> <span data-ttu-id="885e8-120">Se você chamar **DMORegister** ao registrar o DMO, deverá [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) com a mesma categoria ao cancelar o registro do DMO.</span><span class="sxs-lookup"><span data-stu-id="885e8-120">If you call **DMORegister** when you register the DMO, you must [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) with the same category when you unregister the DMO.</span></span>

<span data-ttu-id="885e8-121">O exemplo a seguir remove as entradas do registro criadas no exemplo anterior:</span><span class="sxs-lookup"><span data-stu-id="885e8-121">The following example removes the registry entries created in the previous example:</span></span>


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



<span data-ttu-id="885e8-122">**Valores de mérito do DirectShow**</span><span class="sxs-lookup"><span data-stu-id="885e8-122">**DirectShow Merit Values**</span></span>

<span data-ttu-id="885e8-123">Para fins de criação de gráficos de filtro, o DirectShow atribui um valor de mérito padrão a DMOs.</span><span class="sxs-lookup"><span data-stu-id="885e8-123">For purposes of building filter graphs, DirectShow assigns a default merit value to DMOs.</span></span> <span data-ttu-id="885e8-124">Você pode substituir esse valor adicionando uma entrada de registro à chave do registro do DMO em \_ classe HKEY \_ raiz \\ CLSID.</span><span class="sxs-lookup"><span data-stu-id="885e8-124">You can override this value by adding a registry entry to the DMO's registry key in HKEY\_CLASSES\_ROOT\\CLSID.</span></span> <span data-ttu-id="885e8-125">Inclua um valor **DWORD** chamado `Merit` cujo valor especifique o mérito.</span><span class="sxs-lookup"><span data-stu-id="885e8-125">Include a **DWORD** value named `Merit` whose value specifies the merit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="885e8-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="885e8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="885e8-127">Escrevendo um DMO</span><span class="sxs-lookup"><span data-stu-id="885e8-127">Writing a DMO</span></span>](writing-a-dmo.md)
</dt> </dl>

 

 



