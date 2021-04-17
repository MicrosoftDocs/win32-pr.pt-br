---
description: A estrutura de eventos de atualização \_ atualiza eventos. Essa estrutura é passada de volta para o aplicativo de chamada por meio do procedimento de retorno de chamada de status do evento pelo NPP.
ms.assetid: 6896be5a-f986-44ff-a18b-010f7b9858aa
title: Estrutura de UPDATE_EVENT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UPDATE_EVENT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3da45020a68114182a71b25ff9bba380d3f89eee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812757"
---
# <a name="update_event-structure"></a><span data-ttu-id="3c0ae-104">ATUALIZAR \_ estrutura de eventos</span><span class="sxs-lookup"><span data-stu-id="3c0ae-104">UPDATE\_EVENT structure</span></span>

<span data-ttu-id="3c0ae-105">A estrutura de **\_ eventos de atualização** atualiza eventos.</span><span class="sxs-lookup"><span data-stu-id="3c0ae-105">The **UPDATE\_EVENT** structure updates events.</span></span> <span data-ttu-id="3c0ae-106">Essa estrutura é passada de volta para o aplicativo de chamada por meio do procedimento de retorno de chamada de status do evento pelo NPP.</span><span class="sxs-lookup"><span data-stu-id="3c0ae-106">This structure is passed back to the calling application via the event status callback procedure by the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c0ae-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c0ae-107">Syntax</span></span>


```C++
typedef struct _UPDATE_EVENT {
  USHORT       Event;
  DWORD        Action;
  DWORD        Status;
  DWORD        Value;
  __int64      TimeStamp;
  DWORD_PTR    lpUserContext;
  DWORD_PTR    lpReserved;
  UINT         FramesDropped;
  union {
    DWORD                        Reserved;
    LPFRAMETABLE                 lpFrameTable;
    DWORD_PTR                    lpPacketQueue;
    SECURITY_PERMISSION_RESPONSE SecurityResponse;
  };
  LPSTATISTICS lpFinalStats;
} UPDATE_EVENT, *PUPDATE_EVENT;
```



## <a name="members"></a><span data-ttu-id="3c0ae-108">Membros</span><span class="sxs-lookup"><span data-stu-id="3c0ae-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3c0ae-109">**Evento**</span><span class="sxs-lookup"><span data-stu-id="3c0ae-109">**Event**</span></span>
</dt> <dd>

<span data-ttu-id="3c0ae-110">Evento real que está sendo registrado.</span><span class="sxs-lookup"><span data-stu-id="3c0ae-110">Actual event being recorded.</span></span>

</dd> <dt>

<span data-ttu-id="3c0ae-111">**Ação**</span><span class="sxs-lookup"><span data-stu-id="3c0ae-111">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="3c0ae-112">A ação executada.</span><span class="sxs-lookup"><span data-stu-id="3c0ae-112">The action taken.</span></span>

</dd> <dt>

<span data-ttu-id="3c0ae-113">**Status**</span><span class="sxs-lookup"><span data-stu-id="3c0ae-113">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="3c0ae-114">Indicação de status de rede.</span><span class="sxs-lookup"><span data-stu-id="3c0ae-114">Network status indication.</span></span>

</dd> <dt>

<span data-ttu-id="3c0ae-115">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3c0ae-115">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="3c0ae-116">Variável de contador auxiliar.</span><span class="sxs-lookup"><span data-stu-id="3c0ae-116">Auxiliary counter variable.</span></span>

</dd> <dt>

<span data-ttu-id="3c0ae-117">**Estampa**</span><span class="sxs-lookup"><span data-stu-id="3c0ae-117">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="3c0ae-118">Os eventos marcados, em microssegundos.</span><span class="sxs-lookup"><span data-stu-id="3c0ae-118">The marked events, in microseconds.</span></span>

</dd> <dt>

<span data-ttu-id="3c0ae-119">**lpUserContext**</span><span class="sxs-lookup"><span data-stu-id="3c0ae-119">**lpUserContext**</span></span>
</dt> <dd>

<span data-ttu-id="3c0ae-120">Contexto de usuário fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3c0ae-120">User context given by the application.</span></span>

</dd> <dt>

<span data-ttu-id="3c0ae-121">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="3c0ae-121">**lpReserved**</span></span>
</dt> <dd>

<span data-ttu-id="3c0ae-122">Uso de driver ou NAL.</span><span class="sxs-lookup"><span data-stu-id="3c0ae-122">Driver or NAL use.</span></span>

</dd> <dt>

<span data-ttu-id="3c0ae-123">**FramesDropped**</span><span class="sxs-lookup"><span data-stu-id="3c0ae-123">**FramesDropped**</span></span>
</dt> <dd>

<span data-ttu-id="3c0ae-124">Quadros RTF descartados no buffer especificado.</span><span class="sxs-lookup"><span data-stu-id="3c0ae-124">RTF frames dropped in the specified buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3c0ae-125">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="3c0ae-125">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="3c0ae-126">Nenhum dado é retornado com essa opção de opção.</span><span class="sxs-lookup"><span data-stu-id="3c0ae-126">No data comes back with this switch option.</span></span>

</dd> <dt>

<span data-ttu-id="3c0ae-127">**lpFrameTable**</span><span class="sxs-lookup"><span data-stu-id="3c0ae-127">**lpFrameTable**</span></span>
</dt> <dd>

<span data-ttu-id="3c0ae-128">Somente RTF.</span><span class="sxs-lookup"><span data-stu-id="3c0ae-128">RTF only.</span></span>

</dd> <dt>

<span data-ttu-id="3c0ae-129">**lpPacketQueue**</span><span class="sxs-lookup"><span data-stu-id="3c0ae-129">**lpPacketQueue**</span></span>
</dt> <dd>

<span data-ttu-id="3c0ae-130">Para transmissões.</span><span class="sxs-lookup"><span data-stu-id="3c0ae-130">For transmits.</span></span>

</dd> <dt>

<span data-ttu-id="3c0ae-131">**SecurityResponse**</span><span class="sxs-lookup"><span data-stu-id="3c0ae-131">**SecurityResponse**</span></span>
</dt> <dd>

<span data-ttu-id="3c0ae-132">Resposta do monitor de segurança remota.</span><span class="sxs-lookup"><span data-stu-id="3c0ae-132">Remote security monitor response.</span></span>

</dd> <dt>

<span data-ttu-id="3c0ae-133">**lpFinalStats**</span><span class="sxs-lookup"><span data-stu-id="3c0ae-133">**lpFinalStats**</span></span>
</dt> <dd>

<span data-ttu-id="3c0ae-134">Isso só é preenchido em paradas não relacionadas à segurança (por exemplo, gatilhos).</span><span class="sxs-lookup"><span data-stu-id="3c0ae-134">This is only filled in on non-security related stops (for example, triggers).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c0ae-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c0ae-135">Remarks</span></span>

<span data-ttu-id="3c0ae-136">Os usuários do C++ devem observar que a declaração desse retorno de chamada deve estar na parte pública do arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="3c0ae-136">C++ users should note that the declaration for this callback should be in the public part of the header file:</span></span>

``` syntax
static WINAPI DWORD NetworkCallback( UPDATE_EVENT events);
```

<span data-ttu-id="3c0ae-137">A implementação deve estar na seção protegida do arquivo. cpp:</span><span class="sxs-lookup"><span data-stu-id="3c0ae-137">The implementation should be in the protected section of the .cpp file:</span></span>

``` syntax
DWORD WINAPI ClassName::NetworkCallback( UPDATE_EVENT events) {};
```

## <a name="requirements"></a><span data-ttu-id="3c0ae-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c0ae-138">Requirements</span></span>



| <span data-ttu-id="3c0ae-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c0ae-139">Requirement</span></span> | <span data-ttu-id="3c0ae-140">Valor</span><span class="sxs-lookup"><span data-stu-id="3c0ae-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3c0ae-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c0ae-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3c0ae-142">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3c0ae-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3c0ae-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c0ae-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3c0ae-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3c0ae-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3c0ae-145">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3c0ae-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c0ae-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c0ae-146"><dt>Netmon.h</dt></span></span> </dl> |



 

 




