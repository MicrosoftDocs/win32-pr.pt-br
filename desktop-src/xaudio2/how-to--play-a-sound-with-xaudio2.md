---
description: Este tópico descreve as etapas mínimas necessárias para reproduzir dados de áudio carregados anteriormente no XAudio2.
ms.assetid: 5172b31c-d2af-45aa-5bd4-b62502f3c047
title: 'Como: Reproduzir um som com o XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ee2636ae9b6513dba9a479d63e0fd14be2c198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501932"
---
# <a name="how-to-play-a-sound-with-xaudio2"></a><span data-ttu-id="f20d8-103">Como: Reproduzir um som com o XAudio2</span><span class="sxs-lookup"><span data-stu-id="f20d8-103">How to: Play a Sound with XAudio2</span></span>

<span data-ttu-id="f20d8-104">Este tópico descreve as etapas mínimas necessárias para reproduzir dados de áudio carregados anteriormente no XAudio2.</span><span class="sxs-lookup"><span data-stu-id="f20d8-104">This topic describes the minimum steps required to play previously-loaded audio data in XAudio2.</span></span> <span data-ttu-id="f20d8-105">Depois de inicializar o XAudio2 (consulte [como: inicializar o XAudio2](how-to--initialize-xaudio2.md)) e carregar os dados de áudio (consulte Como: [carregar arquivos de dados de áudio no XAudio2](how-to--load-audio-data-files-in-xaudio2.md)), você pode tocar um som criando uma voz de origem e passando dados de áudio para ela.</span><span class="sxs-lookup"><span data-stu-id="f20d8-105">After you initialize XAudio2 (see [How to: Initialize XAudio2](how-to--initialize-xaudio2.md)) and load the audio data (see How to: [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)), you can play a sound by creating a source voice and passing audio data to it.</span></span>

## <a name="to-play-a-sound"></a><span data-ttu-id="f20d8-106">Para tocar um som</span><span class="sxs-lookup"><span data-stu-id="f20d8-106">To play a sound</span></span>

1.  <span data-ttu-id="f20d8-107">Inicialize o mecanismo XAudio2 seguindo as etapas descritas em [como: inicializar o XAudio2](how-to--initialize-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="f20d8-107">Initialize the XAudio2 engine by following the steps described in [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>
2.  <span data-ttu-id="f20d8-108">Preencha uma estrutura de [**\_ buffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) e XAudio2 seguindo as etapas descritas em [como carregar arquivos de dados de áudio no XAudio2](how-to--load-audio-data-files-in-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="f20d8-108">Populate a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure by following the steps described in [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="f20d8-109">Dependendo do formato dos dados de áudio, talvez seja necessário usar uma estrutura de dados maior que contenha uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) no lugar de um **WAVEFORMATEX**.</span><span class="sxs-lookup"><span data-stu-id="f20d8-109">Depending on the format of the audio data, you may need to use a larger data structure containing a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) structure in place of a **WAVEFORMATEX**.</span></span> <span data-ttu-id="f20d8-110">Consulte a página de referência do **WAVEFORMATEX** para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="f20d8-110">See the **WAVEFORMATEX** reference page for more information.</span></span>

     

3.  <span data-ttu-id="f20d8-111">Crie uma voz de origem chamando o método [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) em uma instância do mecanismo de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="f20d8-111">Create a source voice by calling the [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) method on an instance of the XAudio2 engine.</span></span> <span data-ttu-id="f20d8-112">O formato da voz é especificado pelos valores definidos em uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) .</span><span class="sxs-lookup"><span data-stu-id="f20d8-112">The format of the voice is specified by the values set in a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) structure.</span></span>
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  <span data-ttu-id="f20d8-113">Envie um [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) para a voz de origem usando a função [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).</span><span class="sxs-lookup"><span data-stu-id="f20d8-113">Submit an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) to the source voice using the function [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).</span></span>
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > <span data-ttu-id="f20d8-114">Os dados de exemplo de áudio para os quais os pontos de *buffer* ainda são "possuídos" pelo aplicativo e devem permanecer alocados e acessíveis até que o som pare de ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="f20d8-114">The audio sample data to which *buffer* points is still 'owned' by the app and must remain allocated and accessible until the sound stops playing.</span></span>

     

5.  <span data-ttu-id="f20d8-115">Use a função [**Iniciar**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) para iniciar a voz de origem.</span><span class="sxs-lookup"><span data-stu-id="f20d8-115">Use the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function to start the source voice.</span></span> <span data-ttu-id="f20d8-116">Como todas as vozes XAudio2 enviam sua saída para a voz de mestre por padrão, o áudio da voz de origem automaticamente faz seu caminho para o dispositivo de áudio selecionado na inicialização.</span><span class="sxs-lookup"><span data-stu-id="f20d8-116">Since all XAudio2 voices send their output to the mastering voice by default, audio from the source voice automatically makes its way to the audio device selected at initialization.</span></span> <span data-ttu-id="f20d8-117">Em um grafo de áudio mais complicado, a voz de origem precisaria especificar a voz à qual a saída deve ser enviada.</span><span class="sxs-lookup"><span data-stu-id="f20d8-117">In a more complicated audio graph, the source voice would have to specify the voice to which its output should be sent.</span></span>
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a><span data-ttu-id="f20d8-118">Observações para aplicativos da Windows Store</span><span class="sxs-lookup"><span data-stu-id="f20d8-118">Notes for Windows Store apps</span></span>

<span data-ttu-id="f20d8-119">É recomendável que você use um [ponteiro inteligente](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) para gerenciar o tempo de vida de objetos XAudio2 de forma segura de exceção.</span><span class="sxs-lookup"><span data-stu-id="f20d8-119">We recommend that you make use of a [smart pointer](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) to manage the lifetime of XAUDIO2 objects in an exception safe manner.</span></span> <span data-ttu-id="f20d8-120">Para aplicativos da Windows Store, você pode usar o modelo de ponteiro inteligente [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) do WRL (Windows Runtime C++ Template Library).</span><span class="sxs-lookup"><span data-stu-id="f20d8-120">For Windows Store apps, you can use the [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) smart pointer template from the Windows Runtime C++ Template Library (WRL).</span></span>


```
Microsoft::WRL::ComPtr<IXAudio2SourceVoice> SourceVoice;
HRESULT hr;
if( FAILED(hr = pXAudio2->CreateSourceVoice( &SourceVoice, (WAVEFORMATEX*)&wfx ) ) )
    throw Platform::Exception::CreateException(hr); 

if( FAILED(hr = SourceVoice->SubmitSourceBuffer( &buffer ) ) )
    throw Platform::Exception::CreateException(hr); 

if ( FAILED(hr = SourceVoice->Start( 0 ) ) )
    throw Platform::Exception::CreateException(hr);
```



> [!Note]  
> <span data-ttu-id="f20d8-121">Verifique se todos os ponteiros inteligentes para objetos XAUDIO2 são totalmente liberados antes de liberar o objeto [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .</span><span class="sxs-lookup"><span data-stu-id="f20d8-121">Ensure that all smart pointers to XAUDIO2 objects are fully released before you release the [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f20d8-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f20d8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f20d8-123">Introdução XAudio2</span><span class="sxs-lookup"><span data-stu-id="f20d8-123">XAudio2 Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="f20d8-124">Como: Inicializar o XAudio2</span><span class="sxs-lookup"><span data-stu-id="f20d8-124">How to: Initialize XAudio2</span></span>](how-to--initialize-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="f20d8-125">Como: Carregar arquivos de dados de áudio no XAudio2</span><span class="sxs-lookup"><span data-stu-id="f20d8-125">How to: Load Audio Data Files in XAudio2</span></span>](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 
