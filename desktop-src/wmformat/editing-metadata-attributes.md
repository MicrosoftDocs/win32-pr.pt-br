---
title: Editando atributos de metadados
description: Editando atributos de metadados
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- SDK do Windows Media Format, editando atributos de metadados
- ASF (Advanced Systems Format), editando atributos de metadados
- ASF (formato de sistemas avançados), editando atributos de metadados
- metadados, editando atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52990e5366da178e9ed5021af93a9f6403b80c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365614"
---
# <a name="editing-metadata-attributes"></a>Editando atributos de metadados

A edição de atributos de metadados é muito semelhante à definição de novos. Em vez de usar [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute), use [**IWMHeaderInfo3:: ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute). **ModifyAttribute** é idêntico a **AddAttribute** , exceto que você não especifica um nome de atributo, e o número de índice é um parâmetro de entrada em vez de uma saída.

Você pode usar o número de fluxo 0xFFFF para especificar um atributo a ser modificado usando seu índice global.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com metadados**](working-with-metadata.md)
</dt> </dl>

 

 




