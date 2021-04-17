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
# <a name="how-to-play-a-sound-with-xaudio2"></a>Como: Reproduzir um som com o XAudio2

Este tópico descreve as etapas mínimas necessárias para reproduzir dados de áudio carregados anteriormente no XAudio2. Depois de inicializar o XAudio2 (consulte [como: inicializar o XAudio2](how-to--initialize-xaudio2.md)) e carregar os dados de áudio (consulte Como: [carregar arquivos de dados de áudio no XAudio2](how-to--load-audio-data-files-in-xaudio2.md)), você pode tocar um som criando uma voz de origem e passando dados de áudio para ela.

## <a name="to-play-a-sound"></a>Para tocar um som

1.  Inicialize o mecanismo XAudio2 seguindo as etapas descritas em [como: inicializar o XAudio2](how-to--initialize-xaudio2.md).
2.  Preencha uma estrutura de [**\_ buffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) e XAudio2 seguindo as etapas descritas em [como carregar arquivos de dados de áudio no XAudio2](how-to--load-audio-data-files-in-xaudio2.md).
    > [!Note]  
    > Dependendo do formato dos dados de áudio, talvez seja necessário usar uma estrutura de dados maior que contenha uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) no lugar de um **WAVEFORMATEX**. Consulte a página de referência do **WAVEFORMATEX** para obter mais informações.

     

3.  Crie uma voz de origem chamando o método [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) em uma instância do mecanismo de XAudio2. O formato da voz é especificado pelos valores definidos em uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) .
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  Envie um [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) para a voz de origem usando a função [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > Os dados de exemplo de áudio para os quais os pontos de *buffer* ainda são "possuídos" pelo aplicativo e devem permanecer alocados e acessíveis até que o som pare de ser reproduzido.

     

5.  Use a função [**Iniciar**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) para iniciar a voz de origem. Como todas as vozes XAudio2 enviam sua saída para a voz de mestre por padrão, o áudio da voz de origem automaticamente faz seu caminho para o dispositivo de áudio selecionado na inicialização. Em um grafo de áudio mais complicado, a voz de origem precisaria especificar a voz à qual a saída deve ser enviada.
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Observações para aplicativos da Windows Store

É recomendável que você use um [ponteiro inteligente](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) para gerenciar o tempo de vida de objetos XAudio2 de forma segura de exceção. Para aplicativos da Windows Store, você pode usar o modelo de ponteiro inteligente [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) do WRL (Windows Runtime C++ Template Library).


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
> Verifique se todos os ponteiros inteligentes para objetos XAUDIO2 são totalmente liberados antes de liberar o objeto [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução XAudio2](getting-started.md)
</dt> <dt>

[Como: Inicializar o XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[Como: Carregar arquivos de dados de áudio no XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 
