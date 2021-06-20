---
description: Expor as novas interfaces de um filtro aos clientes como parte da criação de uma página de propriedades de filtro para um filtro DirectShow personalizado.
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: Etapa 3. Suporte a QueryInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b62132a6f24c68453ad4e51f72cdd9a2a78c65
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410019"
---
# <a name="step-3-support-queryinterface"></a><span data-ttu-id="eda60-104">Etapa 3.</span><span class="sxs-lookup"><span data-stu-id="eda60-104">Step 3.</span></span> <span data-ttu-id="eda60-105">Suporte a QueryInterface</span><span class="sxs-lookup"><span data-stu-id="eda60-105">Support QueryInterface</span></span>

<span data-ttu-id="eda60-106">Para expor as novas interfaces do filtro aos clientes, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="eda60-106">To expose the filter's new interfaces to clients, do the following:</span></span>

-   <span data-ttu-id="eda60-107">Inclua a [**macro DECLARE \_ IUNKNOWN**](declare-iunknown.md) na seção de declaração pública do filtro:</span><span class="sxs-lookup"><span data-stu-id="eda60-107">Include the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section of your filter:</span></span>
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   <span data-ttu-id="eda60-108">Substitua [**CUnknown::NonDeltingQueryInterface**](cunknown-nondelegatingqueryinterface.md) para verificar os IIDs das duas interfaces:</span><span class="sxs-lookup"><span data-stu-id="eda60-108">Override [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IIDs of the two interfaces:</span></span>
    ```C++
    STDMETHODIMP CGrayFilter::NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if (riid == IID_ISpecifyPropertyPages)
        {
            return GetInterface(
               static_cast<ISpecifyPropertyPages*>(this),
               ppv);
        }
        else if (riid == IID_ISaturation)
        {
            return GetInterface(static_cast<ISaturation*>(this), ppv);
        }
        else
        {
            // Call the parent class.
            return CBaseFilter::NonDelegatingQueryInterface(riid, ppv);

            // NOTE: This example assumes that the filter inherits directly
            // from CBaseFilter. If your filter inherits from another class,
            // call the NonDelegatingQueryInterface method of that class.
        }
    }
    ```

    

<span data-ttu-id="eda60-109">Próximo: [Etapa 4. Crie a página De propriedades](step-4--create-the-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="eda60-109">Next: [Step 4. Create the Property Page](step-4--create-the-property-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eda60-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eda60-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eda60-111">Criando uma página de propriedades de filtro</span><span class="sxs-lookup"><span data-stu-id="eda60-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> <dt>

[<span data-ttu-id="eda60-112">Como implementar IUnknown</span><span class="sxs-lookup"><span data-stu-id="eda60-112">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 



