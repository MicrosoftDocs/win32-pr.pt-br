---
description: Incrementa a contagem de referência para uma instância de provedor de protocolo de protocolo SSL (SSL).
ms.assetid: 67e7b8b4-b073-4936-b1e0-3fc7c1c011a2
title: Função SslIncrementProviderReferenceCount (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslIncrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 862697035d978db082c303c6e1df6f2a444d8be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755059"
---
# <a name="sslincrementproviderreferencecount-function"></a><span data-ttu-id="de44a-103">Função SslIncrementProviderReferenceCount</span><span class="sxs-lookup"><span data-stu-id="de44a-103">SslIncrementProviderReferenceCount function</span></span>

<span data-ttu-id="de44a-104">A função **SslIncrementProviderReferenceCount** incrementa a contagem de referência para uma instância de provedor de protocolo SSL ( [*protocolo SSL Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="de44a-104">The **SslIncrementProviderReferenceCount** function increments the reference count to a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="de44a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de44a-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslIncrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a><span data-ttu-id="de44a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de44a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de44a-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="de44a-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de44a-108">O identificador para a instância do provedor de protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="de44a-108">The handle to the SSL protocol provider instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de44a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de44a-109">Return value</span></span>

<span data-ttu-id="de44a-110">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="de44a-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="de44a-111">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="de44a-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="de44a-112">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="de44a-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="de44a-113">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="de44a-113">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="de44a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="de44a-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="de44a-115"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="de44a-115"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="de44a-116">O identificador *hSslProvider* não é válido.</span><span class="sxs-lookup"><span data-stu-id="de44a-116">The *hSslProvider* handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="de44a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de44a-117">Requirements</span></span>



| <span data-ttu-id="de44a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="de44a-118">Requirement</span></span> | <span data-ttu-id="de44a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="de44a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de44a-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de44a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="de44a-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de44a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="de44a-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de44a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="de44a-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de44a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="de44a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de44a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="de44a-125"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="de44a-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="de44a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="de44a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de44a-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de44a-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

