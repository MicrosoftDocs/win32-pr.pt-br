---
title: Compilando o provedor de serviços de exemplo usando Visual Studio
description: Compilando o provedor de serviços de exemplo usando Visual Studio
ms.assetid: db0ecc18-d5b0-47d8-9b3f-3a9644343de8
keywords:
- Windows Mídia Gerenciador de Dispositivos, exemplos
- Gerenciador de Dispositivos,exemplos
- Windows Mídia Gerenciador de Dispositivos, exemplo de provedor de serviços
- Gerenciador de Dispositivos, exemplo de provedor de serviços
- provedores de serviços, exemplos
- exemplos, provedores de serviços
- exemplos, compilando usando Visual Studio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd220e314a6de0a9c5e4cf50ccd710a0236c3b3ec469247ef99f319b553b15c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586014"
---
# <a name="compiling-the-sample-service-provider-using-visual-studio"></a>Compilando o provedor de serviços de exemplo usando Visual Studio

O Windows SDK de Formato de Mídia não inclui um arquivo Visual Studio solução. No entanto, este documento inclui dois arquivos que permitem que você use Visual Studio para criar e depurar o provedor de serviços de exemplo. Ambos os arquivos fornecidos são para Visual Studio .NET 2003.

-   Salve o código a seguir como um arquivo de texto chamado mshdsp.vcproj na pasta <caminho de instalação do *SDK* > \\ WMFSDK \\ WMFSDK95 \\ WMDM \\ \\ mdsp mshdsp.


```C++
<?xml version="1.0" encoding="Windows-1252"?>
<VisualStudioProject
    ProjectType="Visual C++"
    Version="7.10"
    Name="mshdsp"
    ProjectGUID="{B0BD0EEB-2048-46E2-ADCB-DA058B246F5E}"
    Keyword="AtlProj">
    <Platforms>
        <Platform
            Name="Win32"/>
    </Platforms>
    <Configurations>
        <Configuration
            Name="Debug|Win32"
            OutputDirectory="Debug"
            IntermediateDirectory="Debug"
            ConfigurationType="2"
            UseOfATL="1"
            ATLMinimizesCRunTimeLibraryUsage="FALSE"
            CharacterSet="2">
            <Tool
                Name="VCCLCompilerTool"
                Optimization="0"
                AdditionalIncludeDirectories="..\..\inc"
                PreprocessorDefinitions="WIN32;_WINDOWS;_DEBUG;_USRDLL;_ATL_ATTRIBUTES;ATL_STATIC_REGISTRY;INC_OLE2;"
                MinimalRebuild="TRUE"
                BasicRuntimeChecks="3"
                RuntimeLibrary="3"
                UsePrecompiledHeader="0"
                WarningLevel="3"
                Detect64BitPortabilityProblems="TRUE"
                DebugInformationFormat="4"/>
            <Tool
                Name="VCCustomBuildTool"/>
            <Tool
                Name="VCLinkerTool"
                IgnoreImportLibrary="TRUE"
                AdditionalOptions="/FIXED:NO"
                AdditionalDependencies="advapi32.lib gdi32.lib kernel32.lib ole32.lib oleaut32.lib olepro32.lib user32.lib uuid.lib mssachlp.lib oldnames.lib shell32.lib atlsd.lib shlwapi.lib msvcrtd.lib"
                OutputFile="$(OutDir)/mshdsp.dll"
                LinkIncremental="2"
                AdditionalLibraryDirectories="..\..\lib"
                IgnoreAllDefaultLibraries="TRUE"
                ModuleDefinitionFile="MsHDSP.def"
                MergedIDLBaseFileName="_mshdsp.idl"
                GenerateDebugInformation="TRUE"
                SubSystem="2"
                OptimizeReferences="1"
                ImportLibrary="$(OutDir)/mshdsp.lib"
                TargetMachine="1"/>
            <Tool
                Name="VCMIDLTool"
                PreprocessorDefinitions="_DEBUG;UNICODE;_UNICODE"
                MkTypLibCompatible="FALSE"
                TargetEnvironment="1"
                GenerateStublessProxies="TRUE"
                TypeLibraryName="$(IntDir)/mshdsp.tlb"
                HeaderFileName="mshdsp.h"
                DLLDataFileName=""
                InterfaceIdentifierFileName="mshdsp_i.c"
                ProxyFileName="mshdsp_p.c"/>
            <Tool
                Name="VCPostBuildEventTool"
                Description="Performing registration"
                CommandLine="regsvr32 /s /c &quot;$(TargetPath)&quot;"/>
            <Tool
                Name="VCPreBuildEventTool"/>
            <Tool
                Name="VCPreLinkEventTool"/>
            <Tool
                Name="VCResourceCompilerTool"
                PreprocessorDefinitions="_DEBUG"
                Culture="1033"
                AdditionalIncludeDirectories="$(IntDir)"/>
            <Tool
                Name="VCWebServiceProxyGeneratorTool"/>
            <Tool
                Name="VCXMLDataGeneratorTool"/>
            <Tool
                Name="VCWebDeploymentTool"/>
            <Tool
                Name="VCManagedWrapperGeneratorTool"/>
            <Tool
                Name="VCAuxiliaryManagedWrapperGeneratorTool"/>
        </Configuration>
        <Configuration
            Name="Release|Win32"
            OutputDirectory="Release"
            IntermediateDirectory="Release"
            ConfigurationType="2"
            UseOfATL="1"
            ATLMinimizesCRunTimeLibraryUsage="FALSE"
            CharacterSet="2">
            <Tool
                Name="VCCLCompilerTool"
                PreprocessorDefinitions="WIN32;_WINDOWS;NDEBUG;_USRDLL;_ATL_ATTRIBUTES"
                RuntimeLibrary="2"
                UsePrecompiledHeader="3"
                WarningLevel="3"
                Detect64BitPortabilityProblems="TRUE"
                DebugInformationFormat="3"/>
            <Tool
                Name="VCCustomBuildTool"/>
            <Tool
                Name="VCLinkerTool"
                IgnoreImportLibrary="TRUE"
                OutputFile="$(OutDir)/mshdsp.dll"
                LinkIncremental="1"
                MergedIDLBaseFileName="_mshdsp.idl"
                GenerateDebugInformation="TRUE"
                SubSystem="2"
                OptimizeReferences="2"
                EnableCOMDATFolding="2"
                ImportLibrary="$(OutDir)/mshdsp.lib"
                TargetMachine="1"/>
            <Tool
                Name="VCMIDLTool"
                PreprocessorDefinitions="NDEBUG"
                MkTypLibCompatible="FALSE"
                TargetEnvironment="1"
                GenerateStublessProxies="TRUE"
                TypeLibraryName="$(IntDir)/mshdsp.tlb"
                HeaderFileName="mshdsp.h"
                DLLDataFileName=""
                InterfaceIdentifierFileName="mshdsp_i.c"
                ProxyFileName="mshdsp_p.c"/>
            <Tool
                Name="VCPostBuildEventTool"
                Description="Performing registration"
                CommandLine="regsvr32 /s /c &quot;$(TargetPath)&quot;"/>
            <Tool
                Name="VCPreBuildEventTool"/>
            <Tool
                Name="VCPreLinkEventTool"/>
            <Tool
                Name="VCResourceCompilerTool"
                PreprocessorDefinitions="NDEBUG"
                Culture="1033"
                AdditionalIncludeDirectories="$(IntDir)"/>
            <Tool
                Name="VCWebServiceProxyGeneratorTool"/>
            <Tool
                Name="VCXMLDataGeneratorTool"/>
            <Tool
                Name="VCWebDeploymentTool"/>
            <Tool
                Name="VCManagedWrapperGeneratorTool"/>
            <Tool
                Name="VCAuxiliaryManagedWrapperGeneratorTool"/>
        </Configuration>
    </Configurations>
    <References>
    </References>
    <Files>
        <Filter
            Name="Source Files"
            Filter="cpp;c;cxx;def;odl;idl;hpj;bat;asm;asmx"
            UniqueIdentifier="{4FC737F1-C7A5-4376-A066-2A32D752A2FF}">
            <File
                RelativePath=".\hdsppch.cpp">
            </File>
            <File
                RelativePath=".\key.c">
            </File>
            <File
                RelativePath=".\loghelp.cpp">
            </File>
            <File
                RelativePath=".\MDServiceProvider.cpp">
            </File>
            <File
                RelativePath=".\Mdsp.cpp">
            </File>
            <File
                RelativePath=".\MDSPDevice.cpp">
            </File>
            <File
                RelativePath=".\MDSPEnumDevice.cpp">
            </File>
            <File
                RelativePath=".\MDSPEnumStorage.cpp">
            </File>
            <File
                RelativePath=".\MDSPStorage.cpp">
            </File>
            <File
                RelativePath=".\MDSPStorageGlobals.cpp">
            </File>
            <File
                RelativePath=".\MDSPutil.cpp">
            </File>
            <File
                RelativePath=".\MsHDSP.def">
            </File>
            <File
                RelativePath=".\MsHDSP.idl">
            </File>
            <File
                RelativePath=".\proppage.cpp">
            </File>
        </Filter>
        <Filter
            Name="Header Files"
            Filter="h;hpp;hxx;hm;inl;inc;xsd"
            UniqueIdentifier="{93995380-89BD-4b04-88EB-625FBE52EBFB}">
            <File
                RelativePath=".\hdsppch.h">
            </File>
            <File
                RelativePath=".\hdsprc.h">
            </File>
            <File
                RelativePath=".\loghelp.h">
            </File>
            <File
                RelativePath=".\MDServiceProvider.h">
            </File>
            <File
                RelativePath=".\MdspDefs.h">
            </File>
            <File
                RelativePath=".\MDSPDevice.h">
            </File>
            <File
                RelativePath=".\MDSPEnumDevice.h">
            </File>
            <File
                RelativePath=".\MDSPEnumStorage.h">
            </File>
            <File
                RelativePath=".\MDSPStorage.h">
            </File>
            <File
                RelativePath=".\MDSPStorageGlobals.h">
            </File>
            <File
                RelativePath=".\proppage.h">
            </File>
            <File
                RelativePath=".\verinfo.h">
            </File>
        </Filter>
        <Filter
            Name="Resource Files"
            Filter="rc;ico;cur;bmp;dlg;rc2;rct;bin;rgs;gif;jpg;jpeg;jpe;resx"
            UniqueIdentifier="{67DA6AB6-F800-4c08-8B7A-83BB121AAD01}">
            <File
                RelativePath=".\icon_hd.ico">
            </File>
            <File
                RelativePath=".\MDServiceProvider.rgs">
            </File>
            <File
                RelativePath=".\mdsp.rc">
            </File>
            <File
                RelativePath=".\proppage.rgs">
            </File>
        </Filter>
        <File
            RelativePath=".\Makefile">
        </File>
        <File
            RelativePath=".\mshdsp.ncb">
        </File>
    </Files>
    <Globals>
    </Globals>
</VisualStudioProject>
```



-   Salve o código a seguir como um arquivo de texto chamado mshdsp.sln na mesma pasta em que você salvou mshdsp.vcproj.


```C++
Microsoft Visual Studio Solution File, Format Version 8.00
Project("{8BC9CEB8-8B4A-11D0-8D11-00A0C91BC942}") = "mshdsp", "mshdsp.vcproj", "{B0BD0EEB-2048-46E2-ADCB-DA058B246F5E}"
    ProjectSection(ProjectDependencies) = postProject
    EndProjectSection
EndProject
Global
    GlobalSection(SolutionConfiguration) = preSolution
        Debug = Debug
        Release = Release
    EndGlobalSection
    GlobalSection(ProjectConfiguration) = postSolution
        {B0BD0EEB-2048-46E2-ADCB-DA058B246F5E}.Debug.ActiveCfg = Debug|Win32
        {B0BD0EEB-2048-46E2-ADCB-DA058B246F5E}.Debug.Build.0 = Debug|Win32
        {B0BD0EEB-2048-46E2-ADCB-DA058B246F5E}.Release.ActiveCfg = Release|Win32
        {B0BD0EEB-2048-46E2-ADCB-DA058B246F5E}.Release.Build.0 = Release|Win32
        {C82A4AF9-14FD-474E-AD38-6EED4A0C0903}.Debug.ActiveCfg = Debug|Win32
        {C82A4AF9-14FD-474E-AD38-6EED4A0C0903}.Release.ActiveCfg = Release|Win32
    EndGlobalSection
    GlobalSection(ExtensibilityGlobals) = postSolution
    EndGlobalSection
    GlobalSection(ExtensibilityAddIns) = postSolution
    EndGlobalSection
EndGlobal
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Provedor de Serviços de Exemplo**](sample-service-provider.md)
</dt> </dl>

 

 




