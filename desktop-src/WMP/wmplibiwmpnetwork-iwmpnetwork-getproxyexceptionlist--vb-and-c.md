---
title: Método IWMPNetwork getProxyExceptionList
description: O método getProxyExceptionList retorna a lista de exceções de proxy.
ms.assetid: 1b209d75-0fa7-420e-831c-160f3826cf3a
keywords:
- método getProxyExceptionList Windows Media Player
- método getProxyExceptionList Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, método getProxyExceptionList
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402e3b28d5423314b499213c9ddb02bca482d629
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753901"
---
# <a name="iwmpnetworkgetproxyexceptionlist-method"></a><span data-ttu-id="f86c4-106">Método IWMPNetwork:: getProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="f86c4-106">IWMPNetwork::getProxyExceptionList method</span></span>

<span data-ttu-id="f86c4-107">O método **getProxyExceptionList** retorna a lista de exceções de proxy.</span><span class="sxs-lookup"><span data-stu-id="f86c4-107">The **getProxyExceptionList** method returns the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f86c4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f86c4-108">Syntax</span></span>


```CSharp
public System.String getProxyExceptionList(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyExceptionList( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyExceptionList
```





## <a name="parameters"></a><span data-ttu-id="f86c4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f86c4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f86c4-110">*bstrProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f86c4-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f86c4-111">Um **System. String** que é o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="f86c4-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="f86c4-112">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="f86c4-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f86c4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f86c4-113">Return value</span></span>

<span data-ttu-id="f86c4-114">Um **System. String** que é uma lista delimitada por ponto-e-vírgula de hosts para os quais o servidor proxy é ignorado.</span><span class="sxs-lookup"><span data-stu-id="f86c4-114">A **System.String** that is a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="f86c4-115">O valor é significativo somente quando **IWMPNetwork. getProxySettings** retorna um valor de 2 (use as configurações manuais).</span><span class="sxs-lookup"><span data-stu-id="f86c4-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="f86c4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f86c4-116">Remarks</span></span>

<span data-ttu-id="f86c4-117">Esta é uma lista de computadores, domínios e/ou endereços que irão ignorar o servidor proxy quando a parte do host da URL de destino corresponder a uma entrada na lista.</span><span class="sxs-lookup"><span data-stu-id="f86c4-117">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="f86c4-118">O \* caractere pode ser usado como um caractere curinga para listar entradas.</span><span class="sxs-lookup"><span data-stu-id="f86c4-118">The \* character can be used as a wildcard character for listing entries.</span></span> <span data-ttu-id="f86c4-119">Por exemplo, \* . com corresponderia a todos os hosts no domínio com, enquanto 67. \* corresponderia a todos os hosts da classe 67 uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="f86c4-119">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="f86c4-120">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="f86c4-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="f86c4-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f86c4-121">Examples</span></span>

<span data-ttu-id="f86c4-122">O exemplo de código a seguir usa **getProxyExceptionList** para exibir se o Windows Media Player está definido para ignorar o servidor proxy para endereços locais.</span><span class="sxs-lookup"><span data-stu-id="f86c4-122">The following code example uses **getProxyExceptionList** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="f86c4-123">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="f86c4-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyExceptionListHTTP = "";
string proxyExceptionListMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyExceptionListHTTP = player.network.getProxyExceptionList("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyExceptionListMMS = player.network.getProxyExceptionList("MMS");
}

// Store the proxy exception lists in a string array and display them
// using a multi-line text box. Unavailable exception lists will display
// as "undefined".
proxyExList[0] = ("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
proxyExList[1] = ("The current MMS proxy exception list: " + proxyExceptionListMMS);
proxyExceptionListText.Lines = proxyExList;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyExceptionListHTTP As String = &quot;&quot;
Dim proxyExceptionListMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyExceptionListHTTP = player.network.getProxyExceptionList(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyExceptionListMMS = player.network.getProxyExceptionList(&quot;MMS&quot;)

End If

&#39; Store the proxy exception lists in a string array and display them
&#39; using a multi-line text box. Unavailable exception lists will display
&#39; as &quot;undefined&quot;.
proxyExList(0) = (&quot;The current HTTP proxy exception list: &quot; + proxyExceptionListHTTP)
proxyExList(1) = (&quot;The current MMS proxy exception list: &quot; + proxyExceptionListMMS)
proxyExceptionList.Lines = proxyExList
```





## <a name="requirements"></a><span data-ttu-id="f86c4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f86c4-124">Requirements</span></span>



| <span data-ttu-id="f86c4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f86c4-125">Requirement</span></span> | <span data-ttu-id="f86c4-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f86c4-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f86c4-127">Versão</span><span class="sxs-lookup"><span data-stu-id="f86c4-127">Version</span></span><br/>   | <span data-ttu-id="f86c4-128">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="f86c4-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f86c4-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="f86c4-129">Namespace</span></span><br/> | <span data-ttu-id="f86c4-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f86c4-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f86c4-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="f86c4-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f86c4-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f86c4-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f86c4-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f86c4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f86c4-134">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f86c4-134">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f86c4-135">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f86c4-135">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f86c4-136">**IWMPNetwork. setProxyExceptionList (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f86c4-136">**IWMPNetwork.setProxyExceptionList (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)
</dt> </dl>

 

 





