---
title: Estrutura de ORPC_DBG_BUFFER
description: A \_ estrutura de \_ buffer DBG ORPC é o formato de buffer usado para dados RPC empacotados para os métodos da interface IOrpcDebugNotify.
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- COM ORPC_DBG_BUFFER estrutura COM
- COM ponteiro de estrutura de PORPC_DBG_BUFFER COM
topic_type:
- apiref
api_name:
- ORPC_DBG_BUFFER
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc42251b928207a2b009a18c1d88e94dcf1492a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813323"
---
# <a name="orpc_dbg_buffer-structure"></a><span data-ttu-id="fd00d-105">\_Estrutura de \_ buffer DBG ORPC</span><span class="sxs-lookup"><span data-stu-id="fd00d-105">ORPC\_DBG\_BUFFER structure</span></span>

<span data-ttu-id="fd00d-106">A estrutura de **\_ \_ buffer DBG ORPC** é o formato de buffer usado para dados RPC empacotados para os métodos da interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="fd00d-106">The **ORPC\_DBG\_BUFFER** structure is the buffer format used to marshalled RPC data to the methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd00d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd00d-107">Syntax</span></span>


```C++
typedef struct _ORPC_DBG_BUFFER {
  DWORD alwaysOrSometimes;
  BYTE  verMajor;
  BYTE  verMinor;
  DWORD cbRemaining;
  GUID  guidSemantic;
  union {
    BOOL   fStopOnOtherSide;
    USHORT wDebuggingOpCode;
    USHORT cExtent;
    BYTE   padding[2];
    struct {
      ULONG cb;
      GUID  guidExtent;
      BYTE  *rgbData;
    };
  };
} ORPC_DBG_BUFFER, *PORPC_DBG_BUFFER;
```



## <a name="members"></a><span data-ttu-id="fd00d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="fd00d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fd00d-109">**alwaysOrSometimes**</span><span class="sxs-lookup"><span data-stu-id="fd00d-109">**alwaysOrSometimes**</span></span>
</dt> <dd>

<span data-ttu-id="fd00d-110">Um valor que controla a geração do depurador.</span><span class="sxs-lookup"><span data-stu-id="fd00d-110">A value that controls debugger spawning.</span></span> <span data-ttu-id="fd00d-111">**alwaysOrSometimes** pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="fd00d-111">**alwaysOrSometimes** can be one of the following values:</span></span>



| <span data-ttu-id="fd00d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="fd00d-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="fd00d-113">Significado</span><span class="sxs-lookup"><span data-stu-id="fd00d-113">Meaning</span></span>                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <span data-ttu-id="fd00d-114"><dt>**ORPC \_ Depurar \_ sempre**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="fd00d-114"><dt>**ORPC\_DEBUG\_ALWAYS**</dt> <dt>0x00000000</dt></span></span> </dl>                              | <span data-ttu-id="fd00d-115">Se definido, COM sempre gerará a notificação de cliente ou servidor no receptor.</span><span class="sxs-lookup"><span data-stu-id="fd00d-115">If set, COM will always raise the client or server notification on the receiver.</span></span><br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <span data-ttu-id="fd00d-116"><dt>**ORPC \_ Depurar \_ se o \_ gancho estiver \_ habilitado**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="fd00d-116"><dt>**ORPC\_DEBUG\_IF\_HOOK\_ENABLED**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="fd00d-117">Se definido, COM irá gerar apenas a notificação de cliente ou servidor no receptor se a depuração COM tiver sido habilitada chamando [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) nesse processo com **FTrace** definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="fd00d-117">If set, COM will only raise the client or server notification on the receiver if COM debugging has been enabled by calling [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) in that process with **fTrace** set to **TRUE**.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="fd00d-118">**verMajor**</span><span class="sxs-lookup"><span data-stu-id="fd00d-118">**verMajor**</span></span>
</dt> <dd>

<span data-ttu-id="fd00d-119">O número de versão principal da especificação de formato de dados.</span><span class="sxs-lookup"><span data-stu-id="fd00d-119">The major version number of the data format specification.</span></span>

</dd> <dt>

<span data-ttu-id="fd00d-120">**verMinor**</span><span class="sxs-lookup"><span data-stu-id="fd00d-120">**verMinor**</span></span>
</dt> <dd>

<span data-ttu-id="fd00d-121">O número de versão secundária da especificação de formato de dados.</span><span class="sxs-lookup"><span data-stu-id="fd00d-121">The minor version number of the data format specification.</span></span>

</dd> <dt>

<span data-ttu-id="fd00d-122">**cbRemaining**</span><span class="sxs-lookup"><span data-stu-id="fd00d-122">**cbRemaining**</span></span>
</dt> <dd>

<span data-ttu-id="fd00d-123">O número de bytes, inclusive de **cbRemaining**, que seguem nessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="fd00d-123">The number of bytes, inclusive of **cbRemaining**, that follow in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="fd00d-124">**guidSemantic**</span><span class="sxs-lookup"><span data-stu-id="fd00d-124">**guidSemantic**</span></span>
</dt> <dd>

<span data-ttu-id="fd00d-125">Um GUID que determina quais membros da União estão presentes abaixo.</span><span class="sxs-lookup"><span data-stu-id="fd00d-125">A GUID that determines which members of the union are present below.</span></span> <span data-ttu-id="fd00d-126">**guidSemantic** pode usar um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="fd00d-126">**guidSemantic** can take one of the following values:</span></span>



| <span data-ttu-id="fd00d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="fd00d-127">Value</span></span>                                                                                                           | <span data-ttu-id="fd00d-128">Significado</span><span class="sxs-lookup"><span data-stu-id="fd00d-128">Meaning</span></span>                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd00d-129"><dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt></span><span class="sxs-lookup"><span data-stu-id="fd00d-129"><dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt></span></span> </dl> | <span data-ttu-id="fd00d-130">Determina se a depuração única deve ser executada pelo depurador.</span><span class="sxs-lookup"><span data-stu-id="fd00d-130">Determines if single stepping is to be performed by the debugger.</span></span> <span data-ttu-id="fd00d-131">Somente o membro **fStopOnOtherSide** da União está presente abaixo.</span><span class="sxs-lookup"><span data-stu-id="fd00d-131">Only the **fStopOnOtherSide** member of the union is present below.</span></span><br/>                                             |
| <dl> <span data-ttu-id="fd00d-132"><dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt></span><span class="sxs-lookup"><span data-stu-id="fd00d-132"><dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt></span></span> </dl> | <span data-ttu-id="fd00d-133">Determina se os dados marshalled de RPC e os opcodes de depuração são passados para o receptor.</span><span class="sxs-lookup"><span data-stu-id="fd00d-133">Determines if RPC marshalled data and debugging opcodes are passed to the receiver.</span></span> <span data-ttu-id="fd00d-134">Todos os membros da União estão presentes abaixo, com exceção de **fStopOnOtherSide**.</span><span class="sxs-lookup"><span data-stu-id="fd00d-134">All of the members of the union are present below with the exception of **fStopOnOtherSide**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fd00d-135">**fStopOnOtherSide**</span><span class="sxs-lookup"><span data-stu-id="fd00d-135">**fStopOnOtherSide**</span></span>
</dt> <dd>

<span data-ttu-id="fd00d-136">Se for **true**, a depuração única será executada pelo depurador e ele deverá sair do servidor e continuar a execução quando o outro lado for atingido.</span><span class="sxs-lookup"><span data-stu-id="fd00d-136">If **TRUE**, single stepping is performed by the debugger and it should step out of the server and continue execution once the other side is reached.</span></span> <span data-ttu-id="fd00d-137">Caso contrário, a depuração única não será executada e a execução do depurador será interrompida no outro lado.</span><span class="sxs-lookup"><span data-stu-id="fd00d-137">Otherwise, single stepping is not performed and debugger execution stops on the other side.</span></span>

</dd> <dt>

<span data-ttu-id="fd00d-138">**wDebuggingOpCode**</span><span class="sxs-lookup"><span data-stu-id="fd00d-138">**wDebuggingOpCode**</span></span>
</dt> <dd>

<span data-ttu-id="fd00d-139">Um valor que permite a especificação de uma série de operações.</span><span class="sxs-lookup"><span data-stu-id="fd00d-139">A value that allows for one of a series of operations to be specified.</span></span> <span data-ttu-id="fd00d-140">**wDebuggingOpCode** pode usar um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="fd00d-140">**wDebuggingOpCode** can take one of the following values:</span></span>



| <span data-ttu-id="fd00d-141">Valor</span><span class="sxs-lookup"><span data-stu-id="fd00d-141">Value</span></span>                                                                             | <span data-ttu-id="fd00d-142">Significado</span><span class="sxs-lookup"><span data-stu-id="fd00d-142">Meaning</span></span>                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd00d-143"><dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="fd00d-143"><dt>0x0000</dt></span></span> </dl> | <span data-ttu-id="fd00d-144">Sem operação.</span><span class="sxs-lookup"><span data-stu-id="fd00d-144">No operation.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="fd00d-145"><dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="fd00d-145"><dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="fd00d-146">Se definido, a semântica de etapa única será idêntica a **fStopOnOtherSide** quando definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="fd00d-146">If set, single step semantics are identical to **fStopOnOtherSide** when set to **TRUE**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fd00d-147">**cExtent**</span><span class="sxs-lookup"><span data-stu-id="fd00d-147">**cExtent**</span></span>
</dt> <dd>

<span data-ttu-id="fd00d-148">Margem.</span><span class="sxs-lookup"><span data-stu-id="fd00d-148">Padding.</span></span> <span data-ttu-id="fd00d-149">Não use.</span><span class="sxs-lookup"><span data-stu-id="fd00d-149">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="fd00d-150">**padding**</span><span class="sxs-lookup"><span data-stu-id="fd00d-150">**padding**</span></span>
</dt> <dd>

<span data-ttu-id="fd00d-151">Margem.</span><span class="sxs-lookup"><span data-stu-id="fd00d-151">Padding.</span></span> <span data-ttu-id="fd00d-152">Não use.</span><span class="sxs-lookup"><span data-stu-id="fd00d-152">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="fd00d-153">**CB**</span><span class="sxs-lookup"><span data-stu-id="fd00d-153">**cb**</span></span>
</dt> <dd>

<span data-ttu-id="fd00d-154">O tamanho, em bytes, dos dados em **rgbData**.</span><span class="sxs-lookup"><span data-stu-id="fd00d-154">The size, in bytes of the data in **rgbData**.</span></span>

</dd> <dt>

<span data-ttu-id="fd00d-155">**guidExtent**</span><span class="sxs-lookup"><span data-stu-id="fd00d-155">**guidExtent**</span></span>
</dt> <dd>

<span data-ttu-id="fd00d-156">Um **GUID** que determina o tipo de dados em **rgbData**.</span><span class="sxs-lookup"><span data-stu-id="fd00d-156">A **GUID** that determines the type of data in **rgbData**.</span></span> <span data-ttu-id="fd00d-157">**guidExtent** pode usar um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="fd00d-157">**guidExtent** can take one of the following values:</span></span>



| <span data-ttu-id="fd00d-158">Valor</span><span class="sxs-lookup"><span data-stu-id="fd00d-158">Value</span></span>                                                                                                           | <span data-ttu-id="fd00d-159">Significado</span><span class="sxs-lookup"><span data-stu-id="fd00d-159">Meaning</span></span>                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="fd00d-160"><dt>53199051-57EB-11ce-A964-00AA006C3706</dt></span><span class="sxs-lookup"><span data-stu-id="fd00d-160"><dt>53199051-57EB-11ce-A964-00AA006C3706</dt></span></span> </dl> | <span data-ttu-id="fd00d-161">**rgbData** é um ponteiro de interface marshalled.</span><span class="sxs-lookup"><span data-stu-id="fd00d-161">**rgbData** is a marshalled interface pointer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fd00d-162">**rgbData**</span><span class="sxs-lookup"><span data-stu-id="fd00d-162">**rgbData**</span></span>
</dt> <dd>

<span data-ttu-id="fd00d-163">Um buffer de **bytes** usado para passar dados com marshalled de RPC entre os depuradores de cliente e de servidor.</span><span class="sxs-lookup"><span data-stu-id="fd00d-163">A **BYTE** buffer used to pass RPC marshalled COM data between the client and server debuggers.</span></span> <span data-ttu-id="fd00d-164">O conteúdo de **rgbData** é determinado pelo **GUID** em **guidExtent**.</span><span class="sxs-lookup"><span data-stu-id="fd00d-164">The contents of **rgbData** are determined by the **GUID** in **guidExtent**.</span></span>



| <span data-ttu-id="fd00d-165">Valor de guidExtent</span><span class="sxs-lookup"><span data-stu-id="fd00d-165">guidExtent Value</span></span>                     | <span data-ttu-id="fd00d-166">conteúdo do rgbData</span><span class="sxs-lookup"><span data-stu-id="fd00d-166">rgbData contents</span></span>                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd00d-167">53199051-57EB-11ce-A964-00AA006C3706</span><span class="sxs-lookup"><span data-stu-id="fd00d-167">53199051-57EB-11ce-A964-00AA006C3706</span></span> | <span data-ttu-id="fd00d-168">Um ponteiro de interface marshalled que resulta da chamada de [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="fd00d-168">A marshalled interface pointer that results from calling [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface).</span></span> <span data-ttu-id="fd00d-169">O ponteiro marshalled é convertido em seu ponteiro de interface correspondente usando [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="fd00d-169">The marshalled pointer is converted into its corresponding interface pointer using [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd00d-170">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd00d-170">Remarks</span></span>

<span data-ttu-id="fd00d-171">Esses membros dessa estrutura têm um alinhamento de 1 byte e sempre são transmitidos em ordem de byte little-endian.</span><span class="sxs-lookup"><span data-stu-id="fd00d-171">This members of this structure have 1-byte alignment and are always transmitted in little-endian byte order.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd00d-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd00d-172">Requirements</span></span>



| <span data-ttu-id="fd00d-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd00d-173">Requirement</span></span> | <span data-ttu-id="fd00d-174">Valor</span><span class="sxs-lookup"><span data-stu-id="fd00d-174">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="fd00d-175">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd00d-175">Minimum supported client</span></span><br/> | <span data-ttu-id="fd00d-176">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fd00d-176">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="fd00d-177">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd00d-177">Minimum supported server</span></span><br/> | <span data-ttu-id="fd00d-178">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fd00d-178">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fd00d-179">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fd00d-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd00d-180"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="fd00d-180"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd00d-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd00d-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd00d-182">**ORPC \_ DBG \_ All**</span><span class="sxs-lookup"><span data-stu-id="fd00d-182">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="fd00d-183">**\_argumentos de inicialização ORPC \_**</span><span class="sxs-lookup"><span data-stu-id="fd00d-183">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="fd00d-184">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="fd00d-184">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="fd00d-185">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="fd00d-185">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





