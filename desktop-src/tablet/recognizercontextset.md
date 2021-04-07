---
description: Testa se o objeto InkDivider pode usar a classe InkRecognizerContext para analisar palavras.
ms.assetid: fd848fcc-5258-401f-8b51-b9d57da173da
title: Função RecognizerContextSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizerContextSet
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 51e75b810c2103afed2e8ac8a28706b9c9af5da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828736"
---
# <a name="recognizercontextset-function"></a><span data-ttu-id="8df98-103">Função RecognizerContextSet</span><span class="sxs-lookup"><span data-stu-id="8df98-103">RecognizerContextSet function</span></span>

<span data-ttu-id="8df98-104">Testa se o objeto [**InkDivider**](inkdivider-class.md) pode usar a classe [**InkRecognizerContext**](inkrecognizercontext-class.md) para analisar palavras.</span><span class="sxs-lookup"><span data-stu-id="8df98-104">Tests whether the [**InkDivider**](inkdivider-class.md) object can use the [**InkRecognizerContext**](inkrecognizercontext-class.md) class to analyze words.</span></span>

<span data-ttu-id="8df98-105">Esta função não se destina a ser usada pelo código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8df98-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8df98-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8df98-106">Syntax</span></span>


```C++
HRESULT WINAPI RecognizerContextSet(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a><span data-ttu-id="8df98-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8df98-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8df98-108">*hDivider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8df98-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df98-109">Um identificador para o objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="8df98-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8df98-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8df98-110">Return value</span></span>

<span data-ttu-id="8df98-111">Essa função pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="8df98-111">This function can return one of these values.</span></span>



| <span data-ttu-id="8df98-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8df98-112">Return code</span></span>                                                                                  | <span data-ttu-id="8df98-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="8df98-113">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="8df98-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8df98-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="8df98-115">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8df98-115">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="8df98-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8df98-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="8df98-117">O parâmetro *pDivider* é inválido.</span><span class="sxs-lookup"><span data-stu-id="8df98-117">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8df98-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8df98-118">Requirements</span></span>



| <span data-ttu-id="8df98-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8df98-119">Requirement</span></span> | <span data-ttu-id="8df98-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8df98-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8df98-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8df98-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8df98-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8df98-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="8df98-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8df98-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8df98-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8df98-124">None supported</span></span><br/>                                                             |
| <span data-ttu-id="8df98-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8df98-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="8df98-126"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8df98-126"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




