---
description: Os leitores são dispositivos padrão em um sistema de cartão inteligente. Eles são controlados por meio de drivers e são introduzidos e removidos do sistema por meio de Plug and Play ou por meio do item Painel de Controle Dispositivos.
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: Leitores de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 335aabe1d815e9b6d41ccfd820242209da63134797595d8a1c85f009f8551b7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917745"
---
# <a name="smart-card-readers"></a>Leitores de cartão inteligente

Os leitores são dispositivos padrão em um [*sistema de cartão*](../secgloss/s-gly.md) inteligente. Eles são controlados por meio de drivers e são introduzidos e removidos do sistema por meio de Plug and Play ou por meio do item Painel de Controle Dispositivos.

Cada leitor deve ser definido para uso pelo [*subsistema de cartão inteligente*](../secgloss/s-gly.md). O subsistema não é responsável por nenhum leitor não especificamente dado a ele.

Leitores de cartão inteligente podem ser divididos em grupos lógicos chamados grupos de leitores. Esses grupos podem ser definidos pelo subsistema , bem como definidos por administradores e usuários. Um leitor pode pertencer a mais de um grupo de leitores

O subsistema de cartão inteligente define os grupos a seguir.



| Grupo                | Descrição                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SCard$AllReaders     | Esse grupo contém todos os leitores no sistema. Um novo leitor dado ao subsistema de cartão inteligente é incluído automaticamente no grupo de leitores de todo o sistema, SCard$AllReaders.                         |
| SCard$DefaultReaders | Esse grupo padrão, um para cada [*terminal,*](../secgloss/t-gly.md)contém todos os leitores atribuídos ao terminal que não estão reservados para uso específico. |



 

 

 
