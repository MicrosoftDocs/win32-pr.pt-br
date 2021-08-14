---
title: DACLs nulas e DACLs vazias (AD DS)
description: A presença de uma DACL (lista de controle de acesso condicional) nula no atributo nTSecurityDescriptor de qualquer objeto pode criar um risco de segurança sério.
ms.assetid: 32b786d2-e676-4402-ad22-550de9289494
ms.tgt_platform: multiple
keywords:
- DACLs nulas e anúncios de DACLs vazios
- DACLs AD, NULL e Empty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41e03917c1190b7926eca11db038e2143bcb91d142e0617d143d4d80bb6e601
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185791"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a>DACLs nulas e DACLs vazias (AD DS)

A presença de uma DACL (lista de controle de acesso condicional) nula no atributo [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) de qualquer objeto pode criar um risco de segurança sério. Uma DACL nula concede acesso completo a qualquer usuário que o solicita; a verificação de segurança normal não é executada em relação ao objeto. Uma DACL nula não deve ser confundida com uma DACL vazia. Uma DACL vazia é uma DACL corretamente alocada e inicializada que não contém ACEs (entradas de controle de acesso). Uma DACL vazia não concede acesso ao objeto ao qual está atribuída.

Para obter mais informações, consulte [DACLs nulas e DACLs vazias](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).

 

 