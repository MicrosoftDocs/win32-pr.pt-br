---
description: Fornece os métodos que o WUA pode usar para coletar informações sobre o token de ponto de extremidade.
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: Interface IUpdateEndpointAuthToken (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a5902b3c91b3ab12b311121bd7dcd8c415a68d6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461164"
---
# <a name="iupdateendpointauthtoken-interface"></a><span data-ttu-id="2efb5-103">Interface IUpdateEndpointAuthToken</span><span class="sxs-lookup"><span data-stu-id="2efb5-103">IUpdateEndpointAuthToken interface</span></span>

<span data-ttu-id="2efb5-104">Fornece os métodos que o WUA pode usar para coletar informações sobre o token de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="2efb5-104">Provides the methods that WUA can use to gather information about the endpoint token.</span></span>

## <a name="members"></a><span data-ttu-id="2efb5-105">Membros</span><span class="sxs-lookup"><span data-stu-id="2efb5-105">Members</span></span>

<span data-ttu-id="2efb5-106">A interface **IUpdateEndpointAuthToken** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2efb5-106">The **IUpdateEndpointAuthToken** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2efb5-107">**IUpdateEndpointAuthToken** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2efb5-107">**IUpdateEndpointAuthToken** also has these types of members:</span></span>

-   [<span data-ttu-id="2efb5-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="2efb5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2efb5-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2efb5-109">Methods</span></span>

<span data-ttu-id="2efb5-110">A interface **IUpdateEndpointAuthToken** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2efb5-110">The **IUpdateEndpointAuthToken** interface has these methods.</span></span>



| <span data-ttu-id="2efb5-111">Método</span><span class="sxs-lookup"><span data-stu-id="2efb5-111">Method</span></span>                                                                                | <span data-ttu-id="2efb5-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="2efb5-112">Description</span></span>                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2efb5-113">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="2efb5-113">**ServiceID**</span></span>](iupdateendpointauthtoken-serviceid.md)                               | <span data-ttu-id="2efb5-114">Obtém o identificador do serviço a ser autenticado.</span><span class="sxs-lookup"><span data-stu-id="2efb5-114">Gets the identifier of the service to be authenticated.</span></span><br/>                                                          |
| [<span data-ttu-id="2efb5-115">**SigningKey**</span><span class="sxs-lookup"><span data-stu-id="2efb5-115">**SigningKey**</span></span>](iupdateendpointauthtoken-signingkey.md)                             | <span data-ttu-id="2efb5-116">Obtém a chave usada para assinar mensagens de saída entre o computador cliente e o sercvice.</span><span class="sxs-lookup"><span data-stu-id="2efb5-116">Gets the key used to sign outgoing messages between the client computer and the sercvice.</span></span><br/>                        |
| [<span data-ttu-id="2efb5-117">**TokenData**</span><span class="sxs-lookup"><span data-stu-id="2efb5-117">**TokenData**</span></span>](iupdateendpointauthtoken-tokendata.md)                               | <span data-ttu-id="2efb5-118">Obtém os dados XML (enviados pela transmissão) que representam o token.</span><span class="sxs-lookup"><span data-stu-id="2efb5-118">Gets the XML data (sent over the wire) that represents the token.</span></span> <br/>                                               |
| [<span data-ttu-id="2efb5-119">**TokenReferenceAttached**</span><span class="sxs-lookup"><span data-stu-id="2efb5-119">**TokenReferenceAttached**</span></span>](iupdateendpointauthtoken-tokenreferenceattached.md)     | <span data-ttu-id="2efb5-120">Obtém o formato XML de uma referência anexada ao token.</span><span class="sxs-lookup"><span data-stu-id="2efb5-120">Gets the XML format of an attached reference to the token.</span></span><br/>                                                       |
| [<span data-ttu-id="2efb5-121">**TokenReferenceUnattached**</span><span class="sxs-lookup"><span data-stu-id="2efb5-121">**TokenReferenceUnattached**</span></span>](iupdateendpointauthtoken-tokenreferenceunattached.md) | <span data-ttu-id="2efb5-122">Obtém o formato XML de uma referência desanexada ao token.</span><span class="sxs-lookup"><span data-stu-id="2efb5-122">Gets the XML format of an unattached reference to the token.</span></span><br/>                                                     |
| [<span data-ttu-id="2efb5-123">**TokenType**</span><span class="sxs-lookup"><span data-stu-id="2efb5-123">**TokenType**</span></span>](iupdateendpointauthtoken-tokentype.md)                               | <span data-ttu-id="2efb5-124">Obtém o tipo do token do ponto de extremidade, como um token WS-Security SAML (Security Assertion Markup Language) 1,1.</span><span class="sxs-lookup"><span data-stu-id="2efb5-124">Gets the type of the endpoint token, such as a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="2efb5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2efb5-125">Requirements</span></span>



| <span data-ttu-id="2efb5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2efb5-126">Requirement</span></span> | <span data-ttu-id="2efb5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="2efb5-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2efb5-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2efb5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2efb5-129">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="2efb5-129">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="2efb5-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2efb5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2efb5-131">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="2efb5-131">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="2efb5-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2efb5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2efb5-133"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="2efb5-133"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="2efb5-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="2efb5-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2efb5-135"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2efb5-135"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="2efb5-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2efb5-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="2efb5-137"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2efb5-137"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="2efb5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2efb5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2efb5-139"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2efb5-139"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



 

 
