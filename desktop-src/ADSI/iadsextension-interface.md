---
title: Interface IADsExtension
description: Este tópico contém exemplos de código C++ para usar a interface IADsExtension.
ms.assetid: fa94cc55-1ab2-4b6e-a3b6-8c20542adb42
ms.tgt_platform: multiple
keywords:
- IADsExtension ADSI, usando
- ADSI ADSI, código de exemplo C/C++, usando IADsExtension
- ADSI de extensões, IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c950b6d305cc4c90ed75ff0cc96b5f7f344e12
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641831"
---
# <a name="iadsextension-interface"></a><span data-ttu-id="378df-106">Interface IADsExtension</span><span class="sxs-lookup"><span data-stu-id="378df-106">IADsExtension Interface</span></span>

<span data-ttu-id="378df-107">A interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="378df-107">The [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface is defined as follows:</span></span>


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



<span data-ttu-id="378df-108">O agregador (ADSI) chama o método [**IADsExtension:: opere**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) .</span><span class="sxs-lookup"><span data-stu-id="378df-108">The aggregator (ADSI) calls the [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method.</span></span> <span data-ttu-id="378df-109">A extensão deve interpretar o parâmetro *dwCode* e cada parâmetro *varData* , de acordo com a documentação do provedor.</span><span class="sxs-lookup"><span data-stu-id="378df-109">The extension should interpret the *dwCode* parameter and each *varData* parameter, according to the provider's documentation.</span></span>

<span data-ttu-id="378df-110">O agregador (ADSI), chama o método [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) .</span><span class="sxs-lookup"><span data-stu-id="378df-110">The aggregator (ADSI), calls the [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) method.</span></span> <span data-ttu-id="378df-111">Ele é chamado depois que a ADSI determina a extensão para atender à expedição.</span><span class="sxs-lookup"><span data-stu-id="378df-111">It is called after ADSI determines the extension to service the dispatch.</span></span> <span data-ttu-id="378df-112">A extensão pode usar as informações de tipo para obter o DISPID, ou seja, usando a função [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) .</span><span class="sxs-lookup"><span data-stu-id="378df-112">The extension could use the type information for getting the DISPID, that is, using the [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) function.</span></span>

<span data-ttu-id="378df-113">O ADSI normalmente chama o método [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) depois de chamar a função [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) .</span><span class="sxs-lookup"><span data-stu-id="378df-113">ADSI normally calls the [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) method after calling the [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) function.</span></span> <span data-ttu-id="378df-114">A extensão deve chamar o método real que ele implementa.</span><span class="sxs-lookup"><span data-stu-id="378df-114">The extension should call the actual method that it implements.</span></span> <span data-ttu-id="378df-115">Como alternativa, a extensão pode usar informações de tipo e chamar a função de [**despinvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) .</span><span class="sxs-lookup"><span data-stu-id="378df-115">Alternatively, the extension can use type information and call the [**DispInvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) function.</span></span>

<span data-ttu-id="378df-116">Todos os parâmetros têm o mesmo significado que os parâmetros no método padrão [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .</span><span class="sxs-lookup"><span data-stu-id="378df-116">All parameters have the same meaning as the parameters in the standard [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) method.</span></span>

 

 