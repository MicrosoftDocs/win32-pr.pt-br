---
description: Habilita o Microsoft Media Foundation fluxo de bytes HTTP para usar identificadores de URL (também chamados de Urlmon).
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: Propriedade MFPKEY_HTTP_ByteStream_Enable_Urlmon (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1858f34a5f719caba1a48f049b95f2031b400240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778455"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a><span data-ttu-id="36cae-103">MFPKEY \_ http \_ bytes \_ habilitar a \_ Propriedade Urlmon</span><span class="sxs-lookup"><span data-stu-id="36cae-103">MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon property</span></span>

<span data-ttu-id="36cae-104">Habilita o Microsoft Media Foundation fluxo de bytes HTTP para usar identificadores de URL (também chamados de *Urlmon*).</span><span class="sxs-lookup"><span data-stu-id="36cae-104">Enables the Microsoft Media Foundation HTTP byte stream to use URL monikers (also called *Urlmon*).</span></span>



<span data-ttu-id="36cae-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="36cae-105">Data type</span></span>

<span data-ttu-id="36cae-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="36cae-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="36cae-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="36cae-107">PROPVARIANT member</span></span>

<span data-ttu-id="36cae-108">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="36cae-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="36cae-109">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="36cae-109">VT\_BOOL</span></span>

<span data-ttu-id="36cae-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="36cae-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="36cae-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="36cae-111">Remarks</span></span>

<span data-ttu-id="36cae-112">Use essa propriedade para configurar o Media Foundation fluxo de bytes HTTP.</span><span class="sxs-lookup"><span data-stu-id="36cae-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="36cae-113">Para definir a propriedade, passe um ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="36cae-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="36cae-114">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="36cae-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="36cae-115">Se o valor for **Variant \_ true**, o fluxo de bytes http usará Urlmon para transporte http.</span><span class="sxs-lookup"><span data-stu-id="36cae-115">If the value is **VARIANT\_TRUE**, the HTTP byte stream uses Urlmon for HTTP transport.</span></span> <span data-ttu-id="36cae-116">Caso contrário, se o valor for **Variant \_ false**, o fluxo de bytes usará o WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="36cae-116">Otherwise, if the value is **VARIANT\_FALSE**, the byte stream uses WinHTTP.</span></span>

<span data-ttu-id="36cae-117">O valor padrão é **Variant \_ true** para aplicativos da Windows Store e **variante \_ false** para o aplicativo da área de trabalho do Windows.</span><span class="sxs-lookup"><span data-stu-id="36cae-117">The default value is **VARIANT\_TRUE** for Windows Store apps and **VARIANT\_FALSE** for Windows desktop application.</span></span>

## <a name="requirements"></a><span data-ttu-id="36cae-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36cae-118">Requirements</span></span>



| <span data-ttu-id="36cae-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="36cae-119">Requirement</span></span> | <span data-ttu-id="36cae-120">Valor</span><span class="sxs-lookup"><span data-stu-id="36cae-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36cae-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36cae-121">Header</span></span><br/> | <dl> <span data-ttu-id="36cae-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="36cae-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36cae-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="36cae-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36cae-124">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="36cae-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
