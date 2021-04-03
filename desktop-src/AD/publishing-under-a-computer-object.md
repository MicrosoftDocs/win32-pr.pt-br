---
title: Publicação em um objeto de computador
description: Normalmente, os serviços baseados em host criam SCPs sob o objeto de computador para o computador host. Os serviços baseados em host são serviços fortemente vinculados a um único computador host.
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fe382001910f3b78b4461c622e94b14c54fb59
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823637"
---
# <a name="publishing-under-a-computer-object"></a>Publicação em um objeto de computador

Normalmente, os serviços baseados em host criam SCPs sob o objeto de computador para o computador host. Os serviços baseados em host são serviços fortemente vinculados a um único computador host.

**Para criar SCPs em um objeto de computador**

1.  Chame a função [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) para obter o DN (nome distinto) no diretório do objeto de computador do computador local.
2.  Use esse DN para associar ao objeto de computador e criar o SCP.

Para obter mais informações e um exemplo de código, consulte [como os clientes encontram e usam um ponto de conexão de serviço](how-clients-find-and-use-a-service-connection-point.md).

Lembre-se de que somente computadores membros do domínio têm objetos de computador válidos no diretório.

Para obter o nome DNS ou NetBIOS do computador local, chame a função [**GetComputerNameEx devia**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) .

 

 