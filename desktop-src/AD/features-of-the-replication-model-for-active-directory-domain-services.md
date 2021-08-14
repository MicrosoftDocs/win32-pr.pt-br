---
title: Recursos do modelo de replicação para Active Directory Domain Services
description: O modelo de replicação usado Active Directory Domain Services é chamado de consistência de vários mestres com convergência.
ms.assetid: 8fd63871-68b4-4ed6-8165-145cbc90c213
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, modelo de replicação
- Recursos do modelo de replicação do Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd113ffe4182be47c9e8c84404fc748e417e78c866e41298ad19d8e7a0dec555
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189527"
---
# <a name="features-of-the-replication-model-for-active-directory-domain-services"></a>Recursos do modelo de replicação para Active Directory Domain Services

O modelo de replicação usado Active Directory Domain Services é chamado de consistência de vários *mestres com convergência.* Nesse modelo, o diretório pode ter muitas réplicas; um sistema de replicação propaga as alterações feitas em qualquer réplica determinada para todas as outras réplicas. Não há garantia de que as réplicas sejam consistentes umas com as outras em qualquer momento específico ("consistência livre"), pois as alterações podem ser aplicadas a qualquer réplica a qualquer momento ("vários mestres"). Se o sistema tiver permissão para alcançar um estado estável, no qual nenhuma nova atualização está ocorrendo e todas as atualizações anteriores foram completamente replicadas, todas as réplicas têm garantia de convergir no mesmo conjunto de valores ("convergência").

 

 




