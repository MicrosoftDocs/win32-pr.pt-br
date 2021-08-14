---
description: Este tópico descreve quando e como usar uma MFT e um coletor MP4 de H. 264/AVC remux.
ms.assetid: 1DD236D9-775B-4417-BC49-BF52A6B3C8AD
title: Quando e como usar o remux do H. 264/AVC e o coletor MP4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ce5b6d63a21e7a9d6b75acd29690cdeaeba5b0105dcf8d45fe0c93e6b768f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119357946"
---
# <a name="when-and-how-to-use-h264avc-remux-mft-and-mp4-sink"></a>Quando e como usar o remux do H. 264/AVC e o coletor MP4

Este tópico descreve quando e como usar uma MFT e um coletor MP4 de H. 264/AVC remux.

## <a name="when-to-use-h264avc-remux-mft"></a>Quando usar o H. 264/AVC remux MFT

O formato de arquivo MPEG-4 requer que cada amostra compactada contenha uma imagem primária com unidades NAL na ordem correta. (Consulte a definição da imagem primária e a ordem obrigatória das unidades de NAL na seção 7.4.1.2.3, **ordem das unidades de nal e imagens codificadas e associação às unidades de acesso**, da especificação da H. 264 AVC.) Ele também requer que cada amostra compactada esteja associada a um carimbo de data/hora de apresentação, decodificação de carimbo de data/hora e duração da amostra.

Em muitos cenários, quando os aplicativos precisam gravar vídeo H. 264/AVC em um contêiner de arquivos MPEG-4, o exemplo compactado pode não atender aos requisitos acima. Por exemplo, um exemplo compactado pode não conter uma imagem primária completa ou pode não ter um carimbo de data/hora de apresentação correto associado a ela. Alguns exemplos de aplicativos são:

-   Escreva o vídeo elementares de streaming H. 264/AVC no contêiner de arquivos MPEG-4.
-   Gravar vídeo da câmera capturada H. 264/AVC no contêiner de arquivos MPEG-4.
-   Registre a conferência de vídeo H. 264/AVC no contêiner de arquivos MPEG-4.
-   Concatenar dois vídeos H. 264/AVC em MPEG-2 TS ou MP4 e gravar no contêiner de arquivos MPEG-4 com carimbos de data/hora corretos.
-   Vídeo remux H. 264/AVC de AVCHD, MPEG-2 formato de arquivo TS/PS para formato de arquivo MPEG-4.
-   Corte o arquivo de vídeo H. 264/AVC sem transcodificação.

Nessa situação, o aplicativo precisa usar um MFT remux de H. 264/AVC para converter as amostras compactadas que não contêm uma imagem primária completa antes de serem gravadas no contêiner de arquivos MPEG-4.

## <a name="how-to-use-h264avc-remux-mft-and-mp4-sink"></a>Como usar a MFT e o coletor MP4 do H. 264/AVC remux

Defina o tipo de mídia de saída de origem como **MFVideoFormat \_ H264 \_ es**, que indica que cada exemplo pode não conter uma imagem primária completa. Defina o tipo de mídia de entrada do coletor MP4 como **MFVideoFormat \_ H264**. Portanto, o tipo de mídia de entrada do MFT H. 264/AVC remux é **MFVideoFormat \_ H264 \_ es** e o tipo de mídia de saída do MFT h. 264/AVC remux é **MFVideoFormat \_ H264**, que será inserido automaticamente no resolvedor de topologia.

A duração da amostra é ignorada pelo remux H. 264/AVC, pois a duração da amostra de um exemplo que não contém uma imagem primária completa não tem significado claro. Em vez disso, a duração da amostra é calculada a partir da taxa de quadros. A taxa de quadros é calculada a partir do parâmetro Sequence. Se as informações não existirem no parâmetro Sequence, a taxa de quadros será calculada a partir dos parâmetros no tipo de mídia de entrada. Se as informações de taxa de quadros não estiverem disponíveis, a taxa de quadros padrão de 29,97 fps será usada.

H. 264/AVC remux MFT interpola linearmente os carimbos de data/hora de decodificação (DTS) para cada imagem compactada de acordo com a taxa de quadros. O MFT H. 264/AVC remux honra os carimbos de data/hora de apresentação de entrada (PTS) nos exemplos de entrada e os transmite para a saída, se existirem. Ele executa a interpolação de PTS de acordo com a taxa de quadros, a PTS anterior e a ordem de saída da imagem por meio do processo de relevo do DBP (buffer de imagem decodificado), conforme especificado no **processo de relevo do anexo C. 4.5.3** da especificação do H. 264 AVC. Cada exemplo de saída do MFT da H. 264/AVC remux deve ter PTS, DTS e duração de amostra. O MFT H. 264/AVC remux também identifica as imagens de IDR no fragmentado e as define como um ponto de limpeza com o atributo MF de [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md).

Atualmente, o MFT da H. 264/AVC remux pode lidar com um máximo de 64 quadro reordenado. Se o número de quadros reordenados exceder 64 com um quadro de referência de longo prazo presente, o MFT H. 264/AVC remux interpolará um PTS incorreto para esse quadro e produzirá esse quadro em um horário incorreto.

Para instanciar um MFT do H. 264/AVC remux, defina os tipos de mídia de entrada e saída corretos no MFT do H. 264/AVC remux, defina o tipo de mídia de entrada para o coletor MP4 e resolva a topologia.

O código de exemplo a seguir mostra como inicializar a MFT e o coletor MP4 do H. 264/AVC remux.

Para o MFT de H. 264/AVC remux,


```C++
hr = CoCreateInstance(
            CLSID_CMSH264RemuxMFT,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IMFTransform,
            (void**) &pIMFTransform
            );
```



Nenhuma outra configuração é necessária.

Para o coletor MP4,


```C++
IMFByteStream*  pMFBSOutputFile = NULL;
hr = MFCreateFile(
    MF_ACCESSMODE_READWRITE,
    MF_OPENMODE_DELETE_IF_EXIST,
    MF_FILEFLAGS_NONE,
    m_pszOutputFile,
    &pMFBSOutputFile);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create output file for MP4 Sink (hr=0x%x)", hr);
    break;
}

hr = MFCreateMPEG4MediaSink(
    pMFBSOutputFile,
    (guidMajorType == MFMediaType_Video) ? pMediaType : NULL,  // pMediaType comes from the output type of the remux MFT
    (guidMajorType == MFMediaType_Audio) ? pMediaType : NULL,
    &m_pMediaSink);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create MP4 Sink (hr=0x%x)", hr);
    break;
}
hr = m_pMediaSink->GetStreamSinkByIndex(0, &pStream);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formatos de mídia compatíveis com o Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



