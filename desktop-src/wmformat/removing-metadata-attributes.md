---
title: Removendo atributos de metadados
description: Removendo atributos de metadados
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- Windows SDK de Formato de Mídia, removendo atributos de metadados
- ASF (Advanced Systems Format), removendo atributos de metadados
- ASF (Formato de Sistemas Avançados), removendo atributos de metadados
- metadados, removendo atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e09e00fbba8ca5464ccec570a03bbd4e30935238bc531d36ce220a60150839e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110206"
---
# <a name="removing-metadata-attributes"></a>Removendo atributos de metadados

Você pode remover um atributo de metadados passando seu índice e número de fluxo para o [**método IWMHeaderInfo3::D eleteAttribute.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) A ordem na qual os atributos restantes são indexados após a remoção de um atributo não é alterada; todos os atributos restantes que originalmente tinham um valor de índice maior que o removido têm seus valores de índice reduzidos em um. Ao remover vários atributos, faça isso em ordem decrescente por índice para evitar a precisar calcular o ajuste na indexação.

Para sua conveniência na remoção de valores, o método [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) retorna os valores de índice em ordem decrescente.

> [!Note]  
> Os valores de índice obtidos usando os métodos [**de IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) não são compatíveis com valores de índice obtidos usando os métodos [**de IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo). Se você usar os métodos de uma interface para alterar atributos em um arquivo, deverá presumir que os valores de índice recuperados anteriormente da outra interface não são mais válidos e devem ser obtidos novamente. Você deve evitar usar os métodos de **IWMHeaderInfo,** se possível.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com metadados**](working-with-metadata.md)
</dt> </dl>

 

 




