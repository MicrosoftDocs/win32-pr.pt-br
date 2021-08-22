---
title: Esquema de calibração do WCS
description: Este tópico descreve o esquema de calibração do WCS que expande o perfil de modelo de dispositivo de cores WCS.
ms.assetid: 99f3e9e3-15b7-4bca-87cc-a3bf3b6d0112
keywords:
- Windows Sistema de cores (WCS), calibragem
- WCS (Windows sistema de cores), calibragem
- gerenciamento de cores de imagem, calibragem
- gerenciamento de cores, calibragem
- cores, calibragem
- esquemas, calibragem
- Calibração do WCS
- calibragem
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3744f8aa0190f09acf80b469ae01fddb035c48deda73d53871094ef9ece8e88b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451416"
---
# <a name="wcs-calibration-schema"></a>Esquema de calibração do WCS

Este tópico descreve o esquema de calibração do WCS que expande o [perfil de modelo de dispositivo de cores WCS](wcs-color-device-model-profile-schema-and-algorithms.md).

## <a name="the-wcs-calibration-schema"></a>O esquema de calibração do WCS

a definição de esquema a seguir é usada para especificar as novas definições de Windows 7 que dão suporte à calibragem de [perfil de modelo de dispositivo de cores WCS](wcs-color-device-model-profile-schema-and-algorithms.md) .


```C++
<?xml version="1.0" encoding="UTF-8"?>
<!--
  Copyright (C) Microsoft. All rights reserved. The Windows Color System
  color profile schemas may be used according to the terms of the license agreement
  available at https://www.microsoft.com/whdc/device/display/color/wcs_license.mspx.
  -->
<xs:schema
  xmlns:cal="http://schemas.microsoft.com/windows/2007/11/color/Calibration"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2007/11/color/Calibration"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Device Model Calibration profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:complexType name="AdapterGammaConfiguration">
    <xs:choice>
      <xs:element name="ParameterizedCurves" type="wcs:ParameterizedCurvesType"/>
      <xs:element name="HDRToneResponseCurves" type="wcs:HDRToneResponseCurvesType"/>
    </xs:choice>
  </xs:complexType>

  <xs:complexType name="Calibration">
    <xs:sequence>
      <xs:element name="AdapterGammaConfiguration" type="cal:AdapterGammaConfiguration" minOccurs="0"/>
    </xs:sequence>
  </xs:complexType>

</xs:schema>
```



para compatibilidade com o Windows Vista, os perfis que contêm marcas de calibragem devem incluir o atributo `mc:Ignoreable="cdm_calibration"` .

 

 




