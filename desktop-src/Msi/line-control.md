---
description: O controle linha é uma linha horizontal.
ms.assetid: 8b180b71-1e80-47c0-bb44-d5fcecabaed2
title: Controle linha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb4dc02db9c701c0c5156a0e3f3e15a039893bae290fc7e8bee7dfce64f2eb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763486"
---
# <a name="line-control"></a>Controle linha

O controle linha é uma linha horizontal.

## <a name="control-attributes"></a>Atributos de controle

Você pode usar os atributos a seguir com este controle. Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent, na [tabela EventMappings](eventmapping-table.md) e liste o identificador do atributo na coluna atributo. Insira o identificador do ControlEvent, na coluna de evento.



| Identificador de atributo                       | Bit hexadecimal                  | Descrição                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Posição](position-control-attribute.md) |                                  | Posição do controle na caixa de diálogo. Insira a largura, a altura e as coordenadas do controle do canto esquerdo do controle nas colunas largura, altura, X e Y da tabela de [controle](control-table.md) ou da [tabela BBControl](bbcontrol-table.md). Use [unidades de instalador](installer-units.md) para duração e distância.<br/>                                         |
| [Visível](visible-control-attribute.md)   | 0x00000000 0x00000001<br/> | Controle oculto. Controle visível.<br/> Inclua esse bit na palavra de bits da coluna atributos na tabela de [controle](control-table.md) ou na [tabela BBControl](bbcontrol-table.md) para tornar o controle visível ou oculto após sua criação.<br/> Você também pode ocultar ou mostrar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/> |
| [Submersa](sunken-control-attribute.md)     | 0x00000000 0x00000004<br/> | Exibe o estilo visual padrão. Exibe o controle com uma aparência de baixo e 3-D.<br/> Inclua esses bits na palavra de bits na coluna atributos da tabela de [controle](control-table.md).<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Comentários

Esse controle pode ser criado a partir da classe estática usando a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Ele tem os estilos **SS \_ ETCHEDHORZ** e **SS \_ relevo** .

 

 
