---
description: Implementando DllRegisterServer
ms.assetid: aaa4069e-0b6a-4a76-b950-1a85a9ed969d
title: Implementando DllRegisterServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b994e80a181b69efffbe6123382957e7a38f8278
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087778"
---
# <a name="implementing-dllregisterserver"></a><span data-ttu-id="1746f-103">Implementando DllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="1746f-103">Implementing DllRegisterServer</span></span>

<span data-ttu-id="1746f-104">A etapa final é implementar a função **DllRegisterServer** .</span><span class="sxs-lookup"><span data-stu-id="1746f-104">The final step is to implement the **DllRegisterServer** function.</span></span> <span data-ttu-id="1746f-105">A DLL que contém o componente deve exportar essa função.</span><span class="sxs-lookup"><span data-stu-id="1746f-105">The DLL that contains the component must export this function.</span></span> <span data-ttu-id="1746f-106">A função será chamada por um aplicativo de configuração ou quando o usuário executar a ferramenta de Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="1746f-106">The function will be called by a set-up application, or when the user runs the Regsvr32.exe tool.</span></span>

<span data-ttu-id="1746f-107">O exemplo a seguir mostra uma implementação mínima de **DlLRegisterServer**:</span><span class="sxs-lookup"><span data-stu-id="1746f-107">The following example shows a minimal implementation of **DlLRegisterServer**:</span></span>


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



<span data-ttu-id="1746f-108">A função [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) cria entradas de registro para cada componente no</span><span class="sxs-lookup"><span data-stu-id="1746f-108">The [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function creates registry entries for every component in the</span></span>


```
g_Templates
```



<span data-ttu-id="1746f-109">matriz.</span><span class="sxs-lookup"><span data-stu-id="1746f-109">array.</span></span> <span data-ttu-id="1746f-110">No entanto, essa função tem algumas limitações.</span><span class="sxs-lookup"><span data-stu-id="1746f-110">However, this function has some limitations.</span></span> <span data-ttu-id="1746f-111">Primeiro, ele atribui todos os filtros à categoria "filtros do DirectShow" (CLSID \_ LegacyAmFilterCategory), mas nem todos os filtros pertencem a essa categoria.</span><span class="sxs-lookup"><span data-stu-id="1746f-111">First, it assigns every filter to the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory), but not every filter belongs in this category.</span></span> <span data-ttu-id="1746f-112">Filtros de captura e filtros de compactação, por exemplo, têm suas próprias categorias.</span><span class="sxs-lookup"><span data-stu-id="1746f-112">Capture filters and compression filters, for example, have their own categories.</span></span> <span data-ttu-id="1746f-113">Em segundo lugar, se o filtro der suporte a um dispositivo de hardware, talvez seja necessário registrar duas partes adicionais de informações que o **AMovieDLLRegisterServer2** não manipula: a *média* e a *categoria do PIN*.</span><span class="sxs-lookup"><span data-stu-id="1746f-113">Second, if your filter supports a hardware device, you might need to register two additional pieces of information that **AMovieDLLRegisterServer2** does not handle: the *medium* and the *pin category*.</span></span> <span data-ttu-id="1746f-114">Um meio define um método de comunicação em um dispositivo de hardware, como um barramento.</span><span class="sxs-lookup"><span data-stu-id="1746f-114">A medium defines a method of communication in a hardware device, such as a bus.</span></span> <span data-ttu-id="1746f-115">A categoria de PIN define a função de um PIN.</span><span class="sxs-lookup"><span data-stu-id="1746f-115">The pin category defines the function of a pin.</span></span> <span data-ttu-id="1746f-116">Para obter informações sobre médias, consulte "KSPIN \_ Medium" no Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="1746f-116">For information on mediums, see "KSPIN\_MEDIUM" in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="1746f-117">Para obter uma lista de categorias de PIN, consulte [Pin Property Set](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="1746f-117">For a list of pin categories, see [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="1746f-118">Se você quiser especificar uma categoria de filtro, uma média ou uma categoria de PIN, chame o método [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) de em **DllRegisterServer**.</span><span class="sxs-lookup"><span data-stu-id="1746f-118">If you want to specify a filter category, a medium, or a pin category, call the [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method from within **DllRegisterServer**.</span></span> <span data-ttu-id="1746f-119">Esse método usa um ponteiro para uma estrutura [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) , que especifica informações sobre o filtro.</span><span class="sxs-lookup"><span data-stu-id="1746f-119">This method takes a pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure, which specifies information about the filter.</span></span>

<span data-ttu-id="1746f-120">Para complicar as questões, a estrutura **REGFILTER2** dá suporte a dois formatos diferentes para o registro de Pins.</span><span class="sxs-lookup"><span data-stu-id="1746f-120">To complicate matters somewhat, the **REGFILTER2** structure supports two different formats for registering pins.</span></span> <span data-ttu-id="1746f-121">O membro **DW** especifica o formato:</span><span class="sxs-lookup"><span data-stu-id="1746f-121">The **dwVersion** member specifies the format:</span></span>

-   <span data-ttu-id="1746f-122">Se **DW** for 1, o formato do PIN será **AMOVIESETUP \_ PIN** (descrito anteriormente).</span><span class="sxs-lookup"><span data-stu-id="1746f-122">If **dwVersion** is 1, the pin format is **AMOVIESETUP\_PIN** (described previously).</span></span>
-   <span data-ttu-id="1746f-123">Se **DW** for 2, o formato do PIN será [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).</span><span class="sxs-lookup"><span data-stu-id="1746f-123">If **dwVersion** is 2, the pin format is [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).</span></span>

<span data-ttu-id="1746f-124">A estrutura **REGFILTERPINS2** inclui entradas para médias de PIN e categorias de PIN.</span><span class="sxs-lookup"><span data-stu-id="1746f-124">The **REGFILTERPINS2** structure includes entries for pin mediums and pin categories.</span></span> <span data-ttu-id="1746f-125">Além disso, ele usa sinalizadores de bit para alguns itens que **AMOVIESETUP \_ PIN** declara como valores Boolianos.</span><span class="sxs-lookup"><span data-stu-id="1746f-125">Also, it uses bit flags for some items that **AMOVIESETUP\_PIN** declares as Boolean values.</span></span>

<span data-ttu-id="1746f-126">O exemplo a seguir mostra como chamar **IFilterMapper2:: RegisterFilter** de dentro de **DllRegisterServer**:</span><span class="sxs-lookup"><span data-stu-id="1746f-126">The following example shows how to call **IFilterMapper2::RegisterFilter** from inside **DllRegisterServer**:</span></span>


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



 

 



