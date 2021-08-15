---
title: Usando uma conta de usuário local como uma conta de logon de serviço
description: Uma conta de usuário local (formato de nome \ 0034;. \\ UserName \ 0034;) existe somente no banco de dados SAM do computador host; ele não tem um objeto de usuário no Active Directory Domain Services.
ms.assetid: a36d4d1c-3cfc-4ae1-8f1d-3f2e766f0c4b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a6d536b83675cc3d4fa9c23db01d8f4137fff228bf72444bec7164a51068ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186851"
---
# <a name="using-a-local-user-account-as-a-service-logon-account"></a>Usando uma conta de usuário local como uma conta de logon de serviço

Uma conta de usuário local (formato de nome: ". \\ *UserName*") existe somente no banco de dados SAM do computador host; ele não tem um objeto de usuário no Active Directory Domain Services. Isso significa que uma conta local não pode ser autenticada pelo domínio. Consequentemente, um serviço executado no contexto de segurança de uma conta de usuário local não tem acesso aos recursos de rede (exceto como um usuário anônimo) e não pode dar suporte à autenticação mútua Kerberos na qual o serviço é autenticado por seus clientes. Por esses motivos, as contas de usuário local normalmente são inadequadas para serviços habilitados para diretório. No lado positivo, os bugs no serviço não podem danificar o sistema. Se o serviço puder ser executado com essas limitações, ele deverá.

 

 




