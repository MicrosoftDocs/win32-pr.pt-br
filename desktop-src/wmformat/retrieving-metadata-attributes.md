---
title: Recuperando atributos de metadados
description: Recuperando atributos de metadados
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- SDK do Windows Media Format, recuperando atributos de metadados
- ASF (Advanced Systems Format), recuperando atributos de metadados
- ASF (formato de sistemas avançados), recuperando atributos de metadados
- metadados, recuperando atributos
- fluxos, recuperando atributos de metadados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c918cb47e77c3fd69c64de586b84b7f6244e4c9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007076"
---
# <a name="retrieving-metadata-attributes"></a>Recuperando atributos de metadados

Para recuperar um atributo de um cabeçalho de arquivo, você deve saber o número de fluxo e o índice do atributo. Você pode usar o método [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) para obter os índices de todos os atributos com o mesmo nome ou todos os índices no mesmo idioma. Como os outros métodos de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), o **GetAttributeIndices** lida com um único fluxo ou com todos os atributos de nível de arquivo usando o fluxo 0. Você pode usar 0xFFFF para o número de fluxo para obter índices globais que correspondem aos seus critérios em todo o arquivo, independentemente do número do fluxo.

Quando você souber o índice do atributo que deseja recuperar, chame [**IWMHeaderInfo3:: GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) para obter o atributo. Você precisa fazer duas chamadas para **GetAttributeByIndexEx** para cada atributo recuperado. Na primeira chamada, passe **NULL** para os ponteiros de nome e buffer de dados para obter o tamanho necessário. Em seguida, aloque os buffers do tamanho indicado e faça a segunda chamada para recuperar o nome e os dados.

Por exemplo, código mostrando como recuperar atributos de metadados, consulte [para recuperar todos os metadados em um arquivo](to-retrieve-all-metadata-in-a-file.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com metadados**](working-with-metadata.md)
</dt> </dl>

 

 




