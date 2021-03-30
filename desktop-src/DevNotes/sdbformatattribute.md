---
description: Converte os dados de atributo especificados em formato XML.
ms.assetid: 7a75726d-f1ec-4137-89c1-eccb4a78fc22
title: Função SdbFormatAttribute
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFormatAttribute
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e06bbaa288c7ecb0e85cd8a779100d547c33d687
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826072"
---
# <a name="sdbformatattribute-function"></a><span data-ttu-id="13ec4-103">Função SdbFormatAttribute</span><span class="sxs-lookup"><span data-stu-id="13ec4-103">SdbFormatAttribute function</span></span>

<span data-ttu-id="13ec4-104">Converte os dados de atributo especificados em formato XML.</span><span class="sxs-lookup"><span data-stu-id="13ec4-104">Converts the specified attribute data to XML format.</span></span>

## <a name="syntax"></a><span data-ttu-id="13ec4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13ec4-105">Syntax</span></span>


```C++
BOOL WINAPI SdbFormatAttribute(
  _In_  PATTRINFO pAttrInfo,
  _Out_ LPTSTR    pchBuffer,
  _In_  DWORD     dwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="13ec4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13ec4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13ec4-107">*pAttrInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="13ec4-107">*pAttrInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13ec4-108">Uma estrutura [**ATTRINFO**](attrinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="13ec4-108">An [**ATTRINFO**](attrinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="13ec4-109">*pchBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="13ec4-109">*pchBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13ec4-110">O buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="13ec4-110">The output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="13ec4-111">*dwBufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="13ec4-111">*dwBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13ec4-112">O tamanho do buffer *pchBuffer* , em caracteres.</span><span class="sxs-lookup"><span data-stu-id="13ec4-112">The size of the *pchBuffer* buffer, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13ec4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="13ec4-113">Return value</span></span>

<span data-ttu-id="13ec4-114">A função retornará **true** em caso de êxito ou **falso** se o buffer for muito pequeno ou se o atributo não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="13ec4-114">The function returns **TRUE** on success or **FALSE** if the buffer is too small or the attribute is not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="13ec4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13ec4-115">Requirements</span></span>



| <span data-ttu-id="13ec4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="13ec4-116">Requirement</span></span> | <span data-ttu-id="13ec4-117">Valor</span><span class="sxs-lookup"><span data-stu-id="13ec4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13ec4-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13ec4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="13ec4-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="13ec4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="13ec4-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13ec4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="13ec4-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="13ec4-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="13ec4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="13ec4-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13ec4-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13ec4-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13ec4-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="13ec4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13ec4-125">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="13ec4-125">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




