---
title: O que você pode saber e quando você pode conhecê-lo
description: Os aplicativos que são sensíveis a Estados induzidos por latência devem reconhecer Estados de problemas e tomar as devidas ações.
ms.assetid: d1d0135e-2d67-47dd-82ac-4869203ce85e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a8a6c6def8475946ad5faa63615d17742fbcb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105753665"
---
# <a name="what-can-you-know-and-when-can-you-know-it"></a>O que você pode saber e quando você pode conhecê-lo?

Os aplicativos que são sensíveis a Estados induzidos por latência devem reconhecer Estados de problemas e tomar as devidas ações. Há dois Estados de problema: distorção de versão e atualização parcial. A distorção de versão não é detectável examinando o serviço de diretório (Lembre-se do axioma de computação distribuída declarado em [por que Active Directory Domain Services usar esse modelo de replicação](why-active-directory-domain-services-uses-this-replication-model.md)). A atualização parcial pode ser detectada adicionando metadados aos objetos que compõem o conjunto relacionado. As sugestões para esses metadados aparecem nas seções subsequentes deste documento. Há estratégias de prevenção que os aplicativos podem tomar para reduzir a possibilidade de distorção de versão e atualização parcial. Essas estratégias também são discutidas nas seções subsequentes deste documento.

 

 




