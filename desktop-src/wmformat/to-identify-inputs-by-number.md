---
title: Para identificar entradas por número
description: Para identificar entradas por número
ms.assetid: f468f74d-7eed-4819-957d-241903f44d2d
keywords:
- ASF (Advanced Systems Format), identificando entradas por número
- ASF (formato de sistemas avançados), identificando entradas por número
- perfis, identificando entradas por número
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0629776eaaff4252a690c0e31cd6002f5de42b31
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007101"
---
# <a name="to-identify-inputs-by-number"></a>Para identificar entradas por número

Cada exemplo que você passa para o gravador deve estar associado a um número de entrada. Cada número de entrada corresponde a um ou mais fluxos no perfil que o gravador está usando para gravar o arquivo. Em um perfil, as fontes de mídia são identificadas por um nome de conexão. O gravador associa um número de entrada a cada nome de conexão quando você define o perfil para o gravador. Antes de poder passar amostras para o gravador, você deve determinar quais dados cada entrada está esperando. Você não pode pressupor que as entradas estarão na mesma ordem que os fluxos em um perfil, mesmo que esse geralmente seja o caso. Portanto, a única maneira confiável de corresponder entradas com fluxos é comparar o nome de conexão da entrada com o nome da conexão do fluxo.

Para identificar os nomes de conexão e os números de entrada correspondentes para um perfil carregado, execute as seguintes etapas:

1.  Crie um objeto do gravador e defina um perfil a ser usado. Para obter mais informações sobre como configurar perfis no gravador, consulte [para usar perfis com o gravador](to-use-profiles-with-the-writer.md). Você deve saber os nomes de conexão usados para os fluxos no perfil. Você pode obter o nome da conexão de dentro do perfil obtendo o objeto de configuração de fluxo para cada fluxo e chamando [**IWMStreamConfig:: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname). Para obter mais informações sobre perfis e objetos de configuração de fluxo, consulte [trabalhando com perfis](working-with-profiles.md).
2.  Recupere o número total de entradas chamando [**IWMWriter:: GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).
3.  Execute o loop por todas as entradas, executando as etapas a seguir para cada uma.
    -   Recupere a interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) para a entrada chamando [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).
    -   Recupere o nome da conexão que corresponde ao número de entrada chamando [**IWMInputMediaProps:: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname). Depois de ter o nome da conexão, você sabe os fluxos associados aos números de entrada atribuídos pelo gravador.

O código de exemplo a seguir exibe o nome da conexão para cada entrada. Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).


```C++
HRESULT GetNamesForInputs(IWMWriter* pWriter)
{
    DWORD    cInputs  = 0;
    HRESULT  hr       = S_OK;
    WCHAR*   pwszName = NULL;
    WORD     cchName  = 0;

    IWMInputMediaProps* pProps = NULL;

    // Get the total number of inputs for the file.
    hr = pWriter->GetInputCount(&cInputs);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all supported inputs.
    for (DWORD inputIndex = 0; inputIndex < cInputs; inputIndex++)
    {
        // Get the input properties for the input.
        hr = pWriter->GetInputProps(inputIndex, &pProps);  
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size of the connection name.
        hr = pProps->GetConnectionName(0, &cchName);
        GOTO_EXIT_IF_FAILED(hr);

        if (cchName > 0)
        {
            // Allocate memory for the connection name.
            pwszName = new WCHAR[cchName];
            if (wszName == NULL)
            {
                hr = E_OUTOFMEMORY;
                goto Exit;
            }

            // Get the connection name.
            hr = pProps->GetConnectionName(pwszName, &cchName);
            GOTO_EXIT_IF_FAILED(hr);
            
            // Display the name.
            printf("Input # %d = %S\n", pwszName);
        } // end if

        // Clean up for next iteration.
        SAFE_ARRAY_DELETE(pwszName);
        SAFE_RELEASE(pProps);
    } // end for inputIndex

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_RELEASE(pProps);
    return hr;
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




