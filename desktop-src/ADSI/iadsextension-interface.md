---
title: IADsExtension Interface
description: Este artigo contém a definição de código C++ da interface IADsExtension e a discussão de seus métodos.
ms.assetid: fa94cc55-1ab2-4b6e-a3b6-8c20542adb42
ms.tgt_platform: multiple
keywords:
- IADsExtension ADSI, usando
- ADSI ADSI, código de exemplo C/C++, usando IADsExtension
- extensões ADSI, IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7d59048d29620cdc2d3703b9ba26a852441a47
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405939"
---
# <a name="iadsextension-interface"></a><span data-ttu-id="c01b3-106">IADsExtension Interface</span><span class="sxs-lookup"><span data-stu-id="c01b3-106">IADsExtension Interface</span></span>

<span data-ttu-id="c01b3-107">A [**interface IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) é definida da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="c01b3-107">The [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface is defined as follows:</span></span>


```C++
IADsExtension : public IUnknown
    {
    public:
        virtual HRESULT STDMETHODCALLTYPE Operate( 
            /* [in] */ DWORD dwCode,
            /* [in] */ VARIANT varData1,
            /* [in] */ VARIANT varData2,
            /* [in] */ VARIANT varData3) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateGetIDsOfNames( 
            /* [in] */ REFIID riid,
            /* [in] */ OLECHAR **rgszNames,
            /* [in] */ unsigned int cNames,
            /* [in] */ LCID lcid,
            /* [out] */ DISPID *rgDispid) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateInvoke( 
            /* [in] */ DISPID dispidMember,
            /* [in] */ REFIID riid,
            /* [in] */ LCID lcid,
            /* [in] */ WORD wFlags,
            /* [in] */ DISPPARAMS *pdispparams,
            /* [out] */ VARIANT *pvarResult,
            /* [out] */ EXCEPINFO *pexcepinfo,
            /* [out] */ unsigned int *puArgErr) = 0;
    };
```



<span data-ttu-id="c01b3-108">O agregador (ADSI) chama o [**método IADsExtension::Operate.**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate)</span><span class="sxs-lookup"><span data-stu-id="c01b3-108">The aggregator (ADSI) calls the [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method.</span></span> <span data-ttu-id="c01b3-109">A extensão deve interpretar o *parâmetro dwCode* e cada *parâmetro varData,* de acordo com a documentação do provedor.</span><span class="sxs-lookup"><span data-stu-id="c01b3-109">The extension should interpret the *dwCode* parameter and each *varData* parameter, according to the provider's documentation.</span></span>

<span data-ttu-id="c01b3-110">O agregador (ADSI), chama o [**método IADsExtension::P rivateGetIDsOfNames.**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames)</span><span class="sxs-lookup"><span data-stu-id="c01b3-110">The aggregator (ADSI), calls the [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) method.</span></span> <span data-ttu-id="c01b3-111">Ele é chamado depois que a ADSI determina a extensão para a expedição de serviço.</span><span class="sxs-lookup"><span data-stu-id="c01b3-111">It is called after ADSI determines the extension to service the dispatch.</span></span> <span data-ttu-id="c01b3-112">A extensão pode usar as informações de tipo para obter a DISPID, ou seja, usando a [**função DispGetIDsOfNames.**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames)</span><span class="sxs-lookup"><span data-stu-id="c01b3-112">The extension could use the type information for getting the DISPID, that is, using the [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) function.</span></span>

<span data-ttu-id="c01b3-113">ADSI normalmente chama o [**método PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) depois de chamar a [**função PrivateGetIDsOfNames.**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames)</span><span class="sxs-lookup"><span data-stu-id="c01b3-113">ADSI normally calls the [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) method after calling the [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) function.</span></span> <span data-ttu-id="c01b3-114">A extensão deve chamar o método real que ela implementa.</span><span class="sxs-lookup"><span data-stu-id="c01b3-114">The extension should call the actual method that it implements.</span></span> <span data-ttu-id="c01b3-115">Como alternativa, a extensão pode usar informações de tipo e chamar a [**função DispInvoke.**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke)</span><span class="sxs-lookup"><span data-stu-id="c01b3-115">Alternatively, the extension can use type information and call the [**DispInvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) function.</span></span>

<span data-ttu-id="c01b3-116">Todos os parâmetros têm o mesmo significado que os parâmetros no método [**padrão IDispatch::Invoke.**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke)</span><span class="sxs-lookup"><span data-stu-id="c01b3-116">All parameters have the same meaning as the parameters in the standard [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) method.</span></span>

 

 