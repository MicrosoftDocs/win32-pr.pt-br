---
description: O controle hiperlink exibe um link HTML para um endereço, que é aberto no navegador padrão do computador.
ms.assetid: 06678b10-0915-4649-b917-ec90c40d5160
title: Controle de hiperlink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d074efa00fcf51fec979d9df07f1854631279d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828984"
---
# <a name="hyperlink-control"></a>Controle de hiperlink

O controle hiperlink exibe um link HTML para um endereço, que é aberto no navegador padrão do computador. Não há suporte para links para protocolos diferentes de HTML.

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. Esse controle está disponível a partir do Windows Installer 5,0.

O valor de texto do controle HyperLink usa a <a> marca Anchor e o valor do atributo href para especificar a URL e o texto exibido do link.

``` syntax
[Blue Yonder Airlines](https://www.blueyonderairlines.com)
```

## <a name="control-attributes"></a>Atributos de controle

Você pode usar os atributos a seguir com o controle HyperLink. Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent, na [tabela EventMappings](eventmapping-table.md) e liste o identificador do atributo na coluna atributo. Insira o identificador do ControlEvent, na coluna de evento.



| Identificador de atributo                             | Bit hexadecimal                  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Posição](position-control-attribute.md)       |                                  | Posição de controle na caixa de diálogo. Insira a largura, a altura e as coordenadas do controle do canto esquerdo do controle nas colunas largura, altura, X e Y da tabela de [controle](control-table.md) ou da [tabela BBControl](bbcontrol-table.md). Use [unidades de instalador](installer-units.md) para duração e distância.<br/>                                                                                                                                                                       |
| [Text](text-control-attribute.md)               |                                  | Texto exibido pelo controle. Para definir a fonte e o estilo da fonte de uma cadeia de texto, Prefixe a cadeia de caracteres exibidos com { \\ Style} ou {&Style}. Em que Style é um identificador listado na coluna TextStyle da [tabela TextStyle](textstyle-table.md). Se nenhuma dessas opções estiver presente, mas a propriedade [**DefaultUIFont**](defaultuifont.md) for definida como um estilo de texto válido, essa fonte será usada. O valor de texto também resolverá a \[ propriedade \] para a propriedade referenciada. <br/> |
| [Visível](visible-control-attribute.md)         | 0x00000000 0x00000001<br/> | Controle oculto. Controle visível.<br/> Inclua esse bit na palavra de bits da coluna atributos na tabela de [controle](control-table.md) ou na [tabela BBControl](bbcontrol-table.md). para tornar o controle visível ou oculto após sua criação.<br/> Você também pode ocultar ou mostrar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                                                                                                           |
| [Enabled](enabled-control-attribute.md)         | 0x00000000 0x00000002<br/> | Controle em um estado desabilitado. Controle em um estado habilitado.<br/> Inclua esse bit na palavra de bits na coluna atributos das tabelas [Control](control-table.md) ou [BBControl](bbcontrol-table.md) para habilitar o controle na criação.<br/> Você também pode habilitar ou desabilitar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                                                                                                        |
| [Submersa](sunken-control-attribute.md)           | 0x00000000 0x00000004<br/> | Exibe o estilo visual padrão. Exibe o controle com uma aparência de baixo e 3-D.<br/> Inclua esses bits na palavra de bits na coluna atributos da tabela de [controle](control-table.md).<br/>                                                                                                                                                                                                                                                                                            |
| [Transparente](transparent-control-attribute.md) | 0x00000000 0x00010000<br/> | Controle opaco. O plano de fundo mostra o controle. O controle tem o \_ \_ estilo transparente WS ex.<br/> Inclua esse bit na coluna Attributes das tabelas [Control](control-table.md) ou [BBControl](bbcontrol-table.md).<br/>                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentários

Esse controle pode ser criado a partir da \_ classe de link WC usando a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Ele tem os \_ estilos WS Child, WS \_ TabStop e WS \_ Group.

Não coloque controles de [texto](text-control.md) transparentes na parte superior dos bitmaps coloridos. O texto pode não estar visível se o usuário alterar o esquema de cores de exibição. Por exemplo, o texto pode se tornar invisível se o usuário definir o parâmetro de alto contraste por motivos de acessibilidade.

Se o texto no controle for maior que a largura do controle, o texto será quebrado ou truncado, dependendo se a altura for suficiente para se ajustar ao texto encapsulado.

 

 
