---
description: O \_ tipo de enumeração de tipos de taxa de bits WPD \_ descreve um tipo de compactação arquivos de áudio.
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: Enumeração de WPD_BITRATE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_BITRATE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2597af21c5655c3c12c0ca29f097d0eba2bb8d54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791599"
---
# <a name="wpd_bitrate_types-enumeration"></a><span data-ttu-id="a98c3-103">\_Enumeração de tipos de taxa de bits WPD \_</span><span class="sxs-lookup"><span data-stu-id="a98c3-103">WPD\_BITRATE\_TYPES enumeration</span></span>

<span data-ttu-id="a98c3-104">O tipo de enumeração de **\_ \_ tipos de taxa de bits WPD** descreve o tipo de compactação de um arquivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="a98c3-104">The **WPD\_BITRATE\_TYPES** enumeration type describes an audio file's compression type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a98c3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a98c3-105">Syntax</span></span>


```C++
typedef enum WPD_BITRATE_TYPES { 
  WPD_BITRATE_TYPE_UNUSED    = 0,
  WPD_BITRATE_TYPE_DISCRETE  = 1,
  WPD_BITRATE_TYPE_VARIABLE  = 2,
  WPD_BITRATE_TYPE_FREE      = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="a98c3-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a98c3-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a98c3-107"><span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**\_tipo de taxa de bits WPD \_ \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="a98c3-107"><span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**WPD\_BITRATE\_TYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="a98c3-108">Este valor não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="a98c3-108">This value has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="a98c3-109"><span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**\_tipo de taxa de bits WPD \_ \_ discreto**</span><span class="sxs-lookup"><span data-stu-id="a98c3-109"><span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**WPD\_BITRATE\_TYPE\_DISCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="a98c3-110">Compactação de taxa de bits constante.</span><span class="sxs-lookup"><span data-stu-id="a98c3-110">Constant bit rate compression.</span></span>

</dd> <dt>

<span data-ttu-id="a98c3-111"><span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**variável de tipo de taxa de \_ bits WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a98c3-111"><span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**WPD\_BITRATE\_TYPE\_VARIABLE**</span></span>
</dt> <dd>

<span data-ttu-id="a98c3-112">Compactação de taxa de bits variável.</span><span class="sxs-lookup"><span data-stu-id="a98c3-112">Variable bit rate compression.</span></span>

</dd> <dt>

<span data-ttu-id="a98c3-113"><span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**\_tipo de taxa de bits WPD \_ \_ gratuito**</span><span class="sxs-lookup"><span data-stu-id="a98c3-113"><span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**WPD\_BITRATE\_TYPE\_FREE**</span></span>
</dt> <dd>

<span data-ttu-id="a98c3-114">Taxa de bits de formato livre.</span><span class="sxs-lookup"><span data-stu-id="a98c3-114">Free format bit rate.</span></span> <span data-ttu-id="a98c3-115">Essa é uma taxa de bits constante inferior à taxa máxima de bits permitida.</span><span class="sxs-lookup"><span data-stu-id="a98c3-115">This is a constant bit rate that is lower than the maximum allowed bit rate.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a98c3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a98c3-116">Requirements</span></span>



| <span data-ttu-id="a98c3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a98c3-117">Requirement</span></span> | <span data-ttu-id="a98c3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a98c3-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a98c3-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a98c3-119">Header</span></span><br/> | <dl> <span data-ttu-id="a98c3-120"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a98c3-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a98c3-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a98c3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a98c3-122">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="a98c3-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




