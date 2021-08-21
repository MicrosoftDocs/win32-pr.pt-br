---
description: Etapa 10.
ms.assetid: 2959f574-1a39-4db1-9e4a-a303d0c7f8f3
title: Etapa 10. Suporte ao registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68efdeda754d5f7b728138a26a6bc9f4b782918f8c4b5140fd2457bcee6012f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652146"
---
# <a name="step-10-support-com-registration"></a>Etapa 10. Suporte ao registro COM

A última tarefa restante é oferecer suporte ao registro COM, para que o quadro de propriedades possa criar novas instâncias da sua página de propriedades. Adicione outra entrada [**CFactoryTemplate**](cfactorytemplate.md) à matriz de *\_ modelos g* globais, que é usada para registrar todos os objetos com em sua dll. Não inclua nenhuma informação de configuração de filtro para a página de propriedades.


```C++
const AMOVIESETUP_FILTER FilterSetupData = 
{ 
    /* Not shown ... */
};

CFactoryTemplate g_Templates[] =
{   
    // This entry is for the filter.
    {
        wszName,
        &CLSID_GrayFilter,
        CGrayFilter::CreateInstance,
        NULL,
        &FilterSetupData 
    },
    // This entry is for the property page.
    { 
        L"Saturation Props",
        &CLSID_SaturationProp,
        CGrayProp::CreateInstance, 
        NULL, NULL
    }
};
```



Se você declarar *g \_ cTemplates* conforme mostrado no código a seguir, ele automaticamente terá o valor correto com base no tamanho da matriz:


```C++
int g_cTemplates = sizeof(g_Templates)/sizeof(g_Templates[0]);
```



Além disso, adicione um `CreateInstance` método estático à classe de página de propriedades. Você pode nomear o método de qualquer forma que preferir, mas a assinatura deve corresponder à mostrada no exemplo a seguir:


```C++
static CUnknown * WINAPI CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CGrayProp *pNewObject = new CGrayProp(pUnk);
    if (pNewObject == NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 
```



Para testar a página de propriedades, registre a DLL e, em seguida, carregue o filtro em GraphEdit. Clique com o botão direito do mouse no filtro e selecione **Propriedades do filtro**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma página de propriedades de filtro](creating-a-filter-property-page.md)
</dt> <dt>

[como criar uma DLL de filtro de DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 



