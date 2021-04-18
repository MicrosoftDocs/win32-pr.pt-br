---
description: Os leitores são dispositivos padrão em um sistema de cartão inteligente. Eles são controlados por meio de drivers e são introduzidos e removidos do sistema por meio de Plug and Play ou por meio do item dispositivos do painel de controle.
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: Leitores de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6f4f5c4d1d487f136fb25052d44659f4b073bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748958"
---
# <a name="smart-card-readers"></a>Leitores de cartão inteligente

Os leitores são dispositivos padrão em um sistema de [*cartão inteligente*](../secgloss/s-gly.md) . Eles são controlados por meio de drivers e são introduzidos e removidos do sistema por meio de Plug and Play ou por meio do item dispositivos do painel de controle.

Cada leitor deve ser definido para ser usado pelo [*subsistema de cartão inteligente*](../secgloss/s-gly.md). O subsistema não é responsável por nenhum leitor especificamente fornecido a ele.

Os leitores de cartão inteligente podem ser divididos em grupos lógicos chamados grupos de leitores. Esses grupos podem ser definidos pelo subsistema, bem como definidos por administradores e usuários. Um leitor pode pertencer a mais de um grupo de leitores

O subsistema de cartão inteligente define os grupos a seguir.



| Grupo                | Descrição                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Scartar $ webreaders     | Esse grupo contém todos os leitores do sistema. Um novo leitor fornecido ao subsistema de cartão inteligente é incluído automaticamente no grupo de leitores de todo o sistema, Scartar $ rowgroup.                         |
| Scartar $ defaultreadrs | Esse grupo padrão, um para cada [*terminal*](../secgloss/t-gly.md), contém todos os leitores atribuídos ao terminal que não estão reservados para uso específico. |



 

 

 
