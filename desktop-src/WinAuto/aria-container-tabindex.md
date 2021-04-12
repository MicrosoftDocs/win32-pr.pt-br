---
title: Erro de TabIndex de contêiner do ARIA
description: Erro de TabIndex de contêiner do ARIA
ms.assetid: CCEA9490-903D-423D-B9FD-641E8B7D3E0B
keywords:
- AriaContainerTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6af684b401627181aaef656215240a312393f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364365"
---
# <a name="aria-container-tabindex-error"></a>Erro de TabIndex de contêiner do ARIA

## <a name="text"></a>Texto

O elemento é um contêiner com foco com descendentes ativos definidos, mas sem valor de **TabIndex** maior ou igual a 0.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Este erro se aplica a elementos que têm o atributo **Aria-activedescendant** , não estão desabilitados e não têm o atributo **TabIndex** definido como um valor maior ou igual a 0. Esses elementos devem estar na ordem de tabulação porque são responsáveis por manipular eventos de teclado para seus elementos filho.

Para corrigir esse erro, defina o atributo **TabIndex** com um valor maior ou igual a 0.

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

[Erro de TabIndex da função de contêiner do ARIA (sem o descendente ativo)](aria-container--no-active-descendant--tabindex.md)
</dt> </dl>

 

 




