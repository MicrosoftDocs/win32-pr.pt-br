---
title: Estrutura de ORPC_DBG_ALL
description: A \_ estrutura ORPC DBG \_ All é usada para passar parâmetros para os métodos da interface IOrpcDebugNotify.
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- COM ORPC_DBG_ALL estrutura COM
- COM ponteiro de estrutura de LPORPC_DBG_ALL COM
topic_type:
- apiref
api_name:
- ORPC_DBG_ALL
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17f5b09e5fe2f668bf2bcd21e2e7fe6f0f766a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085353"
---
# <a name="orpc_dbg_all-structure"></a><span data-ttu-id="1ee2c-105">\_Estrutura ORPC DBG \_ All</span><span class="sxs-lookup"><span data-stu-id="1ee2c-105">ORPC\_DBG\_ALL structure</span></span>

<span data-ttu-id="1ee2c-106">A estrutura **ORPC \_ DBG \_ All** é usada para passar parâmetros para os métodos da interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee2c-106">The **ORPC\_DBG\_ALL** structure is used to pass parameters to the methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

> [!Note]  
> <span data-ttu-id="1ee2c-107">Cada método da interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) usa uma combinação diferente dos membros abaixo.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-107">Each method of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface uses a different combination of the members below.</span></span> <span data-ttu-id="1ee2c-108">Se um membro não for indicado como usado por um método, ele será indefinido quando passado para esse método.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-108">If a member is not indicated as used by a method, it is undefined when passed to that method.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1ee2c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ee2c-109">Syntax</span></span>


```C++
typedef struct ORPC_DBG_ALL {
  BYTE              *pSignature;
  RPCOLEMESSAGE     *pMessage;
  const IID         *refiid;
  IRpcChannelBuffer *pChannel;
  IUnknown          *pUnkProxyMgr;
  void              *pInterface;
  IUnknown          *pUnkObject;
  HRESULT           hresult;
  void              *pvBuffer;
  ULONG             *cbBuffer;
  ULONG             *lpcbBuffer;
  void              *reserved;
} ORPC_DBG_ALL, *LPORPC_DBG_ALL;
```



## <a name="members"></a><span data-ttu-id="1ee2c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="1ee2c-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="1ee2c-111">**pSignature**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-111">**pSignature**</span></span>
</dt> <dd>

<span data-ttu-id="1ee2c-112">Um ponteiro para um buffer de **bytes** que contém:</span><span class="sxs-lookup"><span data-stu-id="1ee2c-112">A pointer to a **BYTE** buffer that contains:</span></span>

-   <span data-ttu-id="1ee2c-113">Primeiros quatro bytes: os caracteres ASCII "MARB" na ordem de memória crescente.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-113">First four bytes: the ASCII characters "MARB" in increasing memory order.</span></span>
-   <span data-ttu-id="1ee2c-114">Próximos 16 bytes: um **GUID** que identifica a notificação que está sendo chamada.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-114">Next 16 bytes: A **GUID** that identifies the notification being called.</span></span> <span data-ttu-id="1ee2c-115">Ele contém um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="1ee2c-115">It contains one of the following:</span></span>
    1.  <span data-ttu-id="1ee2c-116">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="1ee2c-116">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11</span></span>
    2.  <span data-ttu-id="1ee2c-117">[**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):D a45f3e0-9673-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="1ee2c-117">[**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):DA45F3E0-9673-101A-B07B-00DD01113F11</span></span>
    3.  <span data-ttu-id="1ee2c-118">[**ClientNotify**](iorpcdebugnotify-clientnotify.md): 4F60E540-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="1ee2c-118">[**ClientNotify**](iorpcdebugnotify-clientnotify.md):4F60E540-9674-101A-B07B-00DD01113F11</span></span>
    4.  <span data-ttu-id="1ee2c-119">[**ServerNotify**](iorpcdebugnotify-servernotify.md): 1084FA00-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="1ee2c-119">[**ServerNotify**](iorpcdebugnotify-servernotify.md):1084FA00-9674-101A-B07B-00DD01113F11</span></span>
    5.  <span data-ttu-id="1ee2c-120">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): 22080240-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="1ee2c-120">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md):22080240-9674-101A-B07B-00DD01113F11</span></span>
    6.  <span data-ttu-id="1ee2c-121">[**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md): 2FC09500-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="1ee2c-121">[**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md):2FC09500-9674-101A-B07B-00DD01113F11</span></span>
-   <span data-ttu-id="1ee2c-122">Próximos quatro bytes: reservados para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-122">Next four-bytes: Reserved for future use.</span></span>

> [!Note]
>
> <span data-ttu-id="1ee2c-123">Usado por todos os métodos da interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee2c-123">Used by all methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

</dd> <dt>

<span data-ttu-id="1ee2c-124">**pMessage**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-124">**pMessage**</span></span>
</dt> <dd>

<span data-ttu-id="1ee2c-125">Um ponteiro para uma estrutura [**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) que contém informações de Marshalling de dados RPC.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-125">A pointer to an [**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) structure that contains RPC data marshalling information.</span></span>

> [!Note]
>
> <span data-ttu-id="1ee2c-126">Usado pelos métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee2c-126">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="1ee2c-127">**refiid**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-127">**refiid**</span></span>
</dt> <dd>

<span data-ttu-id="1ee2c-128">Um ponteiro para o IID da interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee2c-128">A pointer to the IID of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

> [!Note]
>
> <span data-ttu-id="1ee2c-129">Usado pelos métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee2c-129">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="1ee2c-130">**pChannel**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-130">**pChannel**</span></span>
</dt> <dd>

<span data-ttu-id="1ee2c-131">Um ponteiro para a interface [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) da implementação do canal RPC com no servidor.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-131">A pointer to the [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) interface of the COM RPC channel implementation on the server.</span></span>

> [!Note]
>
> <span data-ttu-id="1ee2c-132">Usado pelos métodos [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee2c-132">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="1ee2c-133">**pUnkProxyMgr**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-133">**pUnkProxyMgr**</span></span>
</dt> <dd>

<span data-ttu-id="1ee2c-134">Um ponteiro para a interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) do objeto envolvido nesta invocação do depurador.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-134">A pointer to the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface of the object involved in this debugger invocation.</span></span> <span data-ttu-id="1ee2c-135">Pode ser **NULL**, no entanto, isso reduz a funcionalidade do depurador.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-135">May be **NULL**, however, this reduces debugger functionality.</span></span>

> [!Note]
>
> <span data-ttu-id="1ee2c-136">Usado pelos métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)e [**ClientNotify**](iorpcdebugnotify-clientnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee2c-136">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), and [**ClientNotify**](iorpcdebugnotify-clientnotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="1ee2c-137">**pInterface**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-137">**pInterface**</span></span>
</dt> <dd>

<span data-ttu-id="1ee2c-138">Um ponteiro para a interface COM do método que será invocado por esse RPC.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-138">A pointer to the COM interface of the method that will be invoked by this RPC.</span></span> <span data-ttu-id="1ee2c-139">Não deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-139">Must not be **NULL**.</span></span>

> [!Note]
>
> <span data-ttu-id="1ee2c-140">Usado pelos métodos [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee2c-140">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="1ee2c-141">**pUnkObject**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-141">**pUnkObject**</span></span>
</dt> <dd>

<span data-ttu-id="1ee2c-142">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-142">Must be **NULL**.</span></span>

> [!Note]
>
> <span data-ttu-id="1ee2c-143">Usado pelos métodos [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee2c-143">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="1ee2c-144">**resultado**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-144">**hresult**</span></span>
</dt> <dd>

<span data-ttu-id="1ee2c-145">A finalidade deste membro é alterada para cada uma das notificações abaixo:</span><span class="sxs-lookup"><span data-stu-id="1ee2c-145">This member's purpose changes for each of the notifications below:</span></span>

<span data-ttu-id="1ee2c-146">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): o número de bytes que o depurador do cliente transmitirá para o depurador do servidor.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-146">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): the number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="1ee2c-147">Se for zero, nenhuma informação precisará ser transmitida.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-147">If zero, no information need be transmitted.</span></span>

<span data-ttu-id="1ee2c-148">[**ClientNotify**](iorpcdebugnotify-clientnotify.md): o **HRESULT** do último RPC.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-148">[**ClientNotify**](iorpcdebugnotify-clientnotify.md): the **HRESULT** of the last RPC.</span></span>

<span data-ttu-id="1ee2c-149">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): o número de bytes que o depurador do cliente transmitirá para o depurador do servidor.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-149">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): the number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="1ee2c-150">Se for zero, nenhuma informação precisará ser transmitida.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-150">If zero, no information need be transmitted.</span></span>

> [!Note]
>
> <span data-ttu-id="1ee2c-151">Usado pelos métodos [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md)e [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee2c-151">Used by the [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), and [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="1ee2c-152">**pvBuffer**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-152">**pvBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="1ee2c-153">Um ponteiro para uma estrutura de [**\_ \_ buffer DBG ORPC**](orpc-dbg-buffer.md) que contém as informações de depuração marshalled RPC.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-153">A pointer to an [**ORPC\_DBG\_BUFFER**](orpc-dbg-buffer.md) structure that contains the RPC marshalled debug information.</span></span> <span data-ttu-id="1ee2c-154">Será indefinido se **cbBuffer** for zero.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-154">Is undefined if **cbBuffer** is zero.</span></span>

> [!Note]
>
> <span data-ttu-id="1ee2c-155">Usado pelos métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee2c-155">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="1ee2c-156">**cbBuffer**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-156">**cbBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="1ee2c-157">O comprimento, em bytes, dos dados apontados por **pvBuffer**.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-157">The length, in bytes, of the data pointed to by **pvBuffer**.</span></span>

> [!Note]
>
> <span data-ttu-id="1ee2c-158">Usado pelos métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee2c-158">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="1ee2c-159">**lpcbBuffer**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-159">**lpcbBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="1ee2c-160">O número de bytes que o depurador do cliente transmitirá para o depurador do servidor.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-160">The number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="1ee2c-161">Se for zero, nenhuma informação precisará ser transmitida.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-161">If zero, no information need be transmitted.</span></span> <span data-ttu-id="1ee2c-162">Esse valor substitui o valor retornado em **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-162">This value supersedes the value returned in **hresult**.</span></span>

> [!Note]
>
> <span data-ttu-id="1ee2c-163">Usado pelos métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee2c-163">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="1ee2c-164">**reservado**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-164">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="1ee2c-165">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-165">Reserved.</span></span> <span data-ttu-id="1ee2c-166">Não use.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-166">Do not use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ee2c-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ee2c-167">Requirements</span></span>



| <span data-ttu-id="1ee2c-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ee2c-168">Requirement</span></span> | <span data-ttu-id="1ee2c-169">Valor</span><span class="sxs-lookup"><span data-stu-id="1ee2c-169">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1ee2c-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ee2c-170">Minimum supported client</span></span><br/> | <span data-ttu-id="1ee2c-171">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ee2c-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="1ee2c-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ee2c-172">Minimum supported server</span></span><br/> | <span data-ttu-id="1ee2c-173">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ee2c-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1ee2c-174">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1ee2c-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ee2c-175"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="1ee2c-175"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ee2c-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ee2c-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee2c-177">**\_buffer de DBG ORPC \_**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-177">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="1ee2c-178">**\_argumentos de inicialização ORPC \_**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-178">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="1ee2c-179">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-179">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="1ee2c-180">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-180">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

