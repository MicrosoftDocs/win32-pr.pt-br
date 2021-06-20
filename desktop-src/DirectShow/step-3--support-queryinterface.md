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
# <a name="step-3-support-queryinterface"></a>Etapa 3. Suporte a QueryInterface

Para expor as novas interfaces do filtro aos clientes, faça o seguinte:

-   Inclua a [**macro DECLARE \_ IUNKNOWN**](declare-iunknown.md) na seção de declaração pública do filtro:
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   Substitua [**CUnknown::NonDeltingQueryInterface**](cunknown-nondelegatingqueryinterface.md) para verificar os IIDs das duas interfaces:
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

    

Próximo: [Etapa 4. Crie a página De propriedades](step-4--create-the-property-page.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma página de propriedades de filtro](creating-a-filter-property-page.md)
</dt> <dt>

[Como implementar IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



