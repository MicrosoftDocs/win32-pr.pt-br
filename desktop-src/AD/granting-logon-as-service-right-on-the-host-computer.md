---
title: Concedendo logon como serviço diretamente no computador host
description: Ao instalar um serviço para ser executado em uma conta de usuário de domínio, a conta deve ter o direito de fazer logon como um serviço no computador local.
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ef2bb87c3cf461e67cb7da20f36d9ac07fb362
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634939"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a>Concedendo logon como serviço diretamente no computador host

Ao instalar um serviço para ser executado em uma conta de usuário de domínio, a conta deve ter o direito de fazer logon como um serviço no computador local. Lembre-se de que esse direito de logon se aplica somente ao computador local e deve ser concedido na política LSA local de cada computador host. Essa etapa não será necessária se o serviço for executado como LocalSystem, que, por padrão, terá esse direito.

Para obter mais informações sobre como conceder programaticamente o direito de logon como um serviço, consulte o [código de exemplo LSAPrivs](https://www.google.com/#q=LSAPrivs).

 

 




