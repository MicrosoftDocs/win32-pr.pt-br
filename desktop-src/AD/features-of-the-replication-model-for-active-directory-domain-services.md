---
title: Recursos do modelo de replicação para Active Directory Domain Services
description: O modelo de replicação usado em Active Directory Domain Services é chamado de consistência de vários mestres flexíveis com convergência.
ms.assetid: 8fd63871-68b4-4ed6-8165-145cbc90c213
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, modelo de replicação
- Recursos de modelo de replicação Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923c49dd648063ebd6afd086be3729f28f1e4080
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105753041"
---
# <a name="features-of-the-replication-model-for-active-directory-domain-services"></a>Recursos do modelo de replicação para Active Directory Domain Services

O modelo de replicação usado em Active Directory Domain Services é chamado de *consistência de vários mestres flexíveis com convergência*. Nesse modelo, o diretório pode ter muitas réplicas; um sistema de replicação propaga as alterações feitas em qualquer réplica específica para todas as outras réplicas. Não há garantia de que as réplicas sejam consistentes entre si em um determinado momento ("consistência flexível"), pois as alterações podem ser aplicadas a qualquer réplica a qualquer momento ("vários mestres"). Se o sistema tiver permissão para alcançar um estado estável, no qual nenhuma nova atualização está ocorrendo e todas as atualizações anteriores foram completamente replicadas, todas as réplicas terão a garantia de convergir no mesmo conjunto de valores ("convergência").

 

 




