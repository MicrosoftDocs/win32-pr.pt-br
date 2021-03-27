---
description: Lê uma linha de setup. inf e extrai o campo especificado da cadeia de caracteres.
ms.assetid: 621e85f8-af30-4f1f-bab1-b7f824daa363
title: Função parsefield (util. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParseField
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 45c7d5bc692f969ba821b5d3243b312d0883658e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170095"
---
# <a name="parsefield-function"></a><span data-ttu-id="3a880-103">Função parsefield</span><span class="sxs-lookup"><span data-stu-id="3a880-103">ParseField function</span></span>

<span data-ttu-id="3a880-104">\[A função **parsefield** , no momento, deve estar disponível para uso na próxima versão do sistema operacional Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3a880-104">\[The **ParseField** function is currently expected to be available for use in the next version of the Microsoft Windows operating system.</span></span> <span data-ttu-id="3a880-105">Ele pode ser alterado ou indisponível nas versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="3a880-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="3a880-106">Lê uma linha de setup. inf e extrai o campo especificado da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3a880-106">Reads a line from Setup.inf and extracts the specified field from the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a880-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a880-107">Syntax</span></span>


```C++
bool ParseField(
  _In_ LPCTSTR *szData,
  _In_ int     n,
  _In_ LPTSTR  *szBuf,
  _In_ int     iBufLen
);
```



## <a name="parameters"></a><span data-ttu-id="3a880-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a880-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a880-109">*szData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a880-109">*szData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a880-110">Tipo: \**LPCTSTR \** _</span><span class="sxs-lookup"><span data-stu-id="3a880-110">Type: \**LPCTSTR\** _</span></span>

<span data-ttu-id="3a880-111">Um ponteiro para a linha do setup. inf.</span><span class="sxs-lookup"><span data-stu-id="3a880-111">A pointer to the line from Setup.inf.</span></span>

</dd> <dt>

<span data-ttu-id="3a880-112">_n \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a880-112">_n\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a880-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="3a880-113">Type: **int**</span></span>

<span data-ttu-id="3a880-114">**Int** que indica qual campo deve ser extraído.</span><span class="sxs-lookup"><span data-stu-id="3a880-114">**INT** that indicates which field to extract.</span></span>

<dt>



 <span data-ttu-id="3a880-115"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="3a880-115">(0)</span></span>


</dt> <dd>

<span data-ttu-id="3a880-116">Indica o campo antes de um sinal de igual (=).</span><span class="sxs-lookup"><span data-stu-id="3a880-116">Indicates the field before an equals sign (=).</span></span>

</dd> <dt>



 <span data-ttu-id="3a880-117">(1)</span><span class="sxs-lookup"><span data-stu-id="3a880-117">(1)</span></span>


</dt> <dd>

<span data-ttu-id="3a880-118">Indica o primeiro campo.</span><span class="sxs-lookup"><span data-stu-id="3a880-118">Indicates the first field.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3a880-119">*szBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a880-119">*szBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a880-120">Tipo: \**LPTSTR \** _</span><span class="sxs-lookup"><span data-stu-id="3a880-120">Type: \**LPTSTR\** _</span></span>

<span data-ttu-id="3a880-121">Um ponteiro para o buffer que recebe o campo extraído.</span><span class="sxs-lookup"><span data-stu-id="3a880-121">A pointer to the buffer that receives the extracted field.</span></span>

</dd> <dt>

<span data-ttu-id="3a880-122">_iBufLen \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a880-122">_iBufLen\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a880-123">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="3a880-123">Type: **int**</span></span>

<span data-ttu-id="3a880-124">**Int** que recebe o tamanho do buffer que recebe o campo extraído.</span><span class="sxs-lookup"><span data-stu-id="3a880-124">**INT** that receives the size of the buffer that receives the extracted field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a880-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a880-125">Return value</span></span>

<span data-ttu-id="3a880-126">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="3a880-126">Type: **bool**</span></span>

<span data-ttu-id="3a880-127">Retornará **true** se a função for bem-sucedida e **false** se falhar.</span><span class="sxs-lookup"><span data-stu-id="3a880-127">Returns **TRUE** if the function is successful and **FALSE** if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a880-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a880-128">Remarks</span></span>

<span data-ttu-id="3a880-129">Os campos na cadeia de caracteres devem ser separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="3a880-129">The fields in the string must be separated by commas.</span></span>

<span data-ttu-id="3a880-130">Espaços à esquerda e à direita são removidos.</span><span class="sxs-lookup"><span data-stu-id="3a880-130">Leading and trailing spaces are removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a880-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a880-131">Requirements</span></span>



| <span data-ttu-id="3a880-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a880-132">Requirement</span></span> | <span data-ttu-id="3a880-133">Valor</span><span class="sxs-lookup"><span data-stu-id="3a880-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a880-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a880-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3a880-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a880-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a880-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a880-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3a880-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a880-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3a880-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3a880-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a880-139"><dt>Util. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a880-139"><dt>Util.h</dt></span></span> </dl>                             |
| <span data-ttu-id="3a880-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a880-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="3a880-141"><dt>Shell32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a880-141"><dt>Shell32.lib</dt></span></span> </dl>                        |
| <span data-ttu-id="3a880-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3a880-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a880-143"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3a880-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




