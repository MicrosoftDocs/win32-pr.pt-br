---
description: Etapa 10.
ms.assetid: 2959f574-1a39-4db1-9e4a-a303d0c7f8f3
title: Etapa 10. Suporte ao registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fead7e3448d8f02fd477141699e1107ca288afd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758426"
---
# <a name="step-10-support-com-registration"></a><span data-ttu-id="38b2f-104">Etapa 10.</span><span class="sxs-lookup"><span data-stu-id="38b2f-104">Step 10.</span></span> <span data-ttu-id="38b2f-105">Suporte ao registro COM</span><span class="sxs-lookup"><span data-stu-id="38b2f-105">Support COM Registration</span></span>

<span data-ttu-id="38b2f-106">A última tarefa restante é oferecer suporte ao registro COM, para que o quadro de propriedades possa criar novas instâncias da sua página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="38b2f-106">The last remaining task is to support COM registration, so that the property frame can create new instances of your property page.</span></span> <span data-ttu-id="38b2f-107">Adicione outra entrada [**CFactoryTemplate**](cfactorytemplate.md) à matriz de *\_ modelos g* globais, que é usada para registrar todos os objetos com em sua dll.</span><span class="sxs-lookup"><span data-stu-id="38b2f-107">Add another [**CFactoryTemplate**](cfactorytemplate.md) entry to the global *g\_Templates* array, which is used to register all of the COM objects in your DLL.</span></span> <span data-ttu-id="38b2f-108">Não inclua nenhuma informação de configuração de filtro para a página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="38b2f-108">Do not include any filter set-up information for the property page.</span></span>


```C++
const AMOVIESETUP_FILTER FilterSetupData = 
{ 
    /* Not shown ... */
};

CFactoryTemplate g_Templates[] =
{   
    // This entry is for the filter.
    {
        wszName,
        &CLSID_GrayFilter,
        CGrayFilter::CreateInstance,
        NULL,
        &FilterSetupData 
    },
    // This entry is for the property page.
    { 
        L"Saturation Props",
        &CLSID_SaturationProp,
        CGrayProp::CreateInstance, 
        NULL, NULL
    }
};
```



<span data-ttu-id="38b2f-109">Se você declarar *g \_ cTemplates* conforme mostrado no código a seguir, ele automaticamente terá o valor correto com base no tamanho da matriz:</span><span class="sxs-lookup"><span data-stu-id="38b2f-109">If you declare *g\_cTemplates* as shown in the following code, then it automatically has the correct value based on the array size:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates)/sizeof(g_Templates[0]);
```



<span data-ttu-id="38b2f-110">Além disso, adicione um `CreateInstance` método estático à classe de página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="38b2f-110">Also, add a static `CreateInstance` method to the property page class.</span></span> <span data-ttu-id="38b2f-111">Você pode nomear o método de qualquer forma que preferir, mas a assinatura deve corresponder à mostrada no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="38b2f-111">You can name the method anything that you prefer, but the signature must match the one shown the following example:</span></span>


```C++
static CUnknown * WINAPI CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CGrayProp *pNewObject = new CGrayProp(pUnk);
    if (pNewObject == NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 
```



<span data-ttu-id="38b2f-112">Para testar a página de propriedades, registre a DLL e, em seguida, carregue o filtro em GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="38b2f-112">To test the property page, register the DLL and then load the filter in GraphEdit.</span></span> <span data-ttu-id="38b2f-113">Clique com o botão direito do mouse no filtro e selecione **Propriedades do filtro**.</span><span class="sxs-lookup"><span data-stu-id="38b2f-113">Right-click the filter and select **Filter Properties**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38b2f-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="38b2f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38b2f-115">Criando uma página de propriedades de filtro</span><span class="sxs-lookup"><span data-stu-id="38b2f-115">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> <dt>

[<span data-ttu-id="38b2f-116">Como criar uma DLL de filtro do DirectShow</span><span class="sxs-lookup"><span data-stu-id="38b2f-116">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 



