---
title: Esquema e algoritmo de perfil do modelo de dispositivo de cores do WCS
description: Este tópico fornece informações sobre o esquema de perfil de modelo de dispositivo de cores WCS e seus algoritmos associados. Este tópico contém as seções a seguir OverviewColor perfil de modelo de dispositivo ArchitectureThe CDMP SchemaWCS CDMP v 2.0 Calibration AdditionThe CDMP Schema ElementsColorDeviceModelProfileColorDeviceModelNamespaceVersionVersionDocumentationCRTDevice elementLCDDevice elementProjectorDevice elementScannerDevice elementCameraDevice elementRGBPrinterDevice elementCMYKPrinterDevice elementRGBVirtualDevice elementPlugInDeviceTypeRGBVirtualMeasurementTypeGammaTypeGammaOffsetGainTypeGammaOffsetGainLinearGainTypeToneResponseCurvesTypeGamutBoundarySamplesTypeFloatPairListCMYKPrinterMeasurementTypeRGBPrinterMeasurementTypeRGBCaptureMeasurementTypeOneBasedIndexRGBProjectorMeasurementTypeDisplayMeasurementTypeMeasurementConditionsTypeGeometryTypeRGBPrimariesGroupNonNegativeCMYKSampleTypeNonNegativeRGBSampleTypeNonNegativeCMYKTypeNonNegativeRGBTypeExtensionTypeNonNegativeXYZTypeXYZTypeThe  CDMP Baseline AlgorithmsCRT dispositivo modelo BaselineLCD dispositivo modelo BaselineRGB impressora modelo de dispositivo BaselineRGB dispositivo virtual modelo de dispositivo BaselineCMYK impressora modelo de dispositivo BaselineRGB
ms.assetid: bbb3b50d-75fc-476d-a011-af7dcc2ac520
keywords:
- Windows Sistema de cores (WCS), perfil de modelo de dispositivo de cores (CDMP)
- WCS (Windows sistema de cores), perfil de modelo de dispositivo de cores (CDMP)
- gerenciamento de cores de imagem, perfil de modelo de dispositivo de cores (CDMP)
- gerenciamento de cores, perfil de modelo de dispositivo de cores (CDMP)
- cores, perfil de modelo de dispositivo de cores (CDMP)
- Windows Sistema de cores (WCS), perfis
- WCS (Windows sistema de cores), perfis
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
ms.openlocfilehash: 5210da85cd320a80e6b29a59e3cb5ff37c86fd174934832404e4b52cf53bd110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118037742"
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

o elemento **ColorDeviceModel** do esquema CDMP foi atualizado no Windows 7 para incluir o novo elemento calibration. O seguinte mostra a alteração no esquema CDMP.


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
7.  Float MinColorant,
8.  Escolha de elementos
    1.  CRTDevice,
    2.  LCDDevice,
    3.  RGBProjectorDevice,
    4.  ScannerDevice,
    5.  CameraDevice,
    6.  RGBPrinterDevice,
    7.  CMYKPrinterDevice,
    8.  RGBVirtualDevice,
9.  PlugInDevice,
10. ExtensionType opcional

**Condições de validação:** Cada subconjunto é validado por seu próprio tipo. Os subconjuntos de cadeia de caracteres têm um máximo de 10.000 caracteres. O subconjunto MaxColorant deve ser maior ou igual a zero (0) e maior que o subconjunto MinColorant. O MinColorant pode ser negativo.

### <a name="namespaceversion"></a>NamespaceVersion

xmlns:cdm=" http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

targetNamespace=" http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

### <a name="version"></a>Versão

Versão = "1.0" com Windows Vista.

**Condições de validação:** Qualquer valor de &gt; versão 0.1 ou =2.0 é válido para dar suporte a alterações sem &lt; quebra no formato.

### <a name="documentation"></a>Documentação

Esquema do Perfil de Modelo de Dispositivo.

Copyright (C) Microsoft. All rights reserved.

### <a name="crtdevice-element"></a>Elemento CRTDevice

Esse elemento é uma sequência de subconjunto de um MeasurementData DisplayMeasurementType.

**Condições de validação:** Cada subconjunto é validado por seu próprio tipo.

### <a name="lcddevice-element"></a>Elemento LCDDevice

Esse elemento é uma sequência de subconjunto de um MeasurementData DisplayMeasurementType.

**Condições de validação:** Cada subconjunto é validado por seu próprio tipo.

### <a name="projectordevice-element"></a>Elemento ProjetoDevice

Esse elemento é uma sequência de subconjunto de um MeasurementData RGBProjectorMeasurementType.

**Condições de validação:** Cada subconjunto é validado por seu próprio tipo.

### <a name="scannerdevice-element"></a>Elemento ScannerDevice

Esse elemento é uma sequência de subconjunto de um MeasurementData RGBCaptureMeasurementType

**Condições de validação:** Cada subconjunto é validado por seu próprio tipo.

### <a name="cameradevice-element"></a>Elemento CameraDevice

Esse elemento é uma sequência de subconjunto de um MeasurementData RGBCaptureMeasurementType

**Condições de validação:** Cada subconjunto é validado por seu próprio tipo.

### <a name="rgbprinterdevice-element"></a>Elemento RGBPrinterDevice

Esse elemento é uma sequência de subconjunto de um MeasurementData RGBPrinterMeasurementType.

**Condições de validação:** Cada subconjunto é validado por seu próprio tipo.

### <a name="cmykprinterdevice-element"></a>Elemento CMYKPrinterDevice

Esse elemento é uma sequência de subconjunto de um MeasurementData CMYKPrinterMeasurementType.

**Condições de validação:** Cada subconjunto é validado por seu próprio tipo.

### <a name="rgbvirtualdevice-element"></a>Elemento RGBVirtualDevice

Esse elemento é uma sequência de subconjunto de um RGBVirtualMeasurementDataType.

**Condições de validação:** Cada subconjunto é validado por seu próprio tipo.

### <a name="plugindevicetype"></a>PlugInDeviceType

Esse elemento é uma sequência de um GUIDType GUID e qualquer subconjunto.

**Condições de validação:** O GUID é usado para corresponder ao GUID de DLL do PlugIn do DM. Há um máximo de 100.000 subconjunto personalizados.

### <a name="rgbvirtualmeasurementtype"></a>RGBVirtualMeasurementType

Esse elemento é uma sequência que consiste em

1.  Grupo RGBPrimariesGroup
2.  Uma escolha de
3.  -   Gama
    -   GammaOffsetGain
    -   GammaOffsetGainLinearGam
    -   Elementos ToneResponseCurves

4.  opcional GamutBoundarySamples GamutBoundarySamplesType
5.  TimeStamp dateTime

**Condições de validação:** Cada subconjunto desses tipos tem suas próprias condições de validação.

### <a name="gammatype"></a>GammaType

Esse elemento é um tipo complexo que consiste no atributo

-   Gama NonNegativeFloatType

**Condições de validação:** A ser determinado com os comentários do setor.

### <a name="gammaoffsetgaintype"></a>GammaOffsetGainType

Esse elemento é um tipo complexo que consiste nos atributos

-   Gama NonNegativeFloatType
-   Offset NonNegativeFloatType
-   Obter NonNegativeFloatType

**Condições de validação:** A ser determinado com os comentários do setor.

### <a name="gammaoffsetgainlineargaintype"></a>GammaOffsetGainLinearGainType

Esse elemento é um tipo complexo que consiste nos atributos

-   Gama NonNegativeFloatType
-   Offset NonNegativeFloatType
-   Obter NonNegativeFloatType
-   LinearGain NonNegativeFloatType
-   TransitionPoint NonNegativeFloatType.

**Condições de validação:** A ser determinado com os comentários do setor.

### <a name="toneresponsecurvestype"></a>ToneResponseCurvesType

Esse elemento é uma sequência de

1.  RedTRC FloatPairList
2.  GreenTRC FloatPairList
3.  BlueTRC FloatPairList

O elemento também tem um atributo TRCLength do tipo unsignedint.

**Condições de validação:** A ser determinado com os comentários do setor.

### <a name="gamutboundarysamplestype"></a>GamutBoundarySamplesType

Esse elemento é uma sequência de RGBTypes RGB.

**Condições de validação:** Ocorrências máximas não unidas no momento, a serem limitados com base nos comentários do setor.

### <a name="floatpairlist"></a>FloatPairList

Esse elemento é um tipo simples de lista de pares de floats.

**Condições de validação:** A ser determinado com os comentários do setor.

### <a name="cmykprintermeasurementtype"></a>CMYKPrinterMeasurementType

Esse elemento é um

1. sequência do elemento ColorCube que consiste em uma sequência de Sample NonNegativeCMYKSampleType

2. Atributo TimeStamp dateTime.

**Condições de validação:** A ser determinado com os comentários do setor.

### <a name="rgbprintermeasurementtype"></a>RGBPrinterMeasurementType

Esse elemento é um

1. sequência do elemento ColorCube que consiste em uma sequência de Sample NonNegativeRGBSampleType

2. Atributo TimeStamp dateTime.

**Condições de validação:** A ser determinado com os comentários do setor.

### <a name="rgbcapturemeasurementtype"></a>RGBCaptureMeasurementType

Esse elemento é uma sequência de

1.  ComplexType PrimaryIndex de
2.  1.  OneBasedIndex branco
    2.  OneBasedIndex preto opcional
    3.  Red OneBasedIndex opcional
    4.  Opcional OneBasedIndex verde
    5.  Opcional Blue OneBasedIndex
    6.  Opcional Cyan OneBasedIndex
    7.  Opcional Magenta OneBasedIndex
    8.  OneBasedIndex amarelo opcional

3.  NeutralIndices de linhas de OneBasedIndex
4.  Sequência ColorSamples de Sample NonNegativeRGBSampleType

O elemento também tem um atributo DateTime TimeStamp.

**Condições de validação:** A ser determinado com os comentários do setor.

### <a name="onebasedindex"></a>OneBasedIndex

Esse elemento é um tipo simples de base de restrição unsigned int com valor minInclusive = "1".

**Condições de validação:** A ser determinado com os comentários do setor.

### <a name="rgbprojectormeasurementtype"></a>RGBProjectorMeasurementType

Esse elemento é uma sequência de

1.  Grupo RGBPrimariesGroup
2.  elemento ColorSamples que consiste na sequência de Sample NonNegativeRGBSampleType

O elemento também tem um atributo DateTime TimeStamp.

**Condições de validação:** A ser determinado com os comentários do setor.

### <a name="displaymeasurementtype"></a>DisplayMeasurementType

Esse elemento é uma sequência de

1.  grupo RGBPrimariesGroup
2.  GrayRamp da sequência de Exemplo NonNegativeRGBType
3.  RedRamp da sequência de Exemplo NonNegativeRGBType
4.  GreenRamp da sequência de Exemplo NonNegativeRGBType
5.  BlueRamp da sequência de Exemplo NonNegativeRGBType

O elemento DisplayMeasurementType também tem um atributo DateTime timeStamp.

**Condições de validação:** A ser determinado com os comentários do setor.

### <a name="measurementconditionstype"></a>MeasurementConditionsType

O MeasurementConditionsType é uma sequência de subconjunto que contém:

1.  Valor de enumeração de cadeia de caracteres restrita do ColorSpace de "CIEXYZ"
2.  opção opcional de enumeração de cadeia de caracteres WhitePoint NonNegativeXYZType ou WhitePointName dos valores D50, D65, A ou F2
3.  Geometry GeometryType
4.  ApertureSize inteiro em milímetros

Os padrões são:

1.  Impressoras RGB e CMYK:
    1.  CIEXYZ MeasurementSpaceType
    2.  D50 WhitePointValue
    3.  0/45 GeometryType
    4.  10mm ApertureSize
2.  Scanners:
    1.  CIEXYZ MeasurementSpaceType
    2.  D50 WhitePointValue
    3.  0/45 GeometryType
    4.  10mm ApertureSize
3.  Exibe e dispositivo virtual RGB:
    1.  CIEXYZ MeasurementSpaceType
    2.  D65 WhitePointValue
    3.  0/45 GeometryType
    4.  10mm ApertureSize
4.  Câmeras:
    1.  CIEXYZ MeasurementSpaceType
    2.  D65 WhitePointValue
    3.  GeometryType Direto
    4.  10mm ApertureSize

**Condições de validação:** A validação de cada subconjunto é determinada pelas condições de validação para esses subconjunto. Se algum subconjunto estiver ausente, o padrão específico do tipo de modelo de dispositivo será usado.

### <a name="geometrytype"></a>GeometryType

String

Valores de enumeração:

-   "0/45"
-   "0/difuso"
-   "difuso/0"
-   "Direto"

**Condições de validação:** Qualquer valor, exceto os valores de enumeração listados, é inválido. Essas informações não alterarão o comportamento de processamento da linha de base.

### <a name="rgbprimariesgroup"></a>RGBPrimariesGroup

Esse elemento é uma sequência de

1.  WhitePrimary NonNegativeXYZType
2.  RedPrimary NonNegativeXYZType
3.  GreenPrimary NonNegativeXYZType
4.  BluePrimary NonNegativeXYZTYpe
5.  BlackPrimary NonNegativeXYZType

**Condições de validação:** A ser determinado com os comentários do setor.

### <a name="nonnegativecmyksampletype"></a>NonNegativeCMYKSampleType

Esse elemento é uma sequência de

1.  CMYK NonNegativeCMYKType
2.  CIEXYZ NonNegativeXYZType

O elemento também tem uma cadeia de caracteres de marca de atributo opcional

**Condições de validação:** A ser determinado com os comentários do setor.

### <a name="nonnegativergbsampletype"></a>NonNegativeRGBSampleType

Esse elemento é uma sequência de

1.  RGB NonNegativeRGBType
2.  CIEXYZ NonNegativeXYZType

O elemento também tem uma cadeia de caracteres de marca de atributo opcional

**Condições de validação:** A ser determinado com os comentários do setor.

### <a name="nonnegativecmyktype"></a>NonNegativeCMYKType

Esse elemento que consiste em atributos

1.  Float C
2.  M float
3.  Y float
4.  K float

**Condições de validação:** A ser determinado com os comentários do setor.

### <a name="nonnegativergbtype"></a>NonNegativeRGBType

Esse elemento que consiste em atributos

1.  Float do R
2.  G float
3.  B float

**Condições de validação:** A ser determinado com os comentários do setor.

### <a name="extensiontype"></a>Extensiontype

O elemento ExtensionType é uma sequência de qualquer tipo de subconjunto e é usado para informações proprietárias de aplicativos que não são da Microsoft.

**Condições de validação:** Esse elemento é opcional. Pode haver um máximo de 1.000 subconjunto de extensão.

### <a name="nonnegativexyztype"></a>NonNegativeXYZType

O elemento NonNegativeXYZType é composto por NonNegativeFloatType três elementos de ponto flutuante IEEE de precisão simples chamados "X", "Y" e "Z". Esses valores são limitados aos valores de medição de perfis DMP. Essas medidas podem ser valores absolutos (não relativos) CIEXYZ 1931 reflexivos ou valores absolutos (não relativos) CIEXYZ 1931 diretos (transmissivos) em candelas por unidades quadradas de medidor.

**Condições de validação:** Somente valores do mundo real são válidos e os valores de medição CIEXYZ negativos são inválidos. Como esses são valores absolutos, os valores podem ser maiores que 1,0f. Um limite razoável para qualquer "X", "Y" ou "Z". value é arbitrariamente definido como 10000.0f.

### <a name="xyztype"></a>XYZType

O elemento XYZType é composto por três valores de ponto flutuante IEEE de precisão simples: "X", "Y" e "Z".

## <a name="the-cdmp-baseline-algorithms"></a>Os algoritmos de linha de base do CDMP

### <a name="crt-device-model-baseline"></a>Linha de base do modelo de dispositivo CRT

Para entender esse modelo, você deve considerar o processo de operação e a modelagem do dispositivo. No processo de exibição, as medidas XYZ são executadas primeiro nas cores obtidas preenchendo o buffer de exibição de um dispositivo de exibição CRT. Os seguintes valores de exemplo gerarão dados bons para o modelo de dispositivo CRT de linha de base:

Vermelho: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Verde: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Azul: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutros: R = G= B = 0, 8, 16, 32, 64, 128, 192, 255

Incrementos que não sejam 15 e incrementos nãolinear também podem ser usados. Cada rampa vermelha, verde, azul e neutra deve conter pelo menos três amostras, mas é recomendável fornecer mais amostras. Você deve fornecer exemplos para vermelho puro, verde, azul, preto e branco. Os exemplos não devem ter um espaço uniforme.

O processo de criação da matriz tristimulus consiste em duas etapas. Primeiro, es estimar o valor XYZ de ponto preto ou a pasta. Esta etapa baseia-se em grande parte no trabalho do Berns 3 com uma função de objetivo ligeiramente \[ \] modificada para a otimização nãolinear. Em segundo lugar, calcule a matriz de trístimulo com base no resultado da etapa um e também de um cálculo de média em todas as medidas por canal, não apenas aquela para a contagem digital máxima.

Cada uma dessas etapas contém procedimentos detalhados. O ponto de partida são as rampas (17 etapas em nosso exemplo) para cada um dos canais R, G e B. Quando as medidas XYZ são plotados no plano *xy* de chromaticity, uma situação típica é mostrada na Figura 1. A etapa um consiste em resolver um problema de otimização não linhar para encontrar o ponto preto "mais adequado" que minimizará o desnquivamento na chromaticidade conforme um percorre os canais R, G e B. Com base no Berns \[ \] 3, buscamos ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z <sub>K</sub>* ) que minimiza a seguinte função de objetivo:

![Mostra a função de objetivo em que Sr, Sg e Sb são o conjunto de pontos de dados nos canais R, G e B.](images/cdmp-formula1.png)

em *que S <sub>R,</sub>**S <sub>G</sub>* e *S <sub>B</sub>* são o conjunto de pontos de dados correspondentes aos pontos nos canais R, G e B. Para qualquer *conjunto S,* defina:

![Mostra uma fórmula para definir qualquer conjunto S.](images/cdmp-formula2.png)

No anterior, \| *S* \| é a cardinalidade de *S,* ou seja, o número de pontos no conjunto *S.* ![ Mostra uma fórmula para a chromaticidade de um ponto.](images/cdmp-formula3.png) é as coordenadas de chromaticity do ponto ![ Mostra uma formaula para um ponto.](images/cdmp-formula4.png) , então Mostra uma fórmula para a média ou o centro de massa. , é a média, ou o centro de massa, de todos os pontos no conjunto S no plano ![ ](images/cdmp-formula5.png) de chromaticity.  Portanto, ![ Mostra uma fórmula para a soma de um segundo momento de pontos.](images/cdmp-formula6.png) é a soma dos segundos momentos dos pontos sobre o centro de massa e é uma medida de como os pontos são distribuídos sobre ele. Por fim, ![ mostra uma fórmula para a medida total da propagação de três clusters de pontos.](images/cdmp-formula7.png) é uma medida total de como os três clusters de pontos são distribuídos sobre seus respectivos centros de massa.

No cálculo de ![ Mostra uma fórmula de f(X,Y,Z; Xk, Yk, Zk).](images/cdmp-formula8.png) , se Mostrar uma fórmula para X. , o cálculo será ![ ignorado e a ](images/cdmp-formula9.png) cardinalidade de *S* será ajustada de acordo.

Apesar da complexidade aparente da função de objetivo, é uma soma dos quadrados de muitas funções diferentes em *X <sub>K</sub>*,*Y <sub>K</sub>Z <sub>K K</sub>* (17 pontos 2 *xy* -components 3 canais = 102, no exemplo) e, portanto, é amenizável a técnicas padrão de quadrados mínimos, como o algoritmo Levenberg-Marquardt, que é o algoritmo usado no WCS. Observe que a função de objetivo anterior é diferente da sugerida em Berns 3, na medida em que a última função mede a variação das distâncias do centro de massa, de modo que a variação seja zero quando os pontos são \[ equidistantes do centro de massa, mesmo que possam se propagar um pouco sobre \] ela. No exemplo, a dispersão de pontos é contolda diretamente usando os segundos instantes.

Assim como com qualquer algoritmo iterativo para o problema de quadrados mínimos nãolinear, Levenberg-Marquardt requer uma estimativa inicial. Há dois candidatos óbvios. Um é (0, 0, 0); o outro é o ponto preto medido. Para a CTE, o ponto preto medido é usado primeiro como a estimativa inicial. Se um máximo de 100 ierções for excedido sem atingir um limite de uma distância média de 0,001 de cada ponto do centro de massa (que corresponde a um valor limite de (0,001) 17 3 = 0,000051 para a função de objetivo), outra rodada de ierações com a estimativa inicial de (0, 0, 0) será executada. A estimativa resultante do ponto preto é XYZ em comparação com a melhor estimativa da rodada anterior de i iterações (com o ponto preto medido como a estimativa inicial). Use a estimativa que fornece o menor valor para a função de objetivo. A escolha de 100 ierções e a distância de erro de 0,001 foram selecionadas empíricamente. Em versões futuras, pode ser razoável parametrizar a distância do erro.

O resultado da etapa um é o ponto preto estimado ( *X <sub>K,</sub>**Y <sub>K,</sub>**Z <sub>K</sub>* ). A etapa dois consiste em determinar a matriz de trístimulo por meio da média da chromaticidade dos pontos nos três clusters obtidos na etapa um. Para CRTs, isso é feito principalmente para minimizar os efeitos dos erros de medição. Os pontos usados na média da chromaticity devem ser os mesmos pontos usados na otimização na etapa um. Em outras palavras, se o primeiro ponto (contagem digital 15, no exemplo) em cada rampa for descartado na etapa de otimização, o mesmo deverá ser feito na média. Se ![ Mostrar fórmulas de chromaticity média para coordenadas nos canais vermelho e verde.](images/cdmp-formula10.png) e ![ Mostra uma fórmula de chromaticity média para coordenadas no canal azul.](images/cdmp-formula11.png) são as coordenadas de chromaticity médias dos canais vermelho, verde e azul e, em seguida, o procedimento a seguir determina a matriz de trístimulo. Primeiro, resolva o sistema linear 3?3:

![Mostra a primeira parte do procedimento para resolver um sistema linear 3?3.](images/cdmp-formula12.png)

![Mostra a segunda parte do sistema linear 3?3.](images/cdmp-formula13.gif)![Mostre o valor b do subscrito t no final da segunda parte do sistema linear 3?3.](images/cdmp-formula14.gif)

*X <sub>W,</sub>**Y <sub>W,</sub>**Z <sub>W</sub>*

![Mostra a parte final do procedimento para resolver um sistema linear 3?3.](images/cdmp-formula15.png)

Depois que a matriz de trístimulo é determinada, a determinação das curvas de tom segue a abordagem padrão. Para exibições de CRT, supõe-se que os canais individuais sigam o modelo "GOG":

![Mostra a fórmula para o modelo 'G O G'.](images/cdmp-formula16.png)

em *que k <sub>g</sub>* é o "ganho",1 -*k <sub>g</sub>* é o "deslocamento" e ? é o "gama". A matriz inversa da matriz de trítulo é aplicada aos dados XYZ dos neutros para obter os dados RGB lineares, que são correlacionados com os valores RGB digitais usando regressão não linear no modelo GOG. Essas características não devem ser as mesmas para os canais R, G e B e geralmente não são as mesmas.

Berns 1 : Princípios de tecnologia de cores de \[ \] *Billria, Billria e Saltzman,* 3 <sub>rd</sub> Ed. John Ltda & Filhos (2000).

Berns 2: Berns eHzh, a função de transferência digital para radiométrica para exibições de CRT controlado \[ \] por computador, o *CIE Expert Symposium '97 Standards For Imaging Technology*, novembro de 1997.

Matheus 3: Matheus, Fernandez e Taplin, Estimando as emissões de Black-Level de exibições do Computer-Controlled, pesquisa de cores e aplicativo \[ \] , 28: 379-383 Periods DeLiney, Inc. (2003) 

Ltd \[ \] 1: Ltd, Color Technology for Electronic *Imaging Devices*, SPIE (1997)

Inscrevah 1: Ltdh, Delle e Berns, uma proposta precisa do monitor CRT (II) para uma extensão para o método CIE e sua \[ \] verificação, *Opt. Rev.* 8: 397-408 (2001)

### <a name="lcd-device-model-baseline"></a>Linha de base do modelo de dispositivo LCD

A linha de base do modelo de dispositivo LCD é semelhante à linha de base do modelo de dispositivo CRT. Esta seção explicará as maneiras pelas quais a modelagem de LCD difere da modelagem CRT.

Uma diferença é que você não pode assumir que as exibições do LCD seguem o modelo gog usado para CRTs e as curvas de tom são obtidas pela interpolação de dados medidos. Por isso, o eixo neutro do dispositivo deve ser amostrado com mais frequência.

Aqui estão alguns valores de exemplo típicos que podem gerar dados bons para a linha de base do modelo de dispositivo LCD:

Vermelho: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Verde: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Azul: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutros: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.

O processo de média de chromaticies de cores medidas para obter as chromaticities para os primários do dispositivo é mais crítico para LCDs do que para CRTs. Quando as medidas XYZ são plotados no plano *xy* de chromaticity, uma situação típica é mostrada na Figura 1. Observe como a chromaticidade se desirói para o ponto preto. Isso ocorre porque todos os LCDs têm uma determinada quantidade de vazamento de luz.

![Diagrama que mostra um grafo da chromaticity usando dados brutos sem correção.](images/cdmp-lcd-dmp-figure1.png)

**Figura 1:** o diagrama de chromaticity usando dados brutos sem correção

Quando isso é subtraído das medidas XYZ brutas, uma situação típica é descrita na Figura 2. Os pontos agora estão clusterados em cerca de três centros, embora eles não se enquadram de forma idêntica neles. O processo de média descrito para CRTs melhora muito os resultados para LCDs.

![Diagrama que mostra um grafo da chromaticity usando dados brutos com um ponto preto ajustado.](images/cdmp-lcd-dmp-figure2.png)

**Figura 2:** o diagrama de chromaticity usando dados com ponto preto ajustado

### <a name="rgb-capture-device-model-baseline"></a>Linha de base do modelo de dispositivo de captura RGB

O modelo de dispositivo de captura RGB de linha de base é uma subclasse da classe IDeviceModel. Na colorimétrica de dispositivos de captura de cores, como scanners e câmeras digitais, a abordagem a seguir é usada. Um destino que consiste em patches de cores com valores CIEXYZ conhecidos é capturado usando o dispositivo de captura. O resultado da captura é uma imagem de bitmap RGB na qual a cor de cada patch é codificada em um valor RGB. Esses valores RGB do dispositivo são específicos para um dispositivo de captura específico. O objetivo da colorimétrica é estabelecer uma relação empírica entre os valores RGB do dispositivo e os valores CIEXYZ, ou uma transformação matemática de RGB para XYZ que modela com a maior precisão possível o comportamento do dispositivo de captura.

Essa transformação matemática pode ser modelada razoavelmente por polinomiais de graus baixos. Este procedimento é detalhado na livros de letras, por exemplo, Entre \[ 92 \] e \[ Milão 97. \] Em Ltd 97, uma abordagem é relatada que usa um conjunto de três \[ \] polinomiais com 3, 6, 8, 9, 11, 14 ou 20 termos nas variáveis R, G e B, enquanto os três polinomiais regredim, respectivamente, aos componentes X, Y, Z do espaço CIEXYZ. Para o polinomial de 20 termos, o formulário é:

![Mostra o polinomial de 20 termos.](images/cdmp-formula20.png)

Há expressões semelhantes para Y e Z. A técnica matemática para ajustar os polinomiais se enquadra em "Regressão Linear Multivariada" e é descrita em qualquer texto elementar em Estatísticas.

Esse método de regressão linear não minimiza a função de objetivo "correta". Por design, a regressão linear localiza a solução de mínimos quadrados, o que implica que os coeficientes obtidos minimizarão a soma total de quadrados de erros no espaço subjacente ou, equivalentemente, a soma de quadrados das distâncias euclidianas. Na prática, você deseja minimizar a soma de quadrados de ? Es, em que ? E é um dos padrões aceitos, como CIE94. Minimizar essa função de objetivo é um problema de regressão não linear.

No novo mecanismo, Lab to XYZ é o espaço de cores do CIE que é regredido e o polinomial cúbico de 20 termos é usado como o modelo para o dispositivo de captura ou coeficientes ls, como, bs, de forma que os polinomiais a seguir minimizem a soma de quadrados de ? E <sub>CIE94</sub> s.

![Mostra um conjunto de fórmulas polinomiais.](images/cdmp-formula21.png)

A solução ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) no espaço numérico real 60 **R** 203 deve ser tal que o seguinte erro total seja minimizado:

![Mostra o erro total a ser minimizado.](images/cdmp-formula22.png)

em que o resumo é por meio de todos os pares de pontos de dados (*R <sub>i,</sub>**G <sub>i,</sub>**B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* ) no conjunto de dados amostrado mais pontos de controle adicionais a serem detalhados no seguinte. Esse é um problema de regressão não linear porque os parâmetros *?<sub> i</sub>*, *a <sub>i</sub>*, * <sub>i</sub>* enter na função objective de uma maneira nãolinear (não quadrática).

Porque a função objective ? é uma função nãolinear (e nãoquadratic) dos parâmetros *?<sub> i</sub>*, *i <sub>e</sub>* * <sub>i</sub>*, você deve recorrer a técnicas iterativas para resolver o problema de otimização. Como a forma da função de objetivo é uma soma de quadrados, uma técnica de otimização padrão chamada Levenberg-Marquardt algoritmo é usada. Ele é considerado o método de escolha para problemas de quadrados mínimos nãolinear. Para algoritmos iterativos, como Levenberg-Marquardt, você deve fornecer uma estimativa inicial. Uma boa estimativa inicial geralmente é essencial para localizar o valor mínimo correto. Nesse caso, um bom candidato para a estimativa inicial é a solução do problema de regressão linear. Primeiro, minimize a soma do quadrado de distâncias euclidianas no espaço lab, definindo uma função de objetivo quadrática:

![Mostra uma função de objetivo quadrática definida.](images/cdmp-formula23.png)

A solução matemática para esse problema de "quadrados mínimos lineares" é bem conhecida. Por *que ?<sub> i</sub>* aparece apenas na modelagem *L,* *um <sub>i</sub>* aparece apenas na modelagem *u* e * <sub>i</sub>* aparece apenas na *modelagem v;* o problema de otimização pode ser decomposto em três subproblemos: um para *L*, um para *u* e outro para *v*. Considere as *equações de L.* (As *equações u* e *as equações v* seguem exatamente o mesmo argumento.) O problema de minimizar a soma de quadrados de erros em *L* pode ser declarado como resolvendo a seguinte equação de matriz no sentido mínimo quadrado:

![Mostra uma equação de matriz para L.](images/cdmp-formula24.png)

em *que N* é o número total de pontos de dados (pontos de amostra originais mais pontos de controle criados de uma maneira descrita abaixo). Normalmente, *N é* muito maior que 20, portanto, a equação anterior é determinada em excesso, exigindo uma solução com menos quadrados. Uma solução de formulário fechado para **?** está disponível:

![Mostra uma solução de formulário fechado.](images/cdmp-formula25.png)

Na prática, a avaliação direta usando a solução de formulário fechado não é usada porque tem propriedades numéricas ruins. Em vez disso, algum tipo de algoritmo de fatorização de matriz é aplicado à matriz de coeficientes, o que reduz o sistema de equações a uma forma canônica. Na implementação atual, a Decomposição de Valor Singular (SVD) é aplicada à matriz **R** e, em seguida, o sistema decomposto resultante é resolvido.

A solução para o problema de regressão linear, anotada por ![ Mostra a solução para o problema de regressão linear.](images/cdmp-formula26.png) , é usado como o ponto de partida do Levenberg-Marquardt algoritmo. Nesse algoritmo, é calculada uma etapa de avaliação que deve mover o ponto para mais perto da solução ideal. A etapa de avaliação satisfaz um conjunto de equações lineares dependentes do valor funcional e dos valores dos derivados no ponto atual. Por esse motivo, os derivados da função objective ? em relação aos parâmetros *?<sub> i</sub>*, *a <sub>i</sub> <sub>i</sub>* são entradas necessárias para o Levenberg-Marquardt algoritmo. Embora haja 60 parâmetros, há um atalho que permite calcular muito menos. Pela Regra de Cadeia de Cálculos,

![Mostra uma equação que permite um atalho usando a Regra de Cadeia de Cálculo.](images/cdmp-formula27.png)

em *que j* = 1, 2, , 20, L *<sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* são o valor CIELAB do *iº* ponto de exemplo e *R <sub>ij</sub>* é a entrada (*i*,*j* )th da matriz **R** definida acima. Portanto, em vez de computar derivados para 60 parâmetros, você pode computar derivados para *L,**a* e *b* usando diferenciação de avanço numérico.

Também é necessário configurar um critério de interrupção para algoritmos iterativos. Na implementação atual, as ierações serão encerradas se a média quadrada DECIE94 for menor que 1 ou se o número de ierções executadas tiver excedido 10. O número 10 vem da experiência prática de que, se as primeiras ierações não reduzirem significativamente o erro, ierações posteriores não ajudarão muito além de mover o ponto de maneira ossiva, ou seja, o algoritmo pode não convergir. Mesmo se o algoritmo diverge, podemos ter certeza de que o DECIE94 não é pior do que o que começamos, ou seja, com os parâmetros obtidos da regressão linear.

Mesmo com o método anterior de regressão não linear, há vários problemas com o ajuste. Um problema é que os polinomiais tendem a ultrapassar ou subfiltrar além dos pontos de dados. Maxima e minima locais artificiais podem ser introduzidos no processo de ajuste. Isso pode ser anulado usando polinomiais de baixo grau, que é o motivo pelo qual você não deve usar mais de três graus. Um aspecto mais sério da superação ou da subfiltração é que, embora um polinomial possa assumir qualquer valor real teoricamente, o espaço que ele tenta modelar normalmente tem restrições físicas e restrições práticas. CIEXYZ deve ter todos X, Y, Z não negativos, que é uma restrição física. Na prática, eles só têm valores na magnitude de centenas, não milhares ou superiores. Da mesma forma, o CIELAB ou o CIELUV tem suas próprias restrições físicas e práticas. Quando o espaço RGB é preenchido suficientemente com pontos de exemplo, o problema de superação ou de subfiliação não é sério. No entanto, os pontos RGB capturados do dispositivo de captura geralmente não preenchem o espaço RGB uniformemente. Os pontos podem preencher apenas os 80% internos do cubo RGB ou, pior ainda, eles podem residir em uma variedade dimensional inferior. Quando isso acontece, os polinomiais regressados podem fazer um trabalho ruim ao extrapolar os valores além dos pontos de dados, às vezes retornando previsões irreais. Você deseja um modelo que sempre retorna valores razoavelmente realistas. Isso requer um método que possa controlar efetivamente o comportamento de limite dos polinomiais de regressão impondo custo adicional para esses polinomiais que se comportam de maneira desastante perto do limite do cubo RGB. Uma medida posterior para garantir que os polinomiais sempre retornem valores realistas é aplicada ao recorte da saída para dentro do locus espectral do CIE.

É neste ponto que a modelagem do scanner e a modelagem da câmera divergem entre si. Espera-se que o modelo de câmera seja extrapolado para regiões além dos pontos amostrados, incluindo os "destaques especulares", a mesma extrapolação não é necessária para o modelo de scanner. Espera-se que o destino do verificador cobre uma imagem semelhante aos materiais impressos a serem verificados. O modelo do scanner ainda é necessário para ser robusto no sentido de que ele não deve retornar valores irreais, mas a extrapolação muito além do destino de estrutura não é necessária. Para garantir a robustez, o L-polynomial acima é recortado em 100, ou seja, o modelo polinomial é forçado a não extrapolar além de "Dmin" do destino do scanner.

O modelo de câmera deve extrapolar para realças especular, portanto, o recorte em 100 é indesejável. Em vez disso, o algoritmo a seguir é usado.

Os pontos de controle artificial são introduzidos para controlar o comportamento dos polinomiais em regiões com amostragem insuficiente. Ao colocar estrategicamente esses pontos de controle com valores apropriados, eles servem para "efetuar pull" dos polinomiais na direção necessária. Na implementação atual, oito pontos de controle correspondentes aos cantos do cubo RGB são usados. Se os valores do dispositivo são normalizados para unity, esses pontos são:

*R* = 0, *G* = 0, *B* = 0

*R* = 0, *G* = 0, *B* = 1

*R* = 0, *G* = 1, *B* = 0

*R* = 0. *G* = 1, *B* = 1

*R* = 1, *G* = 0, *B* = 0

*R* = 1, *G* = 0, *B* = 1

*R* = 1, *G* = 1, *B* = 0

*R* = 1, *G* = 1, *B* = 1

Com exceção do *R* G B = 1 branco, que está associado a um valor  =   =  CIELAB de *L* = 100, *u* v = 0, o algoritmo de extrapolação a seguir é usado para determinar o valor  =  CIELAB apropriado a ser associado. Geralmente, para um determinado (*R,**G*,*B* ), um peso é associado a cada um dos (*R <sub>i,</sub>**G <sub>i</sub>*,*B <sub>i</sub>* ) no conjunto de dados amostrado. Há duas metas para atribuir o peso. Primeiro, o peso é inversamente proporcional à distância entre (*R,**G*,*B* ) e (*R <sub>i,</sub>**G <sub>i</sub>*,*B <sub>i</sub>* ). Em segundo lugar, você deseja descartar ou atribuir peso 0 a pontos que têm um matiz diferente do ponto determinado (*R,**G,**B* ). Para levar em conta o matiz, considere os pontos que estão dentro de um cone cujo vértice está em (0, 0, 0), cujo eixo coincide com a junção de linha (0, 0, 0) para (*R,**G*,*B* ) e cujo ângulo semi-vertical ? satisfaz cos ? = 0,9. Consulte a Figura 3 para ver uma ilustração desse cone.

![Diagrama que mostra a forma da região.](images/cdmp-lcd-dmp-figure3.png)

**Figura 3:** Filtrando os pontos de exemplo por ângulo e distância. A forma da região ilustrada é apenas para fins ilustrados. A forma real depende da distância usada; será uma região em forma de losango se a norma 1 for usada.

Dentro desse cone, uma segunda filtragem é executada com base na distância RGB, que usa a norma 1, definida por

![Mostra a fórmula para a segunda filtragem dentro do cone.](images/cdmp-formula28.png)

Com o cone atual, a pesquisa inicial é para pontos que estão dentro de uma distância de 0,1 de (*R,**G,**B* ). Se nenhum ponto for encontrado dentro desse raio, o raio será aumentado em 0,1 e a pesquisa será reiniciada. Se a próxima rodada também não tiver nenhum ponto, o raio será aumentado em 0,1. Esse processo continua até que o raio exceda MaxDist/5, em que MaxDist = 3, no caso de 1 norma. Se nenhum ponto for encontrado, o cone será ampliado diminuindo o cos ? por 0,05, ou seja, aumentando o ângulo ? e reiniciando todo o processo com um raio crescente. Esse processo continua até que um conjunto não vazio de pontos seja encontrado ou cos ? atinge 0, ou seja, o cone se abriu para se tornar um plano. Neste ponto, a pesquisa é reiniciada aumentando o raio, exceto que a pesquisa continua até que o raio atinja MaxDist. Isso garante que, no pior cenário, um conjunto de pontos não vazio seja encontrado. O algoritmo é resumido no diagrama de fluxo na Figura 4.

![Diagrama que mostra o fluxo do algoritmo.](images/cdmp-lcd-dmp-figure4.png)

**Figura 4:** Flow diagrama para determinar o conjunto S de pontos de exemplo usados na extrapolação para um valor RGB de entrada

Supondo que o processo anterior produza um *conjunto não* vazio S de pontos (*R <sub>i,</sub>**G <sub>i</sub>*,*B <sub>i</sub>* ) e correspondente (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), então, para cada ponto, um peso *w <sub>i</sub>* é atribuído, dado por

![Mostra a fórmula para um peso para cada ponto.](images/cdmp-formula29.png)

Por fim, o extrapolante é definido por

![Mostra a definição do extrapolante.](images/cdmp-formula30.png)

As equações anteriores constituem uma instância dos "métodos ponderados de distância inversa", normalmente chamados de métodos DeIa. Ao executar cada um dos oito pontos de eq (6) por meio do algoritmo, oito pontos de controle são obtidos, cada um com os valores *R,**G,**B* e *L*,*a*,*b,* que são colocados no pool com os dados de exemplo originais.

Para garantir que o modelo sempre produza valores de cores válidos e para integridade do sistema e estabilidade em todo o pipeline de processamento de cores, você deve executar um recorte final para a saída do modelo polinomial. A gama visual do CIE é descrita pelo componente acromático (*Y* ou *L* ) e pelo componente chromatic (*xy* ou *a'b',* que estão relacionados ao espaço XYZ por uma transformação projetiva). Na implementação atual, a chromaticity *a'b'* é usada porque está diretamente relacionada ao espaço CIELUV. Para qualquer *valor CIELAB,* primeiro clip *L* para um valor não negativo:

![Mostra o recorte de L para um valor não negativo.](images/cdmp-formula31.png)

Para permitir a extrapolação para realçamentos especular, *L* não é recortado em 100, o limite superior "convencional" para *L* no espaço do laboratório.

Em seguida, *se L* = 0, *a* e *b* são recortados de forma que a =*b =* 0. Se *L* ? 0, calcular

![Mostra a fórmula se L=0.](images/cdmp-formula32.png)

Esses são os componentes de um vetor no diagrama *a'b'* do ponto branco (*u?'*,*v?'* ) para a cor em questão. Defina o locus espectral da CIE como o chassi convexa de todos os pontos (*a'*,*b'* ), parametrizados pelo ?:

![Mostra a fórmula para a mágica.](images/cdmp-formula33.png)

em ![ que mostra as funções para correspondência de cores do CIE.](images/cdmp-formula34.png) são as funções de correspondência de cores do CIE para o observador de 2 graus. Se o vetor estiver fora do locus CIE, a cor será recortada até o ponto no locus CIE que é a interseção do locus e a linha definida pelo vetor. Consulte a Figura 5. Se o recorte tiver ocorrido, *o valor a* e *b* será reconstruído primeiro subtraindo *um?'* e *b?'* do recortado *a'* *e b'* e, em seguida, multiplicando por 13 *L.*

![Diagrama que mostra o grafo do algoritmo de recorte.](images/cdmp-lcd-dmp-figure5.png)

**Figura 5:** Algoritmo de recorte para valores de laboratório que estão fora da gama visual do CIE

Na implementação atual, o locus espectral da CIE no plano *a'b'* é representado por uma curva linear por parte com 35 segmentos (correspondente a um 360 nm a 700 nm inclusivo). Ordenando os segmentos de linha para que seus ângulos subtendido no ponto branco sejam crescentes, o que é equivalente a reticências decrescentes, o segmento de linha que intersecções com o raio formado pelo vetor acima pode ser encontrado por uma pesquisa binária simples.

### <a name="rgb-printer-device-model-baseline"></a>Linha de base do modelo de dispositivo de impressora RGB

Uma estrutura de dispositivo de uma impressora RGB consiste em construir um modelo empírico do dispositivo que prevê a cor CIELUV independente do dispositivo para qualquer valor RGB determinado

Há duas maneiras de construir o modelo empírico. Uma maneira é usar os dados do dispositivo para uma impressora RGB e a outra é usar dados de parâmetro analítico. Na primeira, os dados de medição fornecidos por um usuário para um dispositivo de impressora RGB são usados para construir a LUT (tabela de pesquisa 3D). Os dados de medição consistem em valores XYZ para patches RGB com amostra uniforme. Os tamanhos de amostragem típicos são 9 ou 17 para cada componente. Cada patch é medido com um colorimeter ou umphotometer no espaço CIEXYZ. O valor XYZ de um patch é convertido em valor CIELUV, formar um LUT 3D. No modelo de dispositivo, o método de interpolaçãohedral de Sakaelo é aplicado ao LUT 3D para prever os dados CIELUV para determinados dados RGB. (Confer US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakaaka), Ltd \[ 1 \] . As duas patentes mencionadas expiraram.). Os dados de parâmetro analítico passados no segundo método são simplesmente um LUT criado anteriormente. Normalmente, esse LUT foi criado usando o primeiro método, embora possa ser criado manualmente.

No gerenciamento de cores atual, o source map é definido como o mapa que vai do espaço RGB para um espaço de cores CIEXYZ independente do dispositivo. O mapa de destino é definido como o mapa que vai do espaço de cores CIEXYZ independente do dispositivo para o espaço RGB. É o inverso da source map.

O modelo empírico é usado diretamente no source map. Primeiro, ele mapeia determinados dados RGB em dados CIELUV, que são convertidos em dados XYZ. No mapa de destino, os dados CIEXYZ independentes de dispositivo são convertidos primeiro em dados CIELUV. Em seguida, o modelo empírico e o método Newton-Raphson clássico são usados para prever os melhores dados RGB para os dados CIELUV. Os detalhes sobre a conversão de dados CieLUV para RGB são os seguinte:

Depois de gerar um LUT 3D de RGB para CieLUV, o mapa de RGB para LUV é criado usando interpolação dehedral em RGB. Esse mapa é anotado pelas seguintes equações:

![Mostra as equações do mapa de R G B para L U V.](images/cdmp-image125.png)

A inversão do mapa consiste em resolver, para qualquer cor ![Mostra o L U V.](images/cdmp-image127.png) , o seguinte sistema de equações não lineares:

![Mostra as equações não lineares para a lvagem de qualquer L U V de cor.](images/cdmp-image129.png)

Uma equação não linear baseada no método Newton-Raphson clássico é usada na nova CTE. Uma estimativa inicial, ou *a priori,* <sub>s</sub> priori see, s prior -(R 0, G 0, B 0 ) é obtida pesquisando por meio de uma "matriz de semente" que consiste em uma grade uniforme 8x8x8 de pares pré-computados (RGB,Luv). O Luv correspondente RGB que está mais próximo do L \* u \* v é \* escolhido. Cada ponto na matriz de semente corresponde ao centro de uma célula para que as ierções não comecem com um ponto na face de limite do cubo RGB. Em outras palavras, o RGB das sementes é definido por: STEP = 1/8 s <sub>ijk</sub> = (STEP/2 + (i-1) STEP, STEP/2+(j-1)STEP, STEP/2+(k-1)STEP) com i,j,k = 1...8 Na *iª* etapa de Newton-Jihson, a próxima estimativa Mostra as variáveis para a próxima ![ estimativa.](images/cdmp-image133.png) é obtido pela fórmula:

![Mostra a fórmula para a estimativa.](images/cdmp-image135.png)

A iteração é interrompida quando o erro (distância no espaço CIELUV) é menor que um nível de tolerância pré-definido (0,1 na CTE) ou quando o número de ierções excedeu o número máximo permitido de ierções (10 na CTE). Os valores para a tolerância e o número de i iterações foram determinados empíricamente como efetivos. Em versões futuras, o valor de tolerância pode ser alterado.

A matriz Demiana é calculada usando a diferença de avanço, exceto em um ponto de limite (um ou mais do R, G, B é 1) em que a diferença regressiva é usada em vez disso. Em vez de calcular o inverso da matriz Linear, o sistema linear é resolvido diretamente usando Gauss-Jordan eliminação com pivô completo.

No final das i iterações, a convergência ainda pode não ser alcançada porque Newton-Raphson é um algoritmo "local", ou seja, só funcionará bem se você começar com uma estimativa inicial próxima da solução verdadeira. Se, no final do Newton-Raphson, a convergência dentro da tolerância a erros pré-definida não tiver sido atingida, as ierações serão reiniciadas com um novo conjunto de sementes, definido da seguinte forma.

Por exemplo, a melhor solução obtida até agora é (r, g, b). Dessa solução, N a sementes posteriori são derivadas, em que N = 4. Intuitivamente, a solução é movida "para o centro" em um tamanho de etapa que depende de N. Consulte a Figura 6.

![Diagrama que mostra as instruções de desagregação da solução.](images/cdmp-image136.png)

**Figura 6:** a direção de desagregação da solução depende de em qual octante ela está.

Em outras palavras, se r 0,5, o valor no canal R será reduzido, caso &gt; contrário, o valor será aumentado. Há uma lógica semelhante para os canais G e B. As definições precisas são:

FORÇAÇÃO = 0,5/(N+1)

Dir(r) = -1 se r &gt; 0,5; +1 caso contrário. Da mesma forma para Dir(g) e Dir(b)

O jth a posteriori seed, s ????, is (r + Dir(r) \* \* jVATION, g + Dir(g) \* \* jVATION, b + Dir(b) \* j \* GATION)

Experimente o primeiro ???? e se ele fornece uma nova solução dentro da tolerância a erros, você pode parar. Caso contrário, tente o segundo ???? e assim por diante até o Nº ????.

Os esquemas de todo o algoritmo são mostrados na Figura 7.

![Diagrama que mostra o fluxo para inverter o modelo de dispositivo.](images/cdmp-image138.png)

**Figura 7:** Esquemas de inversão do modelo de dispositivo

### <a name="rgb-virtual-device-model-baseline"></a>Linha de base do modelo de dispositivo virtual RGB

Esse DM (modelo de dispositivo) é um algoritmo simples de reprodução de matriz/tom. A matriz é derivada do ponto em branco e principalmente do uso de algoritmos de ciência de cores padrão. A curva de reprodução de tom é derivada dos parâmetros de medida de acordo com as descrições de ICC de CurveType e ParametricType (ou invertida conforme necessário). Detalhes dos algoritmos internos serão fornecidos após a validação adicional de problemas de alto intervalo dinâmico.

O modelo de dispositivo virtual RGB é uma curva RGB de reprodução de matriz/tom semelhante ao design de perfil baseado em matriz de três componentes do ICC. Os parâmetros de "medida virtual" da DM incluem um valor de ponto em branco (CIEXYZ absoluto), valores primários RGB (CIEXYZ absoluto) e uma curva de reprodução de tom baseada no ICC ParametricCurveType e CurveType na formatação XML consistente com os esquemas DMP.

A codificação de tipo de função ICC parametricCurveType e o suporte correspondente em IRGBVirtualDeviceModelBase são mostrados na tabela a seguir.



| Tipo de função                                         | Parâmetros                          | Tipo                                     | Observação                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![Mostra a função 'GammaType'.](images/cdmp-image154.png)<br/> | g<br/>              | GammaType<br/>                 | Implementação comum<br/>           |
| ![Mostra a função 'GammaOffsetGainType'.](images/cdmp-image156.png)<br/> | ga b<br/>           | GammaOffsetGainType<br/>       | CIE 122-1966<br/>                    |
| ![Mostra a função 'GammaOffsetGainOffsetType'.](images/cdmp-image158.png)<br/> | ga b c<br/>         | GammaOffsetGainOffsetType<br/> | IEC 61966-3<br/>                     |
| ![Mostra a função 'GammaOffsetGainGainType'.](images/cdmp-image160.png)<br/> | ga b c d<br/>       | GammaOffsetGainGainType<br/>   | IEC 61966-2.1<br/> (sRGB)<br/> |
| ![Mostra uma função para os parâmetros 'g a b c d e f'.](images/cdmp-image162.png)<br/> | ga b c d e f<br/>   | N/D<br/>                       | Sem suporte no WCS<br/>            |



 

A curva de tom para dispositivos virtuais RGB é aplicada em DeviceToColorimetric entre os dados de entrada, pDeviceColors e a multiplicação de matriz. Para ColorimetricToDevice, um método deve ser usado para inverter a curva de tom. Na implementação da linha de base, isso é feito pela interpolação direta na mesma curva de tom usada para DeviceToColorimetric.

As curvas devem ser especificadas nos perfis como pares de números no espaço flutuante. O primeiro número representa valores em pDeviceColors. O segundo número representa a saída da curva de tom. Todos os valores na curva de tom devem estar entre minColorantUsed e maxColorantUsed. As curvas de tom devem conter pelo menos duas entradas: uma para minColorantUsed e outra para maxColorantUsed. O número máximo de entradas no ToneCurve é 2048. Em geral, quanto mais entradas na tabela, mais precisamente você pode modelar a curvatura. Uma interpolação linear por parte é executada entre as entradas.

Você pode considerar métodos de interpolação alternativos. Se você sabe algo sobre o comportamento subjacente do dispositivo, pode usar menos amostras e modelo com mais precisão com uma curva de ordem mais alta. Mas se você usar o tipo de curva errado, será muito impreciso. Sem mais informações, não é possível adivinhar o tipo de curva. Portanto, use a interpolação linear e forneça muitos pontos de dados.

### <a name="cmyk-printer-device-model-baseline"></a>Linha de base do modelo de dispositivo de impressora CMYK

Uma estrutura de dispositivo de uma impressora CMYK consiste em construir um modelo empírico do dispositivo que prevê a cor impressa para qualquer valor cmYK determinado. A meio também inclui a inversão desse modelo para que seja possível dar uma amostra do valor do CMYK para uma determinada cor a ser impressa. Normalmente, isso é definido em termos de valor CIEXYZ ou CIELAB.

Normalmente, um destino IT8.7/3 que contém patches CMYK é usado. Os patches consistem na amostragem do espaço do CMYK de maneira bem definida para que uma grade retangular (com espaçamento não uniforme em C, M, Y e K) seja formada. Cada patch é então medido com um colorimeter ou umphotometer. As medidas em valores CIEXYZ formam uma LUT (tabela de pesquisa), da qual um modelo empírico da impressora é criado usando o método de interpolação de Sakaakaaka. Us Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakaaka), Ltd \[ 1 \] . As duas patentes mencionadas expiraram.

Os requisitos específicos para os exemplos de medida do CMYK necessários para um perfil de modelo de dispositivo serem aceitos como válidos pelo modelo de dispositivo de linha de base da impressora CMYK são os procedimentos a seguir. (O conjunto de exemplos é descrito mais claramente como um conjunto de cubos de exemplo do CMY, cada um associado a um nível K específico.)

-   No mínimo, os cubos CMY válidos devem ser fornecidos para os níveis K = 0 e K = 100.
-   Os níveis intermediários de K podem ter espaço não uniforme.
-   Qualquer nível de K intermediário sem um cubo CMY válido será ignorado.
-   Os cubos CMY podem usar intervalos de exemplo não uniformes (espaçamento de grade), mas o mesmo conjunto de intervalos de exemplo deve ser usado em todas as dimensões C, M e Y no cubo CMY para um determinado nível K.
-   Cada cubo CMY de nível K pode usar um número diferente e espaçamento de intervalos de exemplo.
-   Todos os cubos CMY devem conter os "cantos" do cubo CMY, ou seja, amostras de CMY \[ em 0,0,0 \] , \[ 0,0,100 \] , \[ 0,100,0 \] , \[ 100,0,0 \] , \[ 0.100.100 \] , \[ 100,0.100 \] , \[ 100.100, 0 \] , \[ 100.100.100 \] .
-   Todos os níveis intermediários de grade CMY devem ser totalmente amostrados em cada canal. Em outras palavras, um exemplo deve existir em cada interseção de grade 3D dentro do cubo CMY.
-   Para os cubos K = 0 e K = 100 CMY, os cubos "somente cantos" 2x2x2 são o mínimo aceito como válido.

    \[OBSERVAÇÃO: para níveis K=0 e K=100, um cubo CMY 3x3x3 será processado como um cubo "somente cantos" 2x2x2; o nível de exemplo intermediário é ignorado. 4x4x4 e cubos maiores terão todos os exemplos na grade usados.\]

-   Para níveis de K intermediários, cubos CMY 4x4x4 são o mínimo aceito como válido.

Um perfil de alta qualidade usará grades de amostragem mais finas do que o mínimo necessário para a validade, geralmente 9x9x9x9 ou superior. Os exemplos dos destinos IT8.7/3, IT8.7/4 e ECI produzem DMPs (perfis de modelo de dispositivo) válidos para o modelo de dispositivo de linha de base da impressora CMYK. Embora esse modelo de dispositivo seja capaz de ignorar as amostras (fora da grade) nesses destinos, não há garantia de que ele seja capaz de fazer isso para outros destinos e, portanto, é recomendável que exemplos externos sejam removidos dos conjuntos de medidas que vão para perfis para esse modelo de dispositivo.

A inversão do modelo de impressora apresenta mais dificuldades. Dada uma cor de entrada no CIECAM, há uma questão de se essa cor está dentro da gama de impressoras. Também há o problema em relação à disposição de pontos no espaço de aparência da cor. Embora possamos organizar os valores do CMYK para se enquadrar em uma grade retangular, como é feito no destino IT8.7/3, o mesmo não pode ser dito das cores impressas resultantes, pois elas são organizadas no espaço de aparência da cor. Em geral, eles são dispersos no espaço de aparência de cor sem nenhum padrão específico.

Geralmente, há duas abordagens para o problema de inversão de pontos dispersos. Uma abordagem é usar uma subdivisão geométrica da gama de impressoras usando sólidos tridimensionais elementares, como ohedra. Uma subdivisão da gama de impressoras no espaço de aparência da cor pode ser deduzida da subdivisão correspondente do espaço CMY(K), consulte Hung \[ 93 \] , Ltd \[ 97 \] . Essa abordagem tem a vantagem da simplicidade computacional. No caso de umhedron, apenas quatro pontos são usados em uma interpolação. Por outro lado, o resultado depende muito de alguns pontos, o que significa que um erro de medição terá um efeito significativo no resultado. O interpolante também tende a não ser tão suave. A segunda abordagem não assume nenhuma subdivisão e se baseia na técnica de interpolação de dados dispersos. Um exemplo clássico é a técnica da interpolação de Interpolação de Interpolação ou do método ponderado inverso (Consulte o exemplo \[ Del 68 \] ). Aqui, vários pontos ao redor do ponto de entrada são escolhidos de alguma maneira, cada um atribuído a um peso, geralmente inversamente proporcional à distância, e o interpolante é levado como a média ponderada dos pontos vizinhos. Nessa abordagem, a escolha de pontos vizinhos é fundamental para o desempenho. Embora poucos pontos possam renderizar os pontos interpolantes imprecisos e não suaves, muitos pontos impõem um alto custo computacional, pois os pesos normalmente são funções não lineares e são custosos de computação.

As duas abordagens descritas acima têm problemas. A abordagem de subdivisão depende fundamentalmente dos dados serem razoavelmente nulos de ruído e, geralmente, o interpolante não é muito suave. A interpolação de dados dispersa é mais tolerante ao ruído de dados e geralmente oferece uma interpolação mais suave, mas é computacionalmente mais cara.

A nova CTE tem uma abordagem alternativa. O dispositivo CMYK é tratado como uma coleção de vários dispositivos CMY, cada um dos quais tem um valor específico de preto (K). Usando um algoritmo de seleção que usa como parâmetros leve e chroma, um nível de preto é escolhido. Os valores de CMY são obtidos por inversão da tabela CMY para Luv correspondente usando os métodos Newton empregados em outro lugar pelo algoritmo de impressora RGB.

Use as etapas a seguir.

1.  Imprima o destino de ção, que é o destino IT8.7/3 ou um destino que contém a amostragem do espaço cmyk em intervalos com espaamento regular ou irregular.
2.  Mede o destino usando umphotometer e converta as medidas em espaço CIELUV.
3.  Construa o mapa de avanço do CMYK para o Luv.
4.  Use o mapa de avanço para construir um conjunto de mapas CMY para Luv para um intervalo de valores K.
5.  Para qualquer valor luv de entrada, o valor de CMYK correspondente é obtido selecionando um dos mapas construídos na etapa 4 acima e invertendo usando o método de Newton para obter um conjunto de cores CMY para acompanhar o valor K selecionado.

As etapas 1 e 2, que são procedimentos padrão, são executadas por um programa de criação de perfil que não faz parte da nova CTE. O destino IT8.7/3 contém uma amostragem razoavelmente detalhada de todos os valores de CMYK em vários níveis de C, M, Y e K. Como alternativa, um destino personalizado com amostragem uniforme dos canais C, M, Y e K pode ser usado. Depois que o destino é impresso, umphotometer ou colorimeter pode ser usado para medir o valor XYZ de cada patch e o valor XYZ pode ser convertido no valor Luv usando o modelo CIELUV.

A etapa 3, a construção do mapa de avanço do CMYK para o Luv, pode ser feita aplicando qualquer técnica de interpolação conhecida, como o método multilinear ouhedral, na grade retangular no espaço do CMYK. Na nova CTE, uma interpolação unidimensional tridimensional é usada. Como as grades de amostragem do CMY geralmente são diferentes em cada nível de K, no entanto, usamos uma técnica de super amostragem, conforme detalhado abaixo. Para um determinado ponto do CMYK, os níveis de K de sanduíche são determinados primeiro com base no valor K. Em seguida, introduza uma "super-grade" em cada nível K que é uma união das grades CMY em cada um dos dois níveis K. Em cada nível K, o valor Luv de qualquer ponto de grade recém-introduzido é obtido por uma interpolação tridimensional tridimensional dentro desse nível K. Por fim, uma interpolação tridimensional unidédral para o ponto específico do CMYK é executada nessa nova grade.

![Diagrama que mostra a superamplagem.](images/cdmp-image163.png)

**Figura 8:** Supersampling

A Etapa 4 constrói um conjunto de LUTs (tabelas de lookup de CMY para Luv). O mapa de avanço construído na Etapa 3 é chamado repetidamente para resamplor o espaço do CMYK. O espaço de cores do CMYK é amostrado usando um espaçamento de K e uma amostragem de CMY diferente, mas ainda com espaçamento de maneira espaçada.

A etapa 5 é um procedimento para obter o valor do CMYK usando os LUTs construídos na Etapa 4 para qualquer ponto Luv de entrada. O valor apropriado de K é escolhido analisando a luz, bem como o grau de cor no Luv solicitado. Depois que a tabela é selecionada, os valores CMY são obtidos da tabela usando o método de Newton (conforme documentado no modelo de dispositivo de impressora RGB anteriormente).

O espaço CIELUV é usado no modelo de impressora em vez de CIEJab porque o modelo de dispositivo deve ser baseado exclusivamente em dados colorimétricos disponíveis no DMP. O DMP contém dados colorimétricos para cada patch medido, incluindo o ponto em branco de mídia, portanto, é possível converter dados CIEXYZ em dados CIELUV. No entanto, não é possível converter em CIECAM02 JCh ou Emia, porque não há acesso às informações de condição de exibição no DMP.

### <a name="rgb-projector-device-model-baseline"></a>Linha de base do modelo de dispositivo projetor RGB

Observação: muitos projetores RGB têm mais de um modo de operação. Em um modo, que geralmente é o padrão e pode ser chamado de algo como "apresentação", a resposta de cor do projetor é otimizada para o brilho máximo. No entanto, nesse modo, o projetor perde a capacidade de reproduzir cores claras e ligeiramente chromatic, como amarelos claros e alguns tons de tonalidade. Em outro modo, geralmente chamado de "filme", "vídeo" ou "sRGB", o projetor é otimizado para reprodução de imagens realistas e cenas naturais. Nesse modo, o brilho máximo é trocado para melhorar a qualidade geral da reprodução de cores. Para obter reprodução de cores satisfatória com projetores RGB, é necessário colocar o projetor em um modo em que uma gama suave de cores possa ser reproduzida.

![Diagrama que mostra um modelo de dispositivo D L P.](images/cdmp-image167.png)

**Figura 9:** Modelo de dispositivo DLP

Um valor RGB de entrada passa por dois caminhos computacionais. O primeiro é o modelo de matriz, que resulta em um valor XYZ. Isso é imediatamente seguido pela conversão de XYZ para Luv. A segunda é a interpolação LUT não uniforme usando interpolação dehedral. A saída da interpolação já está no espaço Luv por construção. As duas saídas são adicionadas para obter o valor de Luv previsto. Por fim, isso é convertido em XYZ, que é a saída esperada do modelo colorimétrico para o dispositivo DLP.

Como os projetores são dispositivos de exibição, eles também suportam a inversão do modelo, ou seja, a transformação de XYZ para RGB. Como o modelo de dispositivo transforma o espaço RGB em espaço XYZ, que são tridimensionais, a inversão é equivalente a resolver três equações não lineares em três desconhecidos. Isso pode ser feito por técnicas de resolução de equações padrão, como Newton-Violahson. No entanto, é preferível primeiro converter XYZ em Luv e, em seguida, inverter a transformação Luv para RGB, porque o espaço Luv é mais perceptualmente linear do que o espaço XYZ.

### <a name="icc-device-model-baseline"></a>Linha de base do modelo de dispositivo ICC

A interoperabilidade de fluxo de trabalho CITE ICC é habilitada criando um perfil de modelo de dispositivo de linha de base de dispositivo ICC especial que armazena o objeto de perfil e cria uma transformação ICC usando um perfil XYZ sem operação. Essa transformação é usada para converter entre as cores do dispositivo e CIEXYZ.

![Diagrama que mostra a interoperabilidade de fluxo de trabalho de C I T E C C.](images/cdmp-image168.png)

**Figura 10:** Interoperabilidade de fluxo de trabalho CITE ICC

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos básicos de gerenciamento de cores](basic-color-management-concepts.md)
</dt> <dt>

[Algoritmos e esquemas do sistema de cores do Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





