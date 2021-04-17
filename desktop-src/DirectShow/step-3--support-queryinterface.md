---
description: Etapa 3.
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: Etapa 3. Suporte a QueryInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e3d44b67971e165b8586aa3a02cc65ab3ab05f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760876"
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

 

 



