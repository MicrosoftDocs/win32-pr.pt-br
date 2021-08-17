---
description: 'Saiba mais sobre: conectando-se a um dispositivo'
ms.assetid: 16ff280d-818b-4a4e-b5a6-16e81f5b35c6
title: Conectando a um dispositivo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf98c11b285d4c7aa4705095af99f35c129e27311dbe19ff42e4b0d288c45efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451216"
---
# <a name="connecting-to-a-device"></a>Conectando a um dispositivo

> [!Note]  
> este sistema de scripts foi substituído pela camada de automação da WIA (Windows Image Acquisition). consulte [Windows camada de automação de aquisição de imagem](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

a primeira etapa em qualquer aplicativo ou script que usa o modelo de script wia (Windows Image Acquisition) está criando o objeto [**WIA**](-wia-wia.md) . Esse objeto fornece métodos para obter uma coleção de objetos [**DeviceInfo**](-wia-deviceinfo.md) e conectar esses objetos a dispositivos. Ele também fornece a capacidade de escutar eventos de hardware WIA.

a linha a seguir do código do Microsoft Visual Basic scripting Edition (VBScript) cria o objeto [**Wia**](-wia-wia.md) :


```
objWia = CreateObject("Wia.Script")
```



Depois de criar o objeto [**WIA**](-wia-wia.md) , use seu método [**Create**](-wia-iwia-create.md) para se conectar a um dispositivo de hardware WIA.

Você também pode usar a propriedade de [**dispositivos**](-wia-iwia-devices.md) do objeto [**WIA**](-wia-wia.md) para obter uma coleção de objetos [**DeviceInfo**](-wia-deviceinfo.md) . Enumere essa coleção e use o método [**Create**](-wia-iwiadeviceinfo-create.md) para se conectar a um dispositivo.

 

 
