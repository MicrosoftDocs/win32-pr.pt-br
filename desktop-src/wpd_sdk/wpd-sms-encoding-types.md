---
description: O \_ tipo de enumeração de tipos de codificação do SMS WPD \_ \_ descreve o tipo de codificação de uma mensagem de SMS (serviço de mensagens curtas).
ms.assetid: 5a9752e5-4e09-42a4-8fed-b4ea551fa36f
title: Enumeração de WPD_SMS_ENCODING_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SMS_ENCODING_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f7deae3cdc560e27e19b5ff7664e5566cff6d7e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748677"
---
# <a name="wpd_sms_encoding_types-enumeration"></a><span data-ttu-id="60258-103">\_Enumeração de \_ tipos de codificação de SMS WPD \_</span><span class="sxs-lookup"><span data-stu-id="60258-103">WPD\_SMS\_ENCODING\_TYPES enumeration</span></span>

<span data-ttu-id="60258-104">O tipo de enumeração de **\_ tipos de \_ codificação \_ do SMS WPD** descreve o tipo de codificação de uma mensagem de SMS (serviço de mensagens curtas).</span><span class="sxs-lookup"><span data-stu-id="60258-104">The **WPD\_SMS\_ENCODING\_TYPES** enumeration type describes the encoding type of a short message service (SMS) message.</span></span>

## <a name="syntax"></a><span data-ttu-id="60258-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60258-105">Syntax</span></span>


```C++
typedef enum WPD_SMS_ENCODING_TYPES { 
  SMS_ENCODING_7_BIT   = 0,
  SMS_ENCODING_8_BIT   = 1,
  SMS_ENCODING_UTF_16  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="60258-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="60258-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="60258-107"><span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**Codificação de SMS \_ \_ 7 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="60258-107"><span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**SMS\_ENCODING\_7\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="60258-108">Codificação de sete bits.</span><span class="sxs-lookup"><span data-stu-id="60258-108">Seven-bit encoding.</span></span>

</dd> <dt>

<span data-ttu-id="60258-109"><span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**Codificação de SMS \_ \_ 8 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="60258-109"><span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**SMS\_ENCODING\_8\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="60258-110">Codificação de oito bits.</span><span class="sxs-lookup"><span data-stu-id="60258-110">Eight-bit encoding.</span></span>

</dd> <dt>

<span data-ttu-id="60258-111"><span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**Codificação de SMS de \_ \_ UTF \_ 16**</span><span class="sxs-lookup"><span data-stu-id="60258-111"><span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**SMS\_ENCODING\_UTF\_16**</span></span>
</dt> <dd>

<span data-ttu-id="60258-112">Codificação de 16 bits (UTF).</span><span class="sxs-lookup"><span data-stu-id="60258-112">Sixteen-bit encoding (UTF).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60258-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="60258-113">Remarks</span></span>

<span data-ttu-id="60258-114">Essa enumeração é usada pela propriedade [de \_ \_ codificação de SMS WPD](sms-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="60258-114">This enumeration is used by the [WPD\_SMS\_ENCODING](sms-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="60258-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60258-115">Requirements</span></span>



| <span data-ttu-id="60258-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="60258-116">Requirement</span></span> | <span data-ttu-id="60258-117">Valor</span><span class="sxs-lookup"><span data-stu-id="60258-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="60258-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="60258-118">Header</span></span><br/> | <dl> <span data-ttu-id="60258-119"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="60258-119"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60258-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="60258-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60258-121">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="60258-121">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




