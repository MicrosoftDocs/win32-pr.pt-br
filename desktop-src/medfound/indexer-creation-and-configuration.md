---
description: Este tópico fornece informações sobre como criar o objeto do indexador padrão fornecido pelo Media Foundation.
ms.assetid: 3a2caf11-808b-4910-b83c-a272a026f0d3
title: Criação e configuração do indexador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e0a341e3074ca44aa4403a3f2f518b4fb9082d4c6eadee1f4ca94a69e17bd98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061196"
---
# <a name="indexer-creation-and-configuration"></a>Criação e configuração do indexador

O *indexador* ASF é um componente de camada WMContainer que é usado para ler ou gravar objetos de índice em um arquivo ASF (Advanced Systems Format). Este tópico fornece informações sobre como criar o objeto do indexador padrão fornecido pelo Media Foundation.

Para obter informações sobre a estrutura de um arquivo ASF, consulte [estrutura de arquivo ASF](asf-file-structure.md).

**Para criar e inicializar o indexador ASF**

1.  Chame a função [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) para receber um ponteiro [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) para o objeto indexador.
2.  Chame [**IMFASFIndexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) para especificar o modo de leitura ou gravação para o objeto indexador. Por padrão, o indexador é configurado para busca direta.

    

    | Usar                       | Sinalizador                                           |
    |---------------------------|------------------------------------------------|
    | Lendo (pesquisa direta) | Zero (padrão)                                 |
    | Lendo (procurando inversa) | **\_leitura do indexador MFASF \_ \_ para \_ REVERSEPLAYBACK** |
    | Gravando                   | MFASF \_ indexer \_ gravar \_ novo \_ índice              |

    

     

    > [!Note]  
    > A mesma instância do indexador não pode ser usada para leitura e gravação. Você deve configurar o indexador para um ou outro.

     

3.  Chame [**IMFASFIndexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) para inicializar o indexador especificando o ponteiro [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) do objeto ContentInfo que descreve o arquivo a ser gravado ou lido. O objeto ContentInfo contém informações que constituem o [objeto de cabeçalho ASF](asf-file-structure.md). O objeto indexador requer um objeto ContentInfo válido antes de gerar ou ler entradas de índice de um arquivo ASF.

O exemplo de código a seguir mostra como um aplicativo pode criar e inicializar o objeto indexador para trabalhar com conteúdo ASF específico. O objeto ContentInfo representa o objeto de cabeçalho ASF; o conteúdo é passado como um fluxo de bytes.


```C++
HRESULT CreateASFIndexer(
    IMFASFContentInfo* pContentInfo, 
    DWORD dwFlags,
    IMFASFIndexer** ppIndexer
    )
{
    *ppIndexer = NULL;

    IMFASFIndexer *pIndexer = NULL;

    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pIndexer->SetFlags(dwFlags);
    if (FAILED(hr))
    {
        goto done;
    }

    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the object to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    // Clean up.
    SafeRelease(&pIndexer);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Indexador ASF](asf-index-object.md)
</dt> <dt>

[Usando o indexador para buscar em um arquivo ASF](using-the-indexer-to-seek.md)
</dt> <dt>

[Usando o indexador para gravar um novo índice](using-the-indexer-to-write-a-new-index.md)
</dt> </dl>

 

 



