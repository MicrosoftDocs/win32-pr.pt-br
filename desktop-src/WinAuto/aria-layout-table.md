---
title: Erro de tabela de apresentação do ARIA
description: Erro de tabela de apresentação do ARIA
ms.assetid: 3D5AE911-78E5-4C40-B77B-604E65839F63
keywords:
- AriaLayoutTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae1ef7cae971e6dc365bd3f8ebe6135561f3ff3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103642921"
---
# <a name="aria-presentation-table-error"></a>Erro de tabela de apresentação do ARIA

## <a name="text"></a>Texto

A tabela usada para layout não deve ter informações de cabeçalho, nome acessível ou resumo definidas (**th**, **Summary**, **Aria-DescribedBy**, **Aria-labelledby**, **Aria-Label**, **title**, atributos de **legenda** ).

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Esse erro se aplica a marcas de tabela HTML que têm o atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) definido como "Presentation", ou com uma tabela que tem uma única célula (1 × 1 tabela).

Esse erro indica que uma tabela está marcada como somente layout (tem `role="presentation"` ), mas também contém informações de acessibilidade como se fosse uma tabela de dados, o que pode ser confuso para os usuários do leitor de tela.

Para resolver esse erro, determine se a tabela realmente é apenas uma tabela de layout e, em caso afirmativo, remova a marcação acessível:

-   Elemento [**Caption**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) , [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)ou atributos [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) .
-   atributos de [**Resumo**](https://www.bing.com/search?q=**summary**) ou [**Aria-DescribedBy**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .
-   Marcas do [**thead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) .

## <a name="example"></a>Exemplo

![HTML para um elemento table, com atributos como resumo que disparam o erro de tabela de apresentação do Aria mostrado como marcação HTML com traço e saída ](images/aria-layout-table.png)

## <a name="remarks"></a>Comentários

Se você determinar que uma tabela precisa de informações de acessibilidade, remova o atributo de [**função**](https://developer.mozilla.org/docs/Web/HTML/Reference) ou defina-o com um valor diferente de "apresentação".

 

 




