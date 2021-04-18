---
description: A \_ classe CIM Fileespecífication representa um arquivo que está ligado ou desligado do sistema.
ms.assetid: 25d6cc79-1497-4615-9251-8e00524dff1b
ms.tgt_platform: multiple
title: Classe CIM_FileSpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileSpecification
- CIM_FileSpecification.CheckID
- CIM_FileSpecification.Caption
- CIM_FileSpecification.Description
- CIM_FileSpecification.CheckMode
- CIM_FileSpecification.TargetOperatingSystem
- CIM_FileSpecification.Version
- CIM_FileSpecification.SoftwareElementID
- CIM_FileSpecification.SoftwareElementState
- CIM_FileSpecification.Name
- CIM_FileSpecification.CheckSum
- CIM_FileSpecification.CRC1
- CIM_FileSpecification.CRC2
- CIM_FileSpecification.CreateTimeStamp
- CIM_FileSpecification.FileSize
- CIM_FileSpecification.MD5Checksum
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 503cf9678d2be7a3afb3f8c205f0d042b4bcaec2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751993"
---
# <a name="cim_filespecification-class"></a><span data-ttu-id="ae666-103">\_Classe de Respecificação de CIM</span><span class="sxs-lookup"><span data-stu-id="ae666-103">CIM\_FileSpecification class</span></span>

<span data-ttu-id="ae666-104">A classe **CIM \_ fileespecífication** representa um arquivo que está ligado ou desligado do sistema.</span><span class="sxs-lookup"><span data-stu-id="ae666-104">The **CIM\_FileSpecification** class represents a file that is either on or off of the system.</span></span> <span data-ttu-id="ae666-105">O arquivo está localizado no diretório identificado pela Associação de [**\_ DirectorySpecificationFile do CIM**](cim-directoryspecificationfile.md) .</span><span class="sxs-lookup"><span data-stu-id="ae666-105">The file is located in the directory identified by the [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association.</span></span> <span data-ttu-id="ae666-106">O método [**Invoke**](invoke-method-in-class-cim-filespecification.md) usa as informações para verificar a existência do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ae666-106">The [**Invoke**](invoke-method-in-class-cim-filespecification.md) method uses the information to check for the file's existence.</span></span> <span data-ttu-id="ae666-107">Observe que as propriedades com um valor **nulo** não são verificadas.</span><span class="sxs-lookup"><span data-stu-id="ae666-107">Note that properties with a **Null** value are not checked.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae666-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="ae666-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ae666-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ae666-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ae666-110">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ae666-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ae666-111">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="ae666-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae666-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae666-112">Syntax</span></span>

``` syntax
[UUID("{41F377B0-DB2A-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_FileSpecification : CIM_Check
{
  string   CheckID;
  string   Caption;
  string   Description;
  boolean  CheckMode;
  uint16   TargetOperatingSystem;
  string   Version;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Name;
  uint32   CheckSum;
  uint32   CRC1;
  uint32   CRC2;
  datetime CreateTimeStamp;
  uint64   FileSize;
  string   MD5Checksum;
};
```

## <a name="members"></a><span data-ttu-id="ae666-113">Membros</span><span class="sxs-lookup"><span data-stu-id="ae666-113">Members</span></span>

<span data-ttu-id="ae666-114">A classe **CIM \_ fileespecífication** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ae666-114">The **CIM\_FileSpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="ae666-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="ae666-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="ae666-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ae666-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ae666-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="ae666-117">Methods</span></span>

<span data-ttu-id="ae666-118">A classe **CIM \_ fileespecífication** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ae666-118">The **CIM\_FileSpecification** class has these methods.</span></span>



| <span data-ttu-id="ae666-119">Método</span><span class="sxs-lookup"><span data-stu-id="ae666-119">Method</span></span>                                                         | <span data-ttu-id="ae666-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae666-120">Description</span></span>                                                      |
|:---------------------------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="ae666-121">**Chame**</span><span class="sxs-lookup"><span data-stu-id="ae666-121">**Invoke**</span></span>](invoke-method-in-class-cim-filespecification.md) | <span data-ttu-id="ae666-122">Avalia uma verificação específica.</span><span class="sxs-lookup"><span data-stu-id="ae666-122">Evaluates a particular check.</span></span> <span data-ttu-id="ae666-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ae666-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ae666-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ae666-124">Properties</span></span>

<span data-ttu-id="ae666-125">A classe **CIM \_ fileespecífication** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ae666-125">The **CIM\_FileSpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae666-126">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="ae666-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae666-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae666-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae666-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae666-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae666-129">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ae666-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ae666-130">Uma breve descrição textual do assunto.</span><span class="sxs-lookup"><span data-stu-id="ae666-130">A short textual description of the subject.</span></span>

<span data-ttu-id="ae666-131">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="ae666-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae666-132">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="ae666-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae666-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae666-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae666-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae666-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae666-135">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ae666-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ae666-136">Identificador usado em conjunto com outras chaves para identificar exclusivamente a verificação.</span><span class="sxs-lookup"><span data-stu-id="ae666-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="ae666-137">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="ae666-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae666-138">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="ae666-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae666-139">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ae666-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae666-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae666-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae666-141">Se for **true**, espera-se que a condição exista no ambiente.</span><span class="sxs-lookup"><span data-stu-id="ae666-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="ae666-142">Por exemplo, espera-se que um arquivo esteja em um sistema, portanto, o método [**Invoke**](invoke-method-in-class-cim-check.md) deve retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="ae666-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="ae666-143">Se for **false**, a condição não deverá existir.</span><span class="sxs-lookup"><span data-stu-id="ae666-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="ae666-144">Por exemplo, um arquivo não está em um sistema, portanto, o método [**Invoke**](invoke-method-in-class-cim-check.md) deve retornar **false**.</span><span class="sxs-lookup"><span data-stu-id="ae666-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="ae666-145">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="ae666-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae666-146">**Soma**</span><span class="sxs-lookup"><span data-stu-id="ae666-146">**CheckSum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae666-147">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae666-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae666-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae666-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae666-149">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Assinatura de software DMTF \| 2,4 ")</span><span class="sxs-lookup"><span data-stu-id="ae666-149">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="ae666-150">Valor calculado como a soma de 16 bits dos primeiros 32 bytes do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ae666-150">Value calculated as the 16-bit sum of the file's first 32 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ae666-151">**CRC1**</span><span class="sxs-lookup"><span data-stu-id="ae666-151">**CRC1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae666-152">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae666-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae666-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae666-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae666-154">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Assinatura de software DMTF \| 2,5 ")</span><span class="sxs-lookup"><span data-stu-id="ae666-154">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="ae666-155">Valor de CRC calculado usando o meio 512 KB.</span><span class="sxs-lookup"><span data-stu-id="ae666-155">CRC value calculated using the middle 512 KB.</span></span>

</dd> <dt>

<span data-ttu-id="ae666-156">**CRC2**</span><span class="sxs-lookup"><span data-stu-id="ae666-156">**CRC2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae666-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae666-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae666-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae666-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae666-159">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Assinatura de software DMTF \| 2,6 ")</span><span class="sxs-lookup"><span data-stu-id="ae666-159">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="ae666-160">Valor de CRC para o meio 512 KB do arquivo, módulo 3.</span><span class="sxs-lookup"><span data-stu-id="ae666-160">CRC value for the middle 512 KB of the file, modulo 3.</span></span>

</dd> <dt>

<span data-ttu-id="ae666-161">**Createtimestamp**</span><span class="sxs-lookup"><span data-stu-id="ae666-161">**CreateTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae666-162">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ae666-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ae666-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae666-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae666-164">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ae666-164">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ae666-165">Data e hora de criação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ae666-165">File creation date and time.</span></span>

</dd> <dt>

<span data-ttu-id="ae666-166">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ae666-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae666-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae666-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae666-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae666-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae666-169">Uma descrição dos objetos.</span><span class="sxs-lookup"><span data-stu-id="ae666-169">A description of the objects.</span></span>

<span data-ttu-id="ae666-170">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="ae666-170">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae666-171">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="ae666-171">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae666-172">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ae666-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ae666-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae666-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae666-174">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="ae666-174">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="ae666-175">Tamanho do arquivo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ae666-175">Size of the file, in bytes.</span></span>

<span data-ttu-id="ae666-176">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ae666-176">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="ae666-177">**MD5Checksum**</span><span class="sxs-lookup"><span data-stu-id="ae666-177">**MD5Checksum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae666-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae666-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae666-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae666-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae666-180">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16)</span><span class="sxs-lookup"><span data-stu-id="ae666-180">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16)</span></span>
</dt> </dl>

<span data-ttu-id="ae666-181">Algoritmo para calcular uma soma de verificação de 128 bits para qualquer arquivo ou objeto.</span><span class="sxs-lookup"><span data-stu-id="ae666-181">Algorithm for computing a 128-bit checksum for any file or object.</span></span> <span data-ttu-id="ae666-182">A probabilidade de dois arquivos diferentes que produzem a mesma soma de verificação MD5 é muito pequena (cerca de 1 em 2 ^ 64), e a soma de verificação MD5 de um arquivo pode ser usada para construir um identificador de conteúdo confiável que provavelmente identificará exclusivamente o arquivo.</span><span class="sxs-lookup"><span data-stu-id="ae666-182">The likelihood of two different files producing the same MD5 checksum is very small (about 1 in 2^64), and the MD5 checksum of a file can be used to construct a reliable content identifier that is likely to uniquely identify the file.</span></span> <span data-ttu-id="ae666-183">O inverso também é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="ae666-183">The reverse is also true.</span></span> <span data-ttu-id="ae666-184">Se dois arquivos tiverem a mesma soma de verificação MD5, é muito provável que os arquivos sejam idênticos.</span><span class="sxs-lookup"><span data-stu-id="ae666-184">If two files have the same MD5 checksum, it is very likely that the files are identical.</span></span> <span data-ttu-id="ae666-185">Para fins de especificação do MOF da propriedade MD5, o algoritmo MD5 sempre gera uma cadeia de caracteres de caractere de 32.</span><span class="sxs-lookup"><span data-stu-id="ae666-185">For purposes of MOF specification of the MD5 property, the MD5 algorithm always generates a 32-character string.</span></span> <span data-ttu-id="ae666-186">Por exemplo, a cadeia de caracteres "abcdefghijklmnopqrstuvwxyz" gera a cadeia de caracteres "c3fcd3d76192e4007dfb496cca67e13b".</span><span class="sxs-lookup"><span data-stu-id="ae666-186">For example, the string "abcdefghijklmnopqrstuvwxyz" generates the string "c3fcd3d76192e4007dfb496cca67e13b".</span></span> <span data-ttu-id="ae666-187">Para obter mais informações sobre como implementar o algoritmo MD5, consulte [RFC 1321](https://www.ietf.org/rfc/rfc1321.txt).</span><span class="sxs-lookup"><span data-stu-id="ae666-187">For more information about implementing the MD5 algorithm, see [RFC 1321](https://www.ietf.org/rfc/rfc1321.txt).</span></span>

</dd> <dt>

<span data-ttu-id="ae666-188">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ae666-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae666-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae666-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae666-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae666-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae666-191">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Name), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="ae666-191">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Name), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="ae666-192">O nome do arquivo ou o nome do arquivo com um prefixo de diretório.</span><span class="sxs-lookup"><span data-stu-id="ae666-192">Either the name of the file or the name of the file with a directory prefix.</span></span>

</dd> <dt>

<span data-ttu-id="ae666-193">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="ae666-193">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae666-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae666-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae666-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae666-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae666-196">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ae666-196">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ae666-197">Este é um identificador para este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="ae666-197">This is an identifier for this software element.</span></span>

<span data-ttu-id="ae666-198">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="ae666-198">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae666-199">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="ae666-199">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae666-200">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae666-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae666-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae666-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae666-202">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ae666-202">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ae666-203">O estado do elemento de software de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="ae666-203">The software element state of a software element.</span></span>

<span data-ttu-id="ae666-204">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="ae666-204">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="ae666-205"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="ae666-205"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-206">Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="ae666-206">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="ae666-207"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="ae666-207"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-208">Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="ae666-208">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="ae666-209"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="ae666-209"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-210">Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="ae666-210">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="ae666-211"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="ae666-211"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-212">Descreve os detalhes necessários para monitorar e operar em um elemento inicial.</span><span class="sxs-lookup"><span data-stu-id="ae666-212">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ae666-213">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="ae666-213">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae666-214">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae666-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae666-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae666-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae666-216">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informações do componente de software DMTF \| 2,5 ")</span><span class="sxs-lookup"><span data-stu-id="ae666-216">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="ae666-217">Sistema operacional de destino do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="ae666-217">Target operating system of the software element.</span></span>

<span data-ttu-id="ae666-218">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="ae666-218">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae666-219"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="ae666-219"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ae666-220"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="ae666-220"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="ae666-221"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="ae666-221"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-222">Mac OS</span><span class="sxs-lookup"><span data-stu-id="ae666-222">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="ae666-223"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="ae666-223"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-224">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="ae666-224">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="ae666-225"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="ae666-225"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="ae666-226"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="ae666-226"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="ae666-227"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="ae666-227"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="ae666-228"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="ae666-228"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-229">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="ae666-229">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="ae666-230"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="ae666-230"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-231">HP-UX</span><span class="sxs-lookup"><span data-stu-id="ae666-231">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="ae666-232"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="ae666-232"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="ae666-233"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="ae666-233"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="ae666-234"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="ae666-234"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="ae666-235"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="ae666-235"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="ae666-236"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="ae666-236"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-237">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="ae666-237">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="ae666-238"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="ae666-238"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="ae666-239"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="ae666-239"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-240">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="ae666-240">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="ae666-241"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="ae666-241"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-242">Windows 95</span><span class="sxs-lookup"><span data-stu-id="ae666-242">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="ae666-243"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="ae666-243"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-244">Windows 98</span><span class="sxs-lookup"><span data-stu-id="ae666-244">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="ae666-245"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="ae666-245"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-246">Windows NT</span><span class="sxs-lookup"><span data-stu-id="ae666-246">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="ae666-247"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="ae666-247"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-248">Windows CE</span><span class="sxs-lookup"><span data-stu-id="ae666-248">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="ae666-249"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="ae666-249"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-250">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="ae666-250">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="ae666-251"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="ae666-251"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="ae666-252"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="ae666-252"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="ae666-253"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="ae666-253"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="ae666-254"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="ae666-254"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="ae666-255"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="ae666-255"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="ae666-256"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="ae666-256"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="ae666-257"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="ae666-257"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="ae666-258"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="ae666-258"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="ae666-259"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="ae666-259"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="ae666-260"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="ae666-260"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="ae666-261"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="ae666-261"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="ae666-262"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="ae666-262"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-263">Uma série</span><span class="sxs-lookup"><span data-stu-id="ae666-263">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="ae666-264"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="ae666-264"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-265">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="ae666-265">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="ae666-266"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="ae666-266"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-267">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="ae666-267">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="ae666-268"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="ae666-268"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-269">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="ae666-269">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="ae666-270"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="ae666-270"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="ae666-271"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="ae666-271"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="ae666-272"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="ae666-272"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="ae666-273"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="ae666-273"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="ae666-274"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="ae666-274"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="ae666-275"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="ae666-275"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-276">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="ae666-276">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="ae666-277"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="ae666-277"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="ae666-278"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="ae666-278"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="ae666-279"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="ae666-279"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="ae666-280"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="ae666-280"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-281">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="ae666-281">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="ae666-282"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="ae666-282"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="ae666-283"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="ae666-283"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="ae666-284"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="ae666-284"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="ae666-285"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="ae666-285"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="ae666-286"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="ae666-286"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="ae666-287"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="ae666-287"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="ae666-288"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="ae666-288"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="ae666-289"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="ae666-289"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="ae666-290"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="ae666-290"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="ae666-291"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="ae666-291"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="ae666-292"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="ae666-292"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="ae666-293">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="ae666-293">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="ae666-294"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="ae666-294"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="ae666-295"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="ae666-295"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="ae666-296"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="ae666-296"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="ae666-297"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="ae666-297"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="ae666-298"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="ae666-298"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae666-299">**Versão**</span><span class="sxs-lookup"><span data-stu-id="ae666-299">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae666-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae666-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae666-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae666-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae666-302">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Componente DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="ae666-302">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="ae666-303">Versão da operação.</span><span class="sxs-lookup"><span data-stu-id="ae666-303">Version of the operation.</span></span>

<span data-ttu-id="ae666-304">A versão da operação deve estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="ae666-304">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="ae666-305"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="ae666-305"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="ae666-306"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="ae666-306"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="ae666-307">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="ae666-307">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae666-308">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae666-308">Remarks</span></span>

<span data-ttu-id="ae666-309">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="ae666-309">WMI does not implement this class.</span></span> <span data-ttu-id="ae666-310">Para classes derivadas de **do \_ CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ae666-310">For classes derived from **CIM\_FileSpecification**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ae666-311">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="ae666-311">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ae666-312">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="ae666-312">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae666-313">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae666-313">Requirements</span></span>



| <span data-ttu-id="ae666-314">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae666-314">Requirement</span></span> | <span data-ttu-id="ae666-315">Valor</span><span class="sxs-lookup"><span data-stu-id="ae666-315">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae666-316">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae666-316">Minimum supported client</span></span><br/> | <span data-ttu-id="ae666-317">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae666-317">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae666-318">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae666-318">Minimum supported server</span></span><br/> | <span data-ttu-id="ae666-319">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae666-319">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae666-320">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae666-320">Namespace</span></span><br/>                | <span data-ttu-id="ae666-321">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ae666-321">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ae666-322">MOF</span><span class="sxs-lookup"><span data-stu-id="ae666-322">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae666-323"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae666-323"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae666-324">DLL</span><span class="sxs-lookup"><span data-stu-id="ae666-324">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae666-325"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae666-325"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae666-326">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae666-326">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae666-327">**Verificação de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ae666-327">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

