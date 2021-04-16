---
description: Representa as informações de identificação sobre um monitor de vídeo, como nome do fabricante, ano de fabricação ou número de série.
ms.assetid: 85c8c4b1-20e2-4c0b-9209-a3724509a2f0
title: Classe WmiMonitorID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorID
- WmiMonitorID.Active
- WmiMonitorID.InstanceName
- WmiMonitorID.ManufacturerName
- WmiMonitorID.ManufacturerNameLength
- WmiMonitorID.ProductCodeID
- WmiMonitorID.SerialNumberID
- WmiMonitorID.WeekOfManufacture
- WmiMonitorID.YearOfManufacture
- WmiMonitorID.UserFriendlyName
- WmiMonitorID.UserFriendlyNameLength
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.custom: project-verbatim
ms.openlocfilehash: 485b42a86ca67d15ec00be13992c17b31ed51608
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "105764999"
---
# <a name="wmimonitorid-class"></a><span data-ttu-id="1008d-103">Classe WmiMonitorID</span><span class="sxs-lookup"><span data-stu-id="1008d-103">WmiMonitorID class</span></span>

<span data-ttu-id="1008d-104">A classe WMI **WmiMonitorID** representa as informações de identificação sobre um monitor de vídeo, como nome do fabricante, ano de fabricação ou número de série.</span><span class="sxs-lookup"><span data-stu-id="1008d-104">The **WmiMonitorID** WMI class represents the identifying information about a video monitor, such as manufacturer name, year of manufacture, or serial number.</span></span> <span data-ttu-id="1008d-105">Os dados nessa classe correspondem aos dados no bloco de identificação do fornecedor/produto da definição de entrada de vídeo do padrão de dados de identificação de exibição estendida (VESA) (E-EDID) avançado de associação de vídeo eletrônicos.</span><span class="sxs-lookup"><span data-stu-id="1008d-105">The data in this class correspond to data in the Vendor/Product Identification block of Video Input Definition of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="1008d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1008d-106">Syntax</span></span>

``` syntax
class WmiMonitorID : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint16  ManufacturerName[];
  uint16  ManufacturerNameLength;
  uint16  ProductCodeID[];
  uint16  SerialNumberID[];
  uint8   WeekOfManufacture;
  uint16  YearOfManufacture;
  uint16  UserFriendlyName[];
  uint16  UserFriendlyNameLength;
};
```

## <a name="members"></a><span data-ttu-id="1008d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1008d-107">Members</span></span>

<span data-ttu-id="1008d-108">A classe **WmiMonitorID** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1008d-108">The **WmiMonitorID** class has these types of members:</span></span>

-   [<span data-ttu-id="1008d-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1008d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1008d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1008d-110">Properties</span></span>

<span data-ttu-id="1008d-111">A classe **WmiMonitorID** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1008d-111">The **WmiMonitorID** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1008d-112">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="1008d-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1008d-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1008d-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1008d-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1008d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1008d-115">Indica o monitor ativo.</span><span class="sxs-lookup"><span data-stu-id="1008d-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="1008d-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="1008d-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1008d-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1008d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1008d-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1008d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1008d-119">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="1008d-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1008d-120">Nome da instância de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="1008d-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="1008d-121">**ManufacturerName**</span><span class="sxs-lookup"><span data-stu-id="1008d-121">**ManufacturerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1008d-122">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1008d-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1008d-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1008d-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1008d-124">Nome do fabricante.</span><span class="sxs-lookup"><span data-stu-id="1008d-124">Name of manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="1008d-125">**ManufacturerNameLength**</span><span class="sxs-lookup"><span data-stu-id="1008d-125">**ManufacturerNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1008d-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1008d-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1008d-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1008d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1008d-128">Comprimento do nome do fabricante localizado na propriedade **ManufacturerName** .</span><span class="sxs-lookup"><span data-stu-id="1008d-128">Length of manufacturer name located in the **ManufacturerName** property.</span></span>

</dd> <dt>

<span data-ttu-id="1008d-129">**ProductCodeid**</span><span class="sxs-lookup"><span data-stu-id="1008d-129">**ProductCodeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1008d-130">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1008d-130">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1008d-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1008d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1008d-132">ID de código do produto atribuído pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="1008d-132">Vendor assigned product code ID.</span></span>

</dd> <dt>

<span data-ttu-id="1008d-133">**SerialNumberid**</span><span class="sxs-lookup"><span data-stu-id="1008d-133">**SerialNumberID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1008d-134">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1008d-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1008d-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1008d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1008d-136">Número de série.</span><span class="sxs-lookup"><span data-stu-id="1008d-136">Serial number.</span></span>

</dd> <dt>

<span data-ttu-id="1008d-137">UserFriendlyName</span><span class="sxs-lookup"><span data-stu-id="1008d-137">UserFriendlyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1008d-138">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1008d-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1008d-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1008d-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1008d-140">O nome amigável do monitor.</span><span class="sxs-lookup"><span data-stu-id="1008d-140">The friendly name of the monitor.</span></span> <span data-ttu-id="1008d-141">O tamanho do nome é o comprimento especificado pela propriedade UserFriendlyNameLength.</span><span class="sxs-lookup"><span data-stu-id="1008d-141">The size of the name is the length specified by the UserFriendlyNameLength property.</span></span>

</dd> <dt>

<span data-ttu-id="1008d-142">UserFriendlyNameLength</span><span class="sxs-lookup"><span data-stu-id="1008d-142">UserFriendlyNameLength</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1008d-143">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1008d-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1008d-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1008d-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1008d-145">Número de caracteres no nome localizado na propriedade userfriendlyname.</span><span class="sxs-lookup"><span data-stu-id="1008d-145">Number of characters in the name located in the UserFriendlyName property.</span></span>

</dd> <dt>

<span data-ttu-id="1008d-146">**WeekOfManufacture**</span><span class="sxs-lookup"><span data-stu-id="1008d-146">**WeekOfManufacture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1008d-147">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="1008d-147">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1008d-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1008d-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1008d-149">Semana de fabricação por número da semana.</span><span class="sxs-lookup"><span data-stu-id="1008d-149">Week of manufacture by week number.</span></span> <span data-ttu-id="1008d-150">O intervalo é de 1 a 53.</span><span class="sxs-lookup"><span data-stu-id="1008d-150">The range is from 1 through 53.</span></span> <span data-ttu-id="1008d-151">Zero (0) é indefinido.</span><span class="sxs-lookup"><span data-stu-id="1008d-151">Zero (0) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="1008d-152">**YearOfManufacture**</span><span class="sxs-lookup"><span data-stu-id="1008d-152">**YearOfManufacture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1008d-153">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1008d-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1008d-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1008d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1008d-155">Ano de fabricação.</span><span class="sxs-lookup"><span data-stu-id="1008d-155">Year of manufacture.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1008d-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="1008d-156">Remarks</span></span>

<span data-ttu-id="1008d-157">Para obter uma discussão sobre como converter as matrizes que armazenam IDs de número de série, consulte o artigo [informações do monitor de relatório com Configuration Manager](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) blog.</span><span class="sxs-lookup"><span data-stu-id="1008d-157">For a discussion on how to translate the arrays that store serial number ID's, see the [Reporting Monitor information with Configuration Manager](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) blog article.</span></span>

## <a name="examples"></a><span data-ttu-id="1008d-158">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1008d-158">Examples</span></span>

<span data-ttu-id="1008d-159">O exemplo do PowerShell a seguir recupera o número de série de vários monitores.</span><span class="sxs-lookup"><span data-stu-id="1008d-159">The following PowerShell example retrieves the serial number of multiple monitors.</span></span>


```PowerShell
gwmi WmiMonitorID -Namespace root\wmi | ForEach-Object {($_.UserFriendlyName -ne 0 | foreach {[char]$_}) -join ""; ($_.SerialNumberID -ne 0 | foreach {[char]$_}) -join ""}
```



<span data-ttu-id="1008d-160">O código VBScript a seguir também recupera informações de ID de monitor de um sistema.</span><span class="sxs-lookup"><span data-stu-id="1008d-160">The following VBScript code also retrieves monitor ID information from a system.</span></span>


```VB
Option Explicit

Dim strComputer, objWMIService, colItems, objItem

strComputer = "MyComputer"

Set objWMIService = GetObject("winmgmts:" _ 
  & "{impersonationLevel=impersonate,authenticationLevel=Pkt}!\\" _ 
  & strComputer & "\root\wmi") 

Set colItems = objWMIService.ExecQuery _
  ("SELECT * FROM WMIMonitorID")

For Each objItem In colItems
  Wscript.Echo objItem.InstanceName
Next
```



## <a name="requirements"></a><span data-ttu-id="1008d-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1008d-161">Requirements</span></span>



| <span data-ttu-id="1008d-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="1008d-162">Requirement</span></span> | <span data-ttu-id="1008d-163">Valor</span><span class="sxs-lookup"><span data-stu-id="1008d-163">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1008d-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1008d-164">Minimum supported client</span></span><br/> | <span data-ttu-id="1008d-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1008d-165">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1008d-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1008d-166">Minimum supported server</span></span><br/> | <span data-ttu-id="1008d-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1008d-167">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1008d-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="1008d-168">Namespace</span></span><br/>                | <span data-ttu-id="1008d-169">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="1008d-169">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="1008d-170">MOF</span><span class="sxs-lookup"><span data-stu-id="1008d-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1008d-171"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1008d-171"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="1008d-172">DLL</span><span class="sxs-lookup"><span data-stu-id="1008d-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1008d-173"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1008d-173"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1008d-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="1008d-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1008d-175">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="1008d-175">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

