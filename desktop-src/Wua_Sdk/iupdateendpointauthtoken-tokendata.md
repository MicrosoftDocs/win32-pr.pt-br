---
description: Obtém os dados XML (enviados pela transmissão) que representam o token.
ms.assetid: 52EC991A-0499-4182-AC4F-512BAFB4F896
title: 'Método IUpdateEndpointAuthToken:: TokenData (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenData
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: e75df7f5b13eaf36854cf7ed9abc5988b02462ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765016"
---
# <a name="iupdateendpointauthtokentokendata-method"></a><span data-ttu-id="f6973-103">Método IUpdateEndpointAuthToken:: TokenData</span><span class="sxs-lookup"><span data-stu-id="f6973-103">IUpdateEndpointAuthToken::TokenData method</span></span>

<span data-ttu-id="f6973-104">Obtém os dados XML (enviados pela transmissão) que representam o token.</span><span class="sxs-lookup"><span data-stu-id="f6973-104">Gets the XML data (sent over the wire) that represents the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6973-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6973-105">Syntax</span></span>


```C++
HRESULT TokenData(
  [out] BSTR *pszTokenData
);
```



## <a name="parameters"></a><span data-ttu-id="f6973-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6973-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6973-107">*pszTokenData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f6973-107">*pszTokenData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6973-108">Os dados XML (enviados pela transmissão) que representam o token.</span><span class="sxs-lookup"><span data-stu-id="f6973-108">The XML data (sent over the wire) that represents the token.</span></span> <span data-ttu-id="f6973-109">Por exemplo, os dados de um token WS-Security SAML (Security Assertion Markup Language) 1,1 é o código SAML que é adicionado à solicitação.</span><span class="sxs-lookup"><span data-stu-id="f6973-109">For example, the data for a WS-Security SAML (Security Assertion Markup Language) 1.1 token is the SAML code that is added to the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6973-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6973-110">Return value</span></span>

<span data-ttu-id="f6973-111">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f6973-111">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="f6973-112">Caso contrário, retorna um código de erro COM do Windows.</span><span class="sxs-lookup"><span data-stu-id="f6973-112">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6973-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6973-113">Requirements</span></span>



| <span data-ttu-id="f6973-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6973-114">Requirement</span></span> | <span data-ttu-id="f6973-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f6973-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6973-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6973-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f6973-117">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="f6973-117">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="f6973-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6973-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f6973-119">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="f6973-119">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="f6973-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f6973-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6973-121"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6973-121"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6973-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="f6973-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f6973-123"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f6973-123"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="f6973-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6973-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="f6973-125"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6973-125"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="f6973-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f6973-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6973-127"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6973-127"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6973-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6973-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6973-129">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="f6973-129">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




