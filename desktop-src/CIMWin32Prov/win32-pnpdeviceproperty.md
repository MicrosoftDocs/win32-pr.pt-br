---
description: 'O tipo base para classes que representam uma propriedade retornada pelo \_ método Win32 PnPEntity:: deviceproperties.'
ms.assetid: f636c106-6ca6-407f-804a-0ec554ed565c
ms.tgt_platform: multiple
title: classe Win32_PnPDeviceProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDeviceProperty
- Win32_PnPDeviceProperty.Key
- Win32_PnPDeviceProperty.KeyName
- Win32_PnPDeviceProperty.Type
- Win32_PnPDeviceProperty.DeviceID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d8e1869e5d6cde35404ff9c12eabd35631b3227c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457182"
---
# <a name="win32_pnpdeviceproperty-class"></a><span data-ttu-id="38790-103">\_Classe Win32 PnPDeviceProperty</span><span class="sxs-lookup"><span data-stu-id="38790-103">Win32\_PnPDeviceProperty class</span></span>

<span data-ttu-id="38790-104">O tipo base para classes que representam uma propriedade retornada pelo método [**Win32 \_ PnPEntity**](win32-pnpentity.md):: deviceproperties.[](getdeviceproperties-win32-pnpentity.md)</span><span class="sxs-lookup"><span data-stu-id="38790-104">The base type for classes representing a property returned by the [**Win32\_PnPEntity**](win32-pnpentity.md)::[**GetDeviceProperties**](getdeviceproperties-win32-pnpentity.md) Method.</span></span>

<span data-ttu-id="38790-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="38790-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="38790-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38790-106">Syntax</span></span>

``` syntax
[abstract, UUID("{ee0b76cd-314b-41f1-99d4-d4f3b0421430}"), AMENDMENT]
class Win32_PnPDeviceProperty
{
  string Key;
  string KeyName;
  Uint32 Type;
  string DeviceID;
};
```

## <a name="members"></a><span data-ttu-id="38790-107">Membros</span><span class="sxs-lookup"><span data-stu-id="38790-107">Members</span></span>

<span data-ttu-id="38790-108">A classe **Win32 \_ PnPDeviceProperty** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="38790-108">The **Win32\_PnPDeviceProperty** class has these types of members:</span></span>

-   [<span data-ttu-id="38790-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="38790-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38790-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="38790-110">Properties</span></span>

<span data-ttu-id="38790-111">A classe **Win32 \_ PnPDeviceProperty** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="38790-111">The **Win32\_PnPDeviceProperty** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38790-112">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="38790-112">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38790-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="38790-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38790-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="38790-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38790-115">Identifica o dispositivo PnP.</span><span class="sxs-lookup"><span data-stu-id="38790-115">Identifies the PnP device.</span></span>

</dd> <dt>

<span data-ttu-id="38790-116">**Chave**</span><span class="sxs-lookup"><span data-stu-id="38790-116">**Key**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38790-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="38790-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38790-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="38790-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38790-119">O valor do par de Name-Value de chave que identifica a propriedade de **dados** .</span><span class="sxs-lookup"><span data-stu-id="38790-119">The value of the Key Name-Value pair that identifies the **Data** property.</span></span>

</dd> <dt>

<span data-ttu-id="38790-120">**KeyName**</span><span class="sxs-lookup"><span data-stu-id="38790-120">**KeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38790-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="38790-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38790-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="38790-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38790-123">O nome do par de Name-Value de chave que identifica a propriedade de **dados** .</span><span class="sxs-lookup"><span data-stu-id="38790-123">The name of the Key Name-Value pair that identifies the **Data** property.</span></span>

</dd> <dt>

<span data-ttu-id="38790-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="38790-124">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38790-125">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38790-125">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38790-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="38790-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38790-127">O tipo da propriedade de **dados** .</span><span class="sxs-lookup"><span data-stu-id="38790-127">The type of the **Data** property.</span></span>

<span data-ttu-id="38790-128">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="38790-128">The possible values are.</span></span>

<dt>

<span id="Empty"></span><span id="empty"></span><span id="EMPTY"></span>

<span data-ttu-id="38790-129">**Vazio** (0)</span><span class="sxs-lookup"><span data-stu-id="38790-129">**Empty** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Null"></span><span id="null"></span><span id="NULL"></span>

<span data-ttu-id="38790-130">**NULL** (1)</span><span class="sxs-lookup"><span data-stu-id="38790-130">**Null** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SByte"></span><span id="sbyte"></span><span id="SBYTE"></span>

<span data-ttu-id="38790-131">**SByte** (2)</span><span class="sxs-lookup"><span data-stu-id="38790-131">**SByte** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Byte"></span><span id="byte"></span><span id="BYTE"></span>

<span data-ttu-id="38790-132">**Byte** (3)</span><span class="sxs-lookup"><span data-stu-id="38790-132">**Byte** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16"></span><span id="int16"></span><span id="INT16"></span>

<span data-ttu-id="38790-133">**Int16** (4)</span><span class="sxs-lookup"><span data-stu-id="38790-133">**Int16** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16"></span><span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="38790-134">**UInt16** (5)</span><span class="sxs-lookup"><span data-stu-id="38790-134">**UInt16** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Int32"></span><span id="int32"></span><span id="INT32"></span>

<span data-ttu-id="38790-135">**Int32** (6)</span><span class="sxs-lookup"><span data-stu-id="38790-135">**Int32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Uint32"></span><span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="38790-136">**UInt32** (7)</span><span class="sxs-lookup"><span data-stu-id="38790-136">**Uint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64"></span><span id="int64"></span><span id="INT64"></span>

<span data-ttu-id="38790-137">**Int64** (8)</span><span class="sxs-lookup"><span data-stu-id="38790-137">**Int64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64"></span><span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="38790-138">**UInt64** (9)</span><span class="sxs-lookup"><span data-stu-id="38790-138">**UInt64** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Float"></span><span id="float"></span><span id="FLOAT"></span>

<span data-ttu-id="38790-139">**Float** (10)</span><span class="sxs-lookup"><span data-stu-id="38790-139">**Float** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Double"></span><span id="double"></span><span id="DOUBLE"></span>

<span data-ttu-id="38790-140">**Duplo** (11)</span><span class="sxs-lookup"><span data-stu-id="38790-140">**Double** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Decimal"></span><span id="decimal"></span><span id="DECIMAL"></span>

<span data-ttu-id="38790-141">**Decimal** (12)</span><span class="sxs-lookup"><span data-stu-id="38790-141">**Decimal** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Guid"></span><span id="guid"></span><span id="GUID"></span>

<span data-ttu-id="38790-142">**GUID** (13)</span><span class="sxs-lookup"><span data-stu-id="38790-142">**Guid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Currency"></span><span id="currency"></span><span id="CURRENCY"></span>

<span data-ttu-id="38790-143">**Moeda** (14)</span><span class="sxs-lookup"><span data-stu-id="38790-143">**Currency** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Date"></span><span id="date"></span><span id="DATE"></span>

<span data-ttu-id="38790-144">**Data** (15)</span><span class="sxs-lookup"><span data-stu-id="38790-144">**Date** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTime"></span><span id="filetime"></span><span id="FILETIME"></span>

<span data-ttu-id="38790-145">**FILETIME** (16)</span><span class="sxs-lookup"><span data-stu-id="38790-145">**FileTime** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="38790-146">**Booliano** (17)</span><span class="sxs-lookup"><span data-stu-id="38790-146">**Boolean** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="String"></span><span id="string"></span><span id="STRING"></span>

<span data-ttu-id="38790-147">**Cadeia de caracteres** (18)</span><span class="sxs-lookup"><span data-stu-id="38790-147">**String** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptor"></span><span id="securitydescriptor"></span><span id="SECURITYDESCRIPTOR"></span>

<span data-ttu-id="38790-148">**SecurityDescriptor** (19)</span><span class="sxs-lookup"><span data-stu-id="38790-148">**SecurityDescriptor** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorString"></span><span id="securitydescriptorstring"></span><span id="SECURITYDESCRIPTORSTRING"></span>

<span data-ttu-id="38790-149">**SecurityDescriptorString** (20)</span><span class="sxs-lookup"><span data-stu-id="38790-149">**SecurityDescriptorString** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEY"></span><span id="devpropkey"></span>

<span data-ttu-id="38790-150">**DEVPROPKEY** (21)</span><span class="sxs-lookup"><span data-stu-id="38790-150">**DEVPROPKEY** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPE"></span><span id="devproptype"></span>

<span data-ttu-id="38790-151">**DEVPROPTYPE** (22)</span><span class="sxs-lookup"><span data-stu-id="38790-151">**DEVPROPTYPE** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="38790-152">**Erro** (23)</span><span class="sxs-lookup"><span data-stu-id="38790-152">**Error** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatus"></span><span id="ntstatus"></span><span id="NTSTATUS"></span>

<span data-ttu-id="38790-153">**NTStatus** (24)</span><span class="sxs-lookup"><span data-stu-id="38790-153">**NTStatus** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirect"></span><span id="stringindirect"></span><span id="STRINGINDIRECT"></span>

<span data-ttu-id="38790-154">**StringIndirect** (25)</span><span class="sxs-lookup"><span data-stu-id="38790-154">**StringIndirect** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="38790-155">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="38790-155">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="38790-156">26 – 4097</span><span class="sxs-lookup"><span data-stu-id="38790-156">26–4097</span></span></dd> <dt>

<span id="SByteArray"></span><span id="sbytearray"></span><span id="SBYTEARRAY"></span>

<span data-ttu-id="38790-157">**SByteArray** (4098)</span><span class="sxs-lookup"><span data-stu-id="38790-157">**SByteArray** (4098)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="38790-158">**Binário** (4099)</span><span class="sxs-lookup"><span data-stu-id="38790-158">**Binary** (4099)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16Array"></span><span id="int16array"></span><span id="INT16ARRAY"></span>

<span data-ttu-id="38790-159">**Int16Array** (4100)</span><span class="sxs-lookup"><span data-stu-id="38790-159">**Int16Array** (4100)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16Array"></span><span id="uint16array"></span><span id="UINT16ARRAY"></span>

<span data-ttu-id="38790-160">**UInt16Array** (4101)</span><span class="sxs-lookup"><span data-stu-id="38790-160">**UInt16Array** (4101)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64Array"></span><span id="int64array"></span><span id="INT64ARRAY"></span>

<span data-ttu-id="38790-161">**Int64Array** (4102)</span><span class="sxs-lookup"><span data-stu-id="38790-161">**Int64Array** (4102)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64Array"></span><span id="uint64array"></span><span id="UINT64ARRAY"></span>

<span data-ttu-id="38790-162">**UInt64Array** (4103)</span><span class="sxs-lookup"><span data-stu-id="38790-162">**UInt64Array** (4103)</span></span>


</dt> <dd></dd> <dt>

<span id="FloatArray"></span><span id="floatarray"></span><span id="FLOATARRAY"></span>

<span data-ttu-id="38790-163">**FloatArray** (4104)</span><span class="sxs-lookup"><span data-stu-id="38790-163">**FloatArray** (4104)</span></span>


</dt> <dd></dd> <dt>

<span id="DoubleArray"></span><span id="doublearray"></span><span id="DOUBLEARRAY"></span>

<span data-ttu-id="38790-164">**DoubleArray** (4105)</span><span class="sxs-lookup"><span data-stu-id="38790-164">**DoubleArray** (4105)</span></span>


</dt> <dd></dd> <dt>

<span id="DecimalArray"></span><span id="decimalarray"></span><span id="DECIMALARRAY"></span>

<span data-ttu-id="38790-165">**DecimalArray** (4106)</span><span class="sxs-lookup"><span data-stu-id="38790-165">**DecimalArray** (4106)</span></span>


</dt> <dd></dd> <dt>

<span id="GuidArray"></span><span id="guidarray"></span><span id="GUIDARRAY"></span>

<span data-ttu-id="38790-166">**GuidArray** (4107)</span><span class="sxs-lookup"><span data-stu-id="38790-166">**GuidArray** (4107)</span></span>


</dt> <dd></dd> <dt>

<span id="CurrencyArray"></span><span id="currencyarray"></span><span id="CURRENCYARRAY"></span>

<span data-ttu-id="38790-167">**CurrencyArray** (4108)</span><span class="sxs-lookup"><span data-stu-id="38790-167">**CurrencyArray** (4108)</span></span>


</dt> <dd></dd> <dt>

<span id="DateArray"></span><span id="datearray"></span><span id="DATEARRAY"></span>

<span data-ttu-id="38790-168">**DateArray** (4109)</span><span class="sxs-lookup"><span data-stu-id="38790-168">**DateArray** (4109)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTimeArray"></span><span id="filetimearray"></span><span id="FILETIMEARRAY"></span>

<span data-ttu-id="38790-169">**FileTimeArray** (4110)</span><span class="sxs-lookup"><span data-stu-id="38790-169">**FileTimeArray** (4110)</span></span>


</dt> <dd></dd> <dt>

<span id="BooleanArray"></span><span id="booleanarray"></span><span id="BOOLEANARRAY"></span>

<span data-ttu-id="38790-170">**BooleanArray** (4111)</span><span class="sxs-lookup"><span data-stu-id="38790-170">**BooleanArray** (4111)</span></span>


</dt> <dd></dd> <dt>

<span id="StringList"></span><span id="stringlist"></span><span id="STRINGLIST"></span>

<span data-ttu-id="38790-171">**StringList** (4112)</span><span class="sxs-lookup"><span data-stu-id="38790-171">**StringList** (4112)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorList"></span><span id="securitydescriptorlist"></span><span id="SECURITYDESCRIPTORLIST"></span>

<span data-ttu-id="38790-172">**SecurityDescriptorList** (4113)</span><span class="sxs-lookup"><span data-stu-id="38790-172">**SecurityDescriptorList** (4113)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorStringList"></span><span id="securitydescriptorstringlist"></span><span id="SECURITYDESCRIPTORSTRINGLIST"></span>

<span data-ttu-id="38790-173">**SecurityDescriptorStringList** (8210)</span><span class="sxs-lookup"><span data-stu-id="38790-173">**SecurityDescriptorStringList** (8210)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEYArray"></span><span id="devpropkeyarray"></span><span id="DEVPROPKEYARRAY"></span>

<span data-ttu-id="38790-174">**DEVPROPKEYArray** (8211)</span><span class="sxs-lookup"><span data-stu-id="38790-174">**DEVPROPKEYArray** (8211)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPEArray"></span><span id="devproptypearray"></span><span id="DEVPROPTYPEARRAY"></span>

<span data-ttu-id="38790-175">**DEVPROPTYPEArray** (8212)</span><span class="sxs-lookup"><span data-stu-id="38790-175">**DEVPROPTYPEArray** (8212)</span></span>


</dt> <dd></dd> <dt>

<span id="ErrorArray"></span><span id="errorarray"></span><span id="ERRORARRAY"></span>

<span data-ttu-id="38790-176">**ErrorArray** (4117)</span><span class="sxs-lookup"><span data-stu-id="38790-176">**ErrorArray** (4117)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatusArray"></span><span id="ntstatusarray"></span><span id="NTSTATUSARRAY"></span>

<span data-ttu-id="38790-177">**NTStatusArray** (4118)</span><span class="sxs-lookup"><span data-stu-id="38790-177">**NTStatusArray** (4118)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirectList"></span><span id="stringindirectlist"></span><span id="STRINGINDIRECTLIST"></span>

<span data-ttu-id="38790-178">**StringIndirectList** (4119)</span><span class="sxs-lookup"><span data-stu-id="38790-178">**StringIndirectList** (4119)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_-_check_in_devpropdef.h"></span><span id="unknown_-_check_in_devpropdef.h"></span><span id="UNKNOWN_-_CHECK_IN_DEVPROPDEF.H"></span>

<span data-ttu-id="38790-179">**Desconhecido-verifique em devpropdef. h** (4120)</span><span class="sxs-lookup"><span data-stu-id="38790-179">**Unknown - check in devpropdef.h** (4120)</span></span>


</dt> <dd></dd> <dt>

<span id="TBD"></span><span id="tbd"></span>

<span data-ttu-id="38790-180">**TBD** (8217)</span><span class="sxs-lookup"><span data-stu-id="38790-180">**TBD** (8217)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="38790-181">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="38790-181">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="38790-182">8218 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="38790-182">8218–4294967295</span></span></dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38790-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38790-183">Requirements</span></span>



| <span data-ttu-id="38790-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="38790-184">Requirement</span></span> | <span data-ttu-id="38790-185">Valor</span><span class="sxs-lookup"><span data-stu-id="38790-185">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38790-186">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38790-186">Minimum supported client</span></span><br/> | <span data-ttu-id="38790-187">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="38790-187">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="38790-188">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38790-188">Minimum supported server</span></span><br/> | <span data-ttu-id="38790-189">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="38790-189">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="38790-190">Namespace</span><span class="sxs-lookup"><span data-stu-id="38790-190">Namespace</span></span><br/>                | <span data-ttu-id="38790-191">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="38790-191">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="38790-192">MOF</span><span class="sxs-lookup"><span data-stu-id="38790-192">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38790-193"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38790-193"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="38790-194">DLL</span><span class="sxs-lookup"><span data-stu-id="38790-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38790-195"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38790-195"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38790-196">Confira também</span><span class="sxs-lookup"><span data-stu-id="38790-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38790-197">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="38790-197">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="38790-198">**Getdeviceproperties**</span><span class="sxs-lookup"><span data-stu-id="38790-198">**GetDeviceProperties**</span></span>](getdeviceproperties-win32-pnpentity.md)
</dt> </dl>

 

 
