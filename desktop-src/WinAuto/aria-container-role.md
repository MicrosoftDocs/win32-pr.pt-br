---
title: Erro de função de contêiner do ARIA
description: Erro de função de contêiner do ARIA
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- AriaContainerRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02554c868816c05981fa9f008c8f79f0a3eb0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916580"
---
# <a name="aria-container-role-error"></a>Erro de função de contêiner do ARIA

## <a name="text"></a>Texto

O elemento com o **descendente** definido como ativo não tem uma função de contêiner (**ComboBox**, **Grid**, **ListBox**, **menu**, **MenuBar** **, Radiogroup,** **Tree**, **árvore**, **tablist**, **Row**).

## <a name="type"></a>Type

Erro

## <a name="description"></a>Descrição

Esse erro se aplica a elementos que têm o atributo **Aria-activedescendant** .

Um elemento parece ser um contêiner que tem o atributo **Aria-activedescendant** definido, mas o atributo de função do elemento não tem um valor válido para um contêiner.

Para corrigir esse erro, defina o atributo **role** como um valor de função Rich Internet Applications (WAI-ARIA) acessível para iniciativa de acessibilidade da Web que seja válido para um elemento de contêiner: **ComboBox**, **Grid**, **ListBox**, **menu**, **BarraDeMenu**, **radioobject**, **tablist**, **Tree** ou **árvore**.

## <a name="example"></a>Exemplo


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1">
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Erro de função do ARIA](aria-role-invalid.md)
</dt> </dl>

 

 




