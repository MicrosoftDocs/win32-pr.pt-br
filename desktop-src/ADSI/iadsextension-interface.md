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
# <a name="iadsextension-interface"></a>IADsExtension Interface

A [**interface IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) é definida da seguinte forma:


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



O agregador (ADSI) chama o [**método IADsExtension::Operate.**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) A extensão deve interpretar o *parâmetro dwCode* e cada *parâmetro varData,* de acordo com a documentação do provedor.

O agregador (ADSI), chama o [**método IADsExtension::P rivateGetIDsOfNames.**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) Ele é chamado depois que a ADSI determina a extensão para a expedição de serviço. A extensão pode usar as informações de tipo para obter a DISPID, ou seja, usando a [**função DispGetIDsOfNames.**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames)

ADSI normalmente chama o [**método PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) depois de chamar a [**função PrivateGetIDsOfNames.**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) A extensão deve chamar o método real que ela implementa. Como alternativa, a extensão pode usar informações de tipo e chamar a [**função DispInvoke.**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke)

Todos os parâmetros têm o mesmo significado que os parâmetros no método [**padrão IDispatch::Invoke.**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke)

 

 