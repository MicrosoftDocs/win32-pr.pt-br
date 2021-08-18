---
description: O controle Ícone exibe uma imagem estática de um ícone. A plano de fundo da imagem é transparente.
ms.assetid: a2d19093-73d0-4e1f-bf82-21e7334a3f34
title: Controle de ícone (Windows Instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce6d1dca9e6664018a0c7a36c9b44f3b5a0b6310bc8c6d18309b73649fa9240
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996706"
---
# <a name="icon-control"></a>Controle de ícone

O controle Ícone exibe uma imagem estática de um ícone. A plano de fundo da imagem é transparente.

## <a name="control-attributes"></a>Atributos de controle

Você pode usar os atributos a seguir com esse controle. Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent na tabela [EventMapping](eventmapping-table.md) e liste o identificador do atributo na coluna Atributo. Insira o identificador do ControlEvent na coluna Evento.



| Identificador de atributo                         | Bit hexadecimal                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Posição](position-control-attribute.md)   |                                                                              | Posição do controle na caixa de diálogo. Insira a largura, a altura e as coordenadas do canto esquerdo do controle nas colunas Width, Height, X e Y da [tabela Control](control-table.md). Use [unidades do instalador](installer-units.md) para comprimento e distância.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [Text](text-control-attribute.md)           |                                                                              | Contém o nome de um ícone armazenado na [tabela Binária](binary-table.md). Para exibir um ícone armazenado na tabela Binário, insira o nome do registro da imagem que aparece [](control-table.md) na tabela Binário na coluna Texto do registro da tabela Controle para esse controle.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [Visível](visible-control-attribute.md)     | 0x00000000 0x00000001<br/>                                             | Controle oculto. Controle visível.<br/> Inclua esse bit na palavra bit da coluna Atributos na tabela [Controle](control-table.md) para tornar o controle visível ou oculto após sua criação.<br/> Você também pode ocultar ou mostrar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                                                                                                                                                         |
| [Afundado](sunken-control-attribute.md)       | 0x00000000 0x00000004<br/>                                             | Exibe o estilo visual padrão. Exibe o controle com uma aparência 3D e esquente.<br/> Inclua esses bits na palavra bit na coluna Atributos da [tabela Controle](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [Fixedsize](fixedsize-control-attribute.md) | 0x00000000 0x00100000<br/>                                             | Alonga a imagem do ícone para se ajustar ao controle. Resimos ou centraliza a imagem de ícone no controle .<br/> Inclua esse bit na palavra bit da coluna Atributos da [tabela Controle](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [Iconsize](iconsize-control-attribute.md)   | 0x00000000 0x00200000<br/> 0x00400000<br/> 0x00600000<br/> | Carrega a primeira imagem. Carrega a primeira imagem 16x16.<br/> Carrega a primeira imagem 32x32.<br/> Carrega a primeira imagem 48x48.<br/> Um arquivo de ícone pode conter imagens de tamanho diferentes do mesmo ícone. Incluir o valor da palavra de bit apropriada na coluna Atributos da [tabela Controle](control-table.md)<br/> Se esses bits não estão definidos, o instalador ignora o atributo FixedSize e a imagem é alongada para se ajustar ao retângulo de controle. Se os bits IconSize e FixedSize estão definidos, uma imagem menor do que o controle é centralizada e uma imagem é maior do que o controle que é reduzido para ajustar.<br/> |



 

## <a name="remarks"></a>Comentários

Esse controle pode ser criado com a classe STATIC usando a [**função CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Ele tem os **estilos SS \_ ICON,** **SS \_ CENTERIMAGE,** **WS \_ CHILD** e **WS \_ GROUP.**

 

 
