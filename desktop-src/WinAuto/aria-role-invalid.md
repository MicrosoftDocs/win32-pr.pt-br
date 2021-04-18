---
title: Erro de função do ARIA
description: Erro de função do ARIA
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- AriaRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df04ad94d68ae1e8e2e8d3352aa349834a2389fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "105760430"
---
# <a name="aria-role-error"></a>Erro de função do ARIA

## <a name="text"></a>Texto

O elemento tem uma função WAI-ARIA inválida.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Esse erro se aplica a todos os elementos que têm o atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) . Ele indica que o atributo de **função** não é um valor de função de Wai (aplicativos de Internet avançado) acessível para iniciativa de acessibilidade da Web, conforme definido pela especificação WAI-ARIA. Definir uma função válida ajuda a garantir que o elemento seja interpretado corretamente por leitores de tela e por outras ferramentas de tecnologia assistencial.

Para corrigir esse erro, defina o atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) como um valor de função WAI-ARIA válido. Observe que as funções abstratas WAI-ARIA não são válidas.

## <a name="example"></a>Exemplo


```HTML
<!—The invalid role will not expose this element as a button. -->
<div role="backbutton" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >

<!—Setting the correct role will expose this as a button that can be clicked. -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Erro de função de contêiner do ARIA](aria-container-role.md)
</dt> </dl>

 

 




