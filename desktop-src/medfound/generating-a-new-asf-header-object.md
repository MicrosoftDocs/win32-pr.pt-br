---
description: Gerando um novo objeto de cabeçalho ASF
ms.assetid: cf73306d-156a-45c0-a3d6-ae48734f5709
title: Gerando um novo objeto de cabeçalho ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f303be4eb3353a0e7ddf1dad0eff9956f68d7db5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501165"
---
# <a name="generating-a-new-asf-header-object"></a>Gerando um novo objeto de cabeçalho ASF

Para converter as informações contidas no objeto ContentInfo em um formato de objeto de cabeçalho ASF binário, o aplicativo deve chamar [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader). Essa chamada deve ser feita depois que os pacotes de dados são gerados e o objeto ContentInfo contém informações atualizadas. **GenerateHeader** retorna um ponteiro para um buffer de mídia que contém as informações de cabeçalho no formato válido. Em seguida, o aplicativo pode gravar os dados, apontados pelo buffer de mídia, no início de um novo arquivo ASF.

## <a name="to-write-a-new-header-object-by-using-the-contentinfo-object"></a>Para gravar um novo objeto de cabeçalho usando o objeto ContentInfo

1.  Chame [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para criar um objeto ContentInfo vazio.
2.  Chame [**IMFASFContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para fornecer o objeto de perfil ao objeto ContentInfo. Para obter informações sobre como criar perfis, consulte [criando um perfil de ASF](creating-an-asf-profile.md).
3.  Chame [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) e passe **NULL** no parâmetro *pIHeader* e receba o tamanho do objeto ContentInfo populado no parâmetro *pcbHeader* . O aplicativo pode usar esse valor para alocar memória ou o buffer de mídia que conterá o objeto de cabeçalho.

    O tamanho do cabeçalho recebido inclui o tamanho do preenchimento, que é ajustado dependendo do tamanho real dos objetos de cabeçalho. O tamanho máximo dos objetos de cabeçalho é 10 MB. Se o tamanho exceder esse valor, **GenerateHeader** falhará com o \_ erro de INVALIDDATA MF E \_ ASF \_ .

4.  Chame [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) para criar um buffer de mídia do tamanho recebido na etapa 3.
5.  Chame **GenerateHeader** novamente para gerar o novo objeto de cabeçalho ASF do objeto ContentInfo no buffer de mídia criado na etapa 4.

    O comprimento dos dados no buffer de mídia é atualizado e o novo tamanho é retornado no parâmetro *pcbHeader* .

6.  Grave o conteúdo do buffer de mídia no início do arquivo. O aplicativo pode usar o fluxo de bytes para executar a operação de gravação. Para obter um exemplo de código, consulte [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).

### <a name="example"></a>Exemplo

O código de exemplo a seguir mostra como criar um objeto ContentInfo e gerar um buffer de mídia para armazenar o novo objeto de cabeçalho. Para obter um exemplo completo que usa esse código, consulte [tutorial: copiando fluxos ASF de um arquivo para outro](tutorial--copying-asf-streams-from-one-file-to-another.md).


```C++
//-------------------------------------------------------------------
// WriteASFFile
//
// Writes the complete ASF file.
//-------------------------------------------------------------------

HRESULT WriteASFFile( 
    IMFASFContentInfo *pContentInfo, // ASF Content Info for the output file.
    IMFByteStream *pDataStream,      // Data stream.
    PCWSTR pszFile                   // Output file name.
    )
{
    
    IMFMediaBuffer *pHeaderBuffer = NULL;
    IMFByteStream *pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    // Create output file.
    HRESULT hr = MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        pszFile,
        &pWmaStream
        );

    // Get the size of the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(NULL, &cbHeaderSize);
    }

    // Create a media buffer.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    }

    // Populate the media buffer with the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    }
 
    // Write the header contents to the byte stream for the output file.
    if (SUCCEEDED(hr))
    {
        hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDataStream->SetCurrentPosition(0);
    }

    // Append the data stream to the file.

    if (SUCCEEDED(hr))
    {
        hr = AppendToByteStream(pDataStream, pWmaStream);
    }

    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);

    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando um objeto de cabeçalho ASF para um novo arquivo](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



