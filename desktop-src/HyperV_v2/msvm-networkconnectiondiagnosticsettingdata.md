---
description: Representa as configurações usadas para testar a conectividade de rede de uma máquina virtual.
ms.assetid: d719d9c9-7ca9-40a0-ada8-185b8cd44c22
title: Classe Msvm_NetworkConnectionDiagnosticSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticSettingData
- Msvm_NetworkConnectionDiagnosticSettingData.IsSender
- Msvm_NetworkConnectionDiagnosticSettingData.SenderIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverMac
- Msvm_NetworkConnectionDiagnosticSettingData.IsolationId
- Msvm_NetworkConnectionDiagnosticSettingData.SequenceNumber
- Msvm_NetworkConnectionDiagnosticSettingData.PayloadSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ec0df1957df6c925cf12ce363c89a0bdad52d3e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011730"
---
# <a name="msvm_networkconnectiondiagnosticsettingdata-class"></a><span data-ttu-id="0b35b-103">\_Classe Msvm NetworkConnectionDiagnosticSettingData</span><span class="sxs-lookup"><span data-stu-id="0b35b-103">Msvm\_NetworkConnectionDiagnosticSettingData class</span></span>

<span data-ttu-id="0b35b-104">Representa as configurações usadas para testar a conectividade de rede de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0b35b-104">Represents the settings used to test the network connectivity of a virtual machine.</span></span> <span data-ttu-id="0b35b-105">Usado pelo método [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0b35b-105">Used by the [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="0b35b-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0b35b-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b35b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b35b-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticSettingData : CIM_SettingData
{
  boolean IsSender;
  string  SenderIP;
  string  ReceiverIP;
  string  ReceiverMac;
  uint32  IsolationId;
  uint32  SequenceNumber;
  uint32  PayloadSize;
};
```

## <a name="members"></a><span data-ttu-id="0b35b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0b35b-108">Members</span></span>

<span data-ttu-id="0b35b-109">A classe **Msvm \_ NetworkConnectionDiagnosticSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0b35b-109">The **Msvm\_NetworkConnectionDiagnosticSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0b35b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b35b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b35b-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b35b-111">Properties</span></span>

<span data-ttu-id="0b35b-112">A classe **Msvm \_ NetworkConnectionDiagnosticSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0b35b-112">The **Msvm\_NetworkConnectionDiagnosticSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b35b-113">**Isolamentoid**</span><span class="sxs-lookup"><span data-stu-id="0b35b-113">**IsolationId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35b-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b35b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b35b-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b35b-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0b35b-116">A ID de isolamento.</span><span class="sxs-lookup"><span data-stu-id="0b35b-116">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="0b35b-117">**Isenviador**</span><span class="sxs-lookup"><span data-stu-id="0b35b-117">**IsSender**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35b-118">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0b35b-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b35b-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b35b-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0b35b-120">Indica se este método está sendo invocado no remetente ou no destinatário.</span><span class="sxs-lookup"><span data-stu-id="0b35b-120">Indicates whether this method is being invoked at the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="0b35b-121">**PayloadSize**</span><span class="sxs-lookup"><span data-stu-id="0b35b-121">**PayloadSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35b-122">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b35b-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b35b-123">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b35b-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0b35b-124">O tamanho da carga.</span><span class="sxs-lookup"><span data-stu-id="0b35b-124">The payload size.</span></span>

</dd> <dt>

<span data-ttu-id="0b35b-125">**ReceiverIP**</span><span class="sxs-lookup"><span data-stu-id="0b35b-125">**ReceiverIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35b-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b35b-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b35b-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b35b-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0b35b-128">O endereço IP do destinatário.</span><span class="sxs-lookup"><span data-stu-id="0b35b-128">The receiver IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0b35b-129">**ReceiverMac**</span><span class="sxs-lookup"><span data-stu-id="0b35b-129">**ReceiverMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35b-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b35b-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b35b-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b35b-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0b35b-132">O endereço MAC do destinatário.</span><span class="sxs-lookup"><span data-stu-id="0b35b-132">The receiver MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="0b35b-133">**SenderIP**</span><span class="sxs-lookup"><span data-stu-id="0b35b-133">**SenderIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35b-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b35b-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b35b-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b35b-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0b35b-136">O endereço IP do remetente.</span><span class="sxs-lookup"><span data-stu-id="0b35b-136">The sender IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0b35b-137">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="0b35b-137">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35b-138">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b35b-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b35b-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b35b-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0b35b-140">O número de sequência.</span><span class="sxs-lookup"><span data-stu-id="0b35b-140">The sequence number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b35b-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b35b-141">Requirements</span></span>



| <span data-ttu-id="0b35b-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b35b-142">Requirement</span></span> | <span data-ttu-id="0b35b-143">Valor</span><span class="sxs-lookup"><span data-stu-id="0b35b-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b35b-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b35b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="0b35b-145">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="0b35b-145">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0b35b-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b35b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="0b35b-147">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0b35b-147">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0b35b-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b35b-148">Namespace</span></span><br/>                | <span data-ttu-id="0b35b-149">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0b35b-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0b35b-150">MOF</span><span class="sxs-lookup"><span data-stu-id="0b35b-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b35b-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b35b-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b35b-152">DLL</span><span class="sxs-lookup"><span data-stu-id="0b35b-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b35b-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0b35b-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0b35b-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b35b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b35b-155">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="0b35b-155">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




