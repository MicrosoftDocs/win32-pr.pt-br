---
title: Autenticação (AD DS)
description: Cada objeto no Active Directory Domain Services tem um descritor de segurança exclusivo que define as permissões de acesso que são necessárias para ler ou atualizar o objeto ou suas propriedades individuais.
ms.assetid: a4a663d3-b0f3-4993-a74e-9e4f896e8c95
ms.tgt_platform: multiple
keywords:
- Active Directory, usando, associação, autenticação
- associando o AD de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb80bbca4604a99011d3198eaf6b3e871cd3f84c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453960"
---
# <a name="authentication-ad-ds"></a>Autenticação (AD DS)

Cada objeto no Active Directory Domain Services tem um descritor de segurança exclusivo que define as permissões de acesso que são necessárias para ler ou atualizar o objeto ou suas propriedades individuais. Os privilégios de acesso são determinados pelos direitos concedidos a uma conta de usuário ou a associações de grupo.

Quando um aplicativo é associado a um objeto no diretório, os privilégios de acesso que o aplicativo tem a esse objeto se baseiam no contexto de usuário especificado durante a operação de associação. Para as funções de associação e os métodos [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject), um aplicativo pode usar implicitamente as credenciais do chamador, especificar explicitamente as credenciais de uma conta de usuário ou usar um contexto de usuário não autenticado (convidado).

 

 