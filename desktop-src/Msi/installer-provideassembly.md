---
description: O método ProvideAssembly do objeto do instalador retorna o caminho instalado de um assembly.
ms.assetid: c99b1934-3834-478b-ab1d-7e7583dba779
title: Instalador::P método rovideAssembly
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideAssembly
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f81c9ab9b43b814307242cc828326b2b7e7d79fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747332"
---
# <a name="installerprovideassembly-method"></a><span data-ttu-id="8e532-103">Instalador::P método rovideAssembly</span><span class="sxs-lookup"><span data-stu-id="8e532-103">Installer::ProvideAssembly method</span></span>

<span data-ttu-id="8e532-104">O método **ProvideAssembly** do objeto do [**instalador**](installer-object.md) retorna o caminho instalado de um assembly.</span><span class="sxs-lookup"><span data-stu-id="8e532-104">The **ProvideAssembly** method of the [**Installer**](installer-object.md) object returns the installed path of an assembly.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e532-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e532-105">Syntax</span></span>


```JScript
retVal = .ProvideAssembly(
  assembly,
  appContext,
  installMode,
  assemblyInfo
)
```



## <a name="parameters"></a><span data-ttu-id="8e532-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e532-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e532-107">*)*</span><span class="sxs-lookup"><span data-stu-id="8e532-107">*assembly*</span></span> 
</dt> <dd>

<span data-ttu-id="8e532-108">O nome forte do assembly instalado que deve ser consultado.</span><span class="sxs-lookup"><span data-stu-id="8e532-108">The strong name of installed assembly that is to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="8e532-109">*appContext*</span><span class="sxs-lookup"><span data-stu-id="8e532-109">*appContext*</span></span> 
</dt> <dd>

<span data-ttu-id="8e532-110">Defina como NULL para assemblies globais.</span><span class="sxs-lookup"><span data-stu-id="8e532-110">Set to null for global assemblies.</span></span> <span data-ttu-id="8e532-111">Para assemblies privados, defina *appContext* como o caminho completo do arquivo de configuração do aplicativo ou para o caminho completo do arquivo executável do aplicativo ao qual o assembly foi tornado particular.</span><span class="sxs-lookup"><span data-stu-id="8e532-111">For private assemblies, set *appContext* to the full path of the application configuration file or to the full path of the executable file of the application to which the assembly has been made private.</span></span>

</dd> <dt>

<span data-ttu-id="8e532-112">*installMode*</span><span class="sxs-lookup"><span data-stu-id="8e532-112">*installMode*</span></span> 
</dt> <dd>

<span data-ttu-id="8e532-113">Define o modo de instalação.</span><span class="sxs-lookup"><span data-stu-id="8e532-113">Defines the installation mode.</span></span> <span data-ttu-id="8e532-114">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e532-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="8e532-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8e532-115">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="8e532-116">Significado</span><span class="sxs-lookup"><span data-stu-id="8e532-116">Meaning</span></span>                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="8e532-117"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8e532-117"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                                | <span data-ttu-id="8e532-118">Forneça o componente e execute qualquer instalação necessária para fornecer o componente.</span><span class="sxs-lookup"><span data-stu-id="8e532-118">Provide the component and perform any installation necessary to provide the component.</span></span> <br/>                                                                                        |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="8e532-119"><dt>**msiInstallModeExisting**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="8e532-119"><dt>**msiInstallModeExisting**</dt> <dt>-1</dt></span></span> </dl>                                                                                           | <span data-ttu-id="8e532-120">Forneça o componente somente se o recurso existir.</span><span class="sxs-lookup"><span data-stu-id="8e532-120">Provide the component only if the feature exists.</span></span> <span data-ttu-id="8e532-121">Esta opção verificará se o assembly existe.</span><span class="sxs-lookup"><span data-stu-id="8e532-121">This option will verify that the assembly exists.</span></span><br/>                                                                            |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="8e532-122"><dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt></span><span class="sxs-lookup"><span data-stu-id="8e532-122"><dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt></span></span> </dl>                                                                               | <span data-ttu-id="8e532-123">Forneça o componente somente se o recurso existir.</span><span class="sxs-lookup"><span data-stu-id="8e532-123">Provide the component only if the feature exists.</span></span> <span data-ttu-id="8e532-124">Essa opção não verifica se o assembly existe.</span><span class="sxs-lookup"><span data-stu-id="8e532-124">This option does not verify that the assembly exists.</span></span><br/>                                                                        |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="8e532-125"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt></span><span class="sxs-lookup"><span data-stu-id="8e532-125"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt></span></span> </dl>                                                   | <span data-ttu-id="8e532-126">Fornece o assembly somente se o assembly for instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="8e532-126">Provides the assembly only if the assembly is installed local.</span></span><br/>                                                                                                                 |
| <span id="Combination_of_the_flags_used_by_ReinstallFeature"></span><span id="combination_of_the_flags_used_by_reinstallfeature"></span><span id="COMBINATION_OF_THE_FLAGS_USED_BY_REINSTALLFEATURE"></span><dl> <span data-ttu-id="8e532-127"><dt>**Combinação dos sinalizadores usados pelo [ **ReinstallFeature**](installer-reinstallfeature.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8e532-127"><dt>**Combination of the flags used by [**ReinstallFeature**](installer-reinstallfeature.md)**</dt></span></span> </dl> | <span data-ttu-id="8e532-128">Chama o método [**ReinstallFeature**](installer-reinstallfeature.md) para reinstalar o recurso usando esse parâmetro para *reinstalarmode* e, em seguida, retorna o caminho do assembly.</span><span class="sxs-lookup"><span data-stu-id="8e532-128">Calls the [**ReinstallFeature**](installer-reinstallfeature.md) method to reinstall the feature using this parameter for *ReinstallMode*, and then returns the assembly path.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8e532-129">*assemblyInfo*</span><span class="sxs-lookup"><span data-stu-id="8e532-129">*assemblyInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="8e532-130">Informações de assembly e tipo de assembly.</span><span class="sxs-lookup"><span data-stu-id="8e532-130">Assembly information and assembly type.</span></span> <span data-ttu-id="8e532-131">Defina como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e532-131">Set to one of the following values.</span></span>



| <span data-ttu-id="8e532-132">Valor</span><span class="sxs-lookup"><span data-stu-id="8e532-132">Value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="8e532-133">Significado</span><span class="sxs-lookup"><span data-stu-id="8e532-133">Meaning</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="msiProvideAssemblyNet"></span><span id="msiprovideassemblynet"></span><span id="MSIPROVIDEASSEMBLYNET"></span><dl> <span data-ttu-id="8e532-134"><dt>**msiProvideAssemblyNet**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8e532-134"><dt>**msiProvideAssemblyNet**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="8e532-135">Um assembly .NET.</span><span class="sxs-lookup"><span data-stu-id="8e532-135">A .NET assembly.</span></span><br/>               |
| <span id="msiProvideAssemblyWin32"></span><span id="msiprovideassemblywin32"></span><span id="MSIPROVIDEASSEMBLYWIN32"></span><dl> <span data-ttu-id="8e532-136"><dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8e532-136"><dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="8e532-137">Um assembly lado a lado do Win32.</span><span class="sxs-lookup"><span data-stu-id="8e532-137">A Win32 side-by-side assembly.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e532-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e532-138">Return value</span></span>

<span data-ttu-id="8e532-139">O caminho para o assembly instalado.</span><span class="sxs-lookup"><span data-stu-id="8e532-139">The path to the installed assembly.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e532-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e532-140">Remarks</span></span>

<span data-ttu-id="8e532-141">O método **ProvideAssembly** usa a função [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) .</span><span class="sxs-lookup"><span data-stu-id="8e532-141">The **ProvideAssembly** method uses the [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) function.</span></span>

## <a name="examples"></a><span data-ttu-id="8e532-142">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8e532-142">Examples</span></span>

<span data-ttu-id="8e532-143">O exemplo de script a seguir demonstra o uso do método ProvideAssembly.</span><span class="sxs-lookup"><span data-stu-id="8e532-143">The following sample script demonstrates the use of the ProvideAssembly method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' ProvideAssembly - .NET global
'   
MsgBox Installer.ProvideAssembly("System.Security,Version=""1.0.5000.0"",PublicKeyToken=""b03f5f7f11d50a3a"",Culture=""neutral"",FileVersion=""1.1.4322.573""", vbNullString, 0, 0)

'
' ProvideAssembly - .NET private
'   
MsgBox Installer.ProvideAssembly("Sample,Version=""1.0.0.0"",Culture=""neutral""", "C:\Program Files\Microsoft\Sample\Sample.exe", 0, 0)

'
' ProvideAssembly - win32 global
'
MsgBox Installer.ProvideAssembly("Microsoft.MSXML2,publicKeyToken=""6bd6b9abf345378f"",version=""4.1.0.0"",type=""win32"",processorArchitecture=""x86""", vbNullString , -2, 1)
```



## <a name="requirements"></a><span data-ttu-id="8e532-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e532-144">Requirements</span></span>



| <span data-ttu-id="8e532-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e532-145">Requirement</span></span> | <span data-ttu-id="8e532-146">Valor</span><span class="sxs-lookup"><span data-stu-id="8e532-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e532-147">Versão</span><span class="sxs-lookup"><span data-stu-id="8e532-147">Version</span></span><br/> | <span data-ttu-id="8e532-148">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8e532-148">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8e532-149">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8e532-149">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8e532-150">Windows Installer 4,5 no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="8e532-150">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="8e532-151">DLL</span><span class="sxs-lookup"><span data-stu-id="8e532-151">DLL</span></span><br/>     | <dl> <span data-ttu-id="8e532-152"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e532-152"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="8e532-153">IID</span><span class="sxs-lookup"><span data-stu-id="8e532-153">IID</span></span><br/>     | <span data-ttu-id="8e532-154">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8e532-154">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="8e532-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e532-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e532-156">**Instalador**</span><span class="sxs-lookup"><span data-stu-id="8e532-156">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="8e532-157">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="8e532-157">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




