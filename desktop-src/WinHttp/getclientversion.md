---
description: Obtém a versão do mecanismo de processamento WPAD.
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: função getClientVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0bcf439c8a282e42a28126824ffb70630a341e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828945"
---
# <a name="getclientversion-function"></a><span data-ttu-id="b5b2b-103">função getClientVersion</span><span class="sxs-lookup"><span data-stu-id="b5b2b-103">getClientVersion function</span></span>

<span data-ttu-id="b5b2b-104">Obtém a versão do mecanismo de processamento WPAD.</span><span class="sxs-lookup"><span data-stu-id="b5b2b-104">Gets the version of the WPAD processing engine.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5b2b-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5b2b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5b2b-106">*IpAddresslist*</span><span class="sxs-lookup"><span data-stu-id="b5b2b-106">*IpAddressList*</span></span> 
</dt> <dd>

<span data-ttu-id="b5b2b-107">Uma cadeia de caracteres delimitada por ponto e vírgula contendo endereços IP.</span><span class="sxs-lookup"><span data-stu-id="b5b2b-107">A semi-colon delimited string containing IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5b2b-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5b2b-108">Return value</span></span>

<span data-ttu-id="b5b2b-109">Uma lista de endereços IP delimitados por ponto-e-vírgula ou uma cadeia de caracteres vazia se não for possível classificar a lista de endereços IP.</span><span class="sxs-lookup"><span data-stu-id="b5b2b-109">A list of sorted semi-colon delimited IP addresses or an empty string if unable to sort the IP Address list.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5b2b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5b2b-110">Remarks</span></span>

<span data-ttu-id="b5b2b-111">Atualmente, essa função retorna a versão 1,0.</span><span class="sxs-lookup"><span data-stu-id="b5b2b-111">Currently this function returns version 1.0.</span></span>

<span data-ttu-id="b5b2b-112">A Microsoft adicionou essa função para permitir que os administradores de ti atualizem seus scripts WPAD para usar versões diferentes do mecanismo de processamento WPAD sem causar interrupções na implantação existente.</span><span class="sxs-lookup"><span data-stu-id="b5b2b-112">Microsoft added this function to allow IT administrators to update their WPAD scripts to use different versions of the WPAD processing engine without causing breaks to their existing deployment.</span></span> <span data-ttu-id="b5b2b-113">Por exemplo, se a Microsoft tiver adicionado uma função à versão 2,0 do mecanismo WPAD, os administradores poderão verificar a versão antes de tentar chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="b5b2b-113">For example, if Microsoft added a function to the 2.0 version of the WPAD engine, then administrators can check the version before attempting to call that function.</span></span> <span data-ttu-id="b5b2b-114">Isso permite que o script funcione com o cliente executando as versões 1,0 e 2,0 do mecanismo WPAD.</span><span class="sxs-lookup"><span data-stu-id="b5b2b-114">This allows their script to work with client running versions 1.0 and 2.0 of the WPAD engine.</span></span>

## <a name="examples"></a><span data-ttu-id="b5b2b-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b5b2b-115">Examples</span></span>

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a><span data-ttu-id="b5b2b-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5b2b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5b2b-117">Definições da API auxiliar de proxy com reconhecimento de IPv6</span><span class="sxs-lookup"><span data-stu-id="b5b2b-117">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="b5b2b-118">Formato de arquivo de configuração automática de extensões IPv6 para navegador</span><span class="sxs-lookup"><span data-stu-id="b5b2b-118">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



