---
description: A função RemoveFromBlob exclui qualquer nível de entrada de BLOB (proprietário, categoria ou marca).
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: Função RemoveFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RemoveFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a23e4e7e6e6d5c85b1284f8aaba49c1f8eae728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779598"
---
# <a name="removefromblob-function"></a><span data-ttu-id="f3f47-103">Função RemoveFromBlob</span><span class="sxs-lookup"><span data-stu-id="f3f47-103">RemoveFromBlob function</span></span>

<span data-ttu-id="f3f47-104">A função **RemoveFromBlob** exclui qualquer nível de entrada de BLOB (**proprietário**, **categoria** ou **marca**).</span><span class="sxs-lookup"><span data-stu-id="f3f47-104">The **RemoveFromBlob** function deletes any level of BLOB entry (**Owner**, **Category**, or **Tag**).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3f47-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3f47-105">Syntax</span></span>


```C++
DWORD RemoveFromBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName
);
```



## <a name="parameters"></a><span data-ttu-id="f3f47-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3f47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3f47-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f3f47-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f47-108">Identificador para o BLOB do qual uma entrada é excluída.</span><span class="sxs-lookup"><span data-stu-id="f3f47-108">Handle to the BLOB from which an entry is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="f3f47-109">*pOwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f3f47-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f47-110">Ponteiro para o nome do **proprietário** .</span><span class="sxs-lookup"><span data-stu-id="f3f47-110">Pointer to the **Owner** name.</span></span>

</dd> <dt>

<span data-ttu-id="f3f47-111">*pCategoryName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f3f47-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f47-112">Ponteiro para o nome da **categoria** .</span><span class="sxs-lookup"><span data-stu-id="f3f47-112">Pointer to the **Category** name.</span></span> <span data-ttu-id="f3f47-113">Um valor de parâmetro **nulo** indica que o chamador está tentando excluir as informações de **proprietário** fornecidas e todas as suas entradas filhas.</span><span class="sxs-lookup"><span data-stu-id="f3f47-113">A **NULL** parameter value indicates the caller is attempting to delete the given **Owner** information and all of its child entries.</span></span> <span data-ttu-id="f3f47-114">Observe que, se o valor do parâmetro *pCategoryName* for **NULL**, o parâmetro *pTagName* também deverá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f3f47-114">Note that if the *pCategoryName* parameter value is **NULL**, the *pTagName* parameter must also be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f3f47-115">*pTagName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f3f47-115">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f47-116">Ponteiro para o nome da **marca** .</span><span class="sxs-lookup"><span data-stu-id="f3f47-116">Pointer to the **Tag** name.</span></span> <span data-ttu-id="f3f47-117">Um valor **nulo** de _pTagName_ indica que o chamador está tentando excluir a **categoria** determinada e todas as suas entradas filhas.</span><span class="sxs-lookup"><span data-stu-id="f3f47-117">A **NULL**_pTagName_ value indicates the caller is attempting to delete the given **Category** and all of its child entries.</span></span> <span data-ttu-id="f3f47-118">Se o valor do parâmetro não for **nulo**, o chamador solicitará que apenas as entradas de **marca** especificadas sejam excluídas.</span><span class="sxs-lookup"><span data-stu-id="f3f47-118">If the parameter value is not **NULL**, the caller is asking that only that the specified **Tag** entries be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3f47-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f3f47-119">Return value</span></span>

<span data-ttu-id="f3f47-120">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="f3f47-120">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f3f47-121">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="f3f47-121">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3f47-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3f47-122">Requirements</span></span>



| <span data-ttu-id="f3f47-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3f47-123">Requirement</span></span> | <span data-ttu-id="f3f47-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f3f47-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f47-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3f47-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f3f47-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f3f47-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f3f47-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3f47-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f3f47-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f3f47-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f3f47-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f3f47-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3f47-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3f47-130"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="f3f47-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f3f47-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="f3f47-132"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3f47-132"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="f3f47-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f3f47-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3f47-134"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3f47-134"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




