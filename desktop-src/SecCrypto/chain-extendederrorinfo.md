---
description: Retorna uma cadeia de caracteres que contém informações de erro adicionais sobre a entrada indexada.
ms.assetid: 4f0d5289-c414-4e2b-b612-be8ce1d98b12
title: 'Método IChain2:: ExtendedErrorInfo'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ExtendedErrorInfo
- IChain2.ExtendedErrorInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f8a7840d0f54ea7e93ad9998d5e8772a2ae411f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800086"
---
# <a name="ichain2extendederrorinfo-method"></a><span data-ttu-id="f5472-103">Método IChain2:: ExtendedErrorInfo</span><span class="sxs-lookup"><span data-stu-id="f5472-103">IChain2::ExtendedErrorInfo method</span></span>

<span data-ttu-id="f5472-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f5472-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f5472-105">Em vez disso, use a [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f5472-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f5472-106">O método **ExtendedErrorInfo** retorna uma cadeia de caracteres que contém informações de erro adicionais sobre a entrada indexada.</span><span class="sxs-lookup"><span data-stu-id="f5472-106">The **ExtendedErrorInfo** method returns a string that contains additional error information about the indexed entry.</span></span>

<span data-ttu-id="f5472-107">Esse método é introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="f5472-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5472-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5472-108">Syntax</span></span>


```VB
Chain.ExtendedErrorInfo( _
  [ ByVal Index ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f5472-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5472-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5472-110">*Índice* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f5472-110">*Index* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f5472-111">Um **longo** que representa o índice da entrada.</span><span class="sxs-lookup"><span data-stu-id="f5472-111">A **Long** representing the index of the entry.</span></span> <span data-ttu-id="f5472-112">O valor padrão é 1, que retorna informações de erro para o certificado final na cadeia.</span><span class="sxs-lookup"><span data-stu-id="f5472-112">The default value is 1, which returns error information for the end certificate in the chain.</span></span> <span data-ttu-id="f5472-113">**Certificados. Count** retorna informações sobre o certificado raiz da cadeia.</span><span class="sxs-lookup"><span data-stu-id="f5472-113">**Certificates.Count** returns information about the root certificate of the chain.</span></span> <span data-ttu-id="f5472-114">0 retorna informações de erro estendidas para toda a cadeia.</span><span class="sxs-lookup"><span data-stu-id="f5472-114">0 returns extended error information for the entire chain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5472-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5472-115">Return value</span></span>

<span data-ttu-id="f5472-116">Uma cadeia de caracteres que contém as informações de erro estendidas.</span><span class="sxs-lookup"><span data-stu-id="f5472-116">A string that contains the extended error information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5472-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5472-117">Requirements</span></span>



| <span data-ttu-id="f5472-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5472-118">Requirement</span></span> | <span data-ttu-id="f5472-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f5472-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5472-120">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f5472-120">End of client support</span></span><br/> | <span data-ttu-id="f5472-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5472-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f5472-122">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="f5472-122">End of server support</span></span><br/> | <span data-ttu-id="f5472-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5472-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f5472-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f5472-124">Redistributable</span></span><br/>       | <span data-ttu-id="f5472-125">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5472-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f5472-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f5472-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f5472-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5472-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5472-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5472-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5472-129">**Cadeia**</span><span class="sxs-lookup"><span data-stu-id="f5472-129">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
