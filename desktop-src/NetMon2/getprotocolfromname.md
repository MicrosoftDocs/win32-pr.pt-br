---
description: A função GetProtocolFromName retorna um identificador para um protocolo de um determinado nome.
ms.assetid: 18f5a9a7-4245-479d-a0da-2ede362a60b8
title: Função GetProtocolFromName (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e104c066be2a5465083c7983aaefebd46f548b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646793"
---
# <a name="getprotocolfromname-function"></a><span data-ttu-id="ada17-103">Função GetProtocolFromName</span><span class="sxs-lookup"><span data-stu-id="ada17-103">GetProtocolFromName function</span></span>

<span data-ttu-id="ada17-104">A função **GetProtocolFromName** retorna um identificador para um protocolo de um determinado nome.</span><span class="sxs-lookup"><span data-stu-id="ada17-104">The **GetProtocolFromName** function returns a handle to a protocol of a given name.</span></span>

## <a name="syntax"></a><span data-ttu-id="ada17-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ada17-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI GetProtocolFromName(
  _In_ LPSTR ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="ada17-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ada17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ada17-107">*ProtocolName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ada17-107">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ada17-108">Nome do protocolo (por exemplo, IP).</span><span class="sxs-lookup"><span data-stu-id="ada17-108">Protocol name (for example, IP).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ada17-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ada17-109">Return value</span></span>

<span data-ttu-id="ada17-110">Se a função for bem-sucedida, o valor de retorno será um identificador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="ada17-110">If the function is successful, the return value is a protocol handle.</span></span>

<span data-ttu-id="ada17-111">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ada17-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ada17-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ada17-112">Remarks</span></span>

<span data-ttu-id="ada17-113">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetProtocolFromName** .</span><span class="sxs-lookup"><span data-stu-id="ada17-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolFromName** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ada17-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ada17-114">Requirements</span></span>



| <span data-ttu-id="ada17-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ada17-115">Requirement</span></span> | <span data-ttu-id="ada17-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ada17-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ada17-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ada17-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ada17-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ada17-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ada17-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ada17-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ada17-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ada17-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ada17-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ada17-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ada17-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ada17-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="ada17-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ada17-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="ada17-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ada17-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ada17-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ada17-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ada17-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ada17-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




