---
description: Contém métodos que permitem que você acesse e modifique as configurações de segurança para um namespace.
ms.assetid: a54fdd85-feb8-4727-9f26-fe4f213cab6b
ms.tgt_platform: multiple
title: Classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 58de990b56518550705cda2f8360cd90a0381c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091838"
---
# <a name="__systemsecurity-class"></a><span data-ttu-id="8bcb9-103">\_\_Classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="8bcb9-103">\_\_SystemSecurity class</span></span>

<span data-ttu-id="8bcb9-104">A classe de sistema **\_ \_ SystemSecurity** contém métodos que permitem que você acesse e modifique as configurações de segurança de um namespace.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-104">The **\_\_SystemSecurity** system class contains methods that let you access and modify the security settings for a namespace.</span></span> <span data-ttu-id="8bcb9-105">A classe **\_ \_ SystemSecurity** é uma classe singleton em cada namespace.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-105">The **\_\_SystemSecurity** class is a singleton class in each namespace.</span></span>

> [!Note]  
> <span data-ttu-id="8bcb9-106">Para obter mais informações, consulte [Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="8bcb9-106">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

 

<span data-ttu-id="8bcb9-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8bcb9-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bcb9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8bcb9-109">Syntax</span></span>

``` syntax
class __SystemSecurity
{
};
```

## <a name="members"></a><span data-ttu-id="8bcb9-110">Membros</span><span class="sxs-lookup"><span data-stu-id="8bcb9-110">Members</span></span>

<span data-ttu-id="8bcb9-111">A classe **\_ \_ SystemSecurity** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8bcb9-111">The **\_\_SystemSecurity** class has these types of members:</span></span>

-   [<span data-ttu-id="8bcb9-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8bcb9-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8bcb9-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="8bcb9-113">Methods</span></span>

<span data-ttu-id="8bcb9-114">A classe **\_ \_ SystemSecurity** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-114">The **\_\_SystemSecurity** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="8bcb9-115">Método</span><span class="sxs-lookup"><span data-stu-id="8bcb9-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="8bcb9-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8bcb9-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8bcb9-117"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></span><span class="sxs-lookup"><span data-stu-id="8bcb9-117"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8bcb9-118">Obtém uma lista de usuários que têm permissão de acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-118">Gets a list of users who are allowed remote access.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8bcb9-119">Esse método não funciona em versões do Windows com suporte.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-119">This method does not work on supported versions of Windows.</span></span> <span data-ttu-id="8bcb9-120">Em vez disso, use <a href="--systemsecurity-getsd.md"><strong>gets</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8bcb9-120">Use <a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8bcb9-121"><a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a></span><span class="sxs-lookup"><span data-stu-id="8bcb9-121"><a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8bcb9-122">Retorna uma máscara com cada bit que corresponde a um direito de acesso.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-122">Returns a mask with each bit that corresponds to an access right.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8bcb9-123"><a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a></span><span class="sxs-lookup"><span data-stu-id="8bcb9-123"><a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8bcb9-124">Obtém o <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> para o namespace ao qual o usuário está conectado.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-124">Gets the <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> for the namespace to which the user is connected.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8bcb9-125"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="8bcb9-125"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8bcb9-126">Obtém o descritor de segurança que controla o acesso ao namespace do WMI associado à instância do <strong>__SystemSecurity</strong>.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-126">Gets the security descriptor that controls access to the WMI namespace associated with the instance of <strong>__SystemSecurity</strong>.</span></span> <span data-ttu-id="8bcb9-127">O descritor de segurança é retornado como uma instância de<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-127">The security descriptor is returned as an instance of<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8bcb9-128"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></span><span class="sxs-lookup"><span data-stu-id="8bcb9-128"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8bcb9-129">Define uma lista de usuários que têm permissão de acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-129">Sets a list of users who are allowed remote access.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8bcb9-130">Esse método não funciona em versões do Windows com suporte.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-130">This method does not work on supported versions of Windows.</span></span> <span data-ttu-id="8bcb9-131">Em vez disso, use <a href="--systemsecurity-setsd.md"><strong>sets</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8bcb9-131">Use <a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="8bcb9-132"><a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a></span><span class="sxs-lookup"><span data-stu-id="8bcb9-132"><a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8bcb9-133">Define o descritor de segurança para o namespace ao qual o usuário está conectado.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-133">Sets the security descriptor for the namespace to which the user is connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8bcb9-134"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="8bcb9-134"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="8bcb9-135">Grava uma versão atualizada do descritor de segurança que controla o acesso à impressora.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-135">Writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="8bcb9-136">O descritor de segurança é representado por uma instância do <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-136">The security descriptor is represented by an instance of <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="8bcb9-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="8bcb9-137">Remarks</span></span>

<span data-ttu-id="8bcb9-138">Você pode exigir que os scripts e aplicativos de cliente usem uma conexão criptografada para autenticação adicionando o qualificador **RequiresEncryption** ao arquivo. MOF que cria o namespace.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-138">You can require that client scripts and applications use an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the .mof file that creates the namespace.</span></span> <span data-ttu-id="8bcb9-139">Você também pode modificar um namespace existente adicionando esse atributo e compilar o arquivo. mof novamente.</span><span class="sxs-lookup"><span data-stu-id="8bcb9-139">You can also modify an existing namespace by adding this attribute and compile the .mof file again.</span></span> <span data-ttu-id="8bcb9-140">Para obter mais informações sobre como usar o **RequiresEncryption**, consulte [exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="8bcb9-140">For more information about how to use **RequiresEncryption**, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8bcb9-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bcb9-141">Requirements</span></span>



| <span data-ttu-id="8bcb9-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bcb9-142">Requirement</span></span> | <span data-ttu-id="8bcb9-143">Valor</span><span class="sxs-lookup"><span data-stu-id="8bcb9-143">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8bcb9-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bcb9-144">Minimum supported client</span></span><br/> | <span data-ttu-id="8bcb9-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8bcb9-145">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8bcb9-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bcb9-146">Minimum supported server</span></span><br/> | <span data-ttu-id="8bcb9-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8bcb9-147">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8bcb9-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="8bcb9-148">Namespace</span></span><br/>                | <span data-ttu-id="8bcb9-149">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="8bcb9-149">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="8bcb9-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="8bcb9-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bcb9-151">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="8bcb9-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="8bcb9-152">Constantes de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="8bcb9-152">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="8bcb9-153">Objetos do descritor de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="8bcb9-153">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="8bcb9-154">Protegendo namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="8bcb9-154">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="8bcb9-155">Estabelecendo a herança da segurança do namespace</span><span class="sxs-lookup"><span data-stu-id="8bcb9-155">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="8bcb9-156">ACLs (listas de controle de acesso)</span><span class="sxs-lookup"><span data-stu-id="8bcb9-156">Access Control Lists (ACLs)</span></span>](/windows/desktop/SecAuthZ/access-control-lists)
</dt> <dt>

[<span data-ttu-id="8bcb9-157">**\_Descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="8bcb9-157">**Security\_Descriptor**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

