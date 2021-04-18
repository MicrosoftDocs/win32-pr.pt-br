---
description: Define o tipo de tokens que podem ser usados para autenticação com um ponto de extremidade.
ms.assetid: 2048BD09-056F-47C1-AD2F-998DE6C52EA6
title: Enumeração UpdateEndpointAuthTokenType (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointAuthTokenType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: c978841511b7cfff895a15936a41d169a8500927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788731"
---
# <a name="updateendpointauthtokentype-enumeration"></a><span data-ttu-id="eb508-103">Enumeração UpdateEndpointAuthTokenType</span><span class="sxs-lookup"><span data-stu-id="eb508-103">UpdateEndpointAuthTokenType enumeration</span></span>

<span data-ttu-id="eb508-104">Define o tipo de tokens que podem ser usados para autenticação com um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="eb508-104">Defines the type of tokens that can be used for authenticating with an endpoint.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb508-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb508-105">Syntax</span></span>


```C++
typedef enum tagUpdateEndpointAuthTokenType { 
  ueattInvalidTokenType  = 0x0,
  ueattSAML11Token       = 0X1
} UpdateEndpointAuthTokenType;
```



## <a name="constants"></a><span data-ttu-id="eb508-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="eb508-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="eb508-107"><span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**</span><span class="sxs-lookup"><span data-stu-id="eb508-107"><span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**</span></span>
</dt> <dd>

<span data-ttu-id="eb508-108">Nenhum token de autenticação é necessário.</span><span class="sxs-lookup"><span data-stu-id="eb508-108">No authentication token is needed.</span></span>

</dd> <dt>

<span data-ttu-id="eb508-109"><span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**</span><span class="sxs-lookup"><span data-stu-id="eb508-109"><span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**</span></span>
</dt> <dd>

<span data-ttu-id="eb508-110">O token de autenticação para o ponto de extremidade é um token WS-Security SAML (Security Assertion Markup Language) 1,1.</span><span class="sxs-lookup"><span data-stu-id="eb508-110">The authentication token for the endpoint is a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb508-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb508-111">Requirements</span></span>



| <span data-ttu-id="eb508-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb508-112">Requirement</span></span> | <span data-ttu-id="eb508-113">Valor</span><span class="sxs-lookup"><span data-stu-id="eb508-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb508-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb508-114">Minimum supported client</span></span><br/> | <span data-ttu-id="eb508-115">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="eb508-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="eb508-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb508-116">Minimum supported server</span></span><br/> | <span data-ttu-id="eb508-117">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="eb508-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="eb508-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb508-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb508-119"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb508-119"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb508-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="eb508-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eb508-121"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eb508-121"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



 

 




