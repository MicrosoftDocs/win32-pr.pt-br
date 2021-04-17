---
description: Usando propriedades personalizadas.
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: Usando propriedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca9f8092afa5b8af22080b154fff79a32a6f304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811466"
---
# <a name="using-custom-properties"></a><span data-ttu-id="1c563-103">Usando propriedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="1c563-103">Using Custom Properties</span></span>

<span data-ttu-id="1c563-104">**Usando propriedades personalizadas**.</span><span class="sxs-lookup"><span data-stu-id="1c563-104">**Using Custom Properties**.</span></span>

<span data-ttu-id="1c563-105">Um driver WIA (aquisição de imagem do Windows) pode definir suas próprias propriedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="1c563-105">A Windows Image Acquisition (WIA) driver can define its own custom properties.</span></span> <span data-ttu-id="1c563-106">Os chamadores podem manipular propriedades personalizadas assim como as propriedades de WIA normais.</span><span class="sxs-lookup"><span data-stu-id="1c563-106">Callers can manipulate custom properties just as they would normal WIA properties.</span></span> <span data-ttu-id="1c563-107">No entanto, somente seu aplicativo ou módulo de interface do usuário personalizada pode acessar essas propriedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="1c563-107">However, only your application or custom UI module can access these custom properties.</span></span>

<span data-ttu-id="1c563-108">Os drivers WIA devem definir as propriedades personalizadas para que os identificadores de propriedade sejam deslocados pelo \_ \_ DEVPROP privado do WIA para as propriedades do dispositivo e usem \_ o ItemProperty privado do WIA \_ para propriedades normais do item, como dentro de [IWiaMiniDrv::d rvinititemproperties](https://msdn.microsoft.com/library/ms794131.aspx).</span><span class="sxs-lookup"><span data-stu-id="1c563-108">WIA drivers should define the custom properties to have property identifiers that are offset by WIA\_PRIVATE\_DEVPROP for device properties, and use WIA\_PRIVATE\_ITEMPROP for normal item properties, such as inside [IWiaMiniDrv::drvInitItemProperties](https://msdn.microsoft.com/library/ms794131.aspx).</span></span> <span data-ttu-id="1c563-109">Para obter mais informações, consulte [definindo propriedades personalizadas](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="1c563-109">For more information, see [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="1c563-110">Há duas maneiras de passar parâmetros personalizados para drivers WIA.</span><span class="sxs-lookup"><span data-stu-id="1c563-110">There are two ways to pass custom parameters to WIA drivers.</span></span>

<span data-ttu-id="1c563-111">A primeira opção é usar o método **IWiaItemExtras:: escape** (descrito na documentação do Platform SDK).</span><span class="sxs-lookup"><span data-stu-id="1c563-111">The first option is to use the **IWiaItemExtras::Escape** method (described in the Platform SDK documentation).</span></span> <span data-ttu-id="1c563-112">Isso é semelhante ao método [IStiUSD:: escape](https://msdn.microsoft.com/library/ms794396.aspx) , mas permite que os chamadores usem o WIA diretamente, em vez de usar métodos STI.</span><span class="sxs-lookup"><span data-stu-id="1c563-112">This is similar to the [IStiUSD::Escape](https://msdn.microsoft.com/library/ms794396.aspx) method, but it allows callers to use WIA directly, instead of using STI methods.</span></span> <span data-ttu-id="1c563-113">Usando **IWiaItemExtras:: escape**, você pode passar todas as informações para o driver e o driver pode passar qualquer informação de volta.</span><span class="sxs-lookup"><span data-stu-id="1c563-113">Using **IWiaItemExtras::Escape**, you can pass any information to the driver, and the driver can pass any information back.</span></span> <span data-ttu-id="1c563-114">O serviço WIA gerencia somente os buffers passados entre o chamador e o driver.</span><span class="sxs-lookup"><span data-stu-id="1c563-114">The WIA service manages only those buffers passed between the caller and the driver.</span></span>

<span data-ttu-id="1c563-115">A segunda opção é usar propriedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="1c563-115">The second option is to use custom properties.</span></span> <span data-ttu-id="1c563-116">O uso do método **IWiaItemExtras:: escape** é mais flexível do que o uso de propriedades WIA personalizadas, mas as propriedades WIA personalizadas permitem que você armazene informações no fluxo de propriedades do item para que o driver possa ler as informações em outro momento.</span><span class="sxs-lookup"><span data-stu-id="1c563-116">Using the **IWiaItemExtras::Escape** method is more flexible than using custom WIA properties, but custom WIA properties allow you to store information in the item's property stream so that the driver can read the information at another time.</span></span>

 

 



