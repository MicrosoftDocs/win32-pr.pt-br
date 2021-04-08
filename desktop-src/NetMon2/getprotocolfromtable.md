---
description: A função GetProtocolFromTable retorna um identificador para um protocolo&\# 8212; com base em uma determinada tabela e valor de entrega.
ms.assetid: 34b07079-0b20-40d8-a529-4179ecc68ebf
title: Função GetProtocolFromTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 498892fc2cc5ada2e177b8fb3f70f40a1ef10dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920690"
---
# <a name="getprotocolfromtable-function"></a><span data-ttu-id="5deb2-103">Função GetProtocolFromTable</span><span class="sxs-lookup"><span data-stu-id="5deb2-103">GetProtocolFromTable function</span></span>

<span data-ttu-id="5deb2-104">A função **GetProtocolFromTable** retorna um identificador para um protocolo com base em uma determinada tabela e valor de entrega.</span><span class="sxs-lookup"><span data-stu-id="5deb2-104">The **GetProtocolFromTable** function returns a handle to a protocol based on a given handoff table and value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5deb2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5deb2-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI GetProtocolFromTable(
  _In_  LPHANDOFFTABLE hTable,
  _In_  DWORD          ItemToFind,
  _Out_ PDWORD_PTR     lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="5deb2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5deb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5deb2-107">*hTable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5deb2-107">*hTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5deb2-108">Identificador para uma tabela de entrega.</span><span class="sxs-lookup"><span data-stu-id="5deb2-108">Handle to a handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="5deb2-109">*ItemToFind* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5deb2-109">*ItemToFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5deb2-110">Valor usado para localizar o protocolo em uma tabela de entrega.</span><span class="sxs-lookup"><span data-stu-id="5deb2-110">Value used to locate the protocol in a handoff table.</span></span> <span data-ttu-id="5deb2-111">O valor deve estar disponível nos dados do protocolo.</span><span class="sxs-lookup"><span data-stu-id="5deb2-111">The value must be available in the protocol data.</span></span>

</dd> <dt>

<span data-ttu-id="5deb2-112">*lpInstData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5deb2-112">*lpInstData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5deb2-113">Se disponível na tabela entrega, os dados da instância para o próximo protocolo.</span><span class="sxs-lookup"><span data-stu-id="5deb2-113">If available in the handoff table, instance data for the next protocol.</span></span> <span data-ttu-id="5deb2-114">Os dados da instância não podem ter mais de um \_ PTR de comprimento.</span><span class="sxs-lookup"><span data-stu-id="5deb2-114">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5deb2-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5deb2-115">Return value</span></span>

<span data-ttu-id="5deb2-116">Se a função for bem-sucedida, o valor de retorno será um identificador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="5deb2-116">If the function is successful, the return value is a protocol handle.</span></span>

<span data-ttu-id="5deb2-117">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5deb2-117">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5deb2-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5deb2-118">Remarks</span></span>

<span data-ttu-id="5deb2-119">Ao implementar a função de exportação [RecognizeFrame](recognizeframe.md) , a função **GetProtocolFromTable** é usada para obter um identificador para o próximo protocolo.</span><span class="sxs-lookup"><span data-stu-id="5deb2-119">When implementing the [RecognizeFrame](recognizeframe.md) export function, the **GetProtocolFromTable** function is used to obtain a handle to the next protocol.</span></span> <span data-ttu-id="5deb2-120">A função **GetProtocolFromTable** será chamada para recuperar um identificador do próximo protocolo se o protocolo identificar o protocolo a seguir.</span><span class="sxs-lookup"><span data-stu-id="5deb2-120">The **GetProtocolFromTable** function is called to retrieve a handle from the next protocol if the protocol identifies which protocol follows.</span></span>

<span data-ttu-id="5deb2-121">**Dados de instância**</span><span class="sxs-lookup"><span data-stu-id="5deb2-121">**Instance data**</span></span>

<span data-ttu-id="5deb2-122">Os dados da instância podem ser quaisquer dados que sejam menores ou iguais a um \_ PTR de comprimento, ou um ponteiro para dados, como dados de quadro brutos, que não precisam ser alocados pelo analisador ou liberados pelo parser.</span><span class="sxs-lookup"><span data-stu-id="5deb2-122">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span>

## <a name="requirements"></a><span data-ttu-id="5deb2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5deb2-123">Requirements</span></span>



| <span data-ttu-id="5deb2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5deb2-124">Requirement</span></span> | <span data-ttu-id="5deb2-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5deb2-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5deb2-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5deb2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5deb2-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5deb2-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5deb2-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5deb2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5deb2-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5deb2-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5deb2-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5deb2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5deb2-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5deb2-131"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="5deb2-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5deb2-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="5deb2-133"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5deb2-133"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="5deb2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5deb2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5deb2-135"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5deb2-135"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5deb2-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="5deb2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5deb2-137">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="5deb2-137">RecognizeFrame</span></span>](recognizeframe.md)
</dt> </dl>

 

 




