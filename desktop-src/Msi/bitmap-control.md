---
description: O controle bitmap exibe um bitmap ou um arquivo de imagem estática JPEG. o Windows Installer determinará automaticamente o formato dos dados binários e exibirá a imagem. O controle não oferece suporte à animação.
ms.assetid: 4b511d8a-1819-4a9b-a942-dc32fade75c6
title: Controle de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f677a7745d3920d5fee44cd64489f9f2c69f8cdb1fb697a0020046a92583e569
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045226"
---
# <a name="bitmap-control"></a>Controle de bitmap

O controle bitmap exibe um bitmap ou um arquivo de imagem estática JPEG. o Windows Installer determinará automaticamente o formato dos dados binários e exibirá a imagem. O controle não oferece suporte à animação.

**Windows 8 e Windows Server 2012:** o arquivo de imagem pode estar em qualquer formato padrão com suporte pelo componente de Windows Imaging (WIC), incluindo TIFF, JPEG, PNG, GIF, BMP e HDPhoto. O controle não oferece suporte à animação.

## <a name="control-attributes"></a>Atributos de controle

Você pode usar os atributos a seguir com este controle. Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent, na [tabela EventMappings](eventmapping-table.md) e liste o identificador do atributo na coluna atributo. Insira o identificador do ControlEvent, na coluna de evento.



| Identificador de atributo                                 | Bit hexadecimal                  | Descrição                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Posição](position-control-attribute.md)           |                                  | Posição do controle na caixa de diálogo. Insira a largura, a altura e as coordenadas do controle do canto esquerdo do controle nas colunas largura, altura, X e Y da tabela de [controle](control-table.md) ou da [tabela BBControl](bbcontrol-table.md). Use [unidades de instalador](installer-units.md) para duração e distância.<br/>                                         |
| [Text](text-control-attribute.md)                   |                                  | Contém o nome de um bitmap armazenado na [tabela binária](binary-table.md). Para exibir um bitmap armazenado na tabela binária, faça o seguinte. Insira o nome da imagem de bitmap que aparece na coluna nome da tabela binária na coluna de texto do registro da [tabela de controle](control-table.md) deste controle. <br/>                                         |
| [Visível](visible-control-attribute.md)             | 0x00000000 0x00000001<br/> | Controle oculto. Controle visível.<br/> Inclua esse bit na palavra de bits da coluna atributos na tabela de [controle](control-table.md) ou na [tabela BBControl](bbcontrol-table.md). para tornar o controle visível ou oculto após sua criação.<br/> Você também pode ocultar ou mostrar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/> |
| [Submersa](sunken-control-attribute.md)               | 0x00000000 0x00000004<br/> | Exibe o estilo visual padrão. Exibe o controle com uma aparência de baixo e 3-D.<br/> Inclua esses bits na palavra de bits na coluna atributos da tabela de [controle](control-table.md).<br/>                                                                                                                                                                   |
| [Controle FixedSize](fixedsize-control-attribute.md) | 0x00000000 0x00100000<br/> | Alonga a imagem de bitmap para ajustá-la ao controle. Corta ou centraliza a imagem de bitmap no controle.<br/> Inclua esse bit na palavra bit da coluna Attributes da [tabela BBControl](bbcontrol-table.md) ou da tabela de [controle](control-table.md).<br/>                                                                                                       |



 

## <a name="remarks"></a>Comentários

Esse controle pode ser criado a partir da classe estática usando a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Ele tem os estilos de **\_ grupo** **\_ bitmap SS**, **SS \_ CENTERIMAGE**, **WS \_ Child** e WS.

 

