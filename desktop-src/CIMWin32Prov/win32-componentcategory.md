---
description: A \_ classe WMI ComponentCategory do Win32 representa uma categoria de componente.
ms.assetid: 9c6fc856-8300-4fa5-ae1c-a7d6476f5c51
ms.tgt_platform: multiple
title: Classe Win32_ComponentCategory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComponentCategory
- Win32_ComponentCategory.Caption
- Win32_ComponentCategory.Description
- Win32_ComponentCategory.InstallDate
- Win32_ComponentCategory.Status
- Win32_ComponentCategory.CategoryId
- Win32_ComponentCategory.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1730abf9058f5068def4a01f0d7e7601b9c69e53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920495"
---
# <a name="win32_componentcategory-class"></a><span data-ttu-id="5ec17-103">\_Classe Win32 ComponentCategory</span><span class="sxs-lookup"><span data-stu-id="5ec17-103">Win32\_ComponentCategory class</span></span>

<span data-ttu-id="5ec17-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ComponentCategory do Win32** representa uma categoria de componente.</span><span class="sxs-lookup"><span data-stu-id="5ec17-104">The **Win32\_ComponentCategory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a component category.</span></span> <span data-ttu-id="5ec17-105">Categorias de componente são grupos de classes de Component Object Model (COM) com um conjunto de funcionalidades definido compartilhado entre eles.</span><span class="sxs-lookup"><span data-stu-id="5ec17-105">Component categories are groups of Component Object Model (COM) classes with a defined functionality set shared between them.</span></span> <span data-ttu-id="5ec17-106">Um cliente que usa essas interfaces consulta o registro quanto ao título da categoria e ao identificador exclusivo chamado **CategoryID**, que é criado a partir de um GUID (identificador global exclusivo).</span><span class="sxs-lookup"><span data-stu-id="5ec17-106">A client using these interfaces queries the registry for the category title and unique identifier called **CategoryID**, which is created from a globally unique identifier (GUID).</span></span>

<span data-ttu-id="5ec17-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5ec17-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5ec17-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5ec17-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ec17-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ec17-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED5A-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComponentCategory : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CategoryId;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="5ec17-110">Membros</span><span class="sxs-lookup"><span data-stu-id="5ec17-110">Members</span></span>

<span data-ttu-id="5ec17-111">A classe **Win32 \_ ComponentCategory** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5ec17-111">The **Win32\_ComponentCategory** class has these types of members:</span></span>

-   [<span data-ttu-id="5ec17-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5ec17-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ec17-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5ec17-113">Properties</span></span>

<span data-ttu-id="5ec17-114">A classe **Win32 \_ ComponentCategory** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5ec17-114">The **Win32\_ComponentCategory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ec17-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="5ec17-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ec17-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ec17-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ec17-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ec17-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ec17-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5ec17-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5ec17-119">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5ec17-119">A short textual description of the object.</span></span>

<span data-ttu-id="5ec17-120">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ec17-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ec17-121">**Categoria**</span><span class="sxs-lookup"><span data-stu-id="5ec17-121">**CategoryId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ec17-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ec17-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ec17-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ec17-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ec17-124">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| categorias de componente win32api \| [**CategoryInfo**](/windows/win32/api/comcat/ns-comcat-categoryinfo) \| CATID")</span><span class="sxs-lookup"><span data-stu-id="5ec17-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (16), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Component Categories\|[**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo)\|catid")</span></span>
</dt> </dl>

<span data-ttu-id="5ec17-125">GUID para esta categoria de componente.</span><span class="sxs-lookup"><span data-stu-id="5ec17-125">GUID for this component category.</span></span>

</dd> <dt>

<span data-ttu-id="5ec17-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5ec17-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ec17-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ec17-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ec17-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ec17-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ec17-129">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="5ec17-129">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5ec17-130">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5ec17-130">A textual description of the object.</span></span>

<span data-ttu-id="5ec17-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ec17-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ec17-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5ec17-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ec17-133">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5ec17-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5ec17-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ec17-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ec17-135">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="5ec17-135">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5ec17-136">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="5ec17-136">Indicates when the object was installed.</span></span> <span data-ttu-id="5ec17-137">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="5ec17-137">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5ec17-138">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ec17-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ec17-139">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5ec17-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ec17-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ec17-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ec17-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ec17-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ec17-142">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| categorias de componente \| [**CategoryInfo**](/windows/win32/api/comcat/ns-comcat-categoryinfo) \| szDescription")</span><span class="sxs-lookup"><span data-stu-id="5ec17-142">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Component Categories\|[**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo)\|szDescription")</span></span>
</dt> </dl>

<span data-ttu-id="5ec17-143">A propriedade Name indica um nome descritivo dessa categoria de componente.</span><span class="sxs-lookup"><span data-stu-id="5ec17-143">The Name property indicates a descriptive name of this component category.</span></span>

</dd> <dt>

<span data-ttu-id="5ec17-144">**Status**</span><span class="sxs-lookup"><span data-stu-id="5ec17-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ec17-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ec17-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ec17-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ec17-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ec17-147">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5ec17-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5ec17-148">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5ec17-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="5ec17-149">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="5ec17-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="5ec17-150">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="5ec17-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5ec17-151">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="5ec17-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5ec17-152">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="5ec17-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5ec17-153">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="5ec17-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5ec17-154">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="5ec17-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5ec17-155">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ec17-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5ec17-156">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5ec17-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5ec17-157">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5ec17-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5ec17-158">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="5ec17-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5ec17-159">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5ec17-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5ec17-160">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="5ec17-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5ec17-161">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5ec17-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5ec17-162">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="5ec17-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5ec17-163">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="5ec17-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5ec17-164">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="5ec17-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5ec17-165">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="5ec17-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5ec17-166">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5ec17-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5ec17-167">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="5ec17-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5ec17-168">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="5ec17-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="5ec17-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5ec17-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="5ec17-170">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ec17-170">Remarks</span></span>

<span data-ttu-id="5ec17-171">A classe **Win32 \_ ComponentCategory** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ec17-171">The **Win32\_ComponentCategory** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ec17-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ec17-172">Requirements</span></span>



| <span data-ttu-id="5ec17-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ec17-173">Requirement</span></span> | <span data-ttu-id="5ec17-174">Valor</span><span class="sxs-lookup"><span data-stu-id="5ec17-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec17-175">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ec17-175">Minimum supported client</span></span><br/> | <span data-ttu-id="5ec17-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ec17-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ec17-177">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ec17-177">Minimum supported server</span></span><br/> | <span data-ttu-id="5ec17-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ec17-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ec17-179">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ec17-179">Namespace</span></span><br/>                | <span data-ttu-id="5ec17-180">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5ec17-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5ec17-181">MOF</span><span class="sxs-lookup"><span data-stu-id="5ec17-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ec17-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ec17-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ec17-183">DLL</span><span class="sxs-lookup"><span data-stu-id="5ec17-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ec17-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ec17-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ec17-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ec17-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec17-186">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="5ec17-186">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="5ec17-187">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5ec17-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

