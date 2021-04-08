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
ms.openlocfilehash: 2b841bb0253547fea291232fb4c9e6e0f3377d18
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917112"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a>DACLs nulas e DACLs vazias (AD DS)

A presença de uma DACL (lista de controle de acesso condicional) nula no atributo [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) de qualquer objeto pode criar um risco de segurança sério. Uma DACL nula concede acesso completo a qualquer usuário que o solicita; a verificação de segurança normal não é executada em relação ao objeto. Uma DACL nula não deve ser confundida com uma DACL vazia. Uma DACL vazia é uma DACL corretamente alocada e inicializada que não contém ACEs (entradas de controle de acesso). Uma DACL vazia não concede acesso ao objeto ao qual está atribuída.

Para obter mais informações, consulte [DACLs nulas e DACLs vazias](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).

 

 