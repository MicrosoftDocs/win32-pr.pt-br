---
title: Alterar sinalizadores de notificação
description: Alterar sinalizadores de notificação
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- Alteração
- Alterar sinalizadores de notificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f5311e3313bf23c92972395143d288483181e7a69212115082a2f150d7d1bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791830"
---
# <a name="change-notification-flags"></a>Alterar sinalizadores de notificação



| Constante                         | Valor      | Descrição                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TIPOS DE ALTERAÇÃO \_ DE NUM \_ RTM \_          | 3          | Especifica o número de tipos de alteração que são usados atualmente pelo gerenciador de tabelas de roteamento.                                                                            |
| RTM \_ CHANGE \_ TYPE \_ ALL           | 0x0001     | Notifica o cliente de qualquer alteração em um destino.                                                                                                                   |
| TIPO DE ALTERAÇÃO RTM \_ \_ \_ MELHOR          | 0x0002     | Notifica o cliente de alterações na melhor rota ou quando a melhor rota é muda.                                                                                     |
| ENCAMINHAMENTO DE \_ TIPO \_ DE ALTERAÇÃO \_ RTM    | 0x0004     | Notifica o cliente sobre as melhores alterações de rota que afetam o encaminhamento (como alterações do próximo salto).                                                                      |
| RTM \_ NOTIFY \_ ONLY \_ MARKED \_ DESTS | 0x00010000 | Notifica o cliente de alterações nos destinos que o cliente marcou. Se esse sinalizador não for especificado, as mensagens de notificação de alteração para todos os destinos serão enviadas. |



 

 

 




