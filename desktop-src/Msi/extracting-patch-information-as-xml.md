---
description: As informações de sequenciamento e aplicabilidade de patch retornadas pela função MsiExtractPatchXMLData ou pelo método ExtractPatchXMLData estão no formato de um blob XML que contém os elementos e atributos identificados neste tópico.
ms.assetid: ea40ed1d-1ef9-44f3-8ae8-3d854e308a49
title: Extraindo informações de patch como XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0574d953609b467c42467853f540dc85c9c24a31c07b3b3d006eaa6633472d53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821676"
---
# <a name="extracting-patch-information-as-xml"></a>Extraindo informações de patch como XML

As informações de sequenciamento e aplicabilidade de patch retornadas pela função [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) ou pelo método [**ExtractPatchXMLData**](installer-extractpatchxmldata.md) estão no formato de um blob XML que contém os elementos e atributos identificados neste tópico. O blob XML pode ser fornecido para [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) e [**MsiDetermineApplicablePatches em**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) vez do arquivo de patch completo.

-   O elemento MsiPatch é o elemento superior do blob XML e contém informações sobre o patch.

    O atributo SchemaVersion especifica a versão da definição de esquema. O esquema é especificado por MSIPatchApplicability.xsd e a versão atual do esquema é 1.0.0.0. O valor do atributo PatchGUID é o código de patch guid para o pacote de patch obtido da propriedade [**Resumo**](revision-number-summary.md) do Número de Revisão no Fluxo de Informações [resumidas](summary-information-stream.md) do patch. O MinMsiVersion é a versão mínima do instalador Windows necessário para instalar o patch obtido da propriedade Resumo de [**Contagem de**](word-count-summary.md) Palavras.

-   O elemento TargetProduct é um elemento de contêiner para obter informações sobre um aplicativo destinado a um patch.

    Pode haver vários elementos TargetProduct se o patch puder ser aplicado a vários aplicativos. As informações no elemento TargetProduct são extraídas de transformares inseridas no patch.

-   O elemento TargetProductCode contém o valor da propriedade [**ProductCode**](productcode.md) do aplicativo de destino antes da aplicação do patch.

    Pode haver vários elementos TargetProductCode se o patch puder ser aplicado a vários aplicativos.

-   O elemento UpdatedProductCode contém o GUID do código do produto do aplicativo de destino depois que o patch é aplicado.

    Esse elemento só estará presente se o patch mudar o valor da [**propriedade ProductCode.**](productcode.md) Um patch que altera **o ProductCode** é conhecido como atualização [principal.](major-upgrades.md)

-   O elemento TargetVersion contém a [**propriedade ProductVersion**](productversion.md) do aplicativo de destino antes da aplicação do patch.
-   O elemento UpdateVersion contém o valor da [**propriedade ProductVersion**](productversion.md) do aplicativo de destino depois que o patch é aplicado.

    Esse elemento só estará presente se o patch mudar o valor da [**propriedade ProductVersion.**](productversion.md) O blob XML para um patch que implementa uma [Pequena](small-updates.md)Atualização , também conhecido como QFE, não incluirá esse elemento. O blob XML para um patch que implementa uma atualização secundária, também conhecida como service pack, incluirá esse elemento.

-   O elemento TargetLanguage contém o valor da propriedade [**ProductLanguage**](productlanguage.md) do aplicativo de destino antes da aplicação do patch.
-   O elemento UpdatedLanguages contém o valor da [**propriedade ProductLanguage**](productlanguage.md) após a aplicação do patch.
-   O elemento UpgradeCode contém o valor da [**propriedade UpgradeCode**](upgradecode.md) do aplicativo de destino.
-   O elemento ObsoletedPatch contém os GUIDs (códigos de patch) dos patches especificados como obsoletos por esse patch.

    A lista de patches obsoletos é obtida do Resumo do Número [**de Revisão**](revision-number-summary.md) no Fluxo de [Informações resumidas](summary-information-stream.md) do patch.

-   O elemento SequenceData contém informações de sequenciamento de patch para o patch.

    Pode haver vários elementos SequenceData no blob XML. Cada elemento SequenceData contém as informações em uma linha da [tabela MsiPatchSequence](msipatchsequence-table.md) do patch. O elemento SequenceData contém um subelemento ProductCode, Sequence e Attributes para as informações nos campos correspondentes na tabela MsiPatchSequence. Consulte a [seção tabela MsiPatchSequence](msipatchsequence-table.md) para ver uma descrição de cada campo.

## <a name="extracting-applicability-information"></a>Extraindo informações de aplicabilidade

O exemplo a seguir mostra como extrair as informações de aplicabilidade de um patch do instalador do Windows (arquivo .msp) usando [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa). O blob XML extraído é baseado na definição de esquema em MSIPatchApplicability.xsd e retornado para szXMLData.


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



O exemplo a seguir mostra como extrair as informações de aplicabilidade de um patch do instalador Windows (arquivo .msp) em formato XML. O blob XML extraído é baseado na definição de esquema em MSIPatchApplicability.xsd e retornado em strPatchXML.

``` syntax
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")
strPatchXML = installer.ExtractPatchXMLData("c:\example\patch.msp")
```

## <a name="patch-applicability-schema-definition"></a>Definição de esquema de aplicabilidade de patch

Copie o texto a seguir Bloco de notas ou outro editor de texto para criar o arquivo de definição de esquema para as informações de aplicabilidade do patch no blob XML. Nomeia esse arquivo MSIPatchApplicability.XSD.

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

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ExtractPatchXMLData**](installer-extractpatchxmldata.md)
</dt> <dt>

[**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
</dt> <dt>

[**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
</dt> <dt>

[**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> </dl>

 

 



