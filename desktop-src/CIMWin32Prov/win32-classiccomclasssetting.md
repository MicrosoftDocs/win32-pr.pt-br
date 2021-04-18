---
description: Representa as configurações de um componente de Component Object Model (COM).
ms.assetid: 18d9ddf2-184d-4680-8d56-f012c608ff7d
ms.tgt_platform: multiple
title: Classe Win32_ClassicCOMClassSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSetting
- Win32_ClassicCOMClassSetting.Caption
- Win32_ClassicCOMClassSetting.Description
- Win32_ClassicCOMClassSetting.SettingID
- Win32_ClassicCOMClassSetting.AppID
- Win32_ClassicCOMClassSetting.AutoConvertToClsid
- Win32_ClassicCOMClassSetting.AutoTreatAsClsid
- Win32_ClassicCOMClassSetting.ComponentId
- Win32_ClassicCOMClassSetting.Control
- Win32_ClassicCOMClassSetting.DefaultIcon
- Win32_ClassicCOMClassSetting.InprocHandler
- Win32_ClassicCOMClassSetting.InprocHandler32
- Win32_ClassicCOMClassSetting.InprocServer
- Win32_ClassicCOMClassSetting.InprocServer32
- Win32_ClassicCOMClassSetting.Insertable
- Win32_ClassicCOMClassSetting.JavaClass
- Win32_ClassicCOMClassSetting.LocalServer
- Win32_ClassicCOMClassSetting.LocalServer32
- Win32_ClassicCOMClassSetting.LongDisplayName
- Win32_ClassicCOMClassSetting.ProgId
- Win32_ClassicCOMClassSetting.ShortDisplayName
- Win32_ClassicCOMClassSetting.ThreadingModel
- Win32_ClassicCOMClassSetting.ToolBoxBitmap32
- Win32_ClassicCOMClassSetting.TreatAsClsid
- Win32_ClassicCOMClassSetting.TypeLibraryId
- Win32_ClassicCOMClassSetting.Version
- Win32_ClassicCOMClassSetting.VersionIndependentProgId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f263a888ce9dea80444023faff57998bc3f2c1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771698"
---
# <a name="win32_classiccomclasssetting-class"></a><span data-ttu-id="30ef6-103">\_Classe Win32 ClassicCOMClassSetting</span><span class="sxs-lookup"><span data-stu-id="30ef6-103">Win32\_ClassicCOMClassSetting class</span></span>

<span data-ttu-id="30ef6-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ClassicCOMClassSetting do Win32** representa as configurações de um componente com (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="30ef6-104">The **Win32\_ClassicCOMClassSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings of a Component Object Model (COM) component.</span></span>

<span data-ttu-id="30ef6-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="30ef6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="30ef6-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="30ef6-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ef6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30ef6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A562-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  string  AutoConvertToClsid;
  string  AutoTreatAsClsid;
  string  ComponentId;
  boolean Control;
  string  DefaultIcon;
  string  InprocHandler;
  string  InprocHandler32;
  string  InprocServer;
  string  InprocServer32;
  boolean Insertable;
  boolean JavaClass;
  string  LocalServer;
  string  LocalServer32;
  string  LongDisplayName;
  string  ProgId;
  string  ShortDisplayName;
  string  ThreadingModel;
  string  ToolBoxBitmap32;
  string  TreatAsClsid;
  string  TypeLibraryId;
  string  Version;
  string  VersionIndependentProgId;
};
```

## <a name="members"></a><span data-ttu-id="30ef6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="30ef6-108">Members</span></span>

<span data-ttu-id="30ef6-109">A classe **Win32 \_ ClassicCOMClassSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="30ef6-109">The **Win32\_ClassicCOMClassSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="30ef6-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="30ef6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30ef6-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="30ef6-111">Properties</span></span>

<span data-ttu-id="30ef6-112">A classe **Win32 \_ ClassicCOMClassSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="30ef6-112">The **Win32\_ClassicCOMClassSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30ef6-113">**AppID**</span><span class="sxs-lookup"><span data-stu-id="30ef6-113">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-116">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \[ AppID \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[AppID\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-117">GUID (identificador global exclusivo) para o aplicativo COM usando este componente COM.</span><span class="sxs-lookup"><span data-stu-id="30ef6-117">Globally unique identifier (GUID) for the COM application using this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-118">**AutoConvertToClsid**</span><span class="sxs-lookup"><span data-stu-id="30ef6-118">**AutoConvertToClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-121">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ conversão Autoconverter em \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-121">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AutoConvertTo\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-122">GUID da classe COM na qual esse componente COM será automaticamente convertido.</span><span class="sxs-lookup"><span data-stu-id="30ef6-122">GUID of the COM class to which this COM component will automatically be converted.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-123">**AutoTreatAsClsid**</span><span class="sxs-lookup"><span data-stu-id="30ef6-123">**AutoTreatAsClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-126">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ autotratáas \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-126">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AutoTreatAs\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-127">GUID do componente COM que emulará automaticamente as instâncias dessa classe.</span><span class="sxs-lookup"><span data-stu-id="30ef6-127">GUID for the COM component that will automatically emulate instances of this class.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-128">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="30ef6-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-131">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="30ef6-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-132">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="30ef6-132">Short textual description of the current object.</span></span>

<span data-ttu-id="30ef6-133">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="30ef6-133">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-134">**ComponentId**</span><span class="sxs-lookup"><span data-stu-id="30ef6-134">**ComponentId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-137">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-138">GUID deste componente COM.</span><span class="sxs-lookup"><span data-stu-id="30ef6-138">GUID of this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-139">**Controle**</span><span class="sxs-lookup"><span data-stu-id="30ef6-139">**Control**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-140">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="30ef6-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-142">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ controle")</span><span class="sxs-lookup"><span data-stu-id="30ef6-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Control")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-143">O componente COM é um controle OLE.</span><span class="sxs-lookup"><span data-stu-id="30ef6-143">COM component is an OLE control.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-144">**DefaultIcon**</span><span class="sxs-lookup"><span data-stu-id="30ef6-144">**DefaultIcon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-147">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ DefaultIcon \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\DefaultIcon\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-148">Caminho para o arquivo executável e o identificador de recurso do ícone padrão usado pela classe.</span><span class="sxs-lookup"><span data-stu-id="30ef6-148">Path to the executable file and resource identifier of the default icon used by the class.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-149">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="30ef6-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-152">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="30ef6-152">Textual description of the current object.</span></span>

<span data-ttu-id="30ef6-153">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="30ef6-153">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-154">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="30ef6-154">**InprocHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-157">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocHandler\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-158">Caminho completo incluindo nome de arquivo ou somente nome de arquivo para um manipulador personalizado de 16 bits para o componente COM.</span><span class="sxs-lookup"><span data-stu-id="30ef6-158">Full path including filename or only filename to a 16-bit custom handler for the COM component.</span></span> <span data-ttu-id="30ef6-159">O provedor nem sempre retorna o caminho completo.</span><span class="sxs-lookup"><span data-stu-id="30ef6-159">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-160">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="30ef6-160">**InprocHandler32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-163">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler32 \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocHandler32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-164">Caminho completo incluindo nome de arquivo ou somente nome de arquivo para um manipulador personalizado de 32 bits para o componente COM.</span><span class="sxs-lookup"><span data-stu-id="30ef6-164">Full path including filename or only filename to a 32-bit custom handler for the COM component.</span></span> <span data-ttu-id="30ef6-165">O provedor nem sempre retorna o caminho completo.</span><span class="sxs-lookup"><span data-stu-id="30ef6-165">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-166">**InprocServer**</span><span class="sxs-lookup"><span data-stu-id="30ef6-166">**InprocServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-169">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-169">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-170">Caminho completo incluindo nome de arquivo ou somente nome de arquivo para uma DLL de servidor em processo de 16 bits para este componente COM.</span><span class="sxs-lookup"><span data-stu-id="30ef6-170">Full path including filename or only filename to a 16-bit in-process server DLL for this COM component.</span></span> <span data-ttu-id="30ef6-171">O provedor nem sempre retorna o caminho completo.</span><span class="sxs-lookup"><span data-stu-id="30ef6-171">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-172">**InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="30ef6-172">**InprocServer32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-175">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-176">Caminho completo incluindo nome de arquivo ou somente nome de arquivo para uma DLL de servidor em processo de 32 bits para este componente COM.</span><span class="sxs-lookup"><span data-stu-id="30ef6-176">Full path including filename or only filename to a 32-bit in-process server DLL for this COM component.</span></span> <span data-ttu-id="30ef6-177">O provedor nem sempre retorna o caminho completo.</span><span class="sxs-lookup"><span data-stu-id="30ef6-177">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-178">**Insertable**</span><span class="sxs-lookup"><span data-stu-id="30ef6-178">**Insertable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-179">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="30ef6-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-181">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ Insertable")</span><span class="sxs-lookup"><span data-stu-id="30ef6-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Insertable")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-182">O componente COM pode ser inserido em aplicativos de contêiner OLE.</span><span class="sxs-lookup"><span data-stu-id="30ef6-182">COM component can be inserted into OLE container applications.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-183">**JavaClass**</span><span class="sxs-lookup"><span data-stu-id="30ef6-183">**JavaClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-184">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="30ef6-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-186">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ JavaClass \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-186">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[JavaClass\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-187">O componente COM é um componente Java.</span><span class="sxs-lookup"><span data-stu-id="30ef6-187">COM component is a Java component.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-188">**LocalServer**</span><span class="sxs-lookup"><span data-stu-id="30ef6-188">**LocalServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-191">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-191">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\LocalServer\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-192">Caminho completo incluindo nome de arquivo ou somente nome de arquivo para um aplicativo de servidor local de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="30ef6-192">Full path including filename or only filename to a 16-bit local server application.</span></span> <span data-ttu-id="30ef6-193">O provedor nem sempre retorna o caminho completo.</span><span class="sxs-lookup"><span data-stu-id="30ef6-193">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-194">**LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="30ef6-194">**LocalServer32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-197">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer32 \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-197">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\LocalServer32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-198">Caminho completo incluindo nome de arquivo ou somente nome de arquivo para um aplicativo de servidor local de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="30ef6-198">Full path including filename or only filename to a 32-bit local server application.</span></span> <span data-ttu-id="30ef6-199">O provedor nem sempre retorna o caminho completo.</span><span class="sxs-lookup"><span data-stu-id="30ef6-199">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-200">**LongDisplayName**</span><span class="sxs-lookup"><span data-stu-id="30ef6-200">**LongDisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-203">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 3 \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AuxUserType\\\\3\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-204">Nome completo do aplicativo COM.</span><span class="sxs-lookup"><span data-stu-id="30ef6-204">Full name of the COM application.</span></span> <span data-ttu-id="30ef6-205">Ele é usado em áreas como o campo **resultados** da caixa de diálogo de **colar especial do OLE** .</span><span class="sxs-lookup"><span data-stu-id="30ef6-205">It is used in areas such as the **Results** field of the **OLE Paste Special** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-206">**ProgId**</span><span class="sxs-lookup"><span data-stu-id="30ef6-206">**ProgId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-209">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ ProgID \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-209">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\ProgID\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-210">Identificador programático associado ao componente COM.</span><span class="sxs-lookup"><span data-stu-id="30ef6-210">Programmatic identifier associated with the COM component.</span></span> <span data-ttu-id="30ef6-211">O formato de um ProgID é <<Component. <versão.</span><span class="sxs-lookup"><span data-stu-id="30ef6-211">The format of a ProgID is <Vendor.<Component.<Version.</span></span> <span data-ttu-id="30ef6-212">Não há garantia de que esse identificador seja exclusivo.</span><span class="sxs-lookup"><span data-stu-id="30ef6-212">This identifier is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-213">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="30ef6-213">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-214">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-216">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="30ef6-216">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-217">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="30ef6-217">Identifier by which the current object is known.</span></span>

<span data-ttu-id="30ef6-218">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="30ef6-218">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-219">**ShortDisplayName**</span><span class="sxs-lookup"><span data-stu-id="30ef6-219">**ShortDisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-220">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-222">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 2 \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-222">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AuxUserType\\\\2\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-223">Nome curto do aplicativo COM (usado em menus e pop-ups).</span><span class="sxs-lookup"><span data-stu-id="30ef6-223">Short name of the COM application (used in menus and pop-ups).</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-224">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="30ef6-224">**ThreadingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-227">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ ThreadingModel \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[ThreadingModel\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-228">Modelo de Threading usado por classes COM em processo.</span><span class="sxs-lookup"><span data-stu-id="30ef6-228">Threading model used by in-process COM classes.</span></span> <span data-ttu-id="30ef6-229">Se essa propriedade for **nula**, nenhum modelo de Threading será usado.</span><span class="sxs-lookup"><span data-stu-id="30ef6-229">If this property is **NULL**, then no threading model is used.</span></span> <span data-ttu-id="30ef6-230">O componente é criado no thread principal do cliente e as chamadas de outros threads são empacotadas para esse thread.</span><span class="sxs-lookup"><span data-stu-id="30ef6-230">The component is created on the main thread of the client and calls from other threads are marshaled to this thread.</span></span>

<span data-ttu-id="30ef6-231">O modelo de apartamento especifica que os componentes podem ser inseridos por um e apenas um thread.</span><span class="sxs-lookup"><span data-stu-id="30ef6-231">The Apartment model specifies that components may be entered by one and only one thread.</span></span> <span data-ttu-id="30ef6-232">Os dados comuns mantidos por esses tipos de servidores de objetos devem ser protegidos contra colisões de thread porque o servidor de objetos dá suporte a vários componentes.</span><span class="sxs-lookup"><span data-stu-id="30ef6-232">Common data held by these types of object servers must be protected against thread collisions because the object server supports multiple components.</span></span> <span data-ttu-id="30ef6-233">Cada componente pode ser inserido simultaneamente por threads diferentes.</span><span class="sxs-lookup"><span data-stu-id="30ef6-233">Each component can be entered simultaneously by different threads.</span></span>

<span data-ttu-id="30ef6-234">O modelo gratuito especifica que os componentes não colocam restrições em quais threads ou quantos threads podem inserir o objeto.</span><span class="sxs-lookup"><span data-stu-id="30ef6-234">The Free model specifies that components place no restrictions on which threads or how many threads can enter the object.</span></span> <span data-ttu-id="30ef6-235">O objeto não pode conter dados específicos de thread e deve proteger seus dados de acesso simultâneo por vários threads.</span><span class="sxs-lookup"><span data-stu-id="30ef6-235">The object cannot contain thread-specific data and must protect its data from simultaneous access by multiple threads.</span></span> <span data-ttu-id="30ef6-236">No entanto, os componentes de thread livre não podem ser acessados por threads de apartamento diretamente e as chamadas para eles são empacotadas no apartamento do cliente.</span><span class="sxs-lookup"><span data-stu-id="30ef6-236">Free-threaded components however, cannot be accessed by apartment threads directly, and calls to them are marshaled across from the client apartment.</span></span>

<span data-ttu-id="30ef6-237">Quando ambos são especificados, os componentes podem ser usados nos modos Apartment-Threaded ou Free-threaded.</span><span class="sxs-lookup"><span data-stu-id="30ef6-237">When Both is specified, components can be used in either apartment-threaded or free-threaded modes.</span></span> <span data-ttu-id="30ef6-238">Esses componentes podem ser inseridos por vários threads, proteger seus dados de colisões de thread e não conter dados específicos de thread.</span><span class="sxs-lookup"><span data-stu-id="30ef6-238">These components can be entered by multiple threads, protect their data from thread collisions, and do not contain thread-specific data.</span></span>

<span data-ttu-id="30ef6-239">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="30ef6-239">The values are:</span></span>

<dl> <dd><span data-ttu-id="30ef6-240">Sta</span><span class="sxs-lookup"><span data-stu-id="30ef6-240">"Apartment"</span></span></dd> <dd><span data-ttu-id="30ef6-241">Informações</span><span class="sxs-lookup"><span data-stu-id="30ef6-241">"Free"</span></span></dd> <dd><span data-ttu-id="30ef6-242">Mesmo</span><span class="sxs-lookup"><span data-stu-id="30ef6-242">"Both"</span></span></dd> </dl>

<dt>

<span id="Apartment"></span><span id="apartment"></span><span id="APARTMENT"></span>

<span data-ttu-id="30ef6-243">**Apartamento** ("Apartment")</span><span class="sxs-lookup"><span data-stu-id="30ef6-243">**Apartment** ("Apartment")</span></span>


</dt> <dd></dd> <dt>

<span id="Free"></span><span id="free"></span><span id="FREE"></span>

<span data-ttu-id="30ef6-244">**Gratuito** ("gratuito")</span><span class="sxs-lookup"><span data-stu-id="30ef6-244">**Free** ("Free")</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="30ef6-245">**Ambos** ("both")</span><span class="sxs-lookup"><span data-stu-id="30ef6-245">**Both** ("Both")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="30ef6-246">**ToolBoxBitmap32**</span><span class="sxs-lookup"><span data-stu-id="30ef6-246">**ToolBoxBitmap32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-247">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-249">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ ToolBoxBitmap32 \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-249">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\ToolBoxBitmap32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-250">O nome do módulo e o identificador de recurso para um pequeno bitmap (16x16) usado para a face de uma barra de ferramentas ou botão de caixa de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="30ef6-250">Module name and resource identifier for a small (16x16) bitmap used for the face of a toolbar or toolbox button.</span></span> <span data-ttu-id="30ef6-251">Usado quando o componente COM é um controle OLE ou ActiveX.</span><span class="sxs-lookup"><span data-stu-id="30ef6-251">Used when the COM component is an OLE or ActiveX control.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-252">**TreatAsClsid**</span><span class="sxs-lookup"><span data-stu-id="30ef6-252">**TreatAsClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-253">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-255">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ trata de \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-255">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\TreatAs\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-256">GUID de um componente COM que pode emular instâncias desse componente.</span><span class="sxs-lookup"><span data-stu-id="30ef6-256">GUID of a COM component that can emulate instances of this component.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-257">**TypeLibraryId**</span><span class="sxs-lookup"><span data-stu-id="30ef6-257">**TypeLibraryId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-260">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ TypeLib \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-260">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\TypeLib\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-261">GUID da biblioteca de tipos para este componente COM.</span><span class="sxs-lookup"><span data-stu-id="30ef6-261">GUID for the type library for this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-262">**Versão**</span><span class="sxs-lookup"><span data-stu-id="30ef6-262">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-263">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-265">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ versão \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-265">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Version\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-266">Número de versão desta classe COM.</span><span class="sxs-lookup"><span data-stu-id="30ef6-266">Version number of this COM class.</span></span>

</dd> <dt>

<span data-ttu-id="30ef6-267">**VersionIndependentProgId**</span><span class="sxs-lookup"><span data-stu-id="30ef6-267">**VersionIndependentProgId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ef6-268">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="30ef6-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30ef6-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ef6-270">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ VersionIndependentProgId \[ padrão \] ")</span><span class="sxs-lookup"><span data-stu-id="30ef6-270">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\VersionIndependentProgId\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="30ef6-271">Identificador de programa consistente para todas as versões do mesmo programa.</span><span class="sxs-lookup"><span data-stu-id="30ef6-271">Program identifier that is consistent for all versions of the same program.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30ef6-272">Comentários</span><span class="sxs-lookup"><span data-stu-id="30ef6-272">Remarks</span></span>

<span data-ttu-id="30ef6-273">A classe **Win32 \_ ClassicCOMClassSetting** é derivada da [**\_ configuração do Win32**](win32-comsetting.md).</span><span class="sxs-lookup"><span data-stu-id="30ef6-273">The **Win32\_ClassicCOMClassSetting** class is derived from [**Win32\_COMSetting**](win32-comsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30ef6-274">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30ef6-274">Requirements</span></span>



| <span data-ttu-id="30ef6-275">Requisito</span><span class="sxs-lookup"><span data-stu-id="30ef6-275">Requirement</span></span> | <span data-ttu-id="30ef6-276">Valor</span><span class="sxs-lookup"><span data-stu-id="30ef6-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30ef6-277">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30ef6-277">Minimum supported client</span></span><br/> | <span data-ttu-id="30ef6-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30ef6-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="30ef6-279">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30ef6-279">Minimum supported server</span></span><br/> | <span data-ttu-id="30ef6-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30ef6-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="30ef6-281">Namespace</span><span class="sxs-lookup"><span data-stu-id="30ef6-281">Namespace</span></span><br/>                | <span data-ttu-id="30ef6-282">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="30ef6-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="30ef6-283">MOF</span><span class="sxs-lookup"><span data-stu-id="30ef6-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30ef6-284"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30ef6-284"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="30ef6-285">DLL</span><span class="sxs-lookup"><span data-stu-id="30ef6-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30ef6-286"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30ef6-286"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30ef6-287">Confira também</span><span class="sxs-lookup"><span data-stu-id="30ef6-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ef6-288">**Configuração do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="30ef6-288">**Win32\_COMSetting**</span></span>](win32-comsetting.md)
</dt> <dt>

<span data-ttu-id="30ef6-289">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="30ef6-289">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

