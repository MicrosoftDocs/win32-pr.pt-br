---
title: Método Network. getproxyname
description: O método getproxyname recupera o nome do servidor proxy que está sendo usado.
ms.assetid: 273b1f7d-84b7-4e50-9f80-9fd1978e7528
keywords:
- método getproxyname do Windows Media Player
- método getproxyname Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método getproxyname
topic_type:
- apiref
api_name:
- Network.getProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97e51508e9df9aeac85dbc01116e80e710dcb45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771543"
---
# <a name="networkgetproxyname-method"></a><span data-ttu-id="21199-106">Método Network. getproxyname</span><span class="sxs-lookup"><span data-stu-id="21199-106">Network.getProxyName method</span></span>

<span data-ttu-id="21199-107">O método **Getproxyname** recupera o nome do servidor proxy que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="21199-107">The **getProxyName** method retrieves the name of the proxy server being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="21199-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21199-108">Syntax</span></span>


```JScript
strRetVal = Network.getProxyName(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="21199-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21199-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21199-110">*protocolo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="21199-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21199-111">**Cadeia de caracteres** que especifica o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="21199-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="21199-112">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="21199-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21199-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="21199-113">Return value</span></span>

<span data-ttu-id="21199-114">Esse método retorna uma **cadeia de caracteres** que contém o nome do servidor proxy que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="21199-114">This method returns a **String** containing the name of the proxy server being used.</span></span> <span data-ttu-id="21199-115">O valor retornado é significativo somente quando **getProxySettings** retorna um valor de 2 (use configurações manuais).</span><span class="sxs-lookup"><span data-stu-id="21199-115">The value returned is meaningful only when **getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="21199-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="21199-116">Remarks</span></span>

<span data-ttu-id="21199-117">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="21199-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="21199-118">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="21199-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="21199-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="21199-119">Examples</span></span>

<span data-ttu-id="21199-120">O exemplo de JScript a seguir usa a *rede*. **Getproxyname** para exibir os nomes do servidor proxy do Windows Media Player para os protocolos http e MMS.</span><span class="sxs-lookup"><span data-stu-id="21199-120">The following JScript example uses *Network*.**getProxyName** to display the Windows Media Player proxy server names for the HTTP and MMS protocols.</span></span> <span data-ttu-id="21199-121">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="21199-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy server name for HTTP.
   var proxyNameHTTP = Player.network.getProxyName("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy server name for MMS.
   var proxyNameMMS = Player.network.getProxyName("MMS");

// Display the proxy server names in the browser client area.
// Unavailable proxy server names will display as "undefined".
document.write("The current HTTP proxy server name is: " + proxyNameHTTP);
document.write("<BR>");
document.write("The current MMS proxy server name is: " + proxyNameMMS);

```



## <a name="requirements"></a><span data-ttu-id="21199-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21199-122">Requirements</span></span>



| <span data-ttu-id="21199-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="21199-123">Requirement</span></span> | <span data-ttu-id="21199-124">Valor</span><span class="sxs-lookup"><span data-stu-id="21199-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="21199-125">Versão</span><span class="sxs-lookup"><span data-stu-id="21199-125">Version</span></span><br/> | <span data-ttu-id="21199-126">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="21199-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="21199-127">DLL</span><span class="sxs-lookup"><span data-stu-id="21199-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="21199-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21199-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21199-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="21199-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21199-130">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="21199-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="21199-131">**Network. getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="21199-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





