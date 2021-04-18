---
description: A função de exportação RecognizeFrame indica se um dado é reconhecido como o protocolo que o analisador detecta. A função de exportação RecognizeFrame deve ser implementada para cada analisador compatível com a DLL do analisador.
ms.assetid: 3f835f58-b011-4329-b9b2-ff865a1f0ae5
title: Função de retorno de chamada RecognizeFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizeFrame
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: e2660629cecfa279377794749714102077fb6979
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766247"
---
# <a name="recognizeframe-callback-function"></a><span data-ttu-id="ac0ed-104">Função de retorno de chamada RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="ac0ed-104">RecognizeFrame callback function</span></span>

<span data-ttu-id="ac0ed-105">A função de exportação **RecognizeFrame** indica se um dado é reconhecido como o protocolo que o analisador detecta.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-105">The **RecognizeFrame** export function indicates whether a piece of data is recognized as the protocol that the parser detects.</span></span> <span data-ttu-id="ac0ed-106">A função de exportação **RecognizeFrame** deve ser implementada para cada analisador compatível com a DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-106">The **RecognizeFrame** export function must be implemented for each parser that the parser DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac0ed-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac0ed-107">Syntax</span></span>


```C++
LPBYTE RecognizeFrame(
  _In_    HFRAME      hFrame,
  _In_    LPBYTE      lpFrame,
  _In_    LPBYTE      lpProtocol,
  _In_    DWORD       MacType,
  _In_    DWORD       BytesLeft,
  _In_    HPROTOCOL   hPreviousProtocol,
  _In_    DWORD       nPreviousProtocolOffset,
  _Out_   LPDWORD     ProtocolStatusCode,
  _Out_   LPHPROTOCOL phNextProtocol,
  _Inout_ PDWORD_PTR  lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="ac0ed-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac0ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac0ed-109">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac0ed-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac0ed-110">Identificador para o quadro que contém os dados.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-110">Handle to the frame that contains the data.</span></span>

</dd> <dt>

<span data-ttu-id="ac0ed-111">*lpFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac0ed-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac0ed-112">Ponteiro para o primeiro byte de um quadro.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-112">Pointer to the first byte of a frame.</span></span> <span data-ttu-id="ac0ed-113">O ponteiro fornece uma maneira de exibir os dados que outros analisadores reconhecem.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-113">The pointer provides a way to view data that other parsers recognize.</span></span>

</dd> <dt>

<span data-ttu-id="ac0ed-114">*lpProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac0ed-114">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac0ed-115">Ponteiro para o início dos dados não reivindicados.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-115">Pointer to the start of the unclaimed data.</span></span> <span data-ttu-id="ac0ed-116">Normalmente, os dados não reivindicados estão localizados no meio de um quadro porque um analisador anterior declarou dados antes desse analisador.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-116">Typically, the unclaimed data is located in the middle of a frame because a previous parser has claimed data before this parser.</span></span> <span data-ttu-id="ac0ed-117">O analisador deve testar os dados não reivindicados primeiro.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-117">The parser must test the unclaimed data first.</span></span>

</dd> <dt>

<span data-ttu-id="ac0ed-118">*MacType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac0ed-118">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac0ed-119">Valor MAC do primeiro protocolo em um quadro.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-119">MAC value of the first protocol in a frame.</span></span> <span data-ttu-id="ac0ed-120">Normalmente, o valor de *MacType* é usado quando o analisador deve identificar o primeiro protocolo em um quadro.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-120">Typically, the *MacType* value is used when the parser must identify the first protocol in a frame.</span></span> <span data-ttu-id="ac0ed-121">O valor de *MacType* pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="ac0ed-121">The *MacType* value can be one of the following:</span></span>



| <span data-ttu-id="ac0ed-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ac0ed-122">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="ac0ed-123">Significado</span><span class="sxs-lookup"><span data-stu-id="ac0ed-123">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <span data-ttu-id="ac0ed-124"><dt>**tipo de MAC \_ \_ Ethernet**</dt></span><span class="sxs-lookup"><span data-stu-id="ac0ed-124"><dt>**MAC\_TYPE\_ETHERNET**</dt></span></span> </dl>    | <span data-ttu-id="ac0ed-125">802.3</span><span class="sxs-lookup"><span data-stu-id="ac0ed-125">802.3</span></span> <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <span data-ttu-id="ac0ed-126"><dt>**tipo de MAC \_ \_ TOKENRING**</dt></span><span class="sxs-lookup"><span data-stu-id="ac0ed-126"><dt>**MAC\_TYPE\_TOKENRING**</dt></span></span> </dl> | <span data-ttu-id="ac0ed-127">802.5</span><span class="sxs-lookup"><span data-stu-id="ac0ed-127">802.5</span></span> <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <span data-ttu-id="ac0ed-128"><dt>**tipo de MAC \_ \_ FDDI**</dt></span><span class="sxs-lookup"><span data-stu-id="ac0ed-128"><dt>**MAC\_TYPE\_FDDI**</dt></span></span> </dl>                | <span data-ttu-id="ac0ed-129">ANSI X3T 9.5</span><span class="sxs-lookup"><span data-stu-id="ac0ed-129">ANSI X3T9.5</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="ac0ed-130">*BytesLeft* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac0ed-130">*BytesLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac0ed-131">O número restante de bytes de um local em um quadro até o fim do quadro.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-131">The remaining number of bytes from a location in a frame to the end of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="ac0ed-132">*hPreviousProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac0ed-132">*hPreviousProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac0ed-133">Identificador do protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-133">Handle of the previous protocol.</span></span>

</dd> <dt>

<span data-ttu-id="ac0ed-134">*nPreviousProtocolOffset* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac0ed-134">*nPreviousProtocolOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac0ed-135">Deslocamento do protocolo anterior início do quadro.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-135">Offset of the previous protocol   beginning of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="ac0ed-136">*ProtocolStatusCode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ac0ed-136">*ProtocolStatusCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac0ed-137">Indicador de status de protocolo.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-137">Protocol status indicator.</span></span> <span data-ttu-id="ac0ed-138">A DLL do analisador deve definir um dos códigos de status a seguir.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-138">The parser DLL must set one of the following status codes.</span></span>



| <span data-ttu-id="ac0ed-139">Valor</span><span class="sxs-lookup"><span data-stu-id="ac0ed-139">Value</span></span>                                                                                                                                                                                                              | <span data-ttu-id="ac0ed-140">Significado</span><span class="sxs-lookup"><span data-stu-id="ac0ed-140">Meaning</span></span>                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <span data-ttu-id="ac0ed-141"><dt>**STATUS do protocolo \_ \_ reconhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="ac0ed-141"><dt>**PROTOCOL\_STATUS\_RECOGNIZED**</dt></span></span> </dl>              | <span data-ttu-id="ac0ed-142">O analisador reconhece os dados, mas não sabe qual protocolo segue.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-142">The parser recognizes the data but does not know which protocol follows.</span></span> <span data-ttu-id="ac0ed-143">Depois de definir o código, retorne um ponteiro para os dados não reivindicados restantes que seguem o protocolo reconhecido.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-143">After setting the code, return a pointer to the remaining unclaimed data that follow the recognized protocol.</span></span> <span data-ttu-id="ac0ed-144">Monitor de Rede usa o [*conjunto de acompanhamento*](f.md) do protocolo para continuar a análise.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-144">Network Monitor uses the [*follow set*](f.md) of the protocol to continue parsing.</span></span> <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <span data-ttu-id="ac0ed-145"><dt>**STATUS do protocolo \_ \_ não \_ reconhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="ac0ed-145"><dt>**PROTOCOL\_STATUS\_NOT\_RECOGNIZED**</dt></span></span> </dl> | <span data-ttu-id="ac0ed-146">O analisador não reconhece os dados.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-146">The parser does not recognize the data.</span></span> <span data-ttu-id="ac0ed-147">Depois de definir esse código, retorne o ponteiro para o início dos dados usando o ponteiro que o parâmetro *lpProtocol* passa para a DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-147">After setting this code, return the pointer to the beginning of the data   using the pointer that the *lpProtocol* parameter passes to the parser DLL.</span></span> <span data-ttu-id="ac0ed-148">Monitor de Rede usa o *conjunto de acompanhamento* do protocolo anterior para continuar a análise.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-148">Network Monitor uses the *follow set* of the previous protocol to continue parsing.</span></span> <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <span data-ttu-id="ac0ed-149"><dt>**STATUS do protocolo \_ \_ declarado**</dt></span><span class="sxs-lookup"><span data-stu-id="ac0ed-149"><dt>**PROTOCOL\_STATUS\_CLAIMED**</dt></span></span> </dl>                       | <span data-ttu-id="ac0ed-150">O analisador reconhece os dados e declara os dados restantes.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-150">The parser recognizes the data and claims the remaining data.</span></span> <span data-ttu-id="ac0ed-151">Depois de definir o código, retorne **nulo** para monitor de rede para encerrar a análise de um quadro.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-151">After setting the code, return **NULL** for Network Monitor to terminate parsing a frame.</span></span> <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <span data-ttu-id="ac0ed-152"><dt>**\_ \_ protocolo próximo do status do protocolo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ac0ed-152"><dt>**PROTOCOL\_STATUS\_NEXT\_PROTOCOL**</dt></span></span> </dl>    | <span data-ttu-id="ac0ed-153">O analisador reconhece os dados e sabe qual protocolo segue.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-153">The parser recognizes the data and knows which protocol follows.</span></span> <span data-ttu-id="ac0ed-154">Depois de definir o código, defina o parâmetro *phNextProtocol* e retorne um ponteiro para os dados não reivindicados restantes que seguem o protocolo reconhecido.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-154">After setting the code, set the *phNextProtocol* parameter, and return a pointer to the remaining unclaimed data that follow the recognized protocol.</span></span> <span data-ttu-id="ac0ed-155">Monitor de Rede continua analisando o quadro.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-155">Network Monitor continues parsing the frame.</span></span> <br/>                               |



 

</dd> <dt>

<span data-ttu-id="ac0ed-156">*phNextProtocol* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ac0ed-156">*phNextProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac0ed-157">Aponta para o identificador do próximo protocolo.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-157">Pointer to the handle of the next protocol.</span></span> <span data-ttu-id="ac0ed-158">Esse parâmetro é definido quando um protocolo identifica o protocolo que segue um protocolo.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-158">This parameter is set when a protocol identifies the protocol that follows a protocol.</span></span> <span data-ttu-id="ac0ed-159">Para obter o identificador do próximo protocolo, chame a função [GetProtocolFromTable](getprotocolfromtable.md) .</span><span class="sxs-lookup"><span data-stu-id="ac0ed-159">To obtain the handle of the next protocol, call the [GetProtocolFromTable](getprotocolfromtable.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="ac0ed-160">*lpInstData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ac0ed-160">*lpInstData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac0ed-161">Na entrada, um ponteiro para os dados da instância do protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-161">On input, a pointer to the instance data from the previous protocol.</span></span>

<span data-ttu-id="ac0ed-162">Na saída, um ponteiro para os dados da instância para o protocolo atual.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-162">On output, a pointer to the instance data for the current protocol.</span></span> <span data-ttu-id="ac0ed-163">Os dados da instância não podem ter mais de um \_ PTR de comprimento.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-163">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac0ed-164">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac0ed-164">Return value</span></span>

<span data-ttu-id="ac0ed-165">Se a função for bem-sucedida, o valor de retorno será um ponteiro para o primeiro byte após os dados do analisador reconhecido.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-165">If the function is successful, the return value is a pointer to the first byte after the recognized parser data.</span></span> <span data-ttu-id="ac0ed-166">Se o analisador alegar todos os dados restantes, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-166">If the parser claims all the remaining data, the return value is **NULL**.</span></span>

<span data-ttu-id="ac0ed-167">Se a função não for bem-sucedida, o valor de retorno será um ponteiro inicial que o parâmetro *lpProtocol* passa.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-167">If the function is unsuccessful, the return value is an initial pointer that the *lpProtocol* parameter passes-in.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac0ed-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac0ed-168">Remarks</span></span>

<span data-ttu-id="ac0ed-169">A função **RecognizeFrame** determina se o analisador reconhece os dados brutos começando no ponteiro *lpProtocol* .</span><span class="sxs-lookup"><span data-stu-id="ac0ed-169">The **RecognizeFrame** function determines whether the parser recognizes the raw data   starting at the *lpProtocol* pointer.</span></span>

-   <span data-ttu-id="ac0ed-170">Se o protocolo reconhecer os dados, a função **RecognizeFrame** retornará um ponteiro para os dados restantes ou retornará **NULL** se o protocolo atual for o último protocolo em um quadro.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-170">If the protocol recognizes the data, the **RecognizeFrame** function returns a pointer to the remaining data, or returns **NULL** if the current protocol is the last protocol in a frame.</span></span>
-   <span data-ttu-id="ac0ed-171">Se o protocolo não reconhecer os dados, a função **RecognizeFrame** retornará o ponteiro passado para a DLL do analisador no parâmetro *lpProtocol* .</span><span class="sxs-lookup"><span data-stu-id="ac0ed-171">If the protocol does not recognize the data, the **RecognizeFrame** function returns the pointer passed to the parser DLL in the *lpProtocol* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="ac0ed-172">*RecognizeFrame* pode ser chamado antes que a função [*Register*](register-parser.md) seja chamada para registrar as propriedades de protocolo.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-172">*RecognizeFrame* can be called before the [*Register*](register-parser.md) function is called to register the protocol properties.</span></span> <span data-ttu-id="ac0ed-173">Por esse motivo, a implementação da função *RecognizeFrame* não depende de propriedades ou estruturas criadas ou inicializadas durante a implementação da função de **registro** de protocolo.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-173">For that reason, the implementation of the *RecognizeFrame* function does not rely on any properties or structures that are created or initialized during the implementation of the protocol **Register** function.</span></span>

 

<span data-ttu-id="ac0ed-174">**Conjunto de entrega e conjunto de acompanhamento**</span><span class="sxs-lookup"><span data-stu-id="ac0ed-174">**Handoff Set and Follow Set**</span></span>

<span data-ttu-id="ac0ed-175">Um analisador pode usar um conjunto de entrega ou seguir definido para identificar para Monitor de Rede o protocolo que segue os dados reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-175">A parser can use a handoff set or follow set to identify for Network Monitor the protocol that follows recognized data.</span></span>

-   <span data-ttu-id="ac0ed-176">Se as informações estiverem disponíveis nos dados reconhecidos, o analisador usará sua entrega definida para obter um identificador para o próximo protocolo e, em seguida, passará esse identificador para Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-176">If information is available in recognized data, the parser uses its handoff set to obtain a handle to the next protocol, and then passes that handle to Network Monitor.</span></span>
-   <span data-ttu-id="ac0ed-177">Se as informações não estiverem disponíveis, o analisador não passará por um identificador e Monitor de Rede usará o conjunto de acompanhamento do analisador para determinar o protocolo a seguir.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-177">If information is not available, the parser does not pass a handle, and Network Monitor uses the parser follow set to determine which protocol follows.</span></span>

<span data-ttu-id="ac0ed-178">**Passando informações entre protocolos**</span><span class="sxs-lookup"><span data-stu-id="ac0ed-178">**Passing information between protocols**</span></span>

<span data-ttu-id="ac0ed-179">Use o parâmetro *lpInstData* para passar informações entre protocolos.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-179">Use the *lpInstData* parameter to pass information between protocols.</span></span> <span data-ttu-id="ac0ed-180">Na entrada, você pode recuperar as informações do protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-180">On input, you can retrieve the information from the previous protocol.</span></span> <span data-ttu-id="ac0ed-181">Na saída, você pode passar informações para o próximo protocolo.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-181">On output, you can pass information to the next protocol.</span></span>

<span data-ttu-id="ac0ed-182">Os dados da instância podem ser quaisquer dados que sejam menores ou iguais a um \_ PTR de comprimento, ou um ponteiro para dados, como dados de quadro brutos, que não precisam ser alocados pelo analisador ou liberados pelo parser.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-182">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span>



| <span data-ttu-id="ac0ed-183">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="ac0ed-183">For Information on</span></span>                                        | <span data-ttu-id="ac0ed-184">Consulte</span><span class="sxs-lookup"><span data-stu-id="ac0ed-184">See</span></span>                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac0ed-185">Quais analisadores são e como eles funcionam com Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-185">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="ac0ed-186">Analisadores</span><span class="sxs-lookup"><span data-stu-id="ac0ed-186">Parsers</span></span>](parsers.md)                                                                                                    |
| <span data-ttu-id="ac0ed-187">Quais pontos de entrada são incluídos na DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-187">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="ac0ed-188">Arquitetura de DLL do analisador</span><span class="sxs-lookup"><span data-stu-id="ac0ed-188">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                                                                    |
| <span data-ttu-id="ac0ed-189">Como implementar **RecognizeFrame**  inclui um exemplo.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-189">How to implement **RecognizeFrame**  includes an example.</span></span> | [<span data-ttu-id="ac0ed-190">Implementando RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="ac0ed-190">Implementing RecognizeFrame</span></span>](implementing-recognizeframe.md)                                                            |
| <span data-ttu-id="ac0ed-191">Como especificar um conjunto de entrega e seguir o conjunto.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-191">How to specify a handoff set and follow set.</span></span>              | <span data-ttu-id="ac0ed-192">[Especificando um conjunto de entrega](specifying-a-handoff-set.md)[especificando um conjunto de acompanhamento](specifying-a-follow-set.md)</span><span class="sxs-lookup"><span data-stu-id="ac0ed-192">[Specifying a Handoff Set](specifying-a-handoff-set.md)[Specifying a Follow Set](specifying-a-follow-set.md)</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ac0ed-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac0ed-193">Requirements</span></span>



| <span data-ttu-id="ac0ed-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac0ed-194">Requirement</span></span> | <span data-ttu-id="ac0ed-195">Valor</span><span class="sxs-lookup"><span data-stu-id="ac0ed-195">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ac0ed-196">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac0ed-196">Minimum supported client</span></span><br/> | <span data-ttu-id="ac0ed-197">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ac0ed-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ac0ed-198">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac0ed-198">Minimum supported server</span></span><br/> | <span data-ttu-id="ac0ed-199">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ac0ed-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ac0ed-200">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ac0ed-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac0ed-201"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac0ed-201"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac0ed-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac0ed-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac0ed-203">GetProtocolFromTable</span><span class="sxs-lookup"><span data-stu-id="ac0ed-203">GetProtocolFromTable</span></span>](getprotocolfromtable.md)
</dt> </dl>

 

 




