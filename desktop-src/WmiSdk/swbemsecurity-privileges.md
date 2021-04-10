---
description: A propriedade Privileges é um objeto SWbemPrivilegeSet. Essa propriedade é usada para habilitar ou desabilitar privilégios específicos do Windows. Talvez seja necessário definir um desses privilégios para executar tarefas específicas usando a API Instrumentação de Gerenciamento do Windows (WMI).
ms.assetid: 6e4cae22-23d6-4981-b38c-d298654e59ab
ms.tgt_platform: multiple
title: Propriedade SWbemSecurity. Privileges (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.Privileges
- ISWbemSecurity.Privileges
- ISWbemSecurity.get_Privileges
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6fd8e1c0f9b6667b49d0956bcea5ac9e187443d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165186"
---
# <a name="swbemsecurityprivileges-property"></a><span data-ttu-id="ebebb-105">Propriedade SWbemSecurity. Privileges</span><span class="sxs-lookup"><span data-stu-id="ebebb-105">SWbemSecurity.Privileges property</span></span>

<span data-ttu-id="ebebb-106">A propriedade **Privileges** é um objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) .</span><span class="sxs-lookup"><span data-stu-id="ebebb-106">The **Privileges** property is an [**SWbemPrivilegeSet**](swbemprivilegeset.md) object.</span></span> <span data-ttu-id="ebebb-107">Essa propriedade é usada para habilitar ou desabilitar privilégios específicos do Windows.</span><span class="sxs-lookup"><span data-stu-id="ebebb-107">This property is used to enable or disable specific Windows privileges.</span></span> <span data-ttu-id="ebebb-108">Talvez seja necessário definir um desses privilégios para executar tarefas específicas usando a API Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ebebb-108">You may need to set one of these privileges to perform specific tasks using the Windows Management Instrumentation (WMI) API.</span></span>

<span data-ttu-id="ebebb-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ebebb-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="ebebb-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="ebebb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebebb-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ebebb-111">Syntax</span></span>


```VB
SWbemSecurity.Privileges As Object
```



## <a name="property-value"></a><span data-ttu-id="ebebb-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ebebb-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="ebebb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebebb-113">Remarks</span></span>

<span data-ttu-id="ebebb-114">Essa configuração permite conceder ou revogar privilégios como parte de uma cadeia de caracteres do moniker WMI.</span><span class="sxs-lookup"><span data-stu-id="ebebb-114">This setting allows you to grant or revoke privileges as part of a WMI moniker string.</span></span> <span data-ttu-id="ebebb-115">Para obter a lista completa de valores aplicáveis, consulte [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) e [**constantes de privilégio**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ebebb-115">For the complete list of applicable values, see [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) and [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="ebebb-116">Você pode alterar os privilégios definidos para os objetos [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) adicionando objetos [**SWbemPrivilege**](swbemprivilege.md) à propriedade **Privileges** .</span><span class="sxs-lookup"><span data-stu-id="ebebb-116">You can change the privileges defined for the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects by adding [**SWbemPrivilege**](swbemprivilege.md) objects to the **Privileges** property.</span></span>

<span data-ttu-id="ebebb-117">Há diferenças fundamentais em como as diferentes versões do Windows lidam com os privilégios.</span><span class="sxs-lookup"><span data-stu-id="ebebb-117">There are fundamental differences in how different versions of Windows handle changes to privileges.</span></span> <span data-ttu-id="ebebb-118">Se você estiver desenvolvendo um aplicativo que só é usado em plataformas Windows, poderá definir ou revogar privilégios a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="ebebb-118">If you are developing an application that is only used on Windows platforms, you can set or revoke privileges at any time.</span></span>

<span data-ttu-id="ebebb-119">O exemplo a seguir define o **SeDebugPrivilege** na conexão inicial do moniker para obter um objeto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="ebebb-119">The following example sets the **SeDebugPrivilege** on the initial moniker connection to obtain an [**SWbemServices**](swbemservices.md) object.</span></span>


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



<span data-ttu-id="ebebb-120">Para obter mais informações sobre como formatar a cadeia de caracteres de segurança para uma conexão de moniker, consulte [**constantes de privilégio**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ebebb-120">For more information about how to format the security string for a moniker connection, see [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="ebebb-121">O exemplo a seguir executa a mesma tarefa, mas define o privilégio após o logon inicial no WMI.</span><span class="sxs-lookup"><span data-stu-id="ebebb-121">The following example performs the same task, but it sets the privilege after the initial log on to WMI.</span></span>


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate}")
Service.Security_.Privileges.AddAsString "SeDebugPrivilege", True
```



<span data-ttu-id="ebebb-122">Observe que, para chamadas para [**SwbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md), você deve usar o nome completo do privilégio de segurança, por exemplo, "SeDebugPrivilege" em vez de "debug".</span><span class="sxs-lookup"><span data-stu-id="ebebb-122">Note that for calls to [**SwbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md), you must use the full name of the security privilege, for example, "SeDebugPrivilege" instead of "Debug".</span></span>

## <a name="requirements"></a><span data-ttu-id="ebebb-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebebb-123">Requirements</span></span>



| <span data-ttu-id="ebebb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebebb-124">Requirement</span></span> | <span data-ttu-id="ebebb-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ebebb-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebebb-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebebb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ebebb-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebebb-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ebebb-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebebb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ebebb-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebebb-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ebebb-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ebebb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebebb-131"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebebb-131"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ebebb-132">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ebebb-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="ebebb-133"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ebebb-133"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ebebb-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ebebb-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebebb-135"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebebb-135"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ebebb-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="ebebb-136">CLSID</span></span><br/>                    | <span data-ttu-id="ebebb-137">\_SWBEMSECURITY CLSID</span><span class="sxs-lookup"><span data-stu-id="ebebb-137">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="ebebb-138">IID</span><span class="sxs-lookup"><span data-stu-id="ebebb-138">IID</span></span><br/>                      | <span data-ttu-id="ebebb-139">ISWbemSecurity de IID \_</span><span class="sxs-lookup"><span data-stu-id="ebebb-139">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="ebebb-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebebb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebebb-141">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="ebebb-141">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="ebebb-142">Executando operações privilegiadas</span><span class="sxs-lookup"><span data-stu-id="ebebb-142">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="ebebb-143">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="ebebb-143">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> </dl>

 

 




