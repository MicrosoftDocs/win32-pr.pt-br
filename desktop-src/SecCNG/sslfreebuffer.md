---
description: Usado para liberar memória que foi alocada por uma das funções de provedor de protocolo SSL (protocolo SSL Protocol).
ms.assetid: 75a85013-c745-43cb-85b5-e13a2778ec1d
title: Função SslFreeBuffer (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeBuffer
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: bced83b52ddf37266f64ae0c2b8919902f30fff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011802"
---
# <a name="sslfreebuffer-function"></a><span data-ttu-id="911f1-103">Função SslFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="911f1-103">SslFreeBuffer function</span></span>

<span data-ttu-id="911f1-104">A função **SslFreeBuffer** é usada para liberar memória que foi alocada por uma das funções de provedor de [*protocolo de protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="911f1-104">The **SslFreeBuffer** function is used to free memory that was allocated by one of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="911f1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="911f1-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslFreeBuffer(
  _In_ PVOID pvInput
);
```



## <a name="parameters"></a><span data-ttu-id="911f1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="911f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="911f1-107">*pvInput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="911f1-107">*pvInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="911f1-108">Um ponteiro para o buffer de memória a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="911f1-108">A pointer to the memory buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="911f1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="911f1-109">Return value</span></span>

<span data-ttu-id="911f1-110">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="911f1-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="911f1-111">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="911f1-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="911f1-112">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="911f1-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="911f1-113">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="911f1-113">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="911f1-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="911f1-114">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="911f1-115"><dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="911f1-115"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="911f1-116">O parâmetro *pdwProviderCount* ou *ppProviderList* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="911f1-116">The *pdwProviderCount* or *ppProviderList* parameter is **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="911f1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="911f1-117">Requirements</span></span>



| <span data-ttu-id="911f1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="911f1-118">Requirement</span></span> | <span data-ttu-id="911f1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="911f1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="911f1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="911f1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="911f1-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="911f1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="911f1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="911f1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="911f1-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="911f1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="911f1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="911f1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="911f1-125"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="911f1-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="911f1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="911f1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="911f1-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="911f1-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

