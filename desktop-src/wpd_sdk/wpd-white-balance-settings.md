---
description: O \_ tipo de \_ Enumeração configurações de balanço de branco WPD \_ descreve como um dispositivo de vídeo ou imagem tem como peso os canais de cores para atingir um equilíbrio de branco adequado.
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: Enumeração de WPD_WHITE_BALANCE_SETTINGS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_WHITE_BALANCE_SETTINGS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 06e607acc06ed00cc9fe91670650caee44c30430
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751712"
---
# <a name="wpd_white_balance_settings-enumeration"></a><span data-ttu-id="45aab-103">\_Enumeração de \_ configurações de balanço de branco WPD \_</span><span class="sxs-lookup"><span data-stu-id="45aab-103">WPD\_WHITE\_BALANCE\_SETTINGS enumeration</span></span>

<span data-ttu-id="45aab-104">O tipo de enumeração **\_ configurações de \_ balanço \_ de branco WPD** descreve como um dispositivo de vídeo ou imagem tem como peso os canais de cores para atingir um equilíbrio de branco adequado.</span><span class="sxs-lookup"><span data-stu-id="45aab-104">The **WPD\_WHITE\_BALANCE\_SETTINGS** enumeration type describes how a video or image device weights color channels to achieve a proper white balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="45aab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="45aab-105">Syntax</span></span>


```C++
typedef enum WPD_WHITE_BALANCE_SETTINGS { 
  WPD_WHITE_BALANCE_UNDEFINED           = 0,
  WPD_WHITE_BALANCE_MANUAL              = 1,
  WPD_WHITE_BALANCE_AUTOMATIC           = 2,
  WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC  = 3,
  WPD_WHITE_BALANCE_DAYLIGHT            = 4,
  WPD_WHITE_BALANCE_TUNGSTEN            = 5,
  WPD_WHITE_BALANCE_FLASH               = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="45aab-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="45aab-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="45aab-107"><span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**\_balanço de branco WPD \_ \_ indefinido**</span><span class="sxs-lookup"><span data-stu-id="45aab-107"><span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**WPD\_WHITE\_BALANCE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="45aab-108">Este valor não foi definido.</span><span class="sxs-lookup"><span data-stu-id="45aab-108">This value has not been defined.</span></span>

</dd> <dt>

<span data-ttu-id="45aab-109"><span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**\_manual de \_ saldo de branco WPD \_**</span><span class="sxs-lookup"><span data-stu-id="45aab-109"><span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**WPD\_WHITE\_BALANCE\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="45aab-110">O equilíbrio de branco é definido explicitamente usando a propriedade de [ \_ \_ \_ \_ lucro RGB da imagem ainda](still-image-properties.md) mais e não será alterado por si só.</span><span class="sxs-lookup"><span data-stu-id="45aab-110">The white balance is set explicitly by using the [WPD\_STILL\_IMAGE\_RGB\_GAIN](still-image-properties.md) property and will not change by itself.</span></span>

</dd> <dt>

<span data-ttu-id="45aab-111"><span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**saldo de branco WPD- \_ \_ \_ automático**</span><span class="sxs-lookup"><span data-stu-id="45aab-111"><span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**WPD\_WHITE\_BALANCE\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="45aab-112">O dispositivo definirá o equilíbrio de branco.</span><span class="sxs-lookup"><span data-stu-id="45aab-112">The device will set the white balance.</span></span>

</dd> <dt>

<span data-ttu-id="45aab-113"><span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**pressão branca de WPD de \_ \_ \_ um \_ Push \_ automático**</span><span class="sxs-lookup"><span data-stu-id="45aab-113"><span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**WPD\_WHITE\_BALANCE\_ONE\_PUSH\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="45aab-114">O dispositivo definirá o equilíbrio de branco, mas somente quando o usuário enviar por push o botão de captura do dispositivo enquanto mira o dispositivo em um campo branco.</span><span class="sxs-lookup"><span data-stu-id="45aab-114">The device will set the white balance, but only when the user pushes the device's capture button while aiming the device at a white field.</span></span>

</dd> <dt>

<span data-ttu-id="45aab-115"><span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**\_horário de \_ Verão de saldo branco WPD \_**</span><span class="sxs-lookup"><span data-stu-id="45aab-115"><span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD\_WHITE\_BALANCE\_DAYLIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="45aab-116">O dispositivo usará números de saldo branco apropriados para uso na maioria das configurações de horário de verão.</span><span class="sxs-lookup"><span data-stu-id="45aab-116">The device will use white balance numbers appropriate for use in most daylight settings.</span></span>

</dd> <dt>

<span data-ttu-id="45aab-117"><span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**\_Tungsten de \_ saldo de branco WPD \_**</span><span class="sxs-lookup"><span data-stu-id="45aab-117"><span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**WPD\_WHITE\_BALANCE\_TUNGSTEN**</span></span>
</dt> <dd>

<span data-ttu-id="45aab-118">O dispositivo usará números de saldo branco apropriados para uso na maioria das configurações de iluminação de incandescentes.</span><span class="sxs-lookup"><span data-stu-id="45aab-118">The device will use white balance numbers appropriate for use in most indoor, incandescent lighting settings.</span></span>

</dd> <dt>

<span data-ttu-id="45aab-119"><span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**\_flash de \_ proporção de branco WPD \_**</span><span class="sxs-lookup"><span data-stu-id="45aab-119"><span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**WPD\_WHITE\_BALANCE\_FLASH**</span></span>
</dt> <dd>

<span data-ttu-id="45aab-120">O dispositivo usará números de balanço de branco apropriados para uso com um flash.</span><span class="sxs-lookup"><span data-stu-id="45aab-120">The device will use white balance numbers appropriate for use with a flash.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45aab-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="45aab-121">Remarks</span></span>

<span data-ttu-id="45aab-122">Essa enumeração é usada pela propriedade [de \_ \_ balanço de \_ branco \_ de imagem ainda WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="45aab-122">This enumeration is used by the [WPD\_STILL\_IMAGE\_WHITE\_BALANCE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="45aab-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45aab-123">Requirements</span></span>



| <span data-ttu-id="45aab-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="45aab-124">Requirement</span></span> | <span data-ttu-id="45aab-125">Valor</span><span class="sxs-lookup"><span data-stu-id="45aab-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="45aab-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45aab-126">Header</span></span><br/> | <dl> <span data-ttu-id="45aab-127"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="45aab-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45aab-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="45aab-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45aab-129">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="45aab-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




