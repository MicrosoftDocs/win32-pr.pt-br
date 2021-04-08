---
description: A função GetProtocolInfo retorna um ponteiro para um valor de informações de protocolo.
ms.assetid: 1ba47889-b2ed-47ba-94f9-1b781af6d01f
title: Função GetProtocolInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2ec9fb58957c2e0fd64bc1c5878892fe6542af8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920689"
---
# <a name="getprotocolinfo-function"></a><span data-ttu-id="d3ffd-103">Função GetProtocolInfo</span><span class="sxs-lookup"><span data-stu-id="d3ffd-103">GetProtocolInfo function</span></span>

<span data-ttu-id="d3ffd-104">A função **GetProtocolInfo** retorna um ponteiro para um valor de informações de protocolo.</span><span class="sxs-lookup"><span data-stu-id="d3ffd-104">The **GetProtocolInfo** function returns a pointer to a protocol information value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3ffd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3ffd-105">Syntax</span></span>


```C++
LPPROTOCOLINFO WINAPI GetProtocolInfo(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="d3ffd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3ffd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3ffd-107">*hProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d3ffd-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3ffd-108">Identificador para um protocolo.</span><span class="sxs-lookup"><span data-stu-id="d3ffd-108">Handle to a protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3ffd-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3ffd-109">Return value</span></span>

<span data-ttu-id="d3ffd-110">Se a função for bem-sucedida, o valor de retorno será um ponteiro para o valor de informações de protocolo.</span><span class="sxs-lookup"><span data-stu-id="d3ffd-110">If the function is successful, the return value is a pointer to the protocol information value.</span></span>

<span data-ttu-id="d3ffd-111">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d3ffd-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3ffd-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3ffd-112">Remarks</span></span>

<span data-ttu-id="d3ffd-113">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetProtocolInfo** .</span><span class="sxs-lookup"><span data-stu-id="d3ffd-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolInfo** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3ffd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3ffd-114">Requirements</span></span>



| <span data-ttu-id="d3ffd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3ffd-115">Requirement</span></span> | <span data-ttu-id="d3ffd-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d3ffd-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ffd-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3ffd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ffd-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d3ffd-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d3ffd-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3ffd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ffd-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d3ffd-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d3ffd-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d3ffd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3ffd-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3ffd-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d3ffd-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3ffd-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="d3ffd-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3ffd-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d3ffd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d3ffd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3ffd-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3ffd-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




