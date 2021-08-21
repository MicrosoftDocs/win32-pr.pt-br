---
title: UI_PKEY_Keytip
description: Identifica a propriedade \_ PKEY Keytip da interface \_ do usuário.
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940a855561dfd30dfbf063323f4b86b03561163c4fbf34f9db08be4eb3e1ece3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028604"
---
# <a name="ui_pkey_keytip"></a>Dica de \_ tecla PKEY \_ da interface do usuário

Identifica a propriedade \_ PKEY Keytip da interface \_ do usuário.

```
propertyDescription
   name = UI_PKEY_Keytip
   shellPKey = UI_PKEY_Keytip
   formatID = 00000003-7363-696e-8441798acf5aebb7
   propID = 3
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Comentários

A \_ dica de tecla PKEY \_ da interface do usuário é usada por um aplicativo para consultar o acelerador de teclado de um controle de faixa de opções.

Esse valor da propriedade é uma cadeia de caracteres, composta por qualquer sequência de caracteres, incluindo espaço em branco.

O valor da dica de tecla PKEY da interface do usuário atua como o acelerador de teclado para um Comando, a menos que esse Comando seja \_ exposto por meio de um item de \_ menu. Nesse caso, a estrutura ignora o valor da dica de tecla PKEY da interface do usuário e, em vez disso, usa um caractere precedido por um e comercial, conforme especificado por \_ \_ [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) ou [UI \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md). Se nenhum ampersand for especificado por **Command.LabelTitle** ou rótulo PKEY da interface do usuário, nenhum acelerador de tecla ou teclado \_ \_ será exposto.

O comprimento máximo da dica de tecla PKEY da interface do \_ \_ usuário é ilimitado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do recurso](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command.Keytip**](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




