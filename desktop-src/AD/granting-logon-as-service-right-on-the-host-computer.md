---
title: Concedendo logon como direito de serviço no computador host
description: Ao instalar um serviço para ser executado em uma conta de usuário de domínio, a conta deve ter o direito de fazer logon como um serviço no computador local.
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef53e68feb9312bb8efdca285716aa5b6ea077e2e85f6c5538eb13532b51a8ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188950"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a>Concedendo logon como direito de serviço no computador host

Ao instalar um serviço para ser executado em uma conta de usuário de domínio, a conta deve ter o direito de fazer logon como um serviço no computador local. Esteja ciente de que esse direito de logon se aplica somente ao computador local e deve ser concedido na política LSA local de cada computador host. Essa etapa não será necessária se o serviço for executado como LocalSystem, que, por padrão, tem esse direito.

Para obter mais informações sobre como conceder programaticamente o logon como um direito de serviço, consulte o código de exemplo [LSAPrivs](https://www.google.com/#q=LSAPrivs).

 

 




