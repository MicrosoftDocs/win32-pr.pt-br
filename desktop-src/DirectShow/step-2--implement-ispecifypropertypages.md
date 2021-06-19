---
description: Implemente a interface ISpecifyPropertyPages em seu filtro como parte da criação de uma página de propriedades de filtro para um filtro personalizado do DirectShow.
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: Etapa 2. Implementar ISpecifyPropertyPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe37a22c6ba9c14f8656ac41294360569316be1a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410049"
---
# <a name="step-2-implement-ispecifypropertypages"></a>Etapa 2. Implementar ISpecifyPropertyPages

Em seguida, implemente a interface **ISpecifyPropertyPages** no filtro. Essa interface tem um único método, **GetPages,** que retorna uma matriz de CLSIDs para as páginas de propriedades às quais o filtro dá suporte. Neste exemplo, o filtro tem uma única página de propriedades. Comece gerando o CLSID e declarando-o no arquivo de header:


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



Agora, implemente **o método GetPages:**


```C++
class CGrayFilter : public ISaturation,
                    public ISpecifyPropertyPages, 
                    /* Other inherited classes. */
{
public:
    STDMETHODIMP GetPages(CAUUID *pPages)
    {
        if (pPages == NULL) return E_POINTER;
        pPages->cElems = 1;
        pPages->pElems = (GUID*)CoTaskMemAlloc(sizeof(GUID));
        if (pPages->pElems == NULL) 
        {
            return E_OUTOFMEMORY;
        }
        pPages->pElems[0] = CLSID_SaturationProp;
        return S_OK;
    }
};

/* ... */

}
```



Alocar memória para a matriz usando **CoTaskMemAlloc**. O chamador liberará a memória.

Próximo: [Etapa 3. Suporte a QueryInterface.](step-3--support-queryinterface.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma página de propriedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



