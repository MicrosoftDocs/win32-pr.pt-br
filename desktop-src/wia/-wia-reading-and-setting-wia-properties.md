---
description: A interface IWiaPropertyStorage fornece métodos para ler e gravar as propriedades de um item de aquisição de imagem do Windows (WIA). As propriedades do item incluem comandos de dispositivo, informações de formato de item e informações de dispositivo.
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: Lendo e definindo propriedades WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51df3e8fdb4b29abb6f64743ab8f7f2dd3776358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090497"
---
# <a name="reading-and-setting-wia-properties"></a><span data-ttu-id="e62ff-104">Lendo e definindo propriedades WIA</span><span class="sxs-lookup"><span data-stu-id="e62ff-104">Reading and Setting WIA Properties</span></span>

<span data-ttu-id="e62ff-105">A interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) fornece métodos para ler e gravar as propriedades de um item de aquisição de imagem do Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="e62ff-105">The [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface provides methods for reading and writing a Windows Image Acquisition (WIA) item's properties.</span></span> <span data-ttu-id="e62ff-106">As propriedades do item incluem comandos de dispositivo, informações de formato de item e informações de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e62ff-106">Item properties include device commands, item format information, and device information.</span></span>

<span data-ttu-id="e62ff-107">Um aplicativo pode obter um ponteiro para uma interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) de um item enumerando as informações do dispositivo ou informações de evento do item chamando [**IWiaItem:: EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) ou [**IWiaItem:: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) ou consultando a interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) do item.</span><span class="sxs-lookup"><span data-stu-id="e62ff-107">An application can obtain a pointer to an [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface of an item either by enumerating the item's device information or event information by calling [**IWiaItem::EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) or [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) or by querying the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface of the item.</span></span> <span data-ttu-id="e62ff-108">(No WIA 2,0, faça isso chamando [**IWiaItem2:: EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) ou [**IWiaItem2:: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) ou consultando a interface [**IWiaItem2**](-wia-iwiaitem2.md) do item.)</span><span class="sxs-lookup"><span data-stu-id="e62ff-108">(In WIA 2.0, do this by calling [**IWiaItem2::EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) or [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) or by querying the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item.)</span></span>

<span data-ttu-id="e62ff-109">O [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) herda de [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) e os métodos herdados são implementados conforme descrito na seção de referência de armazenamento estruturado no SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="e62ff-109">[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) inherits from [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) and the inherited methods are implemented as described in the reference section of Structured Storage in the Windows Software Development Kit (SDK).</span></span>

> [!Note]
>
> <span data-ttu-id="e62ff-110">Os aplicativos WIA sempre devem ler cabeçalhos de dados de imagem para obter informações precisas sobre a imagem.</span><span class="sxs-lookup"><span data-stu-id="e62ff-110">WIA applications should always read image data headers for accurate image information.</span></span> <span data-ttu-id="e62ff-111">O driver WIA pode alterar as propriedades de WIA e os cabeçalhos de dados de imagem durante a transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="e62ff-111">The WIA driver can alter the WIA properties and image data headers during data transfer.</span></span>
>
> <span data-ttu-id="e62ff-112">Se não houver nenhum cabeçalho de dados de imagem fornecido com o formato especificado, o aplicativo WIA deverá usar as propriedades WIA como uma fonte de informações sobre a transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="e62ff-112">If there is no image data header supplied with the specified format, the WIA application should use the WIA properties as an information source about the data transfer.</span></span> <span data-ttu-id="e62ff-113">O aplicativo WIA deve ler novamente as propriedades de WIA necessárias depois que a verificação ou captura for concluída para obter as configurações atualizadas.</span><span class="sxs-lookup"><span data-stu-id="e62ff-113">The WIA application should reread the needed WIA properties after the scan or capture completes to get the updated settings.</span></span>

 

<span data-ttu-id="e62ff-114">As seções a seguir descrevem as várias propriedades de WIA:</span><span class="sxs-lookup"><span data-stu-id="e62ff-114">The following sections describe the various WIA properties:</span></span>

-   [<span data-ttu-id="e62ff-115">Validação da propriedade WIA</span><span class="sxs-lookup"><span data-stu-id="e62ff-115">WIA Property Validation</span></span>](-wia-wia-property-validation.md)
-   [<span data-ttu-id="e62ff-116">Propriedades de informações do dispositivo</span><span class="sxs-lookup"><span data-stu-id="e62ff-116">Device Information Properties</span></span>](-wia-device-information-properties-wia-dip-xxxx.md)
-   [<span data-ttu-id="e62ff-117">Propriedades do Dispositivo</span><span class="sxs-lookup"><span data-stu-id="e62ff-117">Device Properties</span></span>](-wia-device-properties.md)
-   [<span data-ttu-id="e62ff-118">Propriedades do item</span><span class="sxs-lookup"><span data-stu-id="e62ff-118">Item Properties</span></span>](-wia-item-properties.md)
-   [<span data-ttu-id="e62ff-119">Propriedades de WIA adicionais</span><span class="sxs-lookup"><span data-stu-id="e62ff-119">Additional WIA Properties</span></span>](-wia-additional-wia-properties.md)
-   [<span data-ttu-id="e62ff-120">Definindo propriedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="e62ff-120">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
-   [<span data-ttu-id="e62ff-121">Usando propriedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="e62ff-121">Using Custom Properties</span></span>](-wia-using-custom-properties.md)
-   [<span data-ttu-id="e62ff-122">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="e62ff-122">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)

 

 
