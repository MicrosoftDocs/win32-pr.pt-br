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
# <a name="iadsextension-interface"></a>Interface IADsExtension

A interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) é definida da seguinte maneira:


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



O agregador (ADSI) chama o método [**IADsExtension:: opere**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) . A extensão deve interpretar o parâmetro *dwCode* e cada parâmetro *varData* , de acordo com a documentação do provedor.

O agregador (ADSI), chama o método [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) . Ele é chamado depois que a ADSI determina a extensão para atender à expedição. A extensão pode usar as informações de tipo para obter o DISPID, ou seja, usando a função [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) .

O ADSI normalmente chama o método [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) depois de chamar a função [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) . A extensão deve chamar o método real que ele implementa. Como alternativa, a extensão pode usar informações de tipo e chamar a função de [**despinvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) .

Todos os parâmetros têm o mesmo significado que os parâmetros no método padrão [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .

 

 