---
description: Este tópico descreve as etapas mínimas necessárias para reproduzir dados de áudio carregados anteriormente no XAudio2.
ms.assetid: 5172b31c-d2af-45aa-5bd4-b62502f3c047
title: 'Como: Reproduzir um som com o XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cfa5cb2a7a47b7fb54e6a7e9f098a545b0c630c6c27889d7aa6eff1242121d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082901"
---
# <a name="how-to-play-a-sound-with-xaudio2"></a>Como: Reproduzir um som com o XAudio2

Este tópico descreve as etapas mínimas necessárias para reproduzir dados de áudio carregados anteriormente no XAudio2. Depois de inicializar o XAudio2 (consulte Como [inicializar XAudio2)](how-to--initialize-xaudio2.md)e carregar os dados de áudio (consulte Como carregar arquivos de dados de áudio no [XAudio2),](how-to--load-audio-data-files-in-xaudio2.md)você pode reproduzir um som criando uma voz de origem e passando dados de áudio para ele.

## <a name="to-play-a-sound"></a>Para reproduzir um som

1.  Inicialize o mecanismo XAudio2 seguindo as etapas descritas [em Como inicializar o XAudio2.](how-to--initialize-xaudio2.md)
2.  Preencha uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) e [**XAUDIO2 \_ BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) seguindo as etapas descritas em Como carregar arquivos de dados de áudio [no XAudio2.](how-to--load-audio-data-files-in-xaudio2.md)
    > [!Note]  
    > Dependendo do formato dos dados de áudio, talvez seja necessário usar uma estrutura de dados maior que contenha uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) no lugar de **um WAVEFORMATEX.** Consulte a **página de referência WAVEFORMATEX** para obter mais informações.

     

3.  Crie uma voz de origem chamando o método [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) em uma instância do mecanismo XAudio2. O formato da voz é especificado pelos valores definidos em uma [**estrutura WAVEFORMATEX.**](/windows/win32/api/mmreg/ns-mmreg-waveformatex)
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  Envie um [**\_ BUFFER XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) para a voz de origem usando a [**função SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > Os dados de exemplo de áudio aos quais os pontos de *buffer* ainda são "de propriedade" do aplicativo e devem permanecer alocados e acessíveis até que o som pare de ser gravado.

     

5.  Use a [**função Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) para iniciar a voz de origem. Como todas as vozes XAudio2 enviam sua saída para a voz mestra por padrão, o áudio da voz de origem automaticamente vai para o dispositivo de áudio selecionado na inicialização. Em um grafo de áudio mais complicado, a voz de origem teria que especificar a voz para a qual sua saída deve ser enviada.
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Notas para aplicativos Windows Store

Recomendamos que você use um ponteiro [inteligente para](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) gerenciar o tempo de vida de objetos XAUDIO2 de maneira segura de exceção. Para Windows aplicativos da Store, você pode usar o modelo de ponteiro [**inteligente ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) da WRL (Biblioteca de Modelos C++) do runtime do Windows.


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
> Verifique se todos os ponteiros inteligentes para objetos XAUDIO2 estão totalmente liberados antes de liberar o [**objeto IXAudio2.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[XAudio2 Ponto de Partida](getting-started.md)
</dt> <dt>

[Como: Inicializar o XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[Como: Carregar arquivos de dados de áudio no XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 
