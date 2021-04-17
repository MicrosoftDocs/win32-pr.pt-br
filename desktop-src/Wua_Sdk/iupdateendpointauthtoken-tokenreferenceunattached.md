---
description: Obtém o formato XML de uma referência desanexada ao token.
ms.assetid: D5D61ED7-68FB-4FC0-9C2A-90D3B1219351
title: 'Método IUpdateEndpointAuthToken:: TokenReferenceUnattached (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceUnattached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 7f9a25c444cf1ba8421d3787a9ead242750e5756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782541"
---
# <a name="iupdateendpointauthtokentokenreferenceunattached-method"></a><span data-ttu-id="35d8f-103">Método IUpdateEndpointAuthToken:: TokenReferenceUnattached</span><span class="sxs-lookup"><span data-stu-id="35d8f-103">IUpdateEndpointAuthToken::TokenReferenceUnattached method</span></span>

<span data-ttu-id="35d8f-104">Obtém o formato XML de uma referência desanexada ao token.</span><span class="sxs-lookup"><span data-stu-id="35d8f-104">Gets the XML format of an unattached reference to the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="35d8f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35d8f-105">Syntax</span></span>


```C++
HRESULT TokenReferenceUnattached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a><span data-ttu-id="35d8f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35d8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35d8f-107">*pszTokenReference* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="35d8f-107">*pszTokenReference* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35d8f-108">Ponteiro para a referência de token desanexado.</span><span class="sxs-lookup"><span data-stu-id="35d8f-108">Pointer to the unattached token reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35d8f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35d8f-109">Return value</span></span>

<span data-ttu-id="35d8f-110">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="35d8f-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="35d8f-111">Caso contrário, retorna um código de erro COM do Windows.</span><span class="sxs-lookup"><span data-stu-id="35d8f-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="35d8f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="35d8f-112">Remarks</span></span>

<span data-ttu-id="35d8f-113">Uma referência desanexada refere-se a um referece (como o assinatura que está usando o token) que não está na mensagem em que o token reside.</span><span class="sxs-lookup"><span data-stu-id="35d8f-113">An unattached reference refers a referece (such as the signiture that is using the token) that is not in the message where the token resides.</span></span>

## <a name="requirements"></a><span data-ttu-id="35d8f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35d8f-114">Requirements</span></span>



| <span data-ttu-id="35d8f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="35d8f-115">Requirement</span></span> | <span data-ttu-id="35d8f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="35d8f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35d8f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35d8f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="35d8f-118">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="35d8f-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="35d8f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35d8f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="35d8f-120">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="35d8f-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="35d8f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35d8f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="35d8f-122"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="35d8f-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="35d8f-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="35d8f-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35d8f-124"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="35d8f-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="35d8f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35d8f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="35d8f-126"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35d8f-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="35d8f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="35d8f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35d8f-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35d8f-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35d8f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="35d8f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d8f-130">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="35d8f-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




