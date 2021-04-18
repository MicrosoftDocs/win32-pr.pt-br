---
title: Método Network. getProxyExceptionList
description: O método getProxyExceptionList recupera a lista de exceções de proxy.
ms.assetid: f81d8c0f-cc75-470c-9c24-ceaf8a4b6f97
keywords:
- método getProxyExceptionList Windows Media Player
- método getProxyExceptionList Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método getProxyExceptionList
topic_type:
- apiref
api_name:
- Network.getProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ace9bd569c1cc53a8f3d522703aee6154e68a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772934"
---
# <a name="networkgetproxyexceptionlist-method"></a><span data-ttu-id="37223-106">Método Network. getProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="37223-106">Network.getProxyExceptionList method</span></span>

<span data-ttu-id="37223-107">O método **getProxyExceptionList** recupera a lista de exceções de proxy.</span><span class="sxs-lookup"><span data-stu-id="37223-107">The **getProxyExceptionList** method retrieves the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="37223-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37223-108">Syntax</span></span>


```JScript
strRetVal = Network.getProxyExceptionList(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="37223-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37223-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37223-110">*protocolo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="37223-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37223-111">**Cadeia de caracteres** que especifica o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="37223-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="37223-112">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="37223-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37223-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37223-113">Return value</span></span>

<span data-ttu-id="37223-114">Esse método retorna uma **cadeia de caracteres** especificando uma lista delimitada por ponto-e-vírgula de hosts para os quais o servidor proxy é ignorado.</span><span class="sxs-lookup"><span data-stu-id="37223-114">This method returns a **String** specifying a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="37223-115">O valor retornado é significativo somente quando **getProxySettings** retorna um valor de dois (use configurações manuais).</span><span class="sxs-lookup"><span data-stu-id="37223-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="37223-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="37223-116">Remarks</span></span>

<span data-ttu-id="37223-117">Esta é uma lista de computadores, domínios e/ou endereços que irão ignorar o servidor proxy quando a parte do host da URL de destino corresponder a uma entrada na lista.</span><span class="sxs-lookup"><span data-stu-id="37223-117">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="37223-118">O \* caractere pode ser usado como um caractere curinga para listar entradas.</span><span class="sxs-lookup"><span data-stu-id="37223-118">The \* character can be used as a wildcard for listing entries.</span></span> <span data-ttu-id="37223-119">Por exemplo, \* . com corresponderia a todos os hosts no domínio com, enquanto 67. \* corresponderia a todos os hosts da classe 67 uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="37223-119">For example, \*.com would match all hosts in the com domain while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="37223-120">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="37223-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="37223-121">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="37223-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="37223-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="37223-122">Examples</span></span>

<span data-ttu-id="37223-123">O exemplo de JScript a seguir usa a *rede*. **getProxyExceptionList** para exibir as listas de proxies ignorados para os protocolos MMS e http.</span><span class="sxs-lookup"><span data-stu-id="37223-123">The following JScript example uses *Network*.**getProxyExceptionList** to display the lists of bypassed proxies for the MMS and HTTP protocols.</span></span> <span data-ttu-id="37223-124">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="37223-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy exception list for HTTP.
   var proxyExceptionListHTTP = Player.network.getProxyExceptionList("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy exception list for MMS.
   var proxyExceptionListMMS = Player.network.getProxyExceptionList("MMS");

// Display the proxy exception lists in the browser client area.
// Unavailable proxy exception lists will display as "undefined".
document.write("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
document.write("<BR>");
document.write("The current MMS proxy exception list: " + proxyExceptionListMMS);

```



## <a name="requirements"></a><span data-ttu-id="37223-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37223-125">Requirements</span></span>



| <span data-ttu-id="37223-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="37223-126">Requirement</span></span> | <span data-ttu-id="37223-127">Valor</span><span class="sxs-lookup"><span data-stu-id="37223-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37223-128">Versão</span><span class="sxs-lookup"><span data-stu-id="37223-128">Version</span></span><br/> | <span data-ttu-id="37223-129">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="37223-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="37223-130">DLL</span><span class="sxs-lookup"><span data-stu-id="37223-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="37223-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37223-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37223-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="37223-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37223-133">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="37223-133">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="37223-134">**Network. getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="37223-134">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





