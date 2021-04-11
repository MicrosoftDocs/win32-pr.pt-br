---
description: Representa uma entrada de autorização para um servidor de recuperação.
ms.assetid: 8c057b39-7102-4fbf-b4be-f18627a88834
title: Classe Msvm_ReplicationAuthorizationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationAuthorizationSettingData
- Msvm_ReplicationAuthorizationSettingData.InstanceID
- Msvm_ReplicationAuthorizationSettingData.Caption
- Msvm_ReplicationAuthorizationSettingData.Description
- Msvm_ReplicationAuthorizationSettingData.ElementName
- Msvm_ReplicationAuthorizationSettingData.AllowedPrimaryHostSystem
- Msvm_ReplicationAuthorizationSettingData.TrustGroup
- Msvm_ReplicationAuthorizationSettingData.ReplicaStorageLocation
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ba069de1bbe005e8a2a06891db8218ab313baa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169729"
---
# <a name="msvm_replicationauthorizationsettingdata-class"></a><span data-ttu-id="413ec-103">\_Classe Msvm ReplicationAuthorizationSettingData</span><span class="sxs-lookup"><span data-stu-id="413ec-103">Msvm\_ReplicationAuthorizationSettingData class</span></span>

<span data-ttu-id="413ec-104">Representa uma entrada de autorização para um servidor de recuperação.</span><span class="sxs-lookup"><span data-stu-id="413ec-104">Represents an authorization entry for a recovery server.</span></span>

<span data-ttu-id="413ec-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="413ec-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="413ec-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="413ec-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationAuthorizationSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string AllowedPrimaryHostSystem;
  string TrustGroup;
  string ReplicaStorageLocation;
};
```

## <a name="members"></a><span data-ttu-id="413ec-107">Membros</span><span class="sxs-lookup"><span data-stu-id="413ec-107">Members</span></span>

<span data-ttu-id="413ec-108">A classe **Msvm \_ ReplicationAuthorizationSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="413ec-108">The **Msvm\_ReplicationAuthorizationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="413ec-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="413ec-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="413ec-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="413ec-110">Properties</span></span>

<span data-ttu-id="413ec-111">A classe **Msvm \_ ReplicationAuthorizationSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="413ec-111">The **Msvm\_ReplicationAuthorizationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="413ec-112">**AllowedPrimaryHostSystem**</span><span class="sxs-lookup"><span data-stu-id="413ec-112">**AllowedPrimaryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="413ec-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="413ec-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="413ec-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="413ec-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="413ec-115">O nome de domínio totalmente qualificado ou o nome de grupo dos servidores primários que têm permissão para replicar para esse servidor de recuperação.</span><span class="sxs-lookup"><span data-stu-id="413ec-115">The fully qualified domain name or group name of the primary servers that are allowed to replicate to this recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="413ec-116">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="413ec-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="413ec-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="413ec-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="413ec-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="413ec-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="413ec-119">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="413ec-119">A short description of the object.</span></span> <span data-ttu-id="413ec-120">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="413ec-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="413ec-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="413ec-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="413ec-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="413ec-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="413ec-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="413ec-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="413ec-124">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="413ec-124">A description of the object.</span></span> <span data-ttu-id="413ec-125">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="413ec-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="413ec-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="413ec-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="413ec-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="413ec-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="413ec-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="413ec-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="413ec-129">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="413ec-129">A display name for the object.</span></span> <span data-ttu-id="413ec-130">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="413ec-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="413ec-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="413ec-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="413ec-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="413ec-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="413ec-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="413ec-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="413ec-134">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="413ec-134">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="413ec-135">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="413ec-135">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="413ec-136">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="413ec-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="413ec-137">**ReplicaStorageLocation**</span><span class="sxs-lookup"><span data-stu-id="413ec-137">**ReplicaStorageLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="413ec-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="413ec-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="413ec-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="413ec-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="413ec-140">O local onde os arquivos de replicação do **AllowedPrimaryHostSystem** serão armazenados.</span><span class="sxs-lookup"><span data-stu-id="413ec-140">The location where replication files from the **AllowedPrimaryHostSystem** will be stored.</span></span>

</dd> <dt>

<span data-ttu-id="413ec-141">**Filetrust**</span><span class="sxs-lookup"><span data-stu-id="413ec-141">**TrustGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="413ec-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="413ec-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="413ec-143">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="413ec-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="413ec-144">O nome do grupo de confiança para a entrada de autorização.</span><span class="sxs-lookup"><span data-stu-id="413ec-144">The name of the trust group for the authorization entry.</span></span> <span data-ttu-id="413ec-145">Isso identifica as várias entradas de autorização que são agrupadas juntas.</span><span class="sxs-lookup"><span data-stu-id="413ec-145">This identifies the multiple authorization entries that are grouped together.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="413ec-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="413ec-146">Requirements</span></span>



| <span data-ttu-id="413ec-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="413ec-147">Requirement</span></span> | <span data-ttu-id="413ec-148">Valor</span><span class="sxs-lookup"><span data-stu-id="413ec-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="413ec-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="413ec-149">Minimum supported client</span></span><br/> | <span data-ttu-id="413ec-150">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="413ec-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="413ec-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="413ec-151">Minimum supported server</span></span><br/> | <span data-ttu-id="413ec-152">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="413ec-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="413ec-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="413ec-153">Namespace</span></span><br/>                | <span data-ttu-id="413ec-154">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="413ec-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="413ec-155">MOF</span><span class="sxs-lookup"><span data-stu-id="413ec-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="413ec-156"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="413ec-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="413ec-157">DLL</span><span class="sxs-lookup"><span data-stu-id="413ec-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="413ec-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="413ec-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="413ec-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="413ec-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="413ec-160">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="413ec-160">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="413ec-161">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="413ec-161">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="413ec-162">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="413ec-162">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="413ec-163">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="413ec-163">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> </dl>

 

