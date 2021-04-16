---
description: A conta LocalService é uma conta local predefinida usada pelo Gerenciador de controle de serviço.
ms.assetid: 5409e2fe-a349-4739-a481-f8a35fd3c9b4
title: Conta do LocalService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67051b95d6e5d18179bb2dc69928e68edb0f3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506132"
---
# <a name="localservice-account"></a><span data-ttu-id="40bbf-103">Conta do LocalService</span><span class="sxs-lookup"><span data-stu-id="40bbf-103">LocalService Account</span></span>

<span data-ttu-id="40bbf-104">A conta LocalService é uma conta local predefinida usada pelo Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="40bbf-104">The LocalService account is a predefined local account used by the service control manager.</span></span> <span data-ttu-id="40bbf-105">Ele tem privilégios mínimos no computador local e apresenta credenciais anônimas na rede.</span><span class="sxs-lookup"><span data-stu-id="40bbf-105">It has minimum privileges on the local computer and presents anonymous credentials on the network.</span></span>

<span data-ttu-id="40bbf-106">Essa conta pode ser especificada em uma chamada para as funções [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .</span><span class="sxs-lookup"><span data-stu-id="40bbf-106">This account can be specified in a call to the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) functions.</span></span> <span data-ttu-id="40bbf-107">Observe que essa conta não tem uma senha, portanto, qualquer informação de senha que você fornecer nessa chamada será ignorada.</span><span class="sxs-lookup"><span data-stu-id="40bbf-107">Note that this account does not have a password, so any password information that you provide in this call is ignored.</span></span> <span data-ttu-id="40bbf-108">Enquanto o subsistema de segurança localiza esse nome de conta, o SCM não oferece suporte a nomes localizados.</span><span class="sxs-lookup"><span data-stu-id="40bbf-108">While the security subsystem localizes this account name, the SCM does not support localized names.</span></span> <span data-ttu-id="40bbf-109">Portanto, você receberá um nome localizado para essa conta da função [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , mas o nome da conta deverá ser a Autoridade NT \\ LocalService quando você chamar **CreateService** ou **ChangeServiceConfig**, independentemente da localidade, ou podem ocorrer resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="40bbf-109">Therefore, you will receive a localized name for this account from the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function, but the name of the account must be NT AUTHORITY\\LocalService when you call **CreateService** or **ChangeServiceConfig**, regardless of the locale, or unexpected results can occur.</span></span>

<span data-ttu-id="40bbf-110">O SID de usuário é criado com base no valor de **\_ \_ \_ RID do serviço local de segurança** .</span><span class="sxs-lookup"><span data-stu-id="40bbf-110">The user SID is created from the **SECURITY\_LOCAL\_SERVICE\_RID** value.</span></span>

<span data-ttu-id="40bbf-111">A conta LocalService tem sua própria subchave na chave do registro **HKEY \_ Users** .</span><span class="sxs-lookup"><span data-stu-id="40bbf-111">The LocalService account has its own subkey under the **HKEY\_USERS** registry key.</span></span> <span data-ttu-id="40bbf-112">Portanto, a chave de registro **HKEY \_ Current \_ User** está associada à conta LocalService.</span><span class="sxs-lookup"><span data-stu-id="40bbf-112">Therefore, the **HKEY\_CURRENT\_USER** registry key is associated with the LocalService account.</span></span>

<span data-ttu-id="40bbf-113">A conta LocalService tem os seguintes privilégios:</span><span class="sxs-lookup"><span data-stu-id="40bbf-113">The LocalService account has the following privileges:</span></span>

-   <span data-ttu-id="40bbf-114">**Se \_ \_Nome do ASSIGNPRIMARYTOKEN** (desabilitado)</span><span class="sxs-lookup"><span data-stu-id="40bbf-114">**SE\_ASSIGNPRIMARYTOKEN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="40bbf-115">**Se \_ \_Nome da auditoria** (desabilitado)</span><span class="sxs-lookup"><span data-stu-id="40bbf-115">**SE\_AUDIT\_NAME** (disabled)</span></span>
-   <span data-ttu-id="40bbf-116">**Se \_ ALTERAR \_ \_ nome da notificação** (habilitado)</span><span class="sxs-lookup"><span data-stu-id="40bbf-116">**SE\_CHANGE\_NOTIFY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="40bbf-117">**Se \_ CRIAR \_ \_ nome global** (habilitado)</span><span class="sxs-lookup"><span data-stu-id="40bbf-117">**SE\_CREATE\_GLOBAL\_NAME** (enabled)</span></span>
-   <span data-ttu-id="40bbf-118">**Se \_ REPRESENTAR \_ nome** (habilitado)</span><span class="sxs-lookup"><span data-stu-id="40bbf-118">**SE\_IMPERSONATE\_NAME** (enabled)</span></span>
-   <span data-ttu-id="40bbf-119">**Se \_ AUMENTAR \_ o \_ nome da cota** (desabilitado)</span><span class="sxs-lookup"><span data-stu-id="40bbf-119">**SE\_INCREASE\_QUOTA\_NAME** (disabled)</span></span>
-   <span data-ttu-id="40bbf-120">**Se \_ \_Nome do DESligamento** (desabilitado)</span><span class="sxs-lookup"><span data-stu-id="40bbf-120">**SE\_SHUTDOWN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="40bbf-121">**Se \_ Desencaixar \_ nome** (desabilitado)</span><span class="sxs-lookup"><span data-stu-id="40bbf-121">**SE\_UNDOCK\_NAME** (disabled)</span></span>
-   <span data-ttu-id="40bbf-122">Quaisquer privilégios atribuídos a usuários e usuários autenticados</span><span class="sxs-lookup"><span data-stu-id="40bbf-122">Any privileges assigned to users and authenticated users</span></span>

<span data-ttu-id="40bbf-123">Para obter mais informações, consulte [segurança de serviço e direitos de acesso](service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="40bbf-123">For more information, see [Service Security and Access Rights](service-security-and-access-rights.md).</span></span>

 

 
