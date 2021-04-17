---
description: Define o identificador de segurança raiz para o Microsoft Media Foundation fluxo de bytes HTTP.
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: Propriedade MFPKEY_HTTP_ByteStream_Urlmon_Security_Id (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf23e0c3d4aa5ab25590cfdb207fd50f04ecaec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759803"
---
# <a name="mfpkey_http_bytestream_urlmon_security_id-property"></a><span data-ttu-id="d7660-103">\_Propriedade de ID de segurança MFPKEY http \_ bytes \_ Urlmon \_ \_</span><span class="sxs-lookup"><span data-stu-id="d7660-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Security\_Id property</span></span>

<span data-ttu-id="d7660-104">Define o identificador de segurança raiz para o Microsoft Media Foundation fluxo de bytes HTTP.</span><span class="sxs-lookup"><span data-stu-id="d7660-104">Sets the root security identifier for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="d7660-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d7660-105">Data type</span></span>

<span data-ttu-id="d7660-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="d7660-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d7660-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="d7660-107">PROPVARIANT member</span></span>

<span data-ttu-id="d7660-108">**CAUB**</span><span class="sxs-lookup"><span data-stu-id="d7660-108">**CAUB**</span></span>

<span data-ttu-id="d7660-109">\_UI1 de vetor \| VT \_ VT</span><span class="sxs-lookup"><span data-stu-id="d7660-109">VT\_VECTOR \| VT\_UI1</span></span>

<span data-ttu-id="d7660-110">**caub**</span><span class="sxs-lookup"><span data-stu-id="d7660-110">**caub**</span></span>



## <a name="remarks"></a><span data-ttu-id="d7660-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7660-111">Remarks</span></span>

<span data-ttu-id="d7660-112">Use essa propriedade para configurar o Media Foundation fluxo de bytes HTTP.</span><span class="sxs-lookup"><span data-stu-id="d7660-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="d7660-113">Para definir a propriedade, passe um ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="d7660-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="d7660-114">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="d7660-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="d7660-115">Essa propriedade só se aplica quando a propriedade [MFPKEY \_ http \_ bytes \_ Enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) está definida como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="d7660-115">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7660-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7660-116">Requirements</span></span>



| <span data-ttu-id="d7660-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7660-117">Requirement</span></span> | <span data-ttu-id="d7660-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d7660-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d7660-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7660-119">Header</span></span><br/> | <dl> <span data-ttu-id="d7660-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7660-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7660-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7660-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7660-122">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d7660-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
