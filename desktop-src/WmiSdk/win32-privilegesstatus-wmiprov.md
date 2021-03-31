---
description: O Win32 \_ PrivilegesStatus &\# 8194; A classe WMI relata informações sobre os privilégios necessários para concluir uma operação. Ele pode ser retornado quando uma operação falha ou quando uma instância parcialmente preenchida tiver sido retornada.
ms.assetid: 85bda855-1488-4d7a-99ed-798e9859fef7
ms.tgt_platform: multiple
title: Classe Win32_PrivilegesStatus (WMI)
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
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 658803be4e70849531bf52e7368e4e9cbcc2f0a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171961"
---
# <a name="win32_privilegesstatus-class-wmi"></a><span data-ttu-id="96c3a-104">Classe Win32_PrivilegesStatus (WMI)</span><span class="sxs-lookup"><span data-stu-id="96c3a-104">Win32_PrivilegesStatus class (WMI)</span></span>

<span data-ttu-id="96c3a-105">A [classe WMI](retrieving-a-class.md) **\_ PrivilegesStatus do Win32** relata informações sobre os privilégios necessários para concluir uma operação.   </span><span class="sxs-lookup"><span data-stu-id="96c3a-105">The **Win32\_PrivilegesStatus**   [WMI class](retrieving-a-class.md) reports information about privileges required to complete an operation.</span></span> <span data-ttu-id="96c3a-106">Ele pode ser retornado quando uma operação falha ou quando uma instância parcialmente preenchida tiver sido retornada.</span><span class="sxs-lookup"><span data-stu-id="96c3a-106">It may be returned when an operation failed or when a partially populated instance has been returned.</span></span>

<span data-ttu-id="96c3a-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="96c3a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="96c3a-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="96c3a-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="96c3a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96c3a-109">Syntax</span></span>

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}")]
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

## <a name="members"></a><span data-ttu-id="96c3a-110">Membros</span><span class="sxs-lookup"><span data-stu-id="96c3a-110">Members</span></span>

<span data-ttu-id="96c3a-111">A classe **Win32 \_ PrivilegesStatus** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="96c3a-111">The **Win32\_PrivilegesStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="96c3a-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="96c3a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96c3a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="96c3a-113">Properties</span></span>

<span data-ttu-id="96c3a-114">A classe **Win32 \_ PrivilegesStatus** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="96c3a-114">The **Win32\_PrivilegesStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96c3a-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="96c3a-115">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96c3a-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="96c3a-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96c3a-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="96c3a-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96c3a-118">Qualquer cadeia de caracteres definida pelo usuário que descreva um erro ou status operacional.</span><span class="sxs-lookup"><span data-stu-id="96c3a-118">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="96c3a-119">Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="96c3a-119">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="96c3a-120">**Operação**</span><span class="sxs-lookup"><span data-stu-id="96c3a-120">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96c3a-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="96c3a-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96c3a-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="96c3a-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96c3a-123">Operação que ocorre no momento de uma falha ou anomalia.</span><span class="sxs-lookup"><span data-stu-id="96c3a-123">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="96c3a-124">Normalmente, Instrumentação de Gerenciamento do Windows (WMI) define essa propriedade como o nome de uma API COM para o método WMI, como o seguinte: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="96c3a-124">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="96c3a-125">Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="96c3a-125">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="96c3a-126">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="96c3a-126">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96c3a-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="96c3a-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96c3a-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="96c3a-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96c3a-129">Parâmetros envolvidos em um erro ou alteração de status.</span><span class="sxs-lookup"><span data-stu-id="96c3a-129">Parameters involved in an error or status change.</span></span> <span data-ttu-id="96c3a-130">Por exemplo, se um aplicativo tentar recuperar uma classe que não existe, essa propriedade será definida como o nome da classe incorreta.</span><span class="sxs-lookup"><span data-stu-id="96c3a-130">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="96c3a-131">Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="96c3a-131">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="96c3a-132">**PrivilegesNotHeld**</span><span class="sxs-lookup"><span data-stu-id="96c3a-132">**PrivilegesNotHeld**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96c3a-133">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="96c3a-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="96c3a-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="96c3a-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96c3a-135">Listando os privilégios de acesso necessários ausentes para concluir uma operação.</span><span class="sxs-lookup"><span data-stu-id="96c3a-135">Listing required access privileges missing to complete an operation.</span></span> <span data-ttu-id="96c3a-136">Os tipos de privilégios de acesso podem ser encontrados sob os privilégios do Windows.</span><span class="sxs-lookup"><span data-stu-id="96c3a-136">The types of access privileges can be found under the Windows Privileges.</span></span>

<span data-ttu-id="96c3a-137">Exemplo: "SE \_ nome de desligamento \_ "</span><span class="sxs-lookup"><span data-stu-id="96c3a-137">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="96c3a-138">**PrivilegesRequired**</span><span class="sxs-lookup"><span data-stu-id="96c3a-138">**PrivilegesRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96c3a-139">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="96c3a-139">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="96c3a-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="96c3a-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96c3a-141">Listagem de todos os privilégios necessários para executar uma operação.</span><span class="sxs-lookup"><span data-stu-id="96c3a-141">Listing of all of the privileges required to perform an operation.</span></span> <span data-ttu-id="96c3a-142">Isso inclui valores da propriedade **PrivilegesNotHeld** .</span><span class="sxs-lookup"><span data-stu-id="96c3a-142">This includes values from the **PrivilegesNotHeld** property.</span></span>

<span data-ttu-id="96c3a-143">Exemplo: "SE \_ nome de desligamento \_ "</span><span class="sxs-lookup"><span data-stu-id="96c3a-143">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="96c3a-144">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="96c3a-144">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96c3a-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="96c3a-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96c3a-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="96c3a-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96c3a-147">Identifica o provedor que causa ou relata um erro ou uma alteração de status.</span><span class="sxs-lookup"><span data-stu-id="96c3a-147">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="96c3a-148">Se um provedor não estiver envolvido, essa cadeia de caracteres será definida como "Gerenciamento do Windows".</span><span class="sxs-lookup"><span data-stu-id="96c3a-148">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="96c3a-149">Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="96c3a-149">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="96c3a-150">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="96c3a-150">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96c3a-151">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96c3a-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96c3a-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="96c3a-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96c3a-153">Contém um código de erro ou informações para uma operação.</span><span class="sxs-lookup"><span data-stu-id="96c3a-153">Contains an error or information code for an operation.</span></span> <span data-ttu-id="96c3a-154">Pode ser qualquer valor definido pelo provedor, mas o valor 0 (zero) geralmente é reservado para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="96c3a-154">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="96c3a-155">Essa propriedade é herdada de [**\_ \_ NotifyStatus**](--notifystatus.md).</span><span class="sxs-lookup"><span data-stu-id="96c3a-155">This property is inherited from [**\_\_NotifyStatus**](--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96c3a-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="96c3a-156">Remarks</span></span>

<span data-ttu-id="96c3a-157">A classe **Win32 \_ PrivilegesStatus** é derivada de [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="96c3a-157">The **Win32\_PrivilegesStatus** class is derived from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="96c3a-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96c3a-158">Requirements</span></span>



| <span data-ttu-id="96c3a-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="96c3a-159">Requirement</span></span> | <span data-ttu-id="96c3a-160">Valor</span><span class="sxs-lookup"><span data-stu-id="96c3a-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="96c3a-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96c3a-161">Minimum supported client</span></span><br/> | <span data-ttu-id="96c3a-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96c3a-162">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="96c3a-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96c3a-163">Minimum supported server</span></span><br/> | <span data-ttu-id="96c3a-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96c3a-164">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="96c3a-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="96c3a-165">Namespace</span></span><br/>                | <span data-ttu-id="96c3a-166">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="96c3a-166">Root\\WMI</span></span><br/>                                                               |
| <span data-ttu-id="96c3a-167">MOF</span><span class="sxs-lookup"><span data-stu-id="96c3a-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96c3a-168"><dt>WMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96c3a-168"><dt>Wmi.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96c3a-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="96c3a-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c3a-170">**\_\_ExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="96c3a-170">**\_\_ExtendedStatus**</span></span>](--extendedstatus.md)
</dt> </dl>

 

 




