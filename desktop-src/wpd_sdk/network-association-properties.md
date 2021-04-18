---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de associação de rede.
ms.assetid: 5e1b3e8d-9620-4b68-b7ef-1642404ed6ed
title: Propriedades de associação de rede (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 41e40e456d4671d1aa8fb190274afd2f5ace98b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810831"
---
# <a name="network-association-properties"></a><span data-ttu-id="81061-103">Propriedades de associação de rede</span><span class="sxs-lookup"><span data-stu-id="81061-103">Network Association Properties</span></span>

<span data-ttu-id="81061-104">Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de associação de rede.</span><span class="sxs-lookup"><span data-stu-id="81061-104">Windows Portable Devices supports the following network association properties.</span></span>



| <span data-ttu-id="81061-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="81061-105">Property</span></span>                                                  | <span data-ttu-id="81061-106">VarType</span><span class="sxs-lookup"><span data-stu-id="81061-106">VarType</span></span>                   | <span data-ttu-id="81061-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="81061-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81061-108">**\_ \_ \_ \_ identificadores de rede do host de associação de rede WPD \_**</span><span class="sxs-lookup"><span data-stu-id="81061-108">**WPD\_NETWORK\_ASSOCIATION\_HOST\_NETWORK\_IDENTIFIERS**</span></span> | <span data-ttu-id="81061-109">**\_UI1 de vetor \| VT \_ VT**</span><span class="sxs-lookup"><span data-stu-id="81061-109">**VT\_VECTOR \| VT\_UI1**</span></span> | <span data-ttu-id="81061-110">A lista de identificadores de host EUI-64 válidos para esta associação. Esta é uma matriz de bytes que contém um número integral de endereços de rede física EUI-64.</span><span class="sxs-lookup"><span data-stu-id="81061-110">The list of EUI-64 host identifiers valid for this association.This is an array of bytes that contains an integral number of EUI-64 physical network addresses.</span></span> <span data-ttu-id="81061-111">Esses valores EUI-64 são os endereços de rede física disponíveis no host no momento da Associação de rede.</span><span class="sxs-lookup"><span data-stu-id="81061-111">These EUI-64 values are the physical network addresses available on the host at Network Association time.</span></span> <span data-ttu-id="81061-112">Se o host tiver endereços de rede física MAC-48 (típicos de redes IPv4), cada endereço MAC-48 será codificado no endereço EUI-64 como as duas metades do endereço MAC-48 separados por FF-FF.</span><span class="sxs-lookup"><span data-stu-id="81061-112">If the host has MAC-48 physical network addresses (typical of IPv4 networks), each MAC-48 address will be encoded in the EUI-64 address as the two halves of the MAC-48 address separated by FF-FF.</span></span><br/> |
| <span data-ttu-id="81061-113">**\_X509V3SEQUENCE de \_ Associação de rede WPD \_**</span><span class="sxs-lookup"><span data-stu-id="81061-113">**WPD\_NETWORK\_ASSOCIATION\_X509V3SEQUENCE**</span></span>             | <span data-ttu-id="81061-114">**\_UI1 de vetor \| VT \_ VT**</span><span class="sxs-lookup"><span data-stu-id="81061-114">**VT\_VECTOR \| VT\_UI1**</span></span> | <span data-ttu-id="81061-115">A sequência de certificados X. 509 v3 a serem fornecidos para a autenticação do servidor TLS.</span><span class="sxs-lookup"><span data-stu-id="81061-115">The sequence of X.509 v3 certificates to be provided for TLS server authentication.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="81061-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81061-116">Requirements</span></span>



| <span data-ttu-id="81061-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="81061-117">Requirement</span></span> | <span data-ttu-id="81061-118">Valor</span><span class="sxs-lookup"><span data-stu-id="81061-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="81061-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81061-119">Header</span></span><br/> | <dl> <span data-ttu-id="81061-120"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="81061-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81061-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="81061-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81061-122">**Propriedades e atributos WPD**</span><span class="sxs-lookup"><span data-stu-id="81061-122">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




