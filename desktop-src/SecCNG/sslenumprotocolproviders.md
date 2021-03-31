---
description: Retorna uma matriz de provedores de protocolo de protocolo de protocolo SSL instalado (SSL).
ms.assetid: a61ddcf5-b7e3-40b2-82fc-1cf87eb963ec
title: Função SslEnumProtocolProviders (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumProtocolProviders
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 94c8648950af20a97bcc34b614aee0d0f716b043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171993"
---
# <a name="sslenumprotocolproviders-function"></a><span data-ttu-id="eab7f-103">Função SslEnumProtocolProviders</span><span class="sxs-lookup"><span data-stu-id="eab7f-103">SslEnumProtocolProviders function</span></span>

<span data-ttu-id="eab7f-104">A função **SslEnumProtocolProviders** retorna uma matriz de provedores de protocolo de [*protocolo de protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL) instalados.</span><span class="sxs-lookup"><span data-stu-id="eab7f-104">The **SslEnumProtocolProviders** function returns an array of installed [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol providers.</span></span>

## <a name="syntax"></a><span data-ttu-id="eab7f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eab7f-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEnumProtocolProviders(
  _Out_ DWORD              *pdwProviderCount,
  _Out_ NCryptProviderName **ppProviderList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="eab7f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eab7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eab7f-107">*pdwProviderCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="eab7f-107">*pdwProviderCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eab7f-108">Um ponteiro para um valor **DWORD** para receber o número de provedores de protocolo retornado.</span><span class="sxs-lookup"><span data-stu-id="eab7f-108">A pointer to a **DWORD** value to receive the number of protocol providers returned.</span></span>

</dd> <dt>

<span data-ttu-id="eab7f-109">*ppProviderList* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="eab7f-109">*ppProviderList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eab7f-110">Um ponteiro para um buffer que recebe a matriz de estruturas [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) .</span><span class="sxs-lookup"><span data-stu-id="eab7f-110">A pointer to a buffer that receives the array of [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) structures.</span></span>

</dd> <dt>

<span data-ttu-id="eab7f-111">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eab7f-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eab7f-112">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="eab7f-112">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eab7f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eab7f-113">Return value</span></span>

<span data-ttu-id="eab7f-114">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="eab7f-114">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="eab7f-115">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="eab7f-115">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="eab7f-116">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="eab7f-116">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="eab7f-117">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="eab7f-117">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="eab7f-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="eab7f-118">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eab7f-119"><dt>**Nte \_ \_Sinalizadores INválidos**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="eab7f-119"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="eab7f-120">O parâmetro *dwFlags* não é zero.</span><span class="sxs-lookup"><span data-stu-id="eab7f-120">The *dwFlags* parameter is not zero.</span></span><br/>                              |
| <dl> <span data-ttu-id="eab7f-121"><dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória</span><span class="sxs-lookup"><span data-stu-id="eab7f-121"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="eab7f-122">Não há memória suficiente disponível para alocar os buffers necessários.</span><span class="sxs-lookup"><span data-stu-id="eab7f-122">Not enough memory is available to allocate necessary buffers.</span></span><br/>     |
| <dl> <span data-ttu-id="eab7f-123"><dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="eab7f-123"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="eab7f-124">O parâmetro *pdwProviderCount* ou *ppProviderList* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="eab7f-124">The *pdwProviderCount* or *ppProviderList* parameter is **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eab7f-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="eab7f-125">Remarks</span></span>

<span data-ttu-id="eab7f-126">Quando você terminar de usar a matriz de estruturas [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) , chame a função [**SslFreeBuffer**](sslfreebuffer.md) para liberar a matriz.</span><span class="sxs-lookup"><span data-stu-id="eab7f-126">When you have finished using the array of [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) structures, call the [**SslFreeBuffer**](sslfreebuffer.md) function to free the array.</span></span>

## <a name="requirements"></a><span data-ttu-id="eab7f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eab7f-127">Requirements</span></span>



| <span data-ttu-id="eab7f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="eab7f-128">Requirement</span></span> | <span data-ttu-id="eab7f-129">Valor</span><span class="sxs-lookup"><span data-stu-id="eab7f-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eab7f-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eab7f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="eab7f-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eab7f-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eab7f-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eab7f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="eab7f-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eab7f-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="eab7f-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eab7f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="eab7f-135"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="eab7f-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="eab7f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="eab7f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eab7f-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eab7f-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

