---
title: Classe Win32_RDMSPublishedApplication
description: Gerencia um aplicativo publicado.
ms.assetid: 7a529f1d-1aaf-42fb-8469-92d38a7b0ffc
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSPublishedApplication Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSPublishedApplication classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSPublishedApplication
- Win32_RDMSPublishedApplication.AppAlias
- Win32_RDMSPublishedApplication.PoolName
- Win32_RDMSPublishedApplication.DisplayName
- Win32_RDMSPublishedApplication.ShowInPortal
- Win32_RDMSPublishedApplication.SecurityDescriptor
- Win32_RDMSPublishedApplication.AppPath
- Win32_RDMSPublishedApplication.VirtualPath
- Win32_RDMSPublishedApplication.CommandLineSetting
- Win32_RDMSPublishedApplication.RequiredCommandLine
- Win32_RDMSPublishedApplication.Folder
- Win32_RDMSPublishedApplication.IconPath
- Win32_RDMSPublishedApplication.IconIndex
- Win32_RDMSPublishedApplication.IconContents
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb003faf5e51c9da1f46f23c5f8d6b5ae977987c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295873"
---
# <a name="win32_rdmspublishedapplication-class"></a><span data-ttu-id="b17f3-105">\_Classe Win32 RDMSPublishedApplication</span><span class="sxs-lookup"><span data-stu-id="b17f3-105">Win32\_RDMSPublishedApplication class</span></span>

<span data-ttu-id="b17f3-106">Gerencia um aplicativo publicado.</span><span class="sxs-lookup"><span data-stu-id="b17f3-106">Manages a published application.</span></span>

<span data-ttu-id="b17f3-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b17f3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b17f3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b17f3-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSPublishedApplication
{
  string  AppAlias;
  string  PoolName;
  string  DisplayName;
  boolean ShowInPortal;
  string  SecurityDescriptor;
  string  AppPath;
  string  VirtualPath;
  uint32  CommandLineSetting;
  string  RequiredCommandLine;
  string  Folder;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
};
```

## <a name="members"></a><span data-ttu-id="b17f3-109">Membros</span><span class="sxs-lookup"><span data-stu-id="b17f3-109">Members</span></span>

<span data-ttu-id="b17f3-110">A classe **Win32 \_ RDMSPublishedApplication** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b17f3-110">The **Win32\_RDMSPublishedApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="b17f3-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b17f3-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b17f3-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b17f3-112">Properties</span></span>

<span data-ttu-id="b17f3-113">A classe **Win32 \_ RDMSPublishedApplication** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b17f3-113">The **Win32\_RDMSPublishedApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b17f3-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="b17f3-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17f3-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b17f3-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17f3-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b17f3-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b17f3-117">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b17f3-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b17f3-118">Obtém e define o alias do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b17f3-118">Gets and sets the alias of the application.</span></span>

</dd> <dt>

<span data-ttu-id="b17f3-119">**AppPath**</span><span class="sxs-lookup"><span data-stu-id="b17f3-119">**AppPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17f3-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b17f3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17f3-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b17f3-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b17f3-122">Obtém e define o caminho para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b17f3-122">Gets and sets the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="b17f3-123">**CommandLineSetting**</span><span class="sxs-lookup"><span data-stu-id="b17f3-123">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17f3-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b17f3-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b17f3-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b17f3-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b17f3-126">Obtém e define a configuração de linha de comando para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b17f3-126">Gets and sets the command line setting for the application.</span></span>

<span data-ttu-id="b17f3-127">Essa propriedade pode ser definida como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b17f3-127">This property can be set to one of the following values:</span></span>

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span data-ttu-id="b17f3-128"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span><span class="sxs-lookup"><span data-stu-id="b17f3-128"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b17f3-129">Não permitir argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="b17f3-129">Do not allow command line arguments.</span></span>

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="b17f3-130"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Permitir** (1)</span><span class="sxs-lookup"><span data-stu-id="b17f3-130"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b17f3-131">Permitir argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="b17f3-131">Allow command line arguments.</span></span>

</dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span data-ttu-id="b17f3-132"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Exigir** (2)</span><span class="sxs-lookup"><span data-stu-id="b17f3-132"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Require** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b17f3-133">Exigir argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="b17f3-133">Require command line arguments.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b17f3-134">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="b17f3-134">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17f3-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b17f3-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17f3-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b17f3-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b17f3-137">Obtém e define o nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b17f3-137">Gets and sets the display name of the application.</span></span>

</dd> <dt>

<span data-ttu-id="b17f3-138">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="b17f3-138">**Folder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17f3-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b17f3-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17f3-140">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b17f3-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b17f3-141">Obtém e define o caminho para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b17f3-141">Gets and sets the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="b17f3-142">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="b17f3-142">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17f3-143">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="b17f3-143">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b17f3-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b17f3-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b17f3-145">Obtém e define uma matriz que contém o ícone do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b17f3-145">Gets and sets an array that contains the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="b17f3-146">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="b17f3-146">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17f3-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b17f3-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b17f3-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b17f3-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b17f3-149">Obtém e define o índice para o ícone do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b17f3-149">Gets and sets the index for the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="b17f3-150">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="b17f3-150">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17f3-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b17f3-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17f3-152">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b17f3-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b17f3-153">Obtém e define o caminho para o ícone deste aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b17f3-153">Gets and sets the path to the icon for this application.</span></span>

</dd> <dt>

<span data-ttu-id="b17f3-154">**PoolName**</span><span class="sxs-lookup"><span data-stu-id="b17f3-154">**PoolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17f3-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b17f3-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17f3-156">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b17f3-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b17f3-157">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b17f3-157">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b17f3-158">Obtém e define o nome do pool de aplicativos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b17f3-158">Gets and sets the name of the application pool of the application.</span></span>

</dd> <dt>

<span data-ttu-id="b17f3-159">**RequiredCommandLine**</span><span class="sxs-lookup"><span data-stu-id="b17f3-159">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17f3-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b17f3-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17f3-161">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b17f3-161">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b17f3-162">Obtém e define os argumentos de linha de comando que são necessários para o aplicativo</span><span class="sxs-lookup"><span data-stu-id="b17f3-162">Gets and sets the command line arguments that are required for the application</span></span>

</dd> <dt>

<span data-ttu-id="b17f3-163">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b17f3-163">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17f3-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b17f3-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17f3-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b17f3-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b17f3-166">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b17f3-166">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b17f3-167">Obtém e define o descritor de segurança que controla o acesso ao aplicativo, no formato SDDL (Security Descriptor Definition Language).</span><span class="sxs-lookup"><span data-stu-id="b17f3-167">Gets and sets the security descriptor that controls access to the application, in security descriptor definition language (SDDL) format.</span></span>

</dd> <dt>

<span data-ttu-id="b17f3-168">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="b17f3-168">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17f3-169">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b17f3-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b17f3-170">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b17f3-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b17f3-171">Indica se o aplicativo deve ser exibido no Terminal Services Acesso via Web (TS Acesso via Web).</span><span class="sxs-lookup"><span data-stu-id="b17f3-171">Indicates whether to display the application in Terminal Services Web Access (TS Web Access).</span></span> <span data-ttu-id="b17f3-172">**True** para exibir o aplicativo no TS acesso via Web; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="b17f3-172">**TRUE** to display the application in TS Web Access; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b17f3-173">**VirtualPath**</span><span class="sxs-lookup"><span data-stu-id="b17f3-173">**VirtualPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17f3-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b17f3-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17f3-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b17f3-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b17f3-176">Obtém e define o caminho virtual para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b17f3-176">Gets and sets the virtual path to the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b17f3-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b17f3-177">Requirements</span></span>



| <span data-ttu-id="b17f3-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="b17f3-178">Requirement</span></span> | <span data-ttu-id="b17f3-179">Valor</span><span class="sxs-lookup"><span data-stu-id="b17f3-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b17f3-180">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b17f3-180">Minimum supported client</span></span><br/> | <span data-ttu-id="b17f3-181">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b17f3-181">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b17f3-182">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b17f3-182">Minimum supported server</span></span><br/> | <span data-ttu-id="b17f3-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b17f3-183">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="b17f3-184">Namespace</span><span class="sxs-lookup"><span data-stu-id="b17f3-184">Namespace</span></span><br/>                | <span data-ttu-id="b17f3-185">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="b17f3-185">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b17f3-186">MOF</span><span class="sxs-lookup"><span data-stu-id="b17f3-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b17f3-187"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b17f3-187"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b17f3-188">DLL</span><span class="sxs-lookup"><span data-stu-id="b17f3-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b17f3-189"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b17f3-189"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b17f3-190">Confira também</span><span class="sxs-lookup"><span data-stu-id="b17f3-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b17f3-191">Provedor de serviços de gerenciamento de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="b17f3-191">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

