---
title: Noções básicas do aplicativo
description: Noções básicas do aplicativo
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- SDK do Windows Media Format, noções básicas do aplicativo DRM
- DRM (gerenciamento de direitos digitais), noções básicas do aplicativo
- DRM (gerenciamento de direitos digitais), noções básicas do aplicativo
- DRM (gerenciamento de direitos digitais), função WMDRMStartup
- DRM (gerenciamento de direitos digitais), função WMDRMStartup
- WMDRMStartup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182a9e54e077c174c4f4cbe74ba392aa44ce5112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159364"
---
# <a name="application-basics"></a>Noções básicas do aplicativo

Há algum processamento extra que você deve executar para qualquer aplicativo que use as APIs estendidas do cliente DRM do Windows Media. Este tópico descreve os requisitos para um aplicativo simples.

Primeiro, você deve inicializar as APIs estendidas do cliente DRM do Windows Media chamando a função [**WMDRMStartup**](wmdrmstartup.md) . Os objetos do SDK são objetos COM, mas você não precisa chamar **CoIntialize**, pois a função **WMDRMStatup** inicializa com para você.

> [!Note]  
> O Windows Media Format SDK usa apenas um subconjunto de COM, portanto, se você usar objetos COM diferentes daqueles na API estendida do cliente DRM do Windows Media, ainda deverá chamar **CoInitialize**.

 

Todos os objetos das APIs estendidas do cliente DRM do Windows Media são criados usando funções e métodos auxiliares. Você nunca precisa chamar **CoCreateInstance** para criar um objeto. A primeira interface a ser instanciada para qualquer aplicativo que usa o SDK é [**IWMDRMProvider**](iwmdrmprovider.md), que você pode usar para instanciar todas as outras interfaces base. Para obter uma instância de **IWMDRMProvider**, você deve chamar [**WMDRMCreateProvider**](wmdrmcreateprovider.md) ou [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md). A diferença entre essas funções é que o **WMDRMCreateProvider** cria um objeto que, por sua vez, pode criar apenas objetos que não dão suporte a métodos que exigem a biblioteca de stub.

Depois de ter uma instância do **IWMDRMProvider**, você pode criar os outros objetos necessários chamando [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).

Quando estiver pronto para sair do aplicativo, você deverá liberar os recursos do subsistema DRM chamando a função [**WMDRMShutdown**](wmdrmshutdown.md) . Essa função também desliga o COM para você.

O exemplo de código a seguir demonstra como inicializar e concluir um aplicativo que usa as APIs estendidas do cliente DRM do Windows Media.


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

 

 




