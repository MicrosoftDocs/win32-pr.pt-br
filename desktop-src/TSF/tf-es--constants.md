---
title: Constantes de TF_ES_ (msctf. h)
description: A seguir estão as constantes usadas pelo método ITfContext RequestEditSession.
ms.assetid: 5498329f-3302-4f66-bdec-cab7db0cdc0e
topic_type:
- apiref
api_name:
- TF_ES_ASYNCDONTCARE
- TF_ES_SYNC
- TF_ES_READ
- TF_ES_READWRITE
- TF_ES_ASYNC
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ed96adc1d6f6d66671e91f7a70bce856663e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760349"
---
# <a name="tf_es_-constants"></a><span data-ttu-id="19113-103">Constantes de TF \_ es \_ \*</span><span class="sxs-lookup"><span data-stu-id="19113-103">TF\_ES\_\* Constants</span></span>

<span data-ttu-id="19113-104">Veja a seguir as constantes usadas pelo método [ITfContext:: RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) .</span><span class="sxs-lookup"><span data-stu-id="19113-104">The following are constants used by the [ITfContext::RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) method.</span></span>



| <span data-ttu-id="19113-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="19113-105">Constant/value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="19113-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="19113-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                             |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_ES_ASYNCDONTCARE"></span><span id="tf_es_asyncdontcare"></span><dl> <span data-ttu-id="19113-107"><dt>**TF \_ ES \_ ASYNCDONTCARE**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="19113-107"><dt>**TF\_ES\_ASYNCDONTCARE**</dt> <dt>( 0 )</dt></span></span> </dl> | <span data-ttu-id="19113-108">A sessão de edição pode ocorrer de forma síncrona ou assíncrona, a critério do gerente.</span><span class="sxs-lookup"><span data-stu-id="19113-108">The edit session can occur synchronously or asynchronously, at the discretion of the manager.</span></span> <span data-ttu-id="19113-109">O gerente tentará agendar uma sessão de edição síncrona para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="19113-109">The manager will attempt to schedule a synchronous edit session for improved performance.</span></span> <span data-ttu-id="19113-110">Esse valor não pode ser combinado com os \_ valores de sincronização de TF es \_ Async ou TF \_ es \_ .</span><span class="sxs-lookup"><span data-stu-id="19113-110">This value cannot be combined with the TF\_ES\_ASYNC or TF\_ES\_SYNC values.</span></span><br/>                                                                         |
| <span id="TF_ES_SYNC"></span><span id="tf_es_sync"></span><dl> <span data-ttu-id="19113-111"><dt>**TF \_ ES \_ sincronização**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="19113-111"><dt>**TF\_ES\_SYNC**</dt> <dt>( 0x1 )</dt></span></span> </dl>                          | <span data-ttu-id="19113-112">A sessão de edição deve ser síncrona, ou a solicitação falhará (com TF \_ E \_ síncrona).</span><span class="sxs-lookup"><span data-stu-id="19113-112">The edit session must be synchronous or the request will fail (with TF\_E\_SYNCHRONOUS).</span></span> <span data-ttu-id="19113-113">Esse sinalizador só deve ser usado em situações documentadas (como tratamento de pressionamentos de teclas), em que pode ser esperado ter sucesso.</span><span class="sxs-lookup"><span data-stu-id="19113-113">This flag should only be used in documented situations (such as keystroke handling) where it can be expected to succeed.</span></span> <span data-ttu-id="19113-114">Caso contrário, a chamada provavelmente falhará.</span><span class="sxs-lookup"><span data-stu-id="19113-114">Otherwise the call will likely fail.</span></span> <span data-ttu-id="19113-115">Esse valor não pode ser combinado com os \_ \_ valores assíncronos de TF es ASYNCDONTCARE ou TF \_ es \_ .</span><span class="sxs-lookup"><span data-stu-id="19113-115">This value cannot be combined with the TF\_ES\_ASYNCDONTCARE or TF\_ES\_ASYNC values.</span></span><br/> |
| <span id="TF_ES_READ"></span><span id="tf_es_read"></span><dl> <span data-ttu-id="19113-116"><dt>**TF \_ ES \_ leitura**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="19113-116"><dt>**TF\_ES\_READ**</dt> <dt>( 0x2 )</dt></span></span> </dl>                          | <span data-ttu-id="19113-117">Solicita acesso somente leitura ao contexto.</span><span class="sxs-lookup"><span data-stu-id="19113-117">Requests read-only access to the context.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="TF_ES_READWRITE"></span><span id="tf_es_readwrite"></span><dl> <span data-ttu-id="19113-118"><dt>**TF \_ ES \_ ReadWrite**</dt> <dt>(0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="19113-118"><dt>**TF\_ES\_READWRITE**</dt> <dt>( 0x6 )</dt></span></span> </dl>           | <span data-ttu-id="19113-119">Solicita acesso de leitura/gravação ao contexto.</span><span class="sxs-lookup"><span data-stu-id="19113-119">Requests read/write access to the context.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span id="TF_ES_ASYNC"></span><span id="tf_es_async"></span><dl> <span data-ttu-id="19113-120"><dt>**TF \_ S \_ Async**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="19113-120"><dt>**TF\_ES\_ASYNC**</dt> <dt>( 0x8 )</dt></span></span> </dl>                       | <span data-ttu-id="19113-121">A sessão de edição deve ser assíncrona ou a solicitação falhará.</span><span class="sxs-lookup"><span data-stu-id="19113-121">The edit session must be asynchronous or the request will fail.</span></span> <span data-ttu-id="19113-122">Esse valor não pode ser combinado com os \_ valores de sincronização TF es \_ ASYNCDONTCARE ou TF \_ es \_ .</span><span class="sxs-lookup"><span data-stu-id="19113-122">This value cannot be combined with the TF\_ES\_ASYNCDONTCARE or TF\_ES\_SYNC values.</span></span><br/>                                                                                                                                                                                         |



## <a name="requirements"></a><span data-ttu-id="19113-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19113-123">Requirements</span></span>



| <span data-ttu-id="19113-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="19113-124">Requirement</span></span> | <span data-ttu-id="19113-125">Valor</span><span class="sxs-lookup"><span data-stu-id="19113-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="19113-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19113-126">Minimum supported client</span></span><br/> | <span data-ttu-id="19113-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="19113-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="19113-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19113-128">Minimum supported server</span></span><br/> | <span data-ttu-id="19113-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="19113-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="19113-130">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="19113-130">Redistributable</span></span><br/>          | <span data-ttu-id="19113-131">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="19113-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="19113-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19113-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="19113-133"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="19113-133"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="19113-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="19113-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19113-135"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="19113-135"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19113-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="19113-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19113-137">ITfContext:: RequestEditSession</span><span class="sxs-lookup"><span data-stu-id="19113-137">ITfContext::RequestEditSession</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession)
</dt> </dl>

 

 





