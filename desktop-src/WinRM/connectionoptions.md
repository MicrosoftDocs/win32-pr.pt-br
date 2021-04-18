---
title: Objeto ConnectionOptions (WSManDisp. h)
description: O objeto ConnectionOptions é passado para o método CreateSession para fornecer o nome de usuário e a senha associados à conta local no computador remoto.
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- Objeto ConnectionOptions Gerenciamento Remoto do Windows
- Gerenciamento Remoto do Windows de objeto ConnectionOptions, descrito
topic_type:
- apiref
api_name:
- ConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 164eb886ce98266cab3109e773b731e002d1abac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105765697"
---
# <a name="connectionoptions-object"></a><span data-ttu-id="1bd2f-105">Objeto ConnectionOptions</span><span class="sxs-lookup"><span data-stu-id="1bd2f-105">ConnectionOptions object</span></span>

<span data-ttu-id="1bd2f-106">O objeto **ConnectionOptions** é passado para o método [**CreateSession**](wsman-createsession.md) para fornecer o nome de usuário e a senha associados à conta local no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="1bd2f-106">The **ConnectionOptions** object is passed to the [**CreateSession**](wsman-createsession.md) method to provide the user name and password associated with the local account on the remote computer.</span></span> <span data-ttu-id="1bd2f-107">Se nenhum parâmetro for fornecido, as credenciais da conta que executa o script serão definidas com os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="1bd2f-107">If no parameters are supplied, then the credentials of the account running the script are set to the default values.</span></span>

## <a name="members"></a><span data-ttu-id="1bd2f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1bd2f-108">Members</span></span>

<span data-ttu-id="1bd2f-109">O objeto **ConnectionOptions** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1bd2f-109">The **ConnectionOptions** object has these types of members:</span></span>

-   [<span data-ttu-id="1bd2f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1bd2f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1bd2f-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1bd2f-111">Properties</span></span>

<span data-ttu-id="1bd2f-112">O objeto **ConnectionOptions** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1bd2f-112">The **ConnectionOptions** object has these properties.</span></span>



| <span data-ttu-id="1bd2f-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1bd2f-113">Property</span></span>                                                  | <span data-ttu-id="1bd2f-114">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="1bd2f-114">Access type</span></span>           | <span data-ttu-id="1bd2f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="1bd2f-115">Description</span></span>                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1bd2f-116">**Senha**</span><span class="sxs-lookup"><span data-stu-id="1bd2f-116">**Password**</span></span>](connectionoptions-password.md)<br/> | <span data-ttu-id="1bd2f-117">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="1bd2f-117">Write-only</span></span><br/> | <span data-ttu-id="1bd2f-118">Define a senha de uma conta local ou de domínio no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="1bd2f-118">Sets the password of a local or domain account on the remote computer.</span></span><br/>           |
| [<span data-ttu-id="1bd2f-119">**Usu**</span><span class="sxs-lookup"><span data-stu-id="1bd2f-119">**UserName**</span></span>](connectionoptions-username.md)<br/> | <span data-ttu-id="1bd2f-120">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1bd2f-120">Read/write</span></span><br/> | <span data-ttu-id="1bd2f-121">Define e Obtém o nome de usuário de uma conta local ou de domínio no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="1bd2f-121">Sets and gets the user name of a local or domain account on the remote computer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1bd2f-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bd2f-122">Remarks</span></span>

<span data-ttu-id="1bd2f-123">O objeto **ConnectionOptions** corresponde à interface [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) .</span><span class="sxs-lookup"><span data-stu-id="1bd2f-123">The **ConnectionOptions** object corresponds to the [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) interface.</span></span>

<span data-ttu-id="1bd2f-124">Se um aplicativo cliente Gerenciamento Remoto do Windows estiver sendo executado sob representação, ocorrerá uma falha se você definir a propriedade [**password**](connectionoptions-password.md) .</span><span class="sxs-lookup"><span data-stu-id="1bd2f-124">If a Windows Remote Management client application is running under impersonation, then a failure occurs if you set the [**Password**](connectionoptions-password.md) property.</span></span> <span data-ttu-id="1bd2f-125">Um aplicativo cliente é um script ou outro programa que envia uma solicitação para o WinRM no computador local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="1bd2f-125">A client application is a script or other program that sends a request to WinRM on the local or a remote computer.</span></span> <span data-ttu-id="1bd2f-126">O aplicativo cliente pode estar sendo executado sob representação porque ele chamou uma função como [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1bd2f-126">The client application may be running under impersonation because it called a function like [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)).</span></span> <span data-ttu-id="1bd2f-127">Uma página de Active Server (ASP) ou serviço não pode solicitar um nome de usuário e senha se o processo ASP for executado em uma conta que representa um cliente.</span><span class="sxs-lookup"><span data-stu-id="1bd2f-127">An Active Server Page (ASP) or service cannot request a user name and password if the ASP process runs under an account that impersonates a client.</span></span>

<span data-ttu-id="1bd2f-128">O sinalizador **WSManFlagCredUserNamePassword** deve ser definido na chamada [**WSman. CreateSession**](wsman-createsession.md) ao usar o [**nome de usuário**](connectionoptions-username.md) e a [**senha**](connectionoptions-password.md) para autenticação.</span><span class="sxs-lookup"><span data-stu-id="1bd2f-128">The **WSManFlagCredUserNamePassword** flag should be set on the [**WSman.CreateSession**](wsman-createsession.md) call when using the [**UserName**](connectionoptions-username.md) and [**Password**](connectionoptions-password.md) for authentication.</span></span>

## <a name="examples"></a><span data-ttu-id="1bd2f-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1bd2f-129">Examples</span></span>

<span data-ttu-id="1bd2f-130">O exemplo de código VBScript a seguir mostra como criar um objeto **ConnectionOptions** , definir as propriedades da conta no computador remoto e usá-lo na criação de um objeto de [**sessão**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="1bd2f-130">The following VBScript code example shows how to create a **ConnectionOptions** object, set the properties for the account on the remote computer, and use it in creating a [**Session**](session.md) object.</span></span>


```VB
Set objWsman = CreateObject( "Wsman.Automation" )
'Create ConnectionOptions object.
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "johns "
objConnectionOptions.Password = "Dtf#4542?98"
iFlags = objWsman.SessionFlagUseBasic Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession _
  ("https://172.30.168.2", iFlags, objConnectionOptions)
strResource = objSession.Get("winrm/config")
```



## <a name="requirements"></a><span data-ttu-id="1bd2f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bd2f-131">Requirements</span></span>



| <span data-ttu-id="1bd2f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bd2f-132">Requirement</span></span> | <span data-ttu-id="1bd2f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="1bd2f-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bd2f-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bd2f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1bd2f-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1bd2f-135">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="1bd2f-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bd2f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1bd2f-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1bd2f-137">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1bd2f-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1bd2f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bd2f-139"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bd2f-139"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1bd2f-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="1bd2f-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1bd2f-141"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1bd2f-141"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="1bd2f-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1bd2f-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="1bd2f-143"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1bd2f-143"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1bd2f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1bd2f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bd2f-145"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bd2f-145"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1bd2f-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bd2f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bd2f-147">Autenticação para conexões remotas</span><span class="sxs-lookup"><span data-stu-id="1bd2f-147">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> <dt>

[<span data-ttu-id="1bd2f-148">API de script do WinRM</span><span class="sxs-lookup"><span data-stu-id="1bd2f-148">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="1bd2f-149">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="1bd2f-149">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="1bd2f-150">Usando Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="1bd2f-150">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="1bd2f-151">Criando scripts no Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="1bd2f-151">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="1bd2f-152">Obtendo dados do computador local</span><span class="sxs-lookup"><span data-stu-id="1bd2f-152">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="1bd2f-153">Obtendo dados de um computador remoto</span><span class="sxs-lookup"><span data-stu-id="1bd2f-153">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

