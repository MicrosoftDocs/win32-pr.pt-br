---
title: Bloqueio de conta (provedor LDAP)
description: Quando o número de tentativas de logon com falha for excedido, a conta de usuário será bloqueada por um período de tempo especificado pelo atributo lockoutDuration.
ms.assetid: bf86f6ac-8209-4306-8736-99ce53c93617
ms.tgt_platform: multiple
keywords:
- ADSI do bloqueio de conta (provedor LDAP)
- ADSI de bloqueio de conta, provedor LDAP
- ADSI do provedor LDAP, exemplos de gerenciamento de usuário, bloqueio de conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b7a25943debfd08469ce9a28463c88159ded9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105769078"
---
# <a name="account-lockout-ldap-provider"></a>Bloqueio de conta (provedor LDAP)

Quando o número de tentativas de logon com falha for excedido, a conta de usuário será bloqueada por um período de tempo especificado pelo atributo [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) . A propriedade [**IADsUser. IsAccountLocked**](iadsuser-property-methods.md) parece ser a propriedade a ser usada para ler e modificar o estado de bloqueio de uma conta de usuário, mas o provedor ADSI LDAP não dá suporte à propriedade **IsAccountLocked** com precisão. Para obter e definir dados de bloqueio de conta precisos, use o provedor WinNT. Para obter mais informações sobre como usar a propriedade **IsAccountLocked** com o provedor WinNT, consulte [bloqueio de conta (provedor de winnt)](winnt-account-lockout.md).

 

 