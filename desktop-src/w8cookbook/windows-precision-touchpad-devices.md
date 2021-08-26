---
title: dispositivos touchpad de Windows precision
description: dispositivos touchpad de Windows precision
ms.assetid: 026F9940-C985-4F3A-BDBB-2977B14EAB1F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb81978c9c9849dfa0d073a4b37af3760d1d4e5bc8e8fa2e81317293db04fc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007896"
---
# <a name="windows-precision-touchpad-devices"></a>dispositivos touchpad de Windows precision

## <a name="platforms"></a>Plataformas

<dl> Clientes-Windows 8.1  
</dl>

## <a name="description"></a>Descrição

o Touchpad de precisão de Windows é uma nova classe de dispositivos de entrada que fornece funcionalidade de gesto e entrada de ponteiro de alta precisão. Por padrão, esses dispositivos geram mensagens de roda de rolagem de precisão extremamente alta para o consumo de aplicativos de área de trabalho.

## <a name="manifestations"></a>Manifestações

Os aplicativos que não foram projetados para lidar com mensagens de roda de rolagem de precisão extremamente alta podem sobrerolar ou não rolar corretamente.

## <a name="mitigation"></a>Atenuação

Os desenvolvedores de aplicativos devem examinar o Delta de rolagem nas mensagens da roda de rolagem do mouse e modificar seus aplicativos adequadamente; no entanto, no interim, um aplicativo pode recusar mensagens de roda de rolagem de precisão extremamente alta (Delta = 1) e escolher para receber mensagens de roda de rolagem de alta precisão (Delta = 40) ou mensagens de roda de rolagem padrão (Delta = 120).

## <a name="solution"></a>Solução

se o aplicativo for capaz de lidar com mensagens de roda de rolagem de precisão extremamente alta, nada precisará ser feito, pois essa é a mensagem padrão enviada por touchpads de precisão Windows.

Se o aplicativo for capaz de lidar com mensagens de roda de rolagem de alta precisão, mas não para mensagens de roda de precisão ultra alta, adicione o seguinte ao manifesto do aplicativo:


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



Se o aplicativo não for capaz de lidar com mensagens de roda de rolagem de alta precisão ou mensagens de roda de precisão extremamente alta, adicione o seguinte ao manifesto do aplicativo para indicar que as mensagens de roda de rolagem padrão são desejadas:


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




