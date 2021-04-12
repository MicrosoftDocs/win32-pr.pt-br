---
title: Sinalizadores de notificação de alteração
description: Sinalizadores de notificação de alteração
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- Alteração
- Sinalizadores de notificação de alteração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e6d3015be29c84b6b93b47b373d05f96f4388b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292262"
---
# <a name="change-notification-flags"></a>Sinalizadores de notificação de alteração



| Constante                         | Valor      | Descrição                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_tipos de \_ alteração de número RTM \_          | 3          | Especifica o número de tipos de alteração que são usados atualmente pelo Gerenciador de tabela de roteamento.                                                                            |
| tipo de alteração de RTM \_ \_ \_ tudo           | 0x0001     | Notifica o cliente sobre qualquer alteração em um destino.                                                                                                                   |
| \_ \_ melhor tipo de alteração de RTM \_          | 0x0002     | Notifica o cliente sobre as alterações na melhor rota ou quando a melhor rota é alterada.                                                                                     |
| \_ \_ encaminhamento de tipo de alteração RTM \_    | 0x0004     | Notifica o cliente sobre as melhores alterações de rota que afetam o encaminhamento (como alterações do próximo salto).                                                                      |
| o RTM \_ notifica \_ apenas os \_ \_ dests marcados | 0x00010000 | Notifica o cliente sobre as alterações nos destinos que o cliente marcou. Se esse sinalizador não for especificado, as mensagens de notificação de alteração para todos os destinos serão enviadas. |



 

 

 




