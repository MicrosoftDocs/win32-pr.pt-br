---
description: Une um sistema de computador a um domínio ou grupo de trabalho.
ms.assetid: b9421f04-9b56-4413-af5c-12dffeb6f0c8
ms.tgt_platform: multiple
title: Método JoinDomainOrWorkgroup da classe Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.JoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 927dd6b2664c92ff07e94407fdc59fdd917363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826593"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a><span data-ttu-id="c20d5-103">Método JoinDomainOrWorkgroup da classe Win32 \_ ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="c20d5-103">JoinDomainOrWorkgroup method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="c20d5-104">O método **JoinDomainOrWorkgroup** une um sistema de computador a um domínio ou grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c20d5-104">The **JoinDomainOrWorkgroup** method joins a computer system to a domain or workgroup.</span></span>

<span data-ttu-id="c20d5-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c20d5-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c20d5-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c20d5-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c20d5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c20d5-107">Syntax</span></span>


```mof
uint32 JoinDomainOrWorkgroup(
  [in] string Name,
  [in] string Password,
  [in] string UserName,
  [in] string AccountOU,
  [in] uint32 FJoinOptions = 
);
```



## <a name="parameters"></a><span data-ttu-id="c20d5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c20d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c20d5-109">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c20d5-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-110">Especifica o domínio ou grupo de trabalho a ser associado.</span><span class="sxs-lookup"><span data-stu-id="c20d5-110">Specifies the domain or workgroup to join.</span></span> <span data-ttu-id="c20d5-111">Não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c20d5-111">Cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c20d5-112">*Senha* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c20d5-112">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-113">Se o parâmetro *username* especificar um nome de conta, o parâmetro *password* deverá apontar para a senha a ser usada na conexão com o controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="c20d5-113">If the *UserName* parameter specifies an account name, the *Password* parameter must point to the password to use when connecting to the domain controller.</span></span> <span data-ttu-id="c20d5-114">Caso contrário, esse parâmetro deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c20d5-114">Otherwise, this parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c20d5-115">*Nome de usuário* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c20d5-115">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-116">Ponteiro para uma cadeia de caracteres constante terminada em **nulo** que especifica o nome da conta a ser usada ao conectar-se ao controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="c20d5-116">Pointer to a constant **null**-terminated character string that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="c20d5-117">É necessário especificar um nome NetBIOS de domínio e uma conta de usuário, por exemplo, usuário de domínio \\ .</span><span class="sxs-lookup"><span data-stu-id="c20d5-117">Must specify a domain NetBIOS name and user account, for example, Domain\\user.</span></span> <span data-ttu-id="c20d5-118">Se esse parâmetro for **nulo**, as informações do chamador serão usadas.</span><span class="sxs-lookup"><span data-stu-id="c20d5-118">If this parameter is **NULL**, the caller information is used.</span></span>

<span data-ttu-id="c20d5-119">Você também pode usar o nome principal do usuário (UPPED) no formulário user@domain .</span><span class="sxs-lookup"><span data-stu-id="c20d5-119">You can also use the user principal name (UPPED) in the form user@domain.</span></span>

</dd> <dt>

<span data-ttu-id="c20d5-120">*AccountOU* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c20d5-120">*AccountOU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-121">Especifica o ponteiro para uma cadeia de caracteres constante terminada em **nulo** que contém o nome do formato [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) da unidade organizacional (UO) da conta do computador.</span><span class="sxs-lookup"><span data-stu-id="c20d5-121">Specifies the pointer to a constant **null**-terminated character string that contains the [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) format name of the organizational unit (OU) for the computer account.</span></span> <span data-ttu-id="c20d5-122">Se você especificar esse parâmetro, a cadeia de caracteres deverá conter um caminho completo; caso contrário, o *acento* deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c20d5-122">If you specify this parameter, the string must contain a full path, otherwise *Accent* must be **NULL**.</span></span>

<span data-ttu-id="c20d5-123">Exemplo: "OU = testOU; DC = Domain; DC = Domain; DC = com "</span><span class="sxs-lookup"><span data-stu-id="c20d5-123">Example: "OU=testOU; DC=domain; DC=Domain; DC=com"</span></span>

</dd> <dt>

<span data-ttu-id="c20d5-124">*FJoinOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c20d5-124">*FJoinOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-125">Conjunto de sinalizadores de bits que definem as opções de junção.</span><span class="sxs-lookup"><span data-stu-id="c20d5-125">Set of bit flags that define the join options.</span></span>

<dt>



 <span data-ttu-id="c20d5-126"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="c20d5-126">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c20d5-127">Padrão.</span><span class="sxs-lookup"><span data-stu-id="c20d5-127">Default.</span></span> <span data-ttu-id="c20d5-128">Nenhuma opção de junção.</span><span class="sxs-lookup"><span data-stu-id="c20d5-128">No join options.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span data-ttu-id="c20d5-129"><span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>INSTALAÇÃO do NET **\_ INGRESSAr no \_ domínio** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="c20d5-129"><span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**NETSETUP\_JOIN\_DOMAIN** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="c20d5-130">Une o computador a um domínio.</span><span class="sxs-lookup"><span data-stu-id="c20d5-130">Joins the computer to a domain.</span></span> <span data-ttu-id="c20d5-131">Se esse valor não for especificado, o ingressará o computador em um grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c20d5-131">If this value is not specified, joins the computer to a workgroup.</span></span>

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span data-ttu-id="c20d5-132"><span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>INSTALAÇÃO do NET **\_ \_Create de acct** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="c20d5-132"><span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**NETSETUP\_ACCT\_CREATE** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="c20d5-133">Cria a conta no domínio.</span><span class="sxs-lookup"><span data-stu-id="c20d5-133">Creates the account on the domain.</span></span>

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span data-ttu-id="c20d5-134"><span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>INSTALAÇÃO do NET **\_ \_Atualização do Win9x** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="c20d5-134"><span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**NETSETUP\_WIN9X\_UPGRADE** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="c20d5-135">A operação de junção está ocorrendo como parte de uma atualização.</span><span class="sxs-lookup"><span data-stu-id="c20d5-135">The join operation is occurring as part of an upgrade.</span></span>

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span data-ttu-id="c20d5-136"><span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>INSTALAÇÃO do NET **\_ Ingresso no domínio \_ \_ se \_ Unido** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="c20d5-136"><span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**NETSETUP\_DOMAIN\_JOIN\_IF\_JOINED** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="c20d5-137">Permite uma junção a um novo domínio, mesmo que o computador já tenha ingressado em um domínio.</span><span class="sxs-lookup"><span data-stu-id="c20d5-137">Allows a join to a new domain even if the computer is already joined to a domain.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span data-ttu-id="c20d5-138"><span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>INSTALAÇÃO do NET **\_ JUNÇÃO \_ não segura** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="c20d5-138"><span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**NETSETUP\_JOIN\_UNSECURE** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="c20d5-139">Executa uma junção não segura.</span><span class="sxs-lookup"><span data-stu-id="c20d5-139">Performs an unsecured join.</span></span>

<span data-ttu-id="c20d5-140">Esta opção solicita um ingresso no domínio para uma conta criada previamente sem autenticação com credenciais de usuário do domínio.</span><span class="sxs-lookup"><span data-stu-id="c20d5-140">This option requests a domain join to a pre-created account without authenticating with domain user credentials.</span></span> <span data-ttu-id="c20d5-141">Essa opção pode ser usada em conjunto com a opção de **instalação do \_ computador \_ pwd \_ aprovada** .</span><span class="sxs-lookup"><span data-stu-id="c20d5-141">This option can be used in conjunction with **NETSETUP\_MACHINE\_PWD\_PASSED** option.</span></span> <span data-ttu-id="c20d5-142">Nesse caso, *password* é a senha da conta de máquina criada previamente.</span><span class="sxs-lookup"><span data-stu-id="c20d5-142">In this case, *Password* is the password of the pre-created machine account.</span></span>

<span data-ttu-id="c20d5-143">Antes do Windows Vista com SP1 e do Windows Server 2008, uma junção não segura não se autenticou no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="c20d5-143">Prior to Windows Vista with SP1 and Windows Server 2008, an unsecure join did not authenticate to the domain controller.</span></span> <span data-ttu-id="c20d5-144">Toda a comunicação foi executada usando uma sessão nula (não autenticada).</span><span class="sxs-lookup"><span data-stu-id="c20d5-144">All communication was performed using a null (unauthenticated) session.</span></span> <span data-ttu-id="c20d5-145">A partir do Windows Vista com SP1 e do Windows Server 2008, o nome da conta de computador e a senha são usados para autenticar no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="c20d5-145">Starting with Windows Vista with SP1 and Windows Server 2008, the machine account name and password are used to authenticate to the domain controller.</span></span>

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span data-ttu-id="c20d5-146"><span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>INSTALAÇÃO do NET **\_ PWD do computador \_ \_ aprovado** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="c20d5-146"><span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**NETSETUP\_MACHINE\_PWD\_PASSED** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="c20d5-147">Indica que o parâmetro de *senha* especifica uma senha de conta de computador local, em vez de uma senha de usuário.</span><span class="sxs-lookup"><span data-stu-id="c20d5-147">Indicates that the *Password* parameter specifies a local machine account password rather than a user password.</span></span> <span data-ttu-id="c20d5-148">Esse sinalizador é válido somente para junções não seguras, que você deve indicar, definindo também o \_ sinalizador de junção não segura do Netsetup \_ .</span><span class="sxs-lookup"><span data-stu-id="c20d5-148">This flag is valid only for unsecured joins, which you must indicate by also setting the NETSETUP\_JOIN\_UNSECURE flag.</span></span>

<span data-ttu-id="c20d5-149">Se você definir esse sinalizador, depois que a operação de junção for concluída com sucesso, a senha do computador será definida como o valor de *senha*, se esse valor for uma senha de computador válida.</span><span class="sxs-lookup"><span data-stu-id="c20d5-149">If you set this flag, then after the join operation succeeds, the machine password will be set to the value of *Password*, if that value is a valid machine password.</span></span>

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span data-ttu-id="c20d5-150"><span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>INSTALAÇÃO do NET **\_ ADIAr \_ \_ conjunto de SPN** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="c20d5-150"><span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**NETSETUP\_DEFER\_SPN\_SET** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="c20d5-151">Indica que o SPN (nome da entidade de serviço) e as propriedades de DnsHostName no objeto de computador não devem ser atualizados no momento.</span><span class="sxs-lookup"><span data-stu-id="c20d5-151">Indicates that the service principal name (SPN) and the DnsHostName properties on the computer object should not be updated at this time.</span></span>

<span data-ttu-id="c20d5-152">Normalmente, essas propriedades são atualizadas durante a operação de junção.</span><span class="sxs-lookup"><span data-stu-id="c20d5-152">Typically, these properties are updated during the join operation.</span></span> <span data-ttu-id="c20d5-153">Em vez disso, essas propriedades devem ser atualizadas durante uma chamada subsequente para o método [**Rename**](rename-method-in-class-win32-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="c20d5-153">Instead, these properties should be updated during a subsequent call to the [**Rename**](rename-method-in-class-win32-computersystem.md) method.</span></span> <span data-ttu-id="c20d5-154">Essas propriedades são sempre atualizadas durante a operação de renomeação.</span><span class="sxs-lookup"><span data-stu-id="c20d5-154">These properties are always updated during the rename operation.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span data-ttu-id="c20d5-155"><span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>INSTALAÇÃO do NET **\_ INGRESSAr na \_ \_ conta DC** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="c20d5-155"><span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**NETSETUP\_JOIN\_DC\_ACCOUNT** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="c20d5-156">Permitir ingresso no domínio se a conta existente for um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="c20d5-156">Allow the domain join if existing account is a domain controller.</span></span>

> [!Note]  
> <span data-ttu-id="c20d5-157">Esse sinalizador tem suporte no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="c20d5-157">This flag is supported on Windows Vista and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span data-ttu-id="c20d5-158"><span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>INSTALAÇÃO do NET **\_ \_DC ambíguo** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="c20d5-158"><span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**NETSETUP\_AMBIGUOUS\_DC** (0x00001000)</span></span>


</dt> <dd>

<span data-ttu-id="c20d5-159">Ao ingressar no domínio, não tente definir o controlador de domínio preferencial no registro.</span><span class="sxs-lookup"><span data-stu-id="c20d5-159">When joining the domain don't try to set the preferred domain controller in the registry.</span></span>

> [!Note]  
> <span data-ttu-id="c20d5-160">Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.</span><span class="sxs-lookup"><span data-stu-id="c20d5-160">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span data-ttu-id="c20d5-161"><span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>INSTALAÇÃO do NET **\_ NENHUM \_ \_ cache Netlogon** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="c20d5-161"><span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**NETSETUP\_NO\_NETLOGON\_CACHE** (0x00002000)</span></span>


</dt> <dd>

<span data-ttu-id="c20d5-162">Ao ingressar no domínio, não crie o cache Netlogon.</span><span class="sxs-lookup"><span data-stu-id="c20d5-162">When joining the domain don't create the Netlogon cache.</span></span>

> [!Note]  
> <span data-ttu-id="c20d5-163">Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.</span><span class="sxs-lookup"><span data-stu-id="c20d5-163">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span data-ttu-id="c20d5-164"><span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>INSTALAÇÃO do NET **\_ Não 0x00004000 ( \_ \_ serviços de controle** )</span><span class="sxs-lookup"><span data-stu-id="c20d5-164"><span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**NETSETUP\_DONT\_CONTROL\_SERVICES** (0x00004000)</span></span>


</dt> <dd>

<span data-ttu-id="c20d5-165">Ao ingressar no domínio, não force o início do serviço Netlogon.</span><span class="sxs-lookup"><span data-stu-id="c20d5-165">When joining the domain don't force Netlogon service to start.</span></span>

> [!Note]  
> <span data-ttu-id="c20d5-166">Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.</span><span class="sxs-lookup"><span data-stu-id="c20d5-166">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span data-ttu-id="c20d5-167"><span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>INSTALAÇÃO do NET **\_ DEFINIR \_ \_ nome do computador** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="c20d5-167"><span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**NETSETUP\_SET\_MACHINE\_NAME** (0x00008000)</span></span>


</dt> <dd>

<span data-ttu-id="c20d5-168">Ao ingressar no domínio somente para junção offline, defina nome de host do computador de destino e NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="c20d5-168">When joining the domain for offline join only, set target machine hostname and NetBIOS name.</span></span>

> [!Note]  
> <span data-ttu-id="c20d5-169">Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.</span><span class="sxs-lookup"><span data-stu-id="c20d5-169">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span data-ttu-id="c20d5-170"><span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>INSTALAÇÃO do NET **\_ FORÇAR \_ \_ conjunto de SPN** (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="c20d5-170"><span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**NETSETUP\_FORCE\_SPN\_SET** (0x00010000)</span></span>


</dt> <dd>

<span data-ttu-id="c20d5-171">Ao ingressar no domínio, substitua outras configurações durante o ingresso no domínio e defina o SPN (nome da entidade de serviço).</span><span class="sxs-lookup"><span data-stu-id="c20d5-171">When joining the domain, override other settings during domain join and set the service principal name (SPN).</span></span>

> [!Note]  
> <span data-ttu-id="c20d5-172">Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.</span><span class="sxs-lookup"><span data-stu-id="c20d5-172">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span data-ttu-id="c20d5-173"><span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>INSTALAÇÃO do NET **\_ NENHUMA \_ \_ reutilização de acct** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="c20d5-173"><span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**NETSETUP\_NO\_ACCT\_REUSE** (0x00020000)</span></span>


</dt> <dd>

<span data-ttu-id="c20d5-174">Ao ingressar no domínio, não reutilize uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="c20d5-174">When joining the domain, do not reuse an existing account.</span></span>

> [!Note]  
> <span data-ttu-id="c20d5-175">Esse sinalizador tem suporte no Windows 7, Windows Server 2008 R2 e posterior.</span><span class="sxs-lookup"><span data-stu-id="c20d5-175">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span data-ttu-id="c20d5-176"><span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>INSTALAÇÃO do NET **\_ IGNORAR \_ \_ sinalizadores sem suporte** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="c20d5-176"><span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**NETSETUP\_IGNORE\_UNSUPPORTED\_FLAGS** (0x10000000)</span></span>


</dt> <dd>

<span data-ttu-id="c20d5-177">Se esse bit for definido, os sinalizadores não reconhecidos serão ignorados pela função **JoinDomainOrWorkgroup** e [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) se comportará como se os sinalizadores não fossem definidos.</span><span class="sxs-lookup"><span data-stu-id="c20d5-177">If this bit is set, unrecognized flags will be ignored by the **JoinDomainOrWorkgroup** function and [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) will behave as if the flags were not set.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c20d5-178">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c20d5-178">Return value</span></span>

<span data-ttu-id="c20d5-179">Retorna um [código de erro do sistema](/windows/desktop/Debug/system-error-codes), que pode incluir um dos valores numéricos a seguir.</span><span class="sxs-lookup"><span data-stu-id="c20d5-179">Returns a [system error code](/windows/desktop/Debug/system-error-codes), which may include one of the following numeric values.</span></span> <span data-ttu-id="c20d5-180">Qualquer outro número indica um erro.</span><span class="sxs-lookup"><span data-stu-id="c20d5-180">Any other number indicates an error.</span></span> <span data-ttu-id="c20d5-181">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c20d5-181">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="c20d5-182">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="c20d5-182">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-183">0</span><span class="sxs-lookup"><span data-stu-id="c20d5-183">0</span></span>

</dd> <dt>

<span data-ttu-id="c20d5-184">**5**</span><span class="sxs-lookup"><span data-stu-id="c20d5-184">**5**</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-185">O acesso foi negado.</span><span class="sxs-lookup"><span data-stu-id="c20d5-185">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="c20d5-186">**87**</span><span class="sxs-lookup"><span data-stu-id="c20d5-186">**87**</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-187">O parâmetro está incorreto.</span><span class="sxs-lookup"><span data-stu-id="c20d5-187">The parameter is incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="c20d5-188">**110**</span><span class="sxs-lookup"><span data-stu-id="c20d5-188">**110**</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-189">o sistema não pode abrir o objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="c20d5-189">he system cannot open the specified object.</span></span>

</dd> <dt>

<span data-ttu-id="c20d5-190">**1323**</span><span class="sxs-lookup"><span data-stu-id="c20d5-190">**1323**</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-191">Não é possível atualizar a senha.</span><span class="sxs-lookup"><span data-stu-id="c20d5-191">Unable to update the password.</span></span>

</dd> <dt>

<span data-ttu-id="c20d5-192">**1326**</span><span class="sxs-lookup"><span data-stu-id="c20d5-192">**1326**</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-193">Falha de logon: nome de usuário desconhecido ou senha inadequada.</span><span class="sxs-lookup"><span data-stu-id="c20d5-193">Logon failure: unknown username or bad password.</span></span>

</dd> <dt>

<span data-ttu-id="c20d5-194">**1355**</span><span class="sxs-lookup"><span data-stu-id="c20d5-194">**1355**</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-195">O domínio especificado não existe ou não pôde ser contatado.</span><span class="sxs-lookup"><span data-stu-id="c20d5-195">The specified domain either does not exist or could not be contacted.</span></span>

</dd> <dt>

<span data-ttu-id="c20d5-196">**2224**</span><span class="sxs-lookup"><span data-stu-id="c20d5-196">**2224**</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-197">A conta já existe.</span><span class="sxs-lookup"><span data-stu-id="c20d5-197">The account already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c20d5-198">**2691**</span><span class="sxs-lookup"><span data-stu-id="c20d5-198">**2691**</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-199">O computador já ingressou no domínio.</span><span class="sxs-lookup"><span data-stu-id="c20d5-199">The machine is already joined to the domain.</span></span>

</dd> <dt>

<span data-ttu-id="c20d5-200">**2692**</span><span class="sxs-lookup"><span data-stu-id="c20d5-200">**2692**</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-201">O computador não está atualmente associado a um domínio.</span><span class="sxs-lookup"><span data-stu-id="c20d5-201">The machine is not currently joined to a domain.</span></span>

</dd> <dt>

<span data-ttu-id="c20d5-202">**conexão de WBEM \_ E \_ criptografada \_ \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="c20d5-202">**WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-203">0x80041087</span><span class="sxs-lookup"><span data-stu-id="c20d5-203">0x80041087</span></span>

<span data-ttu-id="c20d5-204">A *senha* e o *nome de usuário* são especificados, mas o nível de autenticação não é do **RPC \_ C \_ Authn \_ nível de \_ \_ privacidade de PCT**.</span><span class="sxs-lookup"><span data-stu-id="c20d5-204">*Password* and *UserName* are specified but the authentication level is not **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="c20d5-205">Por Visual Basic, **wbemErrEncryptedConnectionRequired** é retornado.</span><span class="sxs-lookup"><span data-stu-id="c20d5-205">For Visual Basic, **wbemErrEncryptedConnectionRequired** is returned.</span></span>

</dd> <dt>

<span data-ttu-id="c20d5-206">**Outras**</span><span class="sxs-lookup"><span data-stu-id="c20d5-206">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="c20d5-207">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="c20d5-207">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c20d5-208">Comentários</span><span class="sxs-lookup"><span data-stu-id="c20d5-208">Remarks</span></span>

<span data-ttu-id="c20d5-209">Ao mover um computador de um domínio para um grupo de trabalho, você deve remover o computador do domínio (com uma chamada para [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) antes de chamar esse método para ingressar em um grupo de trabalho (com uma chamada para **JoinDomainOrWorkgroup**).</span><span class="sxs-lookup"><span data-stu-id="c20d5-209">When moving a computer from a domain to a workgroup, you must remove the computer from the domain (with a call to [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) before calling this method to join a workgroup (with a call to **JoinDomainOrWorkgroup**).</span></span> <span data-ttu-id="c20d5-210">Depois de chamar esse método, reinicie o computador afetado para aplicar as alterações.</span><span class="sxs-lookup"><span data-stu-id="c20d5-210">After calling this method, restart the affected computer to apply the changes.</span></span>

<span data-ttu-id="c20d5-211">O *nome de usuário* e a *senha* podem ser **nulos**.</span><span class="sxs-lookup"><span data-stu-id="c20d5-211">*UserName* and *Password* can be left **null**.</span></span> <span data-ttu-id="c20d5-212">No entanto, a autenticação da conexão com o WMI deve ser 6 em script ou **WbemAuthenticationLevelPktPrivacy** no Visual Basic e em outras linguagens que podem usar a biblioteca de [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) .</span><span class="sxs-lookup"><span data-stu-id="c20d5-212">However, the authentication of the connection to WMI must be 6 in script or **WbemAuthenticationLevelPktPrivacy** in Visual Basic and other languages that can use the [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) library.</span></span> <span data-ttu-id="c20d5-213">Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando o VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).</span><span class="sxs-lookup"><span data-stu-id="c20d5-213">For more information, see [Setting the Default Process Security Level Using VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).</span></span>

<span data-ttu-id="c20d5-214">Em C++, defina a autenticação na **\_ privacidade do \_ PCT do \_ nível \_ \_ de autenticação do RPC C** em [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), para todo o processo ou em [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), para uma conexão com o proxy de [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="c20d5-214">In C++, set the authentication at **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** either in [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), for the entire process, or in [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), for a connection to the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) proxy.</span></span> <span data-ttu-id="c20d5-215">Para obter mais informações, consulte [definindo a autenticação usando C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) e [definindo a segurança em IWbemServices e em outros proxies](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).</span><span class="sxs-lookup"><span data-stu-id="c20d5-215">For more information, see [Setting Authentication Using C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) and [Setting the Security on IWbemServices and Other Proxies](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).</span></span>

## <a name="examples"></a><span data-ttu-id="c20d5-216">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c20d5-216">Examples</span></span>

<span data-ttu-id="c20d5-217">O exemplo [ingressar um computador em um domínio](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) do PowerShell une um computador a um domínio.</span><span class="sxs-lookup"><span data-stu-id="c20d5-217">The [Join a computer to a domain](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell example joins a computer to a domain.</span></span>

<span data-ttu-id="c20d5-218">O exemplo de código VBScript a seguir une um computador a um domínio e cria a conta do computador no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c20d5-218">The following VBScript code example joins a computer to a domain and creates the computer's account in Active Directory.</span></span>


```VB
Const JOIN_DOMAIN             = 1
Const ACCT_CREATE             = 2
Const ACCT_DELETE             = 4
Const WIN9X_UPGRADE           = 16
Const DOMAIN_JOIN_IF_JOINED   = 32
Const JOIN_UNSECURE           = 64
Const MACHINE_PASSWORD_PASSED = 128
Const DEFERRED_SPN_SET        = 256
Const INSTALL_INVOCATION      = 262144
strDomain   = "FABRIKAM"
strPassword = "ls4k5ywA"
strUser     = "shenalan"
Set objNetwork = CreateObject("WScript.Network")
strComputer = objNetwork.ComputerName
Set objComputer = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & _
                            "\root\cimv2:Win32_ComputerSystem.Name='" & strComputer & "'")
ReturnValue = objComputer.JoinDomainOrWorkGroup(strDomain, _
                                                strPassword, _
                                                strDomain & "\" & strUser, _
                                                NULL, _
                                                JOIN_DOMAIN + ACCT_CREATE)
```



## <a name="requirements"></a><span data-ttu-id="c20d5-219">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c20d5-219">Requirements</span></span>



| <span data-ttu-id="c20d5-220">Requisito</span><span class="sxs-lookup"><span data-stu-id="c20d5-220">Requirement</span></span> | <span data-ttu-id="c20d5-221">Valor</span><span class="sxs-lookup"><span data-stu-id="c20d5-221">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c20d5-222">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c20d5-222">Minimum supported client</span></span><br/> | <span data-ttu-id="c20d5-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c20d5-223">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c20d5-224">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c20d5-224">Minimum supported server</span></span><br/> | <span data-ttu-id="c20d5-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c20d5-225">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c20d5-226">Namespace</span><span class="sxs-lookup"><span data-stu-id="c20d5-226">Namespace</span></span><br/>                | <span data-ttu-id="c20d5-227">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c20d5-227">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c20d5-228">MOF</span><span class="sxs-lookup"><span data-stu-id="c20d5-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c20d5-229"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c20d5-229"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c20d5-230">DLL</span><span class="sxs-lookup"><span data-stu-id="c20d5-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c20d5-231"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c20d5-231"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c20d5-232">Confira também</span><span class="sxs-lookup"><span data-stu-id="c20d5-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c20d5-233">**\_Sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="c20d5-233">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="c20d5-234">**Método UnjoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="c20d5-234">**UnjoinDomainOrWorkgroup method**</span></span>](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

