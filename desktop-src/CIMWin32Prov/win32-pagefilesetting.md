---
description: O Win32 \_ PageFileSetting&\# 8194; A classe WMI representa as configurações de um arquivo de paginação.
ms.assetid: 22190ede-1db6-4d69-ae74-63d10977cc78
ms.tgt_platform: multiple
title: Classe Win32_PageFileSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileSetting
- Win32_PageFileSetting.Caption
- Win32_PageFileSetting.Description
- Win32_PageFileSetting.SettingID
- Win32_PageFileSetting.InitialSize
- Win32_PageFileSetting.MaximumSize
- Win32_PageFileSetting.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b3ec2fa36e31cf9075f218f31d3063e3a298b8ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748261"
---
# <a name="win32_pagefilesetting-class"></a><span data-ttu-id="b7132-103">\_Classe Win32 PageFileSetting</span><span class="sxs-lookup"><span data-stu-id="b7132-103">Win32\_PageFileSetting class</span></span>

<span data-ttu-id="b7132-104">A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PageFileSetting do Win32** representa as configurações de um arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="b7132-104">The **Win32\_PageFileSetting** [WMI class](../wmisdk/retrieving-a-class.md) represents the settings of a page file.</span></span> <span data-ttu-id="b7132-105">As informações contidas nos objetos instanciados nessa classe especificam os parâmetros de arquivo de paginação usados quando o arquivo é criado na inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="b7132-105">Information contained within objects instantiated from this class specify the page file parameters used when the file is created at system startup.</span></span> <span data-ttu-id="b7132-106">As propriedades nessa classe podem ser modificadas e adiadas até a inicialização.</span><span class="sxs-lookup"><span data-stu-id="b7132-106">The properties in this class can be modified and deferred until startup.</span></span> <span data-ttu-id="b7132-107">Essas configurações são diferentes do estado de tempo de execução de um arquivo de paginação expresso por meio da classe associada [**Win32 \_ PageFileUsage**](win32-pagefileusage.md).</span><span class="sxs-lookup"><span data-stu-id="b7132-107">These settings are different from the run-time state of a page file expressed through the associated class [**Win32\_PageFileUsage**](win32-pagefileusage.md).</span></span>

<span data-ttu-id="b7132-108">Para criar uma instância dessa classe, habilite o privilégio **SeCreatePagefilePrivilege** .</span><span class="sxs-lookup"><span data-stu-id="b7132-108">To create an instance of this class, enable the **SeCreatePagefilePrivilege** privilege.</span></span> <span data-ttu-id="b7132-109">Para obter mais informações, consulte [**constantes de privilégio**](../wmisdk/privilege-constants.md) e [executando operações privilegiadas](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="b7132-109">For more information, see [**Privilege Constants**](../wmisdk/privilege-constants.md) and [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

<span data-ttu-id="b7132-110">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b7132-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b7132-111">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="b7132-111">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7132-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7132-112">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{514A9270-C856-11D2-B364-00105A1f77A1}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFileSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 InitialSize;
  uint32 MaximumSize;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="b7132-113">Membros</span><span class="sxs-lookup"><span data-stu-id="b7132-113">Members</span></span>

<span data-ttu-id="b7132-114">A classe **Win32 \_ PageFileSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b7132-114">The **Win32\_PageFileSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="b7132-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b7132-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7132-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b7132-116">Properties</span></span>

<span data-ttu-id="b7132-117">A classe **Win32 \_ PageFileSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b7132-117">The **Win32\_PageFileSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7132-118">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b7132-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7132-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7132-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7132-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7132-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7132-121">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="b7132-121">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b7132-122">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="b7132-122">Short textual description of the current object.</span></span>

<span data-ttu-id="b7132-123">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="b7132-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7132-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b7132-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7132-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7132-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7132-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7132-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7132-127">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="b7132-127">Textual description of the current object.</span></span>

<span data-ttu-id="b7132-128">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="b7132-128">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7132-129">**InitialSize**</span><span class="sxs-lookup"><span data-stu-id="b7132-129">**InitialSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7132-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7132-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7132-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b7132-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b7132-132">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="b7132-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="b7132-133">Tamanho inicial do arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="b7132-133">Initial size of the page file.</span></span>

<span data-ttu-id="b7132-134">Exemplo: 139</span><span class="sxs-lookup"><span data-stu-id="b7132-134">Example: 139</span></span>

</dd> <dt>

<span data-ttu-id="b7132-135">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="b7132-135">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7132-136">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7132-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7132-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b7132-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b7132-138">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="b7132-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="b7132-139">Tamanho máximo do arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="b7132-139">Maximum size of the page file.</span></span>

<span data-ttu-id="b7132-140">Exemplo: 178</span><span class="sxs-lookup"><span data-stu-id="b7132-140">Example: 178</span></span>

</dd> <dt>

<span data-ttu-id="b7132-141">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b7132-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7132-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7132-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7132-143">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b7132-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b7132-144">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b7132-144">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b7132-145">Caminho e nome de arquivo do arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="b7132-145">Path and file name of the page file.</span></span>

<span data-ttu-id="b7132-146">Exemplo: "C: \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="b7132-146">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="b7132-147">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="b7132-147">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7132-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7132-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7132-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7132-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7132-150">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="b7132-150">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b7132-151">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="b7132-151">Identifier by which the current object is known.</span></span>

<span data-ttu-id="b7132-152">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="b7132-152">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7132-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7132-153">Remarks</span></span>

<span data-ttu-id="b7132-154">A classe **Win32 \_ PageFileSetting** é derivada da [**\_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="b7132-154">The **Win32\_PageFileSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7132-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7132-155">Requirements</span></span>



| <span data-ttu-id="b7132-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7132-156">Requirement</span></span> | <span data-ttu-id="b7132-157">Valor</span><span class="sxs-lookup"><span data-stu-id="b7132-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7132-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7132-158">Minimum supported client</span></span><br/> | <span data-ttu-id="b7132-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7132-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b7132-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7132-160">Minimum supported server</span></span><br/> | <span data-ttu-id="b7132-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7132-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b7132-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7132-162">Namespace</span></span><br/>                | <span data-ttu-id="b7132-163">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b7132-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b7132-164">MOF</span><span class="sxs-lookup"><span data-stu-id="b7132-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7132-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7132-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7132-166">DLL</span><span class="sxs-lookup"><span data-stu-id="b7132-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7132-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7132-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7132-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7132-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7132-169">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b7132-169">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="b7132-170">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="b7132-170">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
