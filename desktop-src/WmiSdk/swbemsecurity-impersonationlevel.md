---
description: A propriedade ImpersonationLevel é um inteiro que define o nível de representação COM que é atribuído a esse objeto.
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: Propriedade SWbemSecurity. ImpersonationLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.ImpersonationLevel
- ISWbemSecurity.ImpersonationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3b996d5920aba91fddf880ee9ddf6bf8081fb39f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837251"
---
# <a name="swbemsecurityimpersonationlevel-property"></a><span data-ttu-id="be386-103">Propriedade SWbemSecurity. ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="be386-103">SWbemSecurity.ImpersonationLevel property</span></span>

<span data-ttu-id="be386-104">A propriedade **ImpersonationLevel** é um inteiro que define o nível de representação com que é atribuído a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="be386-104">The **ImpersonationLevel** property is an integer that defines the COM impersonation level that is assigned to this object.</span></span> <span data-ttu-id="be386-105">Essa configuração determina se os processos pertencentes à Instrumentação de Gerenciamento do Windows (WMI) podem detectar ou usar suas credenciais de segurança ao fazer chamadas para outros processos.</span><span class="sxs-lookup"><span data-stu-id="be386-105">This setting determines if processes owned by Windows Management Instrumentation (WMI) can detect or use your security credentials when making calls to other processes.</span></span> <span data-ttu-id="be386-106">Para obter mais informações sobre os níveis de representação, consulte [definindo a \_ segurança do \_ processo do aplicativo cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="be386-106">For more information about impersonation levels, see [Setting Client\_Application\_Process Security](setting-client-application-process-security.md).</span></span>

<span data-ttu-id="be386-107">Se você não definir o nível de representação especificamente em um moniker ou definindo a propriedade **SWBemSecurity. ImpersonationLevel** em um objeto protegível, o WMI definirá o nível de representação padrão como o valor especificado na [chave de registro de nível de representação padrão](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="be386-107">If you do not set the impersonation level specifically in either a moniker, or by setting the **SWBemSecurity.ImpersonationLevel** property on a securable object, WMI sets the default impersonation level to the value specified in the [default impersonation level registry key](setting-the-default-process-security-level-using-vbscript.md).</span></span> <span data-ttu-id="be386-108">Se essa configuração não for suficiente, o provedor não atenderá à sua solicitação e a chamada para a API do WMI poderá falhar com um código de erro de **wbemErrAccessDenied** (2147749891/0x80041003).</span><span class="sxs-lookup"><span data-stu-id="be386-108">If this setting is not sufficient, the provider does not service your request, and the call to the WMI API can fail with an error code of **wbemErrAccessDenied** (2147749891/0x80041003).</span></span>

<span data-ttu-id="be386-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="be386-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="be386-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="be386-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="be386-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be386-111">Syntax</span></span>


```VB
SWbemSecurity.ImpersonationLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="be386-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="be386-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="be386-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="be386-113">Remarks</span></span>

<span data-ttu-id="be386-114">Como um nível de representação do DCOM, essa propriedade pode ser definida como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="be386-114">As a DCOM impersonation level, this property can be set to one of the following values:</span></span>



| <span data-ttu-id="be386-115">Valor</span><span class="sxs-lookup"><span data-stu-id="be386-115">Value</span></span>           | <span data-ttu-id="be386-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="be386-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be386-117">**Anônimo**</span><span class="sxs-lookup"><span data-stu-id="be386-117">**Anonymous**</span></span>   | <span data-ttu-id="be386-118">Oculta as credenciais do autor da chamada.</span><span class="sxs-lookup"><span data-stu-id="be386-118">Hides the credentials of the caller.</span></span> <span data-ttu-id="be386-119">Na verdade, o WMI não dá suporte a esse nível de representação; se um script especificar impersonationLevel = Anonymous, o WMI atualizará silenciosamente o nível de representação para identificar.</span><span class="sxs-lookup"><span data-stu-id="be386-119">WMI does not actually support this impersonation level; if a script specifies impersonationLevel=Anonymous, WMI will silently upgrade the impersonation level to Identify.</span></span> <span data-ttu-id="be386-120">No entanto, isso é um exercício sem sentido, porque os scripts que usam o nível de identificação provavelmente falharão.</span><span class="sxs-lookup"><span data-stu-id="be386-120">This is in some ways a meaningless exercise, however, because scripts using the Identify level are likely to fail.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="be386-121">**Identificar**</span><span class="sxs-lookup"><span data-stu-id="be386-121">**Identify**</span></span>    | <span data-ttu-id="be386-122">Permite que os objetos consultem as credenciais do chamador.</span><span class="sxs-lookup"><span data-stu-id="be386-122">Enables objects to query the credentials of the caller.</span></span> <span data-ttu-id="be386-123">Os scripts que usam esse nível de representação provavelmente falharão; o nível de identificação normalmente permite que você não faça mais do que verificar listas de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="be386-123">Scripts using this impersonation level are likely to fail; the Identify level typically lets you do no more than check access control lists.</span></span> <span data-ttu-id="be386-124">Você não poderá executar scripts em computadores remotos usando identificar.</span><span class="sxs-lookup"><span data-stu-id="be386-124">You will not be able to run scripts against remote computers using Identify.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="be386-125">**Impersonate**</span><span class="sxs-lookup"><span data-stu-id="be386-125">**Impersonate**</span></span> | <span data-ttu-id="be386-126">Permite que os objetos usem as credenciais do chamador.</span><span class="sxs-lookup"><span data-stu-id="be386-126">Enables objects to use the credentials of the caller.</span></span> <span data-ttu-id="be386-127">É recomendável que você use esse nível de representação com scripts WMI.</span><span class="sxs-lookup"><span data-stu-id="be386-127">It is recommended that you use this impersonation level with WMI scripts.</span></span> <span data-ttu-id="be386-128">Quando você fizer isso, o script WMI usará suas credenciais de usuário; Como resultado, será capaz de executar qualquer tarefa que você possa executar.</span><span class="sxs-lookup"><span data-stu-id="be386-128">When you do so, the WMI script will use your user credentials; as a result, it will be able to perform any tasks that you are able to perform.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="be386-129">**Delegar**</span><span class="sxs-lookup"><span data-stu-id="be386-129">**Delegate**</span></span>    | <span data-ttu-id="be386-130">Permite que os objetos permitam que outros objetos usem as credenciais do chamador.</span><span class="sxs-lookup"><span data-stu-id="be386-130">Enables objects to permit other objects to use the credentials of the caller.</span></span> <span data-ttu-id="be386-131">A delegação permite que um script use suas credenciais em um computador remoto e, em seguida, permite que esse computador remoto use suas credenciais em outro computador remoto.</span><span class="sxs-lookup"><span data-stu-id="be386-131">Delegation allows a script to use your credentials on a remote computer and then enables that remote computer to use your credentials on another remote computer.</span></span> <span data-ttu-id="be386-132">Embora você possa usar esse nível de representação dentro de scripts WMI, você deve fazer isso somente se necessário, pois ele pode representar um risco de segurança.</span><span class="sxs-lookup"><span data-stu-id="be386-132">While you can use this impersonation level within WMI scripts, you should do so only if necessary because it might pose a security risk.</span></span><br/> <span data-ttu-id="be386-133">Você não pode usar o nível de representação de representante, a menos que todas as contas de usuário e contas de computador envolvidas na transação tenham sido marcadas como confiáveis para delegação em Active Directory.</span><span class="sxs-lookup"><span data-stu-id="be386-133">You cannot use the Delegate impersonation level unless all the user accounts and computer accounts involved in the transaction have all been marked as Trusted for delegation in Active Directory.</span></span> <span data-ttu-id="be386-134">Isso ajuda a minimizar os riscos de segurança.</span><span class="sxs-lookup"><span data-stu-id="be386-134">This helps minimize the security risks.</span></span> <span data-ttu-id="be386-135">Embora um computador remoto possa usar suas credenciais, ele pode fazer isso somente se ele e outros computadores envolvidos na transação forem confiáveis para delegação.</span><span class="sxs-lookup"><span data-stu-id="be386-135">Although a remote computer can use your credentials, it can do so only if both it and any other computers involved in the transaction are trusted for delegation.</span></span><br/> |



 

<span data-ttu-id="be386-136">Como observado, a representação anônima oculta suas credenciais e identifica permite que um objeto remoto consulte suas credenciais, mas o objeto remoto não pode representar o contexto de segurança.</span><span class="sxs-lookup"><span data-stu-id="be386-136">As noted, Anonymous impersonation hides your credentials and Identify permits a remote object to query your credentials, but the remote object cannot impersonate your security context.</span></span> <span data-ttu-id="be386-137">(Em outras palavras, embora o objeto remoto saiba quem você é, ele não pode "fingir" para você.) Os scripts WMI que acessam computadores remotos usando uma dessas duas configurações geralmente falharão.</span><span class="sxs-lookup"><span data-stu-id="be386-137">(In other words, although the remote object knows who you are, it cannot "pretend" to be you.) WMI scripts accessing remote computers using one of these two settings will generally fail.</span></span> <span data-ttu-id="be386-138">Na verdade, a maioria dos scripts executados no computador local usando uma dessas duas configurações também falhará.</span><span class="sxs-lookup"><span data-stu-id="be386-138">In fact, most scripts run on the local computer using one of these two settings will also fail.</span></span>

<span data-ttu-id="be386-139">Impersonate permite que o serviço WMI remoto use seu contexto de segurança para executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="be386-139">Impersonate permits the remote WMI service to use your security context to perform the requested operation.</span></span> <span data-ttu-id="be386-140">Uma solicitação WMI remota que usa a configuração Impersonate normalmente é realizada com sucesso, desde que suas credenciais tenham privilégios suficientes para executar a operação pretendida.</span><span class="sxs-lookup"><span data-stu-id="be386-140">A remote WMI request that uses the Impersonate setting typically succeeds, provided your credentials have sufficient privileges to perform the intended operation.</span></span> <span data-ttu-id="be386-141">Em outras palavras, você não pode usar o WMI para executar uma ação (remotamente ou de outra forma) que você não tem permissão para executar fora do WMI.</span><span class="sxs-lookup"><span data-stu-id="be386-141">In other words, you cannot use WMI to perform an action (remotely or otherwise) that you do not have permission to perform outside WMI.</span></span>

<span data-ttu-id="be386-142">Definir impersonationLevel para delegar permite que o serviço WMI remoto passe suas credenciais para outros objetos e geralmente é considerado um risco de segurança.</span><span class="sxs-lookup"><span data-stu-id="be386-142">Setting impersonationLevel to Delegate permits the remote WMI service to pass your credentials on to other objects and is generally considered a security risk.</span></span>

<span data-ttu-id="be386-143">Você pode definir o nível de representação de um objeto [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) definindo a propriedade **ImpersonationLevel** para o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="be386-143">You can set the impersonation level of an [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) object by setting the **ImpersonationLevel** property to the desired value.</span></span> <span data-ttu-id="be386-144">O exemplo a seguir mostra como definir o nível de representação para um objeto **SWbemObject** :</span><span class="sxs-lookup"><span data-stu-id="be386-144">The following example shows you how to set the impersonation level for an **SWbemObject** object:</span></span>


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



<span data-ttu-id="be386-145">Você também pode especificar os níveis de representação como parte de um moniker.</span><span class="sxs-lookup"><span data-stu-id="be386-145">You can also specify impersonation levels as part of a moniker.</span></span> <span data-ttu-id="be386-146">O exemplo a seguir define o nível de autenticação e o nível de representação e recupera uma instância do [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="be386-146">The following example sets the authentication level and the impersonation level, and retrieves an instance of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,"& _
                         "authenticationLevel=pktPrivacy}"& _
                         "!root/cimv2:Win32_service='ALERTER'")
```



## <a name="requirements"></a><span data-ttu-id="be386-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be386-147">Requirements</span></span>



| <span data-ttu-id="be386-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="be386-148">Requirement</span></span> | <span data-ttu-id="be386-149">Valor</span><span class="sxs-lookup"><span data-stu-id="be386-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be386-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be386-150">Minimum supported client</span></span><br/> | <span data-ttu-id="be386-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be386-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be386-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be386-152">Minimum supported server</span></span><br/> | <span data-ttu-id="be386-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be386-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be386-154">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="be386-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="be386-155"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="be386-155"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="be386-156">DLL</span><span class="sxs-lookup"><span data-stu-id="be386-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be386-157"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be386-157"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="be386-158">CLSID</span><span class="sxs-lookup"><span data-stu-id="be386-158">CLSID</span></span><br/>                    | <span data-ttu-id="be386-159">\_SWBEMSECURITY CLSID</span><span class="sxs-lookup"><span data-stu-id="be386-159">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="be386-160">IID</span><span class="sxs-lookup"><span data-stu-id="be386-160">IID</span></span><br/>                      | <span data-ttu-id="be386-161">ISWbemSecurity de IID \_</span><span class="sxs-lookup"><span data-stu-id="be386-161">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="be386-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="be386-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be386-163">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="be386-163">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="be386-164">Definindo a \_ segurança do processo do aplicativo cliente \_</span><span class="sxs-lookup"><span data-stu-id="be386-164">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="be386-165">**WbemImpersonationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="be386-165">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 

