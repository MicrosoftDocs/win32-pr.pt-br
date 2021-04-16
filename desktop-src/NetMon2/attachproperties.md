---
description: A função de exportação Attachproperties mapeia as propriedades para um local dentro de um pedaço de dados reconhecidos. Anexarproperties deve ser implementado para cada analisador compatível com a DLL do analisador.
ms.assetid: ef28f571-8364-47d0-841c-580e89333afd
title: Função de retorno de chamada attachproperties (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 3b3cb4be93b8d960b39f0f5c5cf2b5a4809573cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757758"
---
# <a name="attachproperties-callback-function"></a><span data-ttu-id="7e283-104">Função de retorno de chamada attachproperties</span><span class="sxs-lookup"><span data-stu-id="7e283-104">AttachProperties callback function</span></span>

<span data-ttu-id="7e283-105">A função de exportação **attachproperties** mapeia as propriedades para um local dentro de um pedaço de dados reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="7e283-105">The **AttachProperties** export function maps the properties to a location within a piece of recognized data.</span></span> <span data-ttu-id="7e283-106">**Anexarproperties** deve ser implementado para cada analisador compatível com a DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="7e283-106">**AttachProperties** must be implemented for each parser that the parser DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e283-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e283-107">Syntax</span></span>


```C++
DWORD AttachProperties(
  _In_ HFRAME    hFrame,
  _In_ LPBYTE    lpFrame,
  _In_ LPBYTE    lpProtocol,
  _In_ DWORD     MacType,
  _In_ DWORD     BytesLeft,
  _In_ HPROTOCOL hPreviousProtocol,
  _In_ DWORD     nPreviousProtocolOffset,
  _In_ DWORD     lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="7e283-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e283-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e283-109">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e283-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e283-110">Identificador do quadro que está sendo analisado.</span><span class="sxs-lookup"><span data-stu-id="7e283-110">Handle of the frame that is being parsed.</span></span>

</dd> <dt>

<span data-ttu-id="7e283-111">*lpFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e283-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e283-112">Ponteiro para o primeiro byte em um quadro.</span><span class="sxs-lookup"><span data-stu-id="7e283-112">Pointer to the first byte in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="7e283-113">*lpProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e283-113">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e283-114">Ponteiro para o início dos dados reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="7e283-114">Pointer to the start of the recognized data.</span></span>

</dd> <dt>

<span data-ttu-id="7e283-115">*MacType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e283-115">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e283-116">Valor MAC do primeiro protocolo em um quadro.</span><span class="sxs-lookup"><span data-stu-id="7e283-116">MAC value of the first protocol in a frame.</span></span> <span data-ttu-id="7e283-117">O *MacType* pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="7e283-117">The *MacType* can be one of the following:</span></span>



| <span data-ttu-id="7e283-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7e283-118">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="7e283-119">Significado</span><span class="sxs-lookup"><span data-stu-id="7e283-119">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <span data-ttu-id="7e283-120"><dt>**tipo de MAC \_ \_ Ethernet**</dt></span><span class="sxs-lookup"><span data-stu-id="7e283-120"><dt>**MAC\_TYPE\_ETHERNET**</dt></span></span> </dl>    | <span data-ttu-id="7e283-121">802.3</span><span class="sxs-lookup"><span data-stu-id="7e283-121">802.3</span></span> <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <span data-ttu-id="7e283-122"><dt>**tipo de MAC \_ \_ TOKENRING**</dt></span><span class="sxs-lookup"><span data-stu-id="7e283-122"><dt>**MAC\_TYPE\_TOKENRING**</dt></span></span> </dl> | <span data-ttu-id="7e283-123">802.5</span><span class="sxs-lookup"><span data-stu-id="7e283-123">802.5</span></span> <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <span data-ttu-id="7e283-124"><dt>**tipo de MAC \_ \_ FDDI**</dt></span><span class="sxs-lookup"><span data-stu-id="7e283-124"><dt>**MAC\_TYPE\_FDDI**</dt></span></span> </dl>                | <span data-ttu-id="7e283-125">ANSI X3T 9.5</span><span class="sxs-lookup"><span data-stu-id="7e283-125">ANSI X3T9.5</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="7e283-126">*BytesLeft* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e283-126">*BytesLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e283-127">O número restante de bytes em um quadro que começa no início dos dados reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="7e283-127">The remaining number of bytes in a frame   starting at the beginning of the recognized data.</span></span>

</dd> <dt>

<span data-ttu-id="7e283-128">*hPreviousProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e283-128">*hPreviousProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e283-129">Identificador do protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="7e283-129">Handle of the previous protocol.</span></span>

</dd> <dt>

<span data-ttu-id="7e283-130">*nPreviousProtocolOffset* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e283-130">*nPreviousProtocolOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e283-131">Deslocamento do protocolo anterior começando no início do quadro.</span><span class="sxs-lookup"><span data-stu-id="7e283-131">Offset of the previous protocol   starting at the beginning of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="7e283-132">*lpInstData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e283-132">*lpInstData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e283-133">Ponteiro para os dados de instância fornecidos pelo protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="7e283-133">Pointer to the instance data that the previous protocol provides.</span></span> <span data-ttu-id="7e283-134">Os dados da instância não podem ter mais de um \_ PTR de comprimento.</span><span class="sxs-lookup"><span data-stu-id="7e283-134">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e283-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e283-135">Return value</span></span>

<span data-ttu-id="7e283-136">Se a função for bem-sucedida, o valor de retorno será um ponteiro para o primeiro byte após os dados reconhecidos em um quadro ou **nulo** se os dados reconhecidos forem a última parte dos dados em um quadro.</span><span class="sxs-lookup"><span data-stu-id="7e283-136">If the function is successful, the return value is a pointer to the first byte after the recognized data in a frame or **NULL** if the recognized data is the last piece of data in a frame.</span></span>

<span data-ttu-id="7e283-137">Se a função não for bem-sucedida, o valor de retorno será um ponteiro para os dados reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="7e283-137">If the function is unsuccessful, the return value is a pointer to the recognized data.</span></span> <span data-ttu-id="7e283-138">O parâmetro *lpProtocol* passa o ponteiro para a DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="7e283-138">The *lpProtocol* parameter passes the pointer to the parser DLL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e283-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e283-139">Remarks</span></span>

<span data-ttu-id="7e283-140">Monitor de Rede chama a função **attachproperties** para cada analisador que reconhece uma parte dos dados em um quadro.</span><span class="sxs-lookup"><span data-stu-id="7e283-140">Network Monitor calls the **AttachProperties** function for each parser that recognizes a piece of data in a frame.</span></span> <span data-ttu-id="7e283-141">Observe que o analisador determina quais propriedades existem nos dados reconhecidos e onde cada propriedade está localizada.</span><span class="sxs-lookup"><span data-stu-id="7e283-141">Note that the parser determines which properties exist in the recognized data, and where each property is located.</span></span>

<span data-ttu-id="7e283-142">Durante a implementação de **attachproperties**, chame [AttachPropertyInstance](attachpropertyinstance.md) para usar os dados como eles existem na captura.</span><span class="sxs-lookup"><span data-stu-id="7e283-142">During the implementation of **AttachProperties**, call [AttachPropertyInstance](attachpropertyinstance.md) to use the data as it exists in the capture.</span></span> <span data-ttu-id="7e283-143">Você também pode chamar a função [AttachPropertyInstanceEx](attachpropertyinstanceex.md) para modificar os dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="7e283-143">You can also call [AttachPropertyInstanceEx](attachpropertyinstanceex.md) function to modify the property data.</span></span> <span data-ttu-id="7e283-144">No entanto, é recomendável que você use os dados como eles existem na captura.</span><span class="sxs-lookup"><span data-stu-id="7e283-144">However, it is advised that you use the data as it exists in the capture.</span></span>

<span data-ttu-id="7e283-145">As funções **AttachPropertyInstanceEx** e **AttachPropertyInstance** são chamadas apenas para as propriedades que existem nos dados reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="7e283-145">The **AttachPropertyInstanceEx** and **AttachPropertyInstance** functions are called only for the properties that exist in the recognized data.</span></span> <span data-ttu-id="7e283-146">Observe que Monitor de Rede tem um [*banco de dados de propriedade*](p.md) para o analisador que contém uma descrição de todas as propriedades que o analisador suporta.</span><span class="sxs-lookup"><span data-stu-id="7e283-146">Note that Network Monitor has a [*property database*](p.md) for the parser that contains a description of all the properties that the parser supports.</span></span>

<span data-ttu-id="7e283-147">**Dados de instância**</span><span class="sxs-lookup"><span data-stu-id="7e283-147">**Instance data**</span></span>

<span data-ttu-id="7e283-148">Os dados da instância são informações passadas de um analisador para outro.</span><span class="sxs-lookup"><span data-stu-id="7e283-148">Instance data is information that is passed from one parser to another.</span></span> <span data-ttu-id="7e283-149">Os dados da instância podem ser quaisquer dados que sejam menores ou iguais a um \_ PTR de comprimento, ou um ponteiro para dados, como dados de quadro brutos, que não precisam ser alocados pelo analisador ou liberados pelo parser.</span><span class="sxs-lookup"><span data-stu-id="7e283-149">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span> <span data-ttu-id="7e283-150">No parâmetro *lpInstData* das funções **attachproperties** e [RecognizeFrame](recognizeframe.md) , monitor de rede fornece um ponteiro para os dados da instância do protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="7e283-150">In the *lpInstData* parameter of the **AttachProperties** and [RecognizeFrame](recognizeframe.md) functions, Network Monitor provides a pointer to the instance data of the previous protocol.</span></span> <span data-ttu-id="7e283-151">Você pode definir os dados da instância para o analisador durante a implementação de **RecognizeFrame**.</span><span class="sxs-lookup"><span data-stu-id="7e283-151">You can set the instance data for your parser during your implementation of **RecognizeFrame**.</span></span>



| <span data-ttu-id="7e283-152">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="7e283-152">For information on</span></span>                                          | <span data-ttu-id="7e283-153">Consulte</span><span class="sxs-lookup"><span data-stu-id="7e283-153">See</span></span>                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="7e283-154">Quais analisadores são e como eles funcionam com Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="7e283-154">What parsers are, and how they work with Network Monitor.</span></span>   | [<span data-ttu-id="7e283-155">Analisadores</span><span class="sxs-lookup"><span data-stu-id="7e283-155">Parsers</span></span>](parsers.md)                                             |
| <span data-ttu-id="7e283-156">Quais pontos de entrada são incluídos na DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="7e283-156">What entry points are included in the parser DLL.</span></span>           | [<span data-ttu-id="7e283-157">Arquitetura de DLL do analisador</span><span class="sxs-lookup"><span data-stu-id="7e283-157">Parser DLL Architecture</span></span>](parser-dll-architecture.md)             |
| <span data-ttu-id="7e283-158">Como reconhecer dados.</span><span class="sxs-lookup"><span data-stu-id="7e283-158">How to recognize data.</span></span>                                      | [<span data-ttu-id="7e283-159">Implementando RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="7e283-159">Implementing RecognizeFrame</span></span>](implementing-recognizeframe.md)     |
| <span data-ttu-id="7e283-160">Como criar um banco de dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="7e283-160">How to create a property database.</span></span>                          | [<span data-ttu-id="7e283-161">Implementando o registro</span><span class="sxs-lookup"><span data-stu-id="7e283-161">Implementing Register</span></span>](implementing-register.md)                 |
| <span data-ttu-id="7e283-162">Como implementar **anexaproperties**  inclui um exemplo.</span><span class="sxs-lookup"><span data-stu-id="7e283-162">How to implement **AttachProperties**  includes an example.</span></span> | [<span data-ttu-id="7e283-163">Implementando Anexaproperties</span><span class="sxs-lookup"><span data-stu-id="7e283-163">Implementing AttachProperties</span></span>](implementing-attachproperties.md) |



 

## <a name="requirements"></a><span data-ttu-id="7e283-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e283-164">Requirements</span></span>



| <span data-ttu-id="7e283-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e283-165">Requirement</span></span> | <span data-ttu-id="7e283-166">Valor</span><span class="sxs-lookup"><span data-stu-id="7e283-166">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7e283-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e283-167">Minimum supported client</span></span><br/> | <span data-ttu-id="7e283-168">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7e283-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7e283-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e283-169">Minimum supported server</span></span><br/> | <span data-ttu-id="7e283-170">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7e283-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7e283-171">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7e283-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e283-172"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e283-172"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e283-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e283-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e283-174">AttachPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="7e283-174">AttachPropertyInstance</span></span>](attachpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="7e283-175">AttachPropertyInstanceEx</span><span class="sxs-lookup"><span data-stu-id="7e283-175">AttachPropertyInstanceEx</span></span>](attachpropertyinstanceex.md)
</dt> <dt>

[<span data-ttu-id="7e283-176">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="7e283-176">RecognizeFrame</span></span>](recognizeframe.md)
</dt> </dl>

 

 




