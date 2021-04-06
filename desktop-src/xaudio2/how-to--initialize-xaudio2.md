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
# <a name="how-to-initialize-xaudio2"></a><span data-ttu-id="25538-103">Como: Inicializar o XAudio2</span><span class="sxs-lookup"><span data-stu-id="25538-103">How to: Initialize XAudio2</span></span>

<span data-ttu-id="25538-104">O XAudio2 é inicializado para reprodução de áudio criando uma instância do mecanismo de XAudio2 e criando uma voz de mestre.</span><span class="sxs-lookup"><span data-stu-id="25538-104">XAudio2 is initialized for audio playback by creating an instance of the XAudio2 engine, and creating a mastering voice.</span></span>

<span data-ttu-id="25538-105">**Para inicializar o XAudio2**</span><span class="sxs-lookup"><span data-stu-id="25538-105">**To initialize XAudio2**</span></span>

1.  <span data-ttu-id="25538-106">Verifique se você inicializou COM.</span><span class="sxs-lookup"><span data-stu-id="25538-106">Make sure you have initialized COM.</span></span> <span data-ttu-id="25538-107">Para um aplicativo da Windows Store, isso é feito como parte da inicialização da Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="25538-107">For a Windows Store app, this is done as part of initializing the Windows Runtime.</span></span> <span data-ttu-id="25538-108">Caso contrário, use [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="25538-108">Otherwise, use [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    ```
    HRESULT hr;
    hr = CoInitializeEx( nullptr, COINIT_MULTITHREADED );
    if (FAILED(hr))
        return hr;
    ```



2.  <span data-ttu-id="25538-109">Use a função [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) para criar uma instância do mecanismo de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="25538-109">Use the [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) function to create an instance of the XAudio2 engine.</span></span>

    ```
    IXAudio2* pXAudio2 = nullptr;
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  <span data-ttu-id="25538-110">Use o método [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) para criar uma voz de mestre.</span><span class="sxs-lookup"><span data-stu-id="25538-110">Use the [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) method to create a mastering voice.</span></span>

    <span data-ttu-id="25538-111">As vozes de mestre encapsulam um dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="25538-111">The mastering voices encapsulates an audio device.</span></span> <span data-ttu-id="25538-112">É o destino final de todo o áudio que passa por um grafo de áudio.</span><span class="sxs-lookup"><span data-stu-id="25538-112">It is the ultimate destination for all audio that passes through an audio graph.</span></span>

    ```
    IXAudio2MasteringVoice* pMasterVoice = nullptr;
    if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a><span data-ttu-id="25538-113">Observações para aplicativos da Windows Store</span><span class="sxs-lookup"><span data-stu-id="25538-113">Notes for Windows Store apps</span></span>

<span data-ttu-id="25538-114">É recomendável que você use um [ponteiro inteligente](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) para gerenciar o tempo de vida de objetos XAudio2 de forma segura de exceção.</span><span class="sxs-lookup"><span data-stu-id="25538-114">We recommend that you make use of a [smart pointer](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) to manage the lifetime of XAUDIO2 objects in an exception safe manner.</span></span> <span data-ttu-id="25538-115">Para aplicativos da Windows Store, você pode usar o modelo de ponteiro inteligente [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) do WRL (Windows Runtime C++ Template Library).</span><span class="sxs-lookup"><span data-stu-id="25538-115">For Windows Store apps, you can use the [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) smart pointer template from the Windows Runtime C++ Template Library (WRL).</span></span>


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
> <span data-ttu-id="25538-116">Verifique se todos os objetos filho XAUDIO2 são totalmente liberados antes de liberar o objeto [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .</span><span class="sxs-lookup"><span data-stu-id="25538-116">Ensure that all XAUDIO2 child objects are fully released before you release the [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="25538-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="25538-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25538-118">Introdução XAudio2</span><span class="sxs-lookup"><span data-stu-id="25538-118">XAudio2 Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="25538-119">Como: Carregar arquivos de dados de áudio no XAudio2</span><span class="sxs-lookup"><span data-stu-id="25538-119">How to: Load Audio Data Files in XAudio2</span></span>](how-to--load-audio-data-files-in-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="25538-120">Como: Reproduzir um som com o XAudio2</span><span class="sxs-lookup"><span data-stu-id="25538-120">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 
