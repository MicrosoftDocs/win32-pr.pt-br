---
description: O WIA representa um dispositivo de câmera como uma árvore hierárquica de objetos IWiaItem.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: Dispositivos de câmera WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb2023af90df6f868dfcace6f088bfe7ffeb6b549e0e20661231497f3fdf014
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592716"
---
# <a name="wia-camera-devices"></a>Dispositivos de câmera WIA

O WIA representa um dispositivo de câmera como uma árvore hierárquica de [**objetos IWiaItem.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) O item raiz, retornado de uma chamada para o método [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) do gerenciador de dispositivos wia (aquisição de imagem) do Windows, é usado para obter e definir informações do dispositivo, controlar o dispositivo e iniciar a enumeração de item de dispositivo.

> [!Note]  
> O WIA não dá suporte a câmeras Windows Vista ou posterior. Para essas versões do Windows, use Windows API wpd (dispositivo portátil) descrita no DDK (Kit de Desenvolvimento de Driver) do Windows para adquirir imagens de câmeras.

 

O diagrama a seguir ilustra uma implementação de câmera de exemplo. O item raiz da câmera tem três itens filho, duas imagens e uma pasta. A pasta tem dois itens filho, ambas as imagens.

![implementação da câmera de exemplo](images/wihierar.gif)

 

 



