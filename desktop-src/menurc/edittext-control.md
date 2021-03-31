---
title: Controle EDITTEXT
description: Define um controle de edição que pertence à classe EDIT.
ms.assetid: 9dc4be90-9503-4c97-813d-db246869ba3c
keywords:
- Menus de controle do EDITTEXT e outros recursos
topic_type:
- apiref
api_name:
- EDITTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 511cff6791703b30ec975625e0cd5cb044f4f492
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640744"
---
# <a name="edittext-control"></a>Controle EDITTEXT

Define um controle de edição que pertence à classe EDIT. Ele cria uma região retangular na qual o usuário pode digitar e editar texto. O controle exibe um cursor quando o usuário clica no mouse nele. Em seguida, o usuário pode usar o teclado para inserir texto ou editar o texto existente. As chaves de edição incluem as chaves Backspace e DELETE. O usuário também pode usar o mouse para selecionar os caracteres a serem excluídos ou para selecionar o local para inserir novos caracteres.

``` syntax
EDITTEXT id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos de controle. Esse valor pode ser uma combinação dos estilos de classe de edição e dos seguintes estilos **: WS \_ TabStop**, **WS \_ Group**, **WS \_ VSCROLL**, **WS \_ HSCROLL** e **WS \_ Disabled**.

Se você não especificar um estilo, o estilo padrão será `ES_LEFT | WS_BORDER | WS_TABSTOP` .

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da instrução **EDITTEXT** :

``` syntax
EDITTEXT  3, 10, 10, 100, 10
```

## <a name="see-also"></a>Consulte também

<dl> <dt>

[Editar controles](../controls/about-edit-controls.md)
</dt> </dl>

 

 