---
title: Noções básicas do aplicativo
description: Noções básicas do aplicativo
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- Windows SDK do formato de mídia, noções básicas do aplicativo DRM
- DRM (gerenciamento de direitos digitais), noções básicas do aplicativo
- DRM (gerenciamento de direitos digitais), noções básicas do aplicativo
- DRM (gerenciamento de direitos digitais), função WMDRMStartup
- DRM (gerenciamento de direitos digitais), função WMDRMStartup
- WMDRMStartup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8356160565754764ac71cb152799a0fd9d1530e6e6969dc7a56e203b7504645d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086202"
---
# <a name="application-basics"></a>Noções básicas do aplicativo

há algum processamento extra que você deve executar para qualquer aplicativo que use as APIs estendidas do cliente DRM de mídia Windows. Este tópico descreve os requisitos para um aplicativo simples.

primeiro, você deve inicializar as APIs estendidas do cliente DRM do Windows de mídia chamando a função [**WMDRMStartup**](wmdrmstartup.md) . Os objetos do SDK são objetos COM, mas você não precisa chamar **CoIntialize**, pois a função **WMDRMStatup** inicializa com para você.

> [!Note]  
> o SDK do formato de mídia Windows usa apenas um subconjunto de COM, portanto, se você usar objetos COM diferentes daqueles na API estendida do cliente do DRM Windows mídia, ainda deverá chamar **coinitialize**.

 

todos os objetos das APIs estendidas do cliente DRM de mídia Windows são criados usando funções e métodos auxiliares. Você nunca precisa chamar **CoCreateInstance** para criar um objeto. A primeira interface a ser instanciada para qualquer aplicativo que usa o SDK é [**IWMDRMProvider**](iwmdrmprovider.md), que você pode usar para instanciar todas as outras interfaces base. Para obter uma instância de **IWMDRMProvider**, você deve chamar [**WMDRMCreateProvider**](wmdrmcreateprovider.md) ou [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md). A diferença entre essas funções é que o **WMDRMCreateProvider** cria um objeto que, por sua vez, pode criar apenas objetos que não dão suporte a métodos que exigem a biblioteca de stub.

Depois de ter uma instância do **IWMDRMProvider**, você pode criar os outros objetos necessários chamando [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).

Quando estiver pronto para sair do aplicativo, você deverá liberar os recursos do subsistema DRM chamando a função [**WMDRMShutdown**](wmdrmshutdown.md) . Essa função também desliga o COM para você.

o exemplo de código a seguir demonstra como inicializar e concluir um aplicativo que usa as APIs estendidas do cliente de DRM de mídia Windows.


```C++
#include <wmdrmsdk.h>
// TODO: Include other headers here as needed.

// This example demonstrates the code required in a single, simple
// main function. You will most likely break this code up into appropriate
// functions.
void main(void)
{
    HRESULT hr = S_OK;

    IWMDRMProvider*     pProvider     = NULL;
    // For the sake of example, this code will instantiate the
    //  IWMDRMLicenseQuery interface. The process is the same for the
    //  other base interfaces.
    IWMDRMLicenseQuery* pLicenseQuery = NULL;

    // Initialize the DRM subsystem.
    hr = WMDRMStartup();

    // Create a provider object, that can be used to create the other
    //  objects.
    if (SUCCEEDED(hr))
    {
        hr = WMDRMCreateProvider(&pProvider);
    }

    if(SUCCEEDED(hr))
    {
        hr = pProvider->CreateObject(
            IID_IWMDRMLicenseQuery, 
            (void**)&pLicenseQuery);
    }

    // TODO: Use the methods of IWMDRMLicenseQuery as required.

    // Cleanup and shutdown.
    SAFE_RELEASE(pLicenseQuery);
    SAFE_RELEASE(pProvider);

    hr = WMDRMShutdown();
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Introdução**](drm-getting-started.md)
</dt> </dl>

 

 




