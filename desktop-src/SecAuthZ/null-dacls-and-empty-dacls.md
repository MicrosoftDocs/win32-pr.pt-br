---
description: Uma DACL nula concede acesso completo a qualquer usuário que a solicite. Uma DACL vazia é uma DACL corretamente alocada e inicializada que não contém entradas de controle de acesso. Uma DACL vazia não concede acesso ao objeto ao qual está atribuída.
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: DACLs nulas e DACLs vazias (autorização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c06942d7b2d188a74b7e3e307cf60d6740a4251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754129"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a>DACLs nulas e DACLs vazias (autorização)

Se a DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) que pertence ao [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) de um objeto for definida como **NULL**, uma DACL nula será criada. Uma DACL nula concede acesso completo a qualquer usuário que o solicita; a verificação de segurança normal não é executada em relação ao objeto. Uma DACL nula não deve ser confundida com uma DACL vazia. Uma DACL vazia é uma DACL corretamente alocada e inicializada que não contém ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ). Uma DACL vazia não concede acesso ao objeto ao qual está atribuída.

Para obter um exemplo de como criar uma DACL, consulte [criando uma DACL](/windows/desktop/SecBP/creating-a-dacl).

 

 
