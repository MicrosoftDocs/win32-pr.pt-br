---
title: Método IWMPNetwork setProxyBypassForLocal
description: O método setProxyBypassForLocal especifica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.
ms.assetid: b308957a-0d7e-45be-8625-db198b276dad
keywords:
- método setProxyBypassForLocal Windows Media Player
- método setProxyBypassForLocal Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, método setProxyBypassForLocal
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f869125d43529a039804fe28c0f0dc493f481e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763078"
---
# <a name="iwmpnetworksetproxybypassforlocal-method"></a><span data-ttu-id="c62f6-106">Método IWMPNetwork:: setProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="c62f6-106">IWMPNetwork::setProxyBypassForLocal method</span></span>

<span data-ttu-id="c62f6-107">O método **setProxyBypassForLocal** especifica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.</span><span class="sxs-lookup"><span data-stu-id="c62f6-107">The **setProxyBypassForLocal** method specifies whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="c62f6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c62f6-108">Syntax</span></span>


```CSharp
public void setProxyBypassForLocal(
  System.String bstrProtocol,
  System.Boolean fBypassForLocal
);
```


```VB

Public Sub setProxyBypassForLocal( _
  ByVal bstrProtocol As System.String, _
  ByVal fBypassForLocal As System.Boolean _
)
Implements IWMPNetwork.setProxyBypassForLocal
```





## <a name="parameters"></a><span data-ttu-id="c62f6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c62f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c62f6-110">*bstrProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c62f6-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c62f6-111">Um **System. String** que é o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="c62f6-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="c62f6-112">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="c62f6-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="c62f6-113">*fBypassForLocal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c62f6-113">*fBypassForLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c62f6-114">Um valor **System. Boolean** que indica se o servidor proxy é ignorado.</span><span class="sxs-lookup"><span data-stu-id="c62f6-114">A **System.Boolean** value that indicates whether the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c62f6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c62f6-115">Return value</span></span>

<span data-ttu-id="c62f6-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c62f6-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c62f6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c62f6-117">Remarks</span></span>

<span data-ttu-id="c62f6-118">Esse método não tem efeito, a menos que o valor recuperado de **IWMPNetwork. getProxySettings** seja 2 (use as configurações manuais).</span><span class="sxs-lookup"><span data-stu-id="c62f6-118">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="c62f6-119">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="c62f6-119">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="c62f6-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c62f6-120">Examples</span></span>

<span data-ttu-id="c62f6-121">O exemplo de código a seguir usa **setProxyBypassForLocal** para especificar se o servidor proxy do Windows Media Player foi ignorado, ao usar o protocolo MMS, se o servidor de origem estiver em uma rede local.</span><span class="sxs-lookup"><span data-stu-id="c62f6-121">The following code example uses **setProxyBypassForLocal** to specify whether the Windows Media Player proxy server is bypassed, when using the MMS protocol, if the origin server is on a local network.</span></span> <span data-ttu-id="c62f6-122">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="c62f6-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Prepare a message, a caption and buttons for the user prompt.
string message = ("Bypass proxy server for local addresses?");
string caption = "Proxy Settings";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.YesNo;

// Test whether the proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    // Prompt the user for a setting. 
    System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

    // Store the return value of the DialogResult in a boolean variable.
    bool proxybypass;
    
    if(result == System.Windows.Forms.DialogResult.Yes)
    {
        proxybypass = true;
    }
    else
    {
        proxybypass = false;
    }

    // Set the proxy bypass value according to the response.
    player.network.setProxyBypassForLocal("MMS", proxybypass);
}
else
{
    // Warn that proxy settings must be set to 2 (manual).
    System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
}
```


```VB

' Prepare a message, a caption and buttons for the user prompt.
Dim message As String = &quot;Bypass proxy server for local addresses?&quot;
Dim caption As String = &quot;Proxy Settings&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.YesNo

&#39; Test whether the proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    &#39; Prompt the user for a setting. 
    Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

    &#39; Store the return value of the DialogResult as a boolean.
    Dim proxybypass As Boolean

    If (result = System.Windows.Forms.DialogResult.Yes) Then

        proxybypass = True

    Else

        proxybypass = False

    End If

    &#39; Set the proxy bypass value according to the response.
    player.network.setProxyBypassForLocal(&quot;MMS&quot;, proxybypass)

Else

    &#39; Warn that proxy settings must be set to 2 (manual).
    System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

End If
```





## <a name="requirements"></a><span data-ttu-id="c62f6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c62f6-123">Requirements</span></span>



| <span data-ttu-id="c62f6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c62f6-124">Requirement</span></span> | <span data-ttu-id="c62f6-125">Valor</span><span class="sxs-lookup"><span data-stu-id="c62f6-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c62f6-126">Versão</span><span class="sxs-lookup"><span data-stu-id="c62f6-126">Version</span></span><br/>   | <span data-ttu-id="c62f6-127">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="c62f6-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c62f6-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="c62f6-128">Namespace</span></span><br/> | <span data-ttu-id="c62f6-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c62f6-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c62f6-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="c62f6-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c62f6-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c62f6-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c62f6-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c62f6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c62f6-133">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c62f6-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c62f6-134">**IWMPNetwork. getProxyBypassForLocal (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c62f6-134">**IWMPNetwork.getProxyBypassForLocal (VB and C#)**</span></span>](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c62f6-135">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c62f6-135">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





