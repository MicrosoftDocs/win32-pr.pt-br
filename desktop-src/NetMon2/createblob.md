---
description: A função createBlob cria um BLOB vazio.
ms.assetid: fa31855b-af85-4ab5-b434-e54111731d8f
title: Função createBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: f2abb32afd68dd321a520c1d56c217e801fa9101
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662284"
---
# <a name="createblob-function"></a><span data-ttu-id="6dfec-103">Função createBlob</span><span class="sxs-lookup"><span data-stu-id="6dfec-103">CreateBlob function</span></span>

<span data-ttu-id="6dfec-104">A função **createBlob** cria um blob vazio.</span><span class="sxs-lookup"><span data-stu-id="6dfec-104">The **CreateBlob** function creates an empty BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dfec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6dfec-105">Syntax</span></span>


```C++
DWORD CreateBlob(
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="6dfec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6dfec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dfec-107">*phBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6dfec-107">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfec-108">Ponteiro para a variável em que o ponteiro para o novo BLOB é retornado.</span><span class="sxs-lookup"><span data-stu-id="6dfec-108">Pointer to the variable where the pointer to the new BLOB is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dfec-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6dfec-109">Return value</span></span>

<span data-ttu-id="6dfec-110">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="6dfec-110">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6dfec-111">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que descreve o erro.</span><span class="sxs-lookup"><span data-stu-id="6dfec-111">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dfec-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6dfec-112">Requirements</span></span>



| <span data-ttu-id="6dfec-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dfec-113">Requirement</span></span> | <span data-ttu-id="6dfec-114">Valor</span><span class="sxs-lookup"><span data-stu-id="6dfec-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dfec-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6dfec-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6dfec-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6dfec-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6dfec-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6dfec-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6dfec-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6dfec-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6dfec-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6dfec-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dfec-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6dfec-120"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="6dfec-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6dfec-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="6dfec-122"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6dfec-122"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="6dfec-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6dfec-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dfec-124"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dfec-124"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dfec-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6dfec-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dfec-126">DestroyBlob</span><span class="sxs-lookup"><span data-stu-id="6dfec-126">DestroyBlob</span></span>](destroyblob.md)
</dt> </dl>

 

 




