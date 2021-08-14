---
title: Definindo atributos de metadados
description: Definindo atributos de metadados
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- Windows SDK de Formato de Mídia, definindo atributos de metadados
- ASF (Advanced Systems Format), definindo atributos de metadados
- ASF (Formato de Sistemas Avançados), definindo atributos de metadados
- metadados, atributos de configuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa352a83e758b97bde6088377f8461a62b2d5071314d45f4978035bec219a5cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197505"
---
# <a name="setting-metadata-attributes"></a>Definindo atributos de metadados

Os atributos de metadados são definidos usando o [**método IWMHeaderInfo3::AddAttribute.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute)

Todos os atributos são atribuídos a um idioma da lista de idiomas para o arquivo. Você pode acessar a lista de idiomas usando a interface [**IWMLanguageList.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) Para obter um ponteiro para uma interface **IWMLanguageList,** chame **QueryInterface** em qualquer interface do objeto do qual você obteve [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).

Você pode adicionar atributos com qualquer nome que quiser. No entanto, o uso de nomes de atributo que não são nomes padrão com suporte do SDK Windows Formato de Mídia pode dificultar a descoberta dos metadados pelos usuários. A maioria dos aplicativos com reprodução de mídia verificará se há valores padrão. Para obter mais informações, consulte [Metadados personalizados.](custom-metadata.md)

Não é possível usar o número de 0xFFFF para adicionar um atributo globalmente. Você deve atribuir cada atributo a um número de fluxo específico ou o fluxo 0 para atributos de nível de arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com metadados**](working-with-metadata.md)
</dt> </dl>

 

 




