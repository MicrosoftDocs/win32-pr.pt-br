---
description: A função DestroyBlob libera toda a memória associada ao BLOB e, em seguida, destrói o BLOB.
ms.assetid: 46cde0b7-1b59-426e-b19b-3c73af3d461a
title: Função DestroyBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e90630981c16f38d601d4e06d04f9326174ef721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768453"
---
# <a name="destroyblob-function"></a><span data-ttu-id="1a66c-103">Função DestroyBlob</span><span class="sxs-lookup"><span data-stu-id="1a66c-103">DestroyBlob function</span></span>

<span data-ttu-id="1a66c-104">A função **DestroyBlob** libera toda a memória associada ao blob e, em seguida, destrói o blob.</span><span class="sxs-lookup"><span data-stu-id="1a66c-104">The **DestroyBlob** function frees all memory associated with the BLOB and then destroys the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a66c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a66c-105">Syntax</span></span>


```C++
DWORD DestroyBlob(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="1a66c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a66c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a66c-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a66c-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a66c-108">Manipule para o BLOB que é destruído.</span><span class="sxs-lookup"><span data-stu-id="1a66c-108">Handle to the to the BLOB that is destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a66c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a66c-109">Return value</span></span>

<span data-ttu-id="1a66c-110">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="1a66c-110">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1a66c-111">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que descreve o erro.</span><span class="sxs-lookup"><span data-stu-id="1a66c-111">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a66c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a66c-112">Requirements</span></span>



| <span data-ttu-id="1a66c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a66c-113">Requirement</span></span> | <span data-ttu-id="1a66c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="1a66c-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a66c-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a66c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1a66c-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1a66c-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1a66c-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a66c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1a66c-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1a66c-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1a66c-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1a66c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a66c-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a66c-120"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="1a66c-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a66c-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a66c-122"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a66c-122"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="1a66c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1a66c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a66c-124"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a66c-124"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a66c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a66c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a66c-126">CreateBlob</span><span class="sxs-lookup"><span data-stu-id="1a66c-126">CreateBlob</span></span>](createblob.md)
</dt> </dl>

 

 




