---
description: Obtém o formato XML de uma referência anexada ao token.
ms.assetid: F4329A2E-61FD-40E0-9E24-87C9A4585E55
title: 'Método IUpdateEndpointAuthToken:: TokenReferenceAttached (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceAttached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 9582c54c42e2416d5d7a98e85eba3151fd6769a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782935"
---
# <a name="iupdateendpointauthtokentokenreferenceattached-method"></a><span data-ttu-id="5e46a-103">Método IUpdateEndpointAuthToken:: TokenReferenceAttached</span><span class="sxs-lookup"><span data-stu-id="5e46a-103">IUpdateEndpointAuthToken::TokenReferenceAttached method</span></span>

<span data-ttu-id="5e46a-104">Obtém o formato XML de uma referência anexada ao token.</span><span class="sxs-lookup"><span data-stu-id="5e46a-104">Gets the XML format of an attached reference to the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e46a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e46a-105">Syntax</span></span>


```C++
HRESULT TokenReferenceAttached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a><span data-ttu-id="5e46a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e46a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e46a-107">*pszTokenReference* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5e46a-107">*pszTokenReference* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e46a-108">Ponteiro para a referência de token anexada.</span><span class="sxs-lookup"><span data-stu-id="5e46a-108">Pointer to the attached token reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e46a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e46a-109">Return value</span></span>

<span data-ttu-id="5e46a-110">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5e46a-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="5e46a-111">Caso contrário, retorna um código de erro COM do Windows.</span><span class="sxs-lookup"><span data-stu-id="5e46a-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e46a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e46a-112">Remarks</span></span>

<span data-ttu-id="5e46a-113">Uma referência anexada refere-se a um referece (como o assinatura que está usando o token) que está na mesma mensagem em que o token reside.</span><span class="sxs-lookup"><span data-stu-id="5e46a-113">An attached reference refers a referece (such as the signiture that is using the token) that is in the same message where the token resides.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e46a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e46a-114">Requirements</span></span>



| <span data-ttu-id="5e46a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e46a-115">Requirement</span></span> | <span data-ttu-id="5e46a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5e46a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e46a-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e46a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5e46a-118">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="5e46a-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="5e46a-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e46a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5e46a-120">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="5e46a-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="5e46a-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e46a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e46a-122"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e46a-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e46a-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="5e46a-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e46a-124"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e46a-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="5e46a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5e46a-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="5e46a-126"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e46a-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="5e46a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5e46a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e46a-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e46a-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e46a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e46a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e46a-130">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="5e46a-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




