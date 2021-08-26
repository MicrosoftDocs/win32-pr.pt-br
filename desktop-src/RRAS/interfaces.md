---
title: Interfaces RAS
description: Uma interface representa uma rede que pode ser alcançada em um adaptador de LAN ou WAN.
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef716e0db05fe37a0a7d326fbf5f8da878a0628d1deec9e996fcc49d917cc051
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030136"
---
# <a name="ras-interfaces"></a>Interfaces RAS

Uma interface representa uma rede que pode ser alcançada em um adaptador de LAN ou WAN. Cada interface tem um identificador exclusivo no roteador. As interfaces que estão ativas têm um adaptador que está fornecendo conectividade à rede que elas representam. As interfaces inativas não têm um adaptador que fornece conectividade, a menos que um administrador tenha desabilitado a interface depois de ter um adaptador.

O roteamento de um pacote para uma rede representada por uma interface fará com que o roteador aloque um adaptador para essa interface e estabeleça uma conexão WAN com a rede remota. A alocação de um adaptador para uma interface é conhecida como *Associação*.

Interfaces são objetos gerenciáveis. Cada interface aparece como uma linha na tabela de interface da MIB SNMP apropriada.