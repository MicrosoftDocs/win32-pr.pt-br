---
description: Declarando o modelo de fábrica
ms.assetid: 3060c167-ea23-4061-b32a-16e750f55e6f
title: Declarando o modelo de fábrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3168f16b6281417846f13b7a17141282053c4705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087330"
---
# <a name="declaring-the-factory-template"></a>Declarando o modelo de fábrica

A próxima etapa é declarar o modelo de fábrica para seu filtro. Um modelo de fábrica é uma classe C++ que contém informações para a fábrica de classes. Em sua DLL, declare uma matriz global de objetos [**CFactoryTemplate**](cfactorytemplate.md) , uma para cada filtro ou componente com em sua dll. A matriz deve ser nomeada *para \_ modelos g*. Para obter mais informações sobre modelos de fábrica, consulte [como criar uma DLL de filtro do DirectShow](how-to-create-a-dll.md).

O membro de **\_ \_ filtro m pAMovieSetup** do modelo de fábrica é um ponteiro para a estrutura de [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) descrita anteriormente. O exemplo a seguir mostra um modelo de fábrica, usando a estrutura fornecida no exemplo anterior:


```C++
CFactoryTemplate g_Templates[] = {
    {
        g_wszName,                      // Name.
        &CLSID_SomeFilter,              // CLSID.
        CSomeFilter::CreateInstance,    // Creation function.
        NULL,
        &sudFilterReg                   // Pointer to filter information.
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);
```



Se você não declarou nenhuma informação de filtro, **o \_ \_ filtro m PAMoveSetup** pode ser **nulo**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como registrar filtros do DirectShow](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



