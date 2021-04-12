---
description: O WIA representa um dispositivo de câmera como uma árvore hierárquica de objetos IWiaItem.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: Dispositivos de câmera WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002a14d8e047019b1af2d2f86c1fd4a2e00d7808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164520"
---
# <a name="wia-camera-devices"></a>Dispositivos de câmera WIA

O WIA representa um dispositivo de câmera como uma árvore hierárquica de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . O item raiz, retornado de uma chamada para o método Gerenciador de dispositivo de aquisição de imagens do Windows (WIA) [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) , é usado para obter e definir informações do dispositivo, para controlar o dispositivo e para iniciar a enumeração do item do dispositivo.

> [!Note]  
> O WIA não oferece suporte a câmeras no Windows Vista ou posterior. Para essas versões do Windows, use a API do dispositivo portátil do Windows (WPD) descrita no kit de desenvolvimento de driver do Windows (DDK) para adquirir imagens de câmeras.

 

O diagrama a seguir ilustra uma implementação de câmera de exemplo. O item da raiz da câmera tem três itens filho, duas imagens e uma pasta. A pasta tem dois itens filho, ambas as imagens.

![implementação de câmera de exemplo](images/wihierar.gif)

 

 



