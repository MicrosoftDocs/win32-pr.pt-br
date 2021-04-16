---
description: Descreve a instalação local do WMI.
ms.assetid: 907b65b2-a853-40f4-8b36-5a05a2b1cf85
ms.tgt_platform: multiple
title: Classe __CIMOMIdentification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CIMOMIdentification
- Root.__CIMOMIdentification.SetupDateTime
- Root.__CIMOMIdentification.VersionCurrentlyRunning
- Root.__CIMOMIdentification.VersionUsedToCreateDB
- Root.__CIMOMIdentification.WorkingDirectory
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: a8590a2a83cdbc9bd06575cf17ddbe65138a4a31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765710"
---
# <a name="__cimomidentification-class"></a><span data-ttu-id="528c6-103">\_\_Classe CIMOMIdentification</span><span class="sxs-lookup"><span data-stu-id="528c6-103">\_\_CIMOMIdentification class</span></span>

<span data-ttu-id="528c6-104">A classe de sistema **\_ \_ CIMOMIdentification** descreve a instalação local do WMI.</span><span class="sxs-lookup"><span data-stu-id="528c6-104">The **\_\_CIMOMIdentification** system class describes the local installation of WMI.</span></span> <span data-ttu-id="528c6-105">Essa é uma classe singleton; Há apenas uma instância.</span><span class="sxs-lookup"><span data-stu-id="528c6-105">This is a singleton class; there is only one instance.</span></span> <span data-ttu-id="528c6-106">A classe **\_ \_ CIMOMIdentification** está disponível apenas nos namespaces **raiz** e **raiz \\ padrão** .</span><span class="sxs-lookup"><span data-stu-id="528c6-106">The **\_\_CIMOMIdentification** class is available only in the **Root** and **Root\\Default** namespaces.</span></span> <span data-ttu-id="528c6-107">Os usuários consultam a instância para obter informações sobre a instalação do WMI.</span><span class="sxs-lookup"><span data-stu-id="528c6-107">Users query for the instance to obtain information about the WMI installation.</span></span>

<span data-ttu-id="528c6-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="528c6-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="528c6-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="528c6-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="528c6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="528c6-110">Syntax</span></span>

``` syntax
[singleton]
class __CIMOMIdentification : __SystemClass
{
  string SetupDateTime;
  string VersionCurrentlyRunning;
  string VersionUsedToCreateDB;
  string WorkingDirectory;
};
```

## <a name="members"></a><span data-ttu-id="528c6-111">Membros</span><span class="sxs-lookup"><span data-stu-id="528c6-111">Members</span></span>

<span data-ttu-id="528c6-112">A classe **\_ \_ CIMOMIdentification** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="528c6-112">The **\_\_CIMOMIdentification** class has these types of members:</span></span>

-   [<span data-ttu-id="528c6-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="528c6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="528c6-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="528c6-114">Properties</span></span>

<span data-ttu-id="528c6-115">A classe **\_ \_ CIMOMIdentification** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="528c6-115">The **\_\_CIMOMIdentification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="528c6-116">**Setupdatetime**</span><span class="sxs-lookup"><span data-stu-id="528c6-116">**SetupDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c6-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="528c6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="528c6-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="528c6-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="528c6-119">Data e hora da instalação.</span><span class="sxs-lookup"><span data-stu-id="528c6-119">Date and time of installation.</span></span> <span data-ttu-id="528c6-120">Essa propriedade estará vazia depois que o sistema operacional for instalado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="528c6-120">This property is empty after the operating system is installed for the first time.</span></span>

<span data-ttu-id="528c6-121">Se o repositório WMI tiver sido excluído e, em seguida, criado novamente, essa propriedade conterá a data e a hora em que o repositório será criado novamente.</span><span class="sxs-lookup"><span data-stu-id="528c6-121">If the WMI repository has been deleted and then created again, this property contains the date and time that the repository is created again.</span></span>

</dd> <dt>

<span data-ttu-id="528c6-122">**VersionCurrentlyRunning**</span><span class="sxs-lookup"><span data-stu-id="528c6-122">**VersionCurrentlyRunning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c6-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="528c6-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="528c6-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="528c6-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="528c6-125">Indica a versão da imagem real que contém o serviço WMI que criou o repositório modelo CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="528c6-125">Indicates the version of the actual image containing the WMI service that created the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="528c6-126">Como o formato do repositório pode ser alterado entre as versões do WMI, essa propriedade permite atualizações futuras do WMI para determinar se o banco de dados deve ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="528c6-126">Because the repository format may change between versions of WMI, this property allows future WMI upgrades to determine whether the database must be upgraded.</span></span> <span data-ttu-id="528c6-127">O formato é:</span><span class="sxs-lookup"><span data-stu-id="528c6-127">The format is:</span></span>

<span data-ttu-id="528c6-128">"1.00.183.0000"</span><span class="sxs-lookup"><span data-stu-id="528c6-128">"1.00.183.0000"</span></span>

<span data-ttu-id="528c6-129">onde o primeiro dígito é a versão principal, os próximos dois dígitos são versões secundárias e os três próximos dígitos são o número da versão.</span><span class="sxs-lookup"><span data-stu-id="528c6-129">where the first digit is the major version, the next two digits are minor versions, and the next three digits are the build number.</span></span> <span data-ttu-id="528c6-130">Os dígitos restantes não são usados.</span><span class="sxs-lookup"><span data-stu-id="528c6-130">The remaining digits are not used.</span></span>

</dd> <dt>

<span data-ttu-id="528c6-131">**VersionUsedToCreateDB**</span><span class="sxs-lookup"><span data-stu-id="528c6-131">**VersionUsedToCreateDB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c6-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="528c6-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="528c6-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="528c6-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="528c6-134">Indica a versão da imagem real que contém o serviço WMI que criou o repositório CIM.</span><span class="sxs-lookup"><span data-stu-id="528c6-134">Indicates the version of the actual image containing the WMI service that created the CIM repository.</span></span> <span data-ttu-id="528c6-135">Como o formato do repositório pode ser alterado entre as versões do WMI, essa propriedade permite atualizações futuras do WMI para determinar se o banco de dados deve ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="528c6-135">Because the repository format may change between versions of WMI, this property allows future WMI upgrades to determine whether the database must be upgraded.</span></span> <span data-ttu-id="528c6-136">O formato é:</span><span class="sxs-lookup"><span data-stu-id="528c6-136">The format is:</span></span>

<span data-ttu-id="528c6-137">"1.00.183.0000"</span><span class="sxs-lookup"><span data-stu-id="528c6-137">"1.00.183.0000"</span></span>

<span data-ttu-id="528c6-138">onde o primeiro dígito é a versão principal, os próximos dois dígitos são versões secundárias e os três próximos dígitos são o número da versão.</span><span class="sxs-lookup"><span data-stu-id="528c6-138">where the first digit is the major version, the next two digits are minor versions, and the next three digits are the build number.</span></span> <span data-ttu-id="528c6-139">Os dígitos restantes não são usados.</span><span class="sxs-lookup"><span data-stu-id="528c6-139">The remaining digits are not used.</span></span>

</dd> <dt>

<span data-ttu-id="528c6-140">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="528c6-140">**WorkingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="528c6-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="528c6-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="528c6-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="528c6-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="528c6-143">Diretório de instalação.</span><span class="sxs-lookup"><span data-stu-id="528c6-143">Installation directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="528c6-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="528c6-144">Remarks</span></span>

<span data-ttu-id="528c6-145">A classe **\_ \_ CIMOMIdentification** é derivada de [**\_ \_ SystemClass**](--systemclass.md), que não tem propriedades.</span><span class="sxs-lookup"><span data-stu-id="528c6-145">The **\_\_CIMOMIdentification** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

## <a name="examples"></a><span data-ttu-id="528c6-146">Exemplos</span><span class="sxs-lookup"><span data-stu-id="528c6-146">Examples</span></span>

<span data-ttu-id="528c6-147">O exemplo de código VBScript a seguir descreve como exibir informações de identificação do modelo de objeto CIM e foi tirado do diretório de exemplo em \\ \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Sysmgmt \\ WMI \\ scripting.</span><span class="sxs-lookup"><span data-stu-id="528c6-147">The following VBScript code sample describes how to display CIM object model identification information, and was taken from the sample directory at \\\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\sysmgmt\\wmi\\scripting.</span></span>


```VB
on error resume next 
set cimomid = GetObject("winmgmts:root\default:__cimomidentification=@")

if err <> 0 then
 WScript.Echo ErrNumber, Err.Source, Err.Description
else
 WScript.Echo cimomid.path_.displayname
 WScript.Echo cimomid.versionusedtocreatedb
end if
```



<span data-ttu-id="528c6-148">O exemplo de código Perl a seguir descreve como exibir informações de identificação do modelo de objeto CIM e foi tirado do diretório de exemplo em \\ \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Sysmgmt \\ WMI \\ scripting.</span><span class="sxs-lookup"><span data-stu-id="528c6-148">The following Perl code sample describes how to display CIM object model identification information, and was taken from the sample directory at \\\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\sysmgmt\\wmi\\scripting.</span></span>


```Perl
use strict;
use Win32::OLE;

my ($Cimomid, $locator, $services);

eval { $Cimomid = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default")->
 Get("__CIMOMIdentification=@"); };

unless ($@)
{
 print "\n", $Cimomid->Path_()->{displayname}, "\n";
 print $Cimomid->{versionusedtocreatedb}, "\n";
}
else
{ 
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="528c6-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="528c6-149">Requirements</span></span>



| <span data-ttu-id="528c6-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="528c6-150">Requirement</span></span> | <span data-ttu-id="528c6-151">Valor</span><span class="sxs-lookup"><span data-stu-id="528c6-151">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="528c6-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="528c6-152">Minimum supported client</span></span><br/> | <span data-ttu-id="528c6-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="528c6-153">Windows Vista</span></span><br/>       |
| <span data-ttu-id="528c6-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="528c6-154">Minimum supported server</span></span><br/> | <span data-ttu-id="528c6-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="528c6-155">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="528c6-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="528c6-156">Namespace</span></span><br/>                | <span data-ttu-id="528c6-157">Root</span><span class="sxs-lookup"><span data-stu-id="528c6-157">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="528c6-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="528c6-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="528c6-159">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="528c6-159">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="528c6-160">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="528c6-160">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

