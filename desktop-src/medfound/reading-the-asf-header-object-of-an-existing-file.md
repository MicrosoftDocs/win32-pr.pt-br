---
description: Lendo o objeto de cabeçalho ASF de um arquivo existente
ms.assetid: 0e37f0d3-a37b-4f36-a133-7b1922e9944b
title: Lendo o objeto de cabeçalho ASF de um arquivo existente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b231cb0b9af6b24f84efaa6403a4774e66bbb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765606"
---
# <a name="reading-the-asf-header-object-of-an-existing-file"></a>Lendo o objeto de cabeçalho ASF de um arquivo existente

O objeto ASF ContentInfo armazena informações que representam os objetos de cabeçalho ASF de um arquivo de mídia. Um objeto ContentInfo populado é necessário para ler e analisar um arquivo ASF existente.

Depois de criar o objeto ContentInfo chamando a função [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , o aplicativo deve inicializá-lo com informações de cabeçalho do arquivo ASF a ser lido. Para popular o objeto, chame [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).

**ParseHeader** requer um buffer de mídia que contenha o objeto de cabeçalho do arquivo asf. Uma opção é preencher um buffer de mídia com o objeto de cabeçalho para criar um fluxo de bytes para o arquivo e, em seguida, ler os primeiros 30 bytes de dados do fluxo de bytes em um buffer de mídia. Em seguida, você pode obter o tamanho passando os primeiros 24 bytes do objeto de cabeçalho para o método [**IMFASFContentInfo:: Getheaders**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) . Depois de obter o tamanho, você pode ler o objeto de cabeçalho inteiro em um buffer de mídia e passá-lo para **ParseHeader**. O método inicia a análise no deslocamento a partir do início do buffer de mídia especificado no parâmetro *cbOffsetWithinHeader* .

O código de exemplo a seguir cria e inicializa um objeto ContentInfo para ler um arquivo ASF existente contido em um fluxo de bytes. Primeiro, definimos uma função auxiliar que lê dados de um fluxo de bytes e aloca um buffer de mídia para manter os dados:


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



O exemplo a seguir lê o objeto de cabeçalho ASF de um fluxo de bytes e popula um objeto ContentInfo do ASF.


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



> [!Note]  
> Esses exemplos usam a função [SafeRelease](saferelease.md) para liberar ponteiros de interface.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objeto ASF ContentInfo](asf-contentinfo-object.md)
</dt> <dt>

[Objeto de cabeçalho ASF](asf-file-structure.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Obtendo informações de objetos de cabeçalho ASF](getting-information-from-asf-header-objects.md)
</dt> </dl>

 

 



