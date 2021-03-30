---
title: Usando marcadores
description: Usando marcadores
ms.assetid: b801c985-4ec7-441e-9f8a-40c69b1299a9
keywords:
- Windows Media Format SDK, marcadores
- ASF (Advanced Systems Format), marcadores
- ASF (formato de sistemas avançados), marcadores
- ASF (Advanced Systems Format), buscando marcadores
- ASF (formato de sistemas avançados), buscando marcadores
- marcadores, sobre
- marcadores, adicionando
- marcadores, removendo
- marcadores, recuperando
- marcadores, buscando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cc585b8c71e3bfbae85953650809ad031d36a2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103640302"
---
# <a name="using-markers"></a>Usando marcadores

Um *marcador* é um ponto nomeado em um arquivo asf. Cada marcador consiste em um nome e uma hora associada, medido como um deslocamento do início do arquivo. Um aplicativo pode usar marcadores para atribuir nomes a vários pontos dentro do conteúdo, exibir esses nomes para o usuário e, em seguida, buscar as posições do marcador. Um aplicativo pode adicionar ou remover marcadores de um arquivo ASF existente.

A interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) contém métodos para trabalhar com marcadores. O objeto editor de metadados dá suporte à adição e remoção de marcadores. Os objetos gravador e leitor podem recuperar marcadores, mas não podem adicionar ou remover marcadores.

## <a name="adding-markers"></a>Adicionando marcadores

Para adicionar um marcador, consulte o editor de metadados para a interface **IWMHeaderInfo** . Em seguida, chame o método [**IWMHeaderInfo:: Addmarkr**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) , especificando o nome do marcador como uma cadeia de caracteres largos e a hora em unidades de 100 a nanossegundos. A hora não deve exceder a duração do arquivo. Dois marcadores podem ter a mesma hora.

O exemplo a seguir adiciona vários marcadores a um arquivo:


```C++
IWMMetadataEditor *pEdit = 0;
IWMHeaderInfo     *pInfo = 0;

// Create the metadata editor object.

WMCreateEditor(&pEdit);
pEdit->Open(L"C:\\example.wmv");
pEdit->QueryInterface(IID_IWMHeaderInfo, (void**)&pInfo);

// Add the markers. Note that we add the last ones first. Do this when possible
// for improved performance when writing the markers to the file.
hr = pInfo->AddMarker(L"End",  520000000);   // 52 sec.
hr = pInfo->AddMarker(L"Segue",  350000000); // 35 sec.
hr = pInfo->AddMarker(L"Intro",  15000000);  // 1.5 sec.

// Commit changes and clean up.

pEdit->Flush();
pEdit->Close(); 
pInfo->Release();
pEdit->Release();

```



## <a name="removing-markers"></a>Removendo marcadores

Para remover um marcador, chame [**IWMHeaderInfo:: RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker), especificando o índice do marcador a ser removido. Os marcadores são automaticamente classificados em ordem de tempo crescente, portanto, o índice 0 é sempre o primeiro marcador. Observe que a chamada de **RemoveMarker** altera os números de índice dos marcadores a seguir. O código a seguir, em que *pInfo* é um ponteiro para uma interface **IWMHeaderInfo** , remove todos os marcadores de um arquivo:


```C++
WORD count = 0;
pInfo->GetMarkerCount(&count);
while (count--)
{
    pInfo->RemoveMarker(0);
}

```



## <a name="retrieving-markers"></a>Recuperando marcadores

Para recuperar o nome e a hora de um marcador, execute as seguintes etapas:

1.  Chame o método [**IWMHeaderInfo:: GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) para determinar quantos marcadores o arquivo contém.
2.  Recupere o tamanho da cadeia de caracteres necessária para conter o nome do marcador. Para fazer isso, chame o método [**IWMHeaderInfo:: Getmarcer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) . Especifique o índice do marcador a ser recuperado e **NULL** para o buffer da cadeia de caracteres (o parâmetro *pwszMarkerName* ). O método retorna o comprimento da cadeia de caracteres, incluindo o caractere de terminação ' \\ 0 ', no parâmetro *pcchMarkerNameLen* .
3.  Aloque uma cadeia de caracteres largos para receber o nome.
4.  Chame **Getmarcer** novamente, mas desta vez passe o endereço da cadeia de caracteres no parâmetro *pwszMarkerName* . O método grava o nome do marcador na cadeia de caracteres e retorna a hora do marcador no parâmetro *pcnsMarkerTime* .

O código a seguir percorre cada marcador em ordem e recupera o nome e a hora:


```C++
WORD cMarkers = 0;
HRESULT hr = pInfo->GetMarkerCount(&cMarkers);

WCHAR *wszName = 0;
WORD  len = 0;
for (WORD iMarker = 0; iMarker < cMarkers; ++iMarker)
{
    QWORD rtTime = 0;
    WORD req_len = 0;
    hr = pInfo->GetMarker(iMarker, 0, &req_len, &rtTime);
    
    // Reallocate if necessary.
    if (len < req_len)
    {
        delete[] wszName;
        wszName = new WCHAR[req_len];
        len = req_len;
    }
    hr = pInfo->GetMarker(iMarker, wszName, &req_len, &rtTime);
    // Display the name...
}
delete[] wszName;

```



## <a name="seeking-to-a-marker"></a>Buscando um marcador

Para iniciar a reprodução de um local de marcador, chame o método [**IWMReaderAdvanced2:: StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) do objeto Reader, especificando o índice do marcador. Os parâmetros restantes são idênticos aos do método [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) . O exemplo a seguir consulta o leitor para a interface [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) e busca o primeiro marcador.


```C++
IWMReaderAdvanced2 *pReader2 = 0
WORD iMarkerIndex = 0;
hr = pReader->QueryInterface(IID_IWMReaderAdvanced2, (void**)&pReader2);
if (SUCCEEDED(hr))
{
    hr = pPlayer2->StartAtMarker(iMarkerIndex, 0, 1.0, 0);
    pPlayer2->Release();
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)
</dt> <dt>

[**Trabalhando com metadados**](working-with-metadata.md)
</dt> </dl>

 

 




