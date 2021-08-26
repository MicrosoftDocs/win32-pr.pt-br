---
description: o Microsoft Image Color Management (ICM) garante que uma imagem colorida, um elemento gráfico ou um objeto de texto seja renderizado o mais próximo possível de sua intenção original em qualquer dispositivo, apesar das diferenças nas tecnologias de geração de imagens e funcionalidades de cores entre os dispositivos.
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: ICM-Enabled funções de contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33337aeea32f1ca84b74e3fc45e9bd67dbfe1ce1a5300a502a5303f55cab357
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944196"
---
# <a name="icm-enabled-device-context-functions"></a>ICM-Enabled funções de contexto de dispositivo

o Microsoft Image Color Management (ICM) garante que uma imagem colorida, um elemento gráfico ou um objeto de texto seja renderizado o mais próximo possível de sua intenção original em qualquer dispositivo, apesar das diferenças nas tecnologias de geração de imagens e funcionalidades de cores entre os dispositivos. (para obter mais informações, consulte [Windows sistema de cores](/previous-versions//dd372446(v=vs.85)).)

Há várias funções na interface gráfica de dispositivo (GDI) que usam ou operam em dados de cores. As seguintes funções de contexto de dispositivo estão habilitadas para uso com ICM:

-   [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [**Selecionarobject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 
