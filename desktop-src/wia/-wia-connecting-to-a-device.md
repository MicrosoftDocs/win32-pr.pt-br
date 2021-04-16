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
ms.openlocfilehash: fc7d8c78f77854a9adbedad7c0870721b3b037ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765589"
---
# <a name="connecting-to-a-device"></a>Conectando a um dispositivo

> [!Note]  
> Este sistema de scripts foi substituído pela camada de automação da WIA (aquisição de imagem do Windows). Consulte [camada de automação de aquisição de imagem do Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

A primeira etapa em qualquer aplicativo ou script que usa o modelo de script de aquisição de imagem do Windows (WIA) está criando o objeto [**WIA**](-wia-wia.md) . Esse objeto fornece métodos para obter uma coleção de objetos [**DeviceInfo**](-wia-deviceinfo.md) e conectar esses objetos a dispositivos. Ele também fornece a capacidade de escutar eventos de hardware WIA.

A linha a seguir do código do Microsoft Visual Basic Scripting Edition (VBScript) cria o objeto [**WIA**](-wia-wia.md) :


```
objWia = CreateObject("Wia.Script")
```



Depois de criar o objeto [**WIA**](-wia-wia.md) , use seu método [**Create**](-wia-iwia-create.md) para se conectar a um dispositivo de hardware WIA.

Você também pode usar a propriedade de [**dispositivos**](-wia-iwia-devices.md) do objeto [**WIA**](-wia-wia.md) para obter uma coleção de objetos [**DeviceInfo**](-wia-deviceinfo.md) . Enumere essa coleção e use o método [**Create**](-wia-iwiadeviceinfo-create.md) para se conectar a um dispositivo.

 

 
