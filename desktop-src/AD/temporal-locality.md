---
title: Localidade temporal
description: A localidade temporal é uma estratégia de prevenção que reduz a janela para atualizações parciais.
ms.assetid: 8f454087-46cb-4fa6-b83a-65b2393029c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceecff05d031875178b6192e7c633f70e4c91c50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453494"
---
# <a name="temporal-locality"></a>Localidade temporal

A *localidade temporal* é uma estratégia de prevenção que reduz a janela para atualizações parciais. A replicação de alterações de uma determinada réplica de origem prossegue em ordem crescente de USN. As gravações que ocorrem em conjunto junto no tempo terão USNs que estão "perto" entre si e serão propagadas junto em tempo. Os aplicativos que criam ou atualizam vários objetos relacionados devem gravar os objetos o mais próximo possível do tempo possível. Por exemplo, o aplicativo pode reunir toda a entrada necessária do usuário e aplicá-la ao diretório quando o usuário clicar em um botão "aplicar".

A localidade temporal também reduz as chances de resolução de colisão introduzindo inconsistências dentro do objeto.

 

 




