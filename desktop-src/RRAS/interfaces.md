---
title: Interfaces RAS
description: Uma interface representa uma rede que pode ser alcançada em um adaptador de LAN ou WAN.
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea285a625377709a4eca3bc8b9947106c2f5cfd
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103823478"
---
# <a name="ras-interfaces"></a>Interfaces RAS

Uma interface representa uma rede que pode ser alcançada em um adaptador de LAN ou WAN. Cada interface tem um identificador exclusivo no roteador. As interfaces que estão ativas têm um adaptador que está fornecendo conectividade à rede que elas representam. As interfaces inativas não têm um adaptador que fornece conectividade, a menos que um administrador tenha desabilitado a interface depois de ter um adaptador.

O roteamento de um pacote para uma rede representada por uma interface fará com que o roteador aloque um adaptador para essa interface e estabeleça uma conexão WAN com a rede remota. A alocação de um adaptador para uma interface é conhecida como *Associação*.

Interfaces são objetos gerenciáveis. Cada interface aparece como uma linha na tabela de interface da MIB SNMP apropriada.