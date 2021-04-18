---
title: Método Network. getProxyBypassForLocal
description: O método getProxyBypassForLocal recupera um valor que indica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- método getProxyBypassForLocal Windows Media Player
- método getProxyBypassForLocal Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método getProxyBypassForLocal
topic_type:
- apiref
api_name:
- Network.getProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60b9248cd5a893496c2de88c5a5370dfb7bf82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760542"
---
# <a name="networkgetproxybypassforlocal-method"></a><span data-ttu-id="8269d-106">Método Network. getProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="8269d-106">Network.getProxyBypassForLocal method</span></span>

<span data-ttu-id="8269d-107">O método **getProxyBypassForLocal** recupera um valor que indica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.</span><span class="sxs-lookup"><span data-stu-id="8269d-107">The **getProxyBypassForLocal** method retrieves a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="8269d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8269d-108">Syntax</span></span>


```JScript
bRetVal = Network.getProxyBypassForLocal(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="8269d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8269d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8269d-110">*protocolo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="8269d-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8269d-111">**Cadeia de caracteres** que especifica o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="8269d-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="8269d-112">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="8269d-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8269d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8269d-113">Return value</span></span>

<span data-ttu-id="8269d-114">Esse método retorna um **valor booleano** que indica se o servidor proxy é ignorado.</span><span class="sxs-lookup"><span data-stu-id="8269d-114">This method returns a **Boolean** indicating whether the proxy server is bypassed.</span></span> <span data-ttu-id="8269d-115">O valor retornado é significativo somente quando **getProxySettings** retorna um valor de dois (use configurações manuais).</span><span class="sxs-lookup"><span data-stu-id="8269d-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="8269d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8269d-116">Remarks</span></span>

<span data-ttu-id="8269d-117">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="8269d-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="8269d-118">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="8269d-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="8269d-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8269d-119">Examples</span></span>

<span data-ttu-id="8269d-120">O exemplo de JScript a seguir usa a *rede*. **getProxyBypassForLocal** para exibir se o Windows Media Player está definido para ignorar o servidor proxy para endereços locais.</span><span class="sxs-lookup"><span data-stu-id="8269d-120">The following JScript example uses *Network*.**getProxyBypassForLocal** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="8269d-121">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="8269d-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy bypass for local value for HTTP.
   var proxyBypassForLocalHTTP = Player.network.getProxyBypassForLocal("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy bypass for local value for MMS.
   var proxyBypassForLocalMMS = Player.network.getProxyBypassForLocal("MMS");

// Display the proxy bypass for local values in the browser client area.
// Unavailable proxy bypass for local values will display as "undefined".
document.write("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP);
document.write("<BR>");
document.write("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS);

```



## <a name="requirements"></a><span data-ttu-id="8269d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8269d-122">Requirements</span></span>



| <span data-ttu-id="8269d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8269d-123">Requirement</span></span> | <span data-ttu-id="8269d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8269d-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8269d-125">Versão</span><span class="sxs-lookup"><span data-stu-id="8269d-125">Version</span></span><br/> | <span data-ttu-id="8269d-126">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="8269d-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8269d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8269d-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="8269d-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8269d-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8269d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8269d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8269d-130">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="8269d-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="8269d-131">**Network. getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="8269d-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





