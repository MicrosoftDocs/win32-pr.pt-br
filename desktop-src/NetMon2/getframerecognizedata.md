---
description: A função GetFrameRecognizeData retorna uma tabela de estruturas RECOGNIZEDATA. Cada uma dessas estruturas contém um identificador de protocolo e um deslocamento que aponta para o início do protocolo especificado nos dados.
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: Função GetFrameRecognizeData (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameRecognizeData
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 627ba046b3adead0291239f5d94f4e56958e6a80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920696"
---
# <a name="getframerecognizedata-function"></a><span data-ttu-id="c8cd6-104">Função GetFrameRecognizeData</span><span class="sxs-lookup"><span data-stu-id="c8cd6-104">GetFrameRecognizeData function</span></span>

<span data-ttu-id="c8cd6-105">A função **GetFrameRecognizeData** retorna uma tabela de estruturas **RECOGNIZEDATA** .</span><span class="sxs-lookup"><span data-stu-id="c8cd6-105">The **GetFrameRecognizeData** function returns a table of **RECOGNIZEDATA** structures.</span></span> <span data-ttu-id="c8cd6-106">Cada uma dessas estruturas contém um identificador de protocolo e um deslocamento que aponta para o início do protocolo especificado nos dados.</span><span class="sxs-lookup"><span data-stu-id="c8cd6-106">Each of these structures contains a protocol identifier and an offset that points to the start of the specified protocol in the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8cd6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8cd6-107">Syntax</span></span>


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="c8cd6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8cd6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8cd6-109">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c8cd6-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8cd6-110">Identificador para um quadro.</span><span class="sxs-lookup"><span data-stu-id="c8cd6-110">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8cd6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c8cd6-111">Return value</span></span>

<span data-ttu-id="c8cd6-112">Se a função for bem-sucedida, o valor de retorno será um ponteiro para uma estrutura **RECOGNIZEDATATABLE** .</span><span class="sxs-lookup"><span data-stu-id="c8cd6-112">If the function is successful, the return value is a pointer to a **RECOGNIZEDATATABLE** structure.</span></span>

<span data-ttu-id="c8cd6-113">Se a função não for bem-sucedida, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="c8cd6-113">If the function is not successful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8cd6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8cd6-114">Remarks</span></span>

<span data-ttu-id="c8cd6-115">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetFrameRecognizeData** .</span><span class="sxs-lookup"><span data-stu-id="c8cd6-115">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameRecognizeData** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8cd6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8cd6-116">Requirements</span></span>



| <span data-ttu-id="c8cd6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8cd6-117">Requirement</span></span> | <span data-ttu-id="c8cd6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c8cd6-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c8cd6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8cd6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c8cd6-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c8cd6-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c8cd6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8cd6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c8cd6-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c8cd6-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c8cd6-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c8cd6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8cd6-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8cd6-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="c8cd6-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8cd6-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="c8cd6-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8cd6-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c8cd6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c8cd6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8cd6-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8cd6-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




