---
description: A estrutura UpdateEndpointProxySettings define as configurações de proxy usadas ao solicitar um token.
ms.assetid: 24AA8843-D4EE-4F17-8B96-63ED25B365D2
title: Estrutura UpdateEndpointProxySettings (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointProxySettings
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: aad6ad294baab37b7516152438dbc9fd05f7036a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010541"
---
# <a name="updateendpointproxysettings-structure"></a><span data-ttu-id="2e143-103">Estrutura UpdateEndpointProxySettings</span><span class="sxs-lookup"><span data-stu-id="2e143-103">UpdateEndpointProxySettings structure</span></span>

<span data-ttu-id="2e143-104">A estrutura **UpdateEndpointProxySettings** define as configurações de proxy usadas ao solicitar um token.</span><span class="sxs-lookup"><span data-stu-id="2e143-104">The **UpdateEndpointProxySettings** structure defines the proxy settings used when requesting a token.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e143-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e143-105">Syntax</span></span>


```C++
typedef struct tagUpdateEndpointProxySettings {
  BSTR szProxyAddr;
  BSTR szBypassList;
  BSTR szUserName;
  BSTR szPassword;
} UpdateEndpointProxySettings;
```



## <a name="members"></a><span data-ttu-id="2e143-106">Membros</span><span class="sxs-lookup"><span data-stu-id="2e143-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2e143-107">**szProxyAddr**</span><span class="sxs-lookup"><span data-stu-id="2e143-107">**szProxyAddr**</span></span>
</dt> <dd>

<span data-ttu-id="2e143-108">O nome DNS ou o endereço IP do servidor proxy a ser usado (por exemplo, "proxy.somecorp.com" ou "192.168.0.4") ou uma cadeia de caracteres vazia se não for necessário usar nenhum proxy.</span><span class="sxs-lookup"><span data-stu-id="2e143-108">The DNS name or IP address of the proxy server to use (for example, "proxy.somecorp.com" or "192.168.0.4"), or an empty string if no proxy should be used.</span></span>

</dd> <dt>

<span data-ttu-id="2e143-109">**szBypassList**</span><span class="sxs-lookup"><span data-stu-id="2e143-109">**szBypassList**</span></span>
</dt> <dd>

<span data-ttu-id="2e143-110">Uma lista de endereços de host que devem ignorar o servidor proxy ou uma cadeia de caracteres vazia se todos os endereços de host tiverem que usar o servidor proxy</span><span class="sxs-lookup"><span data-stu-id="2e143-110">A list of host addresses that should bypass the proxy server, or an empty string if all host addresses should use the proxy server</span></span>

<span data-ttu-id="2e143-111">O WUA não usará esses dados se **szProxyAddr** estiver vazio.</span><span class="sxs-lookup"><span data-stu-id="2e143-111">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> <dt>

<span data-ttu-id="2e143-112">**szUserName**</span><span class="sxs-lookup"><span data-stu-id="2e143-112">**szUserName**</span></span>
</dt> <dd>

<span data-ttu-id="2e143-113">O nome de usuário que é usado para autenticar com o servidor proxy ou a cadeia de caracteres vazia se nenhuma autenticação for necessária.</span><span class="sxs-lookup"><span data-stu-id="2e143-113">The username that is used to authenticate with the proxy server, or the empty string if no authentication is needed.</span></span>

<span data-ttu-id="2e143-114">O WUA não usará esses dados se **szProxyAddr** estiver vazio.</span><span class="sxs-lookup"><span data-stu-id="2e143-114">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> <dt>

<span data-ttu-id="2e143-115">**szPassword**</span><span class="sxs-lookup"><span data-stu-id="2e143-115">**szPassword**</span></span>
</dt> <dd>

<span data-ttu-id="2e143-116">A senha usada para autenticar com o servidor proxy ou a cadeia de caracteres vazia se nenhuma autenticação for necessária.</span><span class="sxs-lookup"><span data-stu-id="2e143-116">The password that is used to authenticate with the proxy server, or the empty string if no authentication is needed.</span></span>

<span data-ttu-id="2e143-117">O WUA não usará esses dados se **szProxyAddr** estiver vazio.</span><span class="sxs-lookup"><span data-stu-id="2e143-117">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e143-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e143-118">Requirements</span></span>



| <span data-ttu-id="2e143-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e143-119">Requirement</span></span> | <span data-ttu-id="2e143-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2e143-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e143-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e143-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2e143-122">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2e143-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="2e143-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e143-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2e143-124">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2e143-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="2e143-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e143-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e143-126"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e143-126"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e143-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="2e143-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e143-128"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e143-128"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e143-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e143-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e143-130">**GetEndpointToken**</span><span class="sxs-lookup"><span data-stu-id="2e143-130">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




