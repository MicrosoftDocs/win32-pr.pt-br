---
description: O Win32 \_ PrivilegesStatus&\# 8194; A classe WMI relata informações sobre os privilégios necessários para concluir uma operação. Ele pode ser retornado quando uma operação falha ou quando uma instância parcialmente preenchida tiver sido retornada.
ms.assetid: 295ec2bd-7996-4031-8503-d4e869d8368d
ms.tgt_platform: multiple
title: Classe Win32_PrivilegesStatus (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrivilegesStatus
- Win32_PrivilegesStatus.Description
- Win32_PrivilegesStatus.Operation
- Win32_PrivilegesStatus.ParameterInfo
- Win32_PrivilegesStatus.ProviderName
- Win32_PrivilegesStatus.StatusCode
- Win32_PrivilegesStatus.PrivilegesNotHeld
- Win32_PrivilegesStatus.PrivilegesRequired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ab399ce08374a954b3bbc015cfee7b4d20167b70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826414"
---
# <a name="win32_privilegesstatus-class-cimwin32-wmi-providers"></a><span data-ttu-id="d4099-104">Classe Win32_PrivilegesStatus (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="d4099-104">Win32_PrivilegesStatus class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="d4099-105">A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PrivilegesStatus do Win32** relata informações sobre os privilégios necessários para concluir uma operação.</span><span class="sxs-lookup"><span data-stu-id="d4099-105">The **Win32\_PrivilegesStatus** [WMI class](../wmisdk/retrieving-a-class.md) reports information about privileges required to complete an operation.</span></span> <span data-ttu-id="d4099-106">Ele pode ser retornado quando uma operação falha ou quando uma instância parcialmente preenchida tiver sido retornada.</span><span class="sxs-lookup"><span data-stu-id="d4099-106">It may be returned when an operation failed or when a partially populated instance has been returned.</span></span>

<span data-ttu-id="d4099-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d4099-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d4099-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="d4099-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4099-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4099-109">Syntax</span></span>

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}"), AMENDMENT]
class Win32_PrivilegesStatus : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string PrivilegesNotHeld[];
  string PrivilegesRequired[];
};
```

## <a name="members"></a><span data-ttu-id="d4099-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d4099-110">Members</span></span>

<span data-ttu-id="d4099-111">A classe **Win32 \_ PrivilegesStatus** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d4099-111">The **Win32\_PrivilegesStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="d4099-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d4099-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d4099-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d4099-113">Properties</span></span>

<span data-ttu-id="d4099-114">A classe **Win32 \_ PrivilegesStatus** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d4099-114">The **Win32\_PrivilegesStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d4099-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d4099-115">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4099-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4099-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4099-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4099-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4099-118">Qualquer cadeia de caracteres definida pelo usuário que descreva um erro ou status operacional.</span><span class="sxs-lookup"><span data-stu-id="d4099-118">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="d4099-119">Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="d4099-119">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4099-120">**Operação**</span><span class="sxs-lookup"><span data-stu-id="d4099-120">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4099-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4099-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4099-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4099-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4099-123">Operação que ocorre no momento de uma falha ou anomalia.</span><span class="sxs-lookup"><span data-stu-id="d4099-123">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="d4099-124">Normalmente, Instrumentação de Gerenciamento do Windows (WMI) define essa propriedade como o nome de uma API COM para o método WMI, como o seguinte: [**IWbemServices:: CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="d4099-124">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="d4099-125">Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="d4099-125">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4099-126">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="d4099-126">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4099-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4099-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4099-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4099-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4099-129">Parâmetros envolvidos em um erro ou alteração de status.</span><span class="sxs-lookup"><span data-stu-id="d4099-129">Parameters involved in an error or status change.</span></span> <span data-ttu-id="d4099-130">Por exemplo, se um aplicativo tentar recuperar uma classe que não existe, essa propriedade será definida como o nome da classe incorreta.</span><span class="sxs-lookup"><span data-stu-id="d4099-130">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="d4099-131">Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="d4099-131">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4099-132">**PrivilegesNotHeld**</span><span class="sxs-lookup"><span data-stu-id="d4099-132">**PrivilegesNotHeld**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4099-133">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4099-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d4099-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4099-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4099-135">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| AccessControl \| Privileges do Windows NT")</span><span class="sxs-lookup"><span data-stu-id="d4099-135">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|AccessControl\|Windows NT Privileges")</span></span>
</dt> </dl>

<span data-ttu-id="d4099-136">Listando os privilégios de acesso necessários ausentes para concluir uma operação.</span><span class="sxs-lookup"><span data-stu-id="d4099-136">Listing required access privileges missing to complete an operation.</span></span> <span data-ttu-id="d4099-137">Os tipos de privilégios de acesso podem ser encontrados sob os privilégios do Windows.</span><span class="sxs-lookup"><span data-stu-id="d4099-137">The types of access privileges can be found under the Windows Privileges.</span></span>

<span data-ttu-id="d4099-138">Exemplo: "SE \_ nome de desligamento \_ "</span><span class="sxs-lookup"><span data-stu-id="d4099-138">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="d4099-139">**PrivilegesRequired**</span><span class="sxs-lookup"><span data-stu-id="d4099-139">**PrivilegesRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4099-140">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4099-140">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d4099-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4099-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4099-142">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| AccessControl \| Privileges do Windows NT")</span><span class="sxs-lookup"><span data-stu-id="d4099-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|AccessControl\|Windows NT Privileges")</span></span>
</dt> </dl>

<span data-ttu-id="d4099-143">Listagem de todos os privilégios necessários para executar uma operação.</span><span class="sxs-lookup"><span data-stu-id="d4099-143">Listing of all of the privileges required to perform an operation.</span></span> <span data-ttu-id="d4099-144">Isso inclui valores da propriedade **PrivilegesNotHeld** .</span><span class="sxs-lookup"><span data-stu-id="d4099-144">This includes values from the **PrivilegesNotHeld** property.</span></span>

<span data-ttu-id="d4099-145">Exemplo: "SE \_ nome de desligamento \_ "</span><span class="sxs-lookup"><span data-stu-id="d4099-145">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="d4099-146">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="d4099-146">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4099-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4099-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4099-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4099-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4099-149">Identifica o provedor que causa ou relata um erro ou uma alteração de status.</span><span class="sxs-lookup"><span data-stu-id="d4099-149">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="d4099-150">Se um provedor não estiver envolvido, essa cadeia de caracteres será definida como "Gerenciamento do Windows".</span><span class="sxs-lookup"><span data-stu-id="d4099-150">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="d4099-151">Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="d4099-151">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4099-152">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="d4099-152">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4099-153">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4099-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4099-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4099-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4099-155">Contém um código de erro ou informações para uma operação.</span><span class="sxs-lookup"><span data-stu-id="d4099-155">Contains an error or information code for an operation.</span></span> <span data-ttu-id="d4099-156">Pode ser qualquer valor definido pelo provedor, mas o valor 0 (zero) geralmente é reservado para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="d4099-156">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span>

<span data-ttu-id="d4099-157">Essa propriedade é herdada de [**\_ \_ NotifyStatus**](../wmisdk/--notifystatus.md).</span><span class="sxs-lookup"><span data-stu-id="d4099-157">This property is inherited from [**\_\_NotifyStatus**](../wmisdk/--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4099-158">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4099-158">Remarks</span></span>

<span data-ttu-id="d4099-159">A classe **Win32 \_ PrivilegesStatus** é derivada de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="d4099-159">The **Win32\_PrivilegesStatus** class is derived from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4099-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4099-160">Requirements</span></span>



| <span data-ttu-id="d4099-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4099-161">Requirement</span></span> | <span data-ttu-id="d4099-162">Valor</span><span class="sxs-lookup"><span data-stu-id="d4099-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4099-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4099-163">Minimum supported client</span></span><br/> | <span data-ttu-id="d4099-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4099-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d4099-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4099-165">Minimum supported server</span></span><br/> | <span data-ttu-id="d4099-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4099-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d4099-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="d4099-167">Namespace</span></span><br/>                | <span data-ttu-id="d4099-168">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d4099-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d4099-169">MOF</span><span class="sxs-lookup"><span data-stu-id="d4099-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4099-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4099-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4099-171">DLL</span><span class="sxs-lookup"><span data-stu-id="d4099-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4099-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4099-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4099-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4099-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4099-174">**\_\_ExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="d4099-174">**\_\_ExtendedStatus**</span></span>](../wmisdk/--extendedstatus.md)
</dt> </dl>

 

 
