---
description: Usando o Windows Media com os serviços de edição do DirectShow
ms.assetid: 26a88197-ec80-4443-9d50-e11df40dd1eb
title: Usando o Windows Media com os serviços de edição do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbfe715495834217b695f887305f1ecb21cb6f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105789676"
---
# <a name="using-windows-media-with-directshow-editing-services"></a>Usando o Windows Media com os serviços de edição do DirectShow

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Esta seção descreve como usar o conteúdo baseado no Windows Media em um aplicativo de [serviços de edição do DirectShow](directshow-editing-services.md) (des). Há dois cenários principais:

-   Clipes de origem. Um projeto DES pode conter clipes de áudio e vídeo de arquivos de mídia do Windows.
-   Formato de destino. O Windows Media é um formato ideal para a saída final de um projeto de edição de vídeo.

Para trabalhar com arquivos de mídia do Windows, o aplicativo deve fornecer um certificado de software, também chamado de chave. Ele faz isso implementando um objeto de provedor de chave. O provedor de chave é um objeto COM que expõe a interface **IServiceProvider** . Para obter informações sobre como implementar o provedor de chaves, consulte [desbloqueando o SDK do Windows Media Format](unlocking-the-windows-media-format-sdk.md).

Para usar DES com arquivos de mídia do Windows, os seguintes objetos DES requerem a chave de software:

-   O mecanismo de renderização, para visualização ou gravação de arquivo.
-   O objeto MediaDet, para obter quadros de vídeo ou tipos de mídia de arquivos ASF.
-   \[! Fundamental\]  
    > Não use o mecanismo de processamento inteligente para ler ou gravar arquivos de mídia do Windows. Sempre use o mecanismo de processamento básico (CLSID \_ RenderEngine).

     

Para dar a um objeto a chave de software, consulte esse objeto para a interface **IObjectWithSite** e chame **IObjectWithSite:: SetSite** com um ponteiro para o provedor de chave. Por exemplo, o código a seguir fornece a chave de software para o mecanismo de renderização:


```C++
// Create your key provider, using an application-defined function:
IServiceProvider *pKey;
hr = MyCreateKeyProviderFunction(&pKey);  

// Query the Render Engine for IObjectWithSite.
IObjectWithSite *pOWS;
hr = pRenderEngine->QueryInterface(__uuidof(IObjectWithSite), 
    reinterpret_cast<void**>(&pOWS));
if (SUCCEEDED(hr))
{
    // Give it your key provider.
    hr = pOWS->SetSite(pKey);
    pOWS->Release();
}
pKey->Release();
```



Para usar os clipes de origem do Windows Media em um projeto DES, basta chamar **IObjectWithSite:: SetSite** no mecanismo de renderização com um ponteiro para o provedor de chave.

Para obter informações sobre como gravar arquivos de mídia do Windows, consulte [gravando um arquivo de mídia do Windows em des](writing-a-windows-media-file-in-des.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando os serviços de edição do DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



