---
description: O XAudio2 é inicializado para reprodução de áudio criando uma instância do mecanismo de XAudio2 e criando uma voz de mestre.
ms.assetid: 4db2e7fc-0a87-0344-a07c-3abf2b21af32
title: 'Como: Inicializar o XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a613c1ae2b7c3a7f0c55ab5349a0a605aaeb2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827305"
---
# <a name="how-to-initialize-xaudio2"></a>Como: Inicializar o XAudio2

O XAudio2 é inicializado para reprodução de áudio criando uma instância do mecanismo de XAudio2 e criando uma voz de mestre.

**Para inicializar o XAudio2**

1.  Verifique se você inicializou COM. Para um aplicativo da Windows Store, isso é feito como parte da inicialização da Windows Runtime. Caso contrário, use [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    ```
    HRESULT hr;
    hr = CoInitializeEx( nullptr, COINIT_MULTITHREADED );
    if (FAILED(hr))
        return hr;
    ```



2.  Use a função [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) para criar uma instância do mecanismo de XAudio2.

    ```
    IXAudio2* pXAudio2 = nullptr;
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  Use o método [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) para criar uma voz de mestre.

    As vozes de mestre encapsulam um dispositivo de áudio. É o destino final de todo o áudio que passa por um grafo de áudio.

    ```
    IXAudio2MasteringVoice* pMasterVoice = nullptr;
    if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Observações para aplicativos da Windows Store

É recomendável que você use um [ponteiro inteligente](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) para gerenciar o tempo de vida de objetos XAudio2 de forma segura de exceção. Para aplicativos da Windows Store, você pode usar o modelo de ponteiro inteligente [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) do WRL (Windows Runtime C++ Template Library).


```C++
Microsoft::WRL::ComPtr<IXAudio2> XAudio2;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &XAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    throw Platform::Exception::CreateException(hr);

IXAudio2MasteringVoice* pMasterVoice = nullptr;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
    return hr;
```



> [!Note]  
> Verifique se todos os objetos filho XAUDIO2 são totalmente liberados antes de liberar o objeto [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução XAudio2](getting-started.md)
</dt> <dt>

[Como: Carregar arquivos de dados de áudio no XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> <dt>

[Como: Reproduzir um som com o XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 
