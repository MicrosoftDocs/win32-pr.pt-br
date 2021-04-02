---
description: O controle GroupBox exibe um retângulo, possivelmente com texto de legenda, que serve para agrupar outros controles juntos na caixa de diálogo.
ms.assetid: e1cdcf71-876f-4115-96a4-95d8a0f61a9b
title: Controle GroupBox (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5182284055d95719299b1fecb7dc3f7825176c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164997"
---
# <a name="groupbox-control"></a>Controle GroupBox

O controle GroupBox exibe um retângulo, possivelmente com texto de legenda, que serve para agrupar outros controles juntos na caixa de diálogo.

## <a name="control-attributes"></a>Atributos de controle

Você pode usar os atributos a seguir com o controle GroupBox. Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent, na [tabela EventMappings](eventmapping-table.md) e liste o identificador do atributo na coluna atributo. Insira o identificador do ControlEvent, na coluna de evento.



| Identificador de atributo                               | Bit hexadecimal                  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Posição](position-control-attribute.md)         |                                  | Posição de controle na caixa de diálogo. Insira a largura, a altura e as coordenadas do controle do canto esquerdo do controle nas colunas largura, altura, X e Y da tabela de [controle](control-table.md) ou da [tabela BBControl](bbcontrol-table.md). Use [unidades de instalador](installer-units.md) para duração e distância.<br/>                                                                                                                         |
| [Text](text-control-attribute.md)                 |                                  | Exibe uma legenda no canto superior esquerdo do controle. Para definir a fonte e o estilo da fonte de uma cadeia de texto, Prefixe a cadeia de caracteres exibidos com { \\ Style} ou {&Style}. Em que Style é um identificador listado na coluna TextStyle da [tabela TextStyle](textstyle-table.md). Se nenhuma dessas opções estiver presente, mas a propriedade [**DefaultUIFont**](defaultuifont.md) for definida como um estilo de texto válido, essa fonte será usada.<br/> |
| [Visível](visible-control-attribute.md)           | 0x00000000 0x00000001<br/> | Controle oculto. Controle visível.<br/> Inclua esse bit na palavra de bits da coluna atributos na tabela de [controle](control-table.md) ou na [tabela BBControl](bbcontrol-table.md) para tornar o controle visível ou oculto após sua criação.<br/> Você também pode ocultar ou mostrar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                                                             |
| [Submersa](sunken-control-attribute.md)             | 0x00000000 0x00000004<br/> | Exibe o estilo visual padrão. Exibe o controle com uma aparência de baixo e 3-D.<br/> Inclua esses bits na palavra de bits na coluna atributos da tabela de [controle](control-table.md).<br/>                                                                                                                                                                                                                                               |
| [RTLRO](rtlro-control-attribute.md)               | 0x00000000 0x00000020<br/> | O texto no controle é exibido na ordem de leitura da esquerda para a direita. O texto no controle é exibido na ordem de leitura da direita para a esquerda.<br/>                                                                                                                                                                                                                                                                                                                |
| [RightAligned](rightaligned-control-attribute.md) | 0x00000000 0x00000040<br/> | O texto no controle é alinhado à esquerda. O texto no controle é alinhado à direita.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Comentários

Esse controle pode ser criado a partir da classe BUTTON usando a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Ele tem os estilos da caixa de grupo **BS \_**, **WS \_ Child** e **WS \_ Group** .

Sempre há uma lacuna entre a parte superior da janela do controle e o quadro visível, mesmo quando não há nenhuma legenda.

 

 
