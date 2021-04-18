---
description: Descreve os recursos do VirtualSystemManagementService Msvm associado \_ .
ms.assetid: 3a167b06-bddd-4bac-95c0-ecf14e01eec0
title: Classe Msvm_VirtualSystemManagementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementCapabilities
- Msvm_VirtualSystemManagementCapabilities.InstanceID
- Msvm_VirtualSystemManagementCapabilities.Caption
- Msvm_VirtualSystemManagementCapabilities.Description
- Msvm_VirtualSystemManagementCapabilities.ElementName
- Msvm_VirtualSystemManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemManagementCapabilities.MaxElementNameLen
- Msvm_VirtualSystemManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemManagementCapabilities.ElementNameMask
- Msvm_VirtualSystemManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualSystemManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualSystemManagementCapabilities.IndicationsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24bc8ce66393a5e9ccd13848ab74640aec8d1760
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296207"
---
# <a name="msvm_virtualsystemmanagementcapabilities-class"></a><span data-ttu-id="c5858-103">\_Classe Msvm VirtualSystemManagementCapabilities</span><span class="sxs-lookup"><span data-stu-id="c5858-103">Msvm\_VirtualSystemManagementCapabilities class</span></span>

<span data-ttu-id="c5858-104">Descreve os recursos do [**\_ VirtualSystemManagementService Msvm**](msvm-virtualsystemmanagementservice.md)associado.</span><span class="sxs-lookup"><span data-stu-id="c5858-104">Describes the capabilities of the associated [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md).</span></span>

<span data-ttu-id="c5858-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c5858-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5858-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5858-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Management Service Capabilities";
  string  Description = "Defines Virtual System Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual System Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="c5858-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c5858-107">Members</span></span>

<span data-ttu-id="c5858-108">A classe **Msvm \_ VirtualSystemManagementCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c5858-108">The **Msvm\_VirtualSystemManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="c5858-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c5858-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5858-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c5858-110">Properties</span></span>

<span data-ttu-id="c5858-111">A classe **Msvm \_ VirtualSystemManagementCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c5858-111">The **Msvm\_VirtualSystemManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5858-112">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="c5858-112">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5858-113">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5858-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c5858-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5858-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5858-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. AsynchronousMethodsSupported")</span><span class="sxs-lookup"><span data-stu-id="c5858-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="c5858-116">Especifica os métodos [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) que têm suporte de forma assíncrona pela implementação.</span><span class="sxs-lookup"><span data-stu-id="c5858-116">Specifies the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) methods that are supported asynchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c5858-117">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c5858-117">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="ValidatePlannedSystem"></span><span id="validateplannedsystem"></span><span id="VALIDATEPLANNEDSYSTEM"></span>

<span data-ttu-id="c5858-118">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span><span class="sxs-lookup"><span data-stu-id="c5858-118">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSystemDefinition"></span><span id="importsystemdefinition"></span><span id="IMPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="c5858-119">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span><span class="sxs-lookup"><span data-stu-id="c5858-119">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSnapshotDefinitions"></span><span id="importsnapshotdefinitions"></span><span id="IMPORTSNAPSHOTDEFINITIONS"></span>

<span data-ttu-id="c5858-120">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span><span class="sxs-lookup"><span data-stu-id="c5858-120">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="RealizePlannedSystem"></span><span id="realizeplannedsystem"></span><span id="REALIZEPLANNEDSYSTEM"></span>

<span data-ttu-id="c5858-121">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span><span class="sxs-lookup"><span data-stu-id="c5858-121">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span></span>


</dt> <dd></dd> <dt>

<span id="ExportSystemDefinition"></span><span id="exportsystemdefinition"></span><span id="EXPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="c5858-122">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span><span class="sxs-lookup"><span data-stu-id="c5858-122">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>

<span data-ttu-id="c5858-123">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span><span class="sxs-lookup"><span data-stu-id="c5858-123">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>

<span data-ttu-id="c5858-124">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span><span class="sxs-lookup"><span data-stu-id="c5858-124">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>

<span data-ttu-id="c5858-125">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span><span class="sxs-lookup"><span data-stu-id="c5858-125">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="GetVirtualSystemThumbnailImage"></span><span id="getvirtualsystemthumbnailimage"></span><span id="GETVIRTUALSYSTEMTHUMBNAILIMAGE"></span>

<span data-ttu-id="c5858-126">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span><span class="sxs-lookup"><span data-stu-id="c5858-126">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyServiceSettings"></span><span id="modifyservicesettings"></span><span id="MODIFYSERVICESETTINGS"></span>

<span data-ttu-id="c5858-127">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span><span class="sxs-lookup"><span data-stu-id="c5858-127">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSummaryInformation"></span><span id="getsummaryinformation"></span><span id="GETSUMMARYINFORMATION"></span>

<span data-ttu-id="c5858-128">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span><span class="sxs-lookup"><span data-stu-id="c5858-128">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="AddKvpItems"></span><span id="addkvpitems"></span><span id="ADDKVPITEMS"></span>

<span data-ttu-id="c5858-129">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span><span class="sxs-lookup"><span data-stu-id="c5858-129">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyKvpItems"></span><span id="modifykvpitems"></span><span id="MODIFYKVPITEMS"></span>

<span data-ttu-id="c5858-130">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span><span class="sxs-lookup"><span data-stu-id="c5858-130">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveKvpItems"></span><span id="removekvpitems"></span><span id="REMOVEKVPITEMS"></span>

<span data-ttu-id="c5858-131">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span><span class="sxs-lookup"><span data-stu-id="c5858-131">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="FormatError"></span><span id="formaterror"></span><span id="FORMATERROR"></span>

<span data-ttu-id="c5858-132">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span><span class="sxs-lookup"><span data-stu-id="c5858-132">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="RequestStateChangeSupported"></span><span id="requeststatechangesupported"></span><span id="REQUESTSTATECHANGESUPPORTED"></span>

<span data-ttu-id="c5858-133">**RequestStateChangeSupported** (32789)</span><span class="sxs-lookup"><span data-stu-id="c5858-133">**RequestStateChangeSupported** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="StartServiceSupported"></span><span id="startservicesupported"></span><span id="STARTSERVICESUPPORTED"></span>

<span data-ttu-id="c5858-134">**StartServiceSupported** (32790)</span><span class="sxs-lookup"><span data-stu-id="c5858-134">**StartServiceSupported** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="StopServiceSupported"></span><span id="stopservicesupported"></span><span id="STOPSERVICESUPPORTED"></span>

<span data-ttu-id="c5858-135">**StopServiceSupported** (32791)</span><span class="sxs-lookup"><span data-stu-id="c5858-135">**StopServiceSupported** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyDiskMergeSettings"></span><span id="modifydiskmergesettings"></span><span id="MODIFYDISKMERGESETTINGS"></span>

<span data-ttu-id="c5858-136">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span><span class="sxs-lookup"><span data-stu-id="c5858-136">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span></span>


</dt> <dd></dd> <dt>

<span id="GenerateWwpn"></span><span id="generatewwpn"></span><span id="GENERATEWWPN"></span>

<span data-ttu-id="c5858-137">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span><span class="sxs-lookup"><span data-stu-id="c5858-137">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFibreChannelChap"></span><span id="addfibrechannelchap"></span><span id="ADDFIBRECHANNELCHAP"></span>

<span data-ttu-id="c5858-138">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span><span class="sxs-lookup"><span data-stu-id="c5858-138">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFibreChannelChap"></span><span id="removefibrechannelchap"></span><span id="REMOVEFIBRECHANNELCHAP"></span>

<span data-ttu-id="c5858-139">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span><span class="sxs-lookup"><span data-stu-id="c5858-139">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span></span>


</dt> <dd></dd> <dt>

<span id="SetGuestNetworkAdapterConfiguration"></span><span id="setguestnetworkadapterconfiguration"></span><span id="SETGUESTNETWORKADAPTERCONFIGURATION"></span>

<span data-ttu-id="c5858-140">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span><span class="sxs-lookup"><span data-stu-id="c5858-140">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSizeOfSystemFiles"></span><span id="getsizeofsystemfiles"></span><span id="GETSIZEOFSYSTEMFILES"></span>

<span data-ttu-id="c5858-141">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span><span class="sxs-lookup"><span data-stu-id="c5858-141">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span></span>


</dt> <dd></dd> <dt>

<span id="GetCurrentWwpnFromGenerator"></span><span id="getcurrentwwpnfromgenerator"></span><span id="GETCURRENTWWPNFROMGENERATOR"></span>

<span data-ttu-id="c5858-142">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span><span class="sxs-lookup"><span data-stu-id="c5858-142">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="c5858-143">**Fornecedor reservado** (32799.. 65535)</span><span class="sxs-lookup"><span data-stu-id="c5858-143">**Vendor Reserved** (32799..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c5858-144">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c5858-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5858-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5858-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5858-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5858-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5858-147">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="c5858-147">A short description of the object.</span></span> <span data-ttu-id="c5858-148">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c5858-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c5858-149">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c5858-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5858-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5858-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5858-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5858-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5858-152">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="c5858-152">A description of the object.</span></span> <span data-ttu-id="c5858-153">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c5858-153">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c5858-154">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c5858-154">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5858-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5858-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5858-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5858-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5858-157">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="c5858-157">A display name for the object.</span></span> <span data-ttu-id="c5858-158">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c5858-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c5858-159">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="c5858-159">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5858-160">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c5858-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c5858-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5858-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5858-162">Indica se a propriedade **ElementName** pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="c5858-162">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="c5858-163">Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="c5858-163">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="c5858-164">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="c5858-164">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5858-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5858-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5858-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5858-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5858-167">Especifica as restrições em **ElementName**, expressas como uma expressão regular.</span><span class="sxs-lookup"><span data-stu-id="c5858-167">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="c5858-168">Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="c5858-168">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="c5858-169">**IndicationsSupported**</span><span class="sxs-lookup"><span data-stu-id="c5858-169">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5858-170">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5858-170">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c5858-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5858-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5858-172">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. IndicationsSupported")</span><span class="sxs-lookup"><span data-stu-id="c5858-172">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.IndicationsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="c5858-173">Especifica as indicações com suporte na implementação.</span><span class="sxs-lookup"><span data-stu-id="c5858-173">Specifies the indications supported by the implementation.</span></span>

<span data-ttu-id="c5858-174">Enumeração de identificadores de indicação, cada um identificando uma indicação com suporte da implementação.</span><span class="sxs-lookup"><span data-stu-id="c5858-174">Enumeration of indication identifiers each identifying an indication that is supported by the implementation.</span></span>

<dt>

<span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="c5858-175"><span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualResourceStateChangeIndicationsSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="c5858-175"><span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualResourceStateChangeIndicationsSupported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c5858-176">A implementação dá suporte à notificação de alterações de estado de instâncias de [**\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) que representam recursos de sistemas virtuais.</span><span class="sxs-lookup"><span data-stu-id="c5858-176">The implementation supports notification of state changes of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) instances representing resources of virtual systems.</span></span>

</dd> <dt>

<span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="c5858-177"><span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>**ConcreteJobStateChangeIndicationsSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="c5858-177"><span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>**ConcreteJobStateChangeIndicationsSupported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c5858-178">A implementação dá suporte à notificação de alterações de estado de instâncias do [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c5858-178">The implementation supports notification of state changes of [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) instances.</span></span>

</dd> <dt>

<span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="c5858-179"><span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualSystemStateChangeIndicationsSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="c5858-179"><span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualSystemStateChangeIndicationsSupported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c5858-180">A implementação dá suporte à notificação de alterações de estado de instâncias de [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representam sistemas virtuais.</span><span class="sxs-lookup"><span data-stu-id="c5858-180">The implementation supports notification of state changes of [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instances representing virtual systems.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c5858-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c5858-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="c5858-182"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="c5858-182"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c5858-183">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c5858-183">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5858-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5858-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5858-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5858-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5858-186">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="c5858-186">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c5858-187">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="c5858-187">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c5858-188">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c5858-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c5858-189">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="c5858-189">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5858-190">Tipo de dados: **unit16**</span><span class="sxs-lookup"><span data-stu-id="c5858-190">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="c5858-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5858-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5858-192">Qualificadores: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="c5858-192">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c5858-193">Especifica o comprimento máximo com suporte da propriedade **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="c5858-193">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="c5858-194">Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="c5858-194">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="c5858-195">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="c5858-195">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5858-196">Tipo de dados: matriz **unit16**</span><span class="sxs-lookup"><span data-stu-id="c5858-196">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="c5858-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5858-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5858-198">Indica os possíveis Estados que podem ser solicitados ao usar o método **RequestStateChange** no elemento lógico habilitado.</span><span class="sxs-lookup"><span data-stu-id="c5858-198">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="c5858-199">Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="c5858-199">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="c5858-200">Valor</span><span class="sxs-lookup"><span data-stu-id="c5858-200">Value</span></span>                                                                         | <span data-ttu-id="c5858-201">Significado</span><span class="sxs-lookup"><span data-stu-id="c5858-201">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="c5858-202"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c5858-202"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="c5858-203">habilitado</span><span class="sxs-lookup"><span data-stu-id="c5858-203">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="c5858-204"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c5858-204"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="c5858-205">Desabilita</span><span class="sxs-lookup"><span data-stu-id="c5858-205">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="c5858-206"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c5858-206"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="c5858-207">Desligar</span><span class="sxs-lookup"><span data-stu-id="c5858-207">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="c5858-208"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c5858-208"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="c5858-209">Offline</span><span class="sxs-lookup"><span data-stu-id="c5858-209">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="c5858-210"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c5858-210"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="c5858-211">Teste</span><span class="sxs-lookup"><span data-stu-id="c5858-211">Test</span></span><br/>      |
| <dl> <span data-ttu-id="c5858-212"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="c5858-212"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="c5858-213">Ferida</span><span class="sxs-lookup"><span data-stu-id="c5858-213">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="c5858-214"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="c5858-214"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="c5858-215">Fechar</span><span class="sxs-lookup"><span data-stu-id="c5858-215">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="c5858-216"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="c5858-216"><dt>10</dt></span></span> </dl> | <span data-ttu-id="c5858-217">Reboot</span><span class="sxs-lookup"><span data-stu-id="c5858-217">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="c5858-218"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="c5858-218"><dt>11</dt></span></span> </dl> | <span data-ttu-id="c5858-219">Redefinir</span><span class="sxs-lookup"><span data-stu-id="c5858-219">Reset</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="c5858-220">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="c5858-220">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5858-221">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5858-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c5858-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5858-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5858-223">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. SynchronousMethodsSupported")</span><span class="sxs-lookup"><span data-stu-id="c5858-223">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.SynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="c5858-224">Especifica os métodos [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) que têm suporte de forma síncrona pela implementação.</span><span class="sxs-lookup"><span data-stu-id="c5858-224">Specifies the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) methods that are supported synchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c5858-225">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c5858-225">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="ValidatePlannedSystem"></span><span id="validateplannedsystem"></span><span id="VALIDATEPLANNEDSYSTEM"></span>

<span data-ttu-id="c5858-226">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span><span class="sxs-lookup"><span data-stu-id="c5858-226">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSystemDefinition"></span><span id="importsystemdefinition"></span><span id="IMPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="c5858-227">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span><span class="sxs-lookup"><span data-stu-id="c5858-227">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSnapshotDefinitions"></span><span id="importsnapshotdefinitions"></span><span id="IMPORTSNAPSHOTDEFINITIONS"></span>

<span data-ttu-id="c5858-228">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span><span class="sxs-lookup"><span data-stu-id="c5858-228">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="RealizePlannedSystem"></span><span id="realizeplannedsystem"></span><span id="REALIZEPLANNEDSYSTEM"></span>

<span data-ttu-id="c5858-229">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span><span class="sxs-lookup"><span data-stu-id="c5858-229">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span></span>


</dt> <dd></dd> <dt>

<span id="ExportSystemDefinition"></span><span id="exportsystemdefinition"></span><span id="EXPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="c5858-230">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span><span class="sxs-lookup"><span data-stu-id="c5858-230">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>

<span data-ttu-id="c5858-231">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span><span class="sxs-lookup"><span data-stu-id="c5858-231">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>

<span data-ttu-id="c5858-232">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span><span class="sxs-lookup"><span data-stu-id="c5858-232">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>

<span data-ttu-id="c5858-233">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span><span class="sxs-lookup"><span data-stu-id="c5858-233">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="GetVirtualSystemThumbnailImage"></span><span id="getvirtualsystemthumbnailimage"></span><span id="GETVIRTUALSYSTEMTHUMBNAILIMAGE"></span>

<span data-ttu-id="c5858-234">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span><span class="sxs-lookup"><span data-stu-id="c5858-234">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyServiceSettings"></span><span id="modifyservicesettings"></span><span id="MODIFYSERVICESETTINGS"></span>

<span data-ttu-id="c5858-235">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span><span class="sxs-lookup"><span data-stu-id="c5858-235">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSummaryInformation"></span><span id="getsummaryinformation"></span><span id="GETSUMMARYINFORMATION"></span>

<span data-ttu-id="c5858-236">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span><span class="sxs-lookup"><span data-stu-id="c5858-236">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="AddKvpItems"></span><span id="addkvpitems"></span><span id="ADDKVPITEMS"></span>

<span data-ttu-id="c5858-237">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span><span class="sxs-lookup"><span data-stu-id="c5858-237">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyKvpItems"></span><span id="modifykvpitems"></span><span id="MODIFYKVPITEMS"></span>

<span data-ttu-id="c5858-238">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span><span class="sxs-lookup"><span data-stu-id="c5858-238">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveKvpItems"></span><span id="removekvpitems"></span><span id="REMOVEKVPITEMS"></span>

<span data-ttu-id="c5858-239">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span><span class="sxs-lookup"><span data-stu-id="c5858-239">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="FormatError"></span><span id="formaterror"></span><span id="FORMATERROR"></span>

<span data-ttu-id="c5858-240">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span><span class="sxs-lookup"><span data-stu-id="c5858-240">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="RequestStateChangeSupported"></span><span id="requeststatechangesupported"></span><span id="REQUESTSTATECHANGESUPPORTED"></span>

<span data-ttu-id="c5858-241">**RequestStateChangeSupported** (32789)</span><span class="sxs-lookup"><span data-stu-id="c5858-241">**RequestStateChangeSupported** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="StartServiceSupported"></span><span id="startservicesupported"></span><span id="STARTSERVICESUPPORTED"></span>

<span data-ttu-id="c5858-242">**StartServiceSupported** (32790)</span><span class="sxs-lookup"><span data-stu-id="c5858-242">**StartServiceSupported** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="StopServiceSupported"></span><span id="stopservicesupported"></span><span id="STOPSERVICESUPPORTED"></span>

<span data-ttu-id="c5858-243">**StopServiceSupported** (32791)</span><span class="sxs-lookup"><span data-stu-id="c5858-243">**StopServiceSupported** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyDiskMergeSettings"></span><span id="modifydiskmergesettings"></span><span id="MODIFYDISKMERGESETTINGS"></span>

<span data-ttu-id="c5858-244">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span><span class="sxs-lookup"><span data-stu-id="c5858-244">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span></span>


</dt> <dd></dd> <dt>

<span id="GenerateWwpn"></span><span id="generatewwpn"></span><span id="GENERATEWWPN"></span>

<span data-ttu-id="c5858-245">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span><span class="sxs-lookup"><span data-stu-id="c5858-245">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFibreChannelChap"></span><span id="addfibrechannelchap"></span><span id="ADDFIBRECHANNELCHAP"></span>

<span data-ttu-id="c5858-246">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span><span class="sxs-lookup"><span data-stu-id="c5858-246">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFibreChannelChap"></span><span id="removefibrechannelchap"></span><span id="REMOVEFIBRECHANNELCHAP"></span>

<span data-ttu-id="c5858-247">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span><span class="sxs-lookup"><span data-stu-id="c5858-247">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span></span>


</dt> <dd></dd> <dt>

<span id="SetGuestNetworkAdapterConfiguration"></span><span id="setguestnetworkadapterconfiguration"></span><span id="SETGUESTNETWORKADAPTERCONFIGURATION"></span>

<span data-ttu-id="c5858-248">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span><span class="sxs-lookup"><span data-stu-id="c5858-248">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSizeOfSystemFiles"></span><span id="getsizeofsystemfiles"></span><span id="GETSIZEOFSYSTEMFILES"></span>

<span data-ttu-id="c5858-249">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span><span class="sxs-lookup"><span data-stu-id="c5858-249">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span></span>


</dt> <dd></dd> <dt>

<span id="GetCurrentWwpnFromGenerator"></span><span id="getcurrentwwpnfromgenerator"></span><span id="GETCURRENTWWPNFROMGENERATOR"></span>

<span data-ttu-id="c5858-250">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span><span class="sxs-lookup"><span data-stu-id="c5858-250">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="c5858-251">**Fornecedor reservado** (32799.. 65535)</span><span class="sxs-lookup"><span data-stu-id="c5858-251">**Vendor Reserved** (32799..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c5858-252">**VirtualSystemTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="c5858-252">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5858-253">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5858-253">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c5858-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5858-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5858-255">Uma matriz de cadeias de caracteres que designa um tipo de sistema virtual compatível com a implementação.</span><span class="sxs-lookup"><span data-stu-id="c5858-255">An array of strings each designating a type of virtual system that the implementation supports.</span></span> <span data-ttu-id="c5858-256">O valor de cada elemento de matriz não **NULL** deve estar de acordo com as cadeias de caracteres definidas para a propriedade [**Msvm \_ VirtualSystemSettingData. VirtualSystemType**](msvm-virtualsystemsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="c5858-256">The value of each non-**NULL** array element must conform to the strings defined for the [**Msvm\_VirtualSystemSettingData.VirtualSystemType**](msvm-virtualsystemsettingdata.md) property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5858-257">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5858-257">Requirements</span></span>



| <span data-ttu-id="c5858-258">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5858-258">Requirement</span></span> | <span data-ttu-id="c5858-259">Valor</span><span class="sxs-lookup"><span data-stu-id="c5858-259">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5858-260">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5858-260">Minimum supported client</span></span><br/> | <span data-ttu-id="c5858-261">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c5858-261">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c5858-262">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5858-262">Minimum supported server</span></span><br/> | <span data-ttu-id="c5858-263">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c5858-263">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c5858-264">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5858-264">Namespace</span></span><br/>                | <span data-ttu-id="c5858-265">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c5858-265">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c5858-266">MOF</span><span class="sxs-lookup"><span data-stu-id="c5858-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5858-267"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5858-267"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5858-268">DLL</span><span class="sxs-lookup"><span data-stu-id="c5858-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5858-269"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c5858-269"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

