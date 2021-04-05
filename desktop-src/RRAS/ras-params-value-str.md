---
title: União de RAS_PARAMS_VALUE (Rassapi. h)
description: A \_ União de valor de params de Ras \_ é usada na estrutura de parâmetros de Ras \_ para armazenar os dados associados a um parâmetro específico de mídia.
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS do RAS_PARAMS_VALUE Union
topic_type:
- apiref
api_name:
- RAS_PARAMS_VALUE
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f8cc6d693b32b1bbe6f05e8d32ca31a48cfb29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085139"
---
# <a name="ras_params_value-union"></a><span data-ttu-id="52c6f-104">União de valor de \_ parâmetros RAS \_</span><span class="sxs-lookup"><span data-stu-id="52c6f-104">RAS\_PARAMS\_VALUE union</span></span>

<span data-ttu-id="52c6f-105">\[A União de **\_ \_ valores de parâmetros RAS** não tem suporte a partir do Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="52c6f-105">\[The **RAS\_PARAMS\_VALUE** union is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="52c6f-106">A União de **\_ \_ valor de params de Ras** é usada na estrutura de [**\_ parâmetros de Ras**](ras-parameters-str.md) para armazenar os dados associados a um parâmetro específico de mídia.</span><span class="sxs-lookup"><span data-stu-id="52c6f-106">The **RAS\_PARAMS\_VALUE** union is used in the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure to store the data associated with a media-specific parameter.</span></span> <span data-ttu-id="52c6f-107">O **membro \_ P Type** da estrutura de **\_ parâmetros de Ras** usa um valor da enumeração de [**\_ \_ formato de params de Ras**](ras-params-format-str.md) para indicar o tipo de valor atualmente armazenado no **\_ \_ valor de params RAS**.</span><span class="sxs-lookup"><span data-stu-id="52c6f-107">The **P\_Type** member of the **RAS\_PARAMETERS** structure uses a value from the [**RAS\_PARAMS\_FORMAT**](ras-params-format-str.md) enumeration to indicate the type of value currently stored in **RAS\_PARAMS\_VALUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c6f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52c6f-108">Syntax</span></span>


```C++
typedef union RAS_PARAMS_VALUE {
  DWORD  Number;
  struct {
    DWORD Length;
    PCHAR Data;
  } String;
} RAS_PARAMS_VALUE;
```



## <a name="members"></a><span data-ttu-id="52c6f-109">Membros</span><span class="sxs-lookup"><span data-stu-id="52c6f-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="52c6f-110">**Número**</span><span class="sxs-lookup"><span data-stu-id="52c6f-110">**Number**</span></span>
</dt> <dd>

<span data-ttu-id="52c6f-111">Se o membro do **\_ tipo P** da estrutura de [**\_ parâmetros de Ras**](ras-parameters-str.md) for ParamNumber, o membro **Number** conterá o valor do parâmetro específico de mídia.</span><span class="sxs-lookup"><span data-stu-id="52c6f-111">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamNumber, the **Number** member contains the value of the media-specific parameter.</span></span> <span data-ttu-id="52c6f-112">Por exemplo, o parâmetro MAXCONNECTBPS é do tipo ParamNumber e o valor pode ser 19200.</span><span class="sxs-lookup"><span data-stu-id="52c6f-112">For example, the MAXCONNECTBPS parameter is of type ParamNumber, and the value might be 19200.</span></span>

<span data-ttu-id="52c6f-113">Se o membro do **\_ tipo P** da estrutura de [**\_ parâmetros de Ras**](ras-parameters-str.md) for ParamNumber, o membro **Number** conterá o valor do parâmetro específico de mídia.</span><span class="sxs-lookup"><span data-stu-id="52c6f-113">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamNumber, the **Number** member contains the value of the media-specific parameter.</span></span> <span data-ttu-id="52c6f-114">Por exemplo, o parâmetro MAXCONNECTBPS é do tipo ParamNumber e o valor pode ser 19200.</span><span class="sxs-lookup"><span data-stu-id="52c6f-114">For example, the MAXCONNECTBPS parameter is of type ParamNumber, and the value might be 19200.</span></span>

</dd> <dt>

<span data-ttu-id="52c6f-115">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="52c6f-115">**String**</span></span>
</dt> <dd>

<span data-ttu-id="52c6f-116">Se o membro do **\_ tipo P** da estrutura de [**\_ parâmetros de Ras**](ras-parameters-str.md) for Paramstring, o membro da **cadeia de caracteres** conterá o valor do parâmetro específico da mídia.</span><span class="sxs-lookup"><span data-stu-id="52c6f-116">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamString, the **String** member contains the value of the media-specific parameter.</span></span>

<dl> <dt>

<span data-ttu-id="52c6f-117">**Comprimento**</span><span class="sxs-lookup"><span data-stu-id="52c6f-117">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="52c6f-118">Especifica o comprimento, em caracteres, da cadeia de caracteres apontada pelo membro de **dados** .</span><span class="sxs-lookup"><span data-stu-id="52c6f-118">Specifies the length, in characters, of the string pointed to by the **Data** member.</span></span>

</dd> <dt>

<span data-ttu-id="52c6f-119">**Dados**</span><span class="sxs-lookup"><span data-stu-id="52c6f-119">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="52c6f-120">Ponteiro para um buffer que contém o valor da cadeia de caracteres de um parâmetro específico de mídia.</span><span class="sxs-lookup"><span data-stu-id="52c6f-120">Pointer to a buffer that contains the string value of a media-specific parameter.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52c6f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52c6f-121">Requirements</span></span>



| <span data-ttu-id="52c6f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="52c6f-122">Requirement</span></span> | <span data-ttu-id="52c6f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="52c6f-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="52c6f-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52c6f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="52c6f-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52c6f-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="52c6f-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52c6f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="52c6f-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52c6f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="52c6f-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="52c6f-128">End of client support</span></span><br/>    | <span data-ttu-id="52c6f-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="52c6f-129">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="52c6f-130">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="52c6f-130">End of server support</span></span><br/>    | <span data-ttu-id="52c6f-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="52c6f-131">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="52c6f-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52c6f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="52c6f-133"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="52c6f-133"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52c6f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="52c6f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52c6f-135">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="52c6f-135">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="52c6f-136">Union de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="52c6f-136">RAS Server Administration Union</span></span>](ras-server-administration-union.md)
</dt> <dt>

[<span data-ttu-id="52c6f-137">**parâmetros de RAS \_**</span><span class="sxs-lookup"><span data-stu-id="52c6f-137">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="52c6f-138">**\_formato de parâmetros \_ RAS**</span><span class="sxs-lookup"><span data-stu-id="52c6f-138">**RAS\_PARAMS\_FORMAT**</span></span>](ras-params-format-str.md)
</dt> </dl>

 

 





