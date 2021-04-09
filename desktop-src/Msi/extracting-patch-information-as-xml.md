---
description: As informações de sequenciamento e aplicabilidade do patch que são retornadas pela função MsiExtractPatchXMLData ou pelo método ExtractPatchXMLData estão no formato de um blob XML que contém os elementos e atributos identificados neste tópico.
ms.assetid: ea40ed1d-1ef9-44f3-8ae8-3d854e308a49
title: Extraindo informações de patch como XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e1e594d3ff2870ca1aaf87245c537045f95d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091136"
---
# <a name="extracting-patch-information-as-xml"></a><span data-ttu-id="2d56c-103">Extraindo informações de patch como XML</span><span class="sxs-lookup"><span data-stu-id="2d56c-103">Extracting Patch Information as XML</span></span>

<span data-ttu-id="2d56c-104">As informações de sequenciamento e aplicabilidade do patch que são retornadas pela função [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) ou pelo método [**ExtractPatchXMLData**](installer-extractpatchxmldata.md) estão no formato de um blob XML que contém os elementos e atributos identificados neste tópico.</span><span class="sxs-lookup"><span data-stu-id="2d56c-104">The patch sequencing and applicability information that is returned by the [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) function or the [**ExtractPatchXMLData**](installer-extractpatchxmldata.md) method is in the format of an XML blob that contains the elements and attributes that are identified in this topic.</span></span> <span data-ttu-id="2d56c-105">O blob XML pode ser fornecido para [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) e [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) em vez do arquivo de patch completo.</span><span class="sxs-lookup"><span data-stu-id="2d56c-105">The XML blob can be provided to [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) and [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) instead of the full patch file.</span></span>

-   <span data-ttu-id="2d56c-106">O elemento MsiPatch é o elemento superior do blob XML e contém informações sobre o patch.</span><span class="sxs-lookup"><span data-stu-id="2d56c-106">The MsiPatch element is the top element of the XML blob, and contains information about the patch.</span></span>

    <span data-ttu-id="2d56c-107">O atributo SchemaVersion especifica a versão da definição de esquema.</span><span class="sxs-lookup"><span data-stu-id="2d56c-107">The SchemaVersion attribute specifies the version of the schema definition.</span></span> <span data-ttu-id="2d56c-108">O esquema é especificado por MSIPatchApplicability. xsd e a versão do esquema atual é 1.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="2d56c-108">The schema is specified by MSIPatchApplicability.xsd and the current schema version is 1.0.0.0.</span></span> <span data-ttu-id="2d56c-109">O valor do atributo PatchGUID é o código de patch GUID para o pacote de patch obtido da propriedade [**Resumo do número de revisão**](revision-number-summary.md) no fluxo de [informações resumidas](summary-information-stream.md) do patch.</span><span class="sxs-lookup"><span data-stu-id="2d56c-109">The value of the PatchGUID attribute is the GUID patch code for the patch package obtained from the [**Revision Number Summary**](revision-number-summary.md) Property in the [Summary Information Stream](summary-information-stream.md) of the patch.</span></span> <span data-ttu-id="2d56c-110">O MinMsiVersion é a versão mínima do Windows Installer necessário para instalar o patch obtido da propriedade de [**Resumo de contagem de palavras**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="2d56c-110">The MinMsiVersion is the minimum version of the Windows Installer required to install the patch obtained from the [**Word Count Summary**](word-count-summary.md) Property.</span></span>

-   <span data-ttu-id="2d56c-111">O elemento TargetProduct é um elemento de contêiner para informações sobre um aplicativo que um patch tem como destino.</span><span class="sxs-lookup"><span data-stu-id="2d56c-111">The TargetProduct element is a container element for information about an application that a patch targets.</span></span>

    <span data-ttu-id="2d56c-112">Pode haver vários elementos TargetProduct se o patch puder ser aplicado a vários aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2d56c-112">There can be multiple TargetProduct elements if the patch can be applied to multiple applications.</span></span> <span data-ttu-id="2d56c-113">As informações no elemento TargetProduct são extraídas das transformações que são inseridas no patch.</span><span class="sxs-lookup"><span data-stu-id="2d56c-113">The information in the TargetProduct element is extracted from transforms that are embedded within the patch.</span></span>

-   <span data-ttu-id="2d56c-114">O elemento TargetProductCode contém o valor da propriedade [**ProductCode**](productcode.md) do aplicativo de destino antes da aplicação do patch.</span><span class="sxs-lookup"><span data-stu-id="2d56c-114">The TargetProductCode element contains the value of the [**ProductCode**](productcode.md) property of the target application before the patch has been applied.</span></span>

    <span data-ttu-id="2d56c-115">Pode haver vários elementos TargetProductCode se o patch puder ser aplicado a vários aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2d56c-115">There can be multiple TargetProductCode elements if the patch can be applied to multiple applications.</span></span>

-   <span data-ttu-id="2d56c-116">O elemento UpdatedProductCode contém o GUID de código do produto do aplicativo de destino após a aplicação do patch.</span><span class="sxs-lookup"><span data-stu-id="2d56c-116">The UpdatedProductCode element contains the product code GUID of the target application after the patch is applied.</span></span>

    <span data-ttu-id="2d56c-117">Esse elemento só estará presente se o patch alterar o valor da propriedade [**ProductCode**](productcode.md) .</span><span class="sxs-lookup"><span data-stu-id="2d56c-117">This element is only present if the patch changes the value of the [**ProductCode**](productcode.md) property.</span></span> <span data-ttu-id="2d56c-118">Um patch que altera o **ProductCode** é conhecido como uma [atualização principal](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="2d56c-118">A patch that changes the **ProductCode** is referred to as a [Major Upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="2d56c-119">O elemento TargetVersion contém a propriedade [**ProductVersion**](productversion.md) do aplicativo de destino antes da aplicação do patch.</span><span class="sxs-lookup"><span data-stu-id="2d56c-119">The TargetVersion element contains the [**ProductVersion**](productversion.md) property of the target application before the patch has been applied.</span></span>
-   <span data-ttu-id="2d56c-120">O elemento UpdateVersion contém o valor da propriedade [**ProductVersion**](productversion.md) do aplicativo de destino após a aplicação do patch.</span><span class="sxs-lookup"><span data-stu-id="2d56c-120">The UpdateVersion element contains the value of the [**ProductVersion**](productversion.md) property of the target application after the patch is applied.</span></span>

    <span data-ttu-id="2d56c-121">Esse elemento só estará presente se o patch alterar o valor da propriedade [**ProductVersion**](productversion.md) .</span><span class="sxs-lookup"><span data-stu-id="2d56c-121">This element is only present if the patch changes the value of the [**ProductVersion**](productversion.md) property.</span></span> <span data-ttu-id="2d56c-122">O blob XML para um patch que implementa uma [pequena atualização](small-updates.md), também conhecido como QFE, não incluirá esse elemento.</span><span class="sxs-lookup"><span data-stu-id="2d56c-122">The XML blob for a patch that implements a [Small Update](small-updates.md), also referred to as a QFE, will not include this element.</span></span> <span data-ttu-id="2d56c-123">O blob XML para um patch que implementa uma atualização secundária, também conhecida como service pack, incluirá esse elemento.</span><span class="sxs-lookup"><span data-stu-id="2d56c-123">The XML blob for a patch that implements a minor upgrade, also referred to as a service pack, will include this element.</span></span>

-   <span data-ttu-id="2d56c-124">O elemento TargetLanguage contém o valor da propriedade [**ProductLanguage**](productlanguage.md) do aplicativo de destino antes da aplicação do patch.</span><span class="sxs-lookup"><span data-stu-id="2d56c-124">The TargetLanguage element contains the value of the [**ProductLanguage**](productlanguage.md) property of the target application before the patch has been applied.</span></span>
-   <span data-ttu-id="2d56c-125">O elemento UpdatedLanguages contém o valor da propriedade [**ProductLanguage**](productlanguage.md) após a aplicação do patch.</span><span class="sxs-lookup"><span data-stu-id="2d56c-125">The UpdatedLanguages element contains the value of the [**ProductLanguage**](productlanguage.md) property after the patch has been applied.</span></span>
-   <span data-ttu-id="2d56c-126">O elemento UpgradeCode contém o valor da propriedade [**UpgradeCode**](upgradecode.md) do aplicativo de destino.</span><span class="sxs-lookup"><span data-stu-id="2d56c-126">The UpgradeCode element contains the value of the [**UpgradeCode**](upgradecode.md) property of the target application.</span></span>
-   <span data-ttu-id="2d56c-127">O elemento ObsoletedPatch contém os códigos de patch (GUIDs) dos patches que são especificados como obsoletos por esse patch.</span><span class="sxs-lookup"><span data-stu-id="2d56c-127">The ObsoletedPatch element contains the patch codes (GUIDs) of the patches that are specified as obsolete by this patch.</span></span>

    <span data-ttu-id="2d56c-128">A lista de patches obsoletos é obtida do [**Resumo do número de revisão**](revision-number-summary.md) no fluxo de [informações resumidas](summary-information-stream.md) do patch.</span><span class="sxs-lookup"><span data-stu-id="2d56c-128">The list of obsolete patches is obtained from [**Revision Number Summary**](revision-number-summary.md) in the [Summary Information Stream](summary-information-stream.md) of the patch.</span></span>

-   <span data-ttu-id="2d56c-129">O elemento SequenceData contém informações de sequenciamento de patch para o patch.</span><span class="sxs-lookup"><span data-stu-id="2d56c-129">The SequenceData element contains patch sequencing information for the patch.</span></span>

    <span data-ttu-id="2d56c-130">Pode haver vários elementos SequenceData no blob XML.</span><span class="sxs-lookup"><span data-stu-id="2d56c-130">There can be multiple SequenceData elements in the XML blob.</span></span> <span data-ttu-id="2d56c-131">Cada elemento SequenceData contém as informações em uma linha da [tabela MsiPatchSequence](msipatchsequence-table.md) do patch.</span><span class="sxs-lookup"><span data-stu-id="2d56c-131">Each SequenceData element contains the information in one row of the [MsiPatchSequence table](msipatchsequence-table.md) of the patch.</span></span> <span data-ttu-id="2d56c-132">O elemento SequenceData contém um subelemento ProductCode, Sequence e Attributes para as informações nos campos correspondentes na tabela MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="2d56c-132">The SequenceData element contains a ProductCode, Sequence, and Attributes subelement for the information in the corresponding fields in the MsiPatchSequence table.</span></span> <span data-ttu-id="2d56c-133">Consulte a seção da [tabela MsiPatchSequence](msipatchsequence-table.md) para obter uma descrição de cada campo.</span><span class="sxs-lookup"><span data-stu-id="2d56c-133">See the [MsiPatchSequence table](msipatchsequence-table.md) section for a description of each field.</span></span>

## <a name="extracting-applicability-information"></a><span data-ttu-id="2d56c-134">Extraindo informações de aplicabilidade</span><span class="sxs-lookup"><span data-stu-id="2d56c-134">Extracting Applicability Information</span></span>

<span data-ttu-id="2d56c-135">O exemplo a seguir mostra como extrair as informações de aplicabilidade para um patch Windows Installer (arquivo. msp) usando [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span><span class="sxs-lookup"><span data-stu-id="2d56c-135">The following example shows you how to extract the applicability information for a Windows Installer Patch (.msp file) using [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span></span> <span data-ttu-id="2d56c-136">O blob XML extraído é baseado na definição de esquema em MSIPatchApplicability. xsd e retornado para szXMLData.</span><span class="sxs-lookup"><span data-stu-id="2d56c-136">The extracted XML blob is based on the schema definition in MSIPatchApplicability.xsd and returned to szXMLData.</span></span>


```C++
#include <windows.h>
#include <msi.h>

#pragma comment( lib, "msi.lib" )

void main()
{
     TCHAR szPatchPath[] = TEXT("c:\\scratch\\RTM-RTMQFE.msp");
    TCHAR* szXMLData = NULL;
    DWORD cchXMLData = 0;

    UINT uiStatus = ERROR_SUCCESS;

    // Determine size of XML blob buffer.
    if (ERROR_SUCCESS == (uiStatus = MsiExtractPatchXMLData(szPatchPath, 
         /*dwReserved: must be 0*/ 0, szXMLData, &cchXMLData)))
    {
        // cchXMLData now includes size of szXMLData in characters not including terminating NULL
        ++cchXMLData;

        szXMLData = new TCHAR[cchXMLData];
        if (ERROR_SUCCESS == (uiStatus = MsiExtractPatchXMLData(szPatchPath, 
            /*dwReserved: must be 0*/ 0, szXMLData, &cchXMLData)))
        {
            //
            // szXMLData now contains the XML patch applicability blob. This could be
            // provided to MsiDetermineApplicablePatches or MsiDeterminePatchSequence in the
            // proper format to evaluate patch applicability.
            //

        }

        delete [] szXMLData;
        szXMLData = NULL;
    }
}
```



<span data-ttu-id="2d56c-137">O exemplo a seguir mostra como extrair as informações de aplicabilidade para um patch Windows Installer (arquivo. msp) no formato XML.</span><span class="sxs-lookup"><span data-stu-id="2d56c-137">The following example shows you how to extract the applicability information for a Windows Installer Patch (.msp file) in XML form.</span></span> <span data-ttu-id="2d56c-138">O blob XML extraído é baseado na definição de esquema em MSIPatchApplicability. xsd e retornado em strPatchXML.</span><span class="sxs-lookup"><span data-stu-id="2d56c-138">The extracted XML blob is based on the schema definition in MSIPatchApplicability.xsd and returned in strPatchXML.</span></span>

``` syntax
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")
strPatchXML = installer.ExtractPatchXMLData("c:\example\patch.msp")
```

## <a name="patch-applicability-schema-definition"></a><span data-ttu-id="2d56c-139">Definição do esquema de aplicabilidade de patch</span><span class="sxs-lookup"><span data-stu-id="2d56c-139">Patch Applicability Schema Definition</span></span>

<span data-ttu-id="2d56c-140">Copie o texto a seguir no bloco de notas ou em outro editor de texto para criar o arquivo de definição de esquema para as informações de aplicabilidade de patch no blob XML.</span><span class="sxs-lookup"><span data-stu-id="2d56c-140">Copy the following text into Notepad or another text editor to create the schema definition file for the patch applicability information in the XML blob.</span></span> <span data-ttu-id="2d56c-141">Nomeie esse arquivo MSIPatchApplicability. XSD.</span><span class="sxs-lookup"><span data-stu-id="2d56c-141">Name this file MSIPatchApplicability.XSD.</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema id="Applicability" 
    targetNamespace="https://www.microsoft.com/msi/patch_applicability.xsd" 
    elementFormDefault="qualified" 
    xmlns="https://www.microsoft.com/msi/patch_applicability.xsd" 
    xmlns:mstns="https://www.microsoft.com/msi/patch_applicability.xsd" 
    xmlns:xs="https://www.w3.org/2001/XMLSchema">
    
    <xs:element name="MsiPatch">
        <xs:complexType>
            <xs:sequence>
                <xs:element name="TargetProduct" minOccurs="1" maxOccurs="unbounded">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element name="TargetProductCode" type="ValidateGUID" />
                            <xs:element name="UpdatedProductCode" type="GUID" minOccurs="0" maxOccurs="1" />
                            <xs:element name="TargetVersion" type="ValidateVersion" />
                            <xs:element name="UpdatedVersion" type="Version" minOccurs="0" maxOccurs="1" />
                            <xs:element name="TargetLanguage" type="ValidateLanguage" />
                            <xs:element name="UpdatedLanguages" type="intList" minOccurs="0" maxOccurs="1" />
                            <xs:element name="UpgradeCode" type="ValidateGUID" />
                            <xs:element name="UpdatedUpgradeCode" type="GUID" minOccurs="0" maxOccurs="1" />
                        </xs:sequence>
                        <xs:attribute name="MinMsiVersion" type="xs:int" />
                    </xs:complexType>
                </xs:element>
                <xs:element name="TargetProductCode" type="GUID" minOccurs="1" maxOccurs="unbounded" />
                <xs:element name="ObsoletedPatch" minOccurs="0" maxOccurs="unbounded" type="GUID" />
                <xs:element name="SequenceData" minOccurs="0" maxOccurs="unbounded">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element name="PatchFamily" type="Identifier" />
                            <xs:element name="ProductCode" type="GUID" minOccurs="0" maxOccurs="1" />
                            <xs:element name="Sequence" type="Version" />
                            <xs:element name="Attributes" type="xs:int" minOccurs="0" maxOccurs="1" />
                        </xs:sequence>
                    </xs:complexType>
                </xs:element>
            </xs:sequence>
            <xs:attribute name="SchemaVersion" type="Version" />
            <xs:attribute name="PatchGUID" type="GUID" />
            <xs:attribute name="MinMsiVersion" type="xs:int" />
            <xs:attribute name="TargetsRTM" type="xs:boolean" use="optional" />
        </xs:complexType>
    </xs:element>
    <xs:simpleType name="GUID">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{12}\}" />
        </xs:restriction>
    </xs:simpleType>
    <xs:simpleType name="Version">
        <xs:restriction base="xs:string">
            <xs:pattern value="[0-9]{1,5}(\.[0-9]{1,5}){0,3}" />
        </xs:restriction>
    </xs:simpleType>
    <xs:complexType name="ValidateGUID">
        <xs:simpleContent>
            <xs:extension base="GUID">
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:complexType name="ValidateVersion">
        <xs:simpleContent>
            <xs:extension base="Version">
                <xs:attribute name="ComparisonType">
                    <xs:simpleType>
                        <xs:restriction base="xs:string">
                            <xs:enumeration value="LessThan" />
                            <xs:enumeration value="LessThanOrEqual" />
                            <xs:enumeration value="Equal" />
                            <xs:enumeration value="GreaterThanOrEqual" />
                            <xs:enumeration value="GreaterThan" />
                            <xs:enumeration value="None" />
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
                <xs:attribute name="ComparisonFilter">
                    <xs:simpleType>
                        <xs:restriction base="xs:string">
                            <xs:enumeration value="Major" />
                            <xs:enumeration value="MajorMinor" />
                            <xs:enumeration value="MajorMinorUpdate" />
                            <xs:enumeration value="None" />
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:complexType name="ValidateLanguage">
        <xs:simpleContent>
            <xs:extension base="xs:int">
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:simpleType name="intList">
        <xs:list itemType="xs:int" />
    </xs:simpleType>
    <xs:simpleType name="Identifier">
        <xs:restriction base="xs:string">
            <xs:pattern value="[_a-zA-Z][_a-zA-Z0-9\.]*" />
        </xs:restriction>
    </xs:simpleType>
</xs:schema>
```

## <a name="related-topics"></a><span data-ttu-id="2d56c-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d56c-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d56c-143">**ExtractPatchXMLData**</span><span class="sxs-lookup"><span data-stu-id="2d56c-143">**ExtractPatchXMLData**</span></span>](installer-extractpatchxmldata.md)
</dt> <dt>

[<span data-ttu-id="2d56c-144">**MsiDeterminePatchSequence**</span><span class="sxs-lookup"><span data-stu-id="2d56c-144">**MsiDeterminePatchSequence**</span></span>](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
</dt> <dt>

[<span data-ttu-id="2d56c-145">**MsiDetermineApplicablePatches**</span><span class="sxs-lookup"><span data-stu-id="2d56c-145">**MsiDetermineApplicablePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
</dt> <dt>

[<span data-ttu-id="2d56c-146">**MsiExtractPatchXMLData**</span><span class="sxs-lookup"><span data-stu-id="2d56c-146">**MsiExtractPatchXMLData**</span></span>](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> </dl>

 

 



