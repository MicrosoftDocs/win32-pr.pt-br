---
title: Método getproxyname de IWMPNetwork
description: O método getproxyname retorna o nome do servidor proxy que está sendo usado.
ms.assetid: 69396b01-1da7-450c-b229-0cc4fb832ae9
keywords:
- método getproxyname do Windows Media Player
- método getproxyname Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork do Windows Media Player, método getproxyname
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5e05b6552e5e6a922cf02037a0bfc4956bfc28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754476"
---
# <a name="iwmpnetworkgetproxyname-method"></a><span data-ttu-id="df43f-106">Método IWMPNetwork:: getproxyname</span><span class="sxs-lookup"><span data-stu-id="df43f-106">IWMPNetwork::getProxyName method</span></span>

<span data-ttu-id="df43f-107">O método **Getproxyname** retorna o nome do servidor proxy que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="df43f-107">The **getProxyName** method returns the name of the proxy server being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="df43f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df43f-108">Syntax</span></span>


```CSharp
public System.String getProxyName(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyName( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyName
```





## <a name="parameters"></a><span data-ttu-id="df43f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df43f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df43f-110">*bstrProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df43f-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df43f-111">Um **System. String** que é o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="df43f-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="df43f-112">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="df43f-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df43f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df43f-113">Return value</span></span>

<span data-ttu-id="df43f-114">Um **System. String** que é o nome do servidor proxy que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="df43f-114">A **System.String** that is the name of the proxy server being used.</span></span> <span data-ttu-id="df43f-115">O valor é significativo somente quando **IWMPNetwork. getProxySettings** retorna um valor de 2 (use as configurações manuais).</span><span class="sxs-lookup"><span data-stu-id="df43f-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="df43f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="df43f-116">Remarks</span></span>

<span data-ttu-id="df43f-117">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="df43f-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="df43f-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="df43f-118">Examples</span></span>

<span data-ttu-id="df43f-119">O exemplo de código a seguir usa **Getproxyname** para exibir os nomes do servidor proxy do Windows Media Player para os protocolos http e MMS.</span><span class="sxs-lookup"><span data-stu-id="df43f-119">The following code example uses **getProxyName** to display the Windows Media Player proxy server names for the HTTP and MMS protocols.</span></span> <span data-ttu-id="df43f-120">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="df43f-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyNameHTTP = "";
string proxyNameMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyNameHTTP = player.network.getProxyName("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyNameMMS = player.network.getProxyName("MMS");
}

// Store the proxy server names in a string array and display them using a multi-line
// text box. Unavailable proxy server names will display as "undefined".
proxyNames[0] = ("The current HTTP proxy server name is: " + proxyNameHTTP);
proxyNames[1] = ("The current MMS proxy server name is: " + proxyNameMMS);
proxyNameText.Lines = proxyNames;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyNameHTTP As String = &quot;&quot;
Dim proxyNameMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyNameHTTP = player.network.getProxyName(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyNameMMS = player.network.getProxyName(&quot;MMS&quot;)

End If

&#39; Store the proxy server names in a string array and display them using a multi-line
&#39; text box. Unavailable proxy server names will display as &quot;undefined&quot;.
proxyNames(0) = (&quot;The current HTTP proxy server name is: &quot; + proxyNameHTTP)
proxyNames(1) = (&quot;The current MMS proxy server name is: &quot; + proxyNameMMS)
proxyNameText.Lines = proxyNames
```





## <a name="requirements"></a><span data-ttu-id="df43f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df43f-121">Requirements</span></span>



| <span data-ttu-id="df43f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="df43f-122">Requirement</span></span> | <span data-ttu-id="df43f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="df43f-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df43f-124">Versão</span><span class="sxs-lookup"><span data-stu-id="df43f-124">Version</span></span><br/>   | <span data-ttu-id="df43f-125">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="df43f-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="df43f-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="df43f-126">Namespace</span></span><br/> | <span data-ttu-id="df43f-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="df43f-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="df43f-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="df43f-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="df43f-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="df43f-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df43f-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="df43f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df43f-131">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="df43f-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="df43f-132">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="df43f-132">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="df43f-133">**IWMPNetwork. setproxyname (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="df43f-133">**IWMPNetwork.setProxyName (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)
</dt> </dl>

 

 





