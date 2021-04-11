---
description: A \_ classe CIM DirectorySpecification captura a estrutura de diretório principal de um elemento de software. Essa classe é usada para organizar os arquivos de um elemento de software em unidades gerenciáveis que podem ser realocadas em um sistema de computador.
ms.assetid: faeab356-e470-477b-97d2-1a19ce1d8d21
ms.tgt_platform: multiple
title: Classe CIM_DirectorySpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecification
- CIM_DirectorySpecification.CheckID
- CIM_DirectorySpecification.Caption
- CIM_DirectorySpecification.Description
- CIM_DirectorySpecification.CheckMode
- CIM_DirectorySpecification.Name
- CIM_DirectorySpecification.TargetOperatingSystem
- CIM_DirectorySpecification.Version
- CIM_DirectorySpecification.SoftwareElementID
- CIM_DirectorySpecification.SoftwareElementState
- CIM_DirectorySpecification.DirectoryPath
- CIM_DirectorySpecification.DirectoryType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a7eb6ae627c8ed9b5639e573e1d2d89132698ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089389"
---
# <a name="cim_directoryspecification-class"></a><span data-ttu-id="178ee-104">\_Classe CIM DirectorySpecification</span><span class="sxs-lookup"><span data-stu-id="178ee-104">CIM\_DirectorySpecification class</span></span>

<span data-ttu-id="178ee-105">A classe **CIM \_ DirectorySpecification** captura a estrutura de diretório principal de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="178ee-105">The **CIM\_DirectorySpecification** class captures the major directory structure of a software element.</span></span> <span data-ttu-id="178ee-106">Essa classe é usada para organizar os arquivos de um elemento de software em unidades gerenciáveis que podem ser realocadas em um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="178ee-106">This class is used to organize the files of a software element into manageable units that can be relocated on a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="178ee-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="178ee-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="178ee-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="178ee-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="178ee-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="178ee-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="178ee-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="178ee-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="178ee-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="178ee-111">Syntax</span></span>

``` syntax
[UUID("{A524EE6E-DB29-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_DirectorySpecification : CIM_Check
{
  string  CheckID;
  string  Caption;
  string  Description;
  boolean CheckMode;
  string  Name;
  uint16  TargetOperatingSystem;
  string  Version;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  string  DirectoryPath;
  uint16  DirectoryType;
};
```

## <a name="members"></a><span data-ttu-id="178ee-112">Membros</span><span class="sxs-lookup"><span data-stu-id="178ee-112">Members</span></span>

<span data-ttu-id="178ee-113">A classe **CIM \_ DirectorySpecification** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="178ee-113">The **CIM\_DirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="178ee-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="178ee-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="178ee-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="178ee-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="178ee-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="178ee-116">Methods</span></span>

<span data-ttu-id="178ee-117">A classe **CIM \_ DirectorySpecification** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="178ee-117">The **CIM\_DirectorySpecification** class has these methods.</span></span>



| <span data-ttu-id="178ee-118">Método</span><span class="sxs-lookup"><span data-stu-id="178ee-118">Method</span></span>                                                              | <span data-ttu-id="178ee-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="178ee-119">Description</span></span>                                                                     |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="178ee-120">**Chame**</span><span class="sxs-lookup"><span data-stu-id="178ee-120">**Invoke**</span></span>](invoke-method-in-class-cim-directoryspecification.md) | <span data-ttu-id="178ee-121">Avalia uma verificação específica.</span><span class="sxs-lookup"><span data-stu-id="178ee-121">Evaluates a particular check.</span></span> <span data-ttu-id="178ee-122">Esse método não é implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="178ee-122">This method is not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="178ee-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="178ee-123">Properties</span></span>

<span data-ttu-id="178ee-124">A classe **CIM \_ DirectorySpecification** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="178ee-124">The **CIM\_DirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="178ee-125">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="178ee-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="178ee-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="178ee-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="178ee-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="178ee-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="178ee-128">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="178ee-128">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="178ee-129">Uma breve descrição textual do assunto.</span><span class="sxs-lookup"><span data-stu-id="178ee-129">A short textual description of the subject.</span></span>

<span data-ttu-id="178ee-130">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="178ee-130">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="178ee-131">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="178ee-131">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="178ee-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="178ee-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="178ee-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="178ee-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="178ee-134">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="178ee-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="178ee-135">Identificador usado em conjunto com outras chaves para identificar exclusivamente a verificação.</span><span class="sxs-lookup"><span data-stu-id="178ee-135">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="178ee-136">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="178ee-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="178ee-137">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="178ee-137">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="178ee-138">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="178ee-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="178ee-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="178ee-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="178ee-140">Se for **true**, espera-se que a condição exista no ambiente.</span><span class="sxs-lookup"><span data-stu-id="178ee-140">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="178ee-141">Por exemplo, espera-se que um arquivo esteja em um sistema, portanto, o método [**Invoke**](invoke-method-in-class-cim-check.md) deve retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="178ee-141">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="178ee-142">Se for **false**, a condição não deverá existir.</span><span class="sxs-lookup"><span data-stu-id="178ee-142">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="178ee-143">Por exemplo, um arquivo não está em um sistema, portanto, o método [**Invoke**](invoke-method-in-class-cim-check.md) deve retornar **false**.</span><span class="sxs-lookup"><span data-stu-id="178ee-143">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="178ee-144">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="178ee-144">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="178ee-145">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="178ee-145">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="178ee-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="178ee-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="178ee-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="178ee-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="178ee-148">Uma descrição dos objetos.</span><span class="sxs-lookup"><span data-stu-id="178ee-148">A description of the objects.</span></span>

<span data-ttu-id="178ee-149">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="178ee-149">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="178ee-150">**DirectoryPath**</span><span class="sxs-lookup"><span data-stu-id="178ee-150">**DirectoryPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="178ee-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="178ee-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="178ee-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="178ee-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="178ee-153">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="178ee-153">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="178ee-154">Nome do diretório.</span><span class="sxs-lookup"><span data-stu-id="178ee-154">Directory name.</span></span> <span data-ttu-id="178ee-155">O valor fornecido por um provedor de aplicativo é um nome de caminho padrão ou recomendado.</span><span class="sxs-lookup"><span data-stu-id="178ee-155">The value supplied by an application provider is a default or recommended path name.</span></span> <span data-ttu-id="178ee-156">O valor pode ser alterado para um ambiente específico.</span><span class="sxs-lookup"><span data-stu-id="178ee-156">The value can be changed for a particular environment.</span></span>

</dd> <dt>

<span data-ttu-id="178ee-157">**Directorytype**</span><span class="sxs-lookup"><span data-stu-id="178ee-157">**DirectoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="178ee-158">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="178ee-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="178ee-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="178ee-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="178ee-160">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Local da DMTF \| \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="178ee-160">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Location\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="178ee-161">Tipo de diretório que está sendo descrito.</span><span class="sxs-lookup"><span data-stu-id="178ee-161">Type of directory being described.</span></span>

<dt>

<span id="Product_base_directory"></span><span id="product_base_directory"></span><span id="PRODUCT_BASE_DIRECTORY"></span>

<span data-ttu-id="178ee-162">**Diretório base do produto** (0)</span><span class="sxs-lookup"><span data-stu-id="178ee-162">**Product base directory** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_executable_directory"></span><span id="product_executable_directory"></span><span id="PRODUCT_EXECUTABLE_DIRECTORY"></span>

<span data-ttu-id="178ee-163">**Diretório executável do produto** (1)</span><span class="sxs-lookup"><span data-stu-id="178ee-163">**Product executable directory** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_library_directory"></span><span id="product_library_directory"></span><span id="PRODUCT_LIBRARY_DIRECTORY"></span>

<span data-ttu-id="178ee-164">**Diretório da biblioteca de produtos** (2)</span><span class="sxs-lookup"><span data-stu-id="178ee-164">**Product library directory** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_configuration_directory"></span><span id="product_configuration_directory"></span><span id="PRODUCT_CONFIGURATION_DIRECTORY"></span>

<span data-ttu-id="178ee-165">**Diretório de configuração do produto** (3)</span><span class="sxs-lookup"><span data-stu-id="178ee-165">**Product configuration directory** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_include_directory"></span><span id="product_include_directory"></span><span id="PRODUCT_INCLUDE_DIRECTORY"></span>

<span data-ttu-id="178ee-166">**Diretório de inclusão do produto** (4)</span><span class="sxs-lookup"><span data-stu-id="178ee-166">**Product include directory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_working_directory"></span><span id="product_working_directory"></span><span id="PRODUCT_WORKING_DIRECTORY"></span>

<span data-ttu-id="178ee-167">**Diretório de trabalho do produto** (5)</span><span class="sxs-lookup"><span data-stu-id="178ee-167">**Product working directory** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_log_directory"></span><span id="product_log_directory"></span><span id="PRODUCT_LOG_DIRECTORY"></span>

<span data-ttu-id="178ee-168">**Diretório de log do produto** (6)</span><span class="sxs-lookup"><span data-stu-id="178ee-168">**Product log directory** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_base_directory"></span><span id="shared_base_directory"></span><span id="SHARED_BASE_DIRECTORY"></span>

<span data-ttu-id="178ee-169">**Diretório base compartilhado** (7)</span><span class="sxs-lookup"><span data-stu-id="178ee-169">**Shared base directory** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_executable_directory"></span><span id="shared_executable_directory"></span><span id="SHARED_EXECUTABLE_DIRECTORY"></span>

<span data-ttu-id="178ee-170">**Diretório executável compartilhado** (8)</span><span class="sxs-lookup"><span data-stu-id="178ee-170">**Shared executable directory** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_library_directory"></span><span id="shared_library_directory"></span><span id="SHARED_LIBRARY_DIRECTORY"></span>

<span data-ttu-id="178ee-171">**Diretório de biblioteca compartilhada** (9)</span><span class="sxs-lookup"><span data-stu-id="178ee-171">**Shared library directory** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_include_directory"></span><span id="shared_include_directory"></span><span id="SHARED_INCLUDE_DIRECTORY"></span>

<span data-ttu-id="178ee-172">**Diretório de inclusão compartilhada** (10)</span><span class="sxs-lookup"><span data-stu-id="178ee-172">**Shared include directory** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="System_base_directory"></span><span id="system_base_directory"></span><span id="SYSTEM_BASE_DIRECTORY"></span>

<span data-ttu-id="178ee-173">**Diretório base do sistema** (11)</span><span class="sxs-lookup"><span data-stu-id="178ee-173">**System base directory** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="System_executable_directory"></span><span id="system_executable_directory"></span><span id="SYSTEM_EXECUTABLE_DIRECTORY"></span>

<span data-ttu-id="178ee-174">**Diretório executável do sistema** (12)</span><span class="sxs-lookup"><span data-stu-id="178ee-174">**System executable directory** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="System_library_directory"></span><span id="system_library_directory"></span><span id="SYSTEM_LIBRARY_DIRECTORY"></span>

<span data-ttu-id="178ee-175">**Diretório da biblioteca do sistema** (13)</span><span class="sxs-lookup"><span data-stu-id="178ee-175">**System library directory** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="System_configuration_directory"></span><span id="system_configuration_directory"></span><span id="SYSTEM_CONFIGURATION_DIRECTORY"></span>

<span data-ttu-id="178ee-176">**Diretório de configuração do sistema** (14)</span><span class="sxs-lookup"><span data-stu-id="178ee-176">**System configuration directory** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="System_include_directory"></span><span id="system_include_directory"></span><span id="SYSTEM_INCLUDE_DIRECTORY"></span>

<span data-ttu-id="178ee-177">**Diretório de inclusão do sistema** (15)</span><span class="sxs-lookup"><span data-stu-id="178ee-177">**System include directory** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="System_log_directory"></span><span id="system_log_directory"></span><span id="SYSTEM_LOG_DIRECTORY"></span>

<span data-ttu-id="178ee-178">**Diretório de log do sistema** (16)</span><span class="sxs-lookup"><span data-stu-id="178ee-178">**System log directory** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="178ee-179">**Outro** (17)</span><span class="sxs-lookup"><span data-stu-id="178ee-179">**Other** (17)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="178ee-180">**Nome**</span><span class="sxs-lookup"><span data-stu-id="178ee-180">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="178ee-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="178ee-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="178ee-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="178ee-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="178ee-183">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="178ee-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="178ee-184">Nome usado para identificar o elemento de software</span><span class="sxs-lookup"><span data-stu-id="178ee-184">Name used to identify the software element</span></span>

<span data-ttu-id="178ee-185">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="178ee-185">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="178ee-186">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="178ee-186">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="178ee-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="178ee-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="178ee-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="178ee-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="178ee-189">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="178ee-189">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="178ee-190">Este é um identificador para este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="178ee-190">This is an identifier for this software element.</span></span>

<span data-ttu-id="178ee-191">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="178ee-191">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="178ee-192">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="178ee-192">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="178ee-193">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="178ee-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="178ee-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="178ee-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="178ee-195">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="178ee-195">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="178ee-196">O estado do elemento de software de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="178ee-196">The software element state of a software element.</span></span>

<span data-ttu-id="178ee-197">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="178ee-197">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="178ee-198"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="178ee-198"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-199">Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="178ee-199">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="178ee-200"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="178ee-200"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-201">Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="178ee-201">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="178ee-202"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="178ee-202"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-203">Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="178ee-203">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="178ee-204"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="178ee-204"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-205">Descreve os detalhes necessários para monitorar e operar em um elemento inicial.</span><span class="sxs-lookup"><span data-stu-id="178ee-205">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="178ee-206">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="178ee-206">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="178ee-207">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="178ee-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="178ee-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="178ee-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="178ee-209">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informações do componente de software DMTF \| 2,5 ")</span><span class="sxs-lookup"><span data-stu-id="178ee-209">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="178ee-210">Sistema operacional de destino do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="178ee-210">Target operating system of the software element.</span></span>

<span data-ttu-id="178ee-211">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="178ee-211">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="178ee-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="178ee-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="178ee-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="178ee-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="178ee-214"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="178ee-214"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-215">Mac OS</span><span class="sxs-lookup"><span data-stu-id="178ee-215">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="178ee-216"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="178ee-216"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-217">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="178ee-217">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="178ee-218"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="178ee-218"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="178ee-219"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="178ee-219"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="178ee-220"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="178ee-220"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="178ee-221"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="178ee-221"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-222">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="178ee-222">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="178ee-223"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="178ee-223"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-224">HP-UX</span><span class="sxs-lookup"><span data-stu-id="178ee-224">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="178ee-225"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="178ee-225"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="178ee-226"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="178ee-226"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="178ee-227"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="178ee-227"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="178ee-228"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="178ee-228"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="178ee-229"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="178ee-229"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-230">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="178ee-230">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="178ee-231"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="178ee-231"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="178ee-232"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="178ee-232"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-233">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="178ee-233">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="178ee-234"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="178ee-234"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-235">Windows 95</span><span class="sxs-lookup"><span data-stu-id="178ee-235">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="178ee-236"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="178ee-236"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-237">Windows 98</span><span class="sxs-lookup"><span data-stu-id="178ee-237">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="178ee-238"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="178ee-238"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-239">Windows NT</span><span class="sxs-lookup"><span data-stu-id="178ee-239">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="178ee-240"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="178ee-240"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-241">Windows CE</span><span class="sxs-lookup"><span data-stu-id="178ee-241">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="178ee-242"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="178ee-242"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-243">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="178ee-243">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="178ee-244"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="178ee-244"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="178ee-245"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="178ee-245"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="178ee-246"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="178ee-246"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="178ee-247"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="178ee-247"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="178ee-248"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="178ee-248"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="178ee-249"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="178ee-249"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="178ee-250"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="178ee-250"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="178ee-251"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="178ee-251"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="178ee-252"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="178ee-252"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="178ee-253"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="178ee-253"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="178ee-254"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="178ee-254"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="178ee-255"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="178ee-255"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-256">Uma série</span><span class="sxs-lookup"><span data-stu-id="178ee-256">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="178ee-257"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="178ee-257"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-258">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="178ee-258">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="178ee-259"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="178ee-259"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-260">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="178ee-260">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="178ee-261"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="178ee-261"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-262">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="178ee-262">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="178ee-263"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="178ee-263"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="178ee-264"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="178ee-264"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="178ee-265"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="178ee-265"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="178ee-266"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="178ee-266"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="178ee-267"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="178ee-267"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="178ee-268"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="178ee-268"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-269">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="178ee-269">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="178ee-270"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="178ee-270"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="178ee-271"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="178ee-271"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="178ee-272"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="178ee-272"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="178ee-273"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="178ee-273"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-274">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="178ee-274">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="178ee-275"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="178ee-275"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="178ee-276"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="178ee-276"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="178ee-277"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="178ee-277"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="178ee-278"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="178ee-278"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="178ee-279"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="178ee-279"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="178ee-280"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="178ee-280"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="178ee-281"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="178ee-281"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="178ee-282"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="178ee-282"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="178ee-283"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="178ee-283"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="178ee-284"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="178ee-284"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="178ee-285"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="178ee-285"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="178ee-286">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="178ee-286">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="178ee-287"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="178ee-287"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="178ee-288"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="178ee-288"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="178ee-289"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="178ee-289"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="178ee-290"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="178ee-290"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="178ee-291"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="178ee-291"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="178ee-292">**Versão**</span><span class="sxs-lookup"><span data-stu-id="178ee-292">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="178ee-293">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="178ee-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="178ee-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="178ee-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="178ee-295">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Componente DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="178ee-295">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="178ee-296">Versão da operação.</span><span class="sxs-lookup"><span data-stu-id="178ee-296">Version of the operation.</span></span>

<span data-ttu-id="178ee-297">A versão da operação deve estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="178ee-297">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="178ee-298"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="178ee-298"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="178ee-299"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="178ee-299"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="178ee-300">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="178ee-300">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="178ee-301">Comentários</span><span class="sxs-lookup"><span data-stu-id="178ee-301">Remarks</span></span>

<span data-ttu-id="178ee-302">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="178ee-302">WMI does not implement this class.</span></span> <span data-ttu-id="178ee-303">Para classes derivadas do **CIM \_ DirectorySpecification**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="178ee-303">For classes derived from **CIM\_DirectorySpecification**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="178ee-304">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="178ee-304">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="178ee-305">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="178ee-305">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="178ee-306">Requisitos</span><span class="sxs-lookup"><span data-stu-id="178ee-306">Requirements</span></span>



| <span data-ttu-id="178ee-307">Requisito</span><span class="sxs-lookup"><span data-stu-id="178ee-307">Requirement</span></span> | <span data-ttu-id="178ee-308">Valor</span><span class="sxs-lookup"><span data-stu-id="178ee-308">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="178ee-309">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="178ee-309">Minimum supported client</span></span><br/> | <span data-ttu-id="178ee-310">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="178ee-310">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="178ee-311">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="178ee-311">Minimum supported server</span></span><br/> | <span data-ttu-id="178ee-312">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="178ee-312">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="178ee-313">Namespace</span><span class="sxs-lookup"><span data-stu-id="178ee-313">Namespace</span></span><br/>                | <span data-ttu-id="178ee-314">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="178ee-314">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="178ee-315">MOF</span><span class="sxs-lookup"><span data-stu-id="178ee-315">MOF</span></span><br/>                      | <dl> <span data-ttu-id="178ee-316"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="178ee-316"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="178ee-317">DLL</span><span class="sxs-lookup"><span data-stu-id="178ee-317">DLL</span></span><br/>                      | <dl> <span data-ttu-id="178ee-318"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="178ee-318"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="178ee-319">Confira também</span><span class="sxs-lookup"><span data-stu-id="178ee-319">See also</span></span>

<dl> <dt>

[<span data-ttu-id="178ee-320">**Verificação de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="178ee-320">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

