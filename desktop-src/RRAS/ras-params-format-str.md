---
title: Enumeração de RAS_PARAMS_FORMAT (Rassapi. h)
description: O \_ tipo de enumeração de formato RAS params \_ é usado na \_ estrutura de parâmetros de RAS para indicar o tipo de dados associado a uma chave específica de mídia.
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS de enumeração de RAS_PARAMS_FORMAT
topic_type:
- apiref
api_name:
- RAS_PARAMS_FORMAT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00065f3781fd2ada420f67367e84e0863fe3b446
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085793"
---
# <a name="ras_params_format-enumeration"></a><span data-ttu-id="11be6-104">Enumeração de formato de \_ parâmetros RAS \_</span><span class="sxs-lookup"><span data-stu-id="11be6-104">RAS\_PARAMS\_FORMAT enumeration</span></span>

<span data-ttu-id="11be6-105">\[A enumeração de **\_ \_ formato de parâmetros RAS** não tem suporte no Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="11be6-105">\[The **RAS\_PARAMS\_FORMAT** enumeration is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="11be6-106">O tipo de enumeração de **\_ \_ formato RAS params** é usado na estrutura de [**\_ parâmetros de Ras**](ras-parameters-str.md) para indicar o tipo de dados associado a uma chave específica de mídia.</span><span class="sxs-lookup"><span data-stu-id="11be6-106">The **RAS\_PARAMS\_FORMAT** enumeration type is used in the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure to indicate the type of data associated with a media-specific key.</span></span>

## <a name="syntax"></a><span data-ttu-id="11be6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="11be6-107">Syntax</span></span>


```C++
typedef enum RAS_PARAMS_FORMAT { 
  ParamNumber  = 0,
  ParamString  = 1
} RAS_PARAMS_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="11be6-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="11be6-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="11be6-109"><span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**</span><span class="sxs-lookup"><span data-stu-id="11be6-109"><span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**</span></span>
</dt> <dd>

<span data-ttu-id="11be6-110">Indica que os dados associados à chave são um número.</span><span class="sxs-lookup"><span data-stu-id="11be6-110">Indicates that the data associated with the key is a number.</span></span>

</dd> <dt>

<span data-ttu-id="11be6-111"><span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**Paramstring**</span><span class="sxs-lookup"><span data-stu-id="11be6-111"><span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**</span></span>
</dt> <dd>

<span data-ttu-id="11be6-112">Indica que os dados associados à chave são uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="11be6-112">Indicates that the data associated with the key is a string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11be6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11be6-113">Requirements</span></span>



| <span data-ttu-id="11be6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="11be6-114">Requirement</span></span> | <span data-ttu-id="11be6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="11be6-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="11be6-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11be6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="11be6-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="11be6-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="11be6-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11be6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="11be6-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="11be6-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="11be6-120">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="11be6-120">End of client support</span></span><br/>    | <span data-ttu-id="11be6-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="11be6-121">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="11be6-122">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="11be6-122">End of server support</span></span><br/>    | <span data-ttu-id="11be6-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="11be6-123">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="11be6-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11be6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="11be6-125"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="11be6-125"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11be6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="11be6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11be6-127">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="11be6-127">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="11be6-128">Enumerações de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="11be6-128">RAS Server Administration Enumerations</span></span>](ras-server-administration-enumerations.md)
</dt> <dt>

[<span data-ttu-id="11be6-129">**parâmetros de RAS \_**</span><span class="sxs-lookup"><span data-stu-id="11be6-129">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> </dl>

 

 





