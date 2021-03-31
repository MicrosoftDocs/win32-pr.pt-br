---
title: Tipo de botão
description: Tipo de botão
ms.assetid: 0c9e72d5-5cc4-4d6f-b184-2c8c8487e366
keywords:
- Aparências móveis do Windows Media Player, tipos de botão
- capas, tipos de botão
- referência para capas, botões
- botões em capas, tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58eeb7402a13730fd7f4030d2e4326fe7f18e63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822401"
---
# <a name="button-type"></a>Tipo de botão

Os botões vêm em dois tipos gerais: local e região. Cada tipo geral tem três tipos específicos, fazendo seis tipos de botão.

> [!Note]  
> Os tipos de botões são preteridos em capas para Windows Media Player 10 Mobile ou posterior.

 

Tipos de botão de localização

Os botões de localização usam coordenadas para definir seus locais em relação ao plano de fundo. A tabela a seguir mostra os valores válidos para os tipos de botão de localização. Não é necessário definir valores para tipos que você não usará em sua capa.



| Valor  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Push   | Define um botão que dispara um evento uma vez. O botão deve ser enviado a cada vez para disparar outros eventos. Um exemplo seria um botão que se move para o próximo item na lista de reprodução. O local do botão é definido por suas coordenadas.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Alternar | Define um botão que dispara um evento que altera um estado. O estado permanece até que o botão seja enviado novamente. Um exemplo é um botão que embaralha a lista de reprodução. Depois que a playlist estiver em um estado em ordem aleatória, ela permanecerá em ordem aleatória até que o botão seja enviado novamente. O local do botão é definido por suas coordenadas.                                                                                                                                                                                                                                                                                                                                                           |
| 2Push  | Define um botão que dispara um evento e, em seguida, muda para um estado que está pronto para disparar um evento diferente. Os dois Estados são alternados toda vez que o botão é enviado por push. Um exemplo é um botão que usa a função **PlayPause** para alternar entre reproduzir e pausar o item de mídia atual. Quando o botão é enviado pela primeira vez, o estado de execução primário é disparado e uma imagem secundária é exibida para indicar que um evento de **pausa** pode ser disparado. Quando o botão é colocado novamente, o estado de pausa é disparado e a imagem original é exibida para indicar que um evento de **reprodução** pode ser disparado. O local do botão é definido por suas coordenadas. |



 

Tipos de botão de região

Os botões de região usam áreas de cores na imagem de região para definir onde os toques serão processados para um determinado botão. A tabela a seguir mostra os valores válidos para os tipos de botão de região. Não é necessário definir valores para tipos que você não usará em sua capa.



| Valor     | Descrição                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| PushHit   | Semelhante ao valor do botão de ação, exceto que a área de pressionamento do botão é definida pelo valor de cor na imagem da região.   |
| ToggleHit | Semelhante ao valor do botão de alternância, exceto que a área de pressionamento do botão é definida pelo valor de cor na imagem da região. |
| 2PushHit  | Semelhante ao valor do botão 2Push, exceto que a área de pressionamento do botão é definida pelo valor de cor na imagem da região.  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Botões**](buttons.md)
</dt> </dl>

 

 




