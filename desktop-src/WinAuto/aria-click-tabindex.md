---
title: Erro de TabIndex do ARIA
description: Erro de TabIndex do ARIA
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- AriaTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acfec56fe1f9f6074579a8b84bccc9dfdef2e1da
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104008537"
---
# <a name="aria-tabindex-error"></a>Erro de TabIndex do ARIA

## <a name="text"></a>Texto

O elemento não está desabilitado e tem um manipulador de eventos de **clique** , mas tem **TabIndex** < 0 e não está na ordem de tabulação por padrão.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Este erro se aplica a elementos que têm um manipulador de eventos de clique e não estão desabilitados. Esses elementos devem estar na ordem de tabulação. Isso garante que um elemento pode ser acessado usando a tecla Tab, que é como os usuários do leitor de tela normalmente navegam pela interface do usuário.

Para corrigir esse erro, defina o atributo [**TabIndex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) para um valor que seja igual ou maior que 0. Você não precisa definir explicitamente o atributo **TabIndex** para as marcas que estão na ordem de tabulação por padrão, como [**um**](https://developer.mozilla.org/docs/Web/HTML/Element/a) (com o atributo [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) ), o [**botão**](https://developer.mozilla.org/docs/Web/HTML/Element/button), a [**entrada**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (excluindo "oculto"), [**Select**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**TextArea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)e [**Area**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (como parte do mapa de imagem).

## <a name="example"></a>Exemplo


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




