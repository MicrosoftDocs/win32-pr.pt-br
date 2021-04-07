---
description: Esse controle exibe uma longa cadeia de caracteres de texto que não se ajusta totalmente à página. Um uso comum para esse controle é exibir o contrato de licença.
ms.assetid: a49209f3-043c-4360-b1e3-9fa9538c2c9b
title: Controle ScrollableText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ff807f2b0175eb411b3c45eb9d1e3b5eeaea01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828426"
---
# <a name="scrollabletext-control"></a>Controle ScrollableText

Esse controle exibe uma longa cadeia de caracteres de texto que não se ajusta totalmente à página. Um uso comum para esse controle é exibir o contrato de licença.

Observe que a cadeia de caracteres de texto usada com esse controle não pode conter uma propriedade incorporada. Para exibir o texto com propriedades inseridas, use o [controle de texto](text-control.md).

## <a name="control-attributes"></a>Atributos de controle

Você pode usar os atributos a seguir com este controle. Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent, na [tabela EventMappings](eventmapping-table.md) e liste o identificador do atributo na coluna atributo. Insira o identificador do ControlEvent, na coluna de evento.



| Identificador de atributo                               | Bit hexadecimal                  | Descrição                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Posição](position-control-attribute.md)         |                                  | Posição de controle na caixa de diálogo. Insira a largura, a altura e as coordenadas do controle do canto esquerdo do controle nas colunas largura, altura, X e Y da tabela de [controle](control-table.md) ou da [tabela BBControl](bbcontrol-table.md). Use [unidades de instalador](installer-units.md) para duração e distância.<br/>                                            |
| [Text](text-control-attribute.md)                 |                                  | Texto exibido pelo controle. Insira a cadeia de texto RTF na coluna de texto da [tabela de controle](control-table.md).                                                                                                                                                                                                                                                       |
| [Visível](visible-control-attribute.md)           | 0x00000000 0x00000001<br/> | Controle oculto. Controle visível.<br/> Para tornar o controle visível ou oculto na criação, inclua esse bit na palavra bit da coluna Attributes na tabela de [controle](control-table.md) ou na [tabela BBControl](bbcontrol-table.md).<br/> Você também pode ocultar ou mostrar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/> |
| [Enabled](enabled-control-attribute.md)           | 0x00000000 0x00000002<br/> | Controle em um estado desabilitado. Controle em um estado habilitado.<br/> Inclua esse bit na coluna atributos das tabelas [Control](control-table.md) ou [BBControl](bbcontrol-table.md) para habilitar o controle na criação.<br/> Você também pode habilitar ou desabilitar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>             |
| [Submersa](sunken-control-attribute.md)             | 0x00000000 0x00000004<br/> | Exibir o estilo visual padrão. Exiba o controle com uma aparência de baixo e baixo, 3D.<br/> Inclua esses bits na palavra de bits na coluna atributos da tabela de [controle](control-table.md).<br/>                                                                                                                                                                    |
| [RTLRO](rtlro-control-attribute.md)               | 0x00000000 0x00000020<br/> | O texto no controle é exibido em uma ordem de leitura da esquerda para a direita. O texto no controle é exibido em uma ordem de leitura da direita para a esquerda.<br/>                                                                                                                                                                                                                               |
| [RightAligned](rightaligned-control-attribute.md) | 0x00000000 0x00000040<br/> | O texto no controle é alinhado à esquerda. O texto no controle está alinhado à direita.<br/>                                                                                                                                                                                                                                                                            |
| [LeftScroll](leftscroll-control-attribute.md)     | 0x00000000 0x00000080<br/> | A barra de rolagem está localizada no lado direito do controle. A barra de rolagem está localizada no lado esquerdo do controle.<br/>                                                                                                                                                                                                                                              |
| [BiDi](bidi-control-attribute.md)                 | 0x000000E0                       | Defina esse valor para uma combinação dos atributos [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)e [LeftScroll](leftscroll-control-attribute.md) .                                                                                                                                                                               |



 

## <a name="remarks"></a>Comentários

Esse controle pode ser criado a partir da classe RICHEDIT usando a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Ele tem os estilos de **\_ multilinha es**, **WS \_ VSCROLL**, **es \_ ReadOnly**, **WS \_ TabStop**, **es \_ AUTOVSCROLL**, **WS \_ Child**, **WS \_ Group** e **es \_ NOOLEDRAGDROP** .

 

 
