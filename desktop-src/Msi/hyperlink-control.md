---
description: O controle Hiperlink exibe um link HTML para um endereço, que é aberto no navegador padrão do computador.
ms.assetid: 06678b10-0915-4649-b917-ec90c40d5160
title: Controle de hiperlink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce515b64a518012ea187eb2c3a933e653b1ea5cf99b316028f9cfe3b397c5f96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129456"
---
# <a name="hyperlink-control"></a>Controle de hiperlink

O controle Hiperlink exibe um link HTML para um endereço, que é aberto no navegador padrão do computador. Não há suporte para links para protocolos que não sejam HTML.

**[Windows Instalador 4.5 ou anterior:](not-supported-in-windows-installer-4-5.md)** Sem suporte. Esse Controle está disponível a partir do Windows Instalador 5.0.

O valor Text do controle HyperLink usa a marca de âncora e o valor do atributo HREF para especificar a URL e <a> o texto exibido do link.

``` syntax
[Blue Yonder Airlines](https://www.blueyonderairlines.com)
```

## <a name="control-attributes"></a>Atributos de controle

Você pode usar os atributos a seguir com o controle Hiperlink. Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent na tabela [EventMapping](eventmapping-table.md) e liste o identificador do atributo na coluna Atributo. Insira o identificador do ControlEvent na coluna Evento.



| Identificador de atributo                             | Bit hexadecimal                  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Posição](position-control-attribute.md)       |                                  | Posição do controle na caixa de diálogo. Insira a largura, a altura e as coordenadas do canto esquerdo do controle nas colunas Width, Height, X e Y da tabela [Control](control-table.md) ou [BBControl](bbcontrol-table.md). Use [unidades do instalador](installer-units.md) para comprimento e distância.<br/>                                                                                                                                                                       |
| [Text](text-control-attribute.md)               |                                  | Texto exibido pelo controle . Para definir o estilo de fonte e fonte de uma cadeia de caracteres de texto, prefixe a cadeia de caracteres exibida com { style} ou \\ {&style}. Em que style é um identificador listado na coluna TextStyle da [tabela TextStyle](textstyle-table.md). Se nenhum deles estiver presente, mas a [**propriedade DefaultUIFont**](defaultuifont.md) for definida como um estilo de texto válido, essa fonte será usada. O valor de texto também \[ resolverá Property \] para a propriedade referenciada. <br/> |
| [Visível](visible-control-attribute.md)         | 0x00000000 0x00000001<br/> | Controle oculto. Controle visível.<br/> Inclua esse bit na palavra bit da coluna Atributos na tabela [Control](control-table.md) ou na tabela [BBControl](bbcontrol-table.md).para tornar o controle visível ou oculto após sua criação.<br/> Você também pode ocultar ou mostrar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                                                                                                           |
| [Habilitada](enabled-control-attribute.md)         | 0x00000000 0x00000002<br/> | Controle em um estado desabilitado. Controle em um estado habilitado.<br/> Inclua esse bit na palavra bit na coluna Atributos das tabelas [Control](control-table.md) ou [BBControl](bbcontrol-table.md) para habilitar o controle na criação.<br/> Você também pode habilitar ou desabilitar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                                                                                                        |
| [Afundado](sunken-control-attribute.md)           | 0x00000000 0x00000004<br/> | Exibe o estilo visual padrão. Exibe o controle com um esquente, 3D, look.<br/> Inclua esses bits na palavra bit na coluna Atributos da [tabela Controle](control-table.md).<br/>                                                                                                                                                                                                                                                                                            |
| [Transparente](transparent-control-attribute.md) | 0x00000000 0x00010000<br/> | Controle opaco. A plano de fundo é mostra por meio do controle . O controle tem o estilo TRANSPARENTE do WS \_ \_ EX.<br/> Inclua esse bit na coluna Atributos das [tabelas Control](control-table.md) ou [BBControl](bbcontrol-table.md).<br/>                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentários

Esse controle pode ser criado a partir da classe WC \_ LINK usando a função [**CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Ele tem os estilos WS \_ CHILD, WS \_ TABSTOP e WS \_ GROUP.

Não coloque controles [de Texto transparentes](text-control.md) sobre bitmaps coloridos. O texto poderá não ficar visível se o usuário mudar o esquema de cores de exibição. Por exemplo, o texto pode se tornar invisível se o usuário define o parâmetro de alto contraste por motivos de acessibilidade.

Se o texto no controle for maior que a largura do controle, o texto será empacotado ou truncado, dependendo se a altura for suficiente para se ajustar ao texto empacotado.

 

 
