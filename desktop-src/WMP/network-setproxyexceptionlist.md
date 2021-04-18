---
title: Método Network. setProxyExceptionList
description: O método setProxyExceptionList especifica a lista de exceções de proxy. | Método Network. setProxyExceptionList
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- método setProxyExceptionList Windows Media Player
- método setProxyExceptionList Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método setProxyExceptionList
topic_type:
- apiref
api_name:
- Network.setProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1e48aa91ec4857181de5c607a586da42d6f2cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763838"
---
# <a name="networksetproxyexceptionlist-method"></a><span data-ttu-id="480b2-107">Método Network. setProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="480b2-107">Network.setProxyExceptionList method</span></span>

<span data-ttu-id="480b2-108">O método **setProxyExceptionList** especifica a lista de exceções de proxy.</span><span class="sxs-lookup"><span data-stu-id="480b2-108">The **setProxyExceptionList** method specifies the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="480b2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="480b2-109">Syntax</span></span>


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a><span data-ttu-id="480b2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="480b2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="480b2-111">*protocolo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="480b2-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="480b2-112">**Cadeia de caracteres** que especifica o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="480b2-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="480b2-113">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="480b2-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="480b2-114">*lista* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="480b2-114">*list* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="480b2-115">**Cadeia de caracteres** que especifica uma lista delimitada por ponto-e-vírgula de hosts para os quais o servidor proxy é ignorado.</span><span class="sxs-lookup"><span data-stu-id="480b2-115">**String** specifying a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="480b2-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="480b2-116">Return value</span></span>

<span data-ttu-id="480b2-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="480b2-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="480b2-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="480b2-118">Remarks</span></span>

<span data-ttu-id="480b2-119">Esta é uma lista de computadores, domínios e/ou endereços que irão ignorar o servidor proxy quando a parte do host da URL de destino corresponder a uma entrada na lista.</span><span class="sxs-lookup"><span data-stu-id="480b2-119">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="480b2-120">O \* caractere pode ser usado como um caractere curinga para listar entradas.</span><span class="sxs-lookup"><span data-stu-id="480b2-120">The \* character can be used as a wildcard for listing entries.</span></span> <span data-ttu-id="480b2-121">Por exemplo, \* . com corresponderia a todos os hosts no domínio com, enquanto 67. \* corresponderia a todos os hosts da classe 67 uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="480b2-121">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="480b2-122">Esse método não tem efeito, a menos que **getProxySettings** retorne um valor de 2 (use as configurações manuais).</span><span class="sxs-lookup"><span data-stu-id="480b2-122">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="480b2-123">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="480b2-123">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="480b2-124">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="480b2-124">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="480b2-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="480b2-125">Examples</span></span>

<span data-ttu-id="480b2-126">O exemplo de JScript a seguir usa a *rede*. **setProxyExceptionList** para especificar uma lista de hosts para os quais o servidor proxy é ignorado ao usar o protocolo MMS.</span><span class="sxs-lookup"><span data-stu-id="480b2-126">The following JScript example uses *Network*.**setProxyExceptionList** to specify a list of hosts for which the proxy server is bypassed when using the MMS protocol.</span></span> <span data-ttu-id="480b2-127">A nova lista é recuperada de um elemento de texto HTML com ID = "XLIST".</span><span class="sxs-lookup"><span data-stu-id="480b2-127">The new list is retrieved from an HTML TEXT element with ID = "XLIST".</span></span> <span data-ttu-id="480b2-128">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="480b2-128">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the user's new exception list.
   var proxyxlist = XLIST.value;

   // Set the exception list.
   Player.network.setProxyExceptionList("MMS", proxyxlist);
}

else

// Warn that the proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="480b2-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="480b2-129">Requirements</span></span>



| <span data-ttu-id="480b2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="480b2-130">Requirement</span></span> | <span data-ttu-id="480b2-131">Valor</span><span class="sxs-lookup"><span data-stu-id="480b2-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="480b2-132">Versão</span><span class="sxs-lookup"><span data-stu-id="480b2-132">Version</span></span><br/> | <span data-ttu-id="480b2-133">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="480b2-133">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="480b2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="480b2-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="480b2-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="480b2-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="480b2-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="480b2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="480b2-137">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="480b2-137">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





