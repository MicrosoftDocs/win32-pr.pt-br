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
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a><span data-ttu-id="edc89-118">Esquema e algoritmo de perfil do modelo de dispositivo de cores do WCS</span><span class="sxs-lookup"><span data-stu-id="edc89-118">WCS Color Device Model Profile Schema and Algorithms</span></span>

<span data-ttu-id="edc89-119">Este tópico fornece informações sobre o esquema de perfil de modelo de dispositivo de cores WCS e seus algoritmos associados.</span><span class="sxs-lookup"><span data-stu-id="edc89-119">This topic provides information about the WCS Color Device Model Profile Schema and its associated algorithms.</span></span>

<span data-ttu-id="edc89-120">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="edc89-120">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="edc89-121">Visão geral</span><span class="sxs-lookup"><span data-stu-id="edc89-121">Overview</span></span>](#overview)
-   [<span data-ttu-id="edc89-122">Arquitetura do perfil de modelo do dispositivo de cores</span><span class="sxs-lookup"><span data-stu-id="edc89-122">Color Device Model Profile Architecture</span></span>](#color-device-model-profile-architecture)
-   [<span data-ttu-id="edc89-123">O esquema CDMP</span><span class="sxs-lookup"><span data-stu-id="edc89-123">The CDMP Schema</span></span>](#the-cdmp-schema)
-   [<span data-ttu-id="edc89-124">Adição de calibração do WCS CDMP v 2.0</span><span class="sxs-lookup"><span data-stu-id="edc89-124">WCS CDMP v2.0 Calibration Addition</span></span>](#wcs-cdmp-v20-calibration-addition)
-   [<span data-ttu-id="edc89-125">Os elementos do esquema CDMP</span><span class="sxs-lookup"><span data-stu-id="edc89-125">The CDMP Schema Elements</span></span>](#the-cdmp-schema-elements)
    -   [<span data-ttu-id="edc89-126">ColorDeviceModelProfile</span><span class="sxs-lookup"><span data-stu-id="edc89-126">ColorDeviceModelProfile</span></span>](#colordevicemodelprofile)
    -   [<span data-ttu-id="edc89-127">ColorDeviceModel</span><span class="sxs-lookup"><span data-stu-id="edc89-127">ColorDeviceModel</span></span>](#colordevicemodelprofile)
    -   [<span data-ttu-id="edc89-128">NamespaceVersion</span><span class="sxs-lookup"><span data-stu-id="edc89-128">NamespaceVersion</span></span>](#namespaceversion)
    -   [<span data-ttu-id="edc89-129">Versão</span><span class="sxs-lookup"><span data-stu-id="edc89-129">Version</span></span>](#namespaceversion)
    -   [<span data-ttu-id="edc89-130">Documentação</span><span class="sxs-lookup"><span data-stu-id="edc89-130">Documentation</span></span>](#documentation)
    -   [<span data-ttu-id="edc89-131">Elemento CRTDevice</span><span class="sxs-lookup"><span data-stu-id="edc89-131">CRTDevice element</span></span>](#crtdevice-element)
    -   [<span data-ttu-id="edc89-132">Elemento LCDDevice</span><span class="sxs-lookup"><span data-stu-id="edc89-132">LCDDevice element</span></span>](#lcddevice-element)
    -   [<span data-ttu-id="edc89-133">Elemento ProjectorDevice</span><span class="sxs-lookup"><span data-stu-id="edc89-133">ProjectorDevice element</span></span>](#projectordevice-element)
    -   [<span data-ttu-id="edc89-134">Elemento ScannerDevice</span><span class="sxs-lookup"><span data-stu-id="edc89-134">ScannerDevice element</span></span>](#scannerdevice-element)
    -   [<span data-ttu-id="edc89-135">Elemento CameraDevice</span><span class="sxs-lookup"><span data-stu-id="edc89-135">CameraDevice element</span></span>](#cameradevice-element)
    -   [<span data-ttu-id="edc89-136">Elemento RGBPrinterDevice</span><span class="sxs-lookup"><span data-stu-id="edc89-136">RGBPrinterDevice element</span></span>](#rgbprinterdevice-element)
    -   [<span data-ttu-id="edc89-137">Elemento CMYKPrinterDevice</span><span class="sxs-lookup"><span data-stu-id="edc89-137">CMYKPrinterDevice element</span></span>](#cmykprinterdevice-element)
    -   [<span data-ttu-id="edc89-138">Elemento RGBVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="edc89-138">RGBVirtualDevice element</span></span>](#rgbvirtualdevice-element)
    -   [<span data-ttu-id="edc89-139">PlugInDeviceType</span><span class="sxs-lookup"><span data-stu-id="edc89-139">PlugInDeviceType</span></span>](#plugindevicetype)
    -   [<span data-ttu-id="edc89-140">RGBVirtualMeasurementType</span><span class="sxs-lookup"><span data-stu-id="edc89-140">RGBVirtualMeasurementType</span></span>](#rgbvirtualmeasurementtype)
    -   [<span data-ttu-id="edc89-141">Gamatype</span><span class="sxs-lookup"><span data-stu-id="edc89-141">GammaType</span></span>](#gammatype)
    -   [<span data-ttu-id="edc89-142">GammaOffsetGainType</span><span class="sxs-lookup"><span data-stu-id="edc89-142">GammaOffsetGainType</span></span>](#gammaoffsetgaintype)
    -   [<span data-ttu-id="edc89-143">GammaOffsetGainLinearGainType</span><span class="sxs-lookup"><span data-stu-id="edc89-143">GammaOffsetGainLinearGainType</span></span>](#gammaoffsetgainlineargaintype)
    -   [<span data-ttu-id="edc89-144">ToneResponseCurvesType</span><span class="sxs-lookup"><span data-stu-id="edc89-144">ToneResponseCurvesType</span></span>](#toneresponsecurvestype)
    -   [<span data-ttu-id="edc89-145">GamutBoundarySamplesType</span><span class="sxs-lookup"><span data-stu-id="edc89-145">GamutBoundarySamplesType</span></span>](#gamutboundarysamplestype)
    -   [<span data-ttu-id="edc89-146">FloatPairList</span><span class="sxs-lookup"><span data-stu-id="edc89-146">FloatPairList</span></span>](#floatpairlist)
    -   [<span data-ttu-id="edc89-147">CMYKPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="edc89-147">CMYKPrinterMeasurementType</span></span>](#cmykprintermeasurementtype)
    -   [<span data-ttu-id="edc89-148">RGBPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="edc89-148">RGBPrinterMeasurementType</span></span>](#rgbprintermeasurementtype)
    -   [<span data-ttu-id="edc89-149">RGBCaptureMeasurementType</span><span class="sxs-lookup"><span data-stu-id="edc89-149">RGBCaptureMeasurementType</span></span>](#rgbcapturemeasurementtype)
    -   [<span data-ttu-id="edc89-150">OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="edc89-150">OneBasedIndex</span></span>](#onebasedindex)
    -   [<span data-ttu-id="edc89-151">RGBProjectorMeasurementType</span><span class="sxs-lookup"><span data-stu-id="edc89-151">RGBProjectorMeasurementType</span></span>](#rgbprojectormeasurementtype)
    -   [<span data-ttu-id="edc89-152">DisplayMeasurementType</span><span class="sxs-lookup"><span data-stu-id="edc89-152">DisplayMeasurementType</span></span>](#displaymeasurementtype)
    -   [<span data-ttu-id="edc89-153">MeasurementConditionsType</span><span class="sxs-lookup"><span data-stu-id="edc89-153">MeasurementConditionsType</span></span>](#measurementconditionstype)
    -   [<span data-ttu-id="edc89-154">GeometryType</span><span class="sxs-lookup"><span data-stu-id="edc89-154">GeometryType</span></span>](#geometrytype)
    -   [<span data-ttu-id="edc89-155">RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="edc89-155">RGBPrimariesGroup</span></span>](#rgbprimariesgroup)
    -   [<span data-ttu-id="edc89-156">NonNegativeCMYKSampleType</span><span class="sxs-lookup"><span data-stu-id="edc89-156">NonNegativeCMYKSampleType</span></span>](#nonnegativecmyksampletype)
    -   [<span data-ttu-id="edc89-157">NonNegativeRGBSampleType</span><span class="sxs-lookup"><span data-stu-id="edc89-157">NonNegativeRGBSampleType</span></span>](#nonnegativergbsampletype)
    -   [<span data-ttu-id="edc89-158">NonNegativeCMYKType</span><span class="sxs-lookup"><span data-stu-id="edc89-158">NonNegativeCMYKType</span></span>](#nonnegativecmyktype)
    -   [<span data-ttu-id="edc89-159">NonNegativeRGBType</span><span class="sxs-lookup"><span data-stu-id="edc89-159">NonNegativeRGBType</span></span>](#nonnegativergbtype)
    -   [<span data-ttu-id="edc89-160">ExtensionType</span><span class="sxs-lookup"><span data-stu-id="edc89-160">ExtensionType</span></span>](#extensiontype)
    -   [<span data-ttu-id="edc89-161">NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="edc89-161">NonNegativeXYZType</span></span>](#nonnegativexyztype)
    -   [<span data-ttu-id="edc89-162">XYZType</span><span class="sxs-lookup"><span data-stu-id="edc89-162">XYZType</span></span>](#nonnegativexyztype)
-   [<span data-ttu-id="edc89-163">Os algoritmos de linha de base CDMP</span><span class="sxs-lookup"><span data-stu-id="edc89-163">The CDMP Baseline Algorithms</span></span>](#the-cdmp-baseline-algorithms)
    -   [<span data-ttu-id="edc89-164">Linha de base de modelo de dispositivo CRT</span><span class="sxs-lookup"><span data-stu-id="edc89-164">CRT Device Model Baseline</span></span>](#crt-device-model-baseline)
    -   [<span data-ttu-id="edc89-165">Linha de base do modelo de dispositivo LCD</span><span class="sxs-lookup"><span data-stu-id="edc89-165">LCD Device Model Baseline</span></span>](#lcd-device-model-baseline)
    -   [<span data-ttu-id="edc89-166">Linha de base de modelo de dispositivo de impressora RGB</span><span class="sxs-lookup"><span data-stu-id="edc89-166">RGB Printer Device Model Baseline</span></span>](#rgb-printer-device-model-baseline)
    -   [<span data-ttu-id="edc89-167">Linha de base de modelo de dispositivo virtual RGB</span><span class="sxs-lookup"><span data-stu-id="edc89-167">RGB Virtual Device Model Baseline</span></span>](#rgb-virtual-device-model-baseline)
    -   [<span data-ttu-id="edc89-168">Linha de base de modelo de dispositivo de impressora CMYK</span><span class="sxs-lookup"><span data-stu-id="edc89-168">CMYK Printer Device Model Baseline</span></span>](#cmyk-printer-device-model-baseline)
    -   [<span data-ttu-id="edc89-169">Linha de base do modelo de dispositivo do projetor RGB</span><span class="sxs-lookup"><span data-stu-id="edc89-169">RGB Projector Device Model Baseline</span></span>](#rgb-projector-device-model-baseline)
    -   [<span data-ttu-id="edc89-170">Linha de base do modelo de dispositivo ICC</span><span class="sxs-lookup"><span data-stu-id="edc89-170">ICC Device Model Baseline</span></span>](#icc-device-model-baseline)
-   [<span data-ttu-id="edc89-171">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="edc89-171">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="edc89-172">Visão geral</span><span class="sxs-lookup"><span data-stu-id="edc89-172">Overview</span></span>

<span data-ttu-id="edc89-173">Esse esquema é usado para especificar o conteúdo de um perfil de modelo de dispositivo de cor (CDMP).</span><span class="sxs-lookup"><span data-stu-id="edc89-173">This schema is used to specify the content of a color device model profile(CDMP).</span></span> <span data-ttu-id="edc89-174">Os algoritmos de linha de base associados são descritos abaixo.</span><span class="sxs-lookup"><span data-stu-id="edc89-174">The associated baseline algorithms are described below.</span></span>

<span data-ttu-id="edc89-175">O esquema básico do DMP (perfil de modelo de dispositivo) consiste nos dados de medição de amostragem.</span><span class="sxs-lookup"><span data-stu-id="edc89-175">The basic device model profile (DMP) schema consists of the sampling measurement data.</span></span>

<span data-ttu-id="edc89-176">O componente de amostragem do esquema XML do DMP fornece suporte para destinos de medição de cores básicas, concentrando-se em destinos padrão comuns e destinos otimizados para os modelos de dispositivo de linha de base.</span><span class="sxs-lookup"><span data-stu-id="edc89-176">The sampling component of the DMP XML schema provides support for basic color measurement targets, focusing on common standard targets and targets optimized for the baseline device models.</span></span>

<span data-ttu-id="edc89-177">Além disso, o perfil do dispositivo fornece informações específicas sobre o modelo de dispositivo de destino e fornece uma política que o modelo de dispositivo de fallback de linha de base pode usar se o modelo de destino não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="edc89-177">In addition, the device profile provides specific information on the targeted device model and provides a policy that the baseline fallback device model can use if the targeted model is unavailable.</span></span> <span data-ttu-id="edc89-178">As instâncias de perfil podem incluir extensões privadas usando mecanismos de extensão XML padrão.</span><span class="sxs-lookup"><span data-stu-id="edc89-178">The profile instances can include private extensions using standard XML extension mechanisms.</span></span>

## <a name="color-device-model-profile-architecture"></a><span data-ttu-id="edc89-179">Arquitetura do perfil de modelo do dispositivo de cores</span><span class="sxs-lookup"><span data-stu-id="edc89-179">Color Device Model Profile Architecture</span></span>

![Diagrama que mostra as informações que compõem um perfil de modelo de dispositivo.](images/cdmp-image002new.png)

## <a name="the-cdmp-schema"></a><span data-ttu-id="edc89-181">O esquema CDMP</span><span class="sxs-lookup"><span data-stu-id="edc89-181">The CDMP Schema</span></span>


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



## <a name="wcs-cdmp-v20-calibration-addition"></a><span data-ttu-id="edc89-182">Adição de calibração do WCS CDMP v 2.0</span><span class="sxs-lookup"><span data-stu-id="edc89-182">WCS CDMP v2.0 Calibration Addition</span></span>

<span data-ttu-id="edc89-183">O elemento **ColorDeviceModel** do esquema CDMP foi atualizado no Windows 7 para incluir o novo elemento Calibration.</span><span class="sxs-lookup"><span data-stu-id="edc89-183">The **ColorDeviceModel** element of the CDMP schema has been updated in Windows 7 to include the new calibration element.</span></span> <span data-ttu-id="edc89-184">O seguinte mostra a alteração no esquema CDMP.</span><span class="sxs-lookup"><span data-stu-id="edc89-184">The following shows the change to the CDMP schema.</span></span>


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



## <a name="the-cdmp-schema-elements"></a><span data-ttu-id="edc89-185">Os elementos do esquema CDMP</span><span class="sxs-lookup"><span data-stu-id="edc89-185">The CDMP Schema Elements</span></span>

> [!Note]  
> <span data-ttu-id="edc89-186">Primárias são exemplos principais de vermelho, verde, azul, preto e branco.</span><span class="sxs-lookup"><span data-stu-id="edc89-186">Primaries are primary samples of red, green, blue, black, and white.</span></span> <span data-ttu-id="edc89-187">Uma rampa primária é uma rampa de tons de menos luminescência até o valor primário completo.</span><span class="sxs-lookup"><span data-stu-id="edc89-187">A primary ramp is a tonal ramp from least luminance to full primary value.</span></span> <span data-ttu-id="edc89-188">O número máximo de entradas em uma rampa de Tom é 4096.</span><span class="sxs-lookup"><span data-stu-id="edc89-188">The maximum number of entries in a tone ramp is 4096.</span></span>

 

> [!Note]  
> <span data-ttu-id="edc89-189">DMPs são necessários para ter dados de medida.</span><span class="sxs-lookup"><span data-stu-id="edc89-189">DMPs are required to have measurement data.</span></span>

 

### <a name="colordevicemodelprofile"></a><span data-ttu-id="edc89-190">ColorDeviceModelProfile</span><span class="sxs-lookup"><span data-stu-id="edc89-190">ColorDeviceModelProfile</span></span>

<span data-ttu-id="edc89-191">Esse elemento é do tipo ColorDeviceModel.</span><span class="sxs-lookup"><span data-stu-id="edc89-191">This element is of type ColorDeviceModel.</span></span>

<span data-ttu-id="edc89-192">**Condições de validação:** Cada subelemento é validado por seu próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="edc89-192">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="colordevicemodel"></a><span data-ttu-id="edc89-193">ColorDeviceModel</span><span class="sxs-lookup"><span data-stu-id="edc89-193">ColorDeviceModel</span></span>

<span data-ttu-id="edc89-194">Este elemento é uma sequência dos seguintes subelementos</span><span class="sxs-lookup"><span data-stu-id="edc89-194">This element is a sequence of the following sub-elements</span></span>

1.  <span data-ttu-id="edc89-195">Cadeia de caracteres ProfileName,</span><span class="sxs-lookup"><span data-stu-id="edc89-195">ProfileName string,</span></span>
2.  <span data-ttu-id="edc89-196">Cadeia de caracteres de descrição opcional,</span><span class="sxs-lookup"><span data-stu-id="edc89-196">optional Description string,</span></span>
3.  <span data-ttu-id="edc89-197">Cadeia de caracteres de autor opcional,</span><span class="sxs-lookup"><span data-stu-id="edc89-197">optional Author string,</span></span>
4.  <span data-ttu-id="edc89-198">MeasurementConditions MeasurementConditionsType opcional,</span><span class="sxs-lookup"><span data-stu-id="edc89-198">optional MeasurementConditions MeasurementConditionsType,</span></span>
5.  <span data-ttu-id="edc89-199">Self-Luminous booliano,</span><span class="sxs-lookup"><span data-stu-id="edc89-199">Self-Luminous Boolean,</span></span>
6.  <span data-ttu-id="edc89-200">MaxColorant float,</span><span class="sxs-lookup"><span data-stu-id="edc89-200">MaxColorant float,</span></span>
7.  <span data-ttu-id="edc89-201">MinColorant float,</span><span class="sxs-lookup"><span data-stu-id="edc89-201">MinColorant float,</span></span>
8.  <span data-ttu-id="edc89-202">Opção de elementos</span><span class="sxs-lookup"><span data-stu-id="edc89-202">Choice of elements</span></span>
    1.  <span data-ttu-id="edc89-203">CRTDevice,</span><span class="sxs-lookup"><span data-stu-id="edc89-203">CRTDevice,</span></span>
    2.  <span data-ttu-id="edc89-204">LCDDevice,</span><span class="sxs-lookup"><span data-stu-id="edc89-204">LCDDevice,</span></span>
    3.  <span data-ttu-id="edc89-205">RGBProjectorDevice,</span><span class="sxs-lookup"><span data-stu-id="edc89-205">RGBProjectorDevice,</span></span>
    4.  <span data-ttu-id="edc89-206">ScannerDevice,</span><span class="sxs-lookup"><span data-stu-id="edc89-206">ScannerDevice,</span></span>
    5.  <span data-ttu-id="edc89-207">CameraDevice,</span><span class="sxs-lookup"><span data-stu-id="edc89-207">CameraDevice,</span></span>
    6.  <span data-ttu-id="edc89-208">RGBPrinterDevice,</span><span class="sxs-lookup"><span data-stu-id="edc89-208">RGBPrinterDevice,</span></span>
    7.  <span data-ttu-id="edc89-209">CMYKPrinterDevice,</span><span class="sxs-lookup"><span data-stu-id="edc89-209">CMYKPrinterDevice,</span></span>
    8.  <span data-ttu-id="edc89-210">RGBVirtualDevice,</span><span class="sxs-lookup"><span data-stu-id="edc89-210">RGBVirtualDevice,</span></span>
9.  <span data-ttu-id="edc89-211">PlugInDevice,</span><span class="sxs-lookup"><span data-stu-id="edc89-211">PlugInDevice,</span></span>
10. <span data-ttu-id="edc89-212">Extensão opcional ExtensionType</span><span class="sxs-lookup"><span data-stu-id="edc89-212">optional Extension ExtensionType</span></span>

<span data-ttu-id="edc89-213">**Condições de validação:** Cada subelemento é validado por seu próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="edc89-213">**Validation conditions:** Each sub-element is validated by its own type.</span></span> <span data-ttu-id="edc89-214">Os subelementos de cadeia de caracteres têm um máximo de 10.000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="edc89-214">String sub-elements have a maximum of 10,000 characters.</span></span> <span data-ttu-id="edc89-215">O subelemento MaxColorant deve ser maior ou igual a zero (0) e maior que o subelemento MinColorant.</span><span class="sxs-lookup"><span data-stu-id="edc89-215">The MaxColorant sub-element must be greater than or equal to zero (0) and greater than the MinColorant sub-element.</span></span> <span data-ttu-id="edc89-216">O MinColorant pode ser negativo.</span><span class="sxs-lookup"><span data-stu-id="edc89-216">The MinColorant can be negative.</span></span>

### <a name="namespaceversion"></a><span data-ttu-id="edc89-217">NamespaceVersion</span><span class="sxs-lookup"><span data-stu-id="edc89-217">NamespaceVersion</span></span>

<span data-ttu-id="edc89-218">xmlns: CDM = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "</span><span class="sxs-lookup"><span data-stu-id="edc89-218">xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"</span></span>

<span data-ttu-id="edc89-219">targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "</span><span class="sxs-lookup"><span data-stu-id="edc89-219">targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"</span></span>

### <a name="version"></a><span data-ttu-id="edc89-220">Versão</span><span class="sxs-lookup"><span data-stu-id="edc89-220">Version</span></span>

<span data-ttu-id="edc89-221">Versão = "1,0" com o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="edc89-221">Version = "1.0" with Windows Vista.</span></span>

<span data-ttu-id="edc89-222">**Condições de validação:** Qualquer valor &gt; de versão 0,1 ou &lt; = 2,0 é válido para dar suporte a alterações não significativas no formato.</span><span class="sxs-lookup"><span data-stu-id="edc89-222">**Validation conditions:** Any version value &gt;0.1 or &lt;=2.0 is valid to support non-breaking changes to the format.</span></span>

### <a name="documentation"></a><span data-ttu-id="edc89-223">Documentação</span><span class="sxs-lookup"><span data-stu-id="edc89-223">Documentation</span></span>

<span data-ttu-id="edc89-224">Esquema de perfil de modelo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="edc89-224">Device Model Profile schema.</span></span>

<span data-ttu-id="edc89-225">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="edc89-225">Copyright (C) Microsoft.</span></span> <span data-ttu-id="edc89-226">Todos os direitos reservados.</span><span class="sxs-lookup"><span data-stu-id="edc89-226">All rights reserved.</span></span>

### <a name="crtdevice-element"></a><span data-ttu-id="edc89-227">Elemento CRTDevice</span><span class="sxs-lookup"><span data-stu-id="edc89-227">CRTDevice element</span></span>

<span data-ttu-id="edc89-228">Esse elemento é uma sequência de subelementos de um MeasurementData DisplayMeasurementType.</span><span class="sxs-lookup"><span data-stu-id="edc89-228">This element is a sequence of sub-elements of a MeasurementData DisplayMeasurementType.</span></span>

<span data-ttu-id="edc89-229">**Condições de validação:** Cada subelemento é validado por seu próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="edc89-229">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="lcddevice-element"></a><span data-ttu-id="edc89-230">Elemento LCDDevice</span><span class="sxs-lookup"><span data-stu-id="edc89-230">LCDDevice element</span></span>

<span data-ttu-id="edc89-231">Esse elemento é uma sequência de subelementos de um MeasurementData DisplayMeasurementType.</span><span class="sxs-lookup"><span data-stu-id="edc89-231">This element is a sequence of sub-elements of a MeasurementData DisplayMeasurementType.</span></span>

<span data-ttu-id="edc89-232">**Condições de validação:** Cada subelemento é validado por seu próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="edc89-232">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="projectordevice-element"></a><span data-ttu-id="edc89-233">Elemento ProjectorDevice</span><span class="sxs-lookup"><span data-stu-id="edc89-233">ProjectorDevice element</span></span>

<span data-ttu-id="edc89-234">Esse elemento é uma sequência de subelementos de um MeasurementData RGBProjectorMeasurementType.</span><span class="sxs-lookup"><span data-stu-id="edc89-234">This element is a sequence of sub-elements of a MeasurementData RGBProjectorMeasurementType.</span></span>

<span data-ttu-id="edc89-235">**Condições de validação:** Cada subelemento é validado por seu próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="edc89-235">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="scannerdevice-element"></a><span data-ttu-id="edc89-236">Elemento ScannerDevice</span><span class="sxs-lookup"><span data-stu-id="edc89-236">ScannerDevice element</span></span>

<span data-ttu-id="edc89-237">Esse elemento é uma sequência de subelementos de um MeasurementData RGBCaptureMeasurementType</span><span class="sxs-lookup"><span data-stu-id="edc89-237">This element is a sequence of sub-elements of a MeasurementData RGBCaptureMeasurementType</span></span>

<span data-ttu-id="edc89-238">**Condições de validação:** Cada subelemento é validado por seu próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="edc89-238">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="cameradevice-element"></a><span data-ttu-id="edc89-239">Elemento CameraDevice</span><span class="sxs-lookup"><span data-stu-id="edc89-239">CameraDevice element</span></span>

<span data-ttu-id="edc89-240">Esse elemento é uma sequência de subelementos de um MeasurementData RGBCaptureMeasurementType</span><span class="sxs-lookup"><span data-stu-id="edc89-240">This element is a sequence of sub-elements of a MeasurementData RGBCaptureMeasurementType</span></span>

<span data-ttu-id="edc89-241">**Condições de validação:** Cada subelemento é validado por seu próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="edc89-241">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="rgbprinterdevice-element"></a><span data-ttu-id="edc89-242">Elemento RGBPrinterDevice</span><span class="sxs-lookup"><span data-stu-id="edc89-242">RGBPrinterDevice element</span></span>

<span data-ttu-id="edc89-243">Esse elemento é uma sequência de subelementos de um MeasurementData RGBPrinterMeasurementType.</span><span class="sxs-lookup"><span data-stu-id="edc89-243">This element is a sequence of sub-elements of a MeasurementData RGBPrinterMeasurementType.</span></span>

<span data-ttu-id="edc89-244">**Condições de validação:** Cada subelemento é validado por seu próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="edc89-244">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="cmykprinterdevice-element"></a><span data-ttu-id="edc89-245">Elemento CMYKPrinterDevice</span><span class="sxs-lookup"><span data-stu-id="edc89-245">CMYKPrinterDevice element</span></span>

<span data-ttu-id="edc89-246">Esse elemento é uma sequência de subelementos de um MeasurementData CMYKPrinterMeasurementType.</span><span class="sxs-lookup"><span data-stu-id="edc89-246">This element is a sequence of sub-elements of a MeasurementData CMYKPrinterMeasurementType.</span></span>

<span data-ttu-id="edc89-247">**Condições de validação:** Cada subelemento é validado por seu próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="edc89-247">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="rgbvirtualdevice-element"></a><span data-ttu-id="edc89-248">Elemento RGBVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="edc89-248">RGBVirtualDevice element</span></span>

<span data-ttu-id="edc89-249">Esse elemento é uma sequência de subelementos de um RGBVirtualMeasurementDataType.</span><span class="sxs-lookup"><span data-stu-id="edc89-249">This element is a sequence of sub-elements of a RGBVirtualMeasurementDataType.</span></span>

<span data-ttu-id="edc89-250">**Condições de validação:** Cada subelemento é validado por seu próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="edc89-250">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="plugindevicetype"></a><span data-ttu-id="edc89-251">PlugInDeviceType</span><span class="sxs-lookup"><span data-stu-id="edc89-251">PlugInDeviceType</span></span>

<span data-ttu-id="edc89-252">Esse elemento é uma sequência de um GUIDtype GUID e quaisquer subelementos.</span><span class="sxs-lookup"><span data-stu-id="edc89-252">This element is a sequence of a GUID GUIDType and any sub-elements.</span></span>

<span data-ttu-id="edc89-253">**Condições de validação:** O GUID é usado para corresponder ao GUID da dll do plug-in DM.</span><span class="sxs-lookup"><span data-stu-id="edc89-253">**Validation conditions:** The GUID is used to match the DM PlugIn Dll GUID.</span></span> <span data-ttu-id="edc89-254">Há um máximo de 100.000 subelementos personalizados.</span><span class="sxs-lookup"><span data-stu-id="edc89-254">There are a maximum of 100,000 custom sub-elements.</span></span>

### <a name="rgbvirtualmeasurementtype"></a><span data-ttu-id="edc89-255">RGBVirtualMeasurementType</span><span class="sxs-lookup"><span data-stu-id="edc89-255">RGBVirtualMeasurementType</span></span>

<span data-ttu-id="edc89-256">Esse elemento é uma sequência que consiste em</span><span class="sxs-lookup"><span data-stu-id="edc89-256">This element is a sequence consisting of</span></span>

1.  <span data-ttu-id="edc89-257">Grupo de RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="edc89-257">RGBPrimariesGroup group</span></span>
2.  <span data-ttu-id="edc89-258">Uma opção de</span><span class="sxs-lookup"><span data-stu-id="edc89-258">A choice of</span></span>
3.  -   <span data-ttu-id="edc89-259">Gama</span><span class="sxs-lookup"><span data-stu-id="edc89-259">Gamma</span></span>
    -   <span data-ttu-id="edc89-260">GammaOffsetGain</span><span class="sxs-lookup"><span data-stu-id="edc89-260">GammaOffsetGain</span></span>
    -   <span data-ttu-id="edc89-261">GammaOffsetGainLinearGam</span><span class="sxs-lookup"><span data-stu-id="edc89-261">GammaOffsetGainLinearGam</span></span>
    -   <span data-ttu-id="edc89-262">Elementos ToneResponseCurves</span><span class="sxs-lookup"><span data-stu-id="edc89-262">ToneResponseCurves elements</span></span>

4.  <span data-ttu-id="edc89-263">GamutBoundarySamples GamutBoundarySamplesType opcional</span><span class="sxs-lookup"><span data-stu-id="edc89-263">optional GamutBoundarySamples GamutBoundarySamplesType</span></span>
5.  <span data-ttu-id="edc89-264">Carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="edc89-264">TimeStamp dateTime</span></span>

<span data-ttu-id="edc89-265">**Condições de validação:** Cada subelemento desses tipos tem suas próprias condições de validação.</span><span class="sxs-lookup"><span data-stu-id="edc89-265">**Validation conditions:** Each sub-element of these types has its own validation conditions.</span></span>

### <a name="gammatype"></a><span data-ttu-id="edc89-266">Gamatype</span><span class="sxs-lookup"><span data-stu-id="edc89-266">GammaType</span></span>

<span data-ttu-id="edc89-267">Este elemento é um tipo complexo que consiste no atributo</span><span class="sxs-lookup"><span data-stu-id="edc89-267">This element is a complex type consisting of the attribute</span></span>

-   <span data-ttu-id="edc89-268">NonNegativeFloatType gama</span><span class="sxs-lookup"><span data-stu-id="edc89-268">Gamma NonNegativeFloatType</span></span>

<span data-ttu-id="edc89-269">**Condições de validação:** Para ser determinado dos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-269">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gammaoffsetgaintype"></a><span data-ttu-id="edc89-270">GammaOffsetGainType</span><span class="sxs-lookup"><span data-stu-id="edc89-270">GammaOffsetGainType</span></span>

<span data-ttu-id="edc89-271">Este elemento é um tipo complexo que consiste nos atributos</span><span class="sxs-lookup"><span data-stu-id="edc89-271">This element is a complex type consisting of the attributes</span></span>

-   <span data-ttu-id="edc89-272">NonNegativeFloatType gama</span><span class="sxs-lookup"><span data-stu-id="edc89-272">Gamma NonNegativeFloatType</span></span>
-   <span data-ttu-id="edc89-273">NonNegativeFloatType de deslocamento</span><span class="sxs-lookup"><span data-stu-id="edc89-273">Offset NonNegativeFloatType</span></span>
-   <span data-ttu-id="edc89-274">Obter NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="edc89-274">Gain NonNegativeFloatType</span></span>

<span data-ttu-id="edc89-275">**Condições de validação:** Para ser determinado dos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-275">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gammaoffsetgainlineargaintype"></a><span data-ttu-id="edc89-276">GammaOffsetGainLinearGainType</span><span class="sxs-lookup"><span data-stu-id="edc89-276">GammaOffsetGainLinearGainType</span></span>

<span data-ttu-id="edc89-277">Este elemento é um tipo complexo que consiste nos atributos</span><span class="sxs-lookup"><span data-stu-id="edc89-277">This element is a complex type consisting of the attributes</span></span>

-   <span data-ttu-id="edc89-278">NonNegativeFloatType gama</span><span class="sxs-lookup"><span data-stu-id="edc89-278">Gamma NonNegativeFloatType</span></span>
-   <span data-ttu-id="edc89-279">NonNegativeFloatType de deslocamento</span><span class="sxs-lookup"><span data-stu-id="edc89-279">Offset NonNegativeFloatType</span></span>
-   <span data-ttu-id="edc89-280">Obter NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="edc89-280">Gain NonNegativeFloatType</span></span>
-   <span data-ttu-id="edc89-281">LinearGain NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="edc89-281">LinearGain NonNegativeFloatType</span></span>
-   <span data-ttu-id="edc89-282">TransitionPoint NonNegativeFloatType.</span><span class="sxs-lookup"><span data-stu-id="edc89-282">TransitionPoint NonNegativeFloatType.</span></span>

<span data-ttu-id="edc89-283">**Condições de validação:** Para ser determinado dos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-283">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="toneresponsecurvestype"></a><span data-ttu-id="edc89-284">ToneResponseCurvesType</span><span class="sxs-lookup"><span data-stu-id="edc89-284">ToneResponseCurvesType</span></span>

<span data-ttu-id="edc89-285">Este elemento é uma sequência de</span><span class="sxs-lookup"><span data-stu-id="edc89-285">This element is a sequence of</span></span>

1.  <span data-ttu-id="edc89-286">RedTRC FloatPairList</span><span class="sxs-lookup"><span data-stu-id="edc89-286">RedTRC FloatPairList</span></span>
2.  <span data-ttu-id="edc89-287">GreenTRC FloatPairList</span><span class="sxs-lookup"><span data-stu-id="edc89-287">GreenTRC FloatPairList</span></span>
3.  <span data-ttu-id="edc89-288">BlueTRC FloatPairList</span><span class="sxs-lookup"><span data-stu-id="edc89-288">BlueTRC FloatPairList</span></span>

<span data-ttu-id="edc89-289">O elemento também tem um atributo TRCLength do tipo unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="edc89-289">The element also has an attribute TRCLength of unsignedint type.</span></span>

<span data-ttu-id="edc89-290">**Condições de validação:** Para ser determinado dos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-290">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gamutboundarysamplestype"></a><span data-ttu-id="edc89-291">GamutBoundarySamplesType</span><span class="sxs-lookup"><span data-stu-id="edc89-291">GamutBoundarySamplesType</span></span>

<span data-ttu-id="edc89-292">Esse elemento é uma sequência de RGBTypes RGB.</span><span class="sxs-lookup"><span data-stu-id="edc89-292">This element is a sequence of RGB RGBTypes.</span></span>

<span data-ttu-id="edc89-293">**Condições de validação:** Ocorrências máximas não associadas no momento, a serem limitadas com base nos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-293">**Validation conditions:** Currently unbounded maximum occurences, to be capped based on industry feedback.</span></span>

### <a name="floatpairlist"></a><span data-ttu-id="edc89-294">FloatPairList</span><span class="sxs-lookup"><span data-stu-id="edc89-294">FloatPairList</span></span>

<span data-ttu-id="edc89-295">Esse elemento é um tipo simples de lista de pares de floats.</span><span class="sxs-lookup"><span data-stu-id="edc89-295">This element is a simple type of list of pairs of floats.</span></span>

<span data-ttu-id="edc89-296">**Condições de validação:** Para ser determinado dos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-296">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="cmykprintermeasurementtype"></a><span data-ttu-id="edc89-297">CMYKPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="edc89-297">CMYKPrinterMeasurementType</span></span>

<span data-ttu-id="edc89-298">Este elemento é um</span><span class="sxs-lookup"><span data-stu-id="edc89-298">This element is a</span></span>

1. <span data-ttu-id="edc89-299">sequência do elemento ColorCube que consiste em uma sequência de NonNegativeCMYKSampleType de amostra</span><span class="sxs-lookup"><span data-stu-id="edc89-299">sequence of ColorCube element consisting of a sequence of Sample NonNegativeCMYKSampleType</span></span>

2. <span data-ttu-id="edc89-300">Atributo dateTime TimeStamp.</span><span class="sxs-lookup"><span data-stu-id="edc89-300">TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="edc89-301">**Condições de validação:** Para ser determinado dos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-301">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbprintermeasurementtype"></a><span data-ttu-id="edc89-302">RGBPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="edc89-302">RGBPrinterMeasurementType</span></span>

<span data-ttu-id="edc89-303">Este elemento é um</span><span class="sxs-lookup"><span data-stu-id="edc89-303">This element is a</span></span>

1. <span data-ttu-id="edc89-304">sequência do elemento ColorCube que consiste em uma sequência de NonNegativeRGBSampleType de amostra</span><span class="sxs-lookup"><span data-stu-id="edc89-304">sequence of ColorCube element consisting of a sequence of Sample NonNegativeRGBSampleType</span></span>

2. <span data-ttu-id="edc89-305">Atributo dateTime TimeStamp.</span><span class="sxs-lookup"><span data-stu-id="edc89-305">TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="edc89-306">**Condições de validação:** Para ser determinado dos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-306">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbcapturemeasurementtype"></a><span data-ttu-id="edc89-307">RGBCaptureMeasurementType</span><span class="sxs-lookup"><span data-stu-id="edc89-307">RGBCaptureMeasurementType</span></span>

<span data-ttu-id="edc89-308">Este elemento é uma sequência de</span><span class="sxs-lookup"><span data-stu-id="edc89-308">This element is a sequence of</span></span>

1.  <span data-ttu-id="edc89-309">ComplexType PrimaryIndex de</span><span class="sxs-lookup"><span data-stu-id="edc89-309">PrimaryIndex complexType of</span></span>
2.  1.  <span data-ttu-id="edc89-310">OneBasedIndex branco</span><span class="sxs-lookup"><span data-stu-id="edc89-310">White OneBasedIndex</span></span>
    2.  <span data-ttu-id="edc89-311">OneBasedIndex preto opcional</span><span class="sxs-lookup"><span data-stu-id="edc89-311">Optional Black OneBasedIndex</span></span>
    3.  <span data-ttu-id="edc89-312">OneBasedIndex vermelho opcional</span><span class="sxs-lookup"><span data-stu-id="edc89-312">Optional Red OneBasedIndex</span></span>
    4.  <span data-ttu-id="edc89-313">OneBasedIndex verde opcional</span><span class="sxs-lookup"><span data-stu-id="edc89-313">Optional Green OneBasedIndex</span></span>
    5.  <span data-ttu-id="edc89-314">OneBasedIndex azul opcional</span><span class="sxs-lookup"><span data-stu-id="edc89-314">Optional Blue OneBasedIndex</span></span>
    6.  <span data-ttu-id="edc89-315">OneBasedIndex ciano opcional</span><span class="sxs-lookup"><span data-stu-id="edc89-315">Optional Cyan OneBasedIndex</span></span>
    7.  <span data-ttu-id="edc89-316">OneBasedIndex magenta opcional</span><span class="sxs-lookup"><span data-stu-id="edc89-316">Optional Magenta OneBasedIndex</span></span>
    8.  <span data-ttu-id="edc89-317">OneBasedIndex amarelo opcional</span><span class="sxs-lookup"><span data-stu-id="edc89-317">Optional Yellow OneBasedIndex</span></span>

3.  <span data-ttu-id="edc89-318">NeutralIndices de linhas de OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="edc89-318">NeutralIndices of lines of OneBasedIndex</span></span>
4.  <span data-ttu-id="edc89-319">ColorSamples sequência de NonNegativeRGBSampleType de amostra</span><span class="sxs-lookup"><span data-stu-id="edc89-319">ColorSamples sequence of Sample NonNegativeRGBSampleType</span></span>

<span data-ttu-id="edc89-320">O elemento também tem um atributo dateTime TimeStamp.</span><span class="sxs-lookup"><span data-stu-id="edc89-320">The element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="edc89-321">**Condições de validação:** Para ser determinado dos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-321">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="onebasedindex"></a><span data-ttu-id="edc89-322">OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="edc89-322">OneBasedIndex</span></span>

<span data-ttu-id="edc89-323">Esse elemento é um tipo simples de restrição base sem sinal int com valor minInclusive = "1".</span><span class="sxs-lookup"><span data-stu-id="edc89-323">This element is a simple type of restriction base unsigned int with minInclusive value = "1."</span></span>

<span data-ttu-id="edc89-324">**Condições de validação:** Para ser determinado dos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-324">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbprojectormeasurementtype"></a><span data-ttu-id="edc89-325">RGBProjectorMeasurementType</span><span class="sxs-lookup"><span data-stu-id="edc89-325">RGBProjectorMeasurementType</span></span>

<span data-ttu-id="edc89-326">Este elemento é uma sequência de</span><span class="sxs-lookup"><span data-stu-id="edc89-326">This element is a sequence of</span></span>

1.  <span data-ttu-id="edc89-327">Grupo de RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="edc89-327">RGBPrimariesGroup group</span></span>
2.  <span data-ttu-id="edc89-328">elemento ColorSamples que consiste em sequência de NonNegativeRGBSampleType de amostra</span><span class="sxs-lookup"><span data-stu-id="edc89-328">element ColorSamples consisting of sequence of Sample NonNegativeRGBSampleType</span></span>

<span data-ttu-id="edc89-329">O elemento também tem um atributo dateTime TimeStamp.</span><span class="sxs-lookup"><span data-stu-id="edc89-329">The element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="edc89-330">**Condições de validação:** Para ser determinado dos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-330">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="displaymeasurementtype"></a><span data-ttu-id="edc89-331">DisplayMeasurementType</span><span class="sxs-lookup"><span data-stu-id="edc89-331">DisplayMeasurementType</span></span>

<span data-ttu-id="edc89-332">Este elemento é uma sequência de</span><span class="sxs-lookup"><span data-stu-id="edc89-332">This element is a sequence of</span></span>

1.  <span data-ttu-id="edc89-333">RGBPrimariesGroup de grupo</span><span class="sxs-lookup"><span data-stu-id="edc89-333">group RGBPrimariesGroup</span></span>
2.  <span data-ttu-id="edc89-334">GrayRamp da sequência de NonNegativeRGBType de amostra</span><span class="sxs-lookup"><span data-stu-id="edc89-334">GrayRamp of sequence of Sample NonNegativeRGBType</span></span>
3.  <span data-ttu-id="edc89-335">RedRamp da sequência de NonNegativeRGBType de amostra</span><span class="sxs-lookup"><span data-stu-id="edc89-335">RedRamp of sequence of Sample NonNegativeRGBType</span></span>
4.  <span data-ttu-id="edc89-336">GreenRamp da sequência de NonNegativeRGBType de amostra</span><span class="sxs-lookup"><span data-stu-id="edc89-336">GreenRamp of sequence of Sample NonNegativeRGBType</span></span>
5.  <span data-ttu-id="edc89-337">BlueRamp da sequência de NonNegativeRGBType de amostra</span><span class="sxs-lookup"><span data-stu-id="edc89-337">BlueRamp of sequence of Sample NonNegativeRGBType</span></span>

<span data-ttu-id="edc89-338">O elemento DisplayMeasurementType também tem um atributo dateTime TimeStamp.</span><span class="sxs-lookup"><span data-stu-id="edc89-338">The DisplayMeasurementType element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="edc89-339">**Condições de validação:** Para ser determinado dos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-339">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="measurementconditionstype"></a><span data-ttu-id="edc89-340">MeasurementConditionsType</span><span class="sxs-lookup"><span data-stu-id="edc89-340">MeasurementConditionsType</span></span>

<span data-ttu-id="edc89-341">O MeasurementConditionsType é uma sequência de subelementos que contém:</span><span class="sxs-lookup"><span data-stu-id="edc89-341">The MeasurementConditionsType is a sequence of sub-elements that contains:</span></span>

1.  <span data-ttu-id="edc89-342">Valor de enumeração de cadeia de caracteres restrita ColorSpace de "CIEXYZ"</span><span class="sxs-lookup"><span data-stu-id="edc89-342">ColorSpace restricted string enumeration value of "CIEXYZ"</span></span>
2.  <span data-ttu-id="edc89-343">opção opcional de enumeração de cadeia de caracteres WhitePoint NonNegativeXYZType ou WhitePointName de valores D50, D65, A ou F2</span><span class="sxs-lookup"><span data-stu-id="edc89-343">optional choice of WhitePoint NonNegativeXYZType or WhitePointName string enumeration of values D50, D65, A, or F2</span></span>
3.  <span data-ttu-id="edc89-344">GeometryType Geometry</span><span class="sxs-lookup"><span data-stu-id="edc89-344">Geometry GeometryType</span></span>
4.  <span data-ttu-id="edc89-345">ApertureSize inteiro em milímetros</span><span class="sxs-lookup"><span data-stu-id="edc89-345">ApertureSize integer in millimeters</span></span>

<span data-ttu-id="edc89-346">Os padrões são:</span><span class="sxs-lookup"><span data-stu-id="edc89-346">Defaults are:</span></span>

1.  <span data-ttu-id="edc89-347">Impressoras RGB e CMYK:</span><span class="sxs-lookup"><span data-stu-id="edc89-347">RGB and CMYK Printers:</span></span>
    1.  <span data-ttu-id="edc89-348">CIEXYZ MeasurementSpaceType</span><span class="sxs-lookup"><span data-stu-id="edc89-348">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="edc89-349">D50 WhitePointValue</span><span class="sxs-lookup"><span data-stu-id="edc89-349">D50 WhitePointValue</span></span>
    3.  <span data-ttu-id="edc89-350">GeometryType 0/45</span><span class="sxs-lookup"><span data-stu-id="edc89-350">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="edc89-351">10mm ApertureSize</span><span class="sxs-lookup"><span data-stu-id="edc89-351">10mm ApertureSize</span></span>
2.  <span data-ttu-id="edc89-352">Scanners</span><span class="sxs-lookup"><span data-stu-id="edc89-352">Scanners:</span></span>
    1.  <span data-ttu-id="edc89-353">CIEXYZ MeasurementSpaceType</span><span class="sxs-lookup"><span data-stu-id="edc89-353">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="edc89-354">D50 WhitePointValue</span><span class="sxs-lookup"><span data-stu-id="edc89-354">D50 WhitePointValue</span></span>
    3.  <span data-ttu-id="edc89-355">GeometryType 0/45</span><span class="sxs-lookup"><span data-stu-id="edc89-355">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="edc89-356">10mm ApertureSize</span><span class="sxs-lookup"><span data-stu-id="edc89-356">10mm ApertureSize</span></span>
3.  <span data-ttu-id="edc89-357">Exibe e o dispositivo virtual RGB:</span><span class="sxs-lookup"><span data-stu-id="edc89-357">Displays and RGB Virtual Device:</span></span>
    1.  <span data-ttu-id="edc89-358">CIEXYZ MeasurementSpaceType</span><span class="sxs-lookup"><span data-stu-id="edc89-358">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="edc89-359">D65 WhitePointValue</span><span class="sxs-lookup"><span data-stu-id="edc89-359">D65 WhitePointValue</span></span>
    3.  <span data-ttu-id="edc89-360">GeometryType 0/45</span><span class="sxs-lookup"><span data-stu-id="edc89-360">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="edc89-361">10mm ApertureSize</span><span class="sxs-lookup"><span data-stu-id="edc89-361">10mm ApertureSize</span></span>
4.  <span data-ttu-id="edc89-362">Câmaras</span><span class="sxs-lookup"><span data-stu-id="edc89-362">Cameras:</span></span>
    1.  <span data-ttu-id="edc89-363">CIEXYZ MeasurementSpaceType</span><span class="sxs-lookup"><span data-stu-id="edc89-363">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="edc89-364">D65 WhitePointValue</span><span class="sxs-lookup"><span data-stu-id="edc89-364">D65 WhitePointValue</span></span>
    3.  <span data-ttu-id="edc89-365">GeometryType direto</span><span class="sxs-lookup"><span data-stu-id="edc89-365">Direct GeometryType</span></span>
    4.  <span data-ttu-id="edc89-366">10mm ApertureSize</span><span class="sxs-lookup"><span data-stu-id="edc89-366">10mm ApertureSize</span></span>

<span data-ttu-id="edc89-367">**Condições de validação:** A validação de cada sub-elemento é determinada pelas condições de validação para esses subelementos.</span><span class="sxs-lookup"><span data-stu-id="edc89-367">**Validation conditions:** Validation of each sub-element is determined by validation conditions for those sub-elements.</span></span> <span data-ttu-id="edc89-368">Se algum subelemento estiver ausente, o padrão específico do tipo de modelo do dispositivo será usado.</span><span class="sxs-lookup"><span data-stu-id="edc89-368">If any sub-element is missing, the device model type specific default is used.</span></span>

### <a name="geometrytype"></a><span data-ttu-id="edc89-369">GeometryType</span><span class="sxs-lookup"><span data-stu-id="edc89-369">GeometryType</span></span>

<span data-ttu-id="edc89-370">String</span><span class="sxs-lookup"><span data-stu-id="edc89-370">String</span></span>

<span data-ttu-id="edc89-371">Valores de enumeração:</span><span class="sxs-lookup"><span data-stu-id="edc89-371">Enumeration values:</span></span>

-   <span data-ttu-id="edc89-372">"0/45"</span><span class="sxs-lookup"><span data-stu-id="edc89-372">"0/45"</span></span>
-   <span data-ttu-id="edc89-373">"0/difuso"</span><span class="sxs-lookup"><span data-stu-id="edc89-373">"0/diffuse"</span></span>
-   <span data-ttu-id="edc89-374">"difuso/0"</span><span class="sxs-lookup"><span data-stu-id="edc89-374">"diffuse/0"</span></span>
-   <span data-ttu-id="edc89-375">Encaminhe</span><span class="sxs-lookup"><span data-stu-id="edc89-375">"Direct"</span></span>

<span data-ttu-id="edc89-376">**Condições de validação:** Qualquer valor, exceto os valores de enumberation listados, é inválido.</span><span class="sxs-lookup"><span data-stu-id="edc89-376">**Validation conditions:** Any value except the enumberation values listed is invalid.</span></span> <span data-ttu-id="edc89-377">Essas informações não alterarão o comportamento de processamento de linha de base.</span><span class="sxs-lookup"><span data-stu-id="edc89-377">This information will not change baseline processing behavior.</span></span>

### <a name="rgbprimariesgroup"></a><span data-ttu-id="edc89-378">RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="edc89-378">RGBPrimariesGroup</span></span>

<span data-ttu-id="edc89-379">Este elemento é uma sequência de</span><span class="sxs-lookup"><span data-stu-id="edc89-379">This element is a sequence of</span></span>

1.  <span data-ttu-id="edc89-380">WhitePrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="edc89-380">WhitePrimary NonNegativeXYZType</span></span>
2.  <span data-ttu-id="edc89-381">RedPrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="edc89-381">RedPrimary NonNegativeXYZType</span></span>
3.  <span data-ttu-id="edc89-382">GreenPrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="edc89-382">GreenPrimary NonNegativeXYZType</span></span>
4.  <span data-ttu-id="edc89-383">BluePrimary NonNegativeXYZTYpe</span><span class="sxs-lookup"><span data-stu-id="edc89-383">BluePrimary NonNegativeXYZTYpe</span></span>
5.  <span data-ttu-id="edc89-384">BlackPrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="edc89-384">BlackPrimary NonNegativeXYZType</span></span>

<span data-ttu-id="edc89-385">**Condições de validação:** Para ser determinado dos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-385">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativecmyksampletype"></a><span data-ttu-id="edc89-386">NonNegativeCMYKSampleType</span><span class="sxs-lookup"><span data-stu-id="edc89-386">NonNegativeCMYKSampleType</span></span>

<span data-ttu-id="edc89-387">Este elemento é uma sequência de</span><span class="sxs-lookup"><span data-stu-id="edc89-387">This element is a sequence of</span></span>

1.  <span data-ttu-id="edc89-388">NonNegativeCMYKType CMYK</span><span class="sxs-lookup"><span data-stu-id="edc89-388">CMYK NonNegativeCMYKType</span></span>
2.  <span data-ttu-id="edc89-389">CIEXYZ NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="edc89-389">CIEXYZ NonNegativeXYZType</span></span>

<span data-ttu-id="edc89-390">O elemento também tem uma cadeia de caracteres de marca de atributo opcional</span><span class="sxs-lookup"><span data-stu-id="edc89-390">The element also has an optional attribute Tag string</span></span>

<span data-ttu-id="edc89-391">**Condições de validação:** Para ser determinado dos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-391">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativergbsampletype"></a><span data-ttu-id="edc89-392">NonNegativeRGBSampleType</span><span class="sxs-lookup"><span data-stu-id="edc89-392">NonNegativeRGBSampleType</span></span>

<span data-ttu-id="edc89-393">Este elemento é uma sequência de</span><span class="sxs-lookup"><span data-stu-id="edc89-393">This element is a sequence of</span></span>

1.  <span data-ttu-id="edc89-394">NonNegativeRGBType RGB</span><span class="sxs-lookup"><span data-stu-id="edc89-394">RGB NonNegativeRGBType</span></span>
2.  <span data-ttu-id="edc89-395">CIEXYZ NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="edc89-395">CIEXYZ NonNegativeXYZType</span></span>

<span data-ttu-id="edc89-396">O elemento também tem uma cadeia de caracteres de marca de atributo opcional</span><span class="sxs-lookup"><span data-stu-id="edc89-396">The element also has an optional attribute Tag string</span></span>

<span data-ttu-id="edc89-397">**Condições de validação:** Para ser determinado dos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-397">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativecmyktype"></a><span data-ttu-id="edc89-398">NonNegativeCMYKType</span><span class="sxs-lookup"><span data-stu-id="edc89-398">NonNegativeCMYKType</span></span>

<span data-ttu-id="edc89-399">Este elemento consiste em atributos</span><span class="sxs-lookup"><span data-stu-id="edc89-399">This element consisting of attributes</span></span>

1.  <span data-ttu-id="edc89-400">C float</span><span class="sxs-lookup"><span data-stu-id="edc89-400">C float</span></span>
2.  <span data-ttu-id="edc89-401">M float</span><span class="sxs-lookup"><span data-stu-id="edc89-401">M float</span></span>
3.  <span data-ttu-id="edc89-402">Float de Y</span><span class="sxs-lookup"><span data-stu-id="edc89-402">Y float</span></span>
4.  <span data-ttu-id="edc89-403">K float</span><span class="sxs-lookup"><span data-stu-id="edc89-403">K float</span></span>

<span data-ttu-id="edc89-404">**Condições de validação:** Para ser determinado dos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-404">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativergbtype"></a><span data-ttu-id="edc89-405">NonNegativeRGBType</span><span class="sxs-lookup"><span data-stu-id="edc89-405">NonNegativeRGBType</span></span>

<span data-ttu-id="edc89-406">Este elemento consiste em atributos</span><span class="sxs-lookup"><span data-stu-id="edc89-406">This element consisting of attributes</span></span>

1.  <span data-ttu-id="edc89-407">Float de R</span><span class="sxs-lookup"><span data-stu-id="edc89-407">R float</span></span>
2.  <span data-ttu-id="edc89-408">G float</span><span class="sxs-lookup"><span data-stu-id="edc89-408">G float</span></span>
3.  <span data-ttu-id="edc89-409">B float</span><span class="sxs-lookup"><span data-stu-id="edc89-409">B float</span></span>

<span data-ttu-id="edc89-410">**Condições de validação:** Para ser determinado dos comentários do setor.</span><span class="sxs-lookup"><span data-stu-id="edc89-410">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="extensiontype"></a><span data-ttu-id="edc89-411">ExtensionType</span><span class="sxs-lookup"><span data-stu-id="edc89-411">ExtensionType</span></span>

<span data-ttu-id="edc89-412">O elemento ExtensionType é uma sequência de qualquer tipo de subelemento e é usado para informações proprietárias de aplicativos que não são da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="edc89-412">The ExtensionType element is a sequence of any sub-element type and is used for proprietary information from non-Microsoft applications.</span></span>

<span data-ttu-id="edc89-413">**Condições de validação:** Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="edc89-413">**Validation conditions:** This element is optional.</span></span> <span data-ttu-id="edc89-414">Pode haver um máximo de 1000 subelementos de extensão.</span><span class="sxs-lookup"><span data-stu-id="edc89-414">There can be a maximum of 1000 extension sub-elements.</span></span>

### <a name="nonnegativexyztype"></a><span data-ttu-id="edc89-415">NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="edc89-415">NonNegativeXYZType</span></span>

<span data-ttu-id="edc89-416">O elemento NonNegativeXYZType é composto por NonNegativeFloatType três elementos de ponto flutuante de IEEE de precisão simples chamados "X", "Y" e "Z".</span><span class="sxs-lookup"><span data-stu-id="edc89-416">The NonNegativeXYZType element is composed of NonNegativeFloatType three single-precision IEEE floating-point elements named "X," "Y," and "Z."</span></span> <span data-ttu-id="edc89-417">Esses valores são limitados aos valores de medição de perfis do DMP.</span><span class="sxs-lookup"><span data-stu-id="edc89-417">These values are limited to the DMP profiles measurement values.</span></span> <span data-ttu-id="edc89-418">Essas medidas podem ser absolutas (não relativas) CIEXYZ 1931 valores de reflexão ou valores absolutos (não relativos) CIEXYZ 1931 diretos (transmissal) em candelas por unidades de metro quadrado.</span><span class="sxs-lookup"><span data-stu-id="edc89-418">These measurements can be either absolute (not relative) CIEXYZ 1931 reflective values or absolute (not relative) CIEXYZ 1931 direct (transmissive) values in candelas per meter squared units.</span></span>

<span data-ttu-id="edc89-419">**Condições de validação:** Somente valores do mundo real são válidos e valores de medição CIEXYZ negativos são inválidos.</span><span class="sxs-lookup"><span data-stu-id="edc89-419">**Validation conditions:** Only real-world values are valid, and negative CIEXYZ measurement values are invalid.</span></span> <span data-ttu-id="edc89-420">Como esses são valores absolutos, os valores podem ser maiores que 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="edc89-420">Because these are absolute values, values can be greater than 1.0f.</span></span> <span data-ttu-id="edc89-421">Um limite razoável para qualquer "X", "Y" ou "Z".</span><span class="sxs-lookup"><span data-stu-id="edc89-421">A reasonable limit for any "X," "Y," or "Z."</span></span> <span data-ttu-id="edc89-422">o valor é definido arbitrariamente como 10000.0 f.</span><span class="sxs-lookup"><span data-stu-id="edc89-422">value is arbitrarily set to 10000.0f.</span></span>

### <a name="xyztype"></a><span data-ttu-id="edc89-423">XYZType</span><span class="sxs-lookup"><span data-stu-id="edc89-423">XYZType</span></span>

<span data-ttu-id="edc89-424">O elemento XYZType é composto por três valores de ponto flutuante IEEE de precisão simples: "X", "Y" e "Z".</span><span class="sxs-lookup"><span data-stu-id="edc89-424">The XYZType element is composed of three single-precision IEEE floating-point values: "X," "Y," and "Z."</span></span>

## <a name="the-cdmp-baseline-algorithms"></a><span data-ttu-id="edc89-425">Os algoritmos de linha de base CDMP</span><span class="sxs-lookup"><span data-stu-id="edc89-425">The CDMP Baseline Algorithms</span></span>

### <a name="crt-device-model-baseline"></a><span data-ttu-id="edc89-426">Linha de base de modelo de dispositivo CRT</span><span class="sxs-lookup"><span data-stu-id="edc89-426">CRT Device Model Baseline</span></span>

<span data-ttu-id="edc89-427">Para entender esse modelo, você deve considerar o processo de caracterização e a modelagem do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="edc89-427">To understand this model, you must consider both the characterization process and the device modeling.</span></span> <span data-ttu-id="edc89-428">No processo de caracterização, as medidas da XYZ são executadas primeiro nas cores obtidas preenchendo o buffer de exibição de um dispositivo de vídeo CRT.</span><span class="sxs-lookup"><span data-stu-id="edc89-428">In the characterization process, XYZ measurements are first performed on the colors obtained by filling the display buffer of a CRT display device.</span></span> <span data-ttu-id="edc89-429">Os seguintes valores de exemplo irão gerar bons dados para o modelo de dispositivo CRT de linha de base:</span><span class="sxs-lookup"><span data-stu-id="edc89-429">The following example values will generate good data for the baseline CRT device model:</span></span>

<span data-ttu-id="edc89-430">Vermelho: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span><span class="sxs-lookup"><span data-stu-id="edc89-430">Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span></span>

<span data-ttu-id="edc89-431">Verde: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span><span class="sxs-lookup"><span data-stu-id="edc89-431">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span></span>

<span data-ttu-id="edc89-432">Azul: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span><span class="sxs-lookup"><span data-stu-id="edc89-432">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span></span>

<span data-ttu-id="edc89-433">Neutrals: R = G = B = 0, 8, 16, 32, 64, 128, 192, 255</span><span class="sxs-lookup"><span data-stu-id="edc89-433">Neutrals: R = G= B = 0, 8, 16, 32, 64, 128, 192, 255</span></span>

<span data-ttu-id="edc89-434">Incrementos diferentes de 15 e incrementos não lineares também podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="edc89-434">Increments other than 15 and nonlinear increments can also be used.</span></span> <span data-ttu-id="edc89-435">Cada rampa vermelha, verde, azul e neutro deve conter pelo menos três exemplos, mas é recomendável fornecer mais amostras.</span><span class="sxs-lookup"><span data-stu-id="edc89-435">Each red, green, blue, and neutral ramp must contain at least three samples, but providing more samples is recommended.</span></span> <span data-ttu-id="edc89-436">Você deve fornecer exemplos para vermelho puro, verde, azul, preto e branco.</span><span class="sxs-lookup"><span data-stu-id="edc89-436">You must provide samples for pure red, green, blue, black, and white.</span></span> <span data-ttu-id="edc89-437">Os exemplos não precisam ser espaçados uniformemente.</span><span class="sxs-lookup"><span data-stu-id="edc89-437">The samples do not have to be uniformly spaced.</span></span>

<span data-ttu-id="edc89-438">O processo de criação da matriz triestímulo consiste em duas etapas.</span><span class="sxs-lookup"><span data-stu-id="edc89-438">The process of building the tristimulus matrix consists of two steps.</span></span> <span data-ttu-id="edc89-439">Em primeiro lugar, estimar o valor do ponto preto ou o FLARE.</span><span class="sxs-lookup"><span data-stu-id="edc89-439">First, estimate the black point XYZ value, or the flare.</span></span> <span data-ttu-id="edc89-440">Esta etapa baseia-se amplamente no trabalho de Berns \[ 3 \] com uma função de objetivo ligeiramente modificada para a otimização não linear.</span><span class="sxs-lookup"><span data-stu-id="edc89-440">This step is based largely on work of Berns\[3\] with a slightly modified objective function for the nonlinear optimization.</span></span> <span data-ttu-id="edc89-441">Em segundo lugar, calcule a matriz de triestímulo com base no resultado da etapa um e também de um cálculo de média em todas as medições por canal, não apenas a única para a contagem digital máxima.</span><span class="sxs-lookup"><span data-stu-id="edc89-441">Second, calculate tristimulus matrix based on the result from step one and also from an averaging calculation on all of the per-channel measurements, not just the one for maximum digital count.</span></span>

<span data-ttu-id="edc89-442">Cada uma dessas etapas contém procedimentos detalhados.</span><span class="sxs-lookup"><span data-stu-id="edc89-442">Each of these steps contains detailed procedures.</span></span> <span data-ttu-id="edc89-443">O ponto de partida é a rampa (17 etapas em nosso exemplo) para cada um dos canais R, G e B.</span><span class="sxs-lookup"><span data-stu-id="edc89-443">The starting point is the ramps (17 steps in our example) for each of R, G, and B channels.</span></span> <span data-ttu-id="edc89-444">Quando as medidas XYZ são plotadas no plano *XY* de desvio, uma situação típica é mostrada na Figura 1.</span><span class="sxs-lookup"><span data-stu-id="edc89-444">When the XYZ measurements are plotted on the chromaticity *xy* -plane, a typical situation is shown in Figure 1.</span></span> <span data-ttu-id="edc89-445">A etapa 1 consiste em resolver um problema de otimização não linear para encontrar o ponto preto "melhor ajuste", que minimizará a descompasso em desvio, uma vez que atravessa os canais R, G e B.</span><span class="sxs-lookup"><span data-stu-id="edc89-445">Step one consists of solving a nonlinear optimization problem to find the "best fit" black point that will minimize the drift in chromaticity as one traverses along the R, G, and B channels.</span></span> <span data-ttu-id="edc89-446">Com base no Berns \[ 3 \] , buscamos ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>k</sub>* ) que minimiza a seguinte função objetiva:</span><span class="sxs-lookup"><span data-stu-id="edc89-446">Based on Berns\[3\], we seek ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z<sub>K</sub>* ) that minimizes the following objective function:</span></span>

![Mostra a função de objetivo em que Sr, SG e SB são o conjunto de pontos de dados nos canais R, G e B.](images/cdmp-formula1.png)

<span data-ttu-id="edc89-448">em que *s <sub>R</sub>*,*s <sub>G</sub>* e *s <sub>B</sub>* são o conjunto de pontos de dados correspondente aos pontos nos canais R, G e B.</span><span class="sxs-lookup"><span data-stu-id="edc89-448">where *S <sub>R</sub>*,*S <sub>G</sub>*, and *S<sub>B</sub>* are the set of data points corresponding to the points on the R, G, and B channels.</span></span> <span data-ttu-id="edc89-449">Para qualquer conjunto de *S*, defina:</span><span class="sxs-lookup"><span data-stu-id="edc89-449">For any set *S*, define:</span></span>

![Mostra uma fórmula para definir quaisquer S de conjunto.](images/cdmp-formula2.png)

<span data-ttu-id="edc89-451">No anterior, \| *s* \| é a cardinalidade de *S*, ou seja, o número de pontos no *S* do conjunto. ![ Mostra uma fórmula para a desvio de um ponto.](images/cdmp-formula3.png)</span><span class="sxs-lookup"><span data-stu-id="edc89-451">In the preceding, \| *S* \| is the cardinality of *S*, i.e., the number of points in the set *S*. ![Shows a formula for the chromaticity of a point.](images/cdmp-formula3.png)</span></span> <span data-ttu-id="edc89-452">é as coordenadas de desvio do ponto ![ mostra um formaula para um ponto.](images/cdmp-formula4.png)</span><span class="sxs-lookup"><span data-stu-id="edc89-452">is the chromaticity coordinates of the point ![Shows a formaula for a point.](images/cdmp-formula4.png)</span></span> <span data-ttu-id="edc89-453">, portanto, ![ mostra uma fórmula para a média ou o centro de massa. ](images/cdmp-formula5.png) é a média ou o centro de massa de todos os pontos do conjunto de *S* no plano de desvio.</span><span class="sxs-lookup"><span data-stu-id="edc89-453">, so ![Shows a formula for the average or center of mass.](images/cdmp-formula5.png), is the average, or center of mass, of all the points in the set *S* in the chromaticity plane.</span></span> <span data-ttu-id="edc89-454">Assim, ![ mostra uma fórmula para a soma de um segundo ponto de pontos.](images/cdmp-formula6.png)</span><span class="sxs-lookup"><span data-stu-id="edc89-454">Thus, ![Shows a formula for the sum of a second moments of points.](images/cdmp-formula6.png)</span></span> <span data-ttu-id="edc89-455">é a soma do segundo instante dos pontos sobre o centro de massa e é uma medida de como distribuir os pontos.</span><span class="sxs-lookup"><span data-stu-id="edc89-455">is the sum of second moments of the points about the center of mass and is a measure of how spread out the points are about it.</span></span> <span data-ttu-id="edc89-456">Por fim, ![ mostra uma fórmula para a medida total da difusão de três clusters de pontos.](images/cdmp-formula7.png)</span><span class="sxs-lookup"><span data-stu-id="edc89-456">Finally, ![Shows a formula for the total measure of the spread of three clusters of points.](images/cdmp-formula7.png)</span></span> <span data-ttu-id="edc89-457">é uma medida total de como distribuir os três clusters de pontos são sobre seus respectivos centros de massa.</span><span class="sxs-lookup"><span data-stu-id="edc89-457">is a total measure of how spread out the three clusters of points are about their respective centers of mass.</span></span>

<span data-ttu-id="edc89-458">No cálculo de ![ mostra uma fórmula de f (X, Y, Z; XK, YK, ZK).](images/cdmp-formula8.png)</span><span class="sxs-lookup"><span data-stu-id="edc89-458">In the calculation of ![Shows a formula of f(X,Y,Z; Xk, Yk, Zk).](images/cdmp-formula8.png)</span></span> <span data-ttu-id="edc89-459">, se ![ mostrar uma fórmula para X. ](images/cdmp-formula9.png) , o cálculo será ignorado e a cardinalidade de *S* será ajustada de acordo.</span><span class="sxs-lookup"><span data-stu-id="edc89-459">, if ![Shows a formula for X.](images/cdmp-formula9.png) , then the calculation is skipped, and the cardinality of *S* is adjusted accordingly.</span></span>

<span data-ttu-id="edc89-460">Apesar da complexidade aparente da função objetiva, é uma soma dos quadrados de muitas funções diferenciávels em *X <sub>K</sub>*,*Y <sub>k</sub>Z <sub>k</sub>* (17 pontos 2 *XY* -Components 3 Channels = 102, no exemplo) e, portanto, é receptivos a técnicas de quadrados mínimos não lineares padrão, como o algoritmo Levenberg-Marquardt, que é o algoritmo usado no WCS.</span><span class="sxs-lookup"><span data-stu-id="edc89-460">Despite the apparent complexity of the objective function, it is a sum of the squares of many differentiable functions in *X <sub>K</sub>*,*Y <sub>K</sub>Z <sub>K</sub>* (17 points   2 *xy* -components   3 channels = 102, in the example), and, therefore, is amenable to standard nonlinear least squares techniques, such as the Levenberg-Marquardt algorithm, which is the algorithm used in WCS.</span></span> <span data-ttu-id="edc89-461">Observe que a função de objetivo anterior é diferente da sugerida no Berns \[ 3 \] , já que a última função mede a variância das distâncias do centro de massa, de forma que a variação seja zero quando os pontos forem equidistante do centro de massa, mesmo que possam se espalhar um pouco.</span><span class="sxs-lookup"><span data-stu-id="edc89-461">Note that the preceding objective function is different from the one suggested in Berns\[3\] in that the latter function measures the variance of the distances from the center of mass, so that the variance is zero when the points are equidistant from the center of mass, even though they may spread out quite a bit about it.</span></span> <span data-ttu-id="edc89-462">No exemplo, a dispersão de pontos é contratada diretamente usando o segundo instante.</span><span class="sxs-lookup"><span data-stu-id="edc89-462">In the example, the dispersion of points is contolled directly using the second moments.</span></span>

<span data-ttu-id="edc89-463">Como com qualquer algoritmo iterativo para o problema de quadrados não lineares, Levenberg-Marquardt requer uma estimativa inicial.</span><span class="sxs-lookup"><span data-stu-id="edc89-463">As with any iterative algorithm for the nonlinear least squares problem, Levenberg-Marquardt requires an initial guess.</span></span> <span data-ttu-id="edc89-464">Há dois candidatos óbvios.</span><span class="sxs-lookup"><span data-stu-id="edc89-464">There are two obvious candidates.</span></span> <span data-ttu-id="edc89-465">Um é (0, 0, 0); o outro é o ponto preto medido.</span><span class="sxs-lookup"><span data-stu-id="edc89-465">One is (0, 0, 0); the other is the measured black point.</span></span> <span data-ttu-id="edc89-466">Para a CTE, o ponto preto medido é usado primeiro como a estimativa inicial.</span><span class="sxs-lookup"><span data-stu-id="edc89-466">For the CTE, the measured black point is first used as the initial guess.</span></span> <span data-ttu-id="edc89-467">Se um máximo de 100 iterações for excedido sem alcançar um limite de uma distância média de 0, 1 de cada ponto de seu centro de massa (que corresponde a um valor limite de (0, 1) 17 3 = 0, 51 para a função objetiva), então, outra rodada de iterações com a estimativa inicial de (0, 0, 0) é executada.</span><span class="sxs-lookup"><span data-stu-id="edc89-467">If a maximum of 100 iterations is exceeded without achieving a threshold of an average distance of 0.001 of each point from its center of mass (which corresponds to a threshold value of (0.001)    17   3 = 0.000051 for the objective function), then another round of iterations with the initial guess of (0, 0, 0) is performed.</span></span> <span data-ttu-id="edc89-468">A estimativa resultante do ponto preto é XYZ comparada com a melhor estimativa da rodada anterior de iterações (com o ponto preto medido como a estimativa inicial).</span><span class="sxs-lookup"><span data-stu-id="edc89-468">The resulting estimate of the black point is XYZ compared with the best estimate from the previous round of iterations (with the measured black point as the initial guess).</span></span> <span data-ttu-id="edc89-469">Use a estimativa que fornece o menor valor para a função Objective.</span><span class="sxs-lookup"><span data-stu-id="edc89-469">Use the estimate that gives the smallest value for the objective function.</span></span> <span data-ttu-id="edc89-470">A escolha de 100 iterações e a distância de erro de 0, 1 foram cada uma das empiricamente selecionadas.</span><span class="sxs-lookup"><span data-stu-id="edc89-470">The choice of 100 iterations and the error distance of 0.001 were each selected empirically.</span></span> <span data-ttu-id="edc89-471">Em versões futuras, pode ser razoável parametrizar a distância do erro.</span><span class="sxs-lookup"><span data-stu-id="edc89-471">In future versions, it might be reasonable to parameterize the error distance.</span></span>

<span data-ttu-id="edc89-472">O resultado da etapa 1 é o ponto preto estimado ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>k</sub>* ).</span><span class="sxs-lookup"><span data-stu-id="edc89-472">The result of step one is the estimated black point ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z<sub>K</sub>* ).</span></span> <span data-ttu-id="edc89-473">A etapa dois consiste em determinar a matriz de triestímulo calculando a média da desvio dos pontos nos três clusters obtidos na etapa um.</span><span class="sxs-lookup"><span data-stu-id="edc89-473">Step two consists of determining the tristimulus matrix by averaging the chromaticity of the points in the three clusters obtained in step one.</span></span> <span data-ttu-id="edc89-474">Para CRTs, isso é feito principalmente para minimizar os efeitos dos erros de medida.</span><span class="sxs-lookup"><span data-stu-id="edc89-474">For CRTs, this is done primarily to minimize the effects of measurement errors.</span></span> <span data-ttu-id="edc89-475">Os pontos usados na média da desvio devem ser os mesmos pontos usados na otimização na etapa um.</span><span class="sxs-lookup"><span data-stu-id="edc89-475">The points used in averaging the chromaticity must be the same points used in the optimization in step one.</span></span> <span data-ttu-id="edc89-476">Em outras palavras, se o primeiro ponto (contagem digital 15, no exemplo) em cada rampa for descartado na etapa de otimização, o mesmo deverá ser feito na média.</span><span class="sxs-lookup"><span data-stu-id="edc89-476">In other words, if the first point (digital count 15, in the example) in each ramp is discarded in the optimization step, then the same must be done in the averaging.</span></span> <span data-ttu-id="edc89-477">Se o ![ Mostrar fórmulas de desvio médio de coordenadas nos canais vermelho e verde.](images/cdmp-formula10.png)</span><span class="sxs-lookup"><span data-stu-id="edc89-477">If ![Shows formulas of averaged chromaticity for coordinates in the red and green channels.](images/cdmp-formula10.png)</span></span> <span data-ttu-id="edc89-478">e ![ mostra uma fórmula de desvio médio de coordenadas no canal azul.](images/cdmp-formula11.png)</span><span class="sxs-lookup"><span data-stu-id="edc89-478">, and ![Shows a formula of averaged chromaticity for coordinates in the blue channel.](images/cdmp-formula11.png)</span></span> <span data-ttu-id="edc89-479">são as coordenadas de desvios médias dos canais vermelho, verde e azul e, em seguida, o procedimento a seguir determina a matriz triestímulo.</span><span class="sxs-lookup"><span data-stu-id="edc89-479">are the averaged chromaticity coordinates of the red, green, and blue channels, then the following procedure determines the tristimulus matrix.</span></span> <span data-ttu-id="edc89-480">Primeiro, resolva o sistema de 3? 3 lineares:</span><span class="sxs-lookup"><span data-stu-id="edc89-480">First, solve the 3?3 linear system:</span></span>

![Mostra a primeira parte do procedimento para resolver um sistema de 3? 3 lineares.](images/cdmp-formula12.png)

![Mostra a segunda parte do sistema de 3? 3 lineares.](images/cdmp-formula13.gif)![Mostrar o valor t subscript b no final da segunda parte do sistema 3? 3 linear.](images/cdmp-formula14.gif)

<span data-ttu-id="edc89-484">*X <sub>w</sub>*,*Y <sub>w</sub>*,*Z <sub>W</sub>*</span><span class="sxs-lookup"><span data-stu-id="edc89-484">*X <sub>W</sub>*,*Y <sub>W</sub>*,*Z<sub>W</sub>*</span></span>

![Mostra a parte final do procedimento para resolver um sistema de 3? 3 lineares.](images/cdmp-formula15.png)

<span data-ttu-id="edc89-486">Depois que a matriz triestímulo é determinada, a determinação das curvas de Tom segue a abordagem padrão.</span><span class="sxs-lookup"><span data-stu-id="edc89-486">After the tristimulus matrix is determined, the determination of tone curves follows the standard approach.</span></span> <span data-ttu-id="edc89-487">Para monitores CRT, presume-se que os canais individuais sigam o modelo "GOG":</span><span class="sxs-lookup"><span data-stu-id="edc89-487">For CRT displays, the individual channels are assumed to follow the "GOG" model:</span></span>

![Mostra a fórmula do modelo ' G O G '.](images/cdmp-formula16.png)

<span data-ttu-id="edc89-489">onde *k <sub>g</sub>* é o "lucro", 1-*k <sub>g</sub>* é o "deslocamento" e?</span><span class="sxs-lookup"><span data-stu-id="edc89-489">where *k <sub>g</sub>* is the "gain",1 -*k<sub>g</sub>* is the "offset", and ?</span></span> <span data-ttu-id="edc89-490">é o "gama".</span><span class="sxs-lookup"><span data-stu-id="edc89-490">is the "gamma."</span></span> <span data-ttu-id="edc89-491">A matriz inversa da matriz triestímulo é aplicada aos dados da XYZ dos neutros para obter os dados RGB lineares, que são correlacionados com os valores RGB digitais usando a regressão não linear no modelo GOG.</span><span class="sxs-lookup"><span data-stu-id="edc89-491">The inverse matrix of the tristimulus matrix is applied to the XYZ data of the neutrals to obtain the linear RGB data, which is then correlated with the digital RGB values using nonlinear regression on the GOG model.</span></span> <span data-ttu-id="edc89-492">Essas características não precisam ser as mesmas para os canais R, G e B e, em geral, não são as mesmas.</span><span class="sxs-lookup"><span data-stu-id="edc89-492">These characteristics do not have to be the same for the R, G, and B channels, and generally are not the same.</span></span>

<span data-ttu-id="edc89-493">Berns \[ 1 \] : Berns, *Billmeyer e Saltzman princípios de tecnologia de cores*, 3 <sub>RD</sub> Ed.</span><span class="sxs-lookup"><span data-stu-id="edc89-493">Berns\[1\]: Berns, *Billmeyer and Saltzman's Principles of Color Technology*, 3 <sub>rd</sub> Ed.</span></span> <span data-ttu-id="edc89-494">John Wiley & filhos (2000).</span><span class="sxs-lookup"><span data-stu-id="edc89-494">John Wiley & Sons (2000).</span></span>

<span data-ttu-id="edc89-495">Berns \[ 2 \] : Berns e Katoh, a função de transferência digital para radiometric para exibições CRT controladas por computador, *padrões de cores cies Symposium ' 97 cor para a tecnologia de geração de imagens*, Nov. 1997.</span><span class="sxs-lookup"><span data-stu-id="edc89-495">Berns\[2\]: Berns and Katoh, The digital to radiometric transfer function for computer controlled CRT displays, *CIE Expert Symposium '97 Colour Standards for Imaging Technology*, Nov. 1997.</span></span>

<span data-ttu-id="edc89-496">Berns \[ 3 \] : Berns, Fernandez e Taplin, estimando Black-Level emissões de exibições de Computer-Controlled, *pesquisa de cores e aplicativo*, 28:379-383 Wiley periódicos, Inc. (2003)</span><span class="sxs-lookup"><span data-stu-id="edc89-496">Berns\[3\]: Berns, Fernandez and Taplin, Estimating Black-Level Emissions of Computer-Controlled Displays, *Color Research and Application*, 28: 379-383 Wiley Periodicals, Inc. (2003)</span></span>

<span data-ttu-id="edc89-497">Kang \[ 1 \] : Kang, *tecnologia de cores para dispositivos de imagem eletrônica*, SPIE (1997)</span><span class="sxs-lookup"><span data-stu-id="edc89-497">Kang\[1\]: Kang, *Color Technology for Electronic Imaging Devices*, SPIE (1997)</span></span>

<span data-ttu-id="edc89-498">Katoh \[ 1 \] : Katoh, Deguchi e Berns, uma caracterização precisa da proposta do monitor CRT (II) para uma extensão do método cie e sua verificação, *opt. Rev.* 8:397-408 (2001)</span><span class="sxs-lookup"><span data-stu-id="edc89-498">Katoh\[1\]: Katoh, Deguchi and Berns, An accurate characterization of CRT monitor (II) proposal for an extension to CIE method and its verification, *Opt. Rev.* 8: 397-408 (2001)</span></span>

### <a name="lcd-device-model-baseline"></a><span data-ttu-id="edc89-499">Linha de base do modelo de dispositivo LCD</span><span class="sxs-lookup"><span data-stu-id="edc89-499">LCD Device Model Baseline</span></span>

<span data-ttu-id="edc89-500">A linha de base do modelo de dispositivo LCD é semelhante à linha de base do modelo de dispositivo CRT.</span><span class="sxs-lookup"><span data-stu-id="edc89-500">The LCD Device Model Baseline is similar to the CRT Device Model Baseline.</span></span> <span data-ttu-id="edc89-501">Esta seção explicará as maneiras pelas quais a modelagem de LCD difere da modelagem CRT.</span><span class="sxs-lookup"><span data-stu-id="edc89-501">This section will explain the ways in which LCD modeling differs from CRT modeling.</span></span>

<span data-ttu-id="edc89-502">Uma diferença é que você não pode supor que as exibições de LCD sigam o modelo GOG usado para CRTs, e as curvas de Tom são obtidas pela interpolação de dados medidos.</span><span class="sxs-lookup"><span data-stu-id="edc89-502">One difference is that you cannot assume that LCD displays follow the GOG model used for CRTs, and the tone curves are obtained by interpolation of measured data.</span></span> <span data-ttu-id="edc89-503">Por isso, o eixo neutro do dispositivo deve ser amostrado com mais frequência.</span><span class="sxs-lookup"><span data-stu-id="edc89-503">Because of that, the device neutral axis should be sampled more frequently.</span></span>

<span data-ttu-id="edc89-504">Aqui estão alguns valores de exemplo típicos que podem gerar bons dados para a linha de base do modelo de dispositivo LCD:</span><span class="sxs-lookup"><span data-stu-id="edc89-504">Here are some typical example values that can generate good data for the LCD device model baseline:</span></span>

<span data-ttu-id="edc89-505">Vermelho: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span><span class="sxs-lookup"><span data-stu-id="edc89-505">Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span></span>

<span data-ttu-id="edc89-506">Verde: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span><span class="sxs-lookup"><span data-stu-id="edc89-506">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span></span>

<span data-ttu-id="edc89-507">Azul: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span><span class="sxs-lookup"><span data-stu-id="edc89-507">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span></span>

<span data-ttu-id="edc89-508">Neutrals: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.</span><span class="sxs-lookup"><span data-stu-id="edc89-508">Neutrals: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.</span></span>

<span data-ttu-id="edc89-509">O processo de cálculo de desvios de cores medidos para obter as desvios para os primários de dispositivos é mais crítico para os LCDs do que para CRTs.</span><span class="sxs-lookup"><span data-stu-id="edc89-509">The process of averaging measured color chromaticies to obtain the chromaticities for the device primaries is more critical for LCDs than it is for CRTs.</span></span> <span data-ttu-id="edc89-510">Quando as medições da XYZ são plotadas no plano *XY* de desvio, uma situação típica é mostrada na Figura 1.</span><span class="sxs-lookup"><span data-stu-id="edc89-510">When XYZ measurements are plotted on the chromaticity *xy* -plane, a typical situation is shown in Figure 1.</span></span> <span data-ttu-id="edc89-511">Observe como a desvio é descompasso em direção ao ponto preto.</span><span class="sxs-lookup"><span data-stu-id="edc89-511">Notice how the chromaticity drifts toward the black point.</span></span> <span data-ttu-id="edc89-512">Isso ocorre porque todos os LCDs têm uma certa quantidade de vazamento de luz.</span><span class="sxs-lookup"><span data-stu-id="edc89-512">This is because all LCDs have a certain amount of light leakage.</span></span>

![Diagrama que mostra um grafo da desvio usando dados brutos sem correção.](images/cdmp-lcd-dmp-figure1.png)

<span data-ttu-id="edc89-514">**Figura 1** : o diagrama de desvios usando dados brutos sem correção</span><span class="sxs-lookup"><span data-stu-id="edc89-514">**Figure 1** : The chromaticity diagram using raw data with no correction</span></span>

<span data-ttu-id="edc89-515">Quando isso é subtraído das medidas brutas da XYZ, uma situação típica é descrita na Figura 2.</span><span class="sxs-lookup"><span data-stu-id="edc89-515">When this is subtracted from the raw XYZ measurements, a typical situation is depicted in Figure 2.</span></span> <span data-ttu-id="edc89-516">Os pontos Tnão agora são clusterizados sobre três centros, embora eles não fiquem idênticos neles.</span><span class="sxs-lookup"><span data-stu-id="edc89-516">Tthe points are now clustered about three centers, although they don't fall identically on them.</span></span> <span data-ttu-id="edc89-517">O processo de média descrito para CRTs melhora muito os resultados de LCDs.</span><span class="sxs-lookup"><span data-stu-id="edc89-517">The averaging process described for CRTs greatly improves the results for LCDs.</span></span>

![Diagrama que mostra um grafo da desvio usando dados brutos com um ponto preto ajustado.](images/cdmp-lcd-dmp-figure2.png)

<span data-ttu-id="edc89-519">**Figura 2** : o diagrama de desvios usando dados com o ponto preto ajustado</span><span class="sxs-lookup"><span data-stu-id="edc89-519">**Figure 2** : The chromaticity diagram using data with adjusted black point</span></span>

### <a name="rgb-capture-device-model-baseline"></a><span data-ttu-id="edc89-520">Linha de base do modelo do dispositivo de captura RGB</span><span class="sxs-lookup"><span data-stu-id="edc89-520">RGB Capture Device Model Baseline</span></span>

<span data-ttu-id="edc89-521">O modelo de dispositivo de captura RGB de linha de base é uma subclasse da classe IDeviceModel.</span><span class="sxs-lookup"><span data-stu-id="edc89-521">The baseline RGB capture device model is a subclass of the IDeviceModel class.</span></span> <span data-ttu-id="edc89-522">Na caracterização de colorimétrico de dispositivos de captura de cor, como scanners e câmeras digitais, a abordagem a seguir é usada.</span><span class="sxs-lookup"><span data-stu-id="edc89-522">In the colorimetric characterization of color capture devices, such as scanners and digital cameras, the following approach is used.</span></span> <span data-ttu-id="edc89-523">Um destino que consiste em patches de cor com valores CIEXYZ conhecidos é capturado usando o dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="edc89-523">A target consisting of color patches with known CIEXYZ values is captured using the capture device.</span></span> <span data-ttu-id="edc89-524">O resultado da captura é uma imagem de bitmap RGB na qual a cor de cada patch é codificada em um valor RGB.</span><span class="sxs-lookup"><span data-stu-id="edc89-524">The result of the capture is an RGB bitmap image in which the color of each patch is encoded in an RGB value.</span></span> <span data-ttu-id="edc89-525">Esses valores RGB de dispositivo são específicos de um dispositivo de captura específico.</span><span class="sxs-lookup"><span data-stu-id="edc89-525">These device RGB values are specific to a particular capture device.</span></span> <span data-ttu-id="edc89-526">O objetivo da caracterização de colorimétrico é estabelecer uma relação de empírica entre os valores RGB do dispositivo e os valores de CIEXYZ, ou uma transformação matemática de RGB para XYZ que modela de forma mais precisa o comportamento do dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="edc89-526">The goal of colorimetric characterization is to establish an empirical relationship between the device RGB values and CIEXYZ values, or a mathematical transformation from RGB to XYZ that models as accurately as possible the behavior of the capture device.</span></span>

<span data-ttu-id="edc89-527">Essa transformação matemática pode ser modelada razoavelmente por polinomiais de baixo grau.</span><span class="sxs-lookup"><span data-stu-id="edc89-527">Such a mathematical transformation can be modeled reasonably by polynomials of low degrees.</span></span> <span data-ttu-id="edc89-528">Esse procedimento é detalhado na literatura, por exemplo, Kang \[ 92 \] , Kang \[ 97 \] .</span><span class="sxs-lookup"><span data-stu-id="edc89-528">This procedure is detailed in the literature, for example Kang\[92\], Kang\[97\].</span></span> <span data-ttu-id="edc89-529">No Kang \[ 97 \] , uma abordagem é relatada que usa um conjunto de três polinomiais com 3, 6, 8, 9, 11, 14 ou 20 termos nas variáveis R, G e B, enquanto os três polinomiais retornam, respectivamente, para os componentes X, Y e Z do espaço CIEXYZ.</span><span class="sxs-lookup"><span data-stu-id="edc89-529">In Kang\[97\], an approach is reported that uses a set of three polynomials with 3, 6, 8, 9, 11, 14 or 20 terms in the R, G, and B variables, while the three polynomials regress respectively into the X, Y, Z components of the CIEXYZ space.</span></span> <span data-ttu-id="edc89-530">Para o polinomial de 20 termos, o formulário é:</span><span class="sxs-lookup"><span data-stu-id="edc89-530">For the 20-term polynomial, the form is:</span></span>

![Mostra o polinomial de 20 termos.](images/cdmp-formula20.png)

<span data-ttu-id="edc89-532">Há expressões semelhantes para Y e Z. A técnica matemática para ajustar os polinomiais cai dentro de "regressão linear multivariada" e é descrita em qualquer texto elementar em estatísticas.</span><span class="sxs-lookup"><span data-stu-id="edc89-532">There are similar expressions for Y and Z. The mathematical technique for fitting the polynomials falls within "Multivariate Linear Regression" and is described in any elementary text in Statistics.</span></span>

<span data-ttu-id="edc89-533">Esse método de regressão linear sofre de não minimizar a função de objetivo "certa".</span><span class="sxs-lookup"><span data-stu-id="edc89-533">This method of linear regression suffers from not minimizing the "right" objective function.</span></span> <span data-ttu-id="edc89-534">Por design, a regressão linear localiza a solução de quadrados mínimos, o que implica que os coeficientes obtidos minimizarão a soma total dos quadrados de erros no espaço subjacente ou, de forma equivalente, a soma dos quadrados das distâncias euclidiana.</span><span class="sxs-lookup"><span data-stu-id="edc89-534">By design, linear regression finds the least squares solution, which implies that the coefficients obtained will minimize the total sum of squares of errors in the underlying space, or equivalently, the sum of squares of the Euclidean distances.</span></span> <span data-ttu-id="edc89-535">Na prática, você deseja minimizar a soma dos quadrados de? Es, onde? E é um dos padrões aceitos, como CIE94.</span><span class="sxs-lookup"><span data-stu-id="edc89-535">In practice, you want to minimize the sum of squares of ?Es, where ?E is one of the accepted standards such as CIE94.</span></span> <span data-ttu-id="edc89-536">Minimizar essa função objetiva é um problema de regressão não linear.</span><span class="sxs-lookup"><span data-stu-id="edc89-536">Minimizing this objective function is a nonlinear regression problem.</span></span>

<span data-ttu-id="edc89-537">No novo mecanismo, o laboratório para a XYZ é o espaço de cores CIE que é resumido, e o polinomial cúbico de 20 termos é usado como modelo para o dispositivo de captura ou coeficientes ls, como a BS, de modo que os seguintes polinomiais minimizem a soma dos quadrados de? E <sub>CIE94</sub> s.</span><span class="sxs-lookup"><span data-stu-id="edc89-537">In the new engine, Lab to XYZ is the CIE color space that is regressed into, and the 20-term cubic polynomial is used as the model for the capture device, or coefficients ls,as,bs such that the following polynomials minimize the sum of squares of ?E <sub>CIE94</sub> s.</span></span>

![Mostra um conjunto de fórmulas polinomiais.](images/cdmp-formula21.png)

<span data-ttu-id="edc89-539">A solução ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub></sub>* ) no espaço numérico real de 60-dimensional **R** 203 deve ser de modo que o seguinte erro total seja minimizado:</span><span class="sxs-lookup"><span data-stu-id="edc89-539">The solution ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) in the 60-dimensional real numeric space **R** 203 must be such that the following total error is minimized:</span></span>

![Mostra o erro total a ser minimizado.](images/cdmp-formula22.png)

<span data-ttu-id="edc89-541">onde a soma é por todos os pares de pontos de dados (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub></sub>* i,*u <sub>i</sub>*,*v <sub>i</sub>* ) no conjunto de dados amostrado mais pontos de controle adicionais a serem detalhados no seguinte.</span><span class="sxs-lookup"><span data-stu-id="edc89-541">where the summation is through all the data point pairs (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub>i</sub>*,*v<sub>i</sub>* ) in the sampled data set plus additional control points to be detailed in the following.</span></span> <span data-ttu-id="edc89-542">Este é um problema de regressão não linear porque os parâmetros *?<sub> i</sub>*, *i <sub></sub>*\* <sub>eu</sub>\* inseri a função Objective de forma não linear (não quadráticamente).</span><span class="sxs-lookup"><span data-stu-id="edc89-542">This is a nonlinear regression problem because the parameters *?<sub>i</sub>*, *a<sub>i</sub>*, \* <sub>i</sub>\* enter into the objective function in a nonlinear way (not quadratically).</span></span>

<span data-ttu-id="edc89-543">Porque a função Objective?</span><span class="sxs-lookup"><span data-stu-id="edc89-543">Because the objective function ?</span></span> <span data-ttu-id="edc89-544">é uma função não linear (e não quadrática) dos parâmetros *?<sub> i</sub>*, *i <sub></sub> e \*\* <sub>i</sub>*, você deve recorrer a técnicas iterativas para resolver o problema de otimização.</span><span class="sxs-lookup"><span data-stu-id="edc89-544">is a nonlinear (and nonquadratic) function of the parameters *?<sub>i</sub>*, *a<sub>i</sub>* and \* <sub>i</sub>\*, you must resort to iterative techniques to solve the optimization problem.</span></span> <span data-ttu-id="edc89-545">Como a forma da função Objective é uma soma de quadrados, uma técnica de otimização padrão chamada de Levenberg-Marquardt algoritmo é usada.</span><span class="sxs-lookup"><span data-stu-id="edc89-545">Because the form of the objective function is a sum of squares, a standard optimization technique called the Levenberg-Marquardt algorithm is used.</span></span> <span data-ttu-id="edc89-546">Ele é considerado o método de escolha para problemas de quadrados não lineares.</span><span class="sxs-lookup"><span data-stu-id="edc89-546">It is considered the method of choice for nonlinear least squares problems.</span></span> <span data-ttu-id="edc89-547">Para algoritmos iterativos como Levenberg-Marquardt, você deve fornecer uma estimativa inicial.</span><span class="sxs-lookup"><span data-stu-id="edc89-547">For iterative algorithms such as Levenberg-Marquardt, you must supply an initial guess.</span></span> <span data-ttu-id="edc89-548">Uma boa estimativa inicial é geralmente crítica na localização do valor mínimo correto.</span><span class="sxs-lookup"><span data-stu-id="edc89-548">A good initial guess is usually critical in finding the correct minimum value.</span></span> <span data-ttu-id="edc89-549">Nesse caso, um bom candidato para a estimativa inicial é a solução do problema de regressão linear.</span><span class="sxs-lookup"><span data-stu-id="edc89-549">In this case, one good candidate for the initial guess is the solution of the linear regression problem.</span></span> <span data-ttu-id="edc89-550">Primeiro, minimize a soma do quadrado de distâncias de euclidiana no espaço do laboratório, definindo uma função de objetivo de quadrática:</span><span class="sxs-lookup"><span data-stu-id="edc89-550">First, minimize the sum of the square of Euclidean distances in Lab space, by defining a quadratic objective function:</span></span>

![Mostra uma função de objetivo quadrática definida.](images/cdmp-formula23.png)

<span data-ttu-id="edc89-552">A solução matemática para esse problema de "quadrados mínimos lineares" é bem conhecida.</span><span class="sxs-lookup"><span data-stu-id="edc89-552">The mathematical solution to such "linear least squares" problem is well known.</span></span> <span data-ttu-id="edc89-553">Porque *?<sub></sub>só aparece* na modelagem *L* , *um <sub>i</sub>* só aparece na modelagem *u* e \* <sub>i</sub>\* aparece apenas na modelagem *v* ; o problema de otimização pode ser decomposto em três subproblemas: um para *L*, um para *u* e outro para *v*.</span><span class="sxs-lookup"><span data-stu-id="edc89-553">Because *?<sub>i</sub>* only appears in the *L* modeling, *a <sub>i</sub>* only appears in the *u* modeling, and \* <sub>i</sub>\* only appears in the *v* modeling; the optimization problem can be decomposed into three subproblems: one for *L*, one for *u* and one for *v*.</span></span> <span data-ttu-id="edc89-554">Considere as equações *L* .</span><span class="sxs-lookup"><span data-stu-id="edc89-554">Consider the *L* equations.</span></span> <span data-ttu-id="edc89-555">(As equações *u* e as equações *v* seguem exatamente o mesmo argumento.) O problema de minimizar a soma dos quadrados de erros em *L* pode ser declarado como solução da equação de matriz a seguir no sentido mínimo de quadrados:</span><span class="sxs-lookup"><span data-stu-id="edc89-555">(The *u* equations and the *v* equations follow exactly the same argument.) The problem of minimizing the sum of squares of errors in *L* can be stated as solving the following matrix equation in the least squares sense:</span></span>

![Mostra uma equação de matriz para L.](images/cdmp-formula24.png)

<span data-ttu-id="edc89-557">em que *N* é o número total de pontos de dados (pontos de amostra originais, mais pontos de controle criados de uma maneira descrita abaixo).</span><span class="sxs-lookup"><span data-stu-id="edc89-557">where *N* is the total number of data points (original sampled points plus control points created in a manner described below).</span></span> <span data-ttu-id="edc89-558">Normalmente, *N* é muito maior que 20, então a equação anterior é excessivamente determinada, exigindo uma solução de mínimo de quadrados.</span><span class="sxs-lookup"><span data-stu-id="edc89-558">Typically, *N* is much larger than 20, so the preceding equation is over-determined, requiring a least squares solution.</span></span> <span data-ttu-id="edc89-559">Uma solução de formulário fechado para o **?**</span><span class="sxs-lookup"><span data-stu-id="edc89-559">A closed form solution for **?**</span></span> <span data-ttu-id="edc89-560">está disponível:</span><span class="sxs-lookup"><span data-stu-id="edc89-560">is available:</span></span>

![Mostra uma solução de formulário fechado.](images/cdmp-formula25.png)

<span data-ttu-id="edc89-562">Na prática, a avaliação direta usando a solução de formulário fechado não é usada porque ela tem propriedades numéricas inadequadas.</span><span class="sxs-lookup"><span data-stu-id="edc89-562">In practice, direct evaluation using the closed form solution is not used because it has poor numerical properties.</span></span> <span data-ttu-id="edc89-563">Em vez disso, algum tipo de algoritmo de fatoração de matriz é aplicado à matriz de coeficiente que reduz o sistema de equações a um formato canônico.</span><span class="sxs-lookup"><span data-stu-id="edc89-563">Instead, some kind of matrix factorization algorithm is applied to the coefficient matrix which reduces the system of equations to a canonical form.</span></span> <span data-ttu-id="edc89-564">Na implementação atual, a decomposição de valor singular (SVD) é aplicada à matriz **R** e, em seguida, o sistema decomposto resultante é resolvido.</span><span class="sxs-lookup"><span data-stu-id="edc89-564">In the current implementation, Singular Value Decomposition (SVD) is applied to the matrix **R** and then the resulting decomposed system is solved.</span></span>

<span data-ttu-id="edc89-565">A solução para o problema de regressão linear, indicada por ![ mostra a solução para o problema de regressão linear.](images/cdmp-formula26.png)</span><span class="sxs-lookup"><span data-stu-id="edc89-565">The solution to the linear regression problem, denoted by ![Shows the solution to the linear regression problem.](images/cdmp-formula26.png)</span></span> <span data-ttu-id="edc89-566">, é usado como o ponto de partida do algoritmo de Levenberg-Marquardt.</span><span class="sxs-lookup"><span data-stu-id="edc89-566">, is used as the starting point of the Levenberg-Marquardt algorithm.</span></span> <span data-ttu-id="edc89-567">Nesse algoritmo, uma etapa de avaliação é computada que deve mover o ponto mais próximo da solução ideal.</span><span class="sxs-lookup"><span data-stu-id="edc89-567">In this algorithm, a trial step is computed that should move the point closer to the optimal solution.</span></span> <span data-ttu-id="edc89-568">A etapa de avaliação atende a um conjunto de equações lineares que dependem do valor funcional e dos valores das derivações no ponto atual.</span><span class="sxs-lookup"><span data-stu-id="edc89-568">The trial step satisfies a set of linear equations dependent on the functional value and values of the derivatives at the current point.</span></span> <span data-ttu-id="edc89-569">Por esse motivo, as derivações da função Objective?</span><span class="sxs-lookup"><span data-stu-id="edc89-569">For this reason, the derivatives of the objective function ?</span></span> <span data-ttu-id="edc89-570">com relação aos parâmetros *?<sub> i</sub>*, *eu tenho entradas <sub></sub> necessárias para o <sub>algoritmo</sub>* de Levenberg-Marquardt.</span><span class="sxs-lookup"><span data-stu-id="edc89-570">with respect to the parameters *?<sub>i</sub>*, *a<sub>i</sub> <sub>i</sub>* are required inputs to the Levenberg-Marquardt algorithm.</span></span> <span data-ttu-id="edc89-571">Embora existam 60 parâmetros, há um atalho que permite que você computar muito menos.</span><span class="sxs-lookup"><span data-stu-id="edc89-571">Although there are 60 parameters, there is a shortcut that allows you to compute a lot less.</span></span> <span data-ttu-id="edc89-572">Pela regra de cadeia de cálculo,</span><span class="sxs-lookup"><span data-stu-id="edc89-572">By the Chain Rule of Calculus,</span></span>

![Mostra uma equação que permite um atalho usando a regra de cadeia de cálculo.](images/cdmp-formula27.png)

<span data-ttu-id="edc89-574">em *que j* = 1, 2,, 20 *, L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* é o valor CIELAB do ponto de exemplo *i* -i, e *R <sub>IJ</sub>* é a entrada (*i*,*j* ) th da matriz **R** definida acima.</span><span class="sxs-lookup"><span data-stu-id="edc89-574">where *j* = 1, 2,  , 20, *L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* are the CIELAB value of the *i* th sample point, and *R <sub>ij</sub>* is the (*i*,*j* )th entry of the matrix **R** defined above.</span></span> <span data-ttu-id="edc89-575">Então, em vez de calcular derivativos para parâmetros 60, você pode calcular derivativos para *L*,*a* e *b* usando diferenciação de encaminhamento numérico.</span><span class="sxs-lookup"><span data-stu-id="edc89-575">So instead of computing derivatives for 60 parameters, you can compute derivatives for *L*,*a*, and *b* using numerical forward differencing.</span></span>

<span data-ttu-id="edc89-576">Também é necessário configurar um critério de interrupção para algoritmos iterativos.</span><span class="sxs-lookup"><span data-stu-id="edc89-576">It is also necessary to set up a stopping criterion for iterative algorithms.</span></span> <span data-ttu-id="edc89-577">Na implementação atual, as iterações serão encerradas se o DECIE94 quadrado médio for menor que 1 ou o número de iterações executadas exceder 10.</span><span class="sxs-lookup"><span data-stu-id="edc89-577">In the current implementation, the iterations are terminated if the mean square DECIE94 is less than 1, or the number of iterations performed has exceeded 10.</span></span> <span data-ttu-id="edc89-578">O número 10 vem da experiência prática que se as primeiras iterações não reduzem o erro significativamente, as iterações adicionais não ajudarão muito além da movimentação do ponto de uma maneira oscillatory, ou seja, o algoritmo pode não convergir.</span><span class="sxs-lookup"><span data-stu-id="edc89-578">The number 10 comes from the practical experience that if the first few iterations do not reduce the error significantly, further iterations would not help much other than moving the point in an oscillatory manner, i.e., the algorithm may not converge.</span></span> <span data-ttu-id="edc89-579">Mesmo no caso de o algoritmo divergir, podemos ter certeza de que o DECIE94 não é pior do que começamos, ou seja, com os parâmetros obtidos da regressão linear.</span><span class="sxs-lookup"><span data-stu-id="edc89-579">Even in the case that the algorithm diverges, we can be sure that the DECIE94 is no worse than what we started, i.e. with the parameters obtained from linear regression.</span></span>

<span data-ttu-id="edc89-580">Mesmo com o método anterior de regressão não linear, há vários problemas com o ajuste.</span><span class="sxs-lookup"><span data-stu-id="edc89-580">Even with the preceding method of nonlinear regression, there are several problems with the fitting.</span></span> <span data-ttu-id="edc89-581">Um problema é que os polinomiais tendem a exceder ou exceder os pontos de dados.</span><span class="sxs-lookup"><span data-stu-id="edc89-581">One problem is that the polynomials tend to overshoot or undershoot beyond the data points.</span></span> <span data-ttu-id="edc89-582">Máximo local artificial e mínimo podem ser introduzidos no processo de ajuste.</span><span class="sxs-lookup"><span data-stu-id="edc89-582">Artificial local maxima and minima may be introduced in the fitting process.</span></span> <span data-ttu-id="edc89-583">Isso pode ser imposto usando polinomiais de baixo grau, que é o motivo pelo qual você não deve usar mais de três graus.</span><span class="sxs-lookup"><span data-stu-id="edc89-583">This can be counteracted by using polynomials of low degree, which is the reason you should not use higher than three degrees.</span></span> <span data-ttu-id="edc89-584">Um aspecto mais sério de sobretratação ou inviabilidade é que, embora um polinomial possa pegar qualquer valor real teoricamente, o espaço que ele tenta modelar normalmente tem restrições físicas e restrições práticas.</span><span class="sxs-lookup"><span data-stu-id="edc89-584">A more serious aspect of overshooting or undershooting is that, while a polynomial can take any real value theoretically, the space it tries to model typically has physical constraints and practical constraints.</span></span> <span data-ttu-id="edc89-585">CIEXYZ deve ter todos os X, Y, Z não negativos, que é uma restrição física.</span><span class="sxs-lookup"><span data-stu-id="edc89-585">CIEXYZ must have all of X, Y, Z non-negative, which is a physical constraint.</span></span> <span data-ttu-id="edc89-586">Na prática, eles só usam valores na magnitude de centenas, não milhares ou mais.</span><span class="sxs-lookup"><span data-stu-id="edc89-586">In practice, they only take values in the magnitude of hundreds, not thousands or higher.</span></span> <span data-ttu-id="edc89-587">Da mesma forma, CIELAB ou CIELUV tem suas próprias restrições físicas e práticas.</span><span class="sxs-lookup"><span data-stu-id="edc89-587">Similarly, CIELAB or CIELUV has its own physical and practical constraints.</span></span> <span data-ttu-id="edc89-588">Quando o espaço em RGB é preenchido suficientemente com pontos de exemplo, o problema de sobreenchente ou de excedente não é sério.</span><span class="sxs-lookup"><span data-stu-id="edc89-588">When the RGB space is filled sufficiently with sample points, the problem of overshooting or undershooting is not serious.</span></span> <span data-ttu-id="edc89-589">No entanto, os pontos RGB capturados do dispositivo de captura geralmente não preenchem o espaço RGB uniformemente.</span><span class="sxs-lookup"><span data-stu-id="edc89-589">However, the captured RGB points from the capture device do not usually fill up the RGB space uniformly.</span></span> <span data-ttu-id="edc89-590">Os pontos podem preencher somente os 80% do cubo RGB ou pior, eles podem residir em um diversa dimensional inferior.</span><span class="sxs-lookup"><span data-stu-id="edc89-590">The points may fill up only inner the 80% of the RGB cube, or worse, they may reside in a lower dimensional manifold.</span></span> <span data-ttu-id="edc89-591">Quando isso acontece, os polinomiais regressados podem fazer um trabalho ruim na extrapolação dos valores além dos pontos de dados, às vezes retornando previsões irreais.</span><span class="sxs-lookup"><span data-stu-id="edc89-591">When this happens, the regressed polynomials may do a poor job at extrapolating the values beyond the data points, sometimes returning unrealistic predictions.</span></span> <span data-ttu-id="edc89-592">Você quer um modelo que sempre retorne valores razoavelmente realistas.</span><span class="sxs-lookup"><span data-stu-id="edc89-592">You want a model that always returns reasonably realistic values.</span></span> <span data-ttu-id="edc89-593">Isso requer um método que possa controlar efetivamente o comportamento do limite de polinomiais de regressão, impondo custos adicionais a esses polinomiais que se comportam incorretamente perto do limite do cubo RGB.</span><span class="sxs-lookup"><span data-stu-id="edc89-593">This requires a method that can effectively control the boundary behavior of regression polynomials by imposing additional cost to those polynomials that behave erratically near the boundary of the RGB cube.</span></span> <span data-ttu-id="edc89-594">Uma medida adicional para garantir que os polinomiais sempre retornam valores realistas são aplicados recortando a saída para dentro do local de CIE Spectral.</span><span class="sxs-lookup"><span data-stu-id="edc89-594">A further measure to ensure that the polynomials always return realistic values is applied by clipping the output to within the CIE spectral locus.</span></span>

<span data-ttu-id="edc89-595">É nesse momento que a modelagem do scanner e a modelagem da câmera divergem uma da outra.</span><span class="sxs-lookup"><span data-stu-id="edc89-595">It is at this point that the scanner modeling and camera modeling diverge from each other.</span></span> <span data-ttu-id="edc89-596">Espera-se que o modelo de câmera expanda para regiões além dos pontos de amostra, incluindo os "realces especulares", a mesma extrapolação não é necessária para o modelo do scanner.</span><span class="sxs-lookup"><span data-stu-id="edc89-596">The camera model is expected to extrapolate to regions beyond the sampled points including the "specular highlights," the same extrapolation is not required for the scanner model.</span></span> <span data-ttu-id="edc89-597">Espera-se que o destino do scanner cubra uma caracterização semelhante aos materiais impressos a serem verificados.</span><span class="sxs-lookup"><span data-stu-id="edc89-597">The scanner target is expected to cover a characterization that is similar to the printed materials to be scanned.</span></span> <span data-ttu-id="edc89-598">O modelo do verificador ainda precisa ser robusto no sentido de que ele não deve retornar valores irreais, mas extrapolação muito além da meta de caracterização não é necessária.</span><span class="sxs-lookup"><span data-stu-id="edc89-598">The scanner model is still required to be robust in the sense that it should not return unrealistic values, but extrapolation far beyond the characterization target is not required.</span></span> <span data-ttu-id="edc89-599">Para garantir a robustez, o L-polinomial acima é recortado em 100, ou seja, o modelo polinomial é forçado a não extrapolar além de "DMín" do destino do scanner.</span><span class="sxs-lookup"><span data-stu-id="edc89-599">To ensure robustness, the L-polynomial above is clipped at 100, that is, the polynomial model is forced not to extrapolate beyond "Dmin" of the scanner target.</span></span>

<span data-ttu-id="edc89-600">Espera-se que o modelo de câmera expanda para os realces especulares, de modo que o recorte em 100 é indesejável.</span><span class="sxs-lookup"><span data-stu-id="edc89-600">The camera model is expected to extrapolate to specular highlights, so clipping at 100 is undesirable.</span></span> <span data-ttu-id="edc89-601">Em vez disso, o algoritmo a seguir é usado.</span><span class="sxs-lookup"><span data-stu-id="edc89-601">Instead, the following algorithm is used.</span></span>

<span data-ttu-id="edc89-602">Pontos de controle artificial são introduzidos para controlar o comportamento dos polinomiais em regiões com amostragem insuficiente.</span><span class="sxs-lookup"><span data-stu-id="edc89-602">Artificial control points are introduced to control the behavior of the polynomials in regions with insufficient sampling.</span></span> <span data-ttu-id="edc89-603">Ao posicionar estrategicamente esses pontos de controle com os valores apropriados, eles servem para "efetuar pull" das polinomiais na direção necessária.</span><span class="sxs-lookup"><span data-stu-id="edc89-603">By strategically placing these control points with appropriate values, they serve to "pull" the polynomials in the required direction.</span></span> <span data-ttu-id="edc89-604">Na implementação atual, são usados oito pontos de controle correspondentes aos cantos do cubo RGB.</span><span class="sxs-lookup"><span data-stu-id="edc89-604">In the current implementation, eight control points corresponding to the corners of the RGB cube are used.</span></span> <span data-ttu-id="edc89-605">Se os valores do dispositivo forem normalizados para o Unity, esses pontos serão:</span><span class="sxs-lookup"><span data-stu-id="edc89-605">If the device values are normalized to unity, then these points are:</span></span>

<span data-ttu-id="edc89-606">*R* = 0, *G* = 0, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="edc89-606">*R* = 0, *G* = 0, *B* = 0</span></span>

<span data-ttu-id="edc89-607">*R* = 0, *G* = 0, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="edc89-607">*R* = 0, *G* = 0, *B* = 1</span></span>

<span data-ttu-id="edc89-608">*R* = 0, *G* = 1, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="edc89-608">*R* = 0, *G* = 1, *B* = 0</span></span>

<span data-ttu-id="edc89-609">*R* = 0.</span><span class="sxs-lookup"><span data-stu-id="edc89-609">*R* = 0.</span></span> <span data-ttu-id="edc89-610">*G* = 1, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="edc89-610">*G* = 1, *B* = 1</span></span>

<span data-ttu-id="edc89-611">*R* = 1, *G* = 0, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="edc89-611">*R* = 1, *G* = 0, *B* = 0</span></span>

<span data-ttu-id="edc89-612">*R* = 1, *G* = 0, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="edc89-612">*R* = 1, *G* = 0, *B* = 1</span></span>

<span data-ttu-id="edc89-613">*R* = 1, *G* = 1, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="edc89-613">*R* = 1, *G* = 1, *B* = 0</span></span>

<span data-ttu-id="edc89-614">*R* = 1, *G* = 1, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="edc89-614">*R* = 1, *G* = 1, *B* = 1</span></span>

<span data-ttu-id="edc89-615">Exceto para o *R*  = *G*  = *B* = 1, que está associado a um valor de CIELAB de *L* = 100, *u*  = *v* = 0, o seguinte algoritmo de extrapolação é usado para determinar o valor de CIELAB apropriado a ser associado.</span><span class="sxs-lookup"><span data-stu-id="edc89-615">Except for the white *R* =*G* =*B* = 1, which is associated with a CIELAB value of *L* = 100, *u* =*v* = 0, the following extrapolation algorithm is used to determine the appropriate CIELAB value to be associated with.</span></span> <span data-ttu-id="edc89-616">Em geral, para um determinado (*r*,*g*,*b* ), um peso é associado a cada (*r <sub>i</sub>*,*g <sub>i</sub>*,*b <sub></sub>* ) no conjunto de dados de amostra.</span><span class="sxs-lookup"><span data-stu-id="edc89-616">Generally, for a given (*R*,*G*,*B* ), a weight is associated with each of the (*R <sub>i</sub>*,*G <sub>i</sub>*,*B<sub>i</sub>* ) in the sampled data set.</span></span> <span data-ttu-id="edc89-617">Há duas metas para atribuir o peso.</span><span class="sxs-lookup"><span data-stu-id="edc89-617">There are two goals to assigning the weight.</span></span> <span data-ttu-id="edc89-618">Primeiro, o peso é inversamente proporcional à distância entre (*r*,*G*,*B* ) e (*r <sub>i</sub>*,*G <sub>i</sub>*,*B <sub></sub>* ).</span><span class="sxs-lookup"><span data-stu-id="edc89-618">First, the weight is inversely proportional to the distance between (*R*,*G*,*B* ) and (*R <sub>i</sub>*,*G <sub>i</sub>*,*B<sub>i</sub>* ).</span></span> <span data-ttu-id="edc89-619">Em segundo lugar, você deseja descartar ou atribuir peso 0 a, pontos que têm um matiz diferente do determinado ponto (*R*,*G*,*B* ).</span><span class="sxs-lookup"><span data-stu-id="edc89-619">Second, you want to discard, or assign weight 0 to, points that have a different hue than the given point (*R*,*G*,*B* ).</span></span> <span data-ttu-id="edc89-620">Para levar o matiz em conta, considere os pontos que estão dentro de um cone cujo vértice esteja em (0, 0, 0), cujo eixo coincide com a linha unindo (0, 0, 0) a (*R*,*G*,*B* ) e cujo ângulo semivertical?</span><span class="sxs-lookup"><span data-stu-id="edc89-620">To take the hue into account, consider points that lie within a cone whose vertex is at (0, 0, 0), whose axis coincides with the line joining (0, 0, 0) to (*R*,*G*,*B* ), and whose semi-vertical angle ?</span></span> <span data-ttu-id="edc89-621">atende ao cos?</span><span class="sxs-lookup"><span data-stu-id="edc89-621">satisfies cos ?</span></span> <span data-ttu-id="edc89-622">= 0,9.</span><span class="sxs-lookup"><span data-stu-id="edc89-622">= 0.9.</span></span> <span data-ttu-id="edc89-623">Consulte a Figura 3 para obter uma ilustração desse cone.</span><span class="sxs-lookup"><span data-stu-id="edc89-623">See Figure 3 for an illustration of this cone.</span></span>

![Diagrama que mostra a forma da vizinhança.](images/cdmp-lcd-dmp-figure3.png)

<span data-ttu-id="edc89-625">**Figura 3** : filtrando os pontos de exemplo por ângulo e distância.</span><span class="sxs-lookup"><span data-stu-id="edc89-625">**Figure 3** : Filtering the sample points by angle and distance.</span></span> <span data-ttu-id="edc89-626">A forma da vizinhança representada é apenas para fins de ilustração.</span><span class="sxs-lookup"><span data-stu-id="edc89-626">The shape of the neighborhood depicted is for illustration purpose only.</span></span> <span data-ttu-id="edc89-627">A forma real depende da distância usada; é um ambiente em forma de losango se a norma 1 é usada.</span><span class="sxs-lookup"><span data-stu-id="edc89-627">The actual shape depends on the distance used; it is a diamond-shaped neighborhood if the 1-norm is used.</span></span>

<span data-ttu-id="edc89-628">Dentro desse cone, uma segunda filtragem é executada com base na distância RGB, que usa a norma 1, definida por</span><span class="sxs-lookup"><span data-stu-id="edc89-628">Within this cone, a second filtering is performed that is based on the RGB distance, which uses the 1-norm, defined by</span></span>

![Mostra a fórmula para a segunda filtragem dentro do cone.](images/cdmp-formula28.png)

<span data-ttu-id="edc89-630">Com o cone atual, a pesquisa inicial é para pontos que estão dentro de uma distância de 0,1 de (*R*,*G*,*B* ).</span><span class="sxs-lookup"><span data-stu-id="edc89-630">With the current cone, the initial search is for points that are within a distance of 0.1 from (*R*,*G*,*B* ).</span></span> <span data-ttu-id="edc89-631">Se nenhum ponto for encontrado nesse raio, o raio será aumentado em 0,1 e a pesquisa será reiniciada.</span><span class="sxs-lookup"><span data-stu-id="edc89-631">If no point is found within this radius, the radius is increased by 0.1, and the search is restarted.</span></span> <span data-ttu-id="edc89-632">Se as próximas redes redondas não forem apontadas, o raio será aumentado em 0,1.</span><span class="sxs-lookup"><span data-stu-id="edc89-632">If the next round nets no point either, the radius is increased by 0.1.</span></span> <span data-ttu-id="edc89-633">Esse processo continua até que o raio exceda MaxDist/5, em que MaxDist = 3, no caso de 1-Norma.</span><span class="sxs-lookup"><span data-stu-id="edc89-633">This process continues until the radius exceeds MaxDist/5, where MaxDist = 3, in the case of 1-norm.</span></span> <span data-ttu-id="edc89-634">Se nenhum ponto for encontrado, o cone será ampliado pela redução do cos?</span><span class="sxs-lookup"><span data-stu-id="edc89-634">If no point is found, the cone is enlarged by decreasing the cos ?</span></span> <span data-ttu-id="edc89-635">por 0, 5, ou seja, aumentando o ângulo?</span><span class="sxs-lookup"><span data-stu-id="edc89-635">by 0.05, that is, increasing the angle ?</span></span> <span data-ttu-id="edc89-636">e reiniciar todo o processo com um raio crescente.</span><span class="sxs-lookup"><span data-stu-id="edc89-636">and restarting the whole process with an increasing radius.</span></span> <span data-ttu-id="edc89-637">Esse processo continua até que um conjunto não vazio de pontos seja encontrado ou cos?</span><span class="sxs-lookup"><span data-stu-id="edc89-637">This process continues until a non-empty set of points is found, or cos ?</span></span> <span data-ttu-id="edc89-638">chega a 0, ou seja, o cone foi aberto para se tornar um plano.</span><span class="sxs-lookup"><span data-stu-id="edc89-638">reaches 0, that is, the cone has opened up to become a plane.</span></span> <span data-ttu-id="edc89-639">Neste ponto, a pesquisa é reiniciada aumentando o raio, exceto que a pesquisa continua até que o raio alcance MaxDist.</span><span class="sxs-lookup"><span data-stu-id="edc89-639">At this point, the search is restarted by increasing the radius, except that the search continues until the radius reaches MaxDist.</span></span> <span data-ttu-id="edc89-640">Isso garante que, no pior cenário, um conjunto de pontos não vazio será encontrado.</span><span class="sxs-lookup"><span data-stu-id="edc89-640">This guarantees that in the worst-case scenario, a non-empty set of points will be found.</span></span> <span data-ttu-id="edc89-641">O algoritmo é resumido no diagrama de fluxo da Figura 4.</span><span class="sxs-lookup"><span data-stu-id="edc89-641">The algorithm is summarized in the flow diagram in Figure 4.</span></span>

![Diagrama que mostra o fluxo do algoritmo.](images/cdmp-lcd-dmp-figure4.png)

<span data-ttu-id="edc89-643">**Figura 4** : diagrama de fluxo para determinar o conjunto de pontos de exemplo usados na extrapolação para um valor RGB de entrada</span><span class="sxs-lookup"><span data-stu-id="edc89-643">**Figure 4** : Flow diagram for determining the set S of sample points used in the extrapolation for an input RGB value</span></span>

<span data-ttu-id="edc89-644">Supondo que o processo anterior produza *um conjunto não* vazio de pontos (*R <sub>i</sub>*,*G <sub>i</sub>*, B) e correspondente (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), para cada um desses pontos, um peso *<sub></sub>* *w <sub></sub>* é atribuído, fornecido por</span><span class="sxs-lookup"><span data-stu-id="edc89-644">Assuming that the preceding process yields a non-empty set *S* of points (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) and corresponding (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), then for each such point, a weight *w<sub>i</sub>* is assigned, given by</span></span>

![Mostra a fórmula para um peso para cada ponto.](images/cdmp-formula29.png)

<span data-ttu-id="edc89-646">Por fim, o extrapolant é definido por</span><span class="sxs-lookup"><span data-stu-id="edc89-646">Finally, the extrapolant is defined by</span></span>

![Mostra a definição para o extrapolant.](images/cdmp-formula30.png)

<span data-ttu-id="edc89-648">As equações anteriores constituem uma instância dos "métodos com peso de distância inverso", normalmente chamados de métodos Shepard.</span><span class="sxs-lookup"><span data-stu-id="edc89-648">The preceding equations constitute an instance of the "inverse-distance weighted methods," commonly called the Shepard methods.</span></span> <span data-ttu-id="edc89-649">Ao executar cada um dos oito pontos de EQ (6) por meio do algoritmo, são obtidos oito pontos de controle, cada um com os valores *R*,*G*,*b* e *L*,*a*,*B* , que são colocados no pool com os dados de exemplo originais.</span><span class="sxs-lookup"><span data-stu-id="edc89-649">By running each of the eight points from eq (6) through the algorithm, eight control points are obtained, each with *R*,*G*,*B* and *L*,*a*,*b* values, which are put into the pool with the original sample data.</span></span>

<span data-ttu-id="edc89-650">Para garantir que o modelo sempre produza valores de cor válidos e a integridade do sistema e a estabilidade de todo o pipeline de processamento de cores, você deve executar um recorte final na saída do modelo polinomial.</span><span class="sxs-lookup"><span data-stu-id="edc89-650">To ensure that the model always produces valid color values and for system integrity and stability down the whole color processing pipeline, you must perform a final clipping to the output of the polynomial model.</span></span> <span data-ttu-id="edc89-651">A gama visual de CIE é descrita pelo componente Achromatic (*Y* ou *L* ) e o componente de desvio (*dispersão* ou *a'b '*, que estão relacionados ao espaço XYZ por uma transformação projetada).</span><span class="sxs-lookup"><span data-stu-id="edc89-651">The CIE visual gamut is described by the achromatic component (*Y* or *L* ) and the chromatic component (*xy* or *a'b'*, which are related to the XYZ space by a projective transformation).</span></span> <span data-ttu-id="edc89-652">Na implementação atual, a desvio de *a'b* é usada porque está diretamente relacionada ao espaço de CIELUV.</span><span class="sxs-lookup"><span data-stu-id="edc89-652">In the current implementation, the *a'b'* chromaticity is used because it is directly related to the CIELUV space.</span></span> <span data-ttu-id="edc89-653">Para qualquer valor de *CIELAB* , primeiro recorte de *L* para um valor não negativo:</span><span class="sxs-lookup"><span data-stu-id="edc89-653">For any *CIELAB* value, first clip *L* to a non-negative value:</span></span>

![Mostra o recorte de L para um valor não negativo.](images/cdmp-formula31.png)

<span data-ttu-id="edc89-655">Para permitir a extrapolação de realces especulares, *L* não é recortado em 100, o limite superior "convencional" para *L* no espaço do laboratório.</span><span class="sxs-lookup"><span data-stu-id="edc89-655">To allow extrapolation for specular highlights, *L* is not clipped at 100, the "conventional" upper bound for *L* in Lab space.</span></span>

<span data-ttu-id="edc89-656">Em seguida, se *L* = 0, *a* e *b* serão recortados de forma que a *= b =* 0.</span><span class="sxs-lookup"><span data-stu-id="edc89-656">Next, if *L* = 0, then *a* and *b* are clipped such that a *= b =* 0.</span></span> <span data-ttu-id="edc89-657">Se for *L* ?</span><span class="sxs-lookup"><span data-stu-id="edc89-657">If *L* ?</span></span> <span data-ttu-id="edc89-658">0, calcular</span><span class="sxs-lookup"><span data-stu-id="edc89-658">0, calculate</span></span>

![Mostra a fórmula se L = 0.](images/cdmp-formula32.png)

<span data-ttu-id="edc89-660">Estes são os componentes de um vetor no diagrama *a'b* do ponto branco (*u? '*,*v? '*</span><span class="sxs-lookup"><span data-stu-id="edc89-660">These are the components of a vector in the *a'b'* diagram from the white point (*u?'*,*v?'*</span></span> <span data-ttu-id="edc89-661">) à cor em questão.</span><span class="sxs-lookup"><span data-stu-id="edc89-661">) to the color in question.</span></span> <span data-ttu-id="edc89-662">Definir o local de CIE Spectral como convexa envoltória de todos os pontos (*a '*,*b '* ), parametrizados pelo comprimento de onda?:</span><span class="sxs-lookup"><span data-stu-id="edc89-662">Define the CIE spectral locus as the convex hull of all the points (*a'*,*b'* ), parameterized by the wavelength ?:</span></span>

![Mostra a fórmula para o comprimento de onda.](images/cdmp-formula33.png)

<span data-ttu-id="edc89-664">onde ![ mostra as funções para a correspondência de cores CIE.](images/cdmp-formula34.png)</span><span class="sxs-lookup"><span data-stu-id="edc89-664">where ![Shows the functions for CIE color-matching.](images/cdmp-formula34.png)</span></span> <span data-ttu-id="edc89-665">são as funções de correspondência de cores CIE para o observador de dois graus.</span><span class="sxs-lookup"><span data-stu-id="edc89-665">are the CIE color-matching functions for the 2-degree observer.</span></span> <span data-ttu-id="edc89-666">Se o vetor estiver fora do CIE local, a cor será recortada para o ponto na local CIE que é a interseção do local e a linha definida pelo vetor.</span><span class="sxs-lookup"><span data-stu-id="edc89-666">If the vector lies outside the CIE locus, the color is clipped to the point on the CIE locus that is the intersection of the locus and the line defined by the vector.</span></span> <span data-ttu-id="edc89-667">Consulte a Figura 5.</span><span class="sxs-lookup"><span data-stu-id="edc89-667">See Figure 5.</span></span> <span data-ttu-id="edc89-668">Se o recorte tiver ocorrido, o *valor a e* *b* será reconstruído pela primeira subtração *de um?*</span><span class="sxs-lookup"><span data-stu-id="edc89-668">If clipping has occurred, the *a* and *b* value is reconstructed by first subtracting *a?'*</span></span> <span data-ttu-id="edc89-669">e *b? '*</span><span class="sxs-lookup"><span data-stu-id="edc89-669">and *b?'*</span></span> <span data-ttu-id="edc89-670">de *um '* e *b '* recortado e, em seguida, multiplique por 13 *L*.</span><span class="sxs-lookup"><span data-stu-id="edc89-670">from the clipped *a'* and *b'*, and then multiplying by 13 *L*.</span></span>

![Diagrama que mostra o grafo para o algoritmo de recorte.](images/cdmp-lcd-dmp-figure5.png)

<span data-ttu-id="edc89-672">**Figura 5** : algoritmo de recorte para valores de laboratório que estão fora da gama visual de CIE</span><span class="sxs-lookup"><span data-stu-id="edc89-672">**Figure 5** : Clipping algorithm for Lab values that are outside the CIE visual gamut</span></span>

<span data-ttu-id="edc89-673">Na implementação atual, o local de CIE Spectral no plano de *a'b* é representado por uma curva linear piecewise com 35 segmentos (correspondendo a um comprimento de ondas de 360 nm a 700 nm, inclusive).</span><span class="sxs-lookup"><span data-stu-id="edc89-673">In the current implementation, the CIE spectral locus in the *a'b'* plane is represented by a piecewise linear curve with 35 segments (corresponding to a wavelength from 360 nm to 700 nm inclusive).</span></span> <span data-ttu-id="edc89-674">Ao ordenar os segmentos de linha para que seus ângulos de pagamento no ponto branco sejam crescentes, o que é equivalente a ondas decrescentes, o segmento de linha que cruza com o raio formado pelo vetor acima pode ser encontrado por uma pesquisa binária simples.</span><span class="sxs-lookup"><span data-stu-id="edc89-674">By ordering the line segments so that their subtended angles at the white point are ascending, which is equivalent to descending wavelengths, the line segment that intersects with the ray formed by the above vector can be found by a simple binary search.</span></span>

### <a name="rgb-printer-device-model-baseline"></a><span data-ttu-id="edc89-675">Linha de base de modelo de dispositivo de impressora RGB</span><span class="sxs-lookup"><span data-stu-id="edc89-675">RGB Printer Device Model Baseline</span></span>

<span data-ttu-id="edc89-676">A caracterização de um dispositivo de uma impressora RGB consiste em construir um modelo empírica do dispositivo que prevê a cor CIELUV independente do dispositivo para qualquer valor RGB determinado</span><span class="sxs-lookup"><span data-stu-id="edc89-676">A device characterization of a RGB printer consists of constructing an empirical model of the device that predicts the device-independent CIELUV color for any given RGB value</span></span>

<span data-ttu-id="edc89-677">Há duas maneiras de construir o modelo empírica.</span><span class="sxs-lookup"><span data-stu-id="edc89-677">There are two ways to construct the empirical model.</span></span> <span data-ttu-id="edc89-678">Uma maneira é usar os dados do dispositivo para uma impressora RGB e a outra é usar dados de parâmetros analíticos.</span><span class="sxs-lookup"><span data-stu-id="edc89-678">One way is to use the device data for a RGB printer, and the other is to use analytical parameter data.</span></span> <span data-ttu-id="edc89-679">Na primeira, os dados de medida fornecidos por um usuário para um dispositivo de impressora RGB são usados para construir a tabela de pesquisa 3-D (LUT).</span><span class="sxs-lookup"><span data-stu-id="edc89-679">In the first one, measurement data provided by a user for a RGB printer device is used to construct 3-D lookup table (LUT).</span></span> <span data-ttu-id="edc89-680">Os dados de medição consistem em valores de XYZ para patches RGB uniformemente amostrados.</span><span class="sxs-lookup"><span data-stu-id="edc89-680">The measurement data consists of XYZ values for uniformly sampled RGB patches.</span></span> <span data-ttu-id="edc89-681">Os tamanhos de amostragem típicos são 9 ou 17 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="edc89-681">Typical sampling sizes are 9 or 17 for each component.</span></span> <span data-ttu-id="edc89-682">Cada patch é medido com um colorimeter ou spectrophotometer no espaço CIEXYZ.</span><span class="sxs-lookup"><span data-stu-id="edc89-682">Each patch is measured with a colorimeter or spectrophotometer in CIEXYZ space.</span></span> <span data-ttu-id="edc89-683">O valor XYZ de um patch é então convertido em valor CIELUV, formando um LUT 3-D.</span><span class="sxs-lookup"><span data-stu-id="edc89-683">The XYZ value for a patch is then converted into CIELUV value, forming a 3-D LUT.</span></span> <span data-ttu-id="edc89-684">No modelo de dispositivo, o método de interpolação tetrahedral do Sakamoto é aplicado ao LUT 3D para prever os dados do CIELUV para determinados dados RGB.</span><span class="sxs-lookup"><span data-stu-id="edc89-684">In the device model, the Sakamoto's tetrahedral interpolation method is applied to the 3-D LUT in order to predict the CIELUV data for a given RGB data.</span></span> <span data-ttu-id="edc89-685">(Conf-US patente 4275413 (Sakamoto et al.), patente dos EUA 4511989 (Sakamoto), Kang \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="edc89-685">(Confer US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[1\].</span></span> <span data-ttu-id="edc89-686">As duas patentes mencionadas expiraram.).</span><span class="sxs-lookup"><span data-stu-id="edc89-686">The two patents mentioned have expired.).</span></span> <span data-ttu-id="edc89-687">Os dados de parâmetro analítico passados no segundo método são simplesmente um LUT que foi criado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="edc89-687">The analytical parameter data passed in the second method is simply a LUT that was built previously.</span></span> <span data-ttu-id="edc89-688">Normalmente, esse LUT foi criado usando o primeiro método, embora possa ser criado manualmente.</span><span class="sxs-lookup"><span data-stu-id="edc89-688">Typically, that LUT was built using the first method, although it could be hand-built.</span></span>

<span data-ttu-id="edc89-689">No gerenciamento de cores atual, o mapa de origem é definido como o mapa que passa do espaço RGB para um espaço de cores CIEXYZ independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="edc89-689">In the current color management, the source map is defined as the map that goes from RGB space to a device-independent CIEXYZ color space.</span></span> <span data-ttu-id="edc89-690">O mapa de destino é definido como o mapa que vai do espaço de cores CIEXYZ independente de dispositivo para o espaço RGB.</span><span class="sxs-lookup"><span data-stu-id="edc89-690">The destination map is defined as the map that goes from the device-independent CIEXYZ color space to RGB space.</span></span> <span data-ttu-id="edc89-691">É o inverso do mapa de origem.</span><span class="sxs-lookup"><span data-stu-id="edc89-691">It is the inverse of the source map.</span></span>

<span data-ttu-id="edc89-692">O modelo empírica é usado diretamente no mapa de origem.</span><span class="sxs-lookup"><span data-stu-id="edc89-692">The empirical model is directly used in the source map.</span></span> <span data-ttu-id="edc89-693">Ele primeiro mapeia determinados dados RGB em um CIELUV dados, que são convertidos em dados do XYZ.</span><span class="sxs-lookup"><span data-stu-id="edc89-693">It first maps a given RGB data into a CIELUV data, which is converted into XYZ data.</span></span> <span data-ttu-id="edc89-694">No mapa de destino, os dados de CIEXYZ independentes do dispositivo são convertidos primeiro em dados do CIELUV.</span><span class="sxs-lookup"><span data-stu-id="edc89-694">In the destination map, device-independent CIEXYZ data is first converted into CIELUV data.</span></span> <span data-ttu-id="edc89-695">Em seguida, o modelo empírica e o método clássico Newton-Raphson são usados para prever os melhores dados RGB para os dados de CIELUV.</span><span class="sxs-lookup"><span data-stu-id="edc89-695">Then, the empirical model and the classical Newton-Raphson method are used to predict the best RGB data for the CIELUV data.</span></span> <span data-ttu-id="edc89-696">Os detalhes sobre a conversão de CieLUV para dados RGB são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="edc89-696">The details about conversion from CieLUV to RGB data are as follows:</span></span>

<span data-ttu-id="edc89-697">Depois de gerar um LUT de 3D de RGB para CieLUV, o mapa de RGB para LUV é criado usando a interpolação de tetrahedral em RGB.</span><span class="sxs-lookup"><span data-stu-id="edc89-697">After generating a 3-D LUT from RGB to CieLUV, the map from RGB to LUV is built using tetrahedral interpolation on RGB.</span></span> <span data-ttu-id="edc89-698">Este mapa é indicado pelas seguintes equações:</span><span class="sxs-lookup"><span data-stu-id="edc89-698">This map is denoted by the following equations:</span></span>

![Mostra as equações do mapa de R G B a L U V.](images/cdmp-image125.png)

<span data-ttu-id="edc89-700">A inversão do mapa consiste em resolver, para qualquer cor</span><span class="sxs-lookup"><span data-stu-id="edc89-700">Inversion of the map consists of solving, for any color</span></span> ![Mostra L U V.](images/cdmp-image127.png) <span data-ttu-id="edc89-702">, o seguinte sistema de equações não lineares:</span><span class="sxs-lookup"><span data-stu-id="edc89-702">, the following system of nonlinear equations:</span></span>

![Mostra as equações não lineares para lolving qualquer cor L U V.](images/cdmp-image129.png)

<span data-ttu-id="edc89-704">Uma equação não linear baseada no método Newton-Raphson clássico é usada na nova CTE.</span><span class="sxs-lookup"><span data-stu-id="edc89-704">A nonlinear equation that is based on the classical Newton-Raphson method is used in the new CTE.</span></span> <span data-ttu-id="edc89-705">Uma estimativa inicial ou *uma priori* vê, s <sub>anterior</sub> -(R 0, G 0, B 0) é obtida por meio da pesquisa por meio de uma "matriz de propagação" que consiste em uma grade 8x8x8 uniforme de pares previamente computados (RGB, Luv).</span><span class="sxs-lookup"><span data-stu-id="edc89-705">An initial guess, or *a priori* see, s <sub>prior</sub> -(R 0, G 0, B 0 ) is obtained by searching through a "seed matrix" consisting of a uniform 8x8x8 grid of pre-computed (RGB,Luv) pairs.</span></span> <span data-ttu-id="edc89-706">O Luv correspondente RGB que está mais próximo ao L \* u \* v \* é escolhido.</span><span class="sxs-lookup"><span data-stu-id="edc89-706">The RGB corresponding Luv that is closest to the L\*u\*v\* is chosen.</span></span> <span data-ttu-id="edc89-707">Cada ponto na matriz de propagação corresponde ao centro de uma célula para que as iterações não comecem com um ponto na face de limite do cubo RGB.</span><span class="sxs-lookup"><span data-stu-id="edc89-707">Each point in the seed matrix corresponds to the center of a cell so that the iterations don't start with a point on the boundary face of the RGB cube.</span></span> <span data-ttu-id="edc89-708">Em outras palavras, o RGB das sementes é definido por: etapa = 1/8 s <sub>IJK</sub> = (etapa/2 + (i-1) etapa, etapa/2 + (j-1) etapa, etapa/2 + (k-1) etapa) com i, j, k = 1... 8 na etapa *i* do Newton-Raphson, a próxima estimativa ![ mostra as variáveis para a próxima estimativa.](images/cdmp-image133.png)</span><span class="sxs-lookup"><span data-stu-id="edc89-708">In other words, the RGB of the seeds is defined by: STEP = 1/8 s <sub>ijk</sub> = (STEP/2 + (i-1) STEP, STEP/2+(j-1)STEP, STEP/2+(k-1)STEP) with i,j,k = 1...8 At the *i* th step of Newton-Raphson, the next estimate ![Shows the variables for the next estimate.](images/cdmp-image133.png)</span></span> <span data-ttu-id="edc89-709">é obtido pela fórmula:</span><span class="sxs-lookup"><span data-stu-id="edc89-709">is obtained by the formula:</span></span>

![Mostra a fórmula da estimativa.](images/cdmp-image135.png)

<span data-ttu-id="edc89-711">A iteração para quando o erro (distância no espaço CIELUV) é menor que um nível de tolerância predefinido (0,1 na CTE) ou quando o número de iterações excedeu o número máximo permitido de iterações (10 na CTE).</span><span class="sxs-lookup"><span data-stu-id="edc89-711">Iteration stops when the error (distance in the CIELUV space) is less than a pre-set tolerance level (0.1 in the CTE), or when the number of iterations has exceeded the maximum allowed number of iterations (10 in the CTE).</span></span> <span data-ttu-id="edc89-712">Os valores para a tolerância e o número de iterações foram empiricamente determinados para serem efetivos.</span><span class="sxs-lookup"><span data-stu-id="edc89-712">The values for the tolerance and the number of iterations were empirically determined to be effective.</span></span> <span data-ttu-id="edc89-713">Em versões futuras, o valor de tolerância pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="edc89-713">In future versions, the tolerance value may be changed.</span></span>

<span data-ttu-id="edc89-714">A matriz Jacobian é calculada usando a diferença de avanço, exceto em um ponto de limite (um ou mais de R, G, B é 1), em que a diferença retroativa é usada.</span><span class="sxs-lookup"><span data-stu-id="edc89-714">The Jacobian matrix is calculated using forward difference, except at a boundary point (one or more of the R, G, B is 1) where backward difference is used instead.</span></span> <span data-ttu-id="edc89-715">Em vez de calcular o inverso da matriz Jacobian, o sistema linear é resolvido diretamente usando Gauss-Jordan eliminação com dinamização completa.</span><span class="sxs-lookup"><span data-stu-id="edc89-715">Instead of calculating the inverse of the Jacobian matrix, the linear system is solved directly using Gauss-Jordan elimination with full pivoting.</span></span>

<span data-ttu-id="edc89-716">No final das iterações, a convergência ainda pode não ser obtida porque Newton-Raphson é um algoritmo "local", ou seja, ela só funcionará bem se você começar com uma estimativa inicial que está próxima da verdadeira solução.</span><span class="sxs-lookup"><span data-stu-id="edc89-716">At the end of the iterations, convergence still might not be achieved because Newton-Raphson is a "local" algorithm, that is, it only works well if you start with an initial guess that is close to the true solution.</span></span> <span data-ttu-id="edc89-717">Se, no final das iterações de Newton-Raphson, a convergência na tolerância de erro predefinida não tiver sido atingida, as iterações serão reiniciadas com um novo conjunto de sementes, definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="edc89-717">If, at the end of the Newton-Raphson iterations, convergence within the pre-defined error tolerance has not been achieved, the iterations are restarted with a new set of seeds, defined as follows.</span></span>

<span data-ttu-id="edc89-718">Por exemplo, a melhor solução obtida até agora é (r, g, b).</span><span class="sxs-lookup"><span data-stu-id="edc89-718">For example, the best solution obtained so far is (r, g, b).</span></span> <span data-ttu-id="edc89-719">A partir dessa solução, N uma posteriori sementes são derivadas, em que N = 4.</span><span class="sxs-lookup"><span data-stu-id="edc89-719">From this solution, N a posteriori seeds are derived, where N = 4.</span></span> <span data-ttu-id="edc89-720">Intuitivamente, a solução é movida "em direção ao centro" em um tamanho de etapa que depende de N. Consulte a Figura 6.</span><span class="sxs-lookup"><span data-stu-id="edc89-720">Intuitively, the solution is moved "toward the center" in a step size that depends on N. See Figure 6.</span></span>

![Diagrama que mostra as direções de muito da solução.](images/cdmp-image136.png)

<span data-ttu-id="edc89-722">**Figura 6** : a direção do muito da solução depende de qual octant está.</span><span class="sxs-lookup"><span data-stu-id="edc89-722">**Figure 6** : Perturbation direction of the solution depends on which octant it is in.</span></span>

<span data-ttu-id="edc89-723">Em outras palavras, se r &gt; 0,5, o valor no canal de r será diminuído, caso contrário, o valor será aumentado.</span><span class="sxs-lookup"><span data-stu-id="edc89-723">In other words, if r &gt; 0.5, the value on the R channel is decreased, otherwise the value is increased.</span></span> <span data-ttu-id="edc89-724">Há uma lógica semelhante para os canais G e B.</span><span class="sxs-lookup"><span data-stu-id="edc89-724">There is similar logic for the G and B channels.</span></span> <span data-ttu-id="edc89-725">As definições precisas são:</span><span class="sxs-lookup"><span data-stu-id="edc89-725">The precise definitions are:</span></span>

<span data-ttu-id="edc89-726">MUITO = 0,5/(N + 1)</span><span class="sxs-lookup"><span data-stu-id="edc89-726">PERTURBATION = 0.5/(N+1)</span></span>

<span data-ttu-id="edc89-727">Dir (r) =-1 se r &gt; 0,5; + 1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="edc89-727">Dir(r) = -1 if r &gt; 0.5; +1 otherwise.</span></span> <span data-ttu-id="edc89-728">Da mesma forma para dir (g) e dir (b)</span><span class="sxs-lookup"><span data-stu-id="edc89-728">Similarly for Dir(g) and Dir(b)</span></span>

<span data-ttu-id="edc89-729">Jth uma semente posteriori, s????, is (r + dir (r) \* j \* muito, g + dir (g) \* j \* muito, b + dir (b) \* j \* muito)</span><span class="sxs-lookup"><span data-stu-id="edc89-729">The jth a posteriori seed, s ????, is (r + Dir(r) \*j \* PERTURBATION, g + Dir(g) \* j \* PERTURBATION, b + Dir(b) \* j \* PERTURBATION)</span></span>

<span data-ttu-id="edc89-730">Experimente as primeiras s????</span><span class="sxs-lookup"><span data-stu-id="edc89-730">Try the first s ????</span></span> <span data-ttu-id="edc89-731">e se ele fornecer uma nova solução dentro da tolerância a erros, você poderá parar.</span><span class="sxs-lookup"><span data-stu-id="edc89-731">and if it gives a new solution within error tolerance, you can stop.</span></span> <span data-ttu-id="edc89-732">Caso contrário, experimente o segundo s????</span><span class="sxs-lookup"><span data-stu-id="edc89-732">Otherwise, try the second s ????</span></span> <span data-ttu-id="edc89-733">e assim por diante até o enésimo s????.</span><span class="sxs-lookup"><span data-stu-id="edc89-733">and so on until the Nth s ????.</span></span>

<span data-ttu-id="edc89-734">Os esquemas de todo o algoritmo são mostrados na Figura 7.</span><span class="sxs-lookup"><span data-stu-id="edc89-734">The schematics of the whole algorithm is shown in Figure 7.</span></span>

![Diagrama que mostra o fluxo para inverter o modelo do dispositivo.](images/cdmp-image138.png)

<span data-ttu-id="edc89-736">**Figura 7** : esquemas de inverter o modelo do dispositivo</span><span class="sxs-lookup"><span data-stu-id="edc89-736">**Figure 7** : Schematics of inverting the device model</span></span>

### <a name="rgb-virtual-device-model-baseline"></a><span data-ttu-id="edc89-737">Linha de base de modelo de dispositivo virtual RGB</span><span class="sxs-lookup"><span data-stu-id="edc89-737">RGB Virtual Device Model Baseline</span></span>

<span data-ttu-id="edc89-738">Esse modelo de dispositivo (DM) é um algoritmo simples de reprodução de matriz/Tom.</span><span class="sxs-lookup"><span data-stu-id="edc89-738">This device model(DM) is a simple matrix/tone reproduction algorithm.</span></span> <span data-ttu-id="edc89-739">A matriz é derivada do ponto branco e dos primários usando algoritmos de ciência de cores padrão.</span><span class="sxs-lookup"><span data-stu-id="edc89-739">The matrix is derived from the white point and primaries using standard color science algorithms.</span></span> <span data-ttu-id="edc89-740">A curva de reprodução de Tom é derivada dos parâmetros de medição de acordo com as descrições de ICC de Curvetype e parametrictype (ou invertidas conforme necessário).</span><span class="sxs-lookup"><span data-stu-id="edc89-740">The tone reproduction curve is derived from the measurement parameters according to the ICC descriptions of CurveType and ParametricType (or inverted as required).</span></span> <span data-ttu-id="edc89-741">Os detalhes dos algoritmos internos serão fornecidos após a validação adicional de problemas de intervalo dinâmico alto.</span><span class="sxs-lookup"><span data-stu-id="edc89-741">Details of the internal algorithms will be provided after additional validation of high dynamic range issues.</span></span>

<span data-ttu-id="edc89-742">O modelo de dispositivo virtual RGB é uma curva de reprodução de matriz/Tom ideal de RGB semelhante ao design de perfil baseado em matriz de três componentes ICC.</span><span class="sxs-lookup"><span data-stu-id="edc89-742">The RGB virtual device model is an idealized matrix/tone reproduction curve RGB similar to the ICC three-component matrix-based profile design.</span></span> <span data-ttu-id="edc89-743">Os parâmetros de "medida virtual" do DM incluem um valor de ponto branco (absoluto CIEXYZ), valores primários RGB (absoluto CIEXYZ) e uma curva de reprodução de Tom que se baseia no ICC ParametricCurveType e no Curvetype na formatação XML consistente com os esquemas DMP.</span><span class="sxs-lookup"><span data-stu-id="edc89-743">The "virtual measurement" parameters of the DM include a white point value (absolute CIEXYZ), RGB primary values (absolute CIEXYZ), and a tone reproduction curve that is based on the ICC ParametricCurveType and CurveType in XML formatting consistent with the DMP schemas.</span></span>

<span data-ttu-id="edc89-744">A codificação de tipo de função parametricCurveType de ICC e o suporte correspondente em IRGBVirtualDeviceModelBase são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="edc89-744">ICC parametricCurveType function type encoding and corresponding support in IRGBVirtualDeviceModelBase are shown in the following table.</span></span>



| <span data-ttu-id="edc89-745">Tipo de função</span><span class="sxs-lookup"><span data-stu-id="edc89-745">Function type</span></span>                                         | <span data-ttu-id="edc89-746">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="edc89-746">Parameters</span></span>                          | <span data-ttu-id="edc89-747">Tipo</span><span class="sxs-lookup"><span data-stu-id="edc89-747">Type</span></span>                                     | <span data-ttu-id="edc89-748">Observação</span><span class="sxs-lookup"><span data-stu-id="edc89-748">Note</span></span>                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![Mostra a função ' Gamatype '.](images/cdmp-image154.png)<br/> | <span data-ttu-id="edc89-750">g</span><span class="sxs-lookup"><span data-stu-id="edc89-750">g</span></span><br/>              | <span data-ttu-id="edc89-751">Gamatype</span><span class="sxs-lookup"><span data-stu-id="edc89-751">GammaType</span></span><br/>                 | <span data-ttu-id="edc89-752">Implementação comum</span><span class="sxs-lookup"><span data-stu-id="edc89-752">Common implementation</span></span><br/>           |
| ![Mostra a função ' GammaOffsetGainType '.](images/cdmp-image156.png)<br/> | <span data-ttu-id="edc89-754">GA b</span><span class="sxs-lookup"><span data-stu-id="edc89-754">ga b</span></span><br/>           | <span data-ttu-id="edc89-755">GammaOffsetGainType</span><span class="sxs-lookup"><span data-stu-id="edc89-755">GammaOffsetGainType</span></span><br/>       | <span data-ttu-id="edc89-756">CIE 122-1966</span><span class="sxs-lookup"><span data-stu-id="edc89-756">CIE 122-1966</span></span><br/>                    |
| ![Mostra a função ' GammaOffsetGainOffsetType '.](images/cdmp-image158.png)<br/> | <span data-ttu-id="edc89-758">GA b c</span><span class="sxs-lookup"><span data-stu-id="edc89-758">ga b c</span></span><br/>         | <span data-ttu-id="edc89-759">GammaOffsetGainOffsetType</span><span class="sxs-lookup"><span data-stu-id="edc89-759">GammaOffsetGainOffsetType</span></span><br/> | <span data-ttu-id="edc89-760">IEC 61966-3</span><span class="sxs-lookup"><span data-stu-id="edc89-760">IEC 61966-3</span></span><br/>                     |
| ![Mostra a função ' GammaOffsetGainGainType '.](images/cdmp-image160.png)<br/> | <span data-ttu-id="edc89-762">GA b c d</span><span class="sxs-lookup"><span data-stu-id="edc89-762">ga b c d</span></span><br/>       | <span data-ttu-id="edc89-763">GammaOffsetGainGainType</span><span class="sxs-lookup"><span data-stu-id="edc89-763">GammaOffsetGainGainType</span></span><br/>   | <span data-ttu-id="edc89-764">IEC 61966-2.1</span><span class="sxs-lookup"><span data-stu-id="edc89-764">IEC 61966-2.1</span></span><br/> <span data-ttu-id="edc89-765">sRGB</span><span class="sxs-lookup"><span data-stu-id="edc89-765">(sRGB)</span></span><br/> |
| ![Mostra uma função para os parâmetros ' g a b c d e f '.](images/cdmp-image162.png)<br/> | <span data-ttu-id="edc89-767">GA b c d e f</span><span class="sxs-lookup"><span data-stu-id="edc89-767">ga b c d e f</span></span><br/>   | <span data-ttu-id="edc89-768">N/D</span><span class="sxs-lookup"><span data-stu-id="edc89-768">N/A</span></span><br/>                       | <span data-ttu-id="edc89-769">Sem suporte no WCS</span><span class="sxs-lookup"><span data-stu-id="edc89-769">Not supported in WCS</span></span><br/>            |



 

<span data-ttu-id="edc89-770">A curva de Tom para dispositivos virtuais RGB é aplicada em DeviceToColorimetric entre os dados de entrada, o pDeviceColors e a matriz de multiplicação.</span><span class="sxs-lookup"><span data-stu-id="edc89-770">The tone curve for RGB virtual devices is applied in DeviceToColorimetric between the input data, pDeviceColors, and the matrix multiply.</span></span> <span data-ttu-id="edc89-771">Para ColorimetricToDevice, um método deve ser usado para inverter a curva de Tom.</span><span class="sxs-lookup"><span data-stu-id="edc89-771">For ColorimetricToDevice, a method must be used to invert the tone curve.</span></span> <span data-ttu-id="edc89-772">Na implementação de linha de base, isso é feito pela interpolação direta na mesma curva de Tom usada para DeviceToColorimetric.</span><span class="sxs-lookup"><span data-stu-id="edc89-772">In the baseline implementation, this is done by direct interpolation in the same tone curve used for DeviceToColorimetric.</span></span>

<span data-ttu-id="edc89-773">As curvas devem ser especificadas nos perfis como pares de números no espaço flutuante.</span><span class="sxs-lookup"><span data-stu-id="edc89-773">The curves should be specified in the profiles as pairs of numbers in float space.</span></span> <span data-ttu-id="edc89-774">O primeiro número representa valores em pDeviceColors.</span><span class="sxs-lookup"><span data-stu-id="edc89-774">The first number represents values in pDeviceColors.</span></span> <span data-ttu-id="edc89-775">O segundo número representa a saída da curva de Tom.</span><span class="sxs-lookup"><span data-stu-id="edc89-775">The second number represents the output of the tone curve.</span></span> <span data-ttu-id="edc89-776">Todos os valores na curva de Tom devem estar entre minColorantUsed e maxColorantUsed.</span><span class="sxs-lookup"><span data-stu-id="edc89-776">All values in the tone curve must be between minColorantUsed and maxColorantUsed.</span></span> <span data-ttu-id="edc89-777">As curvas de Tom devem conter pelo menos duas entradas: uma para minColorantUsed e outra para maxColorantUsed.</span><span class="sxs-lookup"><span data-stu-id="edc89-777">Tone curves must contain at least two entries: one for minColorantUsed and one for maxColorantUsed.</span></span> <span data-ttu-id="edc89-778">O número máximo de entradas no ToneCurve é 2048.</span><span class="sxs-lookup"><span data-stu-id="edc89-778">The maximum number of entries in the ToneCurve is 2048.</span></span> <span data-ttu-id="edc89-779">Em geral, quanto mais entradas na tabela, mais precisamente você pode modelar a curvatura.</span><span class="sxs-lookup"><span data-stu-id="edc89-779">In general, the more entries in the table, the more accurately you can model curvature.</span></span> <span data-ttu-id="edc89-780">Uma interpolação linear piecewise é executada entre as entradas.</span><span class="sxs-lookup"><span data-stu-id="edc89-780">A piecewise linear interpolation is performed between the entries.</span></span>

<span data-ttu-id="edc89-781">Você pode considerar métodos alternativos de interpolação.</span><span class="sxs-lookup"><span data-stu-id="edc89-781">You might consider alternative interpolation methods.</span></span> <span data-ttu-id="edc89-782">Se você souber algo sobre o comportamento subjacente do dispositivo, poderá usar menos amostras e modelar de forma mais precisa com uma curva de ordem mais alta.</span><span class="sxs-lookup"><span data-stu-id="edc89-782">If you know something about the underlying behavior of the device, you can use fewer samples and model more accurately with a higher order curve.</span></span> <span data-ttu-id="edc89-783">Mas se você usar o tipo de curva errado, será muito impreciso.</span><span class="sxs-lookup"><span data-stu-id="edc89-783">But if you use the wrong curve type, you will be very inaccurate.</span></span> <span data-ttu-id="edc89-784">Sem mais informações, não é possível adivinhar o tipo de curva.</span><span class="sxs-lookup"><span data-stu-id="edc89-784">Without more information, you cannot guess the curve type.</span></span> <span data-ttu-id="edc89-785">Portanto, use a interpolação linear e forneça vários pontos de dados.</span><span class="sxs-lookup"><span data-stu-id="edc89-785">So, use linear interpolation and provide many data points.</span></span>

### <a name="cmyk-printer-device-model-baseline"></a><span data-ttu-id="edc89-786">Linha de base de modelo de dispositivo de impressora CMYK</span><span class="sxs-lookup"><span data-stu-id="edc89-786">CMYK Printer Device Model Baseline</span></span>

<span data-ttu-id="edc89-787">A caracterização de um dispositivo de uma impressora CMYK consiste em construir um modelo empírica do dispositivo que prevê a cor impressa para qualquer valor CMYK determinado.</span><span class="sxs-lookup"><span data-stu-id="edc89-787">A device characterization of a CMYK printer consists of constructing an empirical model of the device that predicts the printed color for any given CMYK value.</span></span> <span data-ttu-id="edc89-788">A caracterização também inclui a inversão desse modelo para que uma receita do valor CMYK para nós para uma determinada cor seja impressa possa ser fornecida.</span><span class="sxs-lookup"><span data-stu-id="edc89-788">The characterization also includes the inversion of this model so that a prescription of the CMYK value to us for a given color to be printed can be given.</span></span> <span data-ttu-id="edc89-789">Isso normalmente é definido em termos de valor CIEXYZ ou CIELAB.</span><span class="sxs-lookup"><span data-stu-id="edc89-789">This is typically defined in terms of CIEXYZ or CIELAB value.</span></span>

<span data-ttu-id="edc89-790">Normalmente, um destino de ti 8.7/3 contendo patches CMYK é usado.</span><span class="sxs-lookup"><span data-stu-id="edc89-790">Typically, an IT8.7/3 target containing CMYK patches is used.</span></span> <span data-ttu-id="edc89-791">Os patches consistem em amostragem do espaço CMYK de uma maneira bem definida, de forma que uma grade retangular (com espaçamento não uniforme em C, M, Y e K) seja formada.</span><span class="sxs-lookup"><span data-stu-id="edc89-791">The patches consist of sampling of the CMYK space in a well-defined manner so that a rectangular grid (with non-uniform spacing in C, M, Y and K) is formed.</span></span> <span data-ttu-id="edc89-792">Em seguida, cada patch é medido com um colorimeter ou spectrophotometer.</span><span class="sxs-lookup"><span data-stu-id="edc89-792">Each patch is then measured with a colorimeter or spectrophotometer.</span></span> <span data-ttu-id="edc89-793">Em seguida, as medidas em valores CIEXYZ formam uma tabela de pesquisa (LUT), da qual um modelo de empírica da impressora é criado usando o método de interpolação de Sakamoto.</span><span class="sxs-lookup"><span data-stu-id="edc89-793">The measurements in CIEXYZ values then form a lookup table (LUT), from which an empirical model of the printer is built using Sakamoto's interpolation method.</span></span> <span data-ttu-id="edc89-794">Patente US 4275413 (Sakamoto et al.), patente dos EUA 4511989 (Sakamoto), Kang \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="edc89-794">US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[1\].</span></span> <span data-ttu-id="edc89-795">As duas patentes mencionadas expiraram.</span><span class="sxs-lookup"><span data-stu-id="edc89-795">The two patents mentioned have expired.</span></span>

<span data-ttu-id="edc89-796">Os requisitos específicos para os exemplos de medidas CMYK necessários para que um perfil de modelo de dispositivo seja aceito como válido pelo modelo de dispositivo de linha de base de impressora CMYK são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="edc89-796">Specific requirements for the CMYK measurement samples necessary for a device model profile to be accepted as valid by the CMYK printer baseline device model are as follows.</span></span> <span data-ttu-id="edc89-797">(O conjunto de amostras é descrito mais claramente como um conjunto de cubos de exemplo de CMY, cada um associado a um nível de K específico.)</span><span class="sxs-lookup"><span data-stu-id="edc89-797">(The sample set is most clearly described as a set of CMY sample cubes, each associated with a specific K level.)</span></span>

-   <span data-ttu-id="edc89-798">No mínimo, os cubos CMY válidos devem ser fornecidos para os níveis K = 0 e K = 100.</span><span class="sxs-lookup"><span data-stu-id="edc89-798">At minimum, valid CMY cubes must be provided for the K = 0 and K = 100 levels.</span></span>
-   <span data-ttu-id="edc89-799">Os níveis intermediários de K podem não ter espaçamento uniforme.</span><span class="sxs-lookup"><span data-stu-id="edc89-799">Intermediate K levels may be non-uniformly spaced.</span></span>
-   <span data-ttu-id="edc89-800">Qualquer nível K intermediário sem um cubo CMY válido será ignorado.</span><span class="sxs-lookup"><span data-stu-id="edc89-800">Any intermediate K level without a valid CMY cube will be ignored.</span></span>
-   <span data-ttu-id="edc89-801">Os cubos CMY podem usar intervalos de exemplo não uniformes (espaçamento de grade), mas o mesmo conjunto de intervalos de amostra deve ser usado em todas as dimensões C, M e Y no cubo CMY para um determinado nível de K.</span><span class="sxs-lookup"><span data-stu-id="edc89-801">The CMY cubes may use non-uniform sample intervals (grid spacing), but the same set of sample intervals must be used in all of the C,M, and Y dimensions in the CMY cube for a given K level.</span></span>
-   <span data-ttu-id="edc89-802">Cada cubo CMY de nível K pode usar um número diferente e espaçamento de intervalos de exemplo.</span><span class="sxs-lookup"><span data-stu-id="edc89-802">Each K level CMY cube can use a different number and spacing of sample intervals.</span></span>
-   <span data-ttu-id="edc89-803">Todos os cubos CMY devem conter os "cantos" do cubo CMY, ou seja, exemplos de CMY em \[ 0, 0, 0 \] , \[ 0, 0100, \] \[ 0100, 0 \] , \[ 100, 0, 0 \] , \[ 0100.100 \] , \[ 100, 0100 \] , \[ 100.100, 0 \] , \[ 100.100.100 \] .</span><span class="sxs-lookup"><span data-stu-id="edc89-803">All CMY cubes must contain the "corners" of the CMY cube, that is, CMY samples at \[0,0,0\], \[0,0,100\], \[0,100,0\], \[100,0,0\], \[0,100,100\], \[100,0,100\], \[100,100, 0\], \[100,100,100\].</span></span>
-   <span data-ttu-id="edc89-804">Todos os níveis de grade CMY intermediários devem ser totalmente amostrados em cada canal.</span><span class="sxs-lookup"><span data-stu-id="edc89-804">Any intermediate CMY grid levels must be fully sampled in each channel.</span></span> <span data-ttu-id="edc89-805">Em outras palavras, um exemplo deve existir em cada interseção de grade 3D dentro do cubo CMY.</span><span class="sxs-lookup"><span data-stu-id="edc89-805">In other words, a sample must exist at each 3-D grid intersection within the CMY cube.</span></span>
-   <span data-ttu-id="edc89-806">Para os cubos de AT K = 0 e K = 100 CMY, os cubos de "somente cantos" 2x2x2 são o mínimo aceito como válido.</span><span class="sxs-lookup"><span data-stu-id="edc89-806">For the K = 0 and K = 100 CMY cubes, 2x2x2 "corners-only" cubes are the minimum accepted as valid.</span></span>

    <span data-ttu-id="edc89-807">\[Observação: para K = 0 e K = 100 níveis, um cubo CMY 3x3x3 será processado como um cubo 2x2x2 "somente cantos"; o nível de amostra intermediário é ignorado.</span><span class="sxs-lookup"><span data-stu-id="edc89-807">\[NOTE: for K=0 and K=100 levels, a 3x3x3 CMY cube will be processed as a 2x2x2 "corners-only" cube; the intermediate sample level is ignored.</span></span> <span data-ttu-id="edc89-808">4x4x4 e cubos maiores terão todos os exemplos em grade usados.\]</span><span class="sxs-lookup"><span data-stu-id="edc89-808">4x4x4 and larger cubes will have all on-grid samples used.\]</span></span>

-   <span data-ttu-id="edc89-809">Para os níveis intermediários de K, os cubos CMY 4x4x4 são o mínimo aceito como válido.</span><span class="sxs-lookup"><span data-stu-id="edc89-809">For intermediate K levels, 4x4x4 CMY cubes are the minimum accepted as valid.</span></span>

<span data-ttu-id="edc89-810">Um perfil de alta qualidade usará grades de amostragem mais finas do que o mínimo necessário para a validade, geralmente 9x9x9x9 ou superior.</span><span class="sxs-lookup"><span data-stu-id="edc89-810">A high-quality profile will use finer sampling grids than the minimum required for validity, usually 9x9x9x9 or higher.</span></span> <span data-ttu-id="edc89-811">Os exemplos dos destinos IT 8.7/3, IT 8.7/4 e ECI produzem perfis de modelo de dispositivo (DMPs) válidos para o modelo de dispositivo de linha de base de impressora CMYK.</span><span class="sxs-lookup"><span data-stu-id="edc89-811">The samples from the IT8.7/3, IT8.7/4, and ECI targets produce valid device model profiles (DMPs)for the CMYK printer baseline device model.</span></span> <span data-ttu-id="edc89-812">Embora esse modelo de dispositivo seja capaz de ignorar os exemplos estranhos (fora da grade) nesses destinos, não há garantia de que eles sejam capazes de fazer isso para outros destinos e, portanto, é recomendável que amostras estranhas sejam removidas dos conjuntos de medidas que entram em perfis para esse modelo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="edc89-812">While this device model is able to ignore the extraneous (off-grid) samples in these targets, it is not guaranteed to be able to do so for other targets, and so, it is recommended that extraneous samples be removed from measurement sets going into profiles for this device model.</span></span>

<span data-ttu-id="edc89-813">A inversão do modelo de impressora apresenta mais dificuldades.</span><span class="sxs-lookup"><span data-stu-id="edc89-813">The inversion of the printer model presents more difficulties.</span></span> <span data-ttu-id="edc89-814">Dada uma cor de entrada em CIECAM, há uma pergunta se essa cor está dentro da gama da impressora.</span><span class="sxs-lookup"><span data-stu-id="edc89-814">Given an input color in CIECAM, there is a question of whether this color is within the printer gamut.</span></span> <span data-ttu-id="edc89-815">Também há o problema em relação à disposição de pontos no espaço de aparência da cor.</span><span class="sxs-lookup"><span data-stu-id="edc89-815">There is also the issue regarding the arrangement of points in the color appearance space.</span></span> <span data-ttu-id="edc89-816">Embora possamos organizar os valores CMYK para ficarem em uma grade retangular, como é feito no destino de ti 8.7/3, o mesmo não pode ser dito das cores impressas resultantes, pois estão situadas no espaço de aparência da cor.</span><span class="sxs-lookup"><span data-stu-id="edc89-816">While we can arrange the CMYK values to fall on a rectangular grid, as is done in the IT8.7/3 target, the same cannot be said of the resulting printed colors as they are situated in the color appearance space.</span></span> <span data-ttu-id="edc89-817">Em geral, eles estão espalhados no espaço de aparência de cor sem nenhum padrão específico.</span><span class="sxs-lookup"><span data-stu-id="edc89-817">In general, they are scattered in the color appearance space with no particular pattern.</span></span>

<span data-ttu-id="edc89-818">Em geral, há duas abordagens para o problema de inversão de pontos dispersos.</span><span class="sxs-lookup"><span data-stu-id="edc89-818">There are generally two approaches to the inversion problem of scattered points.</span></span> <span data-ttu-id="edc89-819">Uma abordagem é usar uma subdivisão geométrica da gama da impressora usando sólidos bidimensionais elementares, como tetrahedra.</span><span class="sxs-lookup"><span data-stu-id="edc89-819">One approach is to use a geometric subdivision of the printer gamut using elementary 3-dimensional solids, such as tetrahedra.</span></span> <span data-ttu-id="edc89-820">Uma subdivisão da gama da impressora no espaço de aparência da cor pode ser induzida a partir da subdivisão correspondente do espaço CMY (K), consulte travada \[ 93 \] , Kang \[ 97 \] . Essa abordagem tem a vantagem de uma simplicidade computacional.</span><span class="sxs-lookup"><span data-stu-id="edc89-820">A subdivision of the printer gamut in the color appearance space can be induced from the corresponding subdivision of the CMY(K) space, see Hung\[93\], Kang\[97\].This approach has the advantage of computational simplicity.</span></span> <span data-ttu-id="edc89-821">No caso de um tetraedro, somente quatro pontos são usados em uma interpolação.</span><span class="sxs-lookup"><span data-stu-id="edc89-821">In the case of a tetrahedron, only four points are used in an interpolation.</span></span> <span data-ttu-id="edc89-822">Por outro lado, o resultado depende muito de alguns pontos, o que significa que um erro de medida terá um efeito significativo sobre o resultado.</span><span class="sxs-lookup"><span data-stu-id="edc89-822">On the other hand, the result depends heavily on a few points, which means that a measurement error will have a significant effect on the result.</span></span> <span data-ttu-id="edc89-823">A interpolação também tende a não ser tão suave.</span><span class="sxs-lookup"><span data-stu-id="edc89-823">The interpolant also tends to be not as smooth.</span></span> <span data-ttu-id="edc89-824">A segunda abordagem não assume nenhuma subdivisão e se baseia na técnica de interpolação de dados dispersos.</span><span class="sxs-lookup"><span data-stu-id="edc89-824">The second approach does not assume any subdivision, and is based on the technique of scattered data interpolation.</span></span> <span data-ttu-id="edc89-825">Um exemplo clássico é a técnica de interpolação Shepard ou método inverso invertido (consulte Shepard \[ 68 \] ).</span><span class="sxs-lookup"><span data-stu-id="edc89-825">A classical example is the technique of Shepard interpolation, or inverse weighted method (See Shepard \[68\]).</span></span> <span data-ttu-id="edc89-826">Aqui, vários pontos em torno do ponto de entrada são escolhidos de alguma maneira, cada um atribuído a um peso, geralmente inversamente proporcional à distância, e a interpolação é tomada como a média ponderada dos pontos vizinhos.</span><span class="sxs-lookup"><span data-stu-id="edc89-826">Here, several points surrounding the input point are chosen in some manner, each assigned a weight, usually inversely proportional to the distance, and the interpolant is taken as the weighted average of the neighboring points.</span></span> <span data-ttu-id="edc89-827">Nessa abordagem, a escolha dos pontos vizinhos é fundamental para o desempenho.</span><span class="sxs-lookup"><span data-stu-id="edc89-827">In this approach, the choice of neighboring points is paramount to performance.</span></span> <span data-ttu-id="edc89-828">Embora poucos pontos possam renderizar os pontos intercorretos e não-suaves interpolares, um grande número de casas impõe um custo computacional alto, pois os pesos normalmente são funções não lineares e são dispendiosos para computar.</span><span class="sxs-lookup"><span data-stu-id="edc89-828">While too few points can render the interpolant inaccurate and non-smooth, too many points impose a high computational cost, as the weights are typically non-linear functions and costly to compute.</span></span>

<span data-ttu-id="edc89-829">As duas abordagens descritas acima têm problemas.</span><span class="sxs-lookup"><span data-stu-id="edc89-829">The two approaches described above both have problems.</span></span> <span data-ttu-id="edc89-830">A abordagem de subdivisão depende crucialmente dos dados que são razoavelmente nulos de ruído e, em geral, o interpolação não é muito suave.</span><span class="sxs-lookup"><span data-stu-id="edc89-830">The subdivision approach depends critically on the data being reasonably void of noise, and generally the interpolant is not very smooth.</span></span> <span data-ttu-id="edc89-831">A interpolação de dados dispersos é mais tolerante ao ruído de dados e geralmente proporciona uma interpolação mais suave, mas é computacionalmente mais cara.</span><span class="sxs-lookup"><span data-stu-id="edc89-831">The scattered data interpolation is more tolerant to data noise, and generally gives a smoother interpolant, but it is computationally more expensive.</span></span>

<span data-ttu-id="edc89-832">A nova CTE usa uma abordagem alternativa.</span><span class="sxs-lookup"><span data-stu-id="edc89-832">The new CTE takes an alternative approach.</span></span> <span data-ttu-id="edc89-833">O dispositivo CMYK é tratado como uma coleção de vários dispositivos CMY, cada um com um valor específico de preto (K).</span><span class="sxs-lookup"><span data-stu-id="edc89-833">The CMYK device is treated as a collection of several CMY devices, each of which has a specific value of black (K).</span></span> <span data-ttu-id="edc89-834">Usando um algoritmo de seleção que usa como parâmetros claridade e croma, um nível de preto é escolhido.</span><span class="sxs-lookup"><span data-stu-id="edc89-834">Using a selection algorithm that takes as parameters lightness and chroma, a level of black is chosen.</span></span> <span data-ttu-id="edc89-835">Os valores de CMY são obtidos pela inversão da tabela CMY para Luv correspondente usando os métodos de Newton empregados em outro lugar pelo algoritmo de impressora RGB.</span><span class="sxs-lookup"><span data-stu-id="edc89-835">The CMY values are obtained by inversion of the corresponding CMY to Luv table using the Newton methods employed elsewhere by the RGB printer algorithm.</span></span>

<span data-ttu-id="edc89-836">Use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="edc89-836">Use the following steps.</span></span>

1.  <span data-ttu-id="edc89-837">Imprima o destino de caracterização, que é o destino 8.7/3 ou um destino que contém a amostragem do espaço CMYK em intervalos de espaçamento regular ou irregular.</span><span class="sxs-lookup"><span data-stu-id="edc89-837">Print the characterization target, which is either the IT8.7/3 target, or a target containing sampling of the CMYK space at regularly or irregularly spaced intervals.</span></span>
2.  <span data-ttu-id="edc89-838">Meça o destino usando um spectrophotometer e converta as medidas para o espaço CIELUV.</span><span class="sxs-lookup"><span data-stu-id="edc89-838">Measure the target using a spectrophotometer, and convert the measurements to CIELUV space.</span></span>
3.  <span data-ttu-id="edc89-839">Construa o mapa de encaminhamento de CMYK para luv.</span><span class="sxs-lookup"><span data-stu-id="edc89-839">Construct the forward map from CMYK to Luv.</span></span>
4.  <span data-ttu-id="edc89-840">Use o mapa de encaminhamento para construir um conjunto de CMY para Luv Maps para um intervalo de valores de K.</span><span class="sxs-lookup"><span data-stu-id="edc89-840">Use the forward map to construct a set of CMY to Luv maps for a range of K values.</span></span>
5.  <span data-ttu-id="edc89-841">Para qualquer valor de Luv de entrada, o valor CMYK correspondente é obtido selecionando um dos mapas construídos na etapa 4 acima e invertendo usando o método Newton para obter um conjunto de Colorant de CMY para acompanhar o valor K selecionado.</span><span class="sxs-lookup"><span data-stu-id="edc89-841">For any input Luv value, the corresponding CMYK value is obtained by selecting one of the maps constructed in step 4 above and inverting using Newton's method to obtain a CMY colorant set to accompany the K value selected.</span></span>

<span data-ttu-id="edc89-842">As etapas 1 e 2, que são procedimentos padrão, são executadas por um programa de criação de perfil que não faz parte da nova CTE.</span><span class="sxs-lookup"><span data-stu-id="edc89-842">Steps 1 and 2, which are standard procedures, are performed by a profiling program that is not part of the new CTE.</span></span> <span data-ttu-id="edc89-843">O destino de ti 8.7/3 contém uma amostragem razoavelmente detalhada de todos os valores CMYK em vários níveis de C, M, Y e K. como alternativa, um destino personalizado com a amostragem uniforme dos canais C, M, Y e K pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="edc89-843">The IT8.7/3 target contains a reasonably detailed sampling of all the CMYK values at various levels of C, M, Y, and K. Alternatively, a custom target with uniform sampling of the C, M, Y, and K channels can be used.</span></span> <span data-ttu-id="edc89-844">Depois que o destino é impresso, um spectrophotometer ou colorimeter pode ser usado para medir o valor XYZ de cada patch, e o valor XYZ pode ser convertido para o valor de Luv usando o modelo CIELUV.</span><span class="sxs-lookup"><span data-stu-id="edc89-844">After the target is printed, a spectrophotometer or colorimeter can be used to measure the XYZ value of each patch, and the XYZ value can be converted to the Luv value using the CIELUV model.</span></span>

<span data-ttu-id="edc89-845">A etapa 3, construção do mapa de encaminhamento de CMYK para Luv, pode ser obtida aplicando-se qualquer técnica de interpolação conhecida, como tetrahedral ou método Multiline, na grade retangular no espaço CMYK.</span><span class="sxs-lookup"><span data-stu-id="edc89-845">Step 3, construction of the forward map from CMYK to Luv, can be achieved by applying any known interpolation technique, such as tetrahedral or multilinear method, on the rectangular grid in CMYK space.</span></span> <span data-ttu-id="edc89-846">Na nova CTE, uma interpolação de tetrahedral de 4 dimensões é usada.</span><span class="sxs-lookup"><span data-stu-id="edc89-846">In the new CTE, a 4-dimensional tetrahedral interpolation is used.</span></span> <span data-ttu-id="edc89-847">Como as grades de amostragem de CMY geralmente são diferentes em cada nível de K, no entanto, usamos uma técnica de Superamostragem, conforme detalhado abaixo.</span><span class="sxs-lookup"><span data-stu-id="edc89-847">Because the CMY sampling grids are generally different on each level of K, however, we use a technique of super-sampling, as detailed below.</span></span> <span data-ttu-id="edc89-848">Para um determinado ponto CMYK, os níveis de sanduíche de t são determinados primeiro com base no valor K.</span><span class="sxs-lookup"><span data-stu-id="edc89-848">For a given CMYK point, the sandwiching K levels are first determined based on the K value.</span></span> <span data-ttu-id="edc89-849">Em seguida, introduza uma "super Grid" em cada nível de K que é uma União das grades CMY em cada um dos dois níveis de K.</span><span class="sxs-lookup"><span data-stu-id="edc89-849">Then introduce a "super-grid" on each K level that is a union of the CMY grids on each of the two K levels.</span></span> <span data-ttu-id="edc89-850">Em cada nível de K, o valor de Luv de qualquer ponto de grade introduzido recentemente é obtido por uma interpolação de tetrahedral tridimensional dentro desse nível de K.</span><span class="sxs-lookup"><span data-stu-id="edc89-850">On each K level, the Luv value of any newly introduced grid point is obtained by a 3-dimensional tetrahedral interpolation within that K level.</span></span> <span data-ttu-id="edc89-851">Por fim, uma interpolação de tetrahedral de 4 dimensões para o ponto CMYK específico é executada nessa nova grade.</span><span class="sxs-lookup"><span data-stu-id="edc89-851">Finally, a 4-dimensional tetrahedral interpolation for the specific CMYK point is performed on this new grid.</span></span>

![Diagrama que mostra a superamostragem.](images/cdmp-image163.png)

<span data-ttu-id="edc89-853">**Figura 8** : Superamostragem</span><span class="sxs-lookup"><span data-stu-id="edc89-853">**Figure 8** : Supersampling</span></span>

<span data-ttu-id="edc89-854">A etapa 4 constrói um conjunto de LUTs (tabelas de pesquisa CMY-para-Luv).</span><span class="sxs-lookup"><span data-stu-id="edc89-854">Step 4 constructs a set of CMY-to-Luv lookup tables (LUTs).</span></span> <span data-ttu-id="edc89-855">O mapa de encaminhamento construído na etapa 3 é chamado repetidamente para reamostrar o espaço CMYK.</span><span class="sxs-lookup"><span data-stu-id="edc89-855">The forward map constructed in Step 3 is called repeatedly to resample the CMYK space.</span></span> <span data-ttu-id="edc89-856">O espaço de cores CMYK é amostrado usando um espaçamento par de K e outro, mas ainda com espaçamento uniforme, de amostragem de CMY.</span><span class="sxs-lookup"><span data-stu-id="edc89-856">The CMYK color space is sampled using an even spacing of K and a different, but still evenly spaced, sampling of CMY.</span></span>

<span data-ttu-id="edc89-857">A etapa 5 é um procedimento para obter o valor CMYK usando o LUTs construído na etapa 4 para qualquer ponto de Luv de entrada.</span><span class="sxs-lookup"><span data-stu-id="edc89-857">Step 5 is a procedure to obtain the CMYK value using the LUTs constructed in Step 4 for any input Luv point.</span></span> <span data-ttu-id="edc89-858">O valor apropriado de K é escolhido analisando a claridade, bem como o grau de cor no Luv solicitado.</span><span class="sxs-lookup"><span data-stu-id="edc89-858">The appropriate value of K is chosen by analyzing the lightness as well as the degree of color in the Luv requested.</span></span> <span data-ttu-id="edc89-859">Depois que a tabela é selecionada, os valores de CMY são obtidos da tabela usando o método Newton (conforme documentado no modelo de dispositivo de impressora RGB anteriormente).</span><span class="sxs-lookup"><span data-stu-id="edc89-859">After the table is selected, the CMY values are obtained from the table by using Newton's method (as documented under the RGB printer device model earlier).</span></span>

<span data-ttu-id="edc89-860">O espaço CIELUV é usado no modelo de impressora em vez de CIEJab porque o modelo de dispositivo deve ser baseado apenas em dados colorimétrico disponíveis no DMP.</span><span class="sxs-lookup"><span data-stu-id="edc89-860">CIELUV space is used in the printer model instead of CIEJab because the device model should be based solely on colorimetric data available in the DMP.</span></span> <span data-ttu-id="edc89-861">O DMP contém dados colorimétrico para cada patch medido, incluindo o ponto branco de mídia, portanto, é possível converter dados do CIEXYZ em dados do CIELUV.</span><span class="sxs-lookup"><span data-stu-id="edc89-861">The DMP contains colorimetric data for each measured patch, including the media white point, so it is possible to convert CIEXYZ data into CIELUV data.</span></span> <span data-ttu-id="edc89-862">No entanto, não é possível converter em CIECAM02 JCh ou jab, porque não há acesso às informações da condição de exibição no DMP.</span><span class="sxs-lookup"><span data-stu-id="edc89-862">However, it is not possible to convert to CIECAM02 JCh or Jab, because there is no access to the viewing condition information in the DMP.</span></span>

### <a name="rgb-projector-device-model-baseline"></a><span data-ttu-id="edc89-863">Linha de base do modelo de dispositivo do projetor RGB</span><span class="sxs-lookup"><span data-stu-id="edc89-863">RGB Projector Device Model Baseline</span></span>

<span data-ttu-id="edc89-864">Observação: muitos projetores RGB têm mais de um modo de operação.</span><span class="sxs-lookup"><span data-stu-id="edc89-864">Note: Many RGB projectors have more than one operating mode.</span></span> <span data-ttu-id="edc89-865">Em um modo, que geralmente é o padrão e pode ser chamado algo como "apresentação", a resposta de cor do projetor é otimizada para o brilho máximo.</span><span class="sxs-lookup"><span data-stu-id="edc89-865">In one mode, which is often the default and might be called something like "presentation," the color response of the projector is optimized for maximum brightness.</span></span> <span data-ttu-id="edc89-866">No entanto, nesse modo, o projetor perde a capacidade de reproduzir cores claras, um pouco de desvio, como amarelos pálidos e alguns tons.</span><span class="sxs-lookup"><span data-stu-id="edc89-866">However, in this mode, the projector loses the ability to reproduce light, slightly chromatic colors such as pale yellows and some flesh tones.</span></span> <span data-ttu-id="edc89-867">Em outro modo, geralmente chamado de "filme", "vídeo" ou "sRGB", o projetor é otimizado para reprodução de imagens realísticas e cenas naturais.</span><span class="sxs-lookup"><span data-stu-id="edc89-867">In another mode, often called "film," "video," or "sRGB," the projector is optimized for reproduction of realistic images and natural scenes.</span></span> <span data-ttu-id="edc89-868">Nesse modo, o brilho máximo é negociado para melhorar a qualidade geral da reprodução de cores.</span><span class="sxs-lookup"><span data-stu-id="edc89-868">In this mode, maximum brightness is traded off to improve the overall quality of the color reproduction.</span></span> <span data-ttu-id="edc89-869">Para obter uma reprodução de cores satisfatória com projetores RGB, é necessário posicionar o projetor em um modo em que uma gama suave de cores possa ser reproduzida.</span><span class="sxs-lookup"><span data-stu-id="edc89-869">To obtain satisfactory color reproduction with RGB projectors, it is necessary to place the projector in a mode where a smooth gamut of colors can be reproduced.</span></span>

![Diagrama que mostra um modelo de dispositivo D L P.](images/cdmp-image167.png)

<span data-ttu-id="edc89-871">**Figura 9** : modelo de dispositivo DLP</span><span class="sxs-lookup"><span data-stu-id="edc89-871">**Figure 9** : DLP device model</span></span>

<span data-ttu-id="edc89-872">Um valor RGB de entrada passa por dois caminhos computacionais.</span><span class="sxs-lookup"><span data-stu-id="edc89-872">An incoming RGB value passes through two computational pathways.</span></span> <span data-ttu-id="edc89-873">A primeira é o modelo de matriz, que resulta em um valor XYZ.</span><span class="sxs-lookup"><span data-stu-id="edc89-873">The first is the matrix model, which results in an XYZ value.</span></span> <span data-ttu-id="edc89-874">Isso é seguido imediatamente pela conversão de XYZ para luv.</span><span class="sxs-lookup"><span data-stu-id="edc89-874">This is immediately followed by the conversion from XYZ to Luv.</span></span> <span data-ttu-id="edc89-875">A segunda é a interpolação LUT não uniforme usando a interpolação tetrahedral.</span><span class="sxs-lookup"><span data-stu-id="edc89-875">The second is the non-uniform LUT interpolation using tetrahedral interpolation.</span></span> <span data-ttu-id="edc89-876">A saída da interpolação já está no espaço Luv por construção.</span><span class="sxs-lookup"><span data-stu-id="edc89-876">The output of the interpolation is already in Luv space by construction.</span></span> <span data-ttu-id="edc89-877">As duas saídas são adicionadas para obter o valor Luv previsto.</span><span class="sxs-lookup"><span data-stu-id="edc89-877">The two outputs are added to obtain the predicted Luv value.</span></span> <span data-ttu-id="edc89-878">Isso é finalmente convertido para XYZ, que é a saída esperada do modelo colorimétrico para o dispositivo DLP.</span><span class="sxs-lookup"><span data-stu-id="edc89-878">This is finally converted to XYZ, which is the expected output of the colorimetric model for the DLP device.</span></span>

<span data-ttu-id="edc89-879">Como os projetores são dispositivos de exibição, eles também dão suporte à inversão do modelo, ou seja, a transformação da XYZ para a RGB.</span><span class="sxs-lookup"><span data-stu-id="edc89-879">Since projectors are display devices, they also support the inversion of the model, that is, the transform from XYZ to RGB.</span></span> <span data-ttu-id="edc89-880">Como o modelo de dispositivo transforma o espaço RGB para o espaço XYZ, que são tridimensionais, inversão é equivalente a resolver três equações não lineares em três desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="edc89-880">Because the device model transforms RGB space to XYZ space, which are both three dimensional, inversion is equivalent to solving three nonlinear equations in three unknowns.</span></span> <span data-ttu-id="edc89-881">Isso pode ser feito por técnicas de solução de equações padrão, como Newton-Raphson.</span><span class="sxs-lookup"><span data-stu-id="edc89-881">This can done by standard equation solving techniques, such as Newton-Raphson.</span></span> <span data-ttu-id="edc89-882">No entanto, é preferível primeiro converter a XYZ em luv e, em seguida, inverter a transformação de Luv para RGB, porque o espaço de Luv é mais perceptually linear do que o espaço XYZ.</span><span class="sxs-lookup"><span data-stu-id="edc89-882">It is preferable, however, to first convert XYZ to Luv, and then invert the Luv To RGB transform, because Luv space is more perceptually linear than XYZ space.</span></span>

### <a name="icc-device-model-baseline"></a><span data-ttu-id="edc89-883">Linha de base do modelo de dispositivo ICC</span><span class="sxs-lookup"><span data-stu-id="edc89-883">ICC Device Model Baseline</span></span>

<span data-ttu-id="edc89-884">A interoperabilidade do fluxo de trabalho de ICC de contratação é habilitada criando um perfil de modelo de dispositivo de linha de base de dispositivo ICC especial que armazena o objeto de perfil e cria uma transformação ICC usando um perfil XYZ não operacional.</span><span class="sxs-lookup"><span data-stu-id="edc89-884">The CITE ICC workflow interoperability is enabled by creating a special ICC device baseline device model profile that stores the profile object and creates a ICC transform using a no-op XYZ profile.</span></span> <span data-ttu-id="edc89-885">Em seguida, essa transformação é usada para converter entre as cores do dispositivo e do CIEXYZ.</span><span class="sxs-lookup"><span data-stu-id="edc89-885">This transform is then used to translate between device and CIEXYZ colors.</span></span>

![Diagrama que mostra a interoperabilidade de fluxo de trabalho C I E C c.](images/cdmp-image168.png)

<span data-ttu-id="edc89-887">**Figura 10** : citar a interoperabilidade do fluxo de trabalho ICC</span><span class="sxs-lookup"><span data-stu-id="edc89-887">**Figure 10** : CITE ICC Workflow Interoperability</span></span>

## <a name="related-topics"></a><span data-ttu-id="edc89-888">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="edc89-888">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edc89-889">Conceitos básicos de gerenciamento de cores</span><span class="sxs-lookup"><span data-stu-id="edc89-889">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="edc89-890">Algoritmos e esquemas do sistema de cores do Windows</span><span class="sxs-lookup"><span data-stu-id="edc89-890">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





