---
description: Recupera os dados de atributo para o arquivo especificado.
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: Função SdbGetFileAttributes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 651b9af34afdd2ffd767eba7ca4467ecfee081cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088813"
---
# <a name="sdbgetfileattributes-function"></a><span data-ttu-id="671f0-103">Função SdbGetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="671f0-103">SdbGetFileAttributes function</span></span>

<span data-ttu-id="671f0-104">Recupera os dados de atributo para o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="671f0-104">Retrieves the attribute data for the specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="671f0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="671f0-105">Syntax</span></span>


```C++
BOOL WINAPI SdbGetFileAttributes(
  _In_  LPCTSTR   lpwszFileName,
  _Out_ PATTRINFO *ppAttrInfo,
  _Out_ LPDWORD   lpdwAttrCount
);
```



## <a name="parameters"></a><span data-ttu-id="671f0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="671f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="671f0-107">*lpwszFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="671f0-107">*lpwszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="671f0-108">O caminho para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="671f0-108">The path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="671f0-109">*ppAttrInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="671f0-109">*ppAttrInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="671f0-110">Uma matriz de estruturas [**ATTRINFO**](attrinfo.md) que contêm os dados de atributo.</span><span class="sxs-lookup"><span data-stu-id="671f0-110">An array of [**ATTRINFO**](attrinfo.md) structures that contain the attribute data.</span></span>

</dd> <dt>

<span data-ttu-id="671f0-111">*lpdwAttrCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="671f0-111">*lpdwAttrCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="671f0-112">O número de atributos.</span><span class="sxs-lookup"><span data-stu-id="671f0-112">The number of attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="671f0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="671f0-113">Return value</span></span>

<span data-ttu-id="671f0-114">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="671f0-114">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="671f0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="671f0-115">Remarks</span></span>

<span data-ttu-id="671f0-116">Depois de concluir os dados, libere-os usando a função [**SdbFreeFileAttributes**](sdbfreefileattributes.md) .</span><span class="sxs-lookup"><span data-stu-id="671f0-116">When you have finished with the data, free it using the [**SdbFreeFileAttributes**](sdbfreefileattributes.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="671f0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="671f0-117">Requirements</span></span>



| <span data-ttu-id="671f0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="671f0-118">Requirement</span></span> | <span data-ttu-id="671f0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="671f0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="671f0-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="671f0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="671f0-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="671f0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="671f0-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="671f0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="671f0-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="671f0-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="671f0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="671f0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="671f0-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="671f0-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="671f0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="671f0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671f0-127">**SdbFormatAttribute**</span><span class="sxs-lookup"><span data-stu-id="671f0-127">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
</dt> <dt>

[<span data-ttu-id="671f0-128">**SdbFreeFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="671f0-128">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
</dt> </dl>

 

 




