---
title: Constantes de nível de autenticação (rpcdce. h)
description: Esses valores especificam um nível de autenticação, que indica a quantidade de autenticação fornecida para ajudar a proteger a integridade dos dados. Cada nível inclui a proteção fornecida pelos níveis anteriores.
ms.assetid: 06c409e4-3772-45cf-8c31-c64f99aca244
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf922118a1b332bfe1fe8e744114a6d1d6bf4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499802"
---
# <a name="authentication-level-constants"></a><span data-ttu-id="e8f52-104">Constantes de nível de autenticação</span><span class="sxs-lookup"><span data-stu-id="e8f52-104">Authentication Level Constants</span></span>

<span data-ttu-id="e8f52-105">Esses valores especificam um nível de autenticação, que indica a quantidade de autenticação fornecida para ajudar a proteger a integridade dos dados.</span><span class="sxs-lookup"><span data-stu-id="e8f52-105">These values specify an authentication level, which indicates the amount of authentication provided to help protect the integrity of the data.</span></span> <span data-ttu-id="e8f52-106">Cada nível inclui a proteção fornecida pelos níveis anteriores.</span><span class="sxs-lookup"><span data-stu-id="e8f52-106">Each level includes the protection provided by the previous levels.</span></span>



| <span data-ttu-id="e8f52-107">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="e8f52-107">Constant/value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="e8f52-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8f52-108">Description</span></span>                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <span data-ttu-id="e8f52-109"><dt>**RPC \_ \_ \_ \_ Padrão de nível de autenticação C**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e8f52-109"><dt>**RPC\_C\_AUTHN\_LEVEL\_DEFAULT**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="e8f52-110">Informa ao DCOM para escolher o nível de autenticação usando seu algoritmo normal de negociação ampla de segurança.</span><span class="sxs-lookup"><span data-stu-id="e8f52-110">Tells DCOM to choose the authentication level using its normal security blanket negotiation algorithm.</span></span> <span data-ttu-id="e8f52-111">Para obter mais informações, consulte [negociação de cobertura de segurança](security-blanket-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="e8f52-111">For more information, see [Security Blanket Negotiation](security-blanket-negotiation.md).</span></span> <br/> |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <span data-ttu-id="e8f52-112"><dt>**RPC \_ C \_ Authn \_ nível \_ nenhum**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e8f52-112"><dt>**RPC\_C\_AUTHN\_LEVEL\_NONE**</dt> <dt>1</dt></span></span> </dl>                             | <span data-ttu-id="e8f52-113">Não executa nenhuma autenticação.</span><span class="sxs-lookup"><span data-stu-id="e8f52-113">Performs no authentication.</span></span><br/>                                                                                                                                                                         |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <span data-ttu-id="e8f52-114"><dt>**RPC \_ C \_ Authn \_ nível \_ Connect**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e8f52-114"><dt>**RPC\_C\_AUTHN\_LEVEL\_CONNECT**</dt> <dt>2</dt></span></span> </dl>                    | <span data-ttu-id="e8f52-115">Autentica as credenciais do cliente somente quando o cliente estabelece uma relação com o servidor.</span><span class="sxs-lookup"><span data-stu-id="e8f52-115">Authenticates the credentials of the client only when the client establishes a relationship with the server.</span></span> <span data-ttu-id="e8f52-116">Os transportes de datagrama sempre usam o \_ PCT de nível de autenticação RPC \_ \_ em vez disso.</span><span class="sxs-lookup"><span data-stu-id="e8f52-116">Datagram transports always use RPC\_AUTHN\_LEVEL\_PKT instead.</span></span> <br/>                        |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <span data-ttu-id="e8f52-117"><dt>**RPC \_ \_ \_ \_ Chamada de nível**</dt> <dt>3</dt> da autenticação C</span><span class="sxs-lookup"><span data-stu-id="e8f52-117"><dt>**RPC\_C\_AUTHN\_LEVEL\_CALL**</dt> <dt>3</dt></span></span> </dl>                             | <span data-ttu-id="e8f52-118">Autentica somente no início de cada chamada de procedimento remoto quando o servidor recebe a solicitação.</span><span class="sxs-lookup"><span data-stu-id="e8f52-118">Authenticates only at the beginning of each remote procedure call when the server receives the request.</span></span> <span data-ttu-id="e8f52-119">Os transportes de datagramas usam RPC \_ C \_ Authn \_ nível \_ pkt.</span><span class="sxs-lookup"><span data-stu-id="e8f52-119">Datagram transports use RPC\_C\_AUTHN\_LEVEL\_PKT instead.</span></span><br/>                                  |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <span data-ttu-id="e8f52-120"><dt>**RPC \_ C \_ Authn \_ nível \_ de autenticação**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e8f52-120"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT**</dt> <dt>4</dt></span></span> </dl>                                | <span data-ttu-id="e8f52-121">Autentica que todos os dados recebidos são do cliente esperado.</span><span class="sxs-lookup"><span data-stu-id="e8f52-121">Authenticates that all data received is from the expected client.</span></span><br/>                                                                                                                                   |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <span data-ttu-id="e8f52-122"><dt>**RPC \_ \_Integridade de \_ pkt do \_ nível \_ de autenticação C**</dt> . <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e8f52-122"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="e8f52-123">Autentica e verifica se nenhum dos dados transferidos entre o cliente e o servidor foi modificado.</span><span class="sxs-lookup"><span data-stu-id="e8f52-123">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                           |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <span data-ttu-id="e8f52-124"><dt>**RPC \_ \_Privacidade do \_ PCT do \_ nível \_ da autenticação**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e8f52-124"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="e8f52-125">Autentica todos os níveis anteriores e criptografa o valor do argumento de cada chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="e8f52-125">Authenticates all previous levels and encrypts the argument value of each remote procedure call.</span></span><br/>                                                                                                    |



## <a name="requirements"></a><span data-ttu-id="e8f52-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8f52-126">Requirements</span></span>



| <span data-ttu-id="e8f52-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8f52-127">Requirement</span></span> | <span data-ttu-id="e8f52-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e8f52-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e8f52-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8f52-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e8f52-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e8f52-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e8f52-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8f52-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e8f52-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e8f52-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e8f52-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e8f52-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8f52-134"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8f52-134"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





