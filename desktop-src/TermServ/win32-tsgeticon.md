---
title: Classe Win32_TSGetIcon
description: Retorna o conteúdo do ícone especificado pelo caminho e pelo índice do arquivo.
ms.assetid: c0ab50f1-f5a9-4f5e-8280-40c638f09e1c
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGetIcon Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGetIcon classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSGetIcon
- Win32_TSGetIcon.Caption
- Win32_TSGetIcon.Description
- Win32_TSGetIcon.InstallDate
- Win32_TSGetIcon.Name
- Win32_TSGetIcon.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0186e158f025be8e8a5e6cf3e87f3ad5d8b296
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918547"
---
# <a name="win32_tsgeticon-class"></a><span data-ttu-id="8bbc9-105">\_Classe Win32 TSGetIcon</span><span class="sxs-lookup"><span data-stu-id="8bbc9-105">Win32\_TSGetIcon class</span></span>

<span data-ttu-id="8bbc9-106">Retorna o conteúdo do ícone especificado pelo caminho e o índice do arquivo</span><span class="sxs-lookup"><span data-stu-id="8bbc9-106">Returns the contents of the icon specified by file path and index</span></span>

<span data-ttu-id="8bbc9-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8bbc9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bbc9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8bbc9-108">Syntax</span></span>

``` syntax
class Win32_TSGetIcon : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="8bbc9-109">Membros</span><span class="sxs-lookup"><span data-stu-id="8bbc9-109">Members</span></span>

<span data-ttu-id="8bbc9-110">A classe **Win32 \_ TSGetIcon** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8bbc9-110">The **Win32\_TSGetIcon** class has these types of members:</span></span>

-   [<span data-ttu-id="8bbc9-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="8bbc9-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="8bbc9-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8bbc9-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8bbc9-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="8bbc9-113">Methods</span></span>

<span data-ttu-id="8bbc9-114">A classe **Win32 \_ TSGetIcon** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8bbc9-114">The **Win32\_TSGetIcon** class has these methods.</span></span>



| <span data-ttu-id="8bbc9-115">Método</span><span class="sxs-lookup"><span data-stu-id="8bbc9-115">Method</span></span>                                     | <span data-ttu-id="8bbc9-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8bbc9-116">Description</span></span>                                            |
|:-------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="8bbc9-117">**GetIcon**</span><span class="sxs-lookup"><span data-stu-id="8bbc9-117">**GetIcon**</span></span>](geticon-win32-tsgeticon.md) | <span data-ttu-id="8bbc9-118">Retorna o conteúdo do ícone especificado.</span><span class="sxs-lookup"><span data-stu-id="8bbc9-118">Returns the contents of the specified icon.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8bbc9-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8bbc9-119">Properties</span></span>

<span data-ttu-id="8bbc9-120">A classe **Win32 \_ TSGetIcon** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8bbc9-120">The **Win32\_TSGetIcon** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8bbc9-121">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="8bbc9-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bbc9-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8bbc9-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bbc9-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bbc9-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bbc9-124">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8bbc9-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8bbc9-125">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="8bbc9-125">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="8bbc9-126">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8bbc9-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bbc9-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8bbc9-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bbc9-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8bbc9-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bbc9-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bbc9-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bbc9-130">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="8bbc9-130">Description of the object.</span></span>

<span data-ttu-id="8bbc9-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8bbc9-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bbc9-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8bbc9-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bbc9-133">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8bbc9-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8bbc9-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bbc9-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bbc9-135">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="8bbc9-135">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="8bbc9-136">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="8bbc9-136">The date the object was installed.</span></span> <span data-ttu-id="8bbc9-137">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="8bbc9-137">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8bbc9-138">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8bbc9-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bbc9-139">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8bbc9-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bbc9-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8bbc9-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bbc9-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bbc9-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bbc9-142">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="8bbc9-142">The name of the object.</span></span>

<span data-ttu-id="8bbc9-143">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8bbc9-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bbc9-144">**Status**</span><span class="sxs-lookup"><span data-stu-id="8bbc9-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bbc9-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8bbc9-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bbc9-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bbc9-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bbc9-147">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="8bbc9-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="8bbc9-148">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="8bbc9-148">Current status of the object.</span></span> <span data-ttu-id="8bbc9-149">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="8bbc9-149">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8bbc9-150">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="8bbc9-150">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8bbc9-151">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="8bbc9-151">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8bbc9-152">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="8bbc9-152">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8bbc9-153">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="8bbc9-153">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8bbc9-154">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8bbc9-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="8bbc9-155">("OK")</span><span class="sxs-lookup"><span data-stu-id="8bbc9-155">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8bbc9-156">("Erro")</span><span class="sxs-lookup"><span data-stu-id="8bbc9-156">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8bbc9-157">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="8bbc9-157">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8bbc9-158">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="8bbc9-158">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8bbc9-159">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8bbc9-159">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8bbc9-160">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="8bbc9-160">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8bbc9-161">("Parando")</span><span class="sxs-lookup"><span data-stu-id="8bbc9-161">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8bbc9-162">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="8bbc9-162">("Service")</span></span>


<span data-ttu-id="8bbc9-163"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8bbc9-163"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="8bbc9-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bbc9-164">Requirements</span></span>



| <span data-ttu-id="8bbc9-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bbc9-165">Requirement</span></span> | <span data-ttu-id="8bbc9-166">Valor</span><span class="sxs-lookup"><span data-stu-id="8bbc9-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bbc9-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bbc9-167">Minimum supported client</span></span><br/> | <span data-ttu-id="8bbc9-168">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8bbc9-168">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8bbc9-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bbc9-169">Minimum supported server</span></span><br/> | <span data-ttu-id="8bbc9-170">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8bbc9-170">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="8bbc9-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="8bbc9-171">Namespace</span></span><br/>                | <span data-ttu-id="8bbc9-172">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="8bbc9-172">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8bbc9-173">MOF</span><span class="sxs-lookup"><span data-stu-id="8bbc9-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bbc9-174"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bbc9-174"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="8bbc9-175">DLL</span><span class="sxs-lookup"><span data-stu-id="8bbc9-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bbc9-176"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bbc9-176"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

