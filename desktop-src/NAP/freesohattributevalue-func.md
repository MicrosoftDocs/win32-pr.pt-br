---
title: Função FreeSoHAttributeValue (NapUtil. h)
description: Libera uma estrutura de dados SoHAttributeValue.
ms.assetid: 21647ee6-2ea2-45fd-b1f2-fb1836196f94
keywords:
- Função FreeSoHAttributeValue NAP
topic_type:
- apiref
api_name:
- FreeSoHAttributeValue
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bd56049eb727554227bd5eb509969f6795670a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009696"
---
# <a name="freesohattributevalue-function"></a><span data-ttu-id="4d446-104">Função FreeSoHAttributeValue</span><span class="sxs-lookup"><span data-stu-id="4d446-104">FreeSoHAttributeValue function</span></span>

> [!Note]  
> <span data-ttu-id="4d446-105">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="4d446-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4d446-106">A função **FreeSoHAttributeValue** libera uma estrutura de dados [**SoHAttributeValue**](sohattributevalue-union.md) .</span><span class="sxs-lookup"><span data-stu-id="4d446-106">The **FreeSoHAttributeValue** function frees an [**SoHAttributeValue**](sohattributevalue-union.md) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d446-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d446-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeSoHAttributeValue(
  _In_ SoHAttributeType  type,
  _In_ SoHAttributeValue *value
);
```



## <a name="parameters"></a><span data-ttu-id="4d446-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d446-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d446-109">*tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="4d446-109">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d446-110">Um valor de [**SoHAttributeType**](sohattributetype-enum.md) que especifica o tipo de valor de atributo soh a ser gratuito.</span><span class="sxs-lookup"><span data-stu-id="4d446-110">A [**SoHAttributeType**](sohattributetype-enum.md) value that specifies the type of SoH attribute value to free.</span></span>

</dd> <dt>

<span data-ttu-id="4d446-111">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="4d446-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d446-112">Um ponteiro para o [**SoHAttributeValue**](sohattributevalue-union.md) para liberar.</span><span class="sxs-lookup"><span data-stu-id="4d446-112">A pointer to the [**SoHAttributeValue**](sohattributevalue-union.md) to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d446-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d446-113">Remarks</span></span>

<span data-ttu-id="4d446-114">Todas as interfaces COM com suporte do sistema NAP usam regras de gerenciamento de memória COM padrão e os alocadores de memória COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="4d446-114">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="4d446-115">**Em** parâmetros são alocados e liberados pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="4d446-115">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="4d446-116">Os parâmetros de **saída** são alocados pelo receptor e liberados pelo chamador usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="4d446-116">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="4d446-117">Os parâmetros **in/out** são alocados pelo chamador, liberados e realocados pelo receptor e, por fim, liberados pelo chamador, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="4d446-117">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="4d446-118">Todas as funções NAP para liberar memória também liberam todos os ponteiros inseridos.</span><span class="sxs-lookup"><span data-stu-id="4d446-118">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d446-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d446-119">Requirements</span></span>



| <span data-ttu-id="4d446-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d446-120">Requirement</span></span> | <span data-ttu-id="4d446-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4d446-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4d446-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d446-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4d446-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d446-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4d446-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d446-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4d446-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4d446-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4d446-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4d446-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d446-127"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d446-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="4d446-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4d446-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d446-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d446-129"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





