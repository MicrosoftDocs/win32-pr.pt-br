---
description: Essa API destina-se somente ao uso interno e não deve ser usada em seu código.
ms.assetid: 836A7515-8C22-4032-9E99-F89B32C21685
title: Função ApiSetQueryApiSetPresence (Apiquery. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApiSetQueryApiSetPresence
api_type:
- DllExport
api_location:
- api-ms-win-core-apiquery-l1-1-0.dll
- ntdll.dll
ms.openlocfilehash: 738a69b0d08f7e619dbd64229d0c13b2ae7dfaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756128"
---
# <a name="apisetqueryapisetpresence-function"></a><span data-ttu-id="20801-103">Função ApiSetQueryApiSetPresence</span><span class="sxs-lookup"><span data-stu-id="20801-103">ApiSetQueryApiSetPresence function</span></span>

<span data-ttu-id="20801-104">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="20801-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="20801-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="20801-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="20801-106">Essa API destina-se somente ao uso interno e não deve ser usada em seu código.</span><span class="sxs-lookup"><span data-stu-id="20801-106">This API is intended for internal use only and should not be used in your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="20801-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20801-107">Syntax</span></span>


```C++
BOOL WINAPI ApiSetQueryApiSetPresence(
  _In_  PCUNICODE_STRING Namespace,
  _Out_ PBOOLEAN         Present
);
```



## <a name="parameters"></a><span data-ttu-id="20801-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20801-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20801-109">*Namespace* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="20801-109">*Namespace* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="20801-110">*Presente* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="20801-110">*Present* \[out\]</span></span>
<span data-ttu-id="20801-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="20801-111"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="20801-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20801-112">Requirements</span></span>



| <span data-ttu-id="20801-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="20801-113">Requirement</span></span> | <span data-ttu-id="20801-114">Valor</span><span class="sxs-lookup"><span data-stu-id="20801-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20801-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20801-115">Minimum supported client</span></span><br/> | <span data-ttu-id="20801-116">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="20801-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                                                           |
| <span data-ttu-id="20801-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20801-117">Minimum supported server</span></span><br/> | <span data-ttu-id="20801-118">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="20801-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="20801-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20801-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="20801-120"><dt>Apiquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="20801-120"><dt>Apiquery.h</dt></span></span> </dl>                                                                                                                 |
| <span data-ttu-id="20801-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20801-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="20801-122"><dt>API-MS-Win-Core-apiquery-L1. lib; </dt> <dt>API-MS-Win-Core-apiquery-L1-1-0. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20801-122"><dt>Api-ms-win-core-apiquery-l1.lib; </dt> <dt>Api-ms-win-core-apiquery-l1-1-0.lib</dt></span></span> </dl> |
| <span data-ttu-id="20801-123">DLL</span><span class="sxs-lookup"><span data-stu-id="20801-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20801-124"><dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20801-124"><dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt></span></span> </dl>                                                                                        |



 

 




