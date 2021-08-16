---
description: Matriz de modelo de fábrica
ms.assetid: 310afccd-42a6-426e-b455-7bf98062bf36
title: Matriz de modelo de fábrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1888a2a054473865c713d96cdfa5706c35229dc938f23513a95066176ab138c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401841"
---
# <a name="factory-template-array"></a>Matriz de modelo de fábrica

O modelo de fábrica contém as seguintes variáveis de membro público:

``` syntax
const WCHAR *              m_Name;                // Name
const CLSID *              m_ClsID;               // CLSID
LPFNNewCOMObject           m_lpfnNew;             // Function to create an instance
                                                  //   of the component
LPFNInitRoutine            m_lpfnInit;            // Initialization function (optional)
const AMOVIESETUP_FILTER * m_pAMovieSetup_Filter; // Set-up information (for filters)
```

Os dois ponteiros de função, [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) e [**m \_ lpfnInit,**](cfactorytemplate-m-lpfninit.md)usam as seguintes definições de tipo:

``` syntax
typedef CUnknown *(CALLBACK *LPFNNewCOMObject)(LPUNKNOWN pUnkOuter, HRESULT *phr);
typedef void (CALLBACK *LPFNInitRoutine)(BOOL bLoading, const CLSID *rclsid);
```

A primeira é a função de instalização para o componente. O segundo é uma função de inicialização opcional. Se você fornecer uma função de inicialização, ela será chamada de dentro da função de ponto de entrada da DLL. (A função de ponto de entrada da DLL é discutida posteriormente neste artigo.)

Suponha que você está criando uma DLL que contém um componente chamado CMyComponent, que herda de [**CUnknown**](cunknown.md). Você deve fornecer os seguintes itens em sua DLL:

-   A função de inicialização, um método público que retorna uma nova instância de CMyComponent.
-   Uma matriz global de modelos de fábrica, chamada *g \_ Templates.* Essa matriz contém o modelo de fábrica para CMyComponent.
-   Uma variável global chamada *g \_ cTemplates* que especifica o tamanho da matriz.

O exemplo a seguir mostra como declarar estes itens:


```C++
// Public method that returns a new instance. 
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = new CMyComponent(NAME("My Component"), pUnk, pHr );
    if (pNewObject == NULL) {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 

CFactoryTemplate g_Templates[1] = 
{
    { 
      L"My Component",                // Name
      &CLSID_MyComponent,             // CLSID
      CMyComponent::CreateInstance,   // Method to create an instance of MyComponent
      NULL,                           // Initialization function
      NULL                            // Set-up information (for filters)
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);    
```



O `CreateInstance` método chama o construtor de classe e retorna um ponteiro para a nova instância de classe. O parâmetro *pUnk* é um ponteiro para o [**IUnknown agregador.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) Você pode simplesmente passar esse parâmetro para o construtor de classe. O parâmetro *pHr* é um ponteiro para um valor HRESULT. O construtor de classe define isso como um valor apropriado, mas se o construtor falhar, de definir o valor como E \_ OUTOFMEMORY.

A [**macro NAME**](name.md) gera uma cadeia de caracteres em builds de depuração, mas é resolvida como **NULL** em builds de varejo. Ele é usado neste exemplo para dar ao componente um nome que aparece nos logs de depuração, mas não ocupa memória na versão final.

O `CreateInstance` método pode ter qualquer nome, porque a fábrica de classe refere-se ao ponteiro de função no modelo de fábrica. No entanto, *g \_ Templates* e *g \_ cTemplates* são variáveis globais que a fábrica de classes espera encontrar, portanto, eles devem ter exatamente esses nomes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como criar uma DLL DirectShow filtro de dados](how-to-create-a-dll.md)
</dt> </dl>

 

 
