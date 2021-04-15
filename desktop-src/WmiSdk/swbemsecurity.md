---
description: O objeto SWbemSecurity Obtém ou define as configurações de segurança, como privilégios, impessoas e níveis de autenticação atribuídos a um objeto.
ms.assetid: 794587fa-5feb-455b-be28-ecfaa25625ad
ms.tgt_platform: multiple
title: Objeto SWbemSecurity (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity
- ISWbemSecurity
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: da59c3b996a80384c133336503124141f0907f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768421"
---
# <a name="swbemsecurity-object"></a><span data-ttu-id="c648c-103">Objeto SWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="c648c-103">SWbemSecurity object</span></span>

<span data-ttu-id="c648c-104">O objeto **SWbemSecurity** Obtém ou define as configurações de segurança, como privilégios, impessoas e níveis de autenticação atribuídos a um objeto.</span><span class="sxs-lookup"><span data-stu-id="c648c-104">The **SWbemSecurity** object gets or sets security settings, such as privileges, COM impersonations, and authentication levels assigned to an object.</span></span> <span data-ttu-id="c648c-105">Os objetos [**SWbemLocator**](swbemlocator.md), [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), [**SWbemLastError**](swbemlasterror.md)e [**SWbemEventSource**](swbemeventsource.md) têm uma propriedade **Security \_** , que é o objeto **SWbemSecurity** .</span><span class="sxs-lookup"><span data-stu-id="c648c-105">The [**SWbemLocator**](swbemlocator.md), [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), [**SWbemLastError**](swbemlasterror.md), and [**SWbemEventSource**](swbemeventsource.md) objects have a **Security\_** property, which is the **SWbemSecurity** object.</span></span> <span data-ttu-id="c648c-106">Quando você recupera uma instância ou exibe o log de segurança do WMI, talvez seja necessário definir as propriedades do objeto de **segurança \_** .</span><span class="sxs-lookup"><span data-stu-id="c648c-106">When you retrieve an instance or view the WMI security log, you might need to set the properties of the **Security\_** object.</span></span>

<span data-ttu-id="c648c-107">A chamada do VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) não pode criar o objeto de segurança.</span><span class="sxs-lookup"><span data-stu-id="c648c-107">The VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call cannot create the Security object.</span></span> <span data-ttu-id="c648c-108">As configurações de segurança nesse objeto não identificam as configurações de autenticação, representação ou privilégios em uma conexão com o WMI ou a segurança em vigor para o proxy quando um objeto é entregue a um coletor em uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="c648c-108">The security settings in this object do not identify the authentication, impersonation, or privilege settings on a connection to WMI, or the security in effect for the proxy when an object is delivered to a sink in an asynchronous call.</span></span> <span data-ttu-id="c648c-109">Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="c648c-109">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

## <a name="members"></a><span data-ttu-id="c648c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="c648c-110">Members</span></span>

<span data-ttu-id="c648c-111">O objeto **SWbemSecurity** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c648c-111">The **SWbemSecurity** object has these types of members:</span></span>

-   [<span data-ttu-id="c648c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c648c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c648c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c648c-113">Properties</span></span>

<span data-ttu-id="c648c-114">O objeto **SWbemSecurity** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c648c-114">The **SWbemSecurity** object has these properties.</span></span>



| <span data-ttu-id="c648c-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c648c-115">Property</span></span>                                                                    | <span data-ttu-id="c648c-116">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="c648c-116">Access type</span></span>           | <span data-ttu-id="c648c-117">Description</span><span class="sxs-lookup"><span data-stu-id="c648c-117">Description</span></span>                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c648c-118">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="c648c-118">**AuthenticationLevel**</span></span>](swbemsecurity-authenticationlevel.md)<br/> | <span data-ttu-id="c648c-119">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c648c-119">Read/write</span></span><br/> | <span data-ttu-id="c648c-120">Valor numérico que define o nível de autenticação COM que é atribuído a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="c648c-120">Numeric value that defines the COM Authentication level that is assigned to this object.</span></span> <span data-ttu-id="c648c-121">Essa configuração determina como você protege as informações enviadas do WMI.</span><span class="sxs-lookup"><span data-stu-id="c648c-121">This setting determines how you protect information sent from WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="c648c-122">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="c648c-122">**ImpersonationLevel**</span></span>](swbemsecurity-impersonationlevel.md)<br/>   | <span data-ttu-id="c648c-123">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c648c-123">Read/write</span></span><br/> | <span data-ttu-id="c648c-124">Valor numérico que define o nível de representação COM que é atribuído a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="c648c-124">Numeric value that defines the COM Impersonation level that is assigned to this object.</span></span> <span data-ttu-id="c648c-125">Essa configuração determina se os processos de propriedade da WMI podem detectar ou usar suas credenciais de segurança ao fazer chamadas para outros processos.</span><span class="sxs-lookup"><span data-stu-id="c648c-125">This setting determines if processes owned by WMI can detect or use your security credentials when making calls to other processes.</span></span><br/> |
| [<span data-ttu-id="c648c-126">**Direitos**</span><span class="sxs-lookup"><span data-stu-id="c648c-126">**Privileges**</span></span>](swbemsecurity-privileges.md)<br/>                   | <span data-ttu-id="c648c-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c648c-127">Read-only</span></span><br/>  | <span data-ttu-id="c648c-128">Um objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) que define privilégios para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="c648c-128">An [**SWbemPrivilegeSet**](swbemprivilegeset.md) object that defines privileges for this object.</span></span> <span data-ttu-id="c648c-129">Para obter mais informações, consulte [executando com privilégios especiais](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="c648c-129">For more information, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="c648c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c648c-130">Requirements</span></span>



| <span data-ttu-id="c648c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c648c-131">Requirement</span></span> | <span data-ttu-id="c648c-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c648c-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c648c-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c648c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c648c-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c648c-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c648c-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c648c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c648c-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c648c-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c648c-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c648c-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c648c-138"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c648c-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c648c-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c648c-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="c648c-140"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c648c-140"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c648c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c648c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c648c-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c648c-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c648c-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="c648c-143">CLSID</span></span><br/>                    | <span data-ttu-id="c648c-144">\_SWBEMSECURITY CLSID</span><span class="sxs-lookup"><span data-stu-id="c648c-144">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="c648c-145">IID</span><span class="sxs-lookup"><span data-stu-id="c648c-145">IID</span></span><br/>                      | <span data-ttu-id="c648c-146">ISWbemSecurity de IID \_</span><span class="sxs-lookup"><span data-stu-id="c648c-146">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="c648c-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="c648c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c648c-148">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="c648c-148">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="c648c-149">Mantendo a segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="c648c-149">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="c648c-150">Definindo a \_ segurança do processo do aplicativo cliente \_</span><span class="sxs-lookup"><span data-stu-id="c648c-150">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="c648c-151">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="c648c-151">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="c648c-152">**WbemImpersonationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="c648c-152">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[<span data-ttu-id="c648c-153">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="c648c-153">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> </dl>

 

