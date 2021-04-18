---
description: Define os sinalizadores de associação do moniker para o Microsoft Media Foundation fluxo de bytes HTTP.
ms.assetid: 9426D235-65E1-40BA-94E9-CF0C49263E6F
title: Propriedade MFPKEY_HTTP_ByteStream_Urlmon_Bind_Flags (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32863929b92f16a809468055db81361f8116196e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781112"
---
# <a name="mfpkey_http_bytestream_urlmon_bind_flags-property"></a><span data-ttu-id="513f6-103">\_Propriedade de sinalizadores de associação MFPKEY http \_ bytes \_ Urlmon \_ \_</span><span class="sxs-lookup"><span data-stu-id="513f6-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Bind\_Flags property</span></span>

<span data-ttu-id="513f6-104">Define os sinalizadores de associação do moniker para o Microsoft Media Foundation fluxo de bytes HTTP.</span><span class="sxs-lookup"><span data-stu-id="513f6-104">Sets the moniker binding flags for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="513f6-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="513f6-105">Data type</span></span>

<span data-ttu-id="513f6-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="513f6-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="513f6-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="513f6-107">PROPVARIANT member</span></span>

<span data-ttu-id="513f6-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="513f6-108">**ULONG**</span></span>

<span data-ttu-id="513f6-109">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="513f6-109">VT\_UI4</span></span>

<span data-ttu-id="513f6-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="513f6-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="513f6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="513f6-111">Remarks</span></span>

<span data-ttu-id="513f6-112">Use essa propriedade para configurar o Media Foundation fluxo de bytes HTTP.</span><span class="sxs-lookup"><span data-stu-id="513f6-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="513f6-113">Para definir a propriedade, passe um ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="513f6-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="513f6-114">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="513f6-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="513f6-115">O valor dessa propriedade é um bit a bit **ou** dos sinalizadores da enumeração **BINDF** .</span><span class="sxs-lookup"><span data-stu-id="513f6-115">The value of this property is a bitwise **OR** of flags from the **BINDF** enumeration.</span></span> <span data-ttu-id="513f6-116">Essa propriedade só se aplica quando a propriedade [MFPKEY \_ http \_ bytes \_ Enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) está definida como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="513f6-116">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="513f6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="513f6-117">Requirements</span></span>



| <span data-ttu-id="513f6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="513f6-118">Requirement</span></span> | <span data-ttu-id="513f6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="513f6-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="513f6-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="513f6-120">Header</span></span><br/> | <dl> <span data-ttu-id="513f6-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="513f6-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="513f6-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="513f6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="513f6-123">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="513f6-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
