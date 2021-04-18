---
description: As seguintes constantes de propriedade de dispositivo devem ser suportadas por todas as interfaces de interface IWiaItem, IWiaItem2 e IWiaDrvItem, a menos que indicado de outra forma em suas descrições.
ms.assetid: ef48313e-4df4-4ccd-a085-f714100885a7
title: Constantes de propriedade de item WIA comuns (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPA_ACCESS_RIGHTS
- WIA_IPA_APP_COLOR_MAPPING
- WIA_IPA_BITS_PER_CHANNEL
- WIA_IPA_BUFFER_SIZE
- WIA_IPA_BYTES_PER_LINE
- WIA_IPA_CHANNELS_PER_PIXEL
- WIA_IPA_COLOR_PROFILE
- WIA_IPA_COMPRESSION
- WIA_IPA_DATATYPE
- WIA_IPA_DEPTH
- WIA_IPA_FILENAME_EXTENSION
- WIA_IPA_FORMAT
- WIA_IPA_FULL_ITEM_NAME
- WIA_IPA_GAMMA_CURVES
- WIA_IPA_ICM_PROFILE_NAME
- WIA_IPA_ITEM_CATEGORY
- WIA_IPA_ITEM_FLAGS
- WIA_IPA_ITEM_NAME
- WIA_IPA_ITEM_SIZE
- WIA_IPA_ITEM_TIME
- WIA_IPA_ITEMS_STORED
- WIA_IPA_MIN_BUFFER_SIZE
- WIA_IPA_NUMBER_OF_LINES
- WIA_IPA_PIXELS_PER_LINE
- WIA_IPA_PLANAR
- WIA_IPA_PREFERRED_FORMAT
- WIA_IPA_PROP_STREAM_COMPAT_ID
- WIA_IPA_RAW_BITS_PER_CHANNEL
- WIA_IPA_REGION_TYPE
- WIA_IPA_SUPPRESS_PROPERTY_PAGE
- WIA_IPA_TYMED
- WIA_IPA_UPLOAD_ITEM_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: d36a390256c6a9d183caa0f9231d2a92035d83da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789244"
---
# <a name="common-wia-item-property-constants"></a><span data-ttu-id="c02be-103">Constantes de propriedade de item WIA comuns</span><span class="sxs-lookup"><span data-stu-id="c02be-103">Common WIA Item Property Constants</span></span>

<span data-ttu-id="c02be-104">As seguintes constantes de propriedade de dispositivo devem ser suportadas por todas as interfaces de interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) e [IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) , a menos que indicado de outra forma em suas descrições.</span><span class="sxs-lookup"><span data-stu-id="c02be-104">The following device property constants must be supported by all [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) and [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) interfaces unless otherwise noted in their descriptions.</span></span>

<span data-ttu-id="c02be-105">O prefixo "WIA \_ IPA \_ " indica uma propriedade de item para todos os dispositivos e é a Convenção de nomenclatura usada em C/C++.</span><span class="sxs-lookup"><span data-stu-id="c02be-105">The prefix "WIA\_IPA\_" indicates an item property for all devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="c02be-106">Para fins de script, essas constantes usam o prefixo "Picture" e fazem parte do tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="c02be-106">For scripting purposes these constants use the prefix "Picture" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="c02be-107">O nome de membro correspondente dessa enumeração de script aparece entre parênteses ao lado do nome da constante C/C++ na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="c02be-107">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="c02be-108">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="c02be-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c02be-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c02be-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ACCESS_RIGHTS"></span><span id="wia_ipa_access_rights"></span><dl> <span data-ttu-id="c02be-110"><dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-110"><dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c02be-111">Esse sinalizador controla o acesso ao item, bem como se o item é excluído.</span><span class="sxs-lookup"><span data-stu-id="c02be-111">This flag controls access to the item as well as whether the item is deleted.</span></span><br/> <span data-ttu-id="c02be-112">Necessário para todos os itens do WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="c02be-112">Required for all WIA 2.0 items.</span></span><br/> <span data-ttu-id="c02be-113">Tipo: <strong>VT_I4</strong>; Leitura/gravação ou somente leitura, dependendo da capacidade do item de ter seus direitos de acesso alterados; Valores válidos: WIA_PROP_FLAG</span><span class="sxs-lookup"><span data-stu-id="c02be-113">Type: <strong>VT_I4</strong>; Read/Write or Read Only, depending on the item's ability to have its access rights changed; Valid values: WIA_PROP_FLAG</span></span><br/> <span data-ttu-id="c02be-114">A tabela a seguir tem os cinco sinalizadores que são válidos com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-114">The following table has the five flags that are valid with this property.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c02be-115">Direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="c02be-115">Access Right</span></span></th>
<th><span data-ttu-id="c02be-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c02be-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c02be-117">WIA_ITEM_READ</span><span class="sxs-lookup"><span data-stu-id="c02be-117">WIA_ITEM_READ</span></span></td>
<td><span data-ttu-id="c02be-118">O item tem acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c02be-118">Item has read-only access.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-119">WIA_ITEM_WRITE</span><span class="sxs-lookup"><span data-stu-id="c02be-119">WIA_ITEM_WRITE</span></span></td>
<td><span data-ttu-id="c02be-120">O item tem acesso somente gravação.</span><span class="sxs-lookup"><span data-stu-id="c02be-120">Item has write-only access.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-121">WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="c02be-121">WIA_ITEM_CAN_BE_DELETED</span></span></td>
<td><span data-ttu-id="c02be-122">O item tem acesso somente exclusão.</span><span class="sxs-lookup"><span data-stu-id="c02be-122">Item has delete-only access.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-123">WIA_ITEM_RD</span><span class="sxs-lookup"><span data-stu-id="c02be-123">WIA_ITEM_RD</span></span></td>
<td><span data-ttu-id="c02be-124">WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="c02be-124">WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-125">WIA_ITEM_RWD</span><span class="sxs-lookup"><span data-stu-id="c02be-125">WIA_ITEM_RWD</span></span></td>
<td><span data-ttu-id="c02be-126">WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="c02be-126">WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_APP_COLOR_MAPPING"></span><span id="wia_ipa_app_color_mapping"></span><dl> <span data-ttu-id="c02be-127"><dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-127"><dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-128">Esta propriedade é reservada pelo para uso futuro e não é implementada neste momento.</span><span class="sxs-lookup"><span data-stu-id="c02be-128">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="c02be-129">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-129">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BITS_PER_CHANNEL"></span><span id="wia_ipa_bits_per_channel"></span><dl> <span data-ttu-id="c02be-130"><dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-130"><dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-131">Contém o número de bits por canal para a imagem.</span><span class="sxs-lookup"><span data-stu-id="c02be-131">Contains the number of bits per channel for the image.</span></span> <span data-ttu-id="c02be-132">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-132">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-133">Necessário para todos os itens de imagem armazenados ou habilitados para aquisição do WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="c02be-133">Required for all WIA 2.0 acquisition-enabled or stored image items.</span></span></p>
<p><span data-ttu-id="c02be-134">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-134">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_BUFFER_SIZE"></span><span id="wia_ipa_buffer_size"></span><dl> <span data-ttu-id="c02be-135"><dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-135"><dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-136">Contém o tamanho do buffer, em bytes, usado durante uma transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="c02be-136">Contains the size of the buffer, in bytes, used during a data transfer.</span></span> <span data-ttu-id="c02be-137">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-137">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-138">Um aplicativo pode ler essa propriedade para determinar o tamanho do buffer especificado pelo driver para transferências de dados.</span><span class="sxs-lookup"><span data-stu-id="c02be-138">An application can read this property to determine the driver-specified buffer size for data transfers.</span></span> <span data-ttu-id="c02be-139">O serviço WIA também lê essa propriedade para alocar memória para o minidriver durante a transferência de dados</span><span class="sxs-lookup"><span data-stu-id="c02be-139">The WIA service also reads this property to allocate memory for the minidriver during the data transfer</span></span></p>
<p><span data-ttu-id="c02be-140">Opcional para todos os itens WIA 2,0 habilitados para transferência.</span><span class="sxs-lookup"><span data-stu-id="c02be-140">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="c02be-141">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-141">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="c02be-142">A propriedade <strong>WIA_IPA_BUFFER_SIZE</strong> contém é a quantidade mínima de dados que um aplicativo pode solicitar em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="c02be-142">The <strong>WIA_IPA_BUFFER_SIZE</strong> property contains is the minimum amount of data an application can request at any given time.</span></span> <span data-ttu-id="c02be-143">Quanto maior o tamanho do buffer, maior será as solicitações para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c02be-143">The larger the buffer size, the larger the requests to the device will be.</span></span> <span data-ttu-id="c02be-144">Isso pode fazer com que o dispositivo pareça lento e sem resposta, pode reduzir o desempenho geral do sistema e pode consumir recursos excessivos.</span><span class="sxs-lookup"><span data-stu-id="c02be-144">This can make the device seem slow and unresponsive, can slow the overall system performance, and can consume excessive resources.</span></span> <span data-ttu-id="c02be-145">Os tamanhos de buffer que são muito pequenos podem reduzir o desempenho da transferência de dados exigindo muitas solicitações menores.</span><span class="sxs-lookup"><span data-stu-id="c02be-145">Buffer sizes that are too small can slow performance of the data transfer by requiring many smaller requests.</span></span> <span data-ttu-id="c02be-146">Escolha um tamanho de buffer razoável Considerando o tamanho típico de uma solicitação de dados para seu dispositivo e equilibrando o número de solicitações em relação ao tamanho dessas solicitações.</span><span class="sxs-lookup"><span data-stu-id="c02be-146">Choose a reasonable buffer size by considering the typical size of a data request to your device and balancing the number of requests against the size of those requests.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BYTES_PER_LINE"></span><span id="wia_ipa_bytes_per_line"></span><dl> <span data-ttu-id="c02be-147"><dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-147"><dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-148">Contém o número de bytes em uma linha de verificação da imagem.</span><span class="sxs-lookup"><span data-stu-id="c02be-148">Contains the number of bytes in one scan line of the image.</span></span> <span data-ttu-id="c02be-149">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-149">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-150">Opcional para todos os itens WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="c02be-150">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="c02be-151">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-151">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_CHANNELS_PER_PIXEL"></span><span id="wia_ipa_channels_per_pixel"></span><dl> <span data-ttu-id="c02be-152"><dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-152"><dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-153">Contém o número de canais por pixel para a imagem.</span><span class="sxs-lookup"><span data-stu-id="c02be-153">Contains the number of channels per pixel for the image.</span></span> <span data-ttu-id="c02be-154">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-154">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-155">Necessário para todos os itens de imagem armazenados ou habilitados para aquisição do WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="c02be-155">Required for all WIA 2.0 acquisition-enabled or stored image items.</span></span></p>
<p><span data-ttu-id="c02be-156">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-156">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_COLOR_PROFILE"></span><span id="wia_ipa_color_profile"></span><dl> <span data-ttu-id="c02be-157"><dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-157"><dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-158">Esta propriedade é reservada pelo para uso futuro e não é implementada neste momento.</span><span class="sxs-lookup"><span data-stu-id="c02be-158">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="c02be-159">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-159">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_COMPRESSION"></span><span id="wia_ipa_compression"></span><dl> <span data-ttu-id="c02be-160"><dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-160"><dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-161">Contém o tipo de compactação atual usado.</span><span class="sxs-lookup"><span data-stu-id="c02be-161">Contains the current compression type used.</span></span> <span data-ttu-id="c02be-162">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-162">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-163">Um aplicativo lê essa propriedade para determinar o tipo de compactação da imagem ou define essa propriedade para definir a configuração de compactação.</span><span class="sxs-lookup"><span data-stu-id="c02be-163">An application reads this property to determine the image compression type or sets this property to configure the compression setting.</span></span></p>
<p><span data-ttu-id="c02be-164">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="c02be-164">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="c02be-165">A tabela a seguir tem as constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-165">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="c02be-166">O símbolo <strong>V</strong> indica que a constante tem suporte apenas no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="c02be-166">The <strong>V</strong> symbol indicates that the constant is supported only in Windows Vista and later.</span></span> <span data-ttu-id="c02be-167">(Só está disponível por meio da interface <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</span><span class="sxs-lookup"><span data-stu-id="c02be-167">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c02be-168">Tipo de Compactação</span><span class="sxs-lookup"><span data-stu-id="c02be-168">Compression Type</span></span></th>
<th><span data-ttu-id="c02be-169">Descrição</span><span class="sxs-lookup"><span data-stu-id="c02be-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c02be-170">WIA_COMPRESSION_NONE</span><span class="sxs-lookup"><span data-stu-id="c02be-170">WIA_COMPRESSION_NONE</span></span></td>
<td><span data-ttu-id="c02be-171">Sem compactação.</span><span class="sxs-lookup"><span data-stu-id="c02be-171">No compression.</span></span> <span data-ttu-id="c02be-172">Consulte a <strong>Observação</strong> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c02be-172">See <strong>Note</strong> for more information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-173">WIA_COMPRESSION_AUTO</span><span class="sxs-lookup"><span data-stu-id="c02be-173">WIA_COMPRESSION_AUTO</span></span></td>
<td><span data-ttu-id="c02be-174">Modo de compactação automática.</span><span class="sxs-lookup"><span data-stu-id="c02be-174">Automatic compression mode.</span></span> <span data-ttu-id="c02be-175">Consulte a <strong>Observação</strong> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c02be-175">See <strong>Note</strong> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-176">WIA_COMPRESSION_BI_RLE4</span><span class="sxs-lookup"><span data-stu-id="c02be-176">WIA_COMPRESSION_BI_RLE4</span></span></td>
<td><span data-ttu-id="c02be-177">Compactação RLE4</span><span class="sxs-lookup"><span data-stu-id="c02be-177">RLE4 compression</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-178">WIA_COMPRESSION_BI_RLE8</span><span class="sxs-lookup"><span data-stu-id="c02be-178">WIA_COMPRESSION_BI_RLE8</span></span></td>
<td><span data-ttu-id="c02be-179">Compactação RLE8</span><span class="sxs-lookup"><span data-stu-id="c02be-179">RLE8 compression</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-180">WIA_COMPRESSION_G3</span><span class="sxs-lookup"><span data-stu-id="c02be-180">WIA_COMPRESSION_G3</span></span></td>
<td><span data-ttu-id="c02be-181">Compactação do grupo 3</span><span class="sxs-lookup"><span data-stu-id="c02be-181">Group 3 compression</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-182">WIA_COMPRESSION_G4</span><span class="sxs-lookup"><span data-stu-id="c02be-182">WIA_COMPRESSION_G4</span></span></td>
<td><span data-ttu-id="c02be-183">Compactação do grupo 4</span><span class="sxs-lookup"><span data-stu-id="c02be-183">Group 4 compression</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-184">WIA_COMPRESSION_JPEG</span><span class="sxs-lookup"><span data-stu-id="c02be-184">WIA_COMPRESSION_JPEG</span></span></td>
<td><span data-ttu-id="c02be-185">Compactação JPEG.</span><span class="sxs-lookup"><span data-stu-id="c02be-185">JPEG compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-186">WIA_COMPRESSION_JBIG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="c02be-186">WIA_COMPRESSION_JBIG<strong>V</strong></span></span></td>
<td><span data-ttu-id="c02be-187">Compactação JBIG.</span><span class="sxs-lookup"><span data-stu-id="c02be-187">JBIG compression.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-188">WIA_COMPRESSION_JPEG2K<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="c02be-188">WIA_COMPRESSION_JPEG2K<strong>V</strong></span></span></td>
<td><span data-ttu-id="c02be-189">Compactação JPEG 2000.</span><span class="sxs-lookup"><span data-stu-id="c02be-189">JPEG 2000 compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-190">WIA_COMPRESSION_PNG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="c02be-190">WIA_COMPRESSION_PNG<strong>V</strong></span></span></td>
<td><span data-ttu-id="c02be-191">Compactação de PNG.</span><span class="sxs-lookup"><span data-stu-id="c02be-191">PNG compression.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
<p>[!Note]</p>
<p><span data-ttu-id="c02be-192">Quando essa propriedade é WIA_COMPRESSION_NONE e WIA_IPA_FORMAT é WiaImgFmt_PDFA ou WiaImgFmt_XPS; em seguida, WIA_COMPRESSION_NONE significa que o modo de compactação é indefinido e o verificador deve decidir em um modo.</span><span class="sxs-lookup"><span data-stu-id="c02be-192">When this property is WIA_COMPRESSION_NONE, and WIA_IPA_FORMAT is either WiaImgFmt_PDFA or WiaImgFmt_XPS; then WIA_COMPRESSION_NONE means that the compression mode is undefined and the scanner must decide on a mode.</span></span></p>
<p><span data-ttu-id="c02be-193">WIA_COMPRESSION_AUTO é um novo valor de propriedade definido para a propriedade WIA_IPA_COMPRESSION.</span><span class="sxs-lookup"><span data-stu-id="c02be-193">WIA_COMPRESSION_AUTO is a new property value defined for the WIA_IPA_COMPRESSION property.</span></span> <span data-ttu-id="c02be-194">Esse valor é válido para todos os itens de fonte de dados de imagem programável, incluindo o feed e o alimentador.</span><span class="sxs-lookup"><span data-stu-id="c02be-194">This value is valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="c02be-195">Quando esse valor é suportado pelo mini-driver WIA, o cliente do aplicativo WIA pode definir WIA_IPA_COMPRESSION para habilitar a detecção automática do modo de compactação no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c02be-195">When this value is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_COMPRESSION in order to enable automatic compression mode detection at the device.</span></span> <span data-ttu-id="c02be-196">WIA_COMPRESSION_AUTO pode trabalhar com e sem que a cor automática completa seja suportada ou habilitada (WIA_DATA_AUTO e WIA_DEPTH_AUTO).</span><span class="sxs-lookup"><span data-stu-id="c02be-196">WIA_COMPRESSION_AUTO can work with and without full auto-color being supported or enabled (WIA_DATA_AUTO and WIA_DEPTH_AUTO).</span></span></p>
<p><span data-ttu-id="c02be-197">WIA_COMPRESSION_AUTO é mais útil com os formatos de arquivo de transferência que dão suporte a vários tipos de dados e profundidades de bits, como WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="c02be-197">WIA_COMPRESSION_AUTO is most useful with transfer file formats that support multiple data types and bit depths, such as WiaImgFmt_RAW.</span></span> <span data-ttu-id="c02be-198">Para obter mais informações sobre os formatos de arquivo de transferência, consulte WIA_IPA_FORMAT nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="c02be-198">For more information about transfer file formats, see WIA_IPA_FORMAT in this table.</span></span></p>
<p><span data-ttu-id="c02be-199">Ele é Opitonal para o mini-driver WIA para suporte WIA_COMPRESSION_AUTO.</span><span class="sxs-lookup"><span data-stu-id="c02be-199">It is opitonal for the WIA mini-driver to suport WIA_COMPRESSION_AUTO.</span></span> <span data-ttu-id="c02be-200">Quando há suporte, o mini-driver WIA nunca deve defini-lo como o valor padrão para WIA_IPA_COMPRESSION; somente o aplicativo WIA pode definir esse valor.</span><span class="sxs-lookup"><span data-stu-id="c02be-200">When it is supported, the WIA mini-driver must never set it as the default value for WIA_IPA_COMPRESSION; only the WIA application can set this value.</span></span></p>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_DATATYPE"></span><span id="wia_ipa_datatype"></span><dl> <span data-ttu-id="c02be-201"><dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-201"><dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-202">Contém a configuração de tipo de dados atual para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c02be-202">Contains the current data type setting for the device.</span></span> <span data-ttu-id="c02be-203">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-203">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-204">Um aplicativo lê essa propriedade para determinar o tipo de dados da imagem.</span><span class="sxs-lookup"><span data-stu-id="c02be-204">An application reads this property to determine the data type of the image.</span></span> <span data-ttu-id="c02be-205">Um aplicativo grava essa propriedade para definir o tipo de dados atual da imagem a ser transferida.</span><span class="sxs-lookup"><span data-stu-id="c02be-205">An application writes this property to set the current data type of the image about to be transferred.</span></span></p>
<p><span data-ttu-id="c02be-206">Essa propriedade é necessária para todos os itens WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="c02be-206">This property is required for all WIA 2.0 items.</span></span> <span data-ttu-id="c02be-207">Ele deve ser leitura/gravação para todos os itens habilitados para aquisição do WIA 2,0 e somente leitura para itens de armazenamento WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="c02be-207">It must be Read/Write for all WIA 2.0 acquisition enabled items and Read Only for WIA 2.0 storage items.</span></span></p>
<p><span data-ttu-id="c02be-208">Tipo: <strong>VT_I4</strong>; Acesso para sistemas operacionais anteriores ao Windows Vista: essa propriedade é somente leitura para câmeras e leitura/gravação para scanners; Acesso ao Windows Vista e posterior: essa propriedade é somente leitura para itens WIA_CATEGORY_FOLDER e WIA_CATEGORY_FINISHED_FILE e leitura/gravação para todas as outras categorias de item do WIA 2,0; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="c02be-208">Type: <strong>VT_I4</strong>; Access for pre-Windows Vista operating systems: This property is Read Only for cameras and Read/Write for scanners; Access for Windows Vista and later: This property is Read Only for WIA_CATEGORY_FOLDER and WIA_CATEGORY_FINISHED_FILE items, and Read/Write for all other WIA 2.0 item categories; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="c02be-209">A tabela a seguir tem as seis constantes que são válidas com quando <strong>WIA_IPA_FORMAT</strong> não está definida como WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="c02be-209">The following table has the six constants that are valid with when <strong>WIA_IPA_FORMAT</strong> is not set to WiaImgFmt_RAW.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c02be-210">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="c02be-210">Data Type</span></span></th>
<th><span data-ttu-id="c02be-211">Descrição</span><span class="sxs-lookup"><span data-stu-id="c02be-211">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c02be-212">WIA_DATA_AUTO</span><span class="sxs-lookup"><span data-stu-id="c02be-212">WIA_DATA_AUTO</span></span></td>
<td><span data-ttu-id="c02be-213">Válido para todos os itens de fonte de dados de imagem programável, incluindo o feed e o alimentador.</span><span class="sxs-lookup"><span data-stu-id="c02be-213">Valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="c02be-214">Quando esse valor é suportado pelo mini-driver WIA, o cliente do aplicativo WIA pode definir WIA_IPA_DATATYPE para habilitar a detecção automática de cores no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c02be-214">When this value is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_DATATYPE in order to enable automatic color detection at the device.</span></span> <span data-ttu-id="c02be-215">Quando WIA_DATA_AUTO é definido, o mini-driver WIA deve atualizar WIA_IPA_DEPTH no mesmo item para WIA_DEPTH_AUTO (que deve ser um valor com suporte se o dispositivo oferecer suporte à cor automática).</span><span class="sxs-lookup"><span data-stu-id="c02be-215">When WIA_DATA_AUTO is set, the WIA mini-driver must update WIA_IPA_DEPTH on the same item to WIA_DEPTH_AUTO (which must be a supported value if the device supports automatic color).</span></span><br/> <span data-ttu-id="c02be-216">Esse é um valor opcional, mas é necessário quando WIA_DEPTH_AUTO tem suporte para WIA_IPA_DEPTH.</span><span class="sxs-lookup"><span data-stu-id="c02be-216">This is an optional value, but it is required when WIA_DEPTH_AUTO is supported for WIA_IPA_DEPTH.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-217">WIA_DATA_COLOR</span><span class="sxs-lookup"><span data-stu-id="c02be-217">WIA_DATA_COLOR</span></span></td>
<td><span data-ttu-id="c02be-218">Os dados de verificação são cores vermelha, verde, azul (RGB).</span><span class="sxs-lookup"><span data-stu-id="c02be-218">Scan data is red, green, blue (RGB) color.</span></span> <span data-ttu-id="c02be-219">O formato de cor completa é descrito usando as seguintes propriedades de WIA: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></span><span class="sxs-lookup"><span data-stu-id="c02be-219">The full color format is described using the following WIA properties: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></span></span><br/> <span data-ttu-id="c02be-220"><strong>WIA_IPA_BITS_PER_CHANNEL</strong></span><span class="sxs-lookup"><span data-stu-id="c02be-220"><strong>WIA_IPA_BITS_PER_CHANNEL</strong></span></span><br/> <span data-ttu-id="c02be-221"><strong>WIA_IPA_PLANAR</strong></span><span class="sxs-lookup"><span data-stu-id="c02be-221"><strong>WIA_IPA_PLANAR</strong></span></span><br/> <span data-ttu-id="c02be-222"><strong>WIA_IPA_PIXELS_PER_LINE</strong></span><span class="sxs-lookup"><span data-stu-id="c02be-222"><strong>WIA_IPA_PIXELS_PER_LINE</strong></span></span><br/> <span data-ttu-id="c02be-223"><strong>WIA_IPA_BYTES_PER_LINE</strong></span><span class="sxs-lookup"><span data-stu-id="c02be-223"><strong>WIA_IPA_BYTES_PER_LINE</strong></span></span><br/> <span data-ttu-id="c02be-224"><strong>WIA_IPA_NUMBER_OF_LINES</strong></span><span class="sxs-lookup"><span data-stu-id="c02be-224"><strong>WIA_IPA_NUMBER_OF_LINES</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-225">WIA_DATA_COLOR_DITHER</span><span class="sxs-lookup"><span data-stu-id="c02be-225">WIA_DATA_COLOR_DITHER</span></span></td>
<td><span data-ttu-id="c02be-226">O mesmo que WIA_DATA_COLOR, exceto que os dados são dificados usando o padrão de pontilhamento selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="c02be-226">Same as WIA_DATA_COLOR except that the data is dithered using the currently selected dither pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-227">WIA_DATA_COLOR_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="c02be-227">WIA_DATA_COLOR_THRESHOLD</span></span></td>
<td><span data-ttu-id="c02be-228">O mesmo que WIA_DATA_COLOR, exceto pelo fato de que o valor de limite é usado ao verificar os dados.</span><span class="sxs-lookup"><span data-stu-id="c02be-228">Same as WIA_DATA_COLOR except that the threshold value is used when scanning the data.</span></span> <span data-ttu-id="c02be-229">Valores de cor sobre o valor de <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> são convertidos em brilho completo; as cores sob esse valor são convertidas em preto.</span><span class="sxs-lookup"><span data-stu-id="c02be-229">Color values over the <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> value are converted to full brightness; colors under this value are converted to black.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-230">WIA_DATA_DITHER</span><span class="sxs-lookup"><span data-stu-id="c02be-230">WIA_DATA_DITHER</span></span></td>
<td><span data-ttu-id="c02be-231">Os dados de verificação são dificados usando o padrão de pontilhamento selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="c02be-231">Scan data is dithered using the currently selected dither pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-232">WIA_DATA_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="c02be-232">WIA_DATA_GRAYSCALE</span></span></td>
<td><span data-ttu-id="c02be-233">Os dados de verificação representam a intensidade.</span><span class="sxs-lookup"><span data-stu-id="c02be-233">Scan data represents intensity.</span></span> <span data-ttu-id="c02be-234">A paleta é uma escala de cinza fixa e igualmente espaçada com uma profundidade especificada por <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-234">The palette is a fixed, equally-spaced gray scale with a depth specified by <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-235">WIA_DATA_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="c02be-235">WIA_DATA_THRESHOLD</span></span></td>
<td><span data-ttu-id="c02be-236">O limite é um bit por pixel de dados em preto e branco.</span><span class="sxs-lookup"><span data-stu-id="c02be-236">The threshold is one bit per pixel of black-and-white data.</span></span> <span data-ttu-id="c02be-237">Os dados sobre o valor atual de <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> são convertidos em branco; os dados sob esse valor são convertidos em preto.</span><span class="sxs-lookup"><span data-stu-id="c02be-237">Data over the current value of <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> is converted to white; data under this value is converted to black.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="c02be-238">A propriedade <strong>WIA_IPA_DATATYPE</strong> também é usada para descrever o tipo de transferência de dados brutos a ser usado quando o aplicativo define WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="c02be-238">The <strong>WIA_IPA_DATATYPE</strong> property is also used to describe the type of RAW data transfer to be used when the application sets WiaImgFmt_RAW.</span></span> <span data-ttu-id="c02be-239">O driver deve definir a propriedade <strong>WIA_IPA_DATATYPE</strong> como uma lista de valores permitidos a partir dos quais o aplicativo pode escolher um.</span><span class="sxs-lookup"><span data-stu-id="c02be-239">The driver should set the <strong>WIA_IPA_DATATYPE</strong> property to a list of allowed values from which the application can pick one.</span></span></p>
<p><span data-ttu-id="c02be-240">Se o dispositivo puder ser definido como apenas um único valor, crie um tipo de <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> e coloque o valor válido nele.</span><span class="sxs-lookup"><span data-stu-id="c02be-240">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="c02be-241">Verifique a propriedade <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> para determinar a profundidade de bits.</span><span class="sxs-lookup"><span data-stu-id="c02be-241">Check the <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property to determine the bit depth.</span></span> <span data-ttu-id="c02be-242">Essa propriedade geralmente contém um único valor para câmeras.</span><span class="sxs-lookup"><span data-stu-id="c02be-242">This property usually contains a single value for cameras.</span></span></p>
<p><span data-ttu-id="c02be-243">A tabela a seguir lista as constantes que são válidas com <strong>WIA_IPA_DATATYPE</strong> quando <strong>WIA_IPA_FORMAT</strong> é definido como WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="c02be-243">The following table lists the constants that are valid with <strong>WIA_IPA_DATATYPE</strong> when <strong>WIA_IPA_FORMAT</strong> is set to WiaImgFmt_RAW.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c02be-244">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="c02be-244">Data Type</span></span></th>
<th><span data-ttu-id="c02be-245">Descrição</span><span class="sxs-lookup"><span data-stu-id="c02be-245">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c02be-246">WIA_DATA_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="c02be-246">WIA_DATA_GRAYSCALE</span></span></td>
<td><span data-ttu-id="c02be-247">Os dados de verificação representam a intensidade.</span><span class="sxs-lookup"><span data-stu-id="c02be-247">Scan data represents intensity.</span></span> <span data-ttu-id="c02be-248">A paleta é uma escala de cinza fixa, com espaçamento uniforme, com uma profundidade especificada pela propriedade <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> .</span><span class="sxs-lookup"><span data-stu-id="c02be-248">The palette is a fixed, equally spaced grayscale with a depth specified by the <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property.</span></span> <span data-ttu-id="c02be-249"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve ser definido como 1.</span><span class="sxs-lookup"><span data-stu-id="c02be-249"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-250">WIA_DATA_RAW_BGR</span><span class="sxs-lookup"><span data-stu-id="c02be-250">WIA_DATA_RAW_BGR</span></span></td>
<td><span data-ttu-id="c02be-251">Os dados de verificação estão no colorspace BGR (Blue-Green-Red).</span><span class="sxs-lookup"><span data-stu-id="c02be-251">Scan data is in the BGR (blue-green-red) colorspace.</span></span> <span data-ttu-id="c02be-252">O formato de cor completa é descrito usando o followingWIAproperties: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a></span><span class="sxs-lookup"><span data-stu-id="c02be-252">The full color format is described using the followingWIAproperties: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a></span></span><br/> <span data-ttu-id="c02be-253"><a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a></span><span class="sxs-lookup"><span data-stu-id="c02be-253"><a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a></span></span><br/> <span data-ttu-id="c02be-254"><a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-254"><a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a></span></span><br/> <span data-ttu-id="c02be-255"><a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-255"><a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a></span></span><br/> <span data-ttu-id="c02be-256"><a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a></span><span class="sxs-lookup"><span data-stu-id="c02be-256"><a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a></span></span><br/> <span data-ttu-id="c02be-257"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve ser definido como 3.</span><span class="sxs-lookup"><span data-stu-id="c02be-257"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-258">WIA_DATA_RAW_CMY</span><span class="sxs-lookup"><span data-stu-id="c02be-258">WIA_DATA_RAW_CMY</span></span></td>
<td><span data-ttu-id="c02be-259">Os dados de verificação estão no colorspace de ciano-magenta-amarelo (CMY).</span><span class="sxs-lookup"><span data-stu-id="c02be-259">Scan data is in the cyan-magenta-yellow (CMY) colorspace.</span></span> <span data-ttu-id="c02be-260">O formato de cor completa é descrito usando as mesmas propriedades de WIA que em WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="c02be-260">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="c02be-261"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve ser definido como 3.</span><span class="sxs-lookup"><span data-stu-id="c02be-261"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-262">WIA_DATA_RAW_CMYK</span><span class="sxs-lookup"><span data-stu-id="c02be-262">WIA_DATA_RAW_CMYK</span></span></td>
<td><span data-ttu-id="c02be-263">Os dados de verificação estão no colorspace ciano-magenta-amarelo-preto (CMYK).</span><span class="sxs-lookup"><span data-stu-id="c02be-263">Scan data is in the cyan-magenta-yellow-black (CMYK) colorspace.</span></span> <span data-ttu-id="c02be-264">O formato de cor completa é descrito usando as mesmas propriedades de WIA que em WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="c02be-264">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="c02be-265"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve ser definido como 4.</span><span class="sxs-lookup"><span data-stu-id="c02be-265"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-266">WIA_DATA_RAW_RGB</span><span class="sxs-lookup"><span data-stu-id="c02be-266">WIA_DATA_RAW_RGB</span></span></td>
<td><span data-ttu-id="c02be-267">Os dados de verificação estão no colorspace vermelho-verde-azul (RGB).</span><span class="sxs-lookup"><span data-stu-id="c02be-267">Scan data is in the red-green-blue (RGB) colorspace.</span></span> <span data-ttu-id="c02be-268">O formato de cor completa é descrito usando as mesmas propriedades de WIA que em WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="c02be-268">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="c02be-269"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve ser definido como 3.</span><span class="sxs-lookup"><span data-stu-id="c02be-269"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-270">WIA_DATA_RAW_YUV</span><span class="sxs-lookup"><span data-stu-id="c02be-270">WIA_DATA_RAW_YUV</span></span></td>
<td><span data-ttu-id="c02be-271">Os dados de verificação estão na colorspace de luminância-azul-diferença de cor vermelha (YUV).</span><span class="sxs-lookup"><span data-stu-id="c02be-271">Scan data is in the luminance-blue difference-red difference (YUV) colorspace.</span></span> <span data-ttu-id="c02be-272">O formato de cor completa é descrito usando as mesmas propriedades de WIA que em WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="c02be-272">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="c02be-273"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve ser definido como 3.</span><span class="sxs-lookup"><span data-stu-id="c02be-273"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-274">WIA_DATA_RAW_YUVK</span><span class="sxs-lookup"><span data-stu-id="c02be-274">WIA_DATA_RAW_YUVK</span></span></td>
<td><span data-ttu-id="c02be-275">Os dados de verificação estão na diferença de luminância-azul-diferença vermelha-preto (YUVK) colorspace.</span><span class="sxs-lookup"><span data-stu-id="c02be-275">Scan data is in the luminance-blue difference-red difference-black (YUVK) colorspace.</span></span> <span data-ttu-id="c02be-276">O formato de cor completa é descrito usando as mesmas propriedades de WIA que em WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="c02be-276">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="c02be-277"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve ser definido como 4.</span><span class="sxs-lookup"><span data-stu-id="c02be-277"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 4.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_DEPTH"></span><span id="wia_ipa_depth"></span><dl> <span data-ttu-id="c02be-278"><dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-278"><dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-279">WIA_IPA_DEPTH contém a configuração de profundidade de bits de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="c02be-279">WIA_IPA_DEPTH Contains the bit depth setting of an image.</span></span> <span data-ttu-id="c02be-280">O minidriver cria e mantém essa propriedade. Um aplicativo lê essa propriedade para determinar a configuração de profundidade de bits da imagem.</span><span class="sxs-lookup"><span data-stu-id="c02be-280">The minidriver creates and maintains this property.An application reads this property to determine the bit depth setting of the image.</span></span> <span data-ttu-id="c02be-281">O aplicativo também pode ser capaz de definir esse valor para a profundidade de bits desejada.</span><span class="sxs-lookup"><span data-stu-id="c02be-281">The application might also be able to set this value to the desired bit depth.</span></span></p>
<p><span data-ttu-id="c02be-282">Se o dispositivo puder ser definido como apenas um único valor, crie um <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> tipo e coloque o valor válido nele.</span><span class="sxs-lookup"><span data-stu-id="c02be-282">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span></p>
<p><span data-ttu-id="c02be-283">Essa propriedade é necessária para todos os itens WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="c02be-283">This property is required for all WIA 2.0 items.</span></span> <span data-ttu-id="c02be-284">Ele deve ser leitura/gravação para todos os itens habilitados para aquisição do WIA 2,0 e somente leitura para itens de armazenamento WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="c02be-284">It must be Read/Write for all WIA 2.0 acquisition enabled items and Read Only for WIA 2.0 storage items.</span></span></p>
<p><span data-ttu-id="c02be-285">Tipo: <strong>VT_I4</strong>; Acesso para sistemas operacionais anteriores ao Windows Vista: leitura/gravação; Acesso ao Windows Vista e posterior: essa propriedade é somente leitura para itens WIA_CATEGORY_FOLDER e WIA_CATEGORY_FINISHED_FILE e leitura/gravação para todas as outras categorias de item do WIA 2,0; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="c02be-285">Type: <strong>VT_I4</strong>; Access for pre-Windows Vista operating systems: Read/Write; Access for Windows Vista and later: This property is Read Only for WIA_CATEGORY_FOLDER and WIA_CATEGORY_FINISHED_FILE items, and Read/Write for all other WIA 2.0 item categories; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="c02be-286">WIA_DEPTH_AUTO é definido como 0 bits por pixel e é um novo valor de propriedade definido para o WIA_IPA_DEPTH.</span><span class="sxs-lookup"><span data-stu-id="c02be-286">WIA_DEPTH_AUTO is defined as 0 bits per pixel, and it is a new property value defined for the WIA_IPA_DEPTH.</span></span> <span data-ttu-id="c02be-287">Esse valor é válido para todos os itens de fonte de dados de imagem programável, incluindo o feed e o alimentador.</span><span class="sxs-lookup"><span data-stu-id="c02be-287">This value is valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="c02be-288">Quando WIA_DEPTH_AUTO é compatível com o mini-driver WIA, o cliente do aplicativo WIA pode definir WIA_IPA_DEPTH para esse valor, para habilitar a detecção automática de cores no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c02be-288">When WIA_DEPTH_AUTO is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_DEPTH to this value, to enable automatic color detection at the device.</span></span> <span data-ttu-id="c02be-289">Quando WIA_DEPTH_AUTO é definido, o mini-driver WIA deve atualizar WIA_IPA_DATATYPE no mesmo item para WIA_DATA_AUTO (que deve ser um valor com suporte, se o dispositivo oferecer suporte à cor automática).</span><span class="sxs-lookup"><span data-stu-id="c02be-289">When WIA_DEPTH_AUTO is set, the WIA mini-driver must update WIA_IPA_DATATYPE on the same item to WIA_DATA_AUTO (which must be a supported value, if the device supports automatic color).</span></span></p>
<p><span data-ttu-id="c02be-290">WIA_DEPTH_AUTO é um valor opcional, mas se torna necessário quando WIA_DATA_AUTO tem suporte para WIA_IPA_DATATYPE.</span><span class="sxs-lookup"><span data-stu-id="c02be-290">WIA_DEPTH_AUTO is an optional value, but it becomes required when WIA_DATA_AUTO is supported for WIA_IPA_DATATYPE.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FILENAME_EXTENSION"></span><span id="wia_ipa_filename_extension"></span><dl> <span data-ttu-id="c02be-291"><dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-291"><dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-292">Contém a extensão de nome de arquivo para um formato de arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="c02be-292">Contains the file name extension for a particular file format.</span></span> <span data-ttu-id="c02be-293">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-293">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-294">Opcional para todos os itens WIA 2,0 habilitados para transferência.</span><span class="sxs-lookup"><span data-stu-id="c02be-294">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="c02be-295">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-295">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="c02be-296">O driver atualiza essa propriedade para refletir o valor atual da propriedade <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> .</span><span class="sxs-lookup"><span data-stu-id="c02be-296">The driver updates this property to reflect the current value of the <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> property.</span></span></p>
<p><span data-ttu-id="c02be-297">Por exemplo, se <strong>WIA_IPA_FORMAT</strong> for WiaImgFmt_JPEG, <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> deverá ser <strong>jpg</strong>.</span><span class="sxs-lookup"><span data-stu-id="c02be-297">For example, if <strong>WIA_IPA_FORMAT</strong> is WiaImgFmt_JPEG, then <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> should be <strong>jpg</strong>.</span></span> <span data-ttu-id="c02be-298">Se <strong>WIA_IPA_FORMAT</strong> for WiaImgFmt_BMP, WIA_IPA_FILENAME_EXTENSION deverá ser BMP.</span><span class="sxs-lookup"><span data-stu-id="c02be-298">If <strong>WIA_IPA_FORMAT</strong> is WiaImgFmt_BMP, then WIA_IPA_FILENAME_EXTENSION should be BMP.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="c02be-299">A extensão de nome de arquivo não inclui o ponto.</span><span class="sxs-lookup"><span data-stu-id="c02be-299">The file name extension does not include the dot.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="c02be-300">Essa propriedade é recomendada para drivers que dão suporte a formatos padrão e são necessários para drivers que implementam formatos definidos como personalizados.</span><span class="sxs-lookup"><span data-stu-id="c02be-300">This property is recommended for drivers that support standard formats and is required for drivers that implement custom-defined formats.</span></span> <span data-ttu-id="c02be-301">Ele informa o aplicativo da extensão de nome de arquivo correta a ser usada durante a transferência de arquivos formatados de forma privada.</span><span class="sxs-lookup"><span data-stu-id="c02be-301">It informs the application of the correct file name extension to use during the transfer of privately formatted files.</span></span> <span data-ttu-id="c02be-302">Por exemplo, se a a. Datum Corporation criou um driver WIA que transferiu um arquivo em um novo formato, a empresa poderia especificar uma extensão de &quot; ADC &quot; .</span><span class="sxs-lookup"><span data-stu-id="c02be-302">For example, if the A. Datum Corporation created a WIA driver that transferred a file in a new format, the company could specify an extension of &quot;adc&quot;.</span></span> <span data-ttu-id="c02be-303">Isso permite que os aplicativos transfiram dados nesse formato em um arquivo e criem um nome de arquivo como <em>MyFile. ADC</em>, que é útil para outras pessoas que entendem a nova extensão.</span><span class="sxs-lookup"><span data-stu-id="c02be-303">This allows applications to transfer data in that format to a file and to create a file name such as <em>myfile.adc</em>,which is useful to others who understand the new extension.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_FORMAT"></span><span id="wia_ipa_format"></span><dl> <span data-ttu-id="c02be-304"><dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-304"><dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-305">Contém o formato atual da imagem a ser transferida.</span><span class="sxs-lookup"><span data-stu-id="c02be-305">Contains the current format of the image about to be transferred.</span></span></p>
<p><span data-ttu-id="c02be-306">Um aplicativo lê essa propriedade para determinar o formato da imagem que ela está prestes a receber.</span><span class="sxs-lookup"><span data-stu-id="c02be-306">An application reads this property to determine the format of the image that it is about to receive.</span></span> <span data-ttu-id="c02be-307">Um aplicativo grava essa propriedade para definir o formato.</span><span class="sxs-lookup"><span data-stu-id="c02be-307">An application writes this property to set the format.</span></span> <span data-ttu-id="c02be-308">Essa propriedade depende da propriedade <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> .</span><span class="sxs-lookup"><span data-stu-id="c02be-308">This property depends on the <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> property.</span></span> <span data-ttu-id="c02be-309">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-309">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-310">Se o dispositivo puder ser definido como apenas um único valor, crie um tipo de <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> e coloque o valor válido nele.</span><span class="sxs-lookup"><span data-stu-id="c02be-310">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="c02be-311">Tipo: <strong>CLSID</strong>, acesso: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="c02be-311">Type: <strong>CLSID</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="c02be-312">A tabela a seguir lista as constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-312">The following table lists the constants that are valid with this property.</span></span> <span data-ttu-id="c02be-313">O asterisco \* indica que a constante não tem suporte no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c02be-313">The asterisk \* indicates that the constant is not supported in Windows Vista.</span></span> <span data-ttu-id="c02be-314">(Só está disponível por meio da interface <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .) O asterisco duplo \* \* indica que a constante não tem suporte no Windows Server 2003 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c02be-314">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.) The double asterisk \*\* indicates that the constant is not supported in either Windows Server 2003 or Windows Vista.</span></span> <span data-ttu-id="c02be-315">O símbolo <strong>V</strong> indica que a constante tem suporte apenas no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="c02be-315">The <strong>V</strong> symbol indicates that the constant is supported only in Windows Vista and later.</span></span> <span data-ttu-id="c02be-316">(Só está disponível por meio da interface <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</span><span class="sxs-lookup"><span data-stu-id="c02be-316">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c02be-317">Formatar</span><span class="sxs-lookup"><span data-stu-id="c02be-317">Format</span></span></th>
<th><span data-ttu-id="c02be-318">Descrição</span><span class="sxs-lookup"><span data-stu-id="c02be-318">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c02be-319">WiaAudFmt_AIFF</span><span class="sxs-lookup"><span data-stu-id="c02be-319">WiaAudFmt_AIFF</span></span></td>
<td><span data-ttu-id="c02be-320">Formato de áudio AIFF</span><span class="sxs-lookup"><span data-stu-id="c02be-320">AIFF audio format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-321">WiaAudFmt_MP3</span><span class="sxs-lookup"><span data-stu-id="c02be-321">WiaAudFmt_MP3</span></span></td>
<td><span data-ttu-id="c02be-322">Formato de áudio MP3</span><span class="sxs-lookup"><span data-stu-id="c02be-322">MP3 audio format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-323">WiaAudFmt_WAV</span><span class="sxs-lookup"><span data-stu-id="c02be-323">WiaAudFmt_WAV</span></span></td>
<td><span data-ttu-id="c02be-324">Formato de áudio WAV</span><span class="sxs-lookup"><span data-stu-id="c02be-324">WAV audio format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-325">WiaAudFmt_WMA</span><span class="sxs-lookup"><span data-stu-id="c02be-325">WiaAudFmt_WMA</span></span></td>
<td><span data-ttu-id="c02be-326">Formato de áudio WMA</span><span class="sxs-lookup"><span data-stu-id="c02be-326">WMA audio format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-327">WiaImgFmt_ASF \* \*</span><span class="sxs-lookup"><span data-stu-id="c02be-327">WiaImgFmt_ASF\*\*</span></span></td>
<td><span data-ttu-id="c02be-328">Formato de vídeo ASF</span><span class="sxs-lookup"><span data-stu-id="c02be-328">ASF video format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-329">WiaImgFmt_AVI \* \*</span><span class="sxs-lookup"><span data-stu-id="c02be-329">WiaImgFmt_AVI\*\*</span></span></td>
<td><span data-ttu-id="c02be-330">Formato de vídeo AVI</span><span class="sxs-lookup"><span data-stu-id="c02be-330">AVI video format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-331">WiaImgFmt_BMP</span><span class="sxs-lookup"><span data-stu-id="c02be-331">WiaImgFmt_BMP</span></span></td>
<td><span data-ttu-id="c02be-332">Bitmap do Windows com um arquivo de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c02be-332">Windows bitmap with a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-333">WiaImgFmt_CIFF \*</span><span class="sxs-lookup"><span data-stu-id="c02be-333">WiaImgFmt_CIFF\*</span></span></td>
<td><span data-ttu-id="c02be-334">Formato de arquivo de imagem da câmera</span><span class="sxs-lookup"><span data-stu-id="c02be-334">Camera Image File format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-335">WiaImgFmt_DPOF</span><span class="sxs-lookup"><span data-stu-id="c02be-335">WiaImgFmt_DPOF</span></span></td>
<td><span data-ttu-id="c02be-336">Formato de impressão DPOF</span><span class="sxs-lookup"><span data-stu-id="c02be-336">DPOF printing format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-337">WiaImgFmt_EMF</span><span class="sxs-lookup"><span data-stu-id="c02be-337">WiaImgFmt_EMF</span></span></td>
<td><span data-ttu-id="c02be-338">Metarquivo estendido do Windows</span><span class="sxs-lookup"><span data-stu-id="c02be-338">Extended Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-339">WiaImgFmt_EXEC</span><span class="sxs-lookup"><span data-stu-id="c02be-339">WiaImgFmt_EXEC</span></span></td>
<td><span data-ttu-id="c02be-340">Arquivo executável</span><span class="sxs-lookup"><span data-stu-id="c02be-340">Executable file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-341">WiaImgFmt_EXIF</span><span class="sxs-lookup"><span data-stu-id="c02be-341">WiaImgFmt_EXIF</span></span></td>
<td><span data-ttu-id="c02be-342">Formato de arquivo intercambiável</span><span class="sxs-lookup"><span data-stu-id="c02be-342">Exchangeable File Format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-343">WiaImgFmt_FLASHPIX</span><span class="sxs-lookup"><span data-stu-id="c02be-343">WiaImgFmt_FLASHPIX</span></span></td>
<td><span data-ttu-id="c02be-344">Formato FlashPix</span><span class="sxs-lookup"><span data-stu-id="c02be-344">FlashPix format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-345">WiaImgFmt_GIF</span><span class="sxs-lookup"><span data-stu-id="c02be-345">WiaImgFmt_GIF</span></span></td>
<td><span data-ttu-id="c02be-346">Formato de imagem GIF</span><span class="sxs-lookup"><span data-stu-id="c02be-346">GIF image format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-347">WiaImgFmt_HTML</span><span class="sxs-lookup"><span data-stu-id="c02be-347">WiaImgFmt_HTML</span></span></td>
<td><span data-ttu-id="c02be-348">Formato HTML</span><span class="sxs-lookup"><span data-stu-id="c02be-348">HTML format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-349">WiaImgFmt_ICO</span><span class="sxs-lookup"><span data-stu-id="c02be-349">WiaImgFmt_ICO</span></span></td>
<td><span data-ttu-id="c02be-350">Formato do arquivo de ícone do Windows</span><span class="sxs-lookup"><span data-stu-id="c02be-350">Windows icon file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-351">WiaImgFmt_JBIG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="c02be-351">WiaImgFmt_JBIG<strong>V</strong></span></span></td>
<td><span data-ttu-id="c02be-352">O formato de grupo de especialistas em imagem de nível de BI (JBIG).</span><span class="sxs-lookup"><span data-stu-id="c02be-352">The Joint Bi-level Image Experts Group (JBIG) format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-353">WiaImgFmt_JPEG</span><span class="sxs-lookup"><span data-stu-id="c02be-353">WiaImgFmt_JPEG</span></span></td>
<td><span data-ttu-id="c02be-354">Formato compactado JPEG</span><span class="sxs-lookup"><span data-stu-id="c02be-354">JPEG compressed format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-355">WiaImgFmt_JPEG2K</span><span class="sxs-lookup"><span data-stu-id="c02be-355">WiaImgFmt_JPEG2K</span></span></td>
<td><span data-ttu-id="c02be-356">Formato compactado JPEG 2000</span><span class="sxs-lookup"><span data-stu-id="c02be-356">JPEG 2000 compressed format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-357">WiaImgFmt_JPEG2KX</span><span class="sxs-lookup"><span data-stu-id="c02be-357">WiaImgFmt_JPEG2KX</span></span></td>
<td><span data-ttu-id="c02be-358">Formato compactado JPEG 2000</span><span class="sxs-lookup"><span data-stu-id="c02be-358">JPEG 2000 compressed format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-359">WiaImgFmt_MEMORYBMP</span><span class="sxs-lookup"><span data-stu-id="c02be-359">WiaImgFmt_MEMORYBMP</span></span></td>
<td><span data-ttu-id="c02be-360">Bitmap do Windows sem um arquivo de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c02be-360">Windows bitmap without a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-361">WiaImgFmt_PDFA<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="c02be-361">WiaImgFmt_PDFA<strong>V</strong></span></span></td>
<td><span data-ttu-id="c02be-362">O formato PDF/A (ISO/CD 19005-1).</span><span class="sxs-lookup"><span data-stu-id="c02be-362">The PDF/A (ISO/CD 19005-1) format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-363">WiaImgFmt_MPG \* \*</span><span class="sxs-lookup"><span data-stu-id="c02be-363">WiaImgFmt_MPG\*\*</span></span></td>
<td><span data-ttu-id="c02be-364">Formato de vídeo MPEG</span><span class="sxs-lookup"><span data-stu-id="c02be-364">MPEG video format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-365">WiaImgFmt_PHOTOCD</span><span class="sxs-lookup"><span data-stu-id="c02be-365">WiaImgFmt_PHOTOCD</span></span></td>
<td><span data-ttu-id="c02be-366">Formato de arquivo da Eastman Kodak</span><span class="sxs-lookup"><span data-stu-id="c02be-366">Eastman Kodak file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-367">WiaImgFmt_PICT</span><span class="sxs-lookup"><span data-stu-id="c02be-367">WiaImgFmt_PICT</span></span></td>
<td><span data-ttu-id="c02be-368">Formato de arquivo da Apple</span><span class="sxs-lookup"><span data-stu-id="c02be-368">Apple file format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-369">WiaImgFmt_PNG</span><span class="sxs-lookup"><span data-stu-id="c02be-369">WiaImgFmt_PNG</span></span></td>
<td><span data-ttu-id="c02be-370">Formato W3C PNG</span><span class="sxs-lookup"><span data-stu-id="c02be-370">W3C PNG format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-371">WiaImgFmt_RAW</span><span class="sxs-lookup"><span data-stu-id="c02be-371">WiaImgFmt_RAW</span></span></td>
<td><span data-ttu-id="c02be-372">Formato bruto somente para transferências de dados</span><span class="sxs-lookup"><span data-stu-id="c02be-372">Raw format for data transfers only</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-373">WiaImgFmt_RAWRGB</span><span class="sxs-lookup"><span data-stu-id="c02be-373">WiaImgFmt_RAWRGB</span></span></td>
<td><span data-ttu-id="c02be-374">Formato RGB bruto</span><span class="sxs-lookup"><span data-stu-id="c02be-374">Raw RGB format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-375">WiaImgFmt_RTF</span><span class="sxs-lookup"><span data-stu-id="c02be-375">WiaImgFmt_RTF</span></span></td>
<td><span data-ttu-id="c02be-376">Formato de arquivo de Rich Text</span><span class="sxs-lookup"><span data-stu-id="c02be-376">Rich Text File format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-377">WiaImgFmt_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="c02be-377">WiaImgFmt_SCRIPT</span></span></td>
<td><span data-ttu-id="c02be-378">Arquivo de script</span><span class="sxs-lookup"><span data-stu-id="c02be-378">Script file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-379">WiaImgFmt_TIFF</span><span class="sxs-lookup"><span data-stu-id="c02be-379">WiaImgFmt_TIFF</span></span></td>
<td><span data-ttu-id="c02be-380">Formato TIFF</span><span class="sxs-lookup"><span data-stu-id="c02be-380">Tag Image File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-381">WiaImgFmt_TXT</span><span class="sxs-lookup"><span data-stu-id="c02be-381">WiaImgFmt_TXT</span></span></td>
<td><span data-ttu-id="c02be-382">Arquivo de texto</span><span class="sxs-lookup"><span data-stu-id="c02be-382">Text file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-383">WiaImgFmt_UNICODE16</span><span class="sxs-lookup"><span data-stu-id="c02be-383">WiaImgFmt_UNICODE16</span></span></td>
<td><span data-ttu-id="c02be-384">Codificação UNICODE de 16 bits</span><span class="sxs-lookup"><span data-stu-id="c02be-384">UNICODE 16-bit encoding</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-385">WiaImgFmt_WMF</span><span class="sxs-lookup"><span data-stu-id="c02be-385">WiaImgFmt_WMF</span></span></td>
<td><span data-ttu-id="c02be-386">Metarquivo do Windows</span><span class="sxs-lookup"><span data-stu-id="c02be-386">Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-387">WiaImgFmt_XML</span><span class="sxs-lookup"><span data-stu-id="c02be-387">WiaImgFmt_XML</span></span></td>
<td><span data-ttu-id="c02be-388">Arquivo XML</span><span class="sxs-lookup"><span data-stu-id="c02be-388">XML file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-389">WiaImgFmt_XPS<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="c02be-389">WiaImgFmt_XPS<strong>V</strong></span></span></td>
<td><span data-ttu-id="c02be-390">Formato de pacote XPS</span><span class="sxs-lookup"><span data-stu-id="c02be-390">XPS Package format</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="c02be-391">Quando essa propriedade é WiaImgFmt_PDFA ou WiaImgFmt_XPS e WIA_IPA_COMPRESSION é WIA_COMPRESSION_NONE; em seguida, o último valor significa que o modo de compactação é indefinido e o verificador deve decidir em um modo.</span><span class="sxs-lookup"><span data-stu-id="c02be-391">When this property is either WiaImgFmt_PDFA or WiaImgFmt_XPS, and WIA_IPA_COMPRESSION is WIA_COMPRESSION_NONE; then the latter value means that the compression mode is undefined and the scanner must decide on a mode.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FULL_ITEM_NAME"></span><span id="wia_ipa_full_item_name"></span><dl> <span data-ttu-id="c02be-392"><dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-392"><dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-393">Contém o nome completo do item (o nome do item junto com as informações de caminho).</span><span class="sxs-lookup"><span data-stu-id="c02be-393">Contains the full item name (the item name together with path information).</span></span> <span data-ttu-id="c02be-394">O nome completo do item é o mesmo que o parâmetro <em>bstrFullItemName</em> da função utilitário do serviço <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> .</span><span class="sxs-lookup"><span data-stu-id="c02be-394">The full item name is the same as the <em>bstrFullItemName</em> parameter of the <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> service utility function.</span></span> <span data-ttu-id="c02be-395">Um aplicativo lê essa propriedade para determinar qual item ele está usando no momento e onde esse item está localizado na árvore de itens.</span><span class="sxs-lookup"><span data-stu-id="c02be-395">An application reads this property to determine which item it is currently using and where that item is located in the item tree.</span></span> <span data-ttu-id="c02be-396">Cada item deve ter um nome exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c02be-396">Each item should have a unique name.</span></span> <span data-ttu-id="c02be-397">Normalmente, os aplicativos usam o nome completo do item para pesquisar itens na árvore de itens.</span><span class="sxs-lookup"><span data-stu-id="c02be-397">Applications commonly use the full item name to search for items in the item tree.</span></span> <span data-ttu-id="c02be-398">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-398">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-399">Necessário para todos os itens do WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="c02be-399">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="c02be-400">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-400">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_GAMMA_CURVES"></span><span id="wia_ipa_gamma_curves"></span><dl> <span data-ttu-id="c02be-401"><dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-401"><dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-402">Esta propriedade é reservada para uso futuro e não é implementada neste momento.</span><span class="sxs-lookup"><span data-stu-id="c02be-402">This property is reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="c02be-403">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-403">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ICM_PROFILE_NAME"></span><span id="wia_ipa_icm_profile_name"></span><dl> <span data-ttu-id="c02be-404"><dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-404"><dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-405">Contém o nome do perfil ICM que é necessário para decodificar corretamente a imagem.</span><span class="sxs-lookup"><span data-stu-id="c02be-405">Contains the ICM profile name that is needed to properly decode the image.</span></span> <span data-ttu-id="c02be-406">Um aplicativo lê essa propriedade para determinar o perfil ICM a ser usado ao processar a imagem.</span><span class="sxs-lookup"><span data-stu-id="c02be-406">An application reads this property to determine the ICM profile to use when processing the image.</span></span> <span data-ttu-id="c02be-407">O serviço WIA cria e mantém essa propriedade com base na entrada ICMProfiles no arquivo de instalação do driver.</span><span class="sxs-lookup"><span data-stu-id="c02be-407">The WIA service creates and maintains this property based on the ICMProfiles entry in the driver installation file.</span></span></p>
<p><span data-ttu-id="c02be-408">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-408">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_CATEGORY"></span><span id="wia_ipa_item_category"></span><dl> <span data-ttu-id="c02be-409"><dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-409"><dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-410">Com suporte apenas no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="c02be-410">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="c02be-411">Os itens WIA 2,0 são agrupados em categorias que definem como um <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> deve ser tratado ou usado.</span><span class="sxs-lookup"><span data-stu-id="c02be-411">WIA 2.0 items are grouped into categories that define how a <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> is to be treated or used.</span></span> <span data-ttu-id="c02be-412">Por exemplo, se o item representa um alimentador, o aplicativo deve esperar que ele contenha as propriedades necessárias do alimentador de documentos e opere como um alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="c02be-412">For example, If the item represents a feeder, then the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span> <span data-ttu-id="c02be-413">Se o item representa um arquivo concluído, um aplicativo WIA 2,0 deve tratá-lo dessa forma, supondo que os dados sejam estáticos e localizados no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c02be-413">If the item represents a finished file, then a WIA 2.0 application should treat it that way, assuming that the data is static and located on the device.</span></span> <span data-ttu-id="c02be-414">(As regras para cada item serão definidas em seus documentos de especificação individuais.)</span><span class="sxs-lookup"><span data-stu-id="c02be-414">(The rules for each item will be defined in their individual specification documents.)</span></span></p>
<p><span data-ttu-id="c02be-415">Necessário para todos os itens do WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="c02be-415">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="c02be-416">Tipo: <strong>VT_CLSID</strong>, Access: somente leitura, valores válidos: <a href="-wia-wia2-itemcategoryguids.md"><strong>GUIDs de categoria de item</strong></a></span><span class="sxs-lookup"><span data-stu-id="c02be-416">Type: <strong>VT_CLSID</strong>, Access: Read Only, Valid values: <a href="-wia-wia2-itemcategoryguids.md"><strong>Item Category GUIDs</strong></a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_FLAGS"></span><span id="wia_ipa_item_flags"></span><dl> <span data-ttu-id="c02be-417"><dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-417"><dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-418">Contém os sinalizadores descritivos para um item WIA.</span><span class="sxs-lookup"><span data-stu-id="c02be-418">Contains the descriptive flags for a WIA item.</span></span> <span data-ttu-id="c02be-419">Os sinalizadores de item são os mesmos do parâmetro <em>lObjectFlags</em> da função utilitário de serviço <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> .</span><span class="sxs-lookup"><span data-stu-id="c02be-419">The item flags are the same as those in the <em>lObjectFlags</em> parameter of the <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> service utility function.</span></span> <span data-ttu-id="c02be-420">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-420">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-421">Um aplicativo lê essa propriedade para determinar os valores de sinalizador descritivos do item.</span><span class="sxs-lookup"><span data-stu-id="c02be-421">An application reads this property to determine the item's descriptive flag values.</span></span></p>
<p><span data-ttu-id="c02be-422">Tipo: acesso de <strong>VT_I4</strong> : somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-422">Type: <strong>VT_I4</strong> Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="c02be-423">A tabela a seguir tem os sinalizadores que são válidos com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-423">The following table has the flags that are valid with this property.</span></span> <span data-ttu-id="c02be-424">Um asterisco \* indica que o sinalizador não tem suporte no Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c02be-424">An asterisk \* indicates that the flag is not supported in Windows Vista or later.</span></span> <span data-ttu-id="c02be-425">(Só está disponível por meio da interface <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .) Um asterisco duplo \* \* indica que o sinalizador não tem suporte no Windows Server 2003 ou no Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c02be-425">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.) An double asterisk \*\* indicates that the flag is not supported in either Windows Server 2003 or Windows Vista or later.</span></span> <span data-ttu-id="c02be-426">O símbolo <strong>V</strong> indica que o sinalizador tem suporte apenas no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="c02be-426">The <strong>V</strong> symbol indicates that the flag is supported only in Windows Vista and later.</span></span> <span data-ttu-id="c02be-427">(Só está disponível por meio da interface <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</span><span class="sxs-lookup"><span data-stu-id="c02be-427">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c02be-428">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="c02be-428">Flag</span></span></th>
<th><span data-ttu-id="c02be-429">Definição</span><span class="sxs-lookup"><span data-stu-id="c02be-429">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c02be-430">WiaItemTypeAnalyze\*</span><span class="sxs-lookup"><span data-stu-id="c02be-430">WiaItemTypeAnalyze\*</span></span></td>
<td><span data-ttu-id="c02be-431">Este item dá suporte ao método <strong>IWiaItem:: AnalyzeItem</strong> (descrito na documentação do Platform SDK).</span><span class="sxs-lookup"><span data-stu-id="c02be-431">This item supports the <strong>IWiaItem::AnalyzeItem</strong> method (described in the Platform SDK documentation).</span></span> <span data-ttu-id="c02be-432">Esse item também dá suporte à geração automática de itens filho.</span><span class="sxs-lookup"><span data-stu-id="c02be-432">This item also supports automatic child item generation.</span></span> <span data-ttu-id="c02be-433">Esse recurso é útil para a detecção de região ou a decomposição de página.</span><span class="sxs-lookup"><span data-stu-id="c02be-433">This capability is useful for region detection or page decomposition.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-434">WiaItemTypeAudio</span><span class="sxs-lookup"><span data-stu-id="c02be-434">WiaItemTypeAudio</span></span></td>
<td><span data-ttu-id="c02be-435">Este item dá suporte a áudio.</span><span class="sxs-lookup"><span data-stu-id="c02be-435">This item supports audio.</span></span> <span data-ttu-id="c02be-436">Esse sinalizador é válido somente para itens que também têm o sinalizador <strong>WiaItemTypeFile</strong> definido.</span><span class="sxs-lookup"><span data-stu-id="c02be-436">This flag is valid only for items that also have the <strong>WiaItemTypeFile</strong> flag set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-437">WiaItemTypeBurst\*</span><span class="sxs-lookup"><span data-stu-id="c02be-437">WiaItemTypeBurst\*</span></span></td>
<td><span data-ttu-id="c02be-438">Somente para pastas.</span><span class="sxs-lookup"><span data-stu-id="c02be-438">For folders only.</span></span> <span data-ttu-id="c02be-439">Esse sinalizador indica que as imagens nessa pasta foram executadas em uma sequência de tempo contínua.</span><span class="sxs-lookup"><span data-stu-id="c02be-439">This flag indicates that the images in this folder were taken in a continuous time sequence.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-440">WiaItemTypeDeleted</span><span class="sxs-lookup"><span data-stu-id="c02be-440">WiaItemTypeDeleted</span></span></td>
<td><span data-ttu-id="c02be-441">Este item está marcado para exclusão, este item foi excluído, este item não existe ou o conteúdo deste item é inválido.</span><span class="sxs-lookup"><span data-stu-id="c02be-441">This item is marked for deletion, this item has been deleted, this item does not exist, or the contents of this item are invalid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-442">WiaItemTypeDocument<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="c02be-442">WiaItemTypeDocument<strong>V</strong></span></span></td>
<td><span data-ttu-id="c02be-443">Este item é um arquivo de documento em um dos formatos de documento que a propriedade <strong>WIA_IPA_FORMAT</strong> contém.</span><span class="sxs-lookup"><span data-stu-id="c02be-443">This item is a document file in one of the document formats that the <strong>WIA_IPA_FORMAT</strong> property contains.</span></span> <span data-ttu-id="c02be-444">(Esses formatos incluem aqueles para arquivos que não são de imagem, como. txt,. htm e arquivos. doc.)</span><span class="sxs-lookup"><span data-stu-id="c02be-444">(These formats include those for nonimage files, such as .txt, .htm, and .doc files.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-445">WiaItemTypeDevice</span><span class="sxs-lookup"><span data-stu-id="c02be-445">WiaItemTypeDevice</span></span></td>
<td><span data-ttu-id="c02be-446">Este item representa um dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="c02be-446">This item represents a connected device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-447">WiaItemTypeDisconnected</span><span class="sxs-lookup"><span data-stu-id="c02be-447">WiaItemTypeDisconnected</span></span></td>
<td><span data-ttu-id="c02be-448">Este item representa um dispositivo desconectado.</span><span class="sxs-lookup"><span data-stu-id="c02be-448">This item represents a disconnected device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-449">WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="c02be-449">WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="c02be-450">O item dá suporte a transferências de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c02be-450">The item supports file transfers.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-451">WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="c02be-451">WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="c02be-452">O item é uma pasta.</span><span class="sxs-lookup"><span data-stu-id="c02be-452">The item is a folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-453">WiaItemTypeFree</span><span class="sxs-lookup"><span data-stu-id="c02be-453">WiaItemTypeFree</span></span></td>
<td><span data-ttu-id="c02be-454">O item não foi inicializado ou foi excluído.</span><span class="sxs-lookup"><span data-stu-id="c02be-454">The item is uninitialized or has been deleted.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-455">WiaItemTypeGenerated</span><span class="sxs-lookup"><span data-stu-id="c02be-455">WiaItemTypeGenerated</span></span></td>
<td><span data-ttu-id="c02be-456">Este item foi gerado por um aplicativo ou pelo driver.</span><span class="sxs-lookup"><span data-stu-id="c02be-456">This item has been generated by an application or by the driver.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-457">WiaItemTypeHasAttachments\*</span><span class="sxs-lookup"><span data-stu-id="c02be-457">WiaItemTypeHasAttachments\*</span></span></td>
<td><span data-ttu-id="c02be-458">Este item dá suporte a anexos e atualmente contém anexos.</span><span class="sxs-lookup"><span data-stu-id="c02be-458">This item supports attachments and currently contains attachments.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-459">WiaItemTypeHPanorama\*</span><span class="sxs-lookup"><span data-stu-id="c02be-459">WiaItemTypeHPanorama\*</span></span></td>
<td><span data-ttu-id="c02be-460">Este item representa uma imagem panorâmica horizontal.</span><span class="sxs-lookup"><span data-stu-id="c02be-460">This item represents a horizontal panoramic image.</span></span> <span data-ttu-id="c02be-461">Esse sinalizador é válido somente para itens que também têm o sinalizador <strong>WiaItemTypeFolder</strong> definido.</span><span class="sxs-lookup"><span data-stu-id="c02be-461">This flag is valid only for items that also have the <strong>WiaItemTypeFolder</strong> flag set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-462">WiaItemTypeImage</span><span class="sxs-lookup"><span data-stu-id="c02be-462">WiaItemTypeImage</span></span></td>
<td><span data-ttu-id="c02be-463">O item é um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="c02be-463">The item is an image file.</span></span> <span data-ttu-id="c02be-464">Esse sinalizador é válido somente para itens que também têm o sinalizador <strong>WiaItemTypeFile</strong> definido.</span><span class="sxs-lookup"><span data-stu-id="c02be-464">This flag is valid only for items that also have the <strong>WiaItemTypeFile</strong> flag set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-465">WiaItemTypeProgrammableDataSource<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="c02be-465">WiaItemTypeProgrammableDataSource<strong>V</strong></span></span></td>
<td><span data-ttu-id="c02be-466">O item é uma fonte de dados programável e segue um conjunto de regras de configuração predefinidas, que se baseiam em <strong>WIA_IPA_ITEM_CATEGORY</strong>.</span><span class="sxs-lookup"><span data-stu-id="c02be-466">The item is a programmable data source and follows a set of predefined configuration rules, which are based on <strong>WIA_IPA_ITEM_CATEGORY</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-467">WiaItemTypeRoot<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="c02be-467">WiaItemTypeRoot<strong>V</strong></span></span></td>
<td><span data-ttu-id="c02be-468">Este item é o item raiz, que é o pai de todos os itens de recurso aos quais o dispositivo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="c02be-468">This item is the root item, which is the parent to all the feature items that the device supports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-469">WiaItemTypeStorage</span><span class="sxs-lookup"><span data-stu-id="c02be-469">WiaItemTypeStorage</span></span></td>
<td><span data-ttu-id="c02be-470">Esse sinalizador indica armazenamento adicional para itens de pastas.</span><span class="sxs-lookup"><span data-stu-id="c02be-470">This flag indicates additional storage for folders items.</span></span> <span data-ttu-id="c02be-471">Os drivers WIA especificam seus itens em termos de imagens e pastas.</span><span class="sxs-lookup"><span data-stu-id="c02be-471">WIA drivers specify their items in terms of images and folders.</span></span> <span data-ttu-id="c02be-472">Não existem propriedades WIA que descrevam as características de um item de armazenamento (como espaço de armazenamento restante, velocidade de gravação ou tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="c02be-472">No WIA properties exist that describe the characteristics of a storage item (such as remaining storage space, write speed, or type of media.</span></span> <span data-ttu-id="c02be-473">As propriedades específicas do fornecedor que expõem essas informações podem ser adicionadas.</span><span class="sxs-lookup"><span data-stu-id="c02be-473">Vendor-specific properties that expose this information can be added.</span></span> <span data-ttu-id="c02be-474">Essas propriedades são acessíveis somente para aplicativos ou extensões que são gravadas para reconhecê-las.</span><span class="sxs-lookup"><span data-stu-id="c02be-474">These properties are accessible only to applications or extensions that are written to recognize them.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-475">WiaItemTypeTransfer</span><span class="sxs-lookup"><span data-stu-id="c02be-475">WiaItemTypeTransfer</span></span></td>
<td><span data-ttu-id="c02be-476">Este item pode ser usado para transferir dados.</span><span class="sxs-lookup"><span data-stu-id="c02be-476">This item can be used to transfer data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-477">WiaItemTypeTwainCapabilityPassThrough</span><span class="sxs-lookup"><span data-stu-id="c02be-477">WiaItemTypeTwainCapabilityPassThrough</span></span></td>
<td><span data-ttu-id="c02be-478">Esse tipo indica que o dispositivo WIA é capaz de receber dados de funcionalidade de TWAIN da camada de compatibilidade TWAIN.</span><span class="sxs-lookup"><span data-stu-id="c02be-478">This type indicates that the WIA device is able to receive TWAIN capability data from the TWAIN compatibility layer.</span></span> <span data-ttu-id="c02be-479">Se esse tipo for definido, qualquer recurso de TWAIN que não seja compreendido pela camada de compatibilidade TWAIN será passada para o driver theWIA.</span><span class="sxs-lookup"><span data-stu-id="c02be-479">If this type is set, any TWAIN capability that is not understood by the TWAIN compatibility layer will be passed to theWIA driver.</span></span> <span data-ttu-id="c02be-480">Isso é válido somente para o item raiz.</span><span class="sxs-lookup"><span data-stu-id="c02be-480">This is valid only for the root item.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-481">WiaItemTypeVideo\*\*</span><span class="sxs-lookup"><span data-stu-id="c02be-481">WiaItemTypeVideo\*\*</span></span></td>
<td><span data-ttu-id="c02be-482">Este item dá suporte ao vídeo de streaming.</span><span class="sxs-lookup"><span data-stu-id="c02be-482">This item supports streaming video.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-483">WiaItemTypeVPanorama\*</span><span class="sxs-lookup"><span data-stu-id="c02be-483">WiaItemTypeVPanorama\*</span></span></td>
<td><span data-ttu-id="c02be-484">Este item representa uma imagem panorâmica vertical.</span><span class="sxs-lookup"><span data-stu-id="c02be-484">This item represents a vertical panoramic image.</span></span> <span data-ttu-id="c02be-485">Esse sinalizador é válido somente para itens que também têm o sinalizador <strong>WiaItemTypeFolder</strong> definido.</span><span class="sxs-lookup"><span data-stu-id="c02be-485">This flag is valid only for items that also have the <strong>WiaItemTypeFolder</strong> flag set.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="c02be-486">Alguns desses sinalizadores são obrigatórios ou opcionais para itens WIA 2,0, de acordo com a categoria do item, conforme mostrado nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="c02be-486">Some of these flags are required or optional for WIA 2.0 items, according to the category of the item, as shown in this table.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c02be-487">Categoria do item</span><span class="sxs-lookup"><span data-stu-id="c02be-487">Category of Item</span></span></th>
<th><span data-ttu-id="c02be-488">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c02be-488">Required</span></span></th>
<th><span data-ttu-id="c02be-489">Opcional</span><span class="sxs-lookup"><span data-stu-id="c02be-489">Optional</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c02be-490">WIA_CATEGORY_ROOT</span><span class="sxs-lookup"><span data-stu-id="c02be-490">WIA_CATEGORY_ROOT</span></span></td>
<td><span data-ttu-id="c02be-491">WiaItemTypeRoot WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="c02be-491">WiaItemTypeRoot WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="c02be-492">WiaItemTypeDevice WiaItemTypeDisconnected</span><span class="sxs-lookup"><span data-stu-id="c02be-492">WiaItemTypeDevice WiaItemTypeDisconnected</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-493">WIA_CATEGORY_FLATBED</span><span class="sxs-lookup"><span data-stu-id="c02be-493">WIA_CATEGORY_FLATBED</span></span></td>
<td><span data-ttu-id="c02be-494">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="c02be-494">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="c02be-495">WiaItemTypeFolder (se houver suporte para vários itens de regiões de verificação, esse sinalizador será opcional somente para o item de raiz WIA_CATEGORY_FLATBED.)</span><span class="sxs-lookup"><span data-stu-id="c02be-495">WiaItemTypeFolder (If multiple scan regions items are supported, this flag is optional only for the WIA_CATEGORY_FLATBED root item.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-496">WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</span><span class="sxs-lookup"><span data-stu-id="c02be-496">WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</span></span></td>
<td><span data-ttu-id="c02be-497">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="c02be-497">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="c02be-498">WiaItemTypeFolder (se WIA_CATEGORY_FEEDER_FRONT e WIA_CATEGORY_FEEDER_BACK itens estiverem presentes, esse sinalizador será opcional somente para o item de raiz WIA_CATEGORY_FEEDER.)</span><span class="sxs-lookup"><span data-stu-id="c02be-498">WiaItemTypeFolder (If WIA_CATEGORY_FEEDER_FRONT and WIA_CATEGORY_FEEDER_BACK items are present, then this flag is optional only for the WIA_CATEGORY_FEEDER root item.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-499">WIA_CATEGORY_FILM (raiz)</span><span class="sxs-lookup"><span data-stu-id="c02be-499">WIA_CATEGORY_FILM (root)</span></span></td>
<td><span data-ttu-id="c02be-500">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="c02be-500">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="c02be-501">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c02be-501">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-502">WIA_CATEGORY_FILM (filhos)</span><span class="sxs-lookup"><span data-stu-id="c02be-502">WIA_CATEGORY_FILM (children)</span></span></td>
<td><span data-ttu-id="c02be-503">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="c02be-503">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="c02be-504">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c02be-504">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-505">WIA_CATEGORY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="c02be-505">WIA_CATEGORY_FOLDER</span></span></td>
<td><span data-ttu-id="c02be-506">WiaItemTypeStorage WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="c02be-506">WiaItemTypeStorage WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="c02be-507">WiaItemTypeDeleted</span><span class="sxs-lookup"><span data-stu-id="c02be-507">WiaItemTypeDeleted</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-508">WIA_CATEGORY_FINISHED_FILE</span><span class="sxs-lookup"><span data-stu-id="c02be-508">WIA_CATEGORY_FINISHED_FILE</span></span></td>
<td><span data-ttu-id="c02be-509">WiaItemTypeFile WiaItemTypeTransfer</span><span class="sxs-lookup"><span data-stu-id="c02be-509">WiaItemTypeFile WiaItemTypeTransfer</span></span></td>
<td><span data-ttu-id="c02be-510">WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</span><span class="sxs-lookup"><span data-stu-id="c02be-510">WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_NAME"></span><span id="wia_ipa_item_name"></span><dl> <span data-ttu-id="c02be-511"><dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-511"><dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-512">Contém o nome do item.</span><span class="sxs-lookup"><span data-stu-id="c02be-512">Contains the item name.</span></span> <span data-ttu-id="c02be-513">Um aplicativo lê essa propriedade para determinar qual item ele está usando no momento.</span><span class="sxs-lookup"><span data-stu-id="c02be-513">An application reads this property to determine which item it is currently using.</span></span> <span data-ttu-id="c02be-514">Cada item tem um nome exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c02be-514">Each item has a unique name.</span></span> <span data-ttu-id="c02be-515">O serviço WIA cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-515">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-516">Necessário para todos os itens do WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="c02be-516">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="c02be-517">Tipo: <strong>VT_BSTR</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-517">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_SIZE"></span><span id="wia_ipa_item_size"></span><dl> <span data-ttu-id="c02be-518"><dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-518"><dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-519">Contém o tamanho atual, em bytes, dos dados associados ao item.</span><span class="sxs-lookup"><span data-stu-id="c02be-519">Contains the current size, in bytes, of the data that is associated with the item.</span></span> <span data-ttu-id="c02be-520">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-520">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-521">Contains é o tamanho total dos dados que estão sendo transferidos.</span><span class="sxs-lookup"><span data-stu-id="c02be-521">Contains is the total size of the data being transferred.</span></span> <span data-ttu-id="c02be-522">Se esse valor for zero, significa que o minidriver não tem informações sobre o tamanho exato dos dados.</span><span class="sxs-lookup"><span data-stu-id="c02be-522">If this value is zero, it means that the minidriver has no information about the exact size of the data.</span></span> <span data-ttu-id="c02be-523">(Isso é comum para dados compactados.) Um aplicativo lê esse valor para determinar o tamanho da aquisição antes que ela ocorra.</span><span class="sxs-lookup"><span data-stu-id="c02be-523">(This is common for compressed data.) An application reads this value to determine the size of the acquisition before it takes place.</span></span> <span data-ttu-id="c02be-524">O serviço WIA lê essa propriedade para auxiliar na alocação de memória para transferências de dados.</span><span class="sxs-lookup"><span data-stu-id="c02be-524">The WIA service reads this property to assist in allocating memory for data transfers.</span></span> <span data-ttu-id="c02be-525">Para obter mais informações, consulte <a href="https://msdn.microsoft.com/library/ms792198.aspx">transferindo dados para um aplicativo WIA</a> se a propriedade for definida como zero e TYMED estiver configurado para uma transferência de arquivo, o serviço WIA não alocará memória para o minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="c02be-525">For further information, see <a href="https://msdn.microsoft.com/library/ms792198.aspx">Transferring Data to a WIA Application</a> if the property is set to zero and TYMED is configured for a file transfer, the WIA service does not allocate any memory for the WIA minidriver.</span></span></p>
<p><span data-ttu-id="c02be-526">Necessário para todos os itens WIA 2,0 habilitados para transferência.</span><span class="sxs-lookup"><span data-stu-id="c02be-526">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="c02be-527">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-527">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_TIME"></span><span id="wia_ipa_item_time"></span><dl> <span data-ttu-id="c02be-528"><dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-528"><dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-529">Contém a hora em que a imagem foi capturada originalmente.</span><span class="sxs-lookup"><span data-stu-id="c02be-529">Contains the time that the image was originally captured.</span></span> <span data-ttu-id="c02be-530">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-530">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="c02be-531">Essa propriedade deve ser relatada como um vetor de oito valores de <strong>palavra</strong> na forma de uma estrutura SYSTEMTIME (descrita na documentação do Platform SDK).</span><span class="sxs-lookup"><span data-stu-id="c02be-531">This property should be reported as a vector of eight <strong>WORD</strong> values in the form of a SYSTEMTIME structure (described in the Platform SDK documentation).</span></span></p>
<p><span data-ttu-id="c02be-532">Opcional para todos os itens WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="c02be-532">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="c02be-533">Tipo: <strong>VT_UI2</strong>  |  acesso a<strong>VT_VECTOR</strong> : leitura/gravação ou somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-533">Type: <strong>VT_UI2</strong> | <strong>VT_VECTOR</strong> Access: Read/Write or Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <span data-ttu-id="c02be-534"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-534"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-535">Com suporte apenas no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="c02be-535">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="c02be-536">Especifica quantos itens são armazenados no item de WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="c02be-536">Specifies how many items are stored in the WIA_CATEGORY_FOLDER item.</span></span></p>
<p><span data-ttu-id="c02be-537">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-537">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_MIN_BUFFER_SIZE"></span><span id="wia_ipa_min_buffer_size"></span><dl> <span data-ttu-id="c02be-538"><dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-538"><dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-539">Especifica o tamanho mínimo do buffer que é usado em transferências de dados.</span><span class="sxs-lookup"><span data-stu-id="c02be-539">Specifies the minimum buffer size that is used in data transfers.</span></span> <span data-ttu-id="c02be-540">Se a transferência de dados for executada por meio de um mecanismo de retorno de chamada, o valor da propriedade poderá ser tão pequeno quanto 64 KB.</span><span class="sxs-lookup"><span data-stu-id="c02be-540">If the data transfer is performed through a callback mechanism, the property value can be as small as 64KB.</span></span> <span data-ttu-id="c02be-541">No entanto, se a transferência for para o arquivo, o valor da propriedade será o número de bytes necessários para transferir uma página de dados de cada vez.</span><span class="sxs-lookup"><span data-stu-id="c02be-541">However, if the transfer is to file, the property value is the number of bytes that are needed to transfer one page of data at a time.</span></span> <span data-ttu-id="c02be-542">O minidriver cria e mantém essa propriedade WIA.</span><span class="sxs-lookup"><span data-stu-id="c02be-542">The minidriver creates and maintains this WIA property.</span></span></p>
<p><span data-ttu-id="c02be-543">Opcional para todos os itens WIA 2,0 habilitados para transferência.</span><span class="sxs-lookup"><span data-stu-id="c02be-543">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="c02be-544">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-544">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_NUMBER_OF_LINES"></span><span id="wia_ipa_number_of_lines"></span><dl> <span data-ttu-id="c02be-545"><dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-545"><dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-546">Contém o número de linhas contidas na imagem (a altura vertical da imagem em pixels).</span><span class="sxs-lookup"><span data-stu-id="c02be-546">Contains the number of lines contained in the image (the vertical height of the image in pixels).</span></span> <span data-ttu-id="c02be-547">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-547">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-548">Opcional para todos os itens WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="c02be-548">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="c02be-549">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-549">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PIXELS_PER_LINE"></span><span id="wia_ipa_pixels_per_line"></span><dl> <span data-ttu-id="c02be-550"><dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-550"><dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-551">Contém o número de pixels em cada linha da imagem (a largura da imagem em pixels).</span><span class="sxs-lookup"><span data-stu-id="c02be-551">Contains the number of pixels in each line of the image (the width of the image in pixels).</span></span> <span data-ttu-id="c02be-552">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-552">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-553">Opcional para todos os itens WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="c02be-553">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="c02be-554">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-554">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PLANAR"></span><span id="wia_ipa_planar"></span><dl> <span data-ttu-id="c02be-555"><dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-555"><dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-556">Não há suporte para essa propriedade no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="c02be-556">This property is not supported in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="c02be-557">Contém opções de empacotamento de dados de imagem.</span><span class="sxs-lookup"><span data-stu-id="c02be-557">Contains image data packing options.</span></span> <span data-ttu-id="c02be-558">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-558">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-559">Um aplicativo lê essa propriedade para determinar as opções de empacotamento de imagem ou define as opções de empacotamento da imagem atual.</span><span class="sxs-lookup"><span data-stu-id="c02be-559">An application reads this property to determine the image packing options or sets the current image packing options.</span></span></p>
<p><span data-ttu-id="c02be-560">Tipo: <strong>VT_I4</strong>; Acesso: leitura/gravação; Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span><span class="sxs-lookup"><span data-stu-id="c02be-560">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span></span> <span data-ttu-id="c02be-561">Se o dispositivo puder ser definido como apenas um único valor, crie um WIA_PROP_LIST tipo e coloque o valor válido nele.</span><span class="sxs-lookup"><span data-stu-id="c02be-561">If the device can be set to only a single value, create a WIA_PROP_LIST type and place the valid value in it.</span></span></p>
<p><span data-ttu-id="c02be-562">A tabela a seguir tem as duas constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-562">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c02be-563">Valor</span><span class="sxs-lookup"><span data-stu-id="c02be-563">Value</span></span></th>
<th><span data-ttu-id="c02be-564">Definição</span><span class="sxs-lookup"><span data-stu-id="c02be-564">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c02be-565">WIA_PACKED_PIXEL</span><span class="sxs-lookup"><span data-stu-id="c02be-565">WIA_PACKED_PIXEL</span></span></td>
<td><span data-ttu-id="c02be-566">Os dados da imagem estão no formato de pixel embalado.</span><span class="sxs-lookup"><span data-stu-id="c02be-566">Image data is in packed-pixel format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-567">WIA_PLANAR</span><span class="sxs-lookup"><span data-stu-id="c02be-567">WIA_PLANAR</span></span></td>
<td><span data-ttu-id="c02be-568">Os dados da imagem estão no formato planar.</span><span class="sxs-lookup"><span data-stu-id="c02be-568">Image data is in planar format.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PREFERRED_FORMAT"></span><span id="wia_ipa_preferred_format"></span><dl> <span data-ttu-id="c02be-569"><dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-569"><dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-570">Contém o formato preferencial para as imagens que esse minidriver transfere.</span><span class="sxs-lookup"><span data-stu-id="c02be-570">Contains the preferred format for images that this minidriver transfers.</span></span> <span data-ttu-id="c02be-571">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-571">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-572">Necessário para todos os itens WIA 2,0 habilitados para transferência.</span><span class="sxs-lookup"><span data-stu-id="c02be-572">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="c02be-573">Tipo: <strong>CLSID</strong>, acesso: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-573">Type: <strong>CLSID</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PROP_STREAM_COMPAT_ID"></span><span id="wia_ipa_prop_stream_compat_id"></span><dl> <span data-ttu-id="c02be-574"><dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-574"><dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-575">Especifica um CLSID que representa um conjunto de valores de propriedade de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c02be-575">Specifies a CLSID that represents a set of device property values.</span></span> <span data-ttu-id="c02be-576">Se um driver de dispositivo implementar esse recurso, os aplicativos usarão essa propriedade para determinar se o dispositivo dá suporte a um conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="c02be-576">If a device driver implements this feature, applications use this property to determine if the device supports a set of values.</span></span></p>
<p><span data-ttu-id="c02be-577">Tipo: <strong>CLSID</strong>, acesso: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="c02be-577">Type: <strong>CLSID</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="c02be-578">A tabela a seguir tem as 12 constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-578">The following table has the 12 constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c02be-579">Valor</span><span class="sxs-lookup"><span data-stu-id="c02be-579">Value</span></span></th>
<th><span data-ttu-id="c02be-580">Definição</span><span class="sxs-lookup"><span data-stu-id="c02be-580">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c02be-581">WiaImgFmt_BMP</span><span class="sxs-lookup"><span data-stu-id="c02be-581">WiaImgFmt_BMP</span></span></td>
<td><span data-ttu-id="c02be-582">Bitmap MicrosoftWindows com um arquivo de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c02be-582">MicrosoftWindows bitmap with a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-583">WiaImgFmt_EMF</span><span class="sxs-lookup"><span data-stu-id="c02be-583">WiaImgFmt_EMF</span></span></td>
<td><span data-ttu-id="c02be-584">Metarquivo estendido do Windows</span><span class="sxs-lookup"><span data-stu-id="c02be-584">Extended Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-585">WiaImgFmt_EXIF</span><span class="sxs-lookup"><span data-stu-id="c02be-585">WiaImgFmt_EXIF</span></span></td>
<td><span data-ttu-id="c02be-586">Formato de arquivo intercambiável</span><span class="sxs-lookup"><span data-stu-id="c02be-586">Exchangeable File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-587">WiaImgFmt_FLASHPIX</span><span class="sxs-lookup"><span data-stu-id="c02be-587">WiaImgFmt_FLASHPIX</span></span></td>
<td><span data-ttu-id="c02be-588">Formato FlashPix</span><span class="sxs-lookup"><span data-stu-id="c02be-588">FlashPix format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-589">WiaImgFmt_GIF</span><span class="sxs-lookup"><span data-stu-id="c02be-589">WiaImgFmt_GIF</span></span></td>
<td><span data-ttu-id="c02be-590">Formato de imagem GIF</span><span class="sxs-lookup"><span data-stu-id="c02be-590">GIF image format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-591">WiaImgFmt_ICO</span><span class="sxs-lookup"><span data-stu-id="c02be-591">WiaImgFmt_ICO</span></span></td>
<td><span data-ttu-id="c02be-592">Formato do arquivo de ícone do Windows</span><span class="sxs-lookup"><span data-stu-id="c02be-592">Windows icon file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-593">WiaImgFmt_JPEG</span><span class="sxs-lookup"><span data-stu-id="c02be-593">WiaImgFmt_JPEG</span></span></td>
<td><span data-ttu-id="c02be-594">Formato compactado JPEG</span><span class="sxs-lookup"><span data-stu-id="c02be-594">JPEG compressed format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-595">WiaImgFmt_PHOTOCD</span><span class="sxs-lookup"><span data-stu-id="c02be-595">WiaImgFmt_PHOTOCD</span></span></td>
<td><span data-ttu-id="c02be-596">Formato de arquivo da Eastman Kodak</span><span class="sxs-lookup"><span data-stu-id="c02be-596">Eastman Kodak file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-597">WiaImgFmt_PNG</span><span class="sxs-lookup"><span data-stu-id="c02be-597">WiaImgFmt_PNG</span></span></td>
<td><span data-ttu-id="c02be-598">Formato W3C PNG</span><span class="sxs-lookup"><span data-stu-id="c02be-598">W3C PNG format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-599">WiaImgFmt_MEMORYBMP</span><span class="sxs-lookup"><span data-stu-id="c02be-599">WiaImgFmt_MEMORYBMP</span></span></td>
<td><span data-ttu-id="c02be-600">Bitmap do Windows sem um arquivo de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c02be-600">Windows bitmap without a header file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-601">WiaImgFmt_TIFF</span><span class="sxs-lookup"><span data-stu-id="c02be-601">WiaImgFmt_TIFF</span></span></td>
<td><span data-ttu-id="c02be-602">Formato TIFF</span><span class="sxs-lookup"><span data-stu-id="c02be-602">Tag Image File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-603">WiaImgFmt_WMF</span><span class="sxs-lookup"><span data-stu-id="c02be-603">WiaImgFmt_WMF</span></span></td>
<td><span data-ttu-id="c02be-604">Metarquivo do Windows</span><span class="sxs-lookup"><span data-stu-id="c02be-604">Windows metafile</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_RAW_BITS_PER_CHANNEL"></span><span id="wia_ipa_raw_bits_per_channel"></span><dl> <span data-ttu-id="c02be-605"><dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-605"><dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-606">Com suporte apenas no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="c02be-606">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="c02be-607">Contém o número de bits em cada canal.</span><span class="sxs-lookup"><span data-stu-id="c02be-607">Contains the number of bits in each channel.</span></span> <span data-ttu-id="c02be-608">Essa propriedade deve ser relatada como um vetor de até muitos valores de BYTE que há canais, em que o primeiro BYTE corresponde ao número de bits no primeiro canal, o segundo byte para o número de bits no segundo canal e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c02be-608">This property should be reported as a vector of as many BYTE values as there are channels, where the first BYTE corresponds to the number of bits in the first channel, the second byte to the number of bits in the second channel and so on.</span></span> <span data-ttu-id="c02be-609">Precisa haver tantas entradas quantos forem os canais de acordo com WIA_IPA_CHANNELS_PER_PIXEL.</span><span class="sxs-lookup"><span data-stu-id="c02be-609">There need to be as many entries as there are channels according to WIA_IPA_CHANNELS_PER_PIXEL.</span></span> <span data-ttu-id="c02be-610">O driver define essa propriedade quando o aplicativo alterna para WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="c02be-610">The driver sets that property when the application switches to WiaImgFmt_RAW.</span></span> <span data-ttu-id="c02be-611">Para os subtipos conhecidos, há tantas entradas, conforme listadas na tabela em WIA_IPA_RAW_SUBTYPE.</span><span class="sxs-lookup"><span data-stu-id="c02be-611">For the well-known subtypes, there are as many entries as listed in the table under WIA_IPA_RAW_SUBTYPE.</span></span></p>
<p><span data-ttu-id="c02be-612">Tipo: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, acesso: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-612">Type: <strong>VT_UI1</strong>|<strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_REGION_TYPE"></span><span id="wia_ipa_region_type"></span><dl> <span data-ttu-id="c02be-613"><dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-613"><dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-614">Esta propriedade é reservada pelo para uso futuro e não é implementada neste momento.</span><span class="sxs-lookup"><span data-stu-id="c02be-614">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="c02be-615">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-615">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_SUPPRESS_PROPERTY_PAGE"></span><span id="wia_ipa_suppress_property_page"></span><dl> <span data-ttu-id="c02be-616"><dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-616"><dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-617">Especifica se as páginas de propriedades gerais devem ser suprimidas para os itens no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c02be-617">Specifies whether to suppress the general property pages for items on the device.</span></span></p>
<p><span data-ttu-id="c02be-618">Essa propriedade está disponível no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="c02be-618">This property is available on Windows XP and later.</span></span></p>
<p><span data-ttu-id="c02be-619">Tipo: <strong>VT_I4</strong>, Access: somente leitura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-619">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="c02be-620">A tabela a seguir tem as constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-620">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="c02be-621">O asterisco \* indica que a constante não é válida com o Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="c02be-621">The asterisk \* indicates that the constant is not valid with Windows Vista and later.</span></span> <span data-ttu-id="c02be-622">(Só está disponível por meio da interface <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .)</span><span class="sxs-lookup"><span data-stu-id="c02be-622">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c02be-623">Constante</span><span class="sxs-lookup"><span data-stu-id="c02be-623">Constant</span></span></th>
<th><span data-ttu-id="c02be-624">Descrição</span><span class="sxs-lookup"><span data-stu-id="c02be-624">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c02be-625">WIA_PROPPAGE_CAMERA_ITEM_GENERAL \*</span><span class="sxs-lookup"><span data-stu-id="c02be-625">WIA_PROPPAGE_CAMERA_ITEM_GENERAL\*</span></span></td>
<td><span data-ttu-id="c02be-626">Suprimir a página de propriedades de item geral de uma câmera.</span><span class="sxs-lookup"><span data-stu-id="c02be-626">Suppress the general item property page for a camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-627">WIA_PROPPAGE_SCANNER_ITEM_GENERAL</span><span class="sxs-lookup"><span data-stu-id="c02be-627">WIA_PROPPAGE_SCANNER_ITEM_GENERAL</span></span></td>
<td><span data-ttu-id="c02be-628">Suprimir a página de propriedades de item geral para um scanner.</span><span class="sxs-lookup"><span data-stu-id="c02be-628">Suppress the general item property page for a scanner.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_TYMED"></span><span id="wia_ipa_tymed"></span><dl> <span data-ttu-id="c02be-629"><dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-629"><dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-630">Essa propriedade contém a configuração do método de transferência.</span><span class="sxs-lookup"><span data-stu-id="c02be-630">This property contains the transfer method setting.</span></span> <span data-ttu-id="c02be-631">O minidriver cria e mantém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-631">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="c02be-632">Um aplicativo lê essa propriedade para determinar o método de transferência de dados de minidriver.</span><span class="sxs-lookup"><span data-stu-id="c02be-632">An application reads this property to determine the minidriver's method of data transfer.</span></span></p>
<p><span data-ttu-id="c02be-633">Necessário para todos os itens WIA 2,0 habilitados para transferência.</span><span class="sxs-lookup"><span data-stu-id="c02be-633">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="c02be-634">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="c02be-634">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="c02be-635">A tabela a seguir tem as constantes que são válidas com essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c02be-635">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="c02be-636">O asterisco \* indica constantes que não são válidas com o Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="c02be-636">The asterisk \* indicates constants that are not valid with Windows Vista and later.</span></span> <span data-ttu-id="c02be-637">(Eles só estão disponíveis por meio da interface <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .)</span><span class="sxs-lookup"><span data-stu-id="c02be-637">(They are only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c02be-638">Tipo de Transferência</span><span class="sxs-lookup"><span data-stu-id="c02be-638">Transfer Type</span></span></th>
<th><span data-ttu-id="c02be-639">Descrição</span><span class="sxs-lookup"><span data-stu-id="c02be-639">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c02be-640">TYMED_CALLBACK \*</span><span class="sxs-lookup"><span data-stu-id="c02be-640">TYMED_CALLBACK\*</span></span></td>
<td><span data-ttu-id="c02be-641">Transferir uma imagem para a memória, em bandas.</span><span class="sxs-lookup"><span data-stu-id="c02be-641">Transfer an image to memory, in bands.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-642">TYMED_MULTIPAGE_CALLBACK \*</span><span class="sxs-lookup"><span data-stu-id="c02be-642">TYMED_MULTIPAGE_CALLBACK\*</span></span></td>
<td><span data-ttu-id="c02be-643">Transfira várias imagens para a memória, em bandas.</span><span class="sxs-lookup"><span data-stu-id="c02be-643">Transfer multiple images to memory, in bands.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c02be-644">TYMED_FILE</span><span class="sxs-lookup"><span data-stu-id="c02be-644">TYMED_FILE</span></span></td>
<td><span data-ttu-id="c02be-645">Transferir uma imagem para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c02be-645">Transfer an image to a file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c02be-646">TYMED_MULTIPAGE_FILE</span><span class="sxs-lookup"><span data-stu-id="c02be-646">TYMED_MULTIPAGE_FILE</span></span></td>
<td><span data-ttu-id="c02be-647">Transferir uma imagem para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c02be-647">Transfer an image to a file.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <span data-ttu-id="c02be-648"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </span><span class="sxs-lookup"><span data-stu-id="c02be-648"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c02be-649">Com suporte apenas no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="c02be-649">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="c02be-650">Especifica o número de bytes a serem carregados para um item.</span><span class="sxs-lookup"><span data-stu-id="c02be-650">Specifies the number of bytes to upload for an item.</span></span></p>
<p><span data-ttu-id="c02be-651">Tipo: <strong>VT_I4</strong>, Access: leitura/gravação, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c02be-651">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="c02be-652">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c02be-652">Requirements</span></span>



| <span data-ttu-id="c02be-653">Requisito</span><span class="sxs-lookup"><span data-stu-id="c02be-653">Requirement</span></span> | <span data-ttu-id="c02be-654">Valor</span><span class="sxs-lookup"><span data-stu-id="c02be-654">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c02be-655">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c02be-655">Minimum supported client</span></span><br/> | <span data-ttu-id="c02be-656">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c02be-656">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c02be-657">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c02be-657">Minimum supported server</span></span><br/> | <span data-ttu-id="c02be-658">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c02be-658">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c02be-659">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c02be-659">Header</span></span><br/>                   | <dl> <span data-ttu-id="c02be-660"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="c02be-660"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




