---
description: O controle de mural exibe controles comumente usados que são adicionados e removidos da caixa de diálogo por ControlEvents.
ms.assetid: c4c0ed5a-2518-499f-805f-dcbe0b0f9393
title: Controle de mural
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e056a764ec4a71c3ce6785acf331b4bc1ff95ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828054"
---
# <a name="billboard-control"></a>Controle de mural

O controle de mural exibe controles comumente usados que são adicionados e removidos da caixa de diálogo por ControlEvents. Somente controles que não estão associados a uma propriedade, como [texto](text-control.md), [bitmap](bitmap-control.md)ou [ícone](icon-control.md), ou controles personalizados, podem ser colocados em um mural. Os controles de mensagem geralmente exibem mensagens de progresso.

## <a name="control-attributes"></a>Atributos de controle

Você pode usar os atributos a seguir com o controle de mural. Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent, na [tabela EventMappings](eventmapping-table.md) e liste o identificador do atributo na coluna atributo. Insira o identificador do ControlEvent, na coluna de evento.



| Identificador de atributo                                 | Bit hexadecimal                  | Descrição                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Muralname](billboardname-control-attribute.md) |                                  | Nome do mural atual. Insira o identificador do mural na coluna do mural da [tabela BBControl](bbcontrol-table.md).<br/>                                                                                                                                                                            |
| [Posição](position-control-attribute.md)           |                                  | Posição de controle na caixa de diálogo. Insira a largura, a altura e as coordenadas do controle do canto esquerdo do controle nas colunas largura, altura, X e Y da [tabela BBControl](bbcontrol-table.md). Use [unidades de instalador](installer-units.md) para duração e distância.<br/>                                |
| [Visível](visible-control-attribute.md)             | 0x00000000 0x00000001<br/> | Controle oculto. Controle visível.<br/> Inclua esse bit na palavra de bits da coluna atributos na [tabela BBControl](bbcontrol-table.md) para tornar o controle visível ou oculto após sua criação.<br/> Oculte ou mostre um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/> |
| [Submersa](sunken-control-attribute.md)               | 0x00000000 0x00000004<br/> | Exibe o estilo visual padrão. Exibe o controle com uma aparência de baixo e 3-D.<br/> Inclua esses bits na palavra de bits na coluna atributos da tabela de [controle](control-table.md).<br/>                                                                                                               |



 

## <a name="remarks"></a>Comentários

Este controle não tem nenhuma janela própria.

Os controles de mensagem que aparecem na interface do usuário completa são listados na [tabela do mural](billboard-table.md).

Os controles que estão localizados em um mural devem ser listados na [tabela BBControl](bbcontrol-table.md) em vez da [tabela de controle](control-table.md).

 

 




