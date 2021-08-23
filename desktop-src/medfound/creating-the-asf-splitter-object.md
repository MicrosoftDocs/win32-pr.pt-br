---
description: Criando o objeto divisor ASF
ms.assetid: 448e2b38-70f7-4491-aac8-ee988a6f7473
title: Criando o objeto divisor ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5782f42b53607943704836c350b76e69d872e8d9654959d4453d8e029c21f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600806"
---
# <a name="creating-the-asf-splitter-object"></a>Criando o objeto divisor ASF

O objeto *divisor* ASF é um objeto de camada WMContainer que analisado o objeto de dados ASF de um arquivo ASF (Advanced Systems Format). Para criar uma nova instância do objeto divisor ASF, chame a [**função MFCreateASFSplitter.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) Essa função retorna um ponteiro para a interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) que representa um objeto divisor vazio.

Antes que o divisor possa começar a análise, o aplicativo deve inicializar o divisor com informações do objeto de header ASF. Para inicializar o divisor, chame o [**método IMFASFSplitter::Initialize.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) Esse método leva um ponteiro para o [Objeto ContentInfo do ASF](asf-contentinfo-object.md) que contém informações de título do arquivo ASF a ser analisado. O aplicativo deve inicializar o objeto ContentInfo antes de passá-lo para o divisor para que as características do arquivo de mídia sejam conhecidas pelo aplicativo. O método **Initialize** do divisor extrai informações de fluxo do objeto ContentInfo, como números de fluxo, para que o divisor possa analisar os pacotes de dados.

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
> Este exemplo usa a [função SafeRelease](saferelease.md) para liberar ponteiros de interface.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Divisor ASF](asf-splitter.md)
</dt> </dl>

 

 



