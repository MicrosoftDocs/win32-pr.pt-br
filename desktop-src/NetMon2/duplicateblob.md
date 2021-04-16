---
description: A função DuplicateBlob copia um BLOB específico.
ms.assetid: d2478f53-328c-4799-890c-7849ce1f22e9
title: Função DuplicateBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DuplicateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: df0fc00f0bd51e89da432e6f3b0143ce6092cedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751413"
---
# <a name="duplicateblob-function"></a><span data-ttu-id="e7019-103">Função DuplicateBlob</span><span class="sxs-lookup"><span data-stu-id="e7019-103">DuplicateBlob function</span></span>

<span data-ttu-id="e7019-104">A função **DuplicateBlob** copia um blob específico.</span><span class="sxs-lookup"><span data-stu-id="e7019-104">The **DuplicateBlob** function copies a specific BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7019-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7019-105">Syntax</span></span>


```C++
DWORD DuplicateBlob(
  _In_  HBLOB hSrcBlob,
  _Out_ HBLOB *hBlobThatWillBeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="e7019-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7019-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7019-107">*hSrcBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7019-107">*hSrcBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7019-108">Identificador para o BLOB que é copiado.</span><span class="sxs-lookup"><span data-stu-id="e7019-108">Handle to the BLOB that is copied.</span></span>

</dd> <dt>

<span data-ttu-id="e7019-109">*hBlobThatWillBeCreated* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e7019-109">*hBlobThatWillBeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7019-110">Identificador para o BLOB duplicado.</span><span class="sxs-lookup"><span data-stu-id="e7019-110">Handle to the duplicate BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7019-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7019-111">Return value</span></span>

<span data-ttu-id="e7019-112">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="e7019-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e7019-113">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que descreve o erro.</span><span class="sxs-lookup"><span data-stu-id="e7019-113">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7019-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7019-114">Requirements</span></span>



| <span data-ttu-id="e7019-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7019-115">Requirement</span></span> | <span data-ttu-id="e7019-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e7019-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7019-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7019-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e7019-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e7019-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e7019-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7019-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e7019-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e7019-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e7019-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e7019-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7019-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7019-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="e7019-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7019-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="e7019-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7019-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="e7019-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e7019-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7019-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7019-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7019-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7019-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7019-128">CreateBlob</span><span class="sxs-lookup"><span data-stu-id="e7019-128">CreateBlob</span></span>](createblob.md)
</dt> <dt>

[<span data-ttu-id="e7019-129">DestroyBlob</span><span class="sxs-lookup"><span data-stu-id="e7019-129">DestroyBlob</span></span>](destroyblob.md)
</dt> </dl>

 

 




