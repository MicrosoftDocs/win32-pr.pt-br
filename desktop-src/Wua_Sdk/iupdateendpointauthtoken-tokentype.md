---
description: Obtém o tipo do token do ponto de extremidade, como um token WS-Security SAML (Security Assertion Markup Language) 1,1.
ms.assetid: 1C6FFAD7-DC80-4957-96B4-FA0D954786DD
title: 'Método IUpdateEndpointAuthToken:: TokenType (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bc2373c5dd49a3bf01d39b63360a3cf9df9f57d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501864"
---
# <a name="iupdateendpointauthtokentokentype-method"></a><span data-ttu-id="2d35f-103">Método IUpdateEndpointAuthToken:: TokenType</span><span class="sxs-lookup"><span data-stu-id="2d35f-103">IUpdateEndpointAuthToken::TokenType method</span></span>

<span data-ttu-id="2d35f-104">Obtém o tipo do token do ponto de extremidade, como um token WS-Security SAML (Security Assertion Markup Language) 1,1.</span><span class="sxs-lookup"><span data-stu-id="2d35f-104">Gets the type of the endpoint token, such as a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d35f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d35f-105">Syntax</span></span>


```C++
HRESULT TokenType(
  [out] UpdateEndpointAuthTokenType *pTokenType
);
```



## <a name="parameters"></a><span data-ttu-id="2d35f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d35f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d35f-107">*pTokenType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2d35f-107">*pTokenType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d35f-108">O tipo do token de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="2d35f-108">The type of the endpoint token.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d35f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d35f-109">Return value</span></span>

<span data-ttu-id="2d35f-110">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2d35f-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="2d35f-111">Caso contrário, retorna um código de erro COM do Windows.</span><span class="sxs-lookup"><span data-stu-id="2d35f-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d35f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d35f-112">Requirements</span></span>



| <span data-ttu-id="2d35f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d35f-113">Requirement</span></span> | <span data-ttu-id="2d35f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="2d35f-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d35f-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d35f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2d35f-116">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="2d35f-116">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="2d35f-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d35f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2d35f-118">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="2d35f-118">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="2d35f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d35f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d35f-120"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d35f-120"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d35f-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="2d35f-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2d35f-122"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d35f-122"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="2d35f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d35f-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="2d35f-124"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d35f-124"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="2d35f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2d35f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d35f-126"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d35f-126"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d35f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d35f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d35f-128">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="2d35f-128">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




