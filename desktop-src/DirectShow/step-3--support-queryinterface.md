---
description: expor as novas interfaces de um filtro para os clientes como parte da criação de uma página de propriedades de filtro para um filtro de DirectShow personalizado.
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: Etapa 3. Suporte a QueryInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0761a0ecf57bc7769cf40623c6929655a9f757b66b35bb506167d4263a7e02a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072450"
---
# <a name="step-3-support-queryinterface"></a>Etapa 3. Suporte a QueryInterface

Para expor as novas interfaces do filtro aos clientes, faça o seguinte:

-   Inclua a macro [**Declare \_ IUnknown**](declare-iunknown.md) na seção de declaração pública do seu filtro:
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   Substitua [**CUnknown:: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) para verificar a IIDs das duas interfaces:
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

    

Em seguida: [etapa 4. Crie a página de propriedades](step-4--create-the-property-page.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma página de propriedades de filtro](creating-a-filter-property-page.md)
</dt> <dt>

[Como implementar IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



