---
title: Removendo atributos de metadados
description: Removendo atributos de metadados
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- SDK do Windows Media Format, removendo atributos de metadados
- Formato de sistema avançado (ASF), removendo atributos de metadados
- ASF (formato de sistemas avançados), removendo atributos de metadados
- metadados, removendo atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b10176452dcc78cc3eca898b61c350a157e568
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104365745"
---
# <a name="removing-metadata-attributes"></a>Removendo atributos de metadados

Você pode remover um atributo de metadados passando seu índice e o número de fluxo para o método [**IWMHeaderInfo3::D eleteattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) . A ordem na qual os atributos restantes são indexados após a remoção de um atributo não é alterada; todos os atributos restantes que originalmente tinham um valor de índice maior do que aquele removido têm seus valores de índice reduzidos em um. Ao remover vários atributos, faça isso em ordem decrescente por índice para evitar ter que calcular o ajuste na indexação.

Para sua conveniência na remoção de valores, o método [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) retorna os valores de índice em ordem decrescente.

> [!Note]  
> Os valores de índice obtidos usando os métodos de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) não são compatíveis com os valores de índice obtidos com o uso dos métodos de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo). Se você usar os métodos de uma interface para alterar atributos em um arquivo, deverá assumir que qualquer valor de índice recuperado anteriormente da outra interface não será mais válido e deverá ser obtido novamente. Você deve evitar usar os métodos de **IWMHeaderInfo** , se possível.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com metadados**](working-with-metadata.md)
</dt> </dl>

 

 




