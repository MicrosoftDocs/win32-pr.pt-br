---
description: O WIA (Windows Image Acquisition) Fornece objetos de automação para uso em linguagens de script, como o software de desenvolvimento Microsoft JScript e Microsoft Visual Basic Scripting Edition (VBScript) e linguagens de programação de alto nível, como o sistema de desenvolvimento Microsoft Visual Basic.
ms.assetid: 3d294db3-3349-4b26-aae1-1e3f588a0f0e
title: Modelo de script WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e70863e60e0d7aa6172bd9c93240f38cac27c6be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798000"
---
# <a name="wia-scripting-model"></a>Modelo de script WIA

O WIA (Windows Image Acquisition) Fornece objetos de automação para uso em linguagens de script, como o software de desenvolvimento Microsoft JScript e Microsoft Visual Basic Scripting Edition (VBScript) e linguagens de programação de alto nível, como o sistema de desenvolvimento Microsoft Visual Basic.

> [!Note]  
> Este sistema de scripts foi substituído pela camada de automação da WIA (aquisição de imagem do Windows). Consulte [camada de automação de aquisição de imagem do Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

A tabela a seguir descreve os objetos de script WIA e como eles são usados. 

| Objeto                                | Descrição                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WIA**](-wia-wia.md)               | O objeto de script WIA de nível superior. Use o objeto [**WIA**](-wia-wia.md) para enumerar e conectar-se a dispositivos e para manipular eventos de dispositivo de hardware.                                        |
| [**DeviceInfo**](-wia-deviceinfo.md) | O objeto [**DeviceInfo**](-wia-deviceinfo.md) fornece acesso a informações sobre as propriedades do dispositivo.                                                                                     |
| [**Item**](-wia-item.md)             | Este objeto representa os itens de dispositivo, arquivo e pasta WIA. Um dispositivo de hardware WIA e suas imagens ou ambientes de verificação são representados como uma árvore hierárquica de objetos de [**Item**](-wia-item.md) . |



 

O objeto [**DeviceInfo**](-wia-deviceinfo.md) e o objeto [**Item**](-wia-item.md) estão associados a objetos de coleção. Para obter informações sobre como usar objetos de coleção, consulte usando objetos da coleção WIA.

Os tópicos a seguir abordam informações gerais sobre como usar o modelo de script WIA:

-   [Convenções de sintaxe](-wia-syntax-conventions.md)
-   [Usando objetos de coleção WIA](-wia-using-wia-collection-objects.md)
-   [Definições de constante da propriedade WIA](-wia-wia-property-constant-definitions.md)

 

 
