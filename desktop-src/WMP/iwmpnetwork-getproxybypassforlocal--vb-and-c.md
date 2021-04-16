---
title: Método IWMPNetwork getProxyBypassForLocal
description: O método getProxyBypassForLocal retorna um valor que indica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.
ms.assetid: 150a05f3-6979-4a88-a617-472f07d38807
keywords:
- método getProxyBypassForLocal Windows Media Player
- método getProxyBypassForLocal Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, método getProxyBypassForLocal
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b87b1f00432ec91dd4379a9fa5e31664437afe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779410"
---
# <a name="iwmpnetworkgetproxybypassforlocal-method"></a><span data-ttu-id="9af3d-106">Método IWMPNetwork:: getProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="9af3d-106">IWMPNetwork::getProxyBypassForLocal method</span></span>

<span data-ttu-id="9af3d-107">O método **getProxyBypassForLocal** retorna um valor que indica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.</span><span class="sxs-lookup"><span data-stu-id="9af3d-107">The **getProxyBypassForLocal** method returns a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="9af3d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9af3d-108">Syntax</span></span>


```CSharp
public System.Boolean getProxyBypassForLocal(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyBypassForLocal( _
  ByVal bstrProtocol As System.String _
) As System.Boolean
Implements IWMPNetwork.getProxyBypassForLocal
```





## <a name="parameters"></a><span data-ttu-id="9af3d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9af3d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9af3d-110">*bstrProtocol*</span><span class="sxs-lookup"><span data-stu-id="9af3d-110">*bstrProtocol*</span></span> 
</dt> <dd>

<span data-ttu-id="9af3d-111">Um **System. String** que é o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="9af3d-111">A **System.String** that is the protocol name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9af3d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9af3d-112">Return value</span></span>

<span data-ttu-id="9af3d-113">Um valor **System. Boolean** que indica se o servidor proxy é ignorado.</span><span class="sxs-lookup"><span data-stu-id="9af3d-113">A **System.Boolean** value that indicates whether the proxy server is bypassed.</span></span> <span data-ttu-id="9af3d-114">O valor é significativo somente quando **IWMPNetwork. getProxySettings** retorna um valor de 2 (use as configurações manuais).</span><span class="sxs-lookup"><span data-stu-id="9af3d-114">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="9af3d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9af3d-115">Remarks</span></span>

<span data-ttu-id="9af3d-116">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="9af3d-116">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="9af3d-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9af3d-117">Examples</span></span>

<span data-ttu-id="9af3d-118">O exemplo de código a seguir usa **getProxyBypassForLocal** para exibir se o Windows Media Player está definido para ignorar o servidor proxy para endereços locais.</span><span class="sxs-lookup"><span data-stu-id="9af3d-118">The following code example uses **getProxyBypassForLocal** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="9af3d-119">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="9af3d-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```VB
' Boolean values to hold the results of calls to getProxyBypassForLocal. 
Dim proxyBypassForLocalHTTP As Boolean = False
Dim proxyBypassForLocalMMS As Boolean = False

' Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings("HTTP") = 2) Then

    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal("HTTP")

End If

' Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings("MMS") = 2) Then

    proxyBypassForLocalMMS = player.network.getProxyBypassForLocal("MMS")

End If

' Store the proxy bypass for local values in a string array and display them
' using a multi-line text box. Unavailable proxy bypass for local values will display
' as "undefined".
proxyInfo(0) = ("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP.ToString())
proxyInfo(1) = ("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS.ToString())
proxyBypassText.Lines = proxyInfo
```


```CSharp

// Boolean values to hold the results of calls to getProxyBypassForLocal. 
bool proxyBypassForLocalHTTP = false;
bool proxyBypassForLocalMMS = false;

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings(&quot;HTTP&quot;) == 2)
{
    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal(&quot;HTTP&quot;);
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings(&quot;MMS&quot;) == 2)
{
   proxyBypassForLocalMMS = player.network.getProxyBypassForLocal(&quot;MMS&quot;);
}

// Store the proxy bypass for local values in a string array and display them
// using a multi-line text box. Unavailable proxy bypass for local values will display
// as &quot;undefined&quot;.
proxyInfo[0] = (&quot;The current HTTP proxy bypass for local value: &quot; + proxyBypassForLocalHTTP.ToString());
proxyInfo[1] = (&quot;The current MMS proxy bypass for local value: &quot; + proxyBypassForLocalMMS.ToString());
proxyBypassText.Lines = proxyInfo;
```





## <a name="requirements"></a><span data-ttu-id="9af3d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9af3d-120">Requirements</span></span>



| <span data-ttu-id="9af3d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9af3d-121">Requirement</span></span> | <span data-ttu-id="9af3d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9af3d-122">Value</span></span> |
|----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af3d-123">Versão</span><span class="sxs-lookup"><span data-stu-id="9af3d-123">Version</span></span><br/>   | <span data-ttu-id="9af3d-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="9af3d-124">Windows Media Player 9 Series or later</span></span><br/>                                             |
| <span data-ttu-id="9af3d-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="9af3d-125">Namespace</span></span><br/> | <span data-ttu-id="9af3d-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9af3d-126">**WMPLib**</span></span><br/>                                                                         |
| <span data-ttu-id="9af3d-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="9af3d-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9af3d-128"><dt>Interop.WMPLib.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9af3d-128"><dt>Interop.WMPLib.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9af3d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="9af3d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9af3d-130">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9af3d-130">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9af3d-131">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9af3d-131">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9af3d-132">**IWMPNetwork. setProxyBypassForLocal (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9af3d-132">**IWMPNetwork.setProxyBypassForLocal (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md)
</dt> </dl>

 

 





