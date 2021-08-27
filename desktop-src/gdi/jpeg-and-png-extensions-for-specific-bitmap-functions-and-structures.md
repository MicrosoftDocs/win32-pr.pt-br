---
description: em determinadas versões do Microsoft Windows, as funções StretchDIBits e SetDIBitsToDevice permitem que imagens JPEG e PNG sejam passadas como a imagem de origem para dispositivos de impressora.
ms.assetid: a38a807d-44df-40a2-8af7-0ce5e532cba2
title: Extensões JPEG e PNG para estruturas e funções de bitmap específicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd7dcd2713b737d86f90ab0d49fdf4eed1216f807a4debdffa1963e43a42a9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115286"
---
# <a name="jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures"></a>Extensões JPEG e PNG para estruturas e funções de bitmap específicas

em determinadas versões do Microsoft Windows, as funções [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) e [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) permitem que imagens JPEG e PNG sejam passadas como a imagem de origem para dispositivos de impressora. Essa extensão não se destina como um meio de fornecer descompactação JPEG e PNG geral a aplicativos, mas, em vez disso, permitir que os aplicativos enviem imagens compactadas por JPEG e PNG diretamente a impressoras com suporte de hardware para imagens JPEG e PNG.

As estruturas [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) e [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) são estendidas para permitir a especificação de valores de **bicompressão** indicando que os dados de bitmap são uma imagem JPEG ou png. Esses valores de compactação só são válidos para [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) e [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) quando o parâmetro *HDC* especifica um dispositivo de impressora. Para dar suporte ao spool de metarquivo da impressora, o aplicativo não deve depender do valor de retorno para determinar se o dispositivo dá suporte ao arquivo JPEG ou PNG. O aplicativo deve emitir QUERYESCSUPPORT com o escape correspondente antes de chamar **SetDIBitsToDevice** e **StretchDIBits**. Se o escape de validação falhar, o aplicativo deverá retornar ao seu próprio suporte a JPEG ou PNG para descompactar a imagem em um bitmap.

 

 
