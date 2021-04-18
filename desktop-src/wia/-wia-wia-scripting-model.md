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
# <a name="wia-scripting-model"></a><span data-ttu-id="1ae55-103">Modelo de script WIA</span><span class="sxs-lookup"><span data-stu-id="1ae55-103">WIA Scripting Model</span></span>

<span data-ttu-id="1ae55-104">O WIA (Windows Image Acquisition) Fornece objetos de automação para uso em linguagens de script, como o software de desenvolvimento Microsoft JScript e Microsoft Visual Basic Scripting Edition (VBScript) e linguagens de programação de alto nível, como o sistema de desenvolvimento Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1ae55-104">Windows Image Acquisition (WIA) provides automation objects for use in scripting languages, such as Microsoft JScript and Microsoft Visual Basic Scripting Edition (VBScript) development software, and high-level programming languages such as Microsoft Visual Basic development system.</span></span>

> [!Note]  
> <span data-ttu-id="1ae55-105">Este sistema de scripts foi substituído pela camada de automação da WIA (aquisição de imagem do Windows).</span><span class="sxs-lookup"><span data-stu-id="1ae55-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="1ae55-106">Consulte [camada de automação de aquisição de imagem do Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="1ae55-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="1ae55-107">A tabela a seguir descreve os objetos de script WIA e como eles são usados.</span><span class="sxs-lookup"><span data-stu-id="1ae55-107">The following table describes WIA scripting objects and how they are used.</span></span> 

| <span data-ttu-id="1ae55-108">Objeto</span><span class="sxs-lookup"><span data-stu-id="1ae55-108">Object</span></span>                                | <span data-ttu-id="1ae55-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ae55-109">Description</span></span>                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ae55-110">**WIA**</span><span class="sxs-lookup"><span data-stu-id="1ae55-110">**Wia**</span></span>](-wia-wia.md)               | <span data-ttu-id="1ae55-111">O objeto de script WIA de nível superior.</span><span class="sxs-lookup"><span data-stu-id="1ae55-111">The top-level WIA scripting object.</span></span> <span data-ttu-id="1ae55-112">Use o objeto [**WIA**](-wia-wia.md) para enumerar e conectar-se a dispositivos e para manipular eventos de dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="1ae55-112">Use the [**Wia**](-wia-wia.md) object to enumerate and connect to devices, and to handle hardware device events.</span></span>                                        |
| [<span data-ttu-id="1ae55-113">**DeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="1ae55-113">**DeviceInfo**</span></span>](-wia-deviceinfo.md) | <span data-ttu-id="1ae55-114">O objeto [**DeviceInfo**](-wia-deviceinfo.md) fornece acesso a informações sobre as propriedades do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1ae55-114">The [**DeviceInfo**](-wia-deviceinfo.md) object provides access to information about device properties.</span></span>                                                                                     |
| [<span data-ttu-id="1ae55-115">**Item**</span><span class="sxs-lookup"><span data-stu-id="1ae55-115">**Item**</span></span>](-wia-item.md)             | <span data-ttu-id="1ae55-116">Este objeto representa os itens de dispositivo, arquivo e pasta WIA.</span><span class="sxs-lookup"><span data-stu-id="1ae55-116">This object represents WIA device, file, and folder items.</span></span> <span data-ttu-id="1ae55-117">Um dispositivo de hardware WIA e suas imagens ou ambientes de verificação são representados como uma árvore hierárquica de objetos de [**Item**](-wia-item.md) .</span><span class="sxs-lookup"><span data-stu-id="1ae55-117">A WIA hardware device and its images or scanning beds is represented as a hierarchical tree of [**Item**](-wia-item.md) objects.</span></span> |



 

<span data-ttu-id="1ae55-118">O objeto [**DeviceInfo**](-wia-deviceinfo.md) e o objeto [**Item**](-wia-item.md) estão associados a objetos de coleção.</span><span class="sxs-lookup"><span data-stu-id="1ae55-118">Both the [**DeviceInfo**](-wia-deviceinfo.md) object and the [**Item**](-wia-item.md) object are associated with collection objects.</span></span> <span data-ttu-id="1ae55-119">Para obter informações sobre como usar objetos de coleção, consulte usando objetos da coleção WIA.</span><span class="sxs-lookup"><span data-stu-id="1ae55-119">For information about using collection objects, see Using WIA Collection Objects.</span></span>

<span data-ttu-id="1ae55-120">Os tópicos a seguir abordam informações gerais sobre como usar o modelo de script WIA:</span><span class="sxs-lookup"><span data-stu-id="1ae55-120">The following topics cover general information about using the WIA scripting model:</span></span>

-   [<span data-ttu-id="1ae55-121">Convenções de sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ae55-121">Syntax Conventions</span></span>](-wia-syntax-conventions.md)
-   [<span data-ttu-id="1ae55-122">Usando objetos de coleção WIA</span><span class="sxs-lookup"><span data-stu-id="1ae55-122">Using WIA Collection Objects</span></span>](-wia-using-wia-collection-objects.md)
-   [<span data-ttu-id="1ae55-123">Definições de constante da propriedade WIA</span><span class="sxs-lookup"><span data-stu-id="1ae55-123">WIA Property Constant Definitions</span></span>](-wia-wia-property-constant-definitions.md)

 

 
