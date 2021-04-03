---
description: Exclui um objeto InkDivider e libera recursos associados.
ms.assetid: adf772e0-2829-4410-83c4-45a24bf3a848
title: Função DeleteInkDivider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteInkDivider
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 8338d179b0bd57232463c794feca96885ee006fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829697"
---
# <a name="deleteinkdivider-function"></a><span data-ttu-id="c96ac-103">Função DeleteInkDivider</span><span class="sxs-lookup"><span data-stu-id="c96ac-103">DeleteInkDivider function</span></span>

<span data-ttu-id="c96ac-104">Exclui um objeto [**InkDivider**](inkdivider-class.md) e libera recursos associados.</span><span class="sxs-lookup"><span data-stu-id="c96ac-104">Deletes an [**InkDivider**](inkdivider-class.md) object and releases associated resources.</span></span>

<span data-ttu-id="c96ac-105">Esta função não se destina a ser usada pelo código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c96ac-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c96ac-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c96ac-106">Syntax</span></span>


```C++
HRESULT WINAPI DeleteInkDivider(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a><span data-ttu-id="c96ac-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c96ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c96ac-108">*hDivider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c96ac-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c96ac-109">Um identificador para o objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="c96ac-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c96ac-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c96ac-110">Return value</span></span>

<span data-ttu-id="c96ac-111">Essa função pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="c96ac-111">This function can return one of these values.</span></span>



| <span data-ttu-id="c96ac-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c96ac-112">Return code</span></span>                                                                                  | <span data-ttu-id="c96ac-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="c96ac-113">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="c96ac-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c96ac-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c96ac-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c96ac-115">The method succeeded.</span></span><br/>                |
| <dl> <span data-ttu-id="c96ac-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c96ac-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c96ac-117">O parâmetro *hDivider* é inválido.</span><span class="sxs-lookup"><span data-stu-id="c96ac-117">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c96ac-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c96ac-118">Requirements</span></span>



| <span data-ttu-id="c96ac-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c96ac-119">Requirement</span></span> | <span data-ttu-id="c96ac-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c96ac-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c96ac-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c96ac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c96ac-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c96ac-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c96ac-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c96ac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c96ac-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c96ac-124">None supported</span></span><br/>                                                             |
| <span data-ttu-id="c96ac-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c96ac-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="c96ac-126"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c96ac-126"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




