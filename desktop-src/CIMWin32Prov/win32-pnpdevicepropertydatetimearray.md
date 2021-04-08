---
description: Representa uma propriedade de dispositivo PnP que consiste em uma matriz de elementos DateTime.
ms.assetid: 1036D49E-7F73-43C6-8F6E-BB909E74519E
ms.tgt_platform: multiple
title: Classe Win32_PnPDevicePropertyDateTimeArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevicePropertyDateTimeArray
- Win32_PnPDevicePropertyDateTimeArray.Key
- Win32_PnPDevicePropertyDateTimeArray.KeyName
- Win32_PnPDevicePropertyDateTimeArray.Type
- Win32_PnPDevicePropertyDateTimeArray.DeviceID
- Win32_PnPDevicePropertyDateTimeArray.Data
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: faa0fdf57e5eb4ad44cbb6ada2663baaea7b53ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920582"
---
# <a name="win32_pnpdevicepropertydatetimearray-class"></a><span data-ttu-id="d96fc-103">\_Classe Win32 PnPDevicePropertyDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="d96fc-103">Win32\_PnPDevicePropertyDateTimeArray class</span></span>

<span data-ttu-id="d96fc-104">Representa uma propriedade de dispositivo PnP que consiste em uma matriz de elementos **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="d96fc-104">Represents a PnP device property consisting of an array of **datetime** elements.</span></span>

<span data-ttu-id="d96fc-105">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d96fc-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d96fc-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d96fc-106">Syntax</span></span>

``` syntax
class Win32_PnPDevicePropertyDateTimeArray : Win32_PnPDeviceProperty
{
  string   Key;
  string   KeyName;
  Uint32   Type;
  string   DeviceID;
  datetime Data[];
};
```

## <a name="members"></a><span data-ttu-id="d96fc-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d96fc-107">Members</span></span>

<span data-ttu-id="d96fc-108">A classe **Win32 \_ PnPDevicePropertyDateTimeArray** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d96fc-108">The **Win32\_PnPDevicePropertyDateTimeArray** class has these types of members:</span></span>

-   [<span data-ttu-id="d96fc-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d96fc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d96fc-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d96fc-110">Properties</span></span>

<span data-ttu-id="d96fc-111">A classe **Win32 \_ PnPDevicePropertyDateTimeArray** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d96fc-111">The **Win32\_PnPDevicePropertyDateTimeArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d96fc-112">**Dados**</span><span class="sxs-lookup"><span data-stu-id="d96fc-112">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d96fc-113">Tipo de dados: matriz **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d96fc-113">Data type: **datetime** array</span></span>
</dt> <dt>

<span data-ttu-id="d96fc-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d96fc-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d96fc-115">O valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="d96fc-115">The property value.</span></span>

</dd> <dt>

<span data-ttu-id="d96fc-116">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d96fc-116">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d96fc-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d96fc-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d96fc-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d96fc-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d96fc-119">Identifica o dispositivo PnP.</span><span class="sxs-lookup"><span data-stu-id="d96fc-119">Identifies the PnP device.</span></span>

<span data-ttu-id="d96fc-120">Esta propriedade é herdada do [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="d96fc-120">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="d96fc-121">**Chave**</span><span class="sxs-lookup"><span data-stu-id="d96fc-121">**Key**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d96fc-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d96fc-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d96fc-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d96fc-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d96fc-124">O valor do par de Name-Value de chave que identifica a propriedade de **dados** .</span><span class="sxs-lookup"><span data-stu-id="d96fc-124">The value of the Key Name-Value pair that identifies the **Data** property.</span></span>

<span data-ttu-id="d96fc-125">Esta propriedade é herdada do [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="d96fc-125">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="d96fc-126">**KeyName**</span><span class="sxs-lookup"><span data-stu-id="d96fc-126">**KeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d96fc-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d96fc-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d96fc-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d96fc-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d96fc-129">O nome do par de Name-Value de chave que identifica a propriedade de **dados** .</span><span class="sxs-lookup"><span data-stu-id="d96fc-129">The name of the Key Name-Value pair that identifies the **Data** property.</span></span>

<span data-ttu-id="d96fc-130">Esta propriedade é herdada do [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="d96fc-130">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="d96fc-131">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d96fc-131">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d96fc-132">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d96fc-132">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d96fc-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d96fc-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d96fc-134">O tipo da propriedade de **dados** .</span><span class="sxs-lookup"><span data-stu-id="d96fc-134">The type of the **Data** property.</span></span>

<span data-ttu-id="d96fc-135">Esta propriedade é herdada do [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="d96fc-135">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

<span data-ttu-id="d96fc-136">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="d96fc-136">The possible values are.</span></span>

<dt>

<span id="Empty"></span><span id="empty"></span><span id="EMPTY"></span>

<span data-ttu-id="d96fc-137">**Vazio** (0)</span><span class="sxs-lookup"><span data-stu-id="d96fc-137">**Empty** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Null"></span><span id="null"></span><span id="NULL"></span>

<span data-ttu-id="d96fc-138">**NULL** (1)</span><span class="sxs-lookup"><span data-stu-id="d96fc-138">**Null** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SByte"></span><span id="sbyte"></span><span id="SBYTE"></span>

<span data-ttu-id="d96fc-139">**SByte** (2)</span><span class="sxs-lookup"><span data-stu-id="d96fc-139">**SByte** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Byte"></span><span id="byte"></span><span id="BYTE"></span>

<span data-ttu-id="d96fc-140">**Byte** (3)</span><span class="sxs-lookup"><span data-stu-id="d96fc-140">**Byte** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16"></span><span id="int16"></span><span id="INT16"></span>

<span data-ttu-id="d96fc-141">**Int16** (4)</span><span class="sxs-lookup"><span data-stu-id="d96fc-141">**Int16** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16"></span><span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="d96fc-142">**UInt16** (5)</span><span class="sxs-lookup"><span data-stu-id="d96fc-142">**UInt16** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Int32"></span><span id="int32"></span><span id="INT32"></span>

<span data-ttu-id="d96fc-143">**Int32** (6)</span><span class="sxs-lookup"><span data-stu-id="d96fc-143">**Int32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Uint32"></span><span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="d96fc-144">**UInt32** (7)</span><span class="sxs-lookup"><span data-stu-id="d96fc-144">**Uint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64"></span><span id="int64"></span><span id="INT64"></span>

<span data-ttu-id="d96fc-145">**Int64** (8)</span><span class="sxs-lookup"><span data-stu-id="d96fc-145">**Int64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64"></span><span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="d96fc-146">**UInt64** (9)</span><span class="sxs-lookup"><span data-stu-id="d96fc-146">**UInt64** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Float"></span><span id="float"></span><span id="FLOAT"></span>

<span data-ttu-id="d96fc-147">**Float** (10)</span><span class="sxs-lookup"><span data-stu-id="d96fc-147">**Float** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Double"></span><span id="double"></span><span id="DOUBLE"></span>

<span data-ttu-id="d96fc-148">**Duplo** (11)</span><span class="sxs-lookup"><span data-stu-id="d96fc-148">**Double** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Decimal"></span><span id="decimal"></span><span id="DECIMAL"></span>

<span data-ttu-id="d96fc-149">**Decimal** (12)</span><span class="sxs-lookup"><span data-stu-id="d96fc-149">**Decimal** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Guid"></span><span id="guid"></span><span id="GUID"></span>

<span data-ttu-id="d96fc-150">**GUID** (13)</span><span class="sxs-lookup"><span data-stu-id="d96fc-150">**Guid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Currency"></span><span id="currency"></span><span id="CURRENCY"></span>

<span data-ttu-id="d96fc-151">**Moeda** (14)</span><span class="sxs-lookup"><span data-stu-id="d96fc-151">**Currency** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Date"></span><span id="date"></span><span id="DATE"></span>

<span data-ttu-id="d96fc-152">**Data** (15)</span><span class="sxs-lookup"><span data-stu-id="d96fc-152">**Date** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTime"></span><span id="filetime"></span><span id="FILETIME"></span>

<span data-ttu-id="d96fc-153">**FILETIME** (16)</span><span class="sxs-lookup"><span data-stu-id="d96fc-153">**FileTime** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="d96fc-154">**Booliano** (17)</span><span class="sxs-lookup"><span data-stu-id="d96fc-154">**Boolean** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="String"></span><span id="string"></span><span id="STRING"></span>

<span data-ttu-id="d96fc-155">**Cadeia de caracteres** (18)</span><span class="sxs-lookup"><span data-stu-id="d96fc-155">**String** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptor"></span><span id="securitydescriptor"></span><span id="SECURITYDESCRIPTOR"></span>

<span data-ttu-id="d96fc-156">**SecurityDescriptor** (19)</span><span class="sxs-lookup"><span data-stu-id="d96fc-156">**SecurityDescriptor** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorString"></span><span id="securitydescriptorstring"></span><span id="SECURITYDESCRIPTORSTRING"></span>

<span data-ttu-id="d96fc-157">**SecurityDescriptorString** (20)</span><span class="sxs-lookup"><span data-stu-id="d96fc-157">**SecurityDescriptorString** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEY"></span><span id="devpropkey"></span>

<span data-ttu-id="d96fc-158">**DEVPROPKEY** (21)</span><span class="sxs-lookup"><span data-stu-id="d96fc-158">**DEVPROPKEY** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPE"></span><span id="devproptype"></span>

<span data-ttu-id="d96fc-159">**DEVPROPTYPE** (22)</span><span class="sxs-lookup"><span data-stu-id="d96fc-159">**DEVPROPTYPE** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d96fc-160">**Erro** (23)</span><span class="sxs-lookup"><span data-stu-id="d96fc-160">**Error** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatus"></span><span id="ntstatus"></span><span id="NTSTATUS"></span>

<span data-ttu-id="d96fc-161">**NTStatus** (24)</span><span class="sxs-lookup"><span data-stu-id="d96fc-161">**NTStatus** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirect"></span><span id="stringindirect"></span><span id="STRINGINDIRECT"></span>

<span data-ttu-id="d96fc-162">**StringIndirect** (25)</span><span class="sxs-lookup"><span data-stu-id="d96fc-162">**StringIndirect** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="d96fc-163">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="d96fc-163">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="d96fc-164">26 – 4097</span><span class="sxs-lookup"><span data-stu-id="d96fc-164">26–4097</span></span></dd> <dt>

<span id="SByteArray"></span><span id="sbytearray"></span><span id="SBYTEARRAY"></span>

<span data-ttu-id="d96fc-165">**SByteArray** (4098)</span><span class="sxs-lookup"><span data-stu-id="d96fc-165">**SByteArray** (4098)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="d96fc-166">**Binário** (4099)</span><span class="sxs-lookup"><span data-stu-id="d96fc-166">**Binary** (4099)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16Array"></span><span id="int16array"></span><span id="INT16ARRAY"></span>

<span data-ttu-id="d96fc-167">**Int16Array** (4100)</span><span class="sxs-lookup"><span data-stu-id="d96fc-167">**Int16Array** (4100)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16Array"></span><span id="uint16array"></span><span id="UINT16ARRAY"></span>

<span data-ttu-id="d96fc-168">**UInt16Array** (4101)</span><span class="sxs-lookup"><span data-stu-id="d96fc-168">**UInt16Array** (4101)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64Array"></span><span id="int64array"></span><span id="INT64ARRAY"></span>

<span data-ttu-id="d96fc-169">**Int64Array** (4102)</span><span class="sxs-lookup"><span data-stu-id="d96fc-169">**Int64Array** (4102)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64Array"></span><span id="uint64array"></span><span id="UINT64ARRAY"></span>

<span data-ttu-id="d96fc-170">**UInt64Array** (4103)</span><span class="sxs-lookup"><span data-stu-id="d96fc-170">**UInt64Array** (4103)</span></span>


</dt> <dd></dd> <dt>

<span id="FloatArray"></span><span id="floatarray"></span><span id="FLOATARRAY"></span>

<span data-ttu-id="d96fc-171">**FloatArray** (4104)</span><span class="sxs-lookup"><span data-stu-id="d96fc-171">**FloatArray** (4104)</span></span>


</dt> <dd></dd> <dt>

<span id="DoubleArray"></span><span id="doublearray"></span><span id="DOUBLEARRAY"></span>

<span data-ttu-id="d96fc-172">**DoubleArray** (4105)</span><span class="sxs-lookup"><span data-stu-id="d96fc-172">**DoubleArray** (4105)</span></span>


</dt> <dd></dd> <dt>

<span id="DecimalArray"></span><span id="decimalarray"></span><span id="DECIMALARRAY"></span>

<span data-ttu-id="d96fc-173">**DecimalArray** (4106)</span><span class="sxs-lookup"><span data-stu-id="d96fc-173">**DecimalArray** (4106)</span></span>


</dt> <dd></dd> <dt>

<span id="GuidArray"></span><span id="guidarray"></span><span id="GUIDARRAY"></span>

<span data-ttu-id="d96fc-174">**GuidArray** (4107)</span><span class="sxs-lookup"><span data-stu-id="d96fc-174">**GuidArray** (4107)</span></span>


</dt> <dd></dd> <dt>

<span id="CurrencyArray"></span><span id="currencyarray"></span><span id="CURRENCYARRAY"></span>

<span data-ttu-id="d96fc-175">**CurrencyArray** (4108)</span><span class="sxs-lookup"><span data-stu-id="d96fc-175">**CurrencyArray** (4108)</span></span>


</dt> <dd></dd> <dt>

<span id="DateArray"></span><span id="datearray"></span><span id="DATEARRAY"></span>

<span data-ttu-id="d96fc-176">**DateArray** (4109)</span><span class="sxs-lookup"><span data-stu-id="d96fc-176">**DateArray** (4109)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTimeArray"></span><span id="filetimearray"></span><span id="FILETIMEARRAY"></span>

<span data-ttu-id="d96fc-177">**FileTimeArray** (4110)</span><span class="sxs-lookup"><span data-stu-id="d96fc-177">**FileTimeArray** (4110)</span></span>


</dt> <dd></dd> <dt>

<span id="BooleanArray"></span><span id="booleanarray"></span><span id="BOOLEANARRAY"></span>

<span data-ttu-id="d96fc-178">**BooleanArray** (4111)</span><span class="sxs-lookup"><span data-stu-id="d96fc-178">**BooleanArray** (4111)</span></span>


</dt> <dd></dd> <dt>

<span id="StringList"></span><span id="stringlist"></span><span id="STRINGLIST"></span>

<span data-ttu-id="d96fc-179">**StringList** (4112)</span><span class="sxs-lookup"><span data-stu-id="d96fc-179">**StringList** (4112)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorList"></span><span id="securitydescriptorlist"></span><span id="SECURITYDESCRIPTORLIST"></span>

<span data-ttu-id="d96fc-180">**SecurityDescriptorList** (4113)</span><span class="sxs-lookup"><span data-stu-id="d96fc-180">**SecurityDescriptorList** (4113)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorStringList"></span><span id="securitydescriptorstringlist"></span><span id="SECURITYDESCRIPTORSTRINGLIST"></span>

<span data-ttu-id="d96fc-181">**SecurityDescriptorStringList** (8210)</span><span class="sxs-lookup"><span data-stu-id="d96fc-181">**SecurityDescriptorStringList** (8210)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEYArray"></span><span id="devpropkeyarray"></span><span id="DEVPROPKEYARRAY"></span>

<span data-ttu-id="d96fc-182">**DEVPROPKEYArray** (8211)</span><span class="sxs-lookup"><span data-stu-id="d96fc-182">**DEVPROPKEYArray** (8211)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPEArray"></span><span id="devproptypearray"></span><span id="DEVPROPTYPEARRAY"></span>

<span data-ttu-id="d96fc-183">**DEVPROPTYPEArray** (8212)</span><span class="sxs-lookup"><span data-stu-id="d96fc-183">**DEVPROPTYPEArray** (8212)</span></span>


</dt> <dd></dd> <dt>

<span id="ErrorArray"></span><span id="errorarray"></span><span id="ERRORARRAY"></span>

<span data-ttu-id="d96fc-184">**ErrorArray** (4117)</span><span class="sxs-lookup"><span data-stu-id="d96fc-184">**ErrorArray** (4117)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatusArray"></span><span id="ntstatusarray"></span><span id="NTSTATUSARRAY"></span>

<span data-ttu-id="d96fc-185">**NTStatusArray** (4118)</span><span class="sxs-lookup"><span data-stu-id="d96fc-185">**NTStatusArray** (4118)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirectList"></span><span id="stringindirectlist"></span><span id="STRINGINDIRECTLIST"></span>

<span data-ttu-id="d96fc-186">**StringIndirectList** (4119)</span><span class="sxs-lookup"><span data-stu-id="d96fc-186">**StringIndirectList** (4119)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_-_check_in_devpropdef.h"></span><span id="unknown_-_check_in_devpropdef.h"></span><span id="UNKNOWN_-_CHECK_IN_DEVPROPDEF.H"></span>

<span data-ttu-id="d96fc-187">**Desconhecido-verifique em devpropdef. h** (4120)</span><span class="sxs-lookup"><span data-stu-id="d96fc-187">**Unknown - check in devpropdef.h** (4120)</span></span>


</dt> <dd></dd> <dt>

<span id="TBD"></span><span id="tbd"></span>

<span data-ttu-id="d96fc-188">**TBD** (8217)</span><span class="sxs-lookup"><span data-stu-id="d96fc-188">**TBD** (8217)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="d96fc-189">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="d96fc-189">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="d96fc-190">8218 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="d96fc-190">8218–4294967295</span></span></dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d96fc-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d96fc-191">Requirements</span></span>



| <span data-ttu-id="d96fc-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="d96fc-192">Requirement</span></span> | <span data-ttu-id="d96fc-193">Valor</span><span class="sxs-lookup"><span data-stu-id="d96fc-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d96fc-194">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d96fc-194">Minimum supported client</span></span><br/> | <span data-ttu-id="d96fc-195">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d96fc-195">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d96fc-196">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d96fc-196">Minimum supported server</span></span><br/> | <span data-ttu-id="d96fc-197">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d96fc-197">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="d96fc-198">Namespace</span><span class="sxs-lookup"><span data-stu-id="d96fc-198">Namespace</span></span><br/>                | <span data-ttu-id="d96fc-199">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d96fc-199">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d96fc-200">MOF</span><span class="sxs-lookup"><span data-stu-id="d96fc-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d96fc-201"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d96fc-201"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d96fc-202">DLL</span><span class="sxs-lookup"><span data-stu-id="d96fc-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d96fc-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d96fc-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d96fc-204">Confira também</span><span class="sxs-lookup"><span data-stu-id="d96fc-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d96fc-205">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="d96fc-205">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d96fc-206">**\_PnPDeviceProperty Win32**</span><span class="sxs-lookup"><span data-stu-id="d96fc-206">**Win32\_PnPDeviceProperty**</span></span>](win32-pnpdeviceproperty.md)
</dt> <dt>

[<span data-ttu-id="d96fc-207">**Getdeviceproperties**</span><span class="sxs-lookup"><span data-stu-id="d96fc-207">**GetDeviceProperties**</span></span>](getdeviceproperties-win32-pnpentity.md)
</dt> </dl>

 

 




