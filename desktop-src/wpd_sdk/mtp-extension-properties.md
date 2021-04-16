---
description: Propriedades de extensão MTP
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: Propriedades de extensão MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a653d05285d62c7660bd914a785807a2341a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105808358"
---
# <a name="mtp-extension-properties"></a><span data-ttu-id="f7373-103">Propriedades de extensão MTP</span><span class="sxs-lookup"><span data-stu-id="f7373-103">MTP Extension Properties</span></span>

<span data-ttu-id="f7373-104">As propriedades descrevem objetos, propriedades, recursos e dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f7373-104">Properties describe objects, properties, resources, and devices.</span></span>

## <a name="vendor-extended-object-properties"></a><span data-ttu-id="f7373-105">Fornecedor-Propriedades de objeto estendido</span><span class="sxs-lookup"><span data-stu-id="f7373-105">Vendor-Extended Object Properties</span></span>

<span data-ttu-id="f7373-106">Quando um fabricante de dispositivo cria uma propriedade estendida de fornecedor para um objeto de dispositivo, ele combina o GUID de **\_ Propriedades de \_ \_ \_ objeto estendido do fornecedor \_ \_ MTP** de propriedade com o código de propriedades do objeto para construir uma estrutura **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="f7373-106">When a device manufacturer creates a vendor-extended property for a device object, they combine the **WPD\_PROPERTIES\_MTP\_VENDOR\_EXTENDED\_OBJECT\_PROPS** GUID with the object's property code to construct a **PROPERTYKEY** structure.</span></span>

<span data-ttu-id="f7373-107">Por exemplo, se o código de Propriedade do objeto for 0xD801, o **PROPERTYKEY** resultante será como mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="f7373-107">For example, if the object's property code is 0xD801, the resulting **PROPERTYKEY** would be as shown in the following example:</span></span>


```C++
{4D545058-4FCE-4578-95C8-8698A9BC0F49}\D801
```



## <a name="vendor-extended-device-properties"></a><span data-ttu-id="f7373-108">Fornecedor-Propriedades do dispositivo estendido</span><span class="sxs-lookup"><span data-stu-id="f7373-108">Vendor-Extended Device Properties</span></span>

<span data-ttu-id="f7373-109">Quando um fabricante de dispositivo cria uma propriedade estendida do fornecedor para um dispositivo, ele combina o GUID de **\_ Propriedades do \_ \_ \_ \_ dispositivo \_ estendido do fornecedor MTP do provedor** do objeto com o código de propriedade para construir uma estrutura **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="f7373-109">When a device manufacturer creates a vendor-extended property for a device, they combine the **WPD\_PROPERTIES\_MTP\_VENDOR\_EXTENDED\_DEVICE\_PROPS** GUID with the object's property code to construct a **PROPERTYKEY** structure.</span></span>

<span data-ttu-id="f7373-110">Por exemplo, se o código de Propriedade do objeto for 0xD001, o **PROPERTYKEY** resultante será como mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="f7373-110">For example, if the object's property code is 0xD001, the resulting **PROPERTYKEY** would be as shown in the following example:</span></span>


```C++
{4D545058-8900-40b3-8F1D-DC246E1E8370}\D001
```



## <a name="related-topics"></a><span data-ttu-id="f7373-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7373-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7373-112">Suporte a extensões de MTP</span><span class="sxs-lookup"><span data-stu-id="f7373-112">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



