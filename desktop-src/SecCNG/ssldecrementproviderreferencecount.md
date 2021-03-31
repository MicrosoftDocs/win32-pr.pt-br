---
description: Decrementa as referências ao provedor de protocolo de protocolo SSL (SSL).
ms.assetid: 67bfa4b5-c02c-4a76-871d-93f3bf4e3602
title: Função SslDecrementProviderReferenceCount (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4d3fe072c02f22b713115dd5191b0b5e0cedbb37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921413"
---
# <a name="ssldecrementproviderreferencecount-function"></a><span data-ttu-id="010ca-103">Função SslDecrementProviderReferenceCount</span><span class="sxs-lookup"><span data-stu-id="010ca-103">SslDecrementProviderReferenceCount function</span></span>

<span data-ttu-id="010ca-104">A função **SslDecrementProviderReferenceCount** decrementa as referências ao provedor de [*protocolo de protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="010ca-104">The **SslDecrementProviderReferenceCount** function decrements the references to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="010ca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="010ca-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslDecrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a><span data-ttu-id="010ca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="010ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="010ca-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="010ca-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="010ca-108">O identificador da instância do provedor de protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="010ca-108">The handle of the SSL protocol provider instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="010ca-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="010ca-109">Return value</span></span>

<span data-ttu-id="010ca-110">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="010ca-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="010ca-111">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="010ca-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="010ca-112">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="010ca-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="010ca-113">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="010ca-113">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="010ca-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="010ca-114">Description</span></span>                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="010ca-115"><dt> **Status \_ inválido do \_ identificador**</dt> <dt>0xC0000008L</dt></span><span class="sxs-lookup"><span data-stu-id="010ca-115"><dt>**STATUS\_INVALID\_HANDLE** </dt> <dt>0xC0000008L</dt></span></span> </dl> | <span data-ttu-id="010ca-116">O identificador do provedor SSL não é válido.</span><span class="sxs-lookup"><span data-stu-id="010ca-116">The SSL provider handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="010ca-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="010ca-117">Requirements</span></span>



| <span data-ttu-id="010ca-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="010ca-118">Requirement</span></span> | <span data-ttu-id="010ca-119">Valor</span><span class="sxs-lookup"><span data-stu-id="010ca-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="010ca-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="010ca-120">Minimum supported client</span></span><br/> | <span data-ttu-id="010ca-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="010ca-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="010ca-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="010ca-122">Minimum supported server</span></span><br/> | <span data-ttu-id="010ca-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="010ca-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="010ca-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="010ca-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="010ca-125"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="010ca-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="010ca-126">DLL</span><span class="sxs-lookup"><span data-stu-id="010ca-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="010ca-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="010ca-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

