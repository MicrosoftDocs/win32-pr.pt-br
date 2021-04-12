---
description: O controle ícone exibe uma imagem estática de um ícone. O plano de fundo da imagem é transparente.
ms.assetid: a2d19093-73d0-4e1f-bf82-21e7334a3f34
title: Controle de ícone (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a9bf90697ff3a839c1953918179fb8cf41f2809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501361"
---
# <a name="icon-control"></a>Controle de ícone

O controle ícone exibe uma imagem estática de um ícone. O plano de fundo da imagem é transparente.

## <a name="control-attributes"></a>Atributos de controle

Você pode usar os atributos a seguir com este controle. Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent, na [tabela EventMappings](eventmapping-table.md) e liste o identificador do atributo na coluna atributo. Insira o identificador do ControlEvent, na coluna de evento.



| Identificador de atributo                         | Bit hexadecimal                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Posição](position-control-attribute.md)   |                                                                              | Posição de controle na caixa de diálogo. Insira a largura, a altura e as coordenadas do controle do canto esquerdo do controle nas colunas largura, altura, X e Y da [tabela de controle](control-table.md). Use [unidades de instalador](installer-units.md) para duração e distância.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [Text](text-control-attribute.md)           |                                                                              | Contém o nome de um ícone armazenado na [tabela binária](binary-table.md). Para exibir um ícone que é armazenado na tabela binária, insira o nome do registro da imagem que aparece na tabela binária na coluna de texto do registro da [tabela de controle](control-table.md) deste controle.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [Visível](visible-control-attribute.md)     | 0x00000000 0x00000001<br/>                                             | Controle oculto. Controle visível.<br/> Inclua esse bit na palavra de bits da coluna atributos na tabela de [controle](control-table.md) para tornar o controle visível ou oculto após sua criação.<br/> Você também pode ocultar ou mostrar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                                                                                                                                                         |
| [Submersa](sunken-control-attribute.md)       | 0x00000000 0x00000004<br/>                                             | Exibe o estilo visual padrão. Exibe o controle com uma aparência de baixo e 3-D.<br/> Inclua esses bits na palavra de bits na coluna atributos da tabela de [controle](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [FixedSize](fixedsize-control-attribute.md) | 0x00000000 0x00100000<br/>                                             | Alonga a imagem do ícone para ajustá-la ao controle. Corta ou centraliza a imagem do ícone no controle.<br/> Inclua esse bit na palavra bit da coluna atributos da [tabela de controle](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [Ícones de](iconsize-control-attribute.md)   | 0x00000000 0x00200000<br/> 0x00400000<br/> 0x00600000<br/> | Carrega a primeira imagem. Carrega a primeira imagem 16x16.<br/> Carrega a primeira imagem 32x32.<br/> Carrega a primeira imagem 48x48.<br/> Um arquivo de ícone pode conter imagens de tamanho diferentes do mesmo ícone. Inclua o valor da palavra de bits apropriada na coluna atributos da tabela de [controle](control-table.md)<br/> Se esses bits não estiverem definidos, o instalador ignorará o atributo FixedSize e a imagem será ampliada para se ajustar ao retângulo de controle. Se os bits de ícones e os bits FixedSize estiverem definidos, uma imagem menor do que o controle será centralizado e uma imagem será maior do que o controle para o qual será reduzido.<br/> |



 

## <a name="remarks"></a>Comentários

Esse controle pode ser criado a partir da classe estática usando a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Ele tem o **\_ ícone SS**, **SS \_ CENTERIMAGE**, **WS \_ Child** e **WS \_ Group** Styles.

 

 
