---
description: Criando o objeto divisor de ASF
ms.assetid: 448e2b38-70f7-4491-aac8-ee988a6f7473
title: Criando o objeto divisor de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42c8033a0861102f6d66b22e43516a616d6428b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826736"
---
# <a name="creating-the-asf-splitter-object"></a>Criando o objeto divisor de ASF

O objeto *divisor* de ASF é um objeto de camada WMContainer que analisa o objeto de dados ASF de um arquivo ASF (Advanced Systems Format). Para criar uma nova instância do objeto divisor de ASF, chame a função [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) . Essa função retorna um ponteiro para a interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) que representa um objeto divisor vazio.

Antes que o divisor possa começar a análise, o aplicativo deve inicializar o separador com informações do objeto de cabeçalho ASF. Para inicializar o divisor, chame o método [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) . Esse método usa um ponteiro para o [objeto ContentInfo do ASF](asf-contentinfo-object.md) que contém informações de cabeçalho do arquivo ASF a ser analisado. O aplicativo deve inicializar o objeto ContentInfo antes de passá-lo para o divisor para que as características do arquivo de mídia sejam conhecidas pelo aplicativo. O método **Initialize** do separador extrai informações de fluxo do objeto ContentInfo, como números de fluxo, para que o divisor possa analisar os pacotes de dados.

### <a name="example"></a>Exemplo

O exemplo de código a seguir mostra como criar um divisor e inicializá-lo com um objeto ContentInfo existente.


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



> [!Note]  
> Este exemplo usa a função [SafeRelease](saferelease.md) para liberar ponteiros de interface.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Divisor de ASF](asf-splitter.md)
</dt> </dl>

 

 



