---
description: Esse controle exibe uma cadeia de caracteres longa de texto que não pode caber totalmente na página. Um uso comum para esse controle é exibir o contrato de licença.
ms.assetid: a49209f3-043c-4360-b1e3-9fa9538c2c9b
title: Controle ScrollableText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f4d5ac48f6b89b779960126e62c204d1d09e1f9a7bc832b0e3477635df35ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041296"
---
# <a name="scrollabletext-control"></a>Controle ScrollableText

Esse controle exibe uma cadeia de caracteres longa de texto que não pode caber totalmente na página. Um uso comum para esse controle é exibir o contrato de licença.

Observe que a cadeia de caracteres de texto usada com esse controle não pode conter uma propriedade inserida. Para exibir texto com propriedades inseridas, use o [Controle de Texto](text-control.md).

## <a name="control-attributes"></a>Atributos de controle

Você pode usar os atributos a seguir com esse controle. Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent na tabela [EventMapping](eventmapping-table.md) e liste o identificador do atributo na coluna Atributo. Insira o identificador do ControlEvent na coluna Evento.



| Identificador de atributo                               | Bit hexadecimal                  | Descrição                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Posição](position-control-attribute.md)         |                                  | Posição do controle na caixa de diálogo. Insira a largura, a altura e as coordenadas do canto esquerdo do controle nas colunas Width, Height, X e Y da tabela [Control](control-table.md) ou [BBControl](bbcontrol-table.md). Use [unidades do instalador](installer-units.md) para comprimento e distância.<br/>                                            |
| [Text](text-control-attribute.md)                 |                                  | Texto exibido pelo controle . Insira a cadeia de caracteres de texto RTF na coluna Texto da [tabela Controle](control-table.md).                                                                                                                                                                                                                                                       |
| [Visível](visible-control-attribute.md)           | 0x00000000 0x00000001<br/> | Controle oculto. Controle visível.<br/> Para tornar o controle visível ou oculto em sua criação, inclua esse bit na palavra bit da coluna Atributos na tabela [Control](control-table.md) ou [na tabela BBControl](bbcontrol-table.md).<br/> Você também pode ocultar ou mostrar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/> |
| [Habilitada](enabled-control-attribute.md)           | 0x00000000 0x00000002<br/> | Controle em um estado desabilitado. Controle em um estado habilitado.<br/> Inclua esse bit na coluna Atributos das [tabelas Control](control-table.md) ou [BBControl](bbcontrol-table.md) para habilitar o controle na criação.<br/> Você também pode habilitar ou desabilitar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>             |
| [Afundado](sunken-control-attribute.md)             | 0x00000000 0x00000004<br/> | Exibir o estilo visual padrão. Exibir o controle com um 3D esquenado, look.<br/> Inclua esses bits na palavra bit na coluna Atributos da [tabela Controle](control-table.md).<br/>                                                                                                                                                                    |
| [RTLRO](rtlro-control-attribute.md)               | 0x00000000 0x00000020<br/> | O texto no controle é exibido em uma ordem de leitura da esquerda para a direita. O texto no controle é exibido em uma ordem de leitura da direita para a esquerda.<br/>                                                                                                                                                                                                                               |
| [RightAligned](rightaligned-control-attribute.md) | 0x00000000 0x00000040<br/> | O texto no controle é alinhado à esquerda. O texto no controle é alinhado à direita.<br/>                                                                                                                                                                                                                                                                            |
| [LeftScroll](leftscroll-control-attribute.md)     | 0x00000000 0x00000080<br/> | A barra de rolagem está localizada no lado direito do controle. A barra de rolagem está localizada no lado esquerdo do controle.<br/>                                                                                                                                                                                                                                              |
| [Bidi](bidi-control-attribute.md)                 | 0x000000E0                       | De definir esse valor para uma combinação dos atributos [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)e [LeftScroll.](leftscroll-control-attribute.md)                                                                                                                                                                               |



 

## <a name="remarks"></a>Comentários

Esse controle pode ser criado a partir da classe RICHEDIT usando a [**função CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Ele tem os estilos **ES \_ MULTILINE,** **WS \_ VSCROLL,** **ES \_ READONLY,** **WS \_ TABSTOP,** **ES \_ AUTOVSCROLL,** **WS \_ CHILD,** **WS \_ GROUP** **e ES \_ NOOLEDRAGDROP.**

 

 
