---
title: Método IWMPNetwork getProxyPort
description: O método getProxyPort retorna a porta do proxy que está sendo usada.
ms.assetid: fc94f3a9-458d-410c-98e9-a34be6e08c52
keywords:
- método getProxyPort Windows Media Player
- método getProxyPort Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, método getProxyPort
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyPort
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46fb388c2740e709e75579c01d216af677a826c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751049"
---
# <a name="iwmpnetworkgetproxyport-method"></a><span data-ttu-id="a2c9a-106">Método IWMPNetwork:: getProxyPort</span><span class="sxs-lookup"><span data-stu-id="a2c9a-106">IWMPNetwork::getProxyPort method</span></span>

<span data-ttu-id="a2c9a-107">O método **getProxyPort** retorna a porta do proxy que está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="a2c9a-107">The **getProxyPort** method returns the proxy port being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2c9a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2c9a-108">Syntax</span></span>


```CSharp
public System.Int32 getProxyPort(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyPort( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxyPort
```





## <a name="parameters"></a><span data-ttu-id="a2c9a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2c9a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2c9a-110">*bstrProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2c9a-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2c9a-111">Um **System. String** que é o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="a2c9a-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="a2c9a-112">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="a2c9a-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2c9a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2c9a-113">Return value</span></span>

<span data-ttu-id="a2c9a-114">Um **System. Int32** que é a porta de proxy que está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="a2c9a-114">A **System.Int32** that is the proxy port being used.</span></span> <span data-ttu-id="a2c9a-115">O valor é significativo somente quando **IWMPNetwork. getProxySettings** retorna um valor de 2 (use as configurações manuais).</span><span class="sxs-lookup"><span data-stu-id="a2c9a-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="a2c9a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2c9a-116">Remarks</span></span>

<span data-ttu-id="a2c9a-117">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="a2c9a-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="a2c9a-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a2c9a-118">Examples</span></span>

<span data-ttu-id="a2c9a-119">O exemplo de código a seguir usa **getProxyPort** para exibir os números de porta do proxy do Windows Media Player atuais para os protocolos MMS e http.</span><span class="sxs-lookup"><span data-stu-id="a2c9a-119">The following code example uses **getProxyPort** to display the current Windows Media Player proxy port numbers for the MMS and HTTP protocols.</span></span> <span data-ttu-id="a2c9a-120">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="a2c9a-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Variables to hold the results of calls to getProxyPort. 
int proxyPortHTTP = 0;
int proxyPortMMS = 0;

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyPortHTTP = player.network.getProxyPort("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyPortMMS = player.network.getProxyPort("MMS");
}

// Store the proxy port numbers in a string array and display them using a multi-line
// text box. Unavailable proxy port numbers will display as "undefined".
proxyPorts[0] = ("The current HTTP proxy port is: " + proxyPortHTTP.ToString());
proxyPorts[1] = ("The current MMS proxy port is: " + proxyPortMMS.ToString());
proxyPortText.Lines = proxyPorts;
```


```VB

' Variables to hold the results of calls to getProxyPort. 
Dim proxyPortHTTP As Integer = 0
Dim proxyPortMMS As Integer = 0

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyPortHTTP = player.network.getProxyPort(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyPortMMS = player.network.getProxyPort(&quot;MMS&quot;)

End If

&#39; Store the proxy port numbers in a string array and display them using a multi-line
&#39; text box. Unavailable proxy port numbers will display as &quot;undefined&quot;.
proxyPorts(0) = (&quot;The current HTTP proxy port is: &quot; + proxyPortHTTP.ToString())
proxyPorts(1) = (&quot;The current MMS proxy port is: &quot; + proxyPortMMS.ToString())
proxyPortText.Lines = proxyPorts
```





## <a name="requirements"></a><span data-ttu-id="a2c9a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2c9a-121">Requirements</span></span>



| <span data-ttu-id="a2c9a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2c9a-122">Requirement</span></span> | <span data-ttu-id="a2c9a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a2c9a-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2c9a-124">Versão</span><span class="sxs-lookup"><span data-stu-id="a2c9a-124">Version</span></span><br/>   | <span data-ttu-id="a2c9a-125">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="a2c9a-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a2c9a-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2c9a-126">Namespace</span></span><br/> | <span data-ttu-id="a2c9a-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a2c9a-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a2c9a-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="a2c9a-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a2c9a-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a2c9a-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2c9a-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2c9a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2c9a-131">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a2c9a-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a2c9a-132">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a2c9a-132">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a2c9a-133">**IWMPNetwork. setProxyPort (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a2c9a-133">**IWMPNetwork.setProxyPort (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)
</dt> </dl>

 

 





