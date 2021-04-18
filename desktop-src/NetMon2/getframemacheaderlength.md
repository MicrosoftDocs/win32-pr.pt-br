---
description: A função GetFrameMacHeaderLength retorna o comprimento, em bytes, do cabeçalho MAC do quadro.
ms.assetid: 4a0f6a8c-04e0-47cb-abd1-b4011cd2d062
title: Função GetFrameMacHeaderLength (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacHeaderLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4d11a0efac2086884e984edae986720ef704cf81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751411"
---
# <a name="getframemacheaderlength-function"></a><span data-ttu-id="0bb92-103">Função GetFrameMacHeaderLength</span><span class="sxs-lookup"><span data-stu-id="0bb92-103">GetFrameMacHeaderLength function</span></span>

<span data-ttu-id="0bb92-104">A função **GetFrameMacHeaderLength** retorna o comprimento, em bytes, do cabeçalho Mac do quadro.</span><span class="sxs-lookup"><span data-stu-id="0bb92-104">The **GetFrameMacHeaderLength** function returns the length, in bytes, of the MAC header of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb92-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0bb92-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameMacHeaderLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="0bb92-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0bb92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bb92-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0bb92-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb92-108">Identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="0bb92-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bb92-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0bb92-109">Return value</span></span>

<span data-ttu-id="0bb92-110">Se a função for bem-sucedida, o valor de retorno será o comprimento em bytes do cabeçalho MAC.</span><span class="sxs-lookup"><span data-stu-id="0bb92-110">If the function is successful, the return value is the length   in bytes   of the MAC header.</span></span>

<span data-ttu-id="0bb92-111">Se a função não for bem-sucedida ou se um tipo de MAC desconhecido for encontrado, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="0bb92-111">If the function is not successful, or an unknown MAC type is encountered, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bb92-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bb92-112">Remarks</span></span>

<span data-ttu-id="0bb92-113">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetFrameMacHeaderLength** .</span><span class="sxs-lookup"><span data-stu-id="0bb92-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameMacHeaderLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bb92-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bb92-114">Requirements</span></span>



| <span data-ttu-id="0bb92-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bb92-115">Requirement</span></span> | <span data-ttu-id="0bb92-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0bb92-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb92-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bb92-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0bb92-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0bb92-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0bb92-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bb92-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0bb92-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0bb92-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0bb92-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0bb92-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bb92-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bb92-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="0bb92-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0bb92-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="0bb92-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bb92-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0bb92-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0bb92-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bb92-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bb92-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




