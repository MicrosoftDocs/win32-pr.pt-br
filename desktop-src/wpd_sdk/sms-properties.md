---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades do SMS.
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: Propriedades do SMS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c43917c8c26027713b4e5076e8eb3789b95f08e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105815519"
---
# <a name="sms-properties"></a><span data-ttu-id="ce206-103">Propriedades do SMS</span><span class="sxs-lookup"><span data-stu-id="ce206-103">SMS Properties</span></span>

<span data-ttu-id="ce206-104">Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades do SMS.</span><span class="sxs-lookup"><span data-stu-id="ce206-104">Windows Portable Devices supports the following SMS properties.</span></span>



| <span data-ttu-id="ce206-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ce206-105">Property</span></span>                   | <span data-ttu-id="ce206-106">VarType</span><span class="sxs-lookup"><span data-stu-id="ce206-106">VarType</span></span>        | <span data-ttu-id="ce206-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce206-107">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce206-108">**\_codificação de SMS WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ce206-108">**WPD\_SMS\_ENCODING**</span></span>     | <span data-ttu-id="ce206-109">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="ce206-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="ce206-110">Um valor que especifica como o driver codificará a mensagem de texto enviada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="ce206-110">A value that specifies how the driver will encode the text message sent by the client.</span></span> <span data-ttu-id="ce206-111">Esta é uma propriedade somente leitura; o cliente não pode especificar qual tipo de codificação um dispositivo usa para enviar mensagens.</span><span class="sxs-lookup"><span data-stu-id="ce206-111">This is a read-only property; the client cannot specify what encoding type a device uses to send messages.</span></span> <span data-ttu-id="ce206-112">Esses valores duplicam os valores enumerados dos [**\_ tipos de \_ codificação \_ do SMS WPD**](wpd-sms-encoding-types.md) .</span><span class="sxs-lookup"><span data-stu-id="ce206-112">These values duplicate the [**WPD\_SMS\_ENCODING\_TYPES**](wpd-sms-encoding-types.md) enumerated values.</span></span> |
| <span data-ttu-id="ce206-113">**\_ \_ carga máxima de SMS WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ce206-113">**WPD\_SMS\_MAX\_PAYLOAD**</span></span> | <span data-ttu-id="ce206-114">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="ce206-114">**VT\_UI4**</span></span>    | <span data-ttu-id="ce206-115">O número máximo de bytes que podem estar contidos em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="ce206-115">The maximum number of bytes that can be contained in a message.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="ce206-116">**\_provedor de SMS WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ce206-116">**WPD\_SMS\_PROVIDER**</span></span>     | <span data-ttu-id="ce206-117">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="ce206-117">**VT\_LPWSTR**</span></span> | <span data-ttu-id="ce206-118">O nome do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="ce206-118">The service provider's name.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="ce206-119">**\_tempo limite de SMS WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ce206-119">**WPD\_SMS\_TIMEOUT**</span></span>      | <span data-ttu-id="ce206-120">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="ce206-120">**VT\_UI4**</span></span>    | <span data-ttu-id="ce206-121">O número de milissegundos até que um tempo limite seja retornado.</span><span class="sxs-lookup"><span data-stu-id="ce206-121">The number of milliseconds until a timeout is returned.</span></span>                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="ce206-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce206-122">Requirements</span></span>



| <span data-ttu-id="ce206-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce206-123">Requirement</span></span> | <span data-ttu-id="ce206-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ce206-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce206-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce206-125">Header</span></span><br/> | <dl> <span data-ttu-id="ce206-126"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce206-126"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce206-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce206-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce206-128">**Propriedades e atributos WPD**</span><span class="sxs-lookup"><span data-stu-id="ce206-128">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




