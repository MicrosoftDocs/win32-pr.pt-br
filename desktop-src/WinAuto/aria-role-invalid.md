---
title: Erro de função ARIA
description: Erro de função ARIA
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- AriaRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c0fcef639a54bcd805bcb3f239e8d42cfeda8c5111d128c5f54157db75d7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134009"
---
# <a name="aria-role-error"></a>Erro de função ARIA

## <a name="text"></a>Texto

O elemento tem uma função DED-ARIA inválida.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Esse erro se aplica a todos os elementos que têm o [**atributo de**](https://developer.mozilla.org/docs/Web/HTML/Reference) função. Indica que o  atributo de função não é uma iniciativa de acessibilidade da Web válida – valor de função DENG-ARIA (Aplicativos de Internet Rich Acessível), conforme definido pela especificação DERIA-ARIA. Definir uma função válida ajuda a garantir que o elemento seja interpretado corretamente por leitores de tela e outras ferramentas de tecnologia adaptativa.

Para corrigir esse erro, defina [**o atributo de**](https://developer.mozilla.org/docs/Web/HTML/Reference) função como um valor de função VALID-ARIA. Observe que as funções ABSTRACT-ARIA abstratas não são válidas.

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

 

 




