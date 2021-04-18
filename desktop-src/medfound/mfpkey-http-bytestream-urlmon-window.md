---
description: Define uma janela para o Microsoft Media Foundation fluxo de bytes HTTP.
ms.assetid: 52761AC1-4974-4087-B5EE-A797F5BAD86D
title: Propriedade MFPKEY_HTTP_ByteStream_Urlmon_Window (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df398d2c6d7655a68a139545d84cee48f9cf7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813986"
---
# <a name="mfpkey_http_bytestream_urlmon_window-property"></a><span data-ttu-id="f5aa3-103">\_Propriedade de janela MFPKEY http \_ bytes \_ Urlmon \_</span><span class="sxs-lookup"><span data-stu-id="f5aa3-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Window property</span></span>

<span data-ttu-id="f5aa3-104">Define uma janela para o Microsoft Media Foundation fluxo de bytes HTTP.</span><span class="sxs-lookup"><span data-stu-id="f5aa3-104">Sets a window for the Microsoft Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="f5aa3-105">A janela é usada para apresentar informações na interface do usuário durante uma operação de associação.</span><span class="sxs-lookup"><span data-stu-id="f5aa3-105">The window is used to present information in the user interface during a bind operation.</span></span>



<span data-ttu-id="f5aa3-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f5aa3-106">Data type</span></span>

<span data-ttu-id="f5aa3-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="f5aa3-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f5aa3-108">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="f5aa3-108">PROPVARIANT member</span></span>

<span data-ttu-id="f5aa3-109">**IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="f5aa3-109">**IUnknown\***</span></span>

<span data-ttu-id="f5aa3-110">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="f5aa3-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="f5aa3-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="f5aa3-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="f5aa3-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5aa3-112">Remarks</span></span>

<span data-ttu-id="f5aa3-113">Use essa propriedade para configurar o Media Foundation fluxo de bytes HTTP.</span><span class="sxs-lookup"><span data-stu-id="f5aa3-113">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="f5aa3-114">Para definir a propriedade, passe um ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="f5aa3-114">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="f5aa3-115">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="f5aa3-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="f5aa3-116">O valor dessa propriedade é um ponteiro para a interface **IWindowForBindingUI** .</span><span class="sxs-lookup"><span data-stu-id="f5aa3-116">The value of this property is a pointer to the **IWindowForBindingUI** interface.</span></span> <span data-ttu-id="f5aa3-117">Essa propriedade só se aplica quando a propriedade [MFPKEY \_ http \_ bytes \_ Enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) está definida como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="f5aa3-117">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5aa3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5aa3-118">Requirements</span></span>



| <span data-ttu-id="f5aa3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5aa3-119">Requirement</span></span> | <span data-ttu-id="f5aa3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f5aa3-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5aa3-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5aa3-121">Header</span></span><br/> | <dl> <span data-ttu-id="f5aa3-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5aa3-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5aa3-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5aa3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5aa3-124">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5aa3-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
