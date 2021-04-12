---
description: Localiza o próximo quadro no contexto de captura atual que corresponde ao filtro.
ms.assetid: cc99b4a0-b6b0-43b4-8121-0e402d024009
title: Função FindNextFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2e303f7f9031ad451ad19be8bc8cbcd3abae3f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501355"
---
# <a name="findnextframe-function"></a><span data-ttu-id="6cd27-103">Função FindNextFrame</span><span class="sxs-lookup"><span data-stu-id="6cd27-103">FindNextFrame function</span></span>

<span data-ttu-id="6cd27-104">A função **FindNextFrame** localiza o próximo quadro no contexto de captura atual que corresponde ao filtro.</span><span class="sxs-lookup"><span data-stu-id="6cd27-104">The **FindNextFrame** function finds the next frame in the current capture context that matches the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd27-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cd27-105">Syntax</span></span>


```C++
HFRAME WINAPI FindNextFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     HighestFrame
);
```



## <a name="parameters"></a><span data-ttu-id="6cd27-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cd27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cd27-107">*hCurrentFrame*</span><span class="sxs-lookup"><span data-stu-id="6cd27-107">*hCurrentFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="6cd27-108">Um identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="6cd27-108">A handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="6cd27-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="6cd27-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="6cd27-110">O nome do protocolo, como TCP.</span><span class="sxs-lookup"><span data-stu-id="6cd27-110">The protocol name, such as TCP.</span></span>

</dd> <dt>

<span data-ttu-id="6cd27-111">*DestinationAddress*</span><span class="sxs-lookup"><span data-stu-id="6cd27-111">*DestinationAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="6cd27-112">O endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="6cd27-112">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="6cd27-113">*SourceAddress*</span><span class="sxs-lookup"><span data-stu-id="6cd27-113">*SourceAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="6cd27-114">O endereço de origem.</span><span class="sxs-lookup"><span data-stu-id="6cd27-114">The source address.</span></span>

</dd> <dt>

<span data-ttu-id="6cd27-115">*ProtocolOffset*</span><span class="sxs-lookup"><span data-stu-id="6cd27-115">*ProtocolOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="6cd27-116">Um ponteiro para uma **palavra** que receberá o deslocamento do protocolo.</span><span class="sxs-lookup"><span data-stu-id="6cd27-116">A pointer to a **WORD** that will receive the protocol offset.</span></span>

</dd> <dt>

<span data-ttu-id="6cd27-117">*OriginalFrameNumber*</span><span class="sxs-lookup"><span data-stu-id="6cd27-117">*OriginalFrameNumber*</span></span> 
</dt> <dd>

<span data-ttu-id="6cd27-118">O ponto de partida da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6cd27-118">The starting point of the search.</span></span> <span data-ttu-id="6cd27-119">Por padrão, essa função pesquisa em frente a 1.000 quadros do ponto de partida *OriginalFrameNumber* .</span><span class="sxs-lookup"><span data-stu-id="6cd27-119">By default, this function searches forward 1,000 frames from the *OriginalFrameNumber* starting point.</span></span> <span data-ttu-id="6cd27-120">Para alterar a distância de encaminhamento da pesquisa, adicione essa linha ao arquivo de Nmapi.ini, localizado no \\ diretório monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="6cd27-120">To change the search-forward distance, add this line to the Nmapi.ini file, located in the \\Network Monitor directory.</span></span>

<span data-ttu-id="6cd27-121">MAXLOOKBACK =<new lookforward distance></span><span class="sxs-lookup"><span data-stu-id="6cd27-121">MAXLOOKBACK=<new lookforward distance></span></span>

</dd> <dt>

<span data-ttu-id="6cd27-122">*HighestFrame*</span><span class="sxs-lookup"><span data-stu-id="6cd27-122">*HighestFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="6cd27-123">O número de quadro mais alto na captura que é pesquisada.</span><span class="sxs-lookup"><span data-stu-id="6cd27-123">The highest frame number in the capture that is searched.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cd27-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6cd27-124">Return value</span></span>

<span data-ttu-id="6cd27-125">Se a função for bem-sucedida, o valor de retorno será um identificador para o próximo quadro.</span><span class="sxs-lookup"><span data-stu-id="6cd27-125">If the function is successful, the return value is a handle to the next frame.</span></span>

<span data-ttu-id="6cd27-126">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6cd27-126">If the function is not successful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cd27-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cd27-127">Remarks</span></span>

<span data-ttu-id="6cd27-128">O filtro de captura é definido principalmente pelo parâmetro *ProtocolName* , que é a única entrada de filtro necessária; Você pode adicionar dados *DestinationAddress* e *SourceAddress* para aumentar a velocidade de captura.</span><span class="sxs-lookup"><span data-stu-id="6cd27-128">The capture filter is defined primarily by the *ProtocolName* parameter, which is the only required filter input; you can add *DestinationAddress* and *SourceAddress* data to increase the capture speed.</span></span>

<span data-ttu-id="6cd27-129">O ponteiro *ProtocolOffset* é retornado para o analisador de chamada, que adiciona a **palavra** ao ponteiro retornado bloqueando o quadro (com [ParserTemporaryLockFrame](parsertemporarylockframe.md)) para obter o **LPBYTE** do protocolo procurado.</span><span class="sxs-lookup"><span data-stu-id="6cd27-129">The *ProtocolOffset* pointer is returned to the calling parser, which adds the **WORD** to the pointer returned by locking the frame (with [ParserTemporaryLockFrame](parsertemporarylockframe.md)) to get the **LPBYTE** of the protocol searched for.</span></span> <span data-ttu-id="6cd27-130">No retorno, o HFRAME que passou pelo filtro é fornecido ao analisador.</span><span class="sxs-lookup"><span data-stu-id="6cd27-130">On return, the HFRAME that passed the filter is given to the parser.</span></span> <span data-ttu-id="6cd27-131">Se o analisador descobrir que esse quadro não é o procurado, o analisador poderá entregar o HFRAME de volta à função **FindNextFrame** para obter o próximo quadro.</span><span class="sxs-lookup"><span data-stu-id="6cd27-131">If the parser finds that this frame is not the one sought, the parser can hand the HFRAME back to the **FindNextFrame** function to get the next frame.</span></span> <span data-ttu-id="6cd27-132">Os endereços de origem e destino não são necessários e podem ser passados como **nulos**.</span><span class="sxs-lookup"><span data-stu-id="6cd27-132">The source and destination addresses are not required and can be passed as **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cd27-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cd27-133">Requirements</span></span>



| <span data-ttu-id="6cd27-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cd27-134">Requirement</span></span> | <span data-ttu-id="6cd27-135">Valor</span><span class="sxs-lookup"><span data-stu-id="6cd27-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd27-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cd27-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6cd27-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6cd27-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6cd27-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cd27-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6cd27-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6cd27-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6cd27-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6cd27-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cd27-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cd27-141"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="6cd27-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6cd27-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="6cd27-143"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6cd27-143"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="6cd27-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6cd27-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cd27-145"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cd27-145"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




