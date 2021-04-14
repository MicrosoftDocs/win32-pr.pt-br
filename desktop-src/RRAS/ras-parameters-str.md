---
title: Estrutura de RAS_PARAMETERS (Rassapi. h)
description: A estrutura de parâmetros de RAS \_ é usada pela função RasAdminPortGetInfo para retornar o nome e o valor de um parâmetro específico de mídia associado a uma porta em um servidor RAS.
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS da estrutura de RAS_PARAMETERS
topic_type:
- apiref
api_name:
- RAS_PARAMETERS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffaefa8a6f2cffb895cc18882ed8fc0c382a4bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499622"
---
# <a name="ras_parameters-structure"></a><span data-ttu-id="66ae1-104">Estrutura de parâmetros de RAS \_</span><span class="sxs-lookup"><span data-stu-id="66ae1-104">RAS\_PARAMETERS structure</span></span>

<span data-ttu-id="66ae1-105">\[A estrutura de **\_ parâmetros de Ras** não tem suporte no Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="66ae1-105">\[The **RAS\_PARAMETERS** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="66ae1-106">A estrutura de **\_ parâmetros de Ras** é usada pela função [**RasAdminPortGetInfo**](rasadminportgetinfo.md) para retornar o nome e o valor de um parâmetro específico de mídia associado a uma porta em um servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="66ae1-106">The **RAS\_PARAMETERS** structure is used by the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function to return the name and value of a media-specific parameter associated with a port on a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="66ae1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66ae1-107">Syntax</span></span>


```C++
typedef struct RAS_PARAMETERS {
  CHAR              P_Key[RASSAPI_MAX_PARAM_KEY_SIZE];
  RAS_PARAMS_FORMAT P_Type;
  BYTE              P_Attributes;
  RAS_PARAMS_VALUE  P_Value;
} RAS_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="66ae1-108">Membros</span><span class="sxs-lookup"><span data-stu-id="66ae1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="66ae1-109">**\_Tecla P**</span><span class="sxs-lookup"><span data-stu-id="66ae1-109">**P\_Key**</span></span>
</dt> <dd>

<span data-ttu-id="66ae1-110">Especifica o nome da chave que representa o parâmetro específico de mídia, como MAXCONNECTBPS.</span><span class="sxs-lookup"><span data-stu-id="66ae1-110">Specifies the name of the key that represents the media-specific parameter, such as MAXCONNECTBPS.</span></span>

</dd> <dt>

<span data-ttu-id="66ae1-111">**Tipo de P \_**</span><span class="sxs-lookup"><span data-stu-id="66ae1-111">**P\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="66ae1-112">Identifica o tipo de dados associado ao parâmetro.</span><span class="sxs-lookup"><span data-stu-id="66ae1-112">Identifies the type of data associated with the parameter.</span></span> <span data-ttu-id="66ae1-113">Esse membro pode ser um dos seguintes valores da enumeração de [**\_ \_ formato de parâmetros de Ras**](ras-params-format-str.md) .</span><span class="sxs-lookup"><span data-stu-id="66ae1-113">This member can be one of the following values from the [**RAS\_PARAMS\_FORMAT**](ras-params-format-str.md) enumeration.</span></span>



| <span data-ttu-id="66ae1-114">Valor</span><span class="sxs-lookup"><span data-stu-id="66ae1-114">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="66ae1-115">Significado</span><span class="sxs-lookup"><span data-stu-id="66ae1-115">Meaning</span></span>                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <span data-ttu-id="66ae1-116"><dt>**ParamNumber**</dt></span><span class="sxs-lookup"><span data-stu-id="66ae1-116"><dt>**ParamNumber**</dt></span></span> </dl> | <span data-ttu-id="66ae1-117">Indica que os dados associados à chave são um número.</span><span class="sxs-lookup"><span data-stu-id="66ae1-117">Indicates that the data associated with the key is a number.</span></span><br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <span data-ttu-id="66ae1-118"><dt>**Paramstring**</dt></span><span class="sxs-lookup"><span data-stu-id="66ae1-118"><dt>**ParamString**</dt></span></span> </dl> | <span data-ttu-id="66ae1-119">Indica que os dados associados à chave são uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="66ae1-119">Indicates that the data associated with the key is a string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="66ae1-120">**Atributos de P \_**</span><span class="sxs-lookup"><span data-stu-id="66ae1-120">**P\_Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="66ae1-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="66ae1-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="66ae1-122">**\_Valor P**</span><span class="sxs-lookup"><span data-stu-id="66ae1-122">**P\_Value**</span></span>
</dt> <dd>

<span data-ttu-id="66ae1-123">Especifica o valor associado ao parâmetro.</span><span class="sxs-lookup"><span data-stu-id="66ae1-123">Specifies the value associated with the parameter.</span></span> <span data-ttu-id="66ae1-124">Esse membro é uma União de [**\_ \_ valor de parâmetros RAS**](ras-params-value-str.md) .</span><span class="sxs-lookup"><span data-stu-id="66ae1-124">This member is a [**RAS\_PARAMS\_VALUE**](ras-params-value-str.md) union.</span></span> <span data-ttu-id="66ae1-125">Se o membro do **\_ tipo P** for ParamNumber, o membro **Number** da União conterá o valor.</span><span class="sxs-lookup"><span data-stu-id="66ae1-125">If the **P\_Type** member is ParamNumber, the **Number** member of the union contains the value.</span></span> <span data-ttu-id="66ae1-126">Se **P \_ Type** for paramstring, o membro **String** da União conterá o valor.</span><span class="sxs-lookup"><span data-stu-id="66ae1-126">If **P\_Type** is ParamString, the **String** member of the union contains the value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66ae1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66ae1-127">Requirements</span></span>



| <span data-ttu-id="66ae1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="66ae1-128">Requirement</span></span> | <span data-ttu-id="66ae1-129">Valor</span><span class="sxs-lookup"><span data-stu-id="66ae1-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="66ae1-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66ae1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="66ae1-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="66ae1-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="66ae1-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66ae1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="66ae1-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="66ae1-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="66ae1-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="66ae1-134">End of client support</span></span><br/>    | <span data-ttu-id="66ae1-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="66ae1-135">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="66ae1-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="66ae1-136">End of server support</span></span><br/>    | <span data-ttu-id="66ae1-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="66ae1-137">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="66ae1-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66ae1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="66ae1-139"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="66ae1-139"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66ae1-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="66ae1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66ae1-141">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="66ae1-141">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="66ae1-142">Estruturas de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="66ae1-142">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="66ae1-143">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="66ae1-143">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="66ae1-144">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="66ae1-144">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="66ae1-145">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="66ae1-145">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





