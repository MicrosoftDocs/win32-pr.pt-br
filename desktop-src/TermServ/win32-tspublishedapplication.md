---
title: Classe Win32_TSPublishedApplication
description: Define os aplicativos que são disponibilizados para uso remoto por meio do Windows Server 2008 R2 RemoteApp.
ms.assetid: 5b9cb36b-3d8d-4105-acea-c79440d977fe
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSPublishedApplication Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSPublishedApplication classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSPublishedApplication
- Win32_TSPublishedApplication.Caption
- Win32_TSPublishedApplication.Description
- Win32_TSPublishedApplication.InstallDate
- Win32_TSPublishedApplication.Name
- Win32_TSPublishedApplication.Status
- Win32_TSPublishedApplication.Alias
- Win32_TSPublishedApplication.SecurityDescriptor
- Win32_TSPublishedApplication.Path
- Win32_TSPublishedApplication.PathExists
- Win32_TSPublishedApplication.VPath
- Win32_TSPublishedApplication.IconPath
- Win32_TSPublishedApplication.IconIndex
- Win32_TSPublishedApplication.IconContents
- Win32_TSPublishedApplication.CommandLineSetting
- Win32_TSPublishedApplication.RequiredCommandLine
- Win32_TSPublishedApplication.ShowInPortal
- Win32_TSPublishedApplication.RDPFileContents
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3825087d05b622818c74f011f30b325ed8ff7f60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760118"
---
# <a name="win32_tspublishedapplication-class"></a><span data-ttu-id="c8001-105">\_Classe Win32 TSPublishedApplication</span><span class="sxs-lookup"><span data-stu-id="c8001-105">Win32\_TSPublishedApplication class</span></span>

<span data-ttu-id="c8001-106">Define os aplicativos que são disponibilizados para uso remoto por meio do Windows Server 2008 R2 RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="c8001-106">Defines the applications that are made available for remote use through Windows Server 2008 R2 RemoteApp.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8001-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8001-107">Syntax</span></span>

``` syntax
class Win32_TSPublishedApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  string   SecurityDescriptor;
  string   Path;
  boolean  PathExists;
  string   VPath;
  string   IconPath;
  sint32   IconIndex;
  uint8    IconContents[];
  uint32   CommandLineSetting;
  string   RequiredCommandLine;
  boolean  ShowInPortal;
  string   RDPFileContents;
};
```

## <a name="members"></a><span data-ttu-id="c8001-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c8001-108">Members</span></span>

<span data-ttu-id="c8001-109">A classe **Win32 \_ TSPublishedApplication** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c8001-109">The **Win32\_TSPublishedApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="c8001-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c8001-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8001-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c8001-111">Properties</span></span>

<span data-ttu-id="c8001-112">A classe **Win32 \_ TSPublishedApplication** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c8001-112">The **Win32\_TSPublishedApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8001-113">**Alias**</span><span class="sxs-lookup"><span data-stu-id="c8001-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8001-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8001-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c8001-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c8001-116">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="c8001-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c8001-117">O alias do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c8001-117">The alias of the application.</span></span> <span data-ttu-id="c8001-118">O alias é um identificador exclusivo para o programa que usa como padrão o nome do arquivo do programa (sem a extensão).</span><span class="sxs-lookup"><span data-stu-id="c8001-118">The alias is a unique identifier for the program that defaults to the program's file name (without the extension).</span></span>

</dd> <dt>

<span data-ttu-id="c8001-119">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c8001-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8001-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8001-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8001-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8001-122">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c8001-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c8001-123">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="c8001-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="c8001-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c8001-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8001-125">**CommandLineSetting**</span><span class="sxs-lookup"><span data-stu-id="c8001-125">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-126">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c8001-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8001-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c8001-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8001-128">A configuração de argumentos de linha de comando para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c8001-128">The command-line arguments setting for the application.</span></span> <span data-ttu-id="c8001-129">Os valores a seguir são possíveis.</span><span class="sxs-lookup"><span data-stu-id="c8001-129">The following values are possible.</span></span>

<dt>

<span data-ttu-id="c8001-130">0</span><span class="sxs-lookup"><span data-stu-id="c8001-130">0</span></span>
</dt> <dd>

<span data-ttu-id="c8001-131">Não permitir argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="c8001-131">Do not allow command-line arguments.</span></span>

</dd> <dt>

<span data-ttu-id="c8001-132">1</span><span class="sxs-lookup"><span data-stu-id="c8001-132">1</span></span>
</dt> <dd>

<span data-ttu-id="c8001-133">Permitir qualquer argumento de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="c8001-133">Allow any command-line arguments.</span></span>

</dd> <dt>

<span data-ttu-id="c8001-134">2</span><span class="sxs-lookup"><span data-stu-id="c8001-134">2</span></span>
</dt> <dd>

<span data-ttu-id="c8001-135">Sempre use os argumentos de linha de comando necessários (especificados em **RequiredCommandLine**).</span><span class="sxs-lookup"><span data-stu-id="c8001-135">Always use the required command-line arguments (specified in **RequiredCommandLine**).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c8001-136">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c8001-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8001-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8001-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8001-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8001-139">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="c8001-139">Description of the object.</span></span>

<span data-ttu-id="c8001-140">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c8001-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8001-141">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="c8001-141">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-142">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="c8001-142">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c8001-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8001-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8001-144">O conteúdo em bytes do ícone que corresponde ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c8001-144">The byte contents of the icon that corresponds to the application.</span></span>

</dd> <dt>

<span data-ttu-id="c8001-145">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="c8001-145">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-146">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c8001-146">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8001-147">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c8001-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8001-148">O índice ou a ID do ícone.</span><span class="sxs-lookup"><span data-stu-id="c8001-148">The index or ID of the icon.</span></span>

</dd> <dt>

<span data-ttu-id="c8001-149">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="c8001-149">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8001-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8001-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c8001-151">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8001-152">O caminho do ícone do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c8001-152">The path of the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="c8001-153">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c8001-153">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-154">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c8001-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c8001-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8001-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8001-156">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="c8001-156">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="c8001-157">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="c8001-157">The date the object was installed.</span></span> <span data-ttu-id="c8001-158">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="c8001-158">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c8001-159">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c8001-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8001-160">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c8001-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8001-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8001-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8001-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8001-163">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="c8001-163">The name of the object.</span></span>

<span data-ttu-id="c8001-164">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c8001-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8001-165">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="c8001-165">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8001-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8001-167">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c8001-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8001-168">O caminho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c8001-168">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="c8001-169">**PathExists**</span><span class="sxs-lookup"><span data-stu-id="c8001-169">**PathExists**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-170">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c8001-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c8001-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8001-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8001-172">Indica se o caminho do aplicativo é válido.</span><span class="sxs-lookup"><span data-stu-id="c8001-172">Indicates whether the application path is valid.</span></span>

</dd> <dt>

<span data-ttu-id="c8001-173">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="c8001-173">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8001-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8001-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c8001-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8001-176">O conteúdo do arquivo RDP que corresponde ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c8001-176">The contents of the RDP file that correspond to the application.</span></span>

</dd> <dt>

<span data-ttu-id="c8001-177">**RequiredCommandLine**</span><span class="sxs-lookup"><span data-stu-id="c8001-177">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8001-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8001-179">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c8001-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8001-180">Os argumentos de linha de comando que são necessários para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c8001-180">The command-line arguments that are required for the application.</span></span>

</dd> <dt>

<span data-ttu-id="c8001-181">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c8001-181">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8001-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8001-183">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c8001-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8001-184">Um descritor de segurança que controla o acesso ao aplicativo, no formato SDDL.</span><span class="sxs-lookup"><span data-stu-id="c8001-184">A security descriptor that controls access to the application, in SDDL format.</span></span> <span data-ttu-id="c8001-185">Uma cadeia de caracteres vazia implica permitir todo o acesso.</span><span class="sxs-lookup"><span data-stu-id="c8001-185">An empty string implies allow all access.</span></span> <span data-ttu-id="c8001-186">Este descritor de segurança não oferece suporte a ACEs DENY ou ACEs que se referem a usuários ou grupos que não são de domínio.</span><span class="sxs-lookup"><span data-stu-id="c8001-186">This security descriptor does not support DENY ACEs, or ACEs that refer to nondomain users or groups.</span></span>

</dd> <dt>

<span data-ttu-id="c8001-187">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="c8001-187">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-188">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c8001-188">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c8001-189">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c8001-189">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8001-190">Indica se o aplicativo deve ser mostrado no Acesso via Web de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="c8001-190">Indicates whether the application should be shown in RD Web Access.</span></span>

</dd> <dt>

<span data-ttu-id="c8001-191">**Status**</span><span class="sxs-lookup"><span data-stu-id="c8001-191">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8001-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8001-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8001-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8001-194">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="c8001-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="c8001-195">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c8001-195">Current status of the object.</span></span> <span data-ttu-id="c8001-196">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="c8001-196">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c8001-197">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="c8001-197">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c8001-198">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="c8001-198">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c8001-199">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="c8001-199">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c8001-200">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="c8001-200">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c8001-201">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c8001-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="c8001-202">("OK")</span><span class="sxs-lookup"><span data-stu-id="c8001-202">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c8001-203">("Erro")</span><span class="sxs-lookup"><span data-stu-id="c8001-203">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c8001-204">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="c8001-204">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c8001-205">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="c8001-205">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c8001-206">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c8001-206">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c8001-207">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="c8001-207">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c8001-208">("Parando")</span><span class="sxs-lookup"><span data-stu-id="c8001-208">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c8001-209">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="c8001-209">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c8001-210">**VPath**</span><span class="sxs-lookup"><span data-stu-id="c8001-210">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8001-211">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8001-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8001-212">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c8001-212">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c8001-213">O caminho virtual do aplicativo, que significa o caminho com as variáveis de ambiente incluídas.</span><span class="sxs-lookup"><span data-stu-id="c8001-213">The virtual path of the application, meaning the path with environment variables included.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8001-214">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8001-214">Remarks</span></span>

<span data-ttu-id="c8001-215">Você deve ser um membro do grupo Administradores para definir propriedades usando essa classe.</span><span class="sxs-lookup"><span data-stu-id="c8001-215">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="c8001-216">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="c8001-216">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="c8001-217">Para chamadas C/C++, esse é um nível de autenticação **de \_ \_ privacidade do \_ PCT no \_ nível \_** de autenticado RPC C, que pode ser definido usando a função com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="c8001-217">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="c8001-218">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="c8001-218">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="c8001-219">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="c8001-219">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="c8001-220">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c8001-220">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c8001-221">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c8001-221">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c8001-222">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="c8001-222">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c8001-223">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c8001-223">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8001-224">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8001-224">Requirements</span></span>



| <span data-ttu-id="c8001-225">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8001-225">Requirement</span></span> | <span data-ttu-id="c8001-226">Valor</span><span class="sxs-lookup"><span data-stu-id="c8001-226">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8001-227">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8001-227">Minimum supported client</span></span><br/> | <span data-ttu-id="c8001-228">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c8001-228">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c8001-229">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8001-229">Minimum supported server</span></span><br/> | <span data-ttu-id="c8001-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8001-230">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8001-231">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8001-231">Namespace</span></span><br/>                | <span data-ttu-id="c8001-232">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="c8001-232">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c8001-233">MOF</span><span class="sxs-lookup"><span data-stu-id="c8001-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8001-234"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8001-234"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="c8001-235">DLL</span><span class="sxs-lookup"><span data-stu-id="c8001-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8001-236"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8001-236"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

