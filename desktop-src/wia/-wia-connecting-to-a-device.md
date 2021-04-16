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
# <a name="connecting-to-a-device"></a><span data-ttu-id="05a19-103">Conectando a um dispositivo</span><span class="sxs-lookup"><span data-stu-id="05a19-103">Connecting to a Device</span></span>

> [!Note]  
> <span data-ttu-id="05a19-104">Este sistema de scripts foi substituído pela camada de automação da WIA (aquisição de imagem do Windows).</span><span class="sxs-lookup"><span data-stu-id="05a19-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="05a19-105">Consulte [camada de automação de aquisição de imagem do Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="05a19-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="05a19-106">A primeira etapa em qualquer aplicativo ou script que usa o modelo de script de aquisição de imagem do Windows (WIA) está criando o objeto [**WIA**](-wia-wia.md) .</span><span class="sxs-lookup"><span data-stu-id="05a19-106">The first step in any application or script that uses the Windows Image Acquisition (WIA) scripting model is creating the [**Wia**](-wia-wia.md) object.</span></span> <span data-ttu-id="05a19-107">Esse objeto fornece métodos para obter uma coleção de objetos [**DeviceInfo**](-wia-deviceinfo.md) e conectar esses objetos a dispositivos.</span><span class="sxs-lookup"><span data-stu-id="05a19-107">This object provides methods for to obtain a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects and connect these objects to devices.</span></span> <span data-ttu-id="05a19-108">Ele também fornece a capacidade de escutar eventos de hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="05a19-108">It also provides the ability to listen for WIA hardware events.</span></span>

<span data-ttu-id="05a19-109">A linha a seguir do código do Microsoft Visual Basic Scripting Edition (VBScript) cria o objeto [**WIA**](-wia-wia.md) :</span><span class="sxs-lookup"><span data-stu-id="05a19-109">The following line of Microsoft Visual Basic Scripting Edition (VBScript) code creates the [**Wia**](-wia-wia.md) object:</span></span>


```
objWia = CreateObject("Wia.Script")
```



<span data-ttu-id="05a19-110">Depois de criar o objeto [**WIA**](-wia-wia.md) , use seu método [**Create**](-wia-iwia-create.md) para se conectar a um dispositivo de hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="05a19-110">After creating the [**Wia**](-wia-wia.md) object, use its [**Create**](-wia-iwia-create.md) method to connect to a WIA hardware device.</span></span>

<span data-ttu-id="05a19-111">Você também pode usar a propriedade de [**dispositivos**](-wia-iwia-devices.md) do objeto [**WIA**](-wia-wia.md) para obter uma coleção de objetos [**DeviceInfo**](-wia-deviceinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="05a19-111">You can also use the [**Wia**](-wia-wia.md) object's [**Devices**](-wia-iwia-devices.md) property to obtain a collection of [**DeviceInfo**](-wia-deviceinfo.md) objects.</span></span> <span data-ttu-id="05a19-112">Enumere essa coleção e use o método [**Create**](-wia-iwiadeviceinfo-create.md) para se conectar a um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="05a19-112">Enumerate this collection and use the [**Create**](-wia-iwiadeviceinfo-create.md) method to connect to a device.</span></span>

 

 
