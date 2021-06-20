---
description: Defina um mecanismo para definir a propriedade como parte da criação de uma página de propriedades de filtro para um filtro DirectShow personalizado.
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: Etapa 1. Definir um mecanismo para definir a propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 191014c35e27974c52961c2c6218e3a83effcc99
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410069"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a><span data-ttu-id="a00ec-104">Etapa 1.</span><span class="sxs-lookup"><span data-stu-id="a00ec-104">Step 1.</span></span> <span data-ttu-id="a00ec-105">Definir um mecanismo para definir a propriedade</span><span class="sxs-lookup"><span data-stu-id="a00ec-105">Define a Mechanism for Setting the Property</span></span>

<span data-ttu-id="a00ec-106">O filtro deve dar suporte a uma maneira de a página de propriedades se comunicar com ele, para que a página de propriedades possa definir e recuperar propriedades no filtro.</span><span class="sxs-lookup"><span data-stu-id="a00ec-106">The filter must support a way for the property page to communicate with it, so that the property page can set and retrieve properties on the filter.</span></span> <span data-ttu-id="a00ec-107">Os mecanismos possíveis incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a00ec-107">Possible mechanisms include the following:</span></span>

-   <span data-ttu-id="a00ec-108">Expor uma interface COM personalizada.</span><span class="sxs-lookup"><span data-stu-id="a00ec-108">Expose a custom COM interface.</span></span>
-   <span data-ttu-id="a00ec-109">Suporte a propriedades de Automação, por **meio de IDispatch.**</span><span class="sxs-lookup"><span data-stu-id="a00ec-109">Support Automation properties, through **IDispatch**.</span></span>
-   <span data-ttu-id="a00ec-110">Exponha a interface **IPropertyBag** e defina um conjunto de propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="a00ec-110">Expose the **IPropertyBag** interface and define a set of named properties.</span></span>

<span data-ttu-id="a00ec-111">Este exemplo usa uma interface COM personalizada, chamada IS saturação.</span><span class="sxs-lookup"><span data-stu-id="a00ec-111">This example uses a custom COM interface, named ISaturation.</span></span> <span data-ttu-id="a00ec-112">Essa não é uma interface real do DirectShow; ele é definido somente para este exemplo.</span><span class="sxs-lookup"><span data-stu-id="a00ec-112">This is not an actual DirectShow interface; it is defined only for this example.</span></span> <span data-ttu-id="a00ec-113">Comece declarando a interface em um arquivo de header, juntamente com o IID (identificador de interface):</span><span class="sxs-lookup"><span data-stu-id="a00ec-113">Start by declaring the interface in a header file, along with the interface identifier (IID):</span></span>


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(IID_ISaturation, 0x19412d6e, 0x6401, 
0x475c, 0xb0, 0x48, 0x7a, 0xd2, 0x96, 0xe1, 0x6a, 0x19);

interface ISaturation : public IUnknown
{
    STDMETHOD(GetSaturation)(long *plSat) = 0;
    STDMETHOD(SetSaturation)(long lSat) = 0;
};
```



<span data-ttu-id="a00ec-114">Você também pode definir a interface com IDL e usar o compilador MIDL para criar o arquivo de header.</span><span class="sxs-lookup"><span data-stu-id="a00ec-114">You can also define the interface with IDL and use the MIDL compiler to create the header file.</span></span> <span data-ttu-id="a00ec-115">Em seguida, implemente a interface personalizada no filtro.</span><span class="sxs-lookup"><span data-stu-id="a00ec-115">Next, implement the custom interface in the filter.</span></span> <span data-ttu-id="a00ec-116">Este exemplo usa os métodos "Get" e "Set" para o valor de saturação do filtro.</span><span class="sxs-lookup"><span data-stu-id="a00ec-116">This example uses "Get" and "Set" methods for the filter's saturation value.</span></span> <span data-ttu-id="a00ec-117">Observe que ambos os métodos protegem o membro m \_ lSaturation com uma seção crítica.</span><span class="sxs-lookup"><span data-stu-id="a00ec-117">Notice that both methods protect the m\_lSaturation member with a critical section.</span></span>


```C++
class CGrayFilter : public ISaturation, /* Other inherited classes. */
{
private:
    CCritSec  m_csShared;    // Protects shared data.
    long      m_lSaturation; // Saturation level.
public:
    STDMETHODIMP GetSaturation(long *plSat)
    {
        if (!plSat) return E_POINTER;
        CAutoLock lock(&m_csShared);
        *plSat = m_lSaturation;
        return S_OK;
    }
    STDMETHODIMP SetSaturation(long lSat)
    {
        CAutoLock lock(&m_csShared);
        if (lSat < SATURATION_MIN || lSat > SATURATION_MAX)
        {
            return E_INVALIDARG;
        }
        m_lSaturation = lSat;
        return S_OK;
    }
};
```



<span data-ttu-id="a00ec-118">É claro que os detalhes de sua própria implementação serão diferentes do exemplo mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="a00ec-118">Of course, the details of your own implementation will differ from the example shown here.</span></span>

<span data-ttu-id="a00ec-119">Próximo: [Etapa 2. Implemente ISpecifyPropertyPages.](step-2--implement-ispecifypropertypages.md)</span><span class="sxs-lookup"><span data-stu-id="a00ec-119">Next: [Step 2. Implement ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a00ec-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a00ec-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a00ec-121">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="a00ec-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> <dt>

[<span data-ttu-id="a00ec-122">Criando uma página de propriedades de filtro</span><span class="sxs-lookup"><span data-stu-id="a00ec-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



