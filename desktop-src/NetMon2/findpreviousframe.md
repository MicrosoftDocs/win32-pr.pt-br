---
description: A função FindPreviousFrame localiza o quadro anterior no contexto de captura atual que corresponde ao filtro.
ms.assetid: 16c5b981-a9f4-41e5-bb97-2caa3e9d8512
title: Função FindPreviousFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPreviousFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: deabf10702ca41c23101c5f60c9459e094e567fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920706"
---
# <a name="findpreviousframe-function"></a><span data-ttu-id="cd24a-103">Função FindPreviousFrame</span><span class="sxs-lookup"><span data-stu-id="cd24a-103">FindPreviousFrame function</span></span>

<span data-ttu-id="cd24a-104">A função **FindPreviousFrame** localiza o quadro anterior no contexto de captura atual que corresponde ao filtro.</span><span class="sxs-lookup"><span data-stu-id="cd24a-104">The **FindPreviousFrame** function finds the previous frame in the current capture context that matches the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd24a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd24a-105">Syntax</span></span>


```C++
HFRAME WINAPI FindPreviousFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     LowestFrame
);
```



## <a name="parameters"></a><span data-ttu-id="cd24a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd24a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd24a-107">*hCurrentFrame*</span><span class="sxs-lookup"><span data-stu-id="cd24a-107">*hCurrentFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="cd24a-108">Identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="cd24a-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="cd24a-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="cd24a-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="cd24a-110">Nome do protocolo, como TCP.</span><span class="sxs-lookup"><span data-stu-id="cd24a-110">Protocol name, such as TCP.</span></span>

</dd> <dt>

<span data-ttu-id="cd24a-111">*DestinationAddress*</span><span class="sxs-lookup"><span data-stu-id="cd24a-111">*DestinationAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="cd24a-112">Endereço de destino do quadro procurado.</span><span class="sxs-lookup"><span data-stu-id="cd24a-112">Destination address of the frame that is searched for.</span></span>

</dd> <dt>

<span data-ttu-id="cd24a-113">*SourceAddress*</span><span class="sxs-lookup"><span data-stu-id="cd24a-113">*SourceAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="cd24a-114">Endereço de origem do quadro procurado.</span><span class="sxs-lookup"><span data-stu-id="cd24a-114">Source address of the frame that is searched for.</span></span>

</dd> <dt>

<span data-ttu-id="cd24a-115">*ProtocolOffset*</span><span class="sxs-lookup"><span data-stu-id="cd24a-115">*ProtocolOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="cd24a-116">Ponteiro para uma **palavra** que recebe o deslocamento do protocolo.</span><span class="sxs-lookup"><span data-stu-id="cd24a-116">Pointer to a **WORD** that receives the protocol offset.</span></span>

</dd> <dt>

<span data-ttu-id="cd24a-117">*OriginalFrameNumber*</span><span class="sxs-lookup"><span data-stu-id="cd24a-117">*OriginalFrameNumber*</span></span> 
</dt> <dd>

<span data-ttu-id="cd24a-118">Ponto de partida da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="cd24a-118">Starting point of the search.</span></span> <span data-ttu-id="cd24a-119">Por padrão, essa função pesquisa quadros de 1.000 anteriores do ponto de partida *OriginalFrameNumber* .</span><span class="sxs-lookup"><span data-stu-id="cd24a-119">By default, this function searches backward 1,000 frames from *OriginalFrameNumber* starting point.</span></span> <span data-ttu-id="cd24a-120">Você pode alterar a distância de pesquisa adicionando essa linha ao arquivo de Nmapi.ini, que está localizado no \\ diretório monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="cd24a-120">You can change the search-back distance by adding this line to the Nmapi.ini file, which is located in the \\Network Monitor directory.</span></span>

<span data-ttu-id="cd24a-121">MAXLOOKBACK =<new lookback distance></span><span class="sxs-lookup"><span data-stu-id="cd24a-121">MAXLOOKBACK=<new lookback distance></span></span>

</dd> <dt>

<span data-ttu-id="cd24a-122">*LowestFrame*</span><span class="sxs-lookup"><span data-stu-id="cd24a-122">*LowestFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="cd24a-123">O número de quadro mais baixo na captura que é pesquisada.</span><span class="sxs-lookup"><span data-stu-id="cd24a-123">Lowest frame number in the capture that is searched.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd24a-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd24a-124">Return value</span></span>

<span data-ttu-id="cd24a-125">Se a função for bem-sucedida, o valor de retorno será um identificador para o quadro anterior.</span><span class="sxs-lookup"><span data-stu-id="cd24a-125">If the function is successful, the return value is a handle to the previous frame.</span></span>

<span data-ttu-id="cd24a-126">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="cd24a-126">If the function is not successful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd24a-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd24a-127">Remarks</span></span>

<span data-ttu-id="cd24a-128">O filtro de captura é definido principalmente por *ProtocolName*, que é a única entrada de filtro necessária; Você pode adicionar informações de *DestinationAddress* e *SourceAddress* para aumentar a velocidade de captura.</span><span class="sxs-lookup"><span data-stu-id="cd24a-128">The capture filter is defined primarily by *ProtocolName*, which is the only required filter input; you can add *DestinationAddress* and *SourceAddress* information to increase the capture speed.</span></span>

<span data-ttu-id="cd24a-129">*ProtocolOffset* é retornado para o analisador de chamada, que adiciona esse **DWORD** ao ponteiro retornado bloqueando o quadro (com [PARSERTEMPORARYLOCKFRAME](parsertemporarylockframe.md)) para obter o LPBYTE do protocolo que está sendo pesquisado.</span><span class="sxs-lookup"><span data-stu-id="cd24a-129">*ProtocolOffset* is returned to the calling parser, which adds this **DWORD** to the pointer returned by locking the frame (with [ParserTemporaryLockFrame](parsertemporarylockframe.md)) to get the LPBYTE of the protocol that is being searched for.</span></span> <span data-ttu-id="cd24a-130">No retorno, o HFRAME que passou pelo filtro é fornecido ao analisador.</span><span class="sxs-lookup"><span data-stu-id="cd24a-130">On return, the HFRAME that passed the filter is given to the parser.</span></span> <span data-ttu-id="cd24a-131">Se o analisador descobrir que o quadro não é aquele que está sendo procurado, o analisador poderá entregar esse HFRAME de volta à função **FindPreviousFrame** para recuperar o próximo quadro.</span><span class="sxs-lookup"><span data-stu-id="cd24a-131">If the parser finds that the frame is not the one that is being sought, the parser can hand this HFRAME back to the **FindPreviousFrame** function to retrieve the next frame.</span></span> <span data-ttu-id="cd24a-132">Os endereços de origem e de destino, que não são necessários, podem ser passados como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cd24a-132">The source and destination addresses, which are not required, can be passed in as **NULL**.</span></span> <span data-ttu-id="cd24a-133">Quando usado, esses endereços podem ser do tipo endereço \_ \_ IP, e assim por diante, não apenas tipos de Mac.</span><span class="sxs-lookup"><span data-stu-id="cd24a-133">When used, these addresses can be of type ADDRESS\_TYPE\_IP, and so on, not just MAC types.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd24a-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd24a-134">Requirements</span></span>



| <span data-ttu-id="cd24a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd24a-135">Requirement</span></span> | <span data-ttu-id="cd24a-136">Valor</span><span class="sxs-lookup"><span data-stu-id="cd24a-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cd24a-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd24a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="cd24a-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cd24a-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cd24a-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd24a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="cd24a-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cd24a-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cd24a-141">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cd24a-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd24a-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd24a-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="cd24a-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cd24a-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="cd24a-144"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd24a-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="cd24a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="cd24a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd24a-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd24a-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




