---
description: A conta NetworkService é uma conta local predefinida usada pelo Gerenciador de controle de serviço.
ms.assetid: f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7
title: Conta NetworkService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c319518dbe925a146882014211d131c30420a282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756144"
---
# <a name="networkservice-account"></a><span data-ttu-id="8dab9-103">Conta NetworkService</span><span class="sxs-lookup"><span data-stu-id="8dab9-103">NetworkService Account</span></span>

<span data-ttu-id="8dab9-104">A conta NetworkService é uma conta local predefinida usada pelo Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="8dab9-104">The NetworkService account is a predefined local account used by the service control manager.</span></span> <span data-ttu-id="8dab9-105">Essa conta não é reconhecida pelo subsistema de segurança, portanto, você não pode especificar seu nome em uma chamada para a função [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) .</span><span class="sxs-lookup"><span data-stu-id="8dab9-105">This account is not recognized by the security subsystem, so you cannot specify its name in a call to the [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) function.</span></span> <span data-ttu-id="8dab9-106">Ele tem privilégios mínimos no computador local e atua como o computador na rede.</span><span class="sxs-lookup"><span data-stu-id="8dab9-106">It has minimum privileges on the local computer and acts as the computer on the network.</span></span>

<span data-ttu-id="8dab9-107">Essa conta pode ser especificada em uma chamada para as funções [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .</span><span class="sxs-lookup"><span data-stu-id="8dab9-107">This account can be specified in a call to the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) functions.</span></span> <span data-ttu-id="8dab9-108">Observe que essa conta não tem uma senha, portanto, qualquer informação de senha que você fornecer nessa chamada será ignorada.</span><span class="sxs-lookup"><span data-stu-id="8dab9-108">Note that this account does not have a password, so any password information that you provide in this call is ignored.</span></span> <span data-ttu-id="8dab9-109">Enquanto o subsistema de segurança localiza esse nome de conta, o SCM não oferece suporte a nomes localizados.</span><span class="sxs-lookup"><span data-stu-id="8dab9-109">While the security subsystem localizes this account name, the SCM does not support localized names.</span></span> <span data-ttu-id="8dab9-110">Portanto, você receberá um nome localizado para essa conta da função [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , mas o nome da conta deverá ser a Autoridade NT do \\ NetworkService quando você chamar **CreateService** ou **ChangeServiceConfig**, independentemente da localidade, ou pode ocorrer resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="8dab9-110">Therefore, you will receive a localized name for this account from the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function, but the name of the account must be NT AUTHORITY\\NetworkService when you call **CreateService** or **ChangeServiceConfig**, regardless of the locale, or unexpected results can occur.</span></span>

<span data-ttu-id="8dab9-111">Um serviço executado no contexto da conta NetworkService apresenta as credenciais do computador a servidores remotos.</span><span class="sxs-lookup"><span data-stu-id="8dab9-111">A service that runs in the context of the NetworkService account presents the computer's credentials to remote servers.</span></span> <span data-ttu-id="8dab9-112">Por padrão, o token remoto contém SIDs para os grupos todos e usuários autenticados.</span><span class="sxs-lookup"><span data-stu-id="8dab9-112">By default, the remote token contains SIDs for the Everyone and Authenticated Users groups.</span></span> <span data-ttu-id="8dab9-113">O SID do usuário é criado a partir do valor de **RID do serviço de rede de segurança \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="8dab9-113">The user SID is created from the **SECURITY\_NETWORK\_SERVICE\_RID** value.</span></span>

<span data-ttu-id="8dab9-114">A conta NetworkService tem sua própria subchave na chave do registro **HKEY \_ Users** .</span><span class="sxs-lookup"><span data-stu-id="8dab9-114">The NetworkService account has its own subkey under the **HKEY\_USERS** registry key.</span></span> <span data-ttu-id="8dab9-115">Portanto, a chave de registro **HKEY \_ Current \_ User** está associada à conta NetworkService.</span><span class="sxs-lookup"><span data-stu-id="8dab9-115">Therefore, the **HKEY\_CURRENT\_USER** registry key is associated with the NetworkService account.</span></span>

<span data-ttu-id="8dab9-116">A conta NetworkService tem os seguintes privilégios:</span><span class="sxs-lookup"><span data-stu-id="8dab9-116">The NetworkService account has the following privileges:</span></span>

-   <span data-ttu-id="8dab9-117">**Se \_ \_Nome do ASSIGNPRIMARYTOKEN** (desabilitado)</span><span class="sxs-lookup"><span data-stu-id="8dab9-117">**SE\_ASSIGNPRIMARYTOKEN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="8dab9-118">**Se \_ \_Nome da auditoria** (desabilitado)</span><span class="sxs-lookup"><span data-stu-id="8dab9-118">**SE\_AUDIT\_NAME** (disabled)</span></span>
-   <span data-ttu-id="8dab9-119">**Se \_ ALTERAR \_ \_ nome da notificação** (habilitado)</span><span class="sxs-lookup"><span data-stu-id="8dab9-119">**SE\_CHANGE\_NOTIFY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="8dab9-120">**Se \_ CRIAR \_ \_ nome global** (habilitado)</span><span class="sxs-lookup"><span data-stu-id="8dab9-120">**SE\_CREATE\_GLOBAL\_NAME** (enabled)</span></span>
-   <span data-ttu-id="8dab9-121">**Se \_ REPRESENTAR \_ nome** (habilitado)</span><span class="sxs-lookup"><span data-stu-id="8dab9-121">**SE\_IMPERSONATE\_NAME** (enabled)</span></span>
-   <span data-ttu-id="8dab9-122">**Se \_ AUMENTAR \_ o \_ nome da cota** (desabilitado)</span><span class="sxs-lookup"><span data-stu-id="8dab9-122">**SE\_INCREASE\_QUOTA\_NAME** (disabled)</span></span>
-   <span data-ttu-id="8dab9-123">**Se \_ \_Nome do DESligamento** (desabilitado)</span><span class="sxs-lookup"><span data-stu-id="8dab9-123">**SE\_SHUTDOWN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="8dab9-124">**Se \_ Desencaixar \_ nome** (desabilitado)</span><span class="sxs-lookup"><span data-stu-id="8dab9-124">**SE\_UNDOCK\_NAME** (disabled)</span></span>
-   <span data-ttu-id="8dab9-125">Quaisquer privilégios atribuídos a usuários e usuários autenticados</span><span class="sxs-lookup"><span data-stu-id="8dab9-125">Any privileges assigned to users and authenticated users</span></span>

<span data-ttu-id="8dab9-126">Para obter mais informações, consulte [segurança de serviço e direitos de acesso](service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="8dab9-126">For more information, see [Service Security and Access Rights](service-security-and-access-rights.md).</span></span>

 

 
