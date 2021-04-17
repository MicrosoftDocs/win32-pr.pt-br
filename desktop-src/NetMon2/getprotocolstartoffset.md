---
description: Retorna o deslocamento de um protocolo especificado no quadro.
ms.assetid: bfe5f477-c9de-4bb9-99e5-b8db895b0ae6
title: Função GetProtocolStartOffset (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ff760c4a61cb39ba897351d706c39d240389bf49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757104"
---
# <a name="getprotocolstartoffset-function"></a><span data-ttu-id="a4133-103">Função GetProtocolStartOffset</span><span class="sxs-lookup"><span data-stu-id="a4133-103">GetProtocolStartOffset function</span></span>

<span data-ttu-id="a4133-104">A função **GetProtocolStartOffset** retorna o deslocamento de um protocolo especificado no quadro.</span><span class="sxs-lookup"><span data-stu-id="a4133-104">The **GetProtocolStartOffset** function returns the offset of a specified protocol in the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4133-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4133-105">Syntax</span></span>


```C++
DWORD WINAPI GetProtocolStartOffset(
   HFRAME hFrame,
   LPSTR  ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="a4133-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4133-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4133-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="a4133-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="a4133-108">Um identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="a4133-108">A handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="a4133-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="a4133-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="a4133-110">O nome do protocolo, como TCP.</span><span class="sxs-lookup"><span data-stu-id="a4133-110">The Protocol name, such as TCP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4133-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4133-111">Return value</span></span>

<span data-ttu-id="a4133-112">Se a função for bem-sucedida, o valor de retorno será um deslocamento **DWORD** para o início do protocolo que está sendo pesquisado por um valor de retorno igual a zero indicará que o protocolo é o primeiro protocolo no quadro.</span><span class="sxs-lookup"><span data-stu-id="a4133-112">If the function is successful, the return value is a **DWORD** offset to the beginning of the protocol being searched for   a return value of zero indicates the protocol is the first protocol in the frame.</span></span>

<span data-ttu-id="a4133-113">Se a função não for bem-sucedida, o protocolo não estará no quadro, o valor de retorno será-1.</span><span class="sxs-lookup"><span data-stu-id="a4133-113">If the function is unsuccessful, the protocol is not in the frame, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4133-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4133-114">Remarks</span></span>

<span data-ttu-id="a4133-115">Quando você recebe o identificador para um quadro, essa função retorna o deslocamento para um protocolo especificado no quadro.</span><span class="sxs-lookup"><span data-stu-id="a4133-115">When given the handle to a frame, this function returns the offset to a specified protocol in the frame.</span></span> <span data-ttu-id="a4133-116">Por exemplo, para determinar se o quadro é um quadro DNS, o analisador DNS requer o endereço de porta do protocolo TCP.</span><span class="sxs-lookup"><span data-stu-id="a4133-116">For example, to determine whether the frame is a DNS frame, the DNS parser requires the port address of the TCP protocol.</span></span> <span data-ttu-id="a4133-117">O analisador DNS chamaria essa função com TCP como o valor de *ProtocolName* .</span><span class="sxs-lookup"><span data-stu-id="a4133-117">The DNS parser would call this function with TCP as the *ProtocolName* value.</span></span> <span data-ttu-id="a4133-118">Se o quadro for reconhecido pelo protocolo TCP, o deslocamento da **palavra** do início do quadro até o início do quadro TCP será retornado.</span><span class="sxs-lookup"><span data-stu-id="a4133-118">If the frame is recognized by the TCP protocol, the **WORD** offset from the beginning of the frame to the beginning of the TCP frame is returned.</span></span> <span data-ttu-id="a4133-119">Se não houver nenhum protocolo TCP, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="a4133-119">If there is no TCP protocol, the return value is zero.</span></span>

<span data-ttu-id="a4133-120">Essa função localiza o início de um protocolo em um quadro.</span><span class="sxs-lookup"><span data-stu-id="a4133-120">This function finds the beginning of a protocol in a frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4133-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4133-121">Requirements</span></span>



| <span data-ttu-id="a4133-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4133-122">Requirement</span></span> | <span data-ttu-id="a4133-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a4133-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a4133-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4133-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a4133-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a4133-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a4133-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4133-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a4133-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a4133-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a4133-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a4133-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4133-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4133-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="a4133-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4133-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="a4133-131"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4133-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a4133-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a4133-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4133-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4133-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




