---
title: Definindo atributos de metadados
description: Definindo atributos de metadados
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- SDK do Windows Media Format, definindo atributos de metadados
- ASF (Advanced Systems Format), definindo atributos de metadados
- ASF (formato de sistemas avançados), definindo atributos de metadados
- metadados, definindo atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfde27d7bc965076d1a4b5f9674c6d198ce61da5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365605"
---
# <a name="setting-metadata-attributes"></a>Definindo atributos de metadados

Os atributos de metadados são definidos usando o método [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) .

Todos os atributos são atribuídos a um idioma da lista de idiomas para o arquivo. Você pode acessar a lista de idiomas usando a interface [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) . Para obter um ponteiro para uma interface **IWMLanguageList** , chame **QueryInterface** em qualquer interface do objeto do qual você obteve [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).

Você pode adicionar atributos com qualquer nome que desejar. No entanto, o uso de nomes de atributos que não são nomes padrão com suporte pelo Windows Media Format SDK pode dificultar a descoberta dos seus metadados. A maioria dos aplicativos de reprodução de mídia verificará se há valores padrão. Para obter mais informações, consulte [metadados personalizados](custom-metadata.md).

Você não pode usar o número de fluxo 0xFFFF para adicionar um atributo globalmente. Você deve atribuir cada atributo a um número de fluxo específico ou o fluxo 0 para atributos de nível de arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com metadados**](working-with-metadata.md)
</dt> </dl>

 

 




