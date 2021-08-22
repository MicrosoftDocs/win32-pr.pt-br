---
description: O provedor de registro do sistema tenta enviar uma notificação para cada evento que ocorre.
ms.assetid: 51ef0ccb-02d5-4dac-9c71-a7f4e25a0d00
ms.tgt_platform: multiple
title: Recebendo eventos do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6f3c8f39be30beeb64e7c8d8ff7f1bacfba8a47b7f4bd0c70e7cf638bf726e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817452"
---
# <a name="receiving-registry-events"></a>Recebendo eventos do registro

O provedor de registro do sistema tenta enviar uma notificação para cada evento que ocorre. No entanto, o provedor de registro do sistema não garante que o consumidor receberá um ou todos os eventos. A exceção é que o provedor de registro do sistema garante que um consumidor receberá uma notificação para cada registro de evento.

Por exemplo, suponha que um consumidor se registre em dois eventos de alteração de árvore, solicitando notificação para instâncias de [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) . Cada registro tem o mesmo valor de Hive (subárvore), mas um valor diferente de RootPath. Se as chaves em ambos os caminhos forem alteradas várias vezes, o provedor de registro do sistema garante que o consumidor receberá uma notificação para cada caminho. Dependendo do tempo de resposta do registro e do provedor de registro do sistema, o consumidor pode receber tantas notificações quanto houve ocorrências de eventos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando para eventos de registro do sistema](registering-for-system-registry-events.md)
</dt> </dl>

 

 
