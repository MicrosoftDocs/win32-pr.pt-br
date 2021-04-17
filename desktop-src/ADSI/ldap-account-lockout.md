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
# <a name="account-lockout-ldap-provider"></a><span data-ttu-id="0cc7b-106">Bloqueio de conta (provedor LDAP)</span><span class="sxs-lookup"><span data-stu-id="0cc7b-106">Account Lockout (LDAP Provider)</span></span>

<span data-ttu-id="0cc7b-107">Quando o número de tentativas de logon com falha for excedido, a conta de usuário será bloqueada por um período de tempo especificado pelo atributo [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) .</span><span class="sxs-lookup"><span data-stu-id="0cc7b-107">When the number of failed logon attempts is exceeded, the user account is locked out for a time period specified by the [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) attribute.</span></span> <span data-ttu-id="0cc7b-108">A propriedade [**IADsUser. IsAccountLocked**](iadsuser-property-methods.md) parece ser a propriedade a ser usada para ler e modificar o estado de bloqueio de uma conta de usuário, mas o provedor ADSI LDAP não dá suporte à propriedade **IsAccountLocked** com precisão.</span><span class="sxs-lookup"><span data-stu-id="0cc7b-108">The [**IADsUser.IsAccountLocked**](iadsuser-property-methods.md) property appears to be the property to use to read and modify the lockout state of a user account, but the LDAP ADSI provider does not accurately support the **IsAccountLocked** property.</span></span> <span data-ttu-id="0cc7b-109">Para obter e definir dados de bloqueio de conta precisos, use o provedor WinNT.</span><span class="sxs-lookup"><span data-stu-id="0cc7b-109">To obtain and set accurate account lockout data, use the WinNT provider.</span></span> <span data-ttu-id="0cc7b-110">Para obter mais informações sobre como usar a propriedade **IsAccountLocked** com o provedor WinNT, consulte [bloqueio de conta (provedor de winnt)](winnt-account-lockout.md).</span><span class="sxs-lookup"><span data-stu-id="0cc7b-110">For more information about using the **IsAccountLocked** property with the WinNT provider, see [Account Lockout (WinNT Provider)](winnt-account-lockout.md).</span></span>

 

 