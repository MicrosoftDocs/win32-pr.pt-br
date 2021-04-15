---
title: Esquema e algoritmo de perfil do modelo de dispositivo de cores do WCS
description: Este tópico fornece informações sobre o esquema de perfil de modelo de dispositivo de cores WCS e seus algoritmos associados. Este tópico contém as seções a seguir OverviewColor perfil de modelo de dispositivo ArchitectureThe CDMP SchemaWCS CDMP v 2.0 Calibration AdditionThe CDMP Schema ElementsColorDeviceModelProfileColorDeviceModelNamespaceVersionVersionDocumentationCRTDevice elementLCDDevice elementProjectorDevice elementScannerDevice elementCameraDevice elementRGBPrinterDevice elementCMYKPrinterDevice elementRGBVirtualDevice elementPlugInDeviceTypeRGBVirtualMeasurementTypeGammaTypeGammaOffsetGainTypeGammaOffsetGainLinearGainTypeToneResponseCurvesTypeGamutBoundarySamplesTypeFloatPairListCMYKPrinterMeasurementTypeRGBPrinterMeasurementTypeRGBCaptureMeasurementTypeOneBasedIndexRGBProjectorMeasurementTypeDisplayMeasurementTy peMeasurementConditionsTypeGeometryTypeRGBPrimariesGroupNonNegativeCMYKSampleTypeNonNegativeRGBSampleTypeNonNegativeCMYKTypeNonNegativeRGBTypeExtensionTypeNonNegativeXYZTypeXYZTypeThe CDMP linha de base AlgorithmsCRT modelo de dispositivo BaselineLCD modelo de dispositivo BaselineRGB impressora modelo de dispositivo virtual BaselineRGB modelo de dispositivos virtuais BaselineCMYK impressora modelo de dispositivo BaselineRGB projeto modelo de dispositivo BaselineICC modelo de dispositivo BaselineRelated tópicos
ms.assetid: bbb3b50d-75fc-476d-a011-af7dcc2ac520
keywords:
- WCS (sistema de cores do Windows), CDMP (perfil de modelo de dispositivo de cores)
- WCS (sistema de cores do Windows), perfil de modelo de dispositivo de cores (CDMP)
- gerenciamento de cores de imagem, perfil de modelo de dispositivo de cores (CDMP)
- gerenciamento de cores, perfil de modelo de dispositivo de cores (CDMP)
- cores, perfil de modelo de dispositivo de cores (CDMP)
- WCS (sistema de cores do Windows), perfis
- WCS (sistema de cores do Windows), perfis
- gerenciamento de cores de imagem, perfis
- gerenciamento de cores, perfis
- cores, perfis
- esquemas, perfil de modelo de dispositivo de cores (CDMP)
- algoritmos, perfil de modelo de dispositivo de cores (CDMP)
- Perfil de modelo de dispositivo de cores (CDMP)
- CDMP (perfil de modelo de dispositivo de cores)
- Perfil do modelo de dispositivo de cores WCS
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b671bf97625b00c99060e65be4d39c44e5b35f
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104554622"
---
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a>Esquema e algoritmo de perfil do modelo de dispositivo de cores do WCS

Este tópico fornece informações sobre o esquema de perfil de modelo de dispositivo de cores WCS e seus algoritmos associados.

Este tópico contém as seguintes seções:

-   [Visão geral](#overview)
-   [Arquitetura do perfil de modelo do dispositivo de cores](#color-device-model-profile-architecture)
-   [O esquema CDMP](#the-cdmp-schema)
-   [Adição de calibração do WCS CDMP v 2.0](#wcs-cdmp-v20-calibration-addition)
-   [Os elementos do esquema CDMP](#the-cdmp-schema-elements)
    -   [ColorDeviceModelProfile](#colordevicemodelprofile)
    -   [ColorDeviceModel](#colordevicemodelprofile)
    -   [NamespaceVersion](#namespaceversion)
    -   [Versão](#namespaceversion)
    -   [Documentação](#documentation)
    -   [Elemento CRTDevice](#crtdevice-element)
    -   [Elemento LCDDevice](#lcddevice-element)
    -   [Elemento ProjectorDevice](#projectordevice-element)
    -   [Elemento ScannerDevice](#scannerdevice-element)
    -   [Elemento CameraDevice](#cameradevice-element)
    -   [Elemento RGBPrinterDevice](#rgbprinterdevice-element)
    -   [Elemento CMYKPrinterDevice](#cmykprinterdevice-element)
    -   [Elemento RGBVirtualDevice](#rgbvirtualdevice-element)
    -   [PlugInDeviceType](#plugindevicetype)
    -   [RGBVirtualMeasurementType](#rgbvirtualmeasurementtype)
    -   [Gamatype](#gammatype)
    -   [GammaOffsetGainType](#gammaoffsetgaintype)
    -   [GammaOffsetGainLinearGainType](#gammaoffsetgainlineargaintype)
    -   [ToneResponseCurvesType](#toneresponsecurvestype)
    -   [GamutBoundarySamplesType](#gamutboundarysamplestype)
    -   [FloatPairList](#floatpairlist)
    -   [CMYKPrinterMeasurementType](#cmykprintermeasurementtype)
    -   [RGBPrinterMeasurementType](#rgbprintermeasurementtype)
    -   [RGBCaptureMeasurementType](#rgbcapturemeasurementtype)
    -   [OneBasedIndex](#onebasedindex)
    -   [RGBProjectorMeasurementType](#rgbprojectormeasurementtype)
    -   [DisplayMeasurementType](#displaymeasurementtype)
    -   [MeasurementConditionsType](#measurementconditionstype)
    -   [GeometryType](#geometrytype)
    -   [RGBPrimariesGroup](#rgbprimariesgroup)
    -   [NonNegativeCMYKSampleType](#nonnegativecmyksampletype)
    -   [NonNegativeRGBSampleType](#nonnegativergbsampletype)
    -   [NonNegativeCMYKType](#nonnegativecmyktype)
    -   [NonNegativeRGBType](#nonnegativergbtype)
    -   [ExtensionType](#extensiontype)
    -   [NonNegativeXYZType](#nonnegativexyztype)
    -   [XYZType](#nonnegativexyztype)
-   [Os algoritmos de linha de base CDMP](#the-cdmp-baseline-algorithms)
    -   [Linha de base de modelo de dispositivo CRT](#crt-device-model-baseline)
    -   [Linha de base do modelo de dispositivo LCD](#lcd-device-model-baseline)
    -   [Linha de base de modelo de dispositivo de impressora RGB](#rgb-printer-device-model-baseline)
    -   [Linha de base de modelo de dispositivo virtual RGB](#rgb-virtual-device-model-baseline)
    -   [Linha de base de modelo de dispositivo de impressora CMYK](#cmyk-printer-device-model-baseline)
    -   [Linha de base do modelo de dispositivo do projetor RGB](#rgb-projector-device-model-baseline)
    -   [Linha de base do modelo de dispositivo ICC](#icc-device-model-baseline)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Esse esquema é usado para especificar o conteúdo de um perfil de modelo de dispositivo de cor (CDMP). Os algoritmos de linha de base associados são descritos abaixo.

O esquema básico do DMP (perfil de modelo de dispositivo) consiste nos dados de medição de amostragem.

O componente de amostragem do esquema XML do DMP fornece suporte para destinos de medição de cores básicas, concentrando-se em destinos padrão comuns e destinos otimizados para os modelos de dispositivo de linha de base.

Além disso, o perfil do dispositivo fornece informações específicas sobre o modelo de dispositivo de destino e fornece uma política que o modelo de dispositivo de fallback de linha de base pode usar se o modelo de destino não estiver disponível. As instâncias de perfil podem incluir extensões privadas usando mecanismos de extensão XML padrão.

## <a name="color-device-model-profile-architecture"></a>Arquitetura do perfil de modelo do dispositivo de cores

![Diagrama que mostra as informações que compõem um perfil de modelo de dispositivo.](images/cdmp-image002new.png)

## <a name="the-cdmp-schema"></a>O esquema CDMP


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema 
  xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Device Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:complexType name="RGBType">
    <xs:attribute name="R" type="xs:float" use="required"/>
    <xs:attribute name="G" type="xs:float" use="required"/>
    <xs:attribute name="B" type="xs:float" use="required"/>
  </xs:complexType>

  <xs:complexType name="NonNegativeRGBType">
    <xs:attribute name="R" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="G" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="B" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:complexType name="NonNegativeCMYKType">
    <xs:attribute name="C" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="M" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Y" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="K" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:complexType name="NonNegativeRGBSampleType">
    <xs:sequence>
      <xs:element name="RGB" type="cdm:NonNegativeRGBType"/>
      <xs:element name="CIEXYZ" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
    <xs:attribute name="Tag" type="xs:string" use="optional"/>
  </xs:complexType>
  
  <xs:complexType name="NonNegativeCMYKSampleType">
    <xs:sequence>
      <xs:element name="CMYK" type="cdm:NonNegativeCMYKType"/>
      <xs:element name="CIEXYZ" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
    <xs:attribute name="Tag" type="xs:string" use="optional"/>
  </xs:complexType>
  
  <xs:group name="RGBPrimariesGroup">
    <xs:sequence>
      <xs:element name="WhitePrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="RedPrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="GreenPrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="BluePrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="BlackPrimary" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
  </xs:group> 
  
  <xs:complexType name="MeasurementConditionsType">
    <xs:annotation>
      <xs:documentation>
      Optional measurement conditions. 
       
      We only support CIEXYZ for measurement color space in this version. 
      If the white point value from the measurement conditions is not available, 
      the default processing will use
        - "D50" for printer and scanners
        - "D65" for camera and displays.          
      </xs:documentation>
    </xs:annotation>
    <xs:sequence>
      <xs:element name="ColorSpace" minOccurs="0">
        <xs:simpleType>
          <xs:restriction base="xs:string">
            <xs:enumeration value="CIEXYZ"/>
          </xs:restriction>
        </xs:simpleType>    
      </xs:element>
      <xs:choice minOccurs="0">
        <xs:element name="WhitePoint" type="wcs:NonNegativeCIEXYZType"/>
        <xs:element name="WhitePointName">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="D50"/>
              <xs:enumeration value="D65"/>
              <xs:enumeration value="A"/>
              <xs:enumeration value="F2"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
      </xs:choice>
      <xs:element name="Geometry" minOccurs="0">
        <xs:simpleType>
          <xs:restriction base="xs:string">
            <xs:enumeration value="0/45"/>
            <xs:enumeration value="0/diffuse"/>
            <xs:enumeration value="diffuse/0"/>
            <xs:enumeration value="direct"/>
          </xs:restriction>
        </xs:simpleType>   
      </xs:element>
      <xs:element name="ApertureSize" type="xs:int" minOccurs="0"/>
    </xs:sequence>
  </xs:complexType>
  
  <xs:complexType name="DisplayMeasurementType">
    <xs:sequence>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:element name="GrayRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="RedRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="GreenRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="BlueRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="RGBProjectorMeasurementType">
    <xs:sequence>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:element name="ColorSamples">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:simpleType name="OneBasedIndex">
    <xs:restriction base="xs:int">
      <xs:minInclusive value="1"/>
    </xs:restriction>
  </xs:simpleType>
    
  <xs:complexType name="RGBCaptureMeasurementType">
    <xs:sequence>
      <xs:element name="PrimaryIndex">
        <xs:complexType>
          <xs:all>
            <xs:element name="White" type="cdm:OneBasedIndex"/>
            <xs:element name="Black" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Red" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Green" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Blue" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Cyan" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Magenta" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Yellow" type="cdm:OneBasedIndex" minOccurs="0"/>
          </xs:all>
        </xs:complexType>
      </xs:element>
      <xs:element name="NeutralIndices">
        <xs:simpleType>
          <xs:list itemType="cdm:OneBasedIndex"/>
        </xs:simpleType>
      </xs:element>
      <xs:element name="ColorSamples">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="RGBPrinterMeasurementType">
    <xs:sequence>
      <xs:element name="ColorCube">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>       
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>
  
  <xs:complexType name="CMYKPrinterMeasurementType">
    <xs:sequence>
      <xs:element name="ColorCube">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeCMYKSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>       
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="GammaType">
    <xs:attribute name="value" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:complexType name="GammaOffsetGainType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:complexType name="GammaOffsetGainLinearGainType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="LinearGain" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="TransitionPoint" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:simpleType name="FloatList">
    <xs:list itemType="xs:float"/>
  </xs:simpleType>

  <xs:complexType name="OneDimensionLutType">
    <xs:sequence>
      <xs:element name="Input" type="cdm:FloatList"/>
      <xs:element name="Output" type="cdm:FloatList"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="HDRToneResponseCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="cdm:OneDimensionLutType"/>
      <xs:element name="GreenTRC" type="cdm:OneDimensionLutType"/>
      <xs:element name="BlueTRC" type="cdm:OneDimensionLutType"/>
    </xs:sequence>
    <xs:attribute name="TRCLength" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:int">
          <xs:minInclusive value="0" />
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
  
  <xs:complexType name="GamutBoundarySamplesType">
    <xs:sequence>
      <xs:element name="RGB" type="cdm:RGBType" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>
  
  <xs:complexType name="RGBVirtualMeasurementType">
    <xs:sequence>
      <xs:element name="MaxColorantUsed" type="xs:float"/>
      <xs:element name="MinColorantUsed" type="xs:float"/>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:choice>
        <xs:element name="Gamma" type="cdm:GammaType"/>
        <xs:element name="GammaOffsetGain" type="cdm:GammaOffsetGainType"/>
        <xs:element name="GammaOffsetGainLinearGain" type="cdm:GammaOffsetGainLinearGainType"/>
        <xs:element name="HDRToneResponseCurves" type="cdm:HDRToneResponseCurvesType"/>
      </xs:choice>
      <xs:element name="GamutBoundarySamples" type="cdm:GamutBoundarySamplesType" minOccurs="0"/>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>
  
  <xs:element name="ColorDeviceModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="MeasurementConditions" type="cdm:MeasurementConditionsType" minOccurs="0"/>
        <xs:element name="SelfLuminous" type="xs:boolean" />
        <xs:element name="MaxColorant" type="xs:float"/>
        <xs:element name="MinColorant" type="xs:float"/>
        <xs:choice>
          <xs:element name="CRTDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:DisplayMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="LCDDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:DisplayMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBProjectorDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBProjectorMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="ScannerDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBCaptureMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="CameraDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBCaptureMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBPrinterDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBPrinterMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="CMYKPrinterDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:CMYKPrinterMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBVirtualDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBVirtualMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
        </xs:choice>
        <xs:element name="PlugInDevice" minOccurs="0">
          <xs:complexType>
            <xs:sequence>
              <xs:any namespace="##other" processContents="skip"
                minOccurs="0" maxOccurs="unbounded" />
            </xs:sequence>
            <xs:attribute name="GUID" type="wcs:GUIDType" use="required"/>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>

```



## <a name="wcs-cdmp-v20-calibration-addition"></a>Adição de calibração do WCS CDMP v 2.0

O elemento **ColorDeviceModel** do esquema CDMP foi atualizado no Windows 7 para incluir o novo elemento Calibration. O seguinte mostra a alteração no esquema CDMP.


```C++
  ...
  <xs:element name="ColorDeviceModel">
    <xs:complexType>
      <xs:sequence>
        ...
        <xs:element name="PlugInDevice" minOccurs="0">
             ...
        </xs:element>
        <xs:element name="Calibration" type="cal:Calibration" minOccurs="0"/>
        ...
      <xs:sequence>
    ...
    <xs:complexType>
  ...
```



## <a name="the-cdmp-schema-elements"></a>Os elementos do esquema CDMP

> [!Note]  
> Primárias são exemplos principais de vermelho, verde, azul, preto e branco. Uma rampa primária é uma rampa de tons de menos luminescência até o valor primário completo. O número máximo de entradas em uma rampa de Tom é 4096.

 

> [!Note]  
> DMPs são necessários para ter dados de medida.

 

### <a name="colordevicemodelprofile"></a>ColorDeviceModelProfile

Esse elemento é do tipo ColorDeviceModel.

**Condições de validação:** Cada subelemento é validado por seu próprio tipo.

### <a name="colordevicemodel"></a>ColorDeviceModel

Este elemento é uma sequência dos seguintes subelementos

1.  Cadeia de caracteres ProfileName,
2.  Cadeia de caracteres de descrição opcional,
3.  Cadeia de caracteres de autor opcional,
4.  MeasurementConditions MeasurementConditionsType opcional,
5.  Self-Luminous booliano,
6.  MaxColorant float,
7.  MinColorant float,
8.  Opção de elementos
    1.  CRTDevice,
    2.  LCDDevice,
    3.  RGBProjectorDevice,
    4.  ScannerDevice,
    5.  CameraDevice,
    6.  RGBPrinterDevice,
    7.  CMYKPrinterDevice,
    8.  RGBVirtualDevice,
9.  PlugInDevice,
10. Extensão opcional ExtensionType

**Condições de validação:** Cada subelemento é validado por seu próprio tipo. Os subelementos de cadeia de caracteres têm um máximo de 10.000 caracteres. O subelemento MaxColorant deve ser maior ou igual a zero (0) e maior que o subelemento MinColorant. O MinColorant pode ser negativo.

### <a name="namespaceversion"></a>NamespaceVersion

xmlns: CDM = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

### <a name="version"></a>Versão

Versão = "1,0" com o Windows Vista.

**Condições de validação:** Qualquer valor &gt; de versão 0,1 ou &lt; = 2,0 é válido para dar suporte a alterações não significativas no formato.

### <a name="documentation"></a>Documentação

Esquema de perfil de modelo de dispositivo.

Copyright (C) Microsoft. Todos os direitos reservados.

### <a name="crtdevice-element"></a>Elemento CRTDevice

Esse elemento é uma sequência de subelementos de um MeasurementData DisplayMeasurementType.

**Condições de validação:** Cada subelemento é validado por seu próprio tipo.

### <a name="lcddevice-element"></a>Elemento LCDDevice

Esse elemento é uma sequência de subelementos de um MeasurementData DisplayMeasurementType.

**Condições de validação:** Cada subelemento é validado por seu próprio tipo.

### <a name="projectordevice-element"></a>Elemento ProjectorDevice

Esse elemento é uma sequência de subelementos de um MeasurementData RGBProjectorMeasurementType.

**Condições de validação:** Cada subelemento é validado por seu próprio tipo.

### <a name="scannerdevice-element"></a>Elemento ScannerDevice

Esse elemento é uma sequência de subelementos de um MeasurementData RGBCaptureMeasurementType

**Condições de validação:** Cada subelemento é validado por seu próprio tipo.

### <a name="cameradevice-element"></a>Elemento CameraDevice

Esse elemento é uma sequência de subelementos de um MeasurementData RGBCaptureMeasurementType

**Condições de validação:** Cada subelemento é validado por seu próprio tipo.

### <a name="rgbprinterdevice-element"></a>Elemento RGBPrinterDevice

Esse elemento é uma sequência de subelementos de um MeasurementData RGBPrinterMeasurementType.

**Condições de validação:** Cada subelemento é validado por seu próprio tipo.

### <a name="cmykprinterdevice-element"></a>Elemento CMYKPrinterDevice

Esse elemento é uma sequência de subelementos de um MeasurementData CMYKPrinterMeasurementType.

**Condições de validação:** Cada subelemento é validado por seu próprio tipo.

### <a name="rgbvirtualdevice-element"></a>Elemento RGBVirtualDevice

Esse elemento é uma sequência de subelementos de um RGBVirtualMeasurementDataType.

**Condições de validação:** Cada subelemento é validado por seu próprio tipo.

### <a name="plugindevicetype"></a>PlugInDeviceType

Esse elemento é uma sequência de um GUIDtype GUID e quaisquer subelementos.

**Condições de validação:** O GUID é usado para corresponder ao GUID da dll do plug-in DM. Há um máximo de 100.000 subelementos personalizados.

### <a name="rgbvirtualmeasurementtype"></a>RGBVirtualMeasurementType

Esse elemento é uma sequência que consiste em

1.  Grupo de RGBPrimariesGroup
2.  Uma opção de
3.  -   Gama
    -   GammaOffsetGain
    -   GammaOffsetGainLinearGam
    -   Elementos ToneResponseCurves

4.  GamutBoundarySamples GamutBoundarySamplesType opcional
5.  Carimbo de data/hora

**Condições de validação:** Cada subelemento desses tipos tem suas próprias condições de validação.

### <a name="gammatype"></a>Gamatype

Este elemento é um tipo complexo que consiste no atributo

-   NonNegativeFloatType gama

**Condições de validação:** Para ser determinado dos comentários do setor.

### <a name="gammaoffsetgaintype"></a>GammaOffsetGainType

Este elemento é um tipo complexo que consiste nos atributos

-   NonNegativeFloatType gama
-   NonNegativeFloatType de deslocamento
-   Obter NonNegativeFloatType

**Condições de validação:** Para ser determinado dos comentários do setor.

### <a name="gammaoffsetgainlineargaintype"></a>GammaOffsetGainLinearGainType

Este elemento é um tipo complexo que consiste nos atributos

-   NonNegativeFloatType gama
-   NonNegativeFloatType de deslocamento
-   Obter NonNegativeFloatType
-   LinearGain NonNegativeFloatType
-   TransitionPoint NonNegativeFloatType.

**Condições de validação:** Para ser determinado dos comentários do setor.

### <a name="toneresponsecurvestype"></a>ToneResponseCurvesType

Este elemento é uma sequência de

1.  RedTRC FloatPairList
2.  GreenTRC FloatPairList
3.  BlueTRC FloatPairList

O elemento também tem um atributo TRCLength do tipo unsignedInt.

**Condições de validação:** Para ser determinado dos comentários do setor.

### <a name="gamutboundarysamplestype"></a>GamutBoundarySamplesType

Esse elemento é uma sequência de RGBTypes RGB.

**Condições de validação:** Ocorrências máximas não associadas no momento, a serem limitadas com base nos comentários do setor.

### <a name="floatpairlist"></a>FloatPairList

Esse elemento é um tipo simples de lista de pares de floats.

**Condições de validação:** Para ser determinado dos comentários do setor.

### <a name="cmykprintermeasurementtype"></a>CMYKPrinterMeasurementType

Este elemento é um

1. sequência do elemento ColorCube que consiste em uma sequência de NonNegativeCMYKSampleType de amostra

2. Atributo dateTime TimeStamp.

**Condições de validação:** Para ser determinado dos comentários do setor.

### <a name="rgbprintermeasurementtype"></a>RGBPrinterMeasurementType

Este elemento é um

1. sequência do elemento ColorCube que consiste em uma sequência de NonNegativeRGBSampleType de amostra

2. Atributo dateTime TimeStamp.

**Condições de validação:** Para ser determinado dos comentários do setor.

### <a name="rgbcapturemeasurementtype"></a>RGBCaptureMeasurementType

Este elemento é uma sequência de

1.  ComplexType PrimaryIndex de
2.  1.  OneBasedIndex branco
    2.  OneBasedIndex preto opcional
    3.  OneBasedIndex vermelho opcional
    4.  OneBasedIndex verde opcional
    5.  OneBasedIndex azul opcional
    6.  OneBasedIndex ciano opcional
    7.  OneBasedIndex magenta opcional
    8.  OneBasedIndex amarelo opcional

3.  NeutralIndices de linhas de OneBasedIndex
4.  ColorSamples sequência de NonNegativeRGBSampleType de amostra

O elemento também tem um atributo dateTime TimeStamp.

**Condições de validação:** Para ser determinado dos comentários do setor.

### <a name="onebasedindex"></a>OneBasedIndex

Esse elemento é um tipo simples de restrição base sem sinal int com valor minInclusive = "1".

**Condições de validação:** Para ser determinado dos comentários do setor.

### <a name="rgbprojectormeasurementtype"></a>RGBProjectorMeasurementType

Este elemento é uma sequência de

1.  Grupo de RGBPrimariesGroup
2.  elemento ColorSamples que consiste em sequência de NonNegativeRGBSampleType de amostra

O elemento também tem um atributo dateTime TimeStamp.

**Condições de validação:** Para ser determinado dos comentários do setor.

### <a name="displaymeasurementtype"></a>DisplayMeasurementType

Este elemento é uma sequência de

1.  RGBPrimariesGroup de grupo
2.  GrayRamp da sequência de NonNegativeRGBType de amostra
3.  RedRamp da sequência de NonNegativeRGBType de amostra
4.  GreenRamp da sequência de NonNegativeRGBType de amostra
5.  BlueRamp da sequência de NonNegativeRGBType de amostra

O elemento DisplayMeasurementType também tem um atributo dateTime TimeStamp.

**Condições de validação:** Para ser determinado dos comentários do setor.

### <a name="measurementconditionstype"></a>MeasurementConditionsType

O MeasurementConditionsType é uma sequência de subelementos que contém:

1.  Valor de enumeração de cadeia de caracteres restrita ColorSpace de "CIEXYZ"
2.  opção opcional de enumeração de cadeia de caracteres WhitePoint NonNegativeXYZType ou WhitePointName de valores D50, D65, A ou F2
3.  GeometryType Geometry
4.  ApertureSize inteiro em milímetros

Os padrões são:

1.  Impressoras RGB e CMYK:
    1.  CIEXYZ MeasurementSpaceType
    2.  D50 WhitePointValue
    3.  GeometryType 0/45
    4.  10mm ApertureSize
2.  Scanners
    1.  CIEXYZ MeasurementSpaceType
    2.  D50 WhitePointValue
    3.  GeometryType 0/45
    4.  10mm ApertureSize
3.  Exibe e o dispositivo virtual RGB:
    1.  CIEXYZ MeasurementSpaceType
    2.  D65 WhitePointValue
    3.  GeometryType 0/45
    4.  10mm ApertureSize
4.  Câmaras
    1.  CIEXYZ MeasurementSpaceType
    2.  D65 WhitePointValue
    3.  GeometryType direto
    4.  10mm ApertureSize

**Condições de validação:** A validação de cada sub-elemento é determinada pelas condições de validação para esses subelementos. Se algum subelemento estiver ausente, o padrão específico do tipo de modelo do dispositivo será usado.

### <a name="geometrytype"></a>GeometryType

String

Valores de enumeração:

-   "0/45"
-   "0/difuso"
-   "difuso/0"
-   Encaminhe

**Condições de validação:** Qualquer valor, exceto os valores de enumberation listados, é inválido. Essas informações não alterarão o comportamento de processamento de linha de base.

### <a name="rgbprimariesgroup"></a>RGBPrimariesGroup

Este elemento é uma sequência de

1.  WhitePrimary NonNegativeXYZType
2.  RedPrimary NonNegativeXYZType
3.  GreenPrimary NonNegativeXYZType
4.  BluePrimary NonNegativeXYZTYpe
5.  BlackPrimary NonNegativeXYZType

**Condições de validação:** Para ser determinado dos comentários do setor.

### <a name="nonnegativecmyksampletype"></a>NonNegativeCMYKSampleType

Este elemento é uma sequência de

1.  NonNegativeCMYKType CMYK
2.  CIEXYZ NonNegativeXYZType

O elemento também tem uma cadeia de caracteres de marca de atributo opcional

**Condições de validação:** Para ser determinado dos comentários do setor.

### <a name="nonnegativergbsampletype"></a>NonNegativeRGBSampleType

Este elemento é uma sequência de

1.  NonNegativeRGBType RGB
2.  CIEXYZ NonNegativeXYZType

O elemento também tem uma cadeia de caracteres de marca de atributo opcional

**Condições de validação:** Para ser determinado dos comentários do setor.

### <a name="nonnegativecmyktype"></a>NonNegativeCMYKType

Este elemento consiste em atributos

1.  C float
2.  M float
3.  Float de Y
4.  K float

**Condições de validação:** Para ser determinado dos comentários do setor.

### <a name="nonnegativergbtype"></a>NonNegativeRGBType

Este elemento consiste em atributos

1.  Float de R
2.  G float
3.  B float

**Condições de validação:** Para ser determinado dos comentários do setor.

### <a name="extensiontype"></a>ExtensionType

O elemento ExtensionType é uma sequência de qualquer tipo de subelemento e é usado para informações proprietárias de aplicativos que não são da Microsoft.

**Condições de validação:** Esse elemento é opcional. Pode haver um máximo de 1000 subelementos de extensão.

### <a name="nonnegativexyztype"></a>NonNegativeXYZType

O elemento NonNegativeXYZType é composto por NonNegativeFloatType três elementos de ponto flutuante de IEEE de precisão simples chamados "X", "Y" e "Z". Esses valores são limitados aos valores de medição de perfis do DMP. Essas medidas podem ser absolutas (não relativas) CIEXYZ 1931 valores de reflexão ou valores absolutos (não relativos) CIEXYZ 1931 diretos (transmissal) em candelas por unidades de metro quadrado.

**Condições de validação:** Somente valores do mundo real são válidos e valores de medição CIEXYZ negativos são inválidos. Como esses são valores absolutos, os valores podem ser maiores que 1,0 f. Um limite razoável para qualquer "X", "Y" ou "Z". o valor é definido arbitrariamente como 10000.0 f.

### <a name="xyztype"></a>XYZType

O elemento XYZType é composto por três valores de ponto flutuante IEEE de precisão simples: "X", "Y" e "Z".

## <a name="the-cdmp-baseline-algorithms"></a>Os algoritmos de linha de base CDMP

### <a name="crt-device-model-baseline"></a>Linha de base de modelo de dispositivo CRT

Para entender esse modelo, você deve considerar o processo de caracterização e a modelagem do dispositivo. No processo de caracterização, as medidas da XYZ são executadas primeiro nas cores obtidas preenchendo o buffer de exibição de um dispositivo de vídeo CRT. Os seguintes valores de exemplo irão gerar bons dados para o modelo de dispositivo CRT de linha de base:

Vermelho: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Verde: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Azul: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutrals: R = G = B = 0, 8, 16, 32, 64, 128, 192, 255

Incrementos diferentes de 15 e incrementos não lineares também podem ser usados. Cada rampa vermelha, verde, azul e neutro deve conter pelo menos três exemplos, mas é recomendável fornecer mais amostras. Você deve fornecer exemplos para vermelho puro, verde, azul, preto e branco. Os exemplos não precisam ser espaçados uniformemente.

O processo de criação da matriz triestímulo consiste em duas etapas. Em primeiro lugar, estimar o valor do ponto preto ou o FLARE. Esta etapa baseia-se amplamente no trabalho de Berns \[ 3 \] com uma função de objetivo ligeiramente modificada para a otimização não linear. Em segundo lugar, calcule a matriz de triestímulo com base no resultado da etapa um e também de um cálculo de média em todas as medições por canal, não apenas a única para a contagem digital máxima.

Cada uma dessas etapas contém procedimentos detalhados. O ponto de partida é a rampa (17 etapas em nosso exemplo) para cada um dos canais R, G e B. Quando as medidas XYZ são plotadas no plano *XY* de desvio, uma situação típica é mostrada na Figura 1. A etapa 1 consiste em resolver um problema de otimização não linear para encontrar o ponto preto "melhor ajuste", que minimizará a descompasso em desvio, uma vez que atravessa os canais R, G e B. Com base no Berns \[ 3 \] , buscamos ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>k</sub>* ) que minimiza a seguinte função objetiva:

![Mostra a função de objetivo em que Sr, SG e SB são o conjunto de pontos de dados nos canais R, G e B.](images/cdmp-formula1.png)

em que *s <sub>R</sub>*,*s <sub>G</sub>* e *s <sub>B</sub>* são o conjunto de pontos de dados correspondente aos pontos nos canais R, G e B. Para qualquer conjunto de *S*, defina:

![Mostra uma fórmula para definir quaisquer S de conjunto.](images/cdmp-formula2.png)

No anterior, \| *s* \| é a cardinalidade de *S*, ou seja, o número de pontos no *S* do conjunto. ![ Mostra uma fórmula para a desvio de um ponto.](images/cdmp-formula3.png) é as coordenadas de desvio do ponto ![ mostra um formaula para um ponto.](images/cdmp-formula4.png) , portanto, ![ mostra uma fórmula para a média ou o centro de massa. ](images/cdmp-formula5.png) é a média ou o centro de massa de todos os pontos do conjunto de *S* no plano de desvio. Assim, ![ mostra uma fórmula para a soma de um segundo ponto de pontos.](images/cdmp-formula6.png) é a soma do segundo instante dos pontos sobre o centro de massa e é uma medida de como distribuir os pontos. Por fim, ![ mostra uma fórmula para a medida total da difusão de três clusters de pontos.](images/cdmp-formula7.png) é uma medida total de como distribuir os três clusters de pontos são sobre seus respectivos centros de massa.

No cálculo de ![ mostra uma fórmula de f (X, Y, Z; XK, YK, ZK).](images/cdmp-formula8.png) , se ![ mostrar uma fórmula para X. ](images/cdmp-formula9.png) , o cálculo será ignorado e a cardinalidade de *S* será ajustada de acordo.

Apesar da complexidade aparente da função objetiva, é uma soma dos quadrados de muitas funções diferenciávels em *X <sub>K</sub>*,*Y <sub>k</sub>Z <sub>k</sub>* (17 pontos 2 *XY* -Components 3 Channels = 102, no exemplo) e, portanto, é receptivos a técnicas de quadrados mínimos não lineares padrão, como o algoritmo Levenberg-Marquardt, que é o algoritmo usado no WCS. Observe que a função de objetivo anterior é diferente da sugerida no Berns \[ 3 \] , já que a última função mede a variância das distâncias do centro de massa, de forma que a variação seja zero quando os pontos forem equidistante do centro de massa, mesmo que possam se espalhar um pouco. No exemplo, a dispersão de pontos é contratada diretamente usando o segundo instante.

Como com qualquer algoritmo iterativo para o problema de quadrados não lineares, Levenberg-Marquardt requer uma estimativa inicial. Há dois candidatos óbvios. Um é (0, 0, 0); o outro é o ponto preto medido. Para a CTE, o ponto preto medido é usado primeiro como a estimativa inicial. Se um máximo de 100 iterações for excedido sem alcançar um limite de uma distância média de 0, 1 de cada ponto de seu centro de massa (que corresponde a um valor limite de (0, 1) 17 3 = 0, 51 para a função objetiva), então, outra rodada de iterações com a estimativa inicial de (0, 0, 0) é executada. A estimativa resultante do ponto preto é XYZ comparada com a melhor estimativa da rodada anterior de iterações (com o ponto preto medido como a estimativa inicial). Use a estimativa que fornece o menor valor para a função Objective. A escolha de 100 iterações e a distância de erro de 0, 1 foram cada uma das empiricamente selecionadas. Em versões futuras, pode ser razoável parametrizar a distância do erro.

O resultado da etapa 1 é o ponto preto estimado ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>k</sub>* ). A etapa dois consiste em determinar a matriz de triestímulo calculando a média da desvio dos pontos nos três clusters obtidos na etapa um. Para CRTs, isso é feito principalmente para minimizar os efeitos dos erros de medida. Os pontos usados na média da desvio devem ser os mesmos pontos usados na otimização na etapa um. Em outras palavras, se o primeiro ponto (contagem digital 15, no exemplo) em cada rampa for descartado na etapa de otimização, o mesmo deverá ser feito na média. Se o ![ Mostrar fórmulas de desvio médio de coordenadas nos canais vermelho e verde.](images/cdmp-formula10.png) e ![ mostra uma fórmula de desvio médio de coordenadas no canal azul.](images/cdmp-formula11.png) são as coordenadas de desvios médias dos canais vermelho, verde e azul e, em seguida, o procedimento a seguir determina a matriz triestímulo. Primeiro, resolva o sistema de 3? 3 lineares:

![Mostra a primeira parte do procedimento para resolver um sistema de 3? 3 lineares.](images/cdmp-formula12.png)

![Mostra a segunda parte do sistema de 3? 3 lineares.](images/cdmp-formula13.gif)![Mostrar o valor t subscript b no final da segunda parte do sistema 3? 3 linear.](images/cdmp-formula14.gif)

*X <sub>w</sub>*,*Y <sub>w</sub>*,*Z <sub>W</sub>*

![Mostra a parte final do procedimento para resolver um sistema de 3? 3 lineares.](images/cdmp-formula15.png)

Depois que a matriz triestímulo é determinada, a determinação das curvas de Tom segue a abordagem padrão. Para monitores CRT, presume-se que os canais individuais sigam o modelo "GOG":

![Mostra a fórmula do modelo ' G O G '.](images/cdmp-formula16.png)

onde *k <sub>g</sub>* é o "lucro", 1-*k <sub>g</sub>* é o "deslocamento" e? é o "gama". A matriz inversa da matriz triestímulo é aplicada aos dados da XYZ dos neutros para obter os dados RGB lineares, que são correlacionados com os valores RGB digitais usando a regressão não linear no modelo GOG. Essas características não precisam ser as mesmas para os canais R, G e B e, em geral, não são as mesmas.

Berns \[ 1 \] : Berns, *Billmeyer e Saltzman princípios de tecnologia de cores*, 3 <sub>RD</sub> Ed. John Wiley & filhos (2000).

Berns \[ 2 \] : Berns e Katoh, a função de transferência digital para radiometric para exibições CRT controladas por computador, *padrões de cores cies Symposium ' 97 cor para a tecnologia de geração de imagens*, Nov. 1997.

Berns \[ 3 \] : Berns, Fernandez e Taplin, estimando Black-Level emissões de exibições de Computer-Controlled, *pesquisa de cores e aplicativo*, 28:379-383 Wiley periódicos, Inc. (2003)

Kang \[ 1 \] : Kang, *tecnologia de cores para dispositivos de imagem eletrônica*, SPIE (1997)

Katoh \[ 1 \] : Katoh, Deguchi e Berns, uma caracterização precisa da proposta do monitor CRT (II) para uma extensão do método cie e sua verificação, *opt. Rev.* 8:397-408 (2001)

### <a name="lcd-device-model-baseline"></a>Linha de base do modelo de dispositivo LCD

A linha de base do modelo de dispositivo LCD é semelhante à linha de base do modelo de dispositivo CRT. Esta seção explicará as maneiras pelas quais a modelagem de LCD difere da modelagem CRT.

Uma diferença é que você não pode supor que as exibições de LCD sigam o modelo GOG usado para CRTs, e as curvas de Tom são obtidas pela interpolação de dados medidos. Por isso, o eixo neutro do dispositivo deve ser amostrado com mais frequência.

Aqui estão alguns valores de exemplo típicos que podem gerar bons dados para a linha de base do modelo de dispositivo LCD:

Vermelho: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Verde: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Azul: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutrals: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.

O processo de cálculo de desvios de cores medidos para obter as desvios para os primários de dispositivos é mais crítico para os LCDs do que para CRTs. Quando as medições da XYZ são plotadas no plano *XY* de desvio, uma situação típica é mostrada na Figura 1. Observe como a desvio é descompasso em direção ao ponto preto. Isso ocorre porque todos os LCDs têm uma certa quantidade de vazamento de luz.

![Diagrama que mostra um grafo da desvio usando dados brutos sem correção.](images/cdmp-lcd-dmp-figure1.png)

**Figura 1** : o diagrama de desvios usando dados brutos sem correção

Quando isso é subtraído das medidas brutas da XYZ, uma situação típica é descrita na Figura 2. Os pontos Tnão agora são clusterizados sobre três centros, embora eles não fiquem idênticos neles. O processo de média descrito para CRTs melhora muito os resultados de LCDs.

![Diagrama que mostra um grafo da desvio usando dados brutos com um ponto preto ajustado.](images/cdmp-lcd-dmp-figure2.png)

**Figura 2** : o diagrama de desvios usando dados com o ponto preto ajustado

### <a name="rgb-capture-device-model-baseline"></a>Linha de base do modelo do dispositivo de captura RGB

O modelo de dispositivo de captura RGB de linha de base é uma subclasse da classe IDeviceModel. Na caracterização de colorimétrico de dispositivos de captura de cor, como scanners e câmeras digitais, a abordagem a seguir é usada. Um destino que consiste em patches de cor com valores CIEXYZ conhecidos é capturado usando o dispositivo de captura. O resultado da captura é uma imagem de bitmap RGB na qual a cor de cada patch é codificada em um valor RGB. Esses valores RGB de dispositivo são específicos de um dispositivo de captura específico. O objetivo da caracterização de colorimétrico é estabelecer uma relação de empírica entre os valores RGB do dispositivo e os valores de CIEXYZ, ou uma transformação matemática de RGB para XYZ que modela de forma mais precisa o comportamento do dispositivo de captura.

Essa transformação matemática pode ser modelada razoavelmente por polinomiais de baixo grau. Esse procedimento é detalhado na literatura, por exemplo, Kang \[ 92 \] , Kang \[ 97 \] . No Kang \[ 97 \] , uma abordagem é relatada que usa um conjunto de três polinomiais com 3, 6, 8, 9, 11, 14 ou 20 termos nas variáveis R, G e B, enquanto os três polinomiais retornam, respectivamente, para os componentes X, Y e Z do espaço CIEXYZ. Para o polinomial de 20 termos, o formulário é:

![Mostra o polinomial de 20 termos.](images/cdmp-formula20.png)

Há expressões semelhantes para Y e Z. A técnica matemática para ajustar os polinomiais cai dentro de "regressão linear multivariada" e é descrita em qualquer texto elementar em estatísticas.

Esse método de regressão linear sofre de não minimizar a função de objetivo "certa". Por design, a regressão linear localiza a solução de quadrados mínimos, o que implica que os coeficientes obtidos minimizarão a soma total dos quadrados de erros no espaço subjacente ou, de forma equivalente, a soma dos quadrados das distâncias euclidiana. Na prática, você deseja minimizar a soma dos quadrados de? Es, onde? E é um dos padrões aceitos, como CIE94. Minimizar essa função objetiva é um problema de regressão não linear.

No novo mecanismo, o laboratório para a XYZ é o espaço de cores CIE que é resumido, e o polinomial cúbico de 20 termos é usado como modelo para o dispositivo de captura ou coeficientes ls, como a BS, de modo que os seguintes polinomiais minimizem a soma dos quadrados de? E <sub>CIE94</sub> s.

![Mostra um conjunto de fórmulas polinomiais.](images/cdmp-formula21.png)

A solução ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub></sub>* ) no espaço numérico real de 60-dimensional **R** 203 deve ser de modo que o seguinte erro total seja minimizado:

![Mostra o erro total a ser minimizado.](images/cdmp-formula22.png)

onde a soma é por todos os pares de pontos de dados (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub></sub>* i,*u <sub>i</sub>*,*v <sub>i</sub>* ) no conjunto de dados amostrado mais pontos de controle adicionais a serem detalhados no seguinte. Este é um problema de regressão não linear porque os parâmetros *?<sub> i</sub>*, *i <sub></sub>** <sub>eu</sub>* inseri a função Objective de forma não linear (não quadráticamente).

Porque a função Objective? é uma função não linear (e não quadrática) dos parâmetros *?<sub> i</sub>*, *i <sub></sub> e ** <sub>i</sub>*, você deve recorrer a técnicas iterativas para resolver o problema de otimização. Como a forma da função Objective é uma soma de quadrados, uma técnica de otimização padrão chamada de Levenberg-Marquardt algoritmo é usada. Ele é considerado o método de escolha para problemas de quadrados não lineares. Para algoritmos iterativos como Levenberg-Marquardt, você deve fornecer uma estimativa inicial. Uma boa estimativa inicial é geralmente crítica na localização do valor mínimo correto. Nesse caso, um bom candidato para a estimativa inicial é a solução do problema de regressão linear. Primeiro, minimize a soma do quadrado de distâncias de euclidiana no espaço do laboratório, definindo uma função de objetivo de quadrática:

![Mostra uma função de objetivo quadrática definida.](images/cdmp-formula23.png)

A solução matemática para esse problema de "quadrados mínimos lineares" é bem conhecida. Porque *?<sub></sub>só aparece* na modelagem *L* , *um <sub>i</sub>* só aparece na modelagem *u* e * <sub>i</sub>* aparece apenas na modelagem *v* ; o problema de otimização pode ser decomposto em três subproblemas: um para *L*, um para *u* e outro para *v*. Considere as equações *L* . (As equações *u* e as equações *v* seguem exatamente o mesmo argumento.) O problema de minimizar a soma dos quadrados de erros em *L* pode ser declarado como solução da equação de matriz a seguir no sentido mínimo de quadrados:

![Mostra uma equação de matriz para L.](images/cdmp-formula24.png)

em que *N* é o número total de pontos de dados (pontos de amostra originais, mais pontos de controle criados de uma maneira descrita abaixo). Normalmente, *N* é muito maior que 20, então a equação anterior é excessivamente determinada, exigindo uma solução de mínimo de quadrados. Uma solução de formulário fechado para o **?** está disponível:

![Mostra uma solução de formulário fechado.](images/cdmp-formula25.png)

Na prática, a avaliação direta usando a solução de formulário fechado não é usada porque ela tem propriedades numéricas inadequadas. Em vez disso, algum tipo de algoritmo de fatoração de matriz é aplicado à matriz de coeficiente que reduz o sistema de equações a um formato canônico. Na implementação atual, a decomposição de valor singular (SVD) é aplicada à matriz **R** e, em seguida, o sistema decomposto resultante é resolvido.

A solução para o problema de regressão linear, indicada por ![ mostra a solução para o problema de regressão linear.](images/cdmp-formula26.png) , é usado como o ponto de partida do algoritmo de Levenberg-Marquardt. Nesse algoritmo, uma etapa de avaliação é computada que deve mover o ponto mais próximo da solução ideal. A etapa de avaliação atende a um conjunto de equações lineares que dependem do valor funcional e dos valores das derivações no ponto atual. Por esse motivo, as derivações da função Objective? com relação aos parâmetros *?<sub> i</sub>*, *eu tenho entradas <sub></sub> necessárias para o <sub>algoritmo</sub>* de Levenberg-Marquardt. Embora existam 60 parâmetros, há um atalho que permite que você computar muito menos. Pela regra de cadeia de cálculo,

![Mostra uma equação que permite um atalho usando a regra de cadeia de cálculo.](images/cdmp-formula27.png)

em *que j* = 1, 2,, 20 *, L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* é o valor CIELAB do ponto de exemplo *i* -i, e *R <sub>IJ</sub>* é a entrada (*i*,*j* ) th da matriz **R** definida acima. Então, em vez de calcular derivativos para parâmetros 60, você pode calcular derivativos para *L*,*a* e *b* usando diferenciação de encaminhamento numérico.

Também é necessário configurar um critério de interrupção para algoritmos iterativos. Na implementação atual, as iterações serão encerradas se o DECIE94 quadrado médio for menor que 1 ou o número de iterações executadas exceder 10. O número 10 vem da experiência prática que se as primeiras iterações não reduzem o erro significativamente, as iterações adicionais não ajudarão muito além da movimentação do ponto de uma maneira oscillatory, ou seja, o algoritmo pode não convergir. Mesmo no caso de o algoritmo divergir, podemos ter certeza de que o DECIE94 não é pior do que começamos, ou seja, com os parâmetros obtidos da regressão linear.

Mesmo com o método anterior de regressão não linear, há vários problemas com o ajuste. Um problema é que os polinomiais tendem a exceder ou exceder os pontos de dados. Máximo local artificial e mínimo podem ser introduzidos no processo de ajuste. Isso pode ser imposto usando polinomiais de baixo grau, que é o motivo pelo qual você não deve usar mais de três graus. Um aspecto mais sério de sobretratação ou inviabilidade é que, embora um polinomial possa pegar qualquer valor real teoricamente, o espaço que ele tenta modelar normalmente tem restrições físicas e restrições práticas. CIEXYZ deve ter todos os X, Y, Z não negativos, que é uma restrição física. Na prática, eles só usam valores na magnitude de centenas, não milhares ou mais. Da mesma forma, CIELAB ou CIELUV tem suas próprias restrições físicas e práticas. Quando o espaço em RGB é preenchido suficientemente com pontos de exemplo, o problema de sobreenchente ou de excedente não é sério. No entanto, os pontos RGB capturados do dispositivo de captura geralmente não preenchem o espaço RGB uniformemente. Os pontos podem preencher somente os 80% do cubo RGB ou pior, eles podem residir em um diversa dimensional inferior. Quando isso acontece, os polinomiais regressados podem fazer um trabalho ruim na extrapolação dos valores além dos pontos de dados, às vezes retornando previsões irreais. Você quer um modelo que sempre retorne valores razoavelmente realistas. Isso requer um método que possa controlar efetivamente o comportamento do limite de polinomiais de regressão, impondo custos adicionais a esses polinomiais que se comportam incorretamente perto do limite do cubo RGB. Uma medida adicional para garantir que os polinomiais sempre retornam valores realistas são aplicados recortando a saída para dentro do local de CIE Spectral.

É nesse momento que a modelagem do scanner e a modelagem da câmera divergem uma da outra. Espera-se que o modelo de câmera expanda para regiões além dos pontos de amostra, incluindo os "realces especulares", a mesma extrapolação não é necessária para o modelo do scanner. Espera-se que o destino do scanner cubra uma caracterização semelhante aos materiais impressos a serem verificados. O modelo do verificador ainda precisa ser robusto no sentido de que ele não deve retornar valores irreais, mas extrapolação muito além da meta de caracterização não é necessária. Para garantir a robustez, o L-polinomial acima é recortado em 100, ou seja, o modelo polinomial é forçado a não extrapolar além de "DMín" do destino do scanner.

Espera-se que o modelo de câmera expanda para os realces especulares, de modo que o recorte em 100 é indesejável. Em vez disso, o algoritmo a seguir é usado.

Pontos de controle artificial são introduzidos para controlar o comportamento dos polinomiais em regiões com amostragem insuficiente. Ao posicionar estrategicamente esses pontos de controle com os valores apropriados, eles servem para "efetuar pull" das polinomiais na direção necessária. Na implementação atual, são usados oito pontos de controle correspondentes aos cantos do cubo RGB. Se os valores do dispositivo forem normalizados para o Unity, esses pontos serão:

*R* = 0, *G* = 0, *B* = 0

*R* = 0, *G* = 0, *B* = 1

*R* = 0, *G* = 1, *B* = 0

*R* = 0. *G* = 1, *B* = 1

*R* = 1, *G* = 0, *B* = 0

*R* = 1, *G* = 0, *B* = 1

*R* = 1, *G* = 1, *B* = 0

*R* = 1, *G* = 1, *B* = 1

Exceto para o *R*  = *G*  = *B* = 1, que está associado a um valor de CIELAB de *L* = 100, *u*  = *v* = 0, o seguinte algoritmo de extrapolação é usado para determinar o valor de CIELAB apropriado a ser associado. Em geral, para um determinado (*r*,*g*,*b* ), um peso é associado a cada (*r <sub>i</sub>*,*g <sub>i</sub>*,*b <sub></sub>* ) no conjunto de dados de amostra. Há duas metas para atribuir o peso. Primeiro, o peso é inversamente proporcional à distância entre (*r*,*G*,*B* ) e (*r <sub>i</sub>*,*G <sub>i</sub>*,*B <sub></sub>* ). Em segundo lugar, você deseja descartar ou atribuir peso 0 a, pontos que têm um matiz diferente do determinado ponto (*R*,*G*,*B* ). Para levar o matiz em conta, considere os pontos que estão dentro de um cone cujo vértice esteja em (0, 0, 0), cujo eixo coincide com a linha unindo (0, 0, 0) a (*R*,*G*,*B* ) e cujo ângulo semivertical? atende ao cos? = 0,9. Consulte a Figura 3 para obter uma ilustração desse cone.

![Diagrama que mostra a forma da vizinhança.](images/cdmp-lcd-dmp-figure3.png)

**Figura 3** : filtrando os pontos de exemplo por ângulo e distância. A forma da vizinhança representada é apenas para fins de ilustração. A forma real depende da distância usada; é um ambiente em forma de losango se a norma 1 é usada.

Dentro desse cone, uma segunda filtragem é executada com base na distância RGB, que usa a norma 1, definida por

![Mostra a fórmula para a segunda filtragem dentro do cone.](images/cdmp-formula28.png)

Com o cone atual, a pesquisa inicial é para pontos que estão dentro de uma distância de 0,1 de (*R*,*G*,*B* ). Se nenhum ponto for encontrado nesse raio, o raio será aumentado em 0,1 e a pesquisa será reiniciada. Se as próximas redes redondas não forem apontadas, o raio será aumentado em 0,1. Esse processo continua até que o raio exceda MaxDist/5, em que MaxDist = 3, no caso de 1-Norma. Se nenhum ponto for encontrado, o cone será ampliado pela redução do cos? por 0, 5, ou seja, aumentando o ângulo? e reiniciar todo o processo com um raio crescente. Esse processo continua até que um conjunto não vazio de pontos seja encontrado ou cos? chega a 0, ou seja, o cone foi aberto para se tornar um plano. Neste ponto, a pesquisa é reiniciada aumentando o raio, exceto que a pesquisa continua até que o raio alcance MaxDist. Isso garante que, no pior cenário, um conjunto de pontos não vazio será encontrado. O algoritmo é resumido no diagrama de fluxo da Figura 4.

![Diagrama que mostra o fluxo do algoritmo.](images/cdmp-lcd-dmp-figure4.png)

**Figura 4** : diagrama de fluxo para determinar o conjunto de pontos de exemplo usados na extrapolação para um valor RGB de entrada

Supondo que o processo anterior produza *um conjunto não* vazio de pontos (*R <sub>i</sub>*,*G <sub>i</sub>*, B) e correspondente (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), para cada um desses pontos, um peso *<sub></sub>* *w <sub></sub>* é atribuído, fornecido por

![Mostra a fórmula para um peso para cada ponto.](images/cdmp-formula29.png)

Por fim, o extrapolant é definido por

![Mostra a definição para o extrapolant.](images/cdmp-formula30.png)

As equações anteriores constituem uma instância dos "métodos com peso de distância inverso", normalmente chamados de métodos Shepard. Ao executar cada um dos oito pontos de EQ (6) por meio do algoritmo, são obtidos oito pontos de controle, cada um com os valores *R*,*G*,*b* e *L*,*a*,*B* , que são colocados no pool com os dados de exemplo originais.

Para garantir que o modelo sempre produza valores de cor válidos e a integridade do sistema e a estabilidade de todo o pipeline de processamento de cores, você deve executar um recorte final na saída do modelo polinomial. A gama visual de CIE é descrita pelo componente Achromatic (*Y* ou *L* ) e o componente de desvio (*dispersão* ou *a'b '*, que estão relacionados ao espaço XYZ por uma transformação projetada). Na implementação atual, a desvio de *a'b* é usada porque está diretamente relacionada ao espaço de CIELUV. Para qualquer valor de *CIELAB* , primeiro recorte de *L* para um valor não negativo:

![Mostra o recorte de L para um valor não negativo.](images/cdmp-formula31.png)

Para permitir a extrapolação de realces especulares, *L* não é recortado em 100, o limite superior "convencional" para *L* no espaço do laboratório.

Em seguida, se *L* = 0, *a* e *b* serão recortados de forma que a *= b =* 0. Se for *L* ? 0, calcular

![Mostra a fórmula se L = 0.](images/cdmp-formula32.png)

Estes são os componentes de um vetor no diagrama *a'b* do ponto branco (*u? '*,*v? '* ) à cor em questão. Definir o local de CIE Spectral como convexa envoltória de todos os pontos (*a '*,*b '* ), parametrizados pelo comprimento de onda?:

![Mostra a fórmula para o comprimento de onda.](images/cdmp-formula33.png)

onde ![ mostra as funções para a correspondência de cores CIE.](images/cdmp-formula34.png) são as funções de correspondência de cores CIE para o observador de dois graus. Se o vetor estiver fora do CIE local, a cor será recortada para o ponto na local CIE que é a interseção do local e a linha definida pelo vetor. Consulte a Figura 5. Se o recorte tiver ocorrido, o *valor a e* *b* será reconstruído pela primeira subtração *de um?* e *b? '* de *um '* e *b '* recortado e, em seguida, multiplique por 13 *L*.

![Diagrama que mostra o grafo para o algoritmo de recorte.](images/cdmp-lcd-dmp-figure5.png)

**Figura 5** : algoritmo de recorte para valores de laboratório que estão fora da gama visual de CIE

Na implementação atual, o local de CIE Spectral no plano de *a'b* é representado por uma curva linear piecewise com 35 segmentos (correspondendo a um comprimento de ondas de 360 nm a 700 nm, inclusive). Ao ordenar os segmentos de linha para que seus ângulos de pagamento no ponto branco sejam crescentes, o que é equivalente a ondas decrescentes, o segmento de linha que cruza com o raio formado pelo vetor acima pode ser encontrado por uma pesquisa binária simples.

### <a name="rgb-printer-device-model-baseline"></a>Linha de base de modelo de dispositivo de impressora RGB

A caracterização de um dispositivo de uma impressora RGB consiste em construir um modelo empírica do dispositivo que prevê a cor CIELUV independente do dispositivo para qualquer valor RGB determinado

Há duas maneiras de construir o modelo empírica. Uma maneira é usar os dados do dispositivo para uma impressora RGB e a outra é usar dados de parâmetros analíticos. Na primeira, os dados de medida fornecidos por um usuário para um dispositivo de impressora RGB são usados para construir a tabela de pesquisa 3-D (LUT). Os dados de medição consistem em valores de XYZ para patches RGB uniformemente amostrados. Os tamanhos de amostragem típicos são 9 ou 17 para cada componente. Cada patch é medido com um colorimeter ou spectrophotometer no espaço CIEXYZ. O valor XYZ de um patch é então convertido em valor CIELUV, formando um LUT 3-D. No modelo de dispositivo, o método de interpolação tetrahedral do Sakamoto é aplicado ao LUT 3D para prever os dados do CIELUV para determinados dados RGB. (Conf-US patente 4275413 (Sakamoto et al.), patente dos EUA 4511989 (Sakamoto), Kang \[ 1 \] . As duas patentes mencionadas expiraram.). Os dados de parâmetro analítico passados no segundo método são simplesmente um LUT que foi criado anteriormente. Normalmente, esse LUT foi criado usando o primeiro método, embora possa ser criado manualmente.

No gerenciamento de cores atual, o mapa de origem é definido como o mapa que passa do espaço RGB para um espaço de cores CIEXYZ independente de dispositivo. O mapa de destino é definido como o mapa que vai do espaço de cores CIEXYZ independente de dispositivo para o espaço RGB. É o inverso do mapa de origem.

O modelo empírica é usado diretamente no mapa de origem. Ele primeiro mapeia determinados dados RGB em um CIELUV dados, que são convertidos em dados do XYZ. No mapa de destino, os dados de CIEXYZ independentes do dispositivo são convertidos primeiro em dados do CIELUV. Em seguida, o modelo empírica e o método clássico Newton-Raphson são usados para prever os melhores dados RGB para os dados de CIELUV. Os detalhes sobre a conversão de CieLUV para dados RGB são os seguintes:

Depois de gerar um LUT de 3D de RGB para CieLUV, o mapa de RGB para LUV é criado usando a interpolação de tetrahedral em RGB. Este mapa é indicado pelas seguintes equações:

![Mostra as equações do mapa de R G B a L U V.](images/cdmp-image125.png)

A inversão do mapa consiste em resolver, para qualquer cor ![Mostra L U V.](images/cdmp-image127.png) , o seguinte sistema de equações não lineares:

![Mostra as equações não lineares para lolving qualquer cor L U V.](images/cdmp-image129.png)

Uma equação não linear baseada no método Newton-Raphson clássico é usada na nova CTE. Uma estimativa inicial ou *uma priori* vê, s <sub>anterior</sub> -(R 0, G 0, B 0) é obtida por meio da pesquisa por meio de uma "matriz de propagação" que consiste em uma grade 8x8x8 uniforme de pares previamente computados (RGB, Luv). O Luv correspondente RGB que está mais próximo ao L \* u \* v \* é escolhido. Cada ponto na matriz de propagação corresponde ao centro de uma célula para que as iterações não comecem com um ponto na face de limite do cubo RGB. Em outras palavras, o RGB das sementes é definido por: etapa = 1/8 s <sub>IJK</sub> = (etapa/2 + (i-1) etapa, etapa/2 + (j-1) etapa, etapa/2 + (k-1) etapa) com i, j, k = 1... 8 na etapa *i* do Newton-Raphson, a próxima estimativa ![ mostra as variáveis para a próxima estimativa.](images/cdmp-image133.png) é obtido pela fórmula:

![Mostra a fórmula da estimativa.](images/cdmp-image135.png)

A iteração para quando o erro (distância no espaço CIELUV) é menor que um nível de tolerância predefinido (0,1 na CTE) ou quando o número de iterações excedeu o número máximo permitido de iterações (10 na CTE). Os valores para a tolerância e o número de iterações foram empiricamente determinados para serem efetivos. Em versões futuras, o valor de tolerância pode ser alterado.

A matriz Jacobian é calculada usando a diferença de avanço, exceto em um ponto de limite (um ou mais de R, G, B é 1), em que a diferença retroativa é usada. Em vez de calcular o inverso da matriz Jacobian, o sistema linear é resolvido diretamente usando Gauss-Jordan eliminação com dinamização completa.

No final das iterações, a convergência ainda pode não ser obtida porque Newton-Raphson é um algoritmo "local", ou seja, ela só funcionará bem se você começar com uma estimativa inicial que está próxima da verdadeira solução. Se, no final das iterações de Newton-Raphson, a convergência na tolerância de erro predefinida não tiver sido atingida, as iterações serão reiniciadas com um novo conjunto de sementes, definido da seguinte maneira.

Por exemplo, a melhor solução obtida até agora é (r, g, b). A partir dessa solução, N uma posteriori sementes são derivadas, em que N = 4. Intuitivamente, a solução é movida "em direção ao centro" em um tamanho de etapa que depende de N. Consulte a Figura 6.

![Diagrama que mostra as direções de muito da solução.](images/cdmp-image136.png)

**Figura 6** : a direção do muito da solução depende de qual octant está.

Em outras palavras, se r &gt; 0,5, o valor no canal de r será diminuído, caso contrário, o valor será aumentado. Há uma lógica semelhante para os canais G e B. As definições precisas são:

MUITO = 0,5/(N + 1)

Dir (r) =-1 se r &gt; 0,5; + 1 caso contrário. Da mesma forma para dir (g) e dir (b)

Jth uma semente posteriori, s????, is (r + dir (r) \* j \* muito, g + dir (g) \* j \* muito, b + dir (b) \* j \* muito)

Experimente as primeiras s???? e se ele fornecer uma nova solução dentro da tolerância a erros, você poderá parar. Caso contrário, experimente o segundo s???? e assim por diante até o enésimo s????.

Os esquemas de todo o algoritmo são mostrados na Figura 7.

![Diagrama que mostra o fluxo para inverter o modelo do dispositivo.](images/cdmp-image138.png)

**Figura 7** : esquemas de inverter o modelo do dispositivo

### <a name="rgb-virtual-device-model-baseline"></a>Linha de base de modelo de dispositivo virtual RGB

Esse modelo de dispositivo (DM) é um algoritmo simples de reprodução de matriz/Tom. A matriz é derivada do ponto branco e dos primários usando algoritmos de ciência de cores padrão. A curva de reprodução de Tom é derivada dos parâmetros de medição de acordo com as descrições de ICC de Curvetype e parametrictype (ou invertidas conforme necessário). Os detalhes dos algoritmos internos serão fornecidos após a validação adicional de problemas de intervalo dinâmico alto.

O modelo de dispositivo virtual RGB é uma curva de reprodução de matriz/Tom ideal de RGB semelhante ao design de perfil baseado em matriz de três componentes ICC. Os parâmetros de "medida virtual" do DM incluem um valor de ponto branco (absoluto CIEXYZ), valores primários RGB (absoluto CIEXYZ) e uma curva de reprodução de Tom que se baseia no ICC ParametricCurveType e no Curvetype na formatação XML consistente com os esquemas DMP.

A codificação de tipo de função parametricCurveType de ICC e o suporte correspondente em IRGBVirtualDeviceModelBase são mostrados na tabela a seguir.



| Tipo de função                                         | Parâmetros                          | Tipo                                     | Observação                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![Mostra a função ' Gamatype '.](images/cdmp-image154.png)<br/> | g<br/>              | Gamatype<br/>                 | Implementação comum<br/>           |
| ![Mostra a função ' GammaOffsetGainType '.](images/cdmp-image156.png)<br/> | GA b<br/>           | GammaOffsetGainType<br/>       | CIE 122-1966<br/>                    |
| ![Mostra a função ' GammaOffsetGainOffsetType '.](images/cdmp-image158.png)<br/> | GA b c<br/>         | GammaOffsetGainOffsetType<br/> | IEC 61966-3<br/>                     |
| ![Mostra a função ' GammaOffsetGainGainType '.](images/cdmp-image160.png)<br/> | GA b c d<br/>       | GammaOffsetGainGainType<br/>   | IEC 61966-2.1<br/> sRGB<br/> |
| ![Mostra uma função para os parâmetros ' g a b c d e f '.](images/cdmp-image162.png)<br/> | GA b c d e f<br/>   | N/D<br/>                       | Sem suporte no WCS<br/>            |



 

A curva de Tom para dispositivos virtuais RGB é aplicada em DeviceToColorimetric entre os dados de entrada, o pDeviceColors e a matriz de multiplicação. Para ColorimetricToDevice, um método deve ser usado para inverter a curva de Tom. Na implementação de linha de base, isso é feito pela interpolação direta na mesma curva de Tom usada para DeviceToColorimetric.

As curvas devem ser especificadas nos perfis como pares de números no espaço flutuante. O primeiro número representa valores em pDeviceColors. O segundo número representa a saída da curva de Tom. Todos os valores na curva de Tom devem estar entre minColorantUsed e maxColorantUsed. As curvas de Tom devem conter pelo menos duas entradas: uma para minColorantUsed e outra para maxColorantUsed. O número máximo de entradas no ToneCurve é 2048. Em geral, quanto mais entradas na tabela, mais precisamente você pode modelar a curvatura. Uma interpolação linear piecewise é executada entre as entradas.

Você pode considerar métodos alternativos de interpolação. Se você souber algo sobre o comportamento subjacente do dispositivo, poderá usar menos amostras e modelar de forma mais precisa com uma curva de ordem mais alta. Mas se você usar o tipo de curva errado, será muito impreciso. Sem mais informações, não é possível adivinhar o tipo de curva. Portanto, use a interpolação linear e forneça vários pontos de dados.

### <a name="cmyk-printer-device-model-baseline"></a>Linha de base de modelo de dispositivo de impressora CMYK

A caracterização de um dispositivo de uma impressora CMYK consiste em construir um modelo empírica do dispositivo que prevê a cor impressa para qualquer valor CMYK determinado. A caracterização também inclui a inversão desse modelo para que uma receita do valor CMYK para nós para uma determinada cor seja impressa possa ser fornecida. Isso normalmente é definido em termos de valor CIEXYZ ou CIELAB.

Normalmente, um destino de ti 8.7/3 contendo patches CMYK é usado. Os patches consistem em amostragem do espaço CMYK de uma maneira bem definida, de forma que uma grade retangular (com espaçamento não uniforme em C, M, Y e K) seja formada. Em seguida, cada patch é medido com um colorimeter ou spectrophotometer. Em seguida, as medidas em valores CIEXYZ formam uma tabela de pesquisa (LUT), da qual um modelo de empírica da impressora é criado usando o método de interpolação de Sakamoto. Patente US 4275413 (Sakamoto et al.), patente dos EUA 4511989 (Sakamoto), Kang \[ 1 \] . As duas patentes mencionadas expiraram.

Os requisitos específicos para os exemplos de medidas CMYK necessários para que um perfil de modelo de dispositivo seja aceito como válido pelo modelo de dispositivo de linha de base de impressora CMYK são os seguintes. (O conjunto de amostras é descrito mais claramente como um conjunto de cubos de exemplo de CMY, cada um associado a um nível de K específico.)

-   No mínimo, os cubos CMY válidos devem ser fornecidos para os níveis K = 0 e K = 100.
-   Os níveis intermediários de K podem não ter espaçamento uniforme.
-   Qualquer nível K intermediário sem um cubo CMY válido será ignorado.
-   Os cubos CMY podem usar intervalos de exemplo não uniformes (espaçamento de grade), mas o mesmo conjunto de intervalos de amostra deve ser usado em todas as dimensões C, M e Y no cubo CMY para um determinado nível de K.
-   Cada cubo CMY de nível K pode usar um número diferente e espaçamento de intervalos de exemplo.
-   Todos os cubos CMY devem conter os "cantos" do cubo CMY, ou seja, exemplos de CMY em \[ 0, 0, 0 \] , \[ 0, 0100, \] \[ 0100, 0 \] , \[ 100, 0, 0 \] , \[ 0100.100 \] , \[ 100, 0100 \] , \[ 100.100, 0 \] , \[ 100.100.100 \] .
-   Todos os níveis de grade CMY intermediários devem ser totalmente amostrados em cada canal. Em outras palavras, um exemplo deve existir em cada interseção de grade 3D dentro do cubo CMY.
-   Para os cubos de AT K = 0 e K = 100 CMY, os cubos de "somente cantos" 2x2x2 são o mínimo aceito como válido.

    \[Observação: para K = 0 e K = 100 níveis, um cubo CMY 3x3x3 será processado como um cubo 2x2x2 "somente cantos"; o nível de amostra intermediário é ignorado. 4x4x4 e cubos maiores terão todos os exemplos em grade usados.\]

-   Para os níveis intermediários de K, os cubos CMY 4x4x4 são o mínimo aceito como válido.

Um perfil de alta qualidade usará grades de amostragem mais finas do que o mínimo necessário para a validade, geralmente 9x9x9x9 ou superior. Os exemplos dos destinos IT 8.7/3, IT 8.7/4 e ECI produzem perfis de modelo de dispositivo (DMPs) válidos para o modelo de dispositivo de linha de base de impressora CMYK. Embora esse modelo de dispositivo seja capaz de ignorar os exemplos estranhos (fora da grade) nesses destinos, não há garantia de que eles sejam capazes de fazer isso para outros destinos e, portanto, é recomendável que amostras estranhas sejam removidas dos conjuntos de medidas que entram em perfis para esse modelo de dispositivo.

A inversão do modelo de impressora apresenta mais dificuldades. Dada uma cor de entrada em CIECAM, há uma pergunta se essa cor está dentro da gama da impressora. Também há o problema em relação à disposição de pontos no espaço de aparência da cor. Embora possamos organizar os valores CMYK para ficarem em uma grade retangular, como é feito no destino de ti 8.7/3, o mesmo não pode ser dito das cores impressas resultantes, pois estão situadas no espaço de aparência da cor. Em geral, eles estão espalhados no espaço de aparência de cor sem nenhum padrão específico.

Em geral, há duas abordagens para o problema de inversão de pontos dispersos. Uma abordagem é usar uma subdivisão geométrica da gama da impressora usando sólidos bidimensionais elementares, como tetrahedra. Uma subdivisão da gama da impressora no espaço de aparência da cor pode ser induzida a partir da subdivisão correspondente do espaço CMY (K), consulte travada \[ 93 \] , Kang \[ 97 \] . Essa abordagem tem a vantagem de uma simplicidade computacional. No caso de um tetraedro, somente quatro pontos são usados em uma interpolação. Por outro lado, o resultado depende muito de alguns pontos, o que significa que um erro de medida terá um efeito significativo sobre o resultado. A interpolação também tende a não ser tão suave. A segunda abordagem não assume nenhuma subdivisão e se baseia na técnica de interpolação de dados dispersos. Um exemplo clássico é a técnica de interpolação Shepard ou método inverso invertido (consulte Shepard \[ 68 \] ). Aqui, vários pontos em torno do ponto de entrada são escolhidos de alguma maneira, cada um atribuído a um peso, geralmente inversamente proporcional à distância, e a interpolação é tomada como a média ponderada dos pontos vizinhos. Nessa abordagem, a escolha dos pontos vizinhos é fundamental para o desempenho. Embora poucos pontos possam renderizar os pontos intercorretos e não-suaves interpolares, um grande número de casas impõe um custo computacional alto, pois os pesos normalmente são funções não lineares e são dispendiosos para computar.

As duas abordagens descritas acima têm problemas. A abordagem de subdivisão depende crucialmente dos dados que são razoavelmente nulos de ruído e, em geral, o interpolação não é muito suave. A interpolação de dados dispersos é mais tolerante ao ruído de dados e geralmente proporciona uma interpolação mais suave, mas é computacionalmente mais cara.

A nova CTE usa uma abordagem alternativa. O dispositivo CMYK é tratado como uma coleção de vários dispositivos CMY, cada um com um valor específico de preto (K). Usando um algoritmo de seleção que usa como parâmetros claridade e croma, um nível de preto é escolhido. Os valores de CMY são obtidos pela inversão da tabela CMY para Luv correspondente usando os métodos de Newton empregados em outro lugar pelo algoritmo de impressora RGB.

Use as etapas a seguir.

1.  Imprima o destino de caracterização, que é o destino 8.7/3 ou um destino que contém a amostragem do espaço CMYK em intervalos de espaçamento regular ou irregular.
2.  Meça o destino usando um spectrophotometer e converta as medidas para o espaço CIELUV.
3.  Construa o mapa de encaminhamento de CMYK para luv.
4.  Use o mapa de encaminhamento para construir um conjunto de CMY para Luv Maps para um intervalo de valores de K.
5.  Para qualquer valor de Luv de entrada, o valor CMYK correspondente é obtido selecionando um dos mapas construídos na etapa 4 acima e invertendo usando o método Newton para obter um conjunto de Colorant de CMY para acompanhar o valor K selecionado.

As etapas 1 e 2, que são procedimentos padrão, são executadas por um programa de criação de perfil que não faz parte da nova CTE. O destino de ti 8.7/3 contém uma amostragem razoavelmente detalhada de todos os valores CMYK em vários níveis de C, M, Y e K. como alternativa, um destino personalizado com a amostragem uniforme dos canais C, M, Y e K pode ser usado. Depois que o destino é impresso, um spectrophotometer ou colorimeter pode ser usado para medir o valor XYZ de cada patch, e o valor XYZ pode ser convertido para o valor de Luv usando o modelo CIELUV.

A etapa 3, construção do mapa de encaminhamento de CMYK para Luv, pode ser obtida aplicando-se qualquer técnica de interpolação conhecida, como tetrahedral ou método Multiline, na grade retangular no espaço CMYK. Na nova CTE, uma interpolação de tetrahedral de 4 dimensões é usada. Como as grades de amostragem de CMY geralmente são diferentes em cada nível de K, no entanto, usamos uma técnica de Superamostragem, conforme detalhado abaixo. Para um determinado ponto CMYK, os níveis de sanduíche de t são determinados primeiro com base no valor K. Em seguida, introduza uma "super Grid" em cada nível de K que é uma União das grades CMY em cada um dos dois níveis de K. Em cada nível de K, o valor de Luv de qualquer ponto de grade introduzido recentemente é obtido por uma interpolação de tetrahedral tridimensional dentro desse nível de K. Por fim, uma interpolação de tetrahedral de 4 dimensões para o ponto CMYK específico é executada nessa nova grade.

![Diagrama que mostra a superamostragem.](images/cdmp-image163.png)

**Figura 8** : Superamostragem

A etapa 4 constrói um conjunto de LUTs (tabelas de pesquisa CMY-para-Luv). O mapa de encaminhamento construído na etapa 3 é chamado repetidamente para reamostrar o espaço CMYK. O espaço de cores CMYK é amostrado usando um espaçamento par de K e outro, mas ainda com espaçamento uniforme, de amostragem de CMY.

A etapa 5 é um procedimento para obter o valor CMYK usando o LUTs construído na etapa 4 para qualquer ponto de Luv de entrada. O valor apropriado de K é escolhido analisando a claridade, bem como o grau de cor no Luv solicitado. Depois que a tabela é selecionada, os valores de CMY são obtidos da tabela usando o método Newton (conforme documentado no modelo de dispositivo de impressora RGB anteriormente).

O espaço CIELUV é usado no modelo de impressora em vez de CIEJab porque o modelo de dispositivo deve ser baseado apenas em dados colorimétrico disponíveis no DMP. O DMP contém dados colorimétrico para cada patch medido, incluindo o ponto branco de mídia, portanto, é possível converter dados do CIEXYZ em dados do CIELUV. No entanto, não é possível converter em CIECAM02 JCh ou jab, porque não há acesso às informações da condição de exibição no DMP.

### <a name="rgb-projector-device-model-baseline"></a>Linha de base do modelo de dispositivo do projetor RGB

Observação: muitos projetores RGB têm mais de um modo de operação. Em um modo, que geralmente é o padrão e pode ser chamado algo como "apresentação", a resposta de cor do projetor é otimizada para o brilho máximo. No entanto, nesse modo, o projetor perde a capacidade de reproduzir cores claras, um pouco de desvio, como amarelos pálidos e alguns tons. Em outro modo, geralmente chamado de "filme", "vídeo" ou "sRGB", o projetor é otimizado para reprodução de imagens realísticas e cenas naturais. Nesse modo, o brilho máximo é negociado para melhorar a qualidade geral da reprodução de cores. Para obter uma reprodução de cores satisfatória com projetores RGB, é necessário posicionar o projetor em um modo em que uma gama suave de cores possa ser reproduzida.

![Diagrama que mostra um modelo de dispositivo D L P.](images/cdmp-image167.png)

**Figura 9** : modelo de dispositivo DLP

Um valor RGB de entrada passa por dois caminhos computacionais. A primeira é o modelo de matriz, que resulta em um valor XYZ. Isso é seguido imediatamente pela conversão de XYZ para luv. A segunda é a interpolação LUT não uniforme usando a interpolação tetrahedral. A saída da interpolação já está no espaço Luv por construção. As duas saídas são adicionadas para obter o valor Luv previsto. Isso é finalmente convertido para XYZ, que é a saída esperada do modelo colorimétrico para o dispositivo DLP.

Como os projetores são dispositivos de exibição, eles também dão suporte à inversão do modelo, ou seja, a transformação da XYZ para a RGB. Como o modelo de dispositivo transforma o espaço RGB para o espaço XYZ, que são tridimensionais, inversão é equivalente a resolver três equações não lineares em três desconhecidas. Isso pode ser feito por técnicas de solução de equações padrão, como Newton-Raphson. No entanto, é preferível primeiro converter a XYZ em luv e, em seguida, inverter a transformação de Luv para RGB, porque o espaço de Luv é mais perceptually linear do que o espaço XYZ.

### <a name="icc-device-model-baseline"></a>Linha de base do modelo de dispositivo ICC

A interoperabilidade do fluxo de trabalho de ICC de contratação é habilitada criando um perfil de modelo de dispositivo de linha de base de dispositivo ICC especial que armazena o objeto de perfil e cria uma transformação ICC usando um perfil XYZ não operacional. Em seguida, essa transformação é usada para converter entre as cores do dispositivo e do CIEXYZ.

![Diagrama que mostra a interoperabilidade de fluxo de trabalho C I E C c.](images/cdmp-image168.png)

**Figura 10** : citar a interoperabilidade do fluxo de trabalho ICC

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos básicos de gerenciamento de cores](basic-color-management-concepts.md)
</dt> <dt>

[Algoritmos e esquemas do sistema de cores do Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





