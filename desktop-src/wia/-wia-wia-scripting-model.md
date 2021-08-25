---
description: Windows A WIA (Aquisição de Imagem) fornece objetos de automação para uso em linguagens de script, como software de desenvolvimento do Microsoft JScript e VBScript (Microsoft Visual Basic Scripting Edition) e linguagens de programação de alto nível, como o sistema de desenvolvimento microsoft Visual Basic.
ms.assetid: 3d294db3-3349-4b26-aae1-1e3f588a0f0e
title: Modelo de script WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b558e84dd4095fd0d5dc3f1f14a7de76d9108c488cf3fc3613e3a09bc4830714
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812846"
---
# <a name="wia-scripting-model"></a>Modelo de script WIA

Windows A WIA (Aquisição de Imagem) fornece objetos de automação para uso em linguagens de script, como software de desenvolvimento do Microsoft JScript e VBScript (Microsoft Visual Basic Scripting Edition) e linguagens de programação de alto nível, como o sistema de desenvolvimento microsoft Visual Basic.

> [!Note]  
> Esse sistema de scripts foi substituído pela camada de automação wia (aquisição de imagem) Windows imagem. Consulte [Windows de automação de aquisição de imagem.](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)

 

A tabela a seguir descreve objetos de script WIA e como eles são usados. 

| Objeto                                | Descrição                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wia**](-wia-wia.md)               | O objeto de script WIA de nível superior. Use o [**objeto Wia**](-wia-wia.md) para enumerar e conectar-se a dispositivos e manipular eventos de dispositivo de hardware.                                        |
| [**DeviceInfo**](-wia-deviceinfo.md) | O [**objeto DeviceInfo**](-wia-deviceinfo.md) fornece acesso a informações sobre as propriedades do dispositivo.                                                                                     |
| [**Item**](-wia-item.md)             | Esse objeto representa itens de dispositivo, arquivo e pasta WIA. Um dispositivo de hardware WIA e suas imagens ou colchas de varredura são representados como uma árvore hierárquica de [**objetos item.**](-wia-item.md) |



 

O objeto [**DeviceInfo**](-wia-deviceinfo.md) e o [**objeto Item**](-wia-item.md) estão associados a objetos de coleção. Para obter informações sobre como usar objetos de coleção, consulte Usando objetos de coleção WIA.

Os tópicos a seguir abrangem informações gerais sobre como usar o modelo de script WIA:

-   [Convenções de sintaxe](-wia-syntax-conventions.md)
-   [Usando objetos de coleção WIA](-wia-using-wia-collection-objects.md)
-   [Definições constantes da propriedade WIA](-wia-wia-property-constant-definitions.md)

 

 
