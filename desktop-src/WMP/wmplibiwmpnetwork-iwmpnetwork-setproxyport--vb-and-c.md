---
title: Método IWMPNetwork setProxyPort
description: O método setProxyPort especifica a porta proxy a ser usada. | Método IWMPNetwork setProxyPort
ms.assetid: df4b33f6-52b5-437f-ade2-0d08ca2878a9
keywords:
- método setProxyPort Windows Media Player
- método setProxyPort Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, método setProxyPort
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyPort
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d171fa1afc129dd1d13c1d9d12d71c4370cba9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812161"
---
# <a name="iwmpnetworksetproxyport-method"></a><span data-ttu-id="65d71-107">Método IWMPNetwork:: setProxyPort</span><span class="sxs-lookup"><span data-stu-id="65d71-107">IWMPNetwork::setProxyPort method</span></span>

<span data-ttu-id="65d71-108">O método **setProxyPort** especifica a porta proxy a ser usada.</span><span class="sxs-lookup"><span data-stu-id="65d71-108">The **setProxyPort** method specifies the proxy port to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="65d71-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65d71-109">Syntax</span></span>


```CSharp
public void setProxyPort(
  System.String bstrProtocol,
  System.Int32 lProxyPort
);
```


```VB

Public Sub setProxyPort( _
  ByVal bstrProtocol As System.String, _
  ByVal lProxyPort As System.Int32 _
)
Implements IWMPNetwork.setProxyPort
```





## <a name="parameters"></a><span data-ttu-id="65d71-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65d71-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65d71-111">*bstrProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65d71-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65d71-112">Um **System. String** que é o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="65d71-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="65d71-113">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="65d71-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="65d71-114">*lProxyPort* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65d71-114">*lProxyPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65d71-115">Um **System. Int32** que é a porta proxy a ser usada.</span><span class="sxs-lookup"><span data-stu-id="65d71-115">A **System.Int32** that is the proxy port to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65d71-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65d71-116">Return value</span></span>

<span data-ttu-id="65d71-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="65d71-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65d71-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="65d71-118">Remarks</span></span>

<span data-ttu-id="65d71-119">Esse método não tem efeito, a menos que o valor recuperado de **IWMPNetwork. getProxySettings** seja 2 (use as configurações manuais).</span><span class="sxs-lookup"><span data-stu-id="65d71-119">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="65d71-120">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="65d71-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="65d71-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="65d71-121">Examples</span></span>

<span data-ttu-id="65d71-122">O exemplo de código a seguir usa **setProxyPort** para especificar o número da porta proxy do Windows Media Player para o protocolo MMS.</span><span class="sxs-lookup"><span data-stu-id="65d71-122">The following code example uses **setProxyPort** to specify the Windows Media Player proxy port number for the MMS protocol.</span></span> <span data-ttu-id="65d71-123">O número da porta é recuperado de uma caixa de texto quando um botão é clicado.</span><span class="sxs-lookup"><span data-stu-id="65d71-123">The port number is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="65d71-124">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="65d71-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setProxyPort_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy port number.
        int portnumber = System.Convert.ToInt32(portText.Text);

        // Set the proxy port.
        player.network.setProxyPort("MMS", portnumber);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyPort_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyPort.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy port number.
        Dim portnumber As Integer = System.Convert.ToInt32(portText.Text)

        &#39; Set the proxy port.
        player.network.setProxyPort(&quot;MMS&quot;, portnumber)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="65d71-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65d71-125">Requirements</span></span>



| <span data-ttu-id="65d71-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="65d71-126">Requirement</span></span> | <span data-ttu-id="65d71-127">Valor</span><span class="sxs-lookup"><span data-stu-id="65d71-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65d71-128">Versão</span><span class="sxs-lookup"><span data-stu-id="65d71-128">Version</span></span><br/>   | <span data-ttu-id="65d71-129">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="65d71-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="65d71-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="65d71-130">Namespace</span></span><br/> | <span data-ttu-id="65d71-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="65d71-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="65d71-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="65d71-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="65d71-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="65d71-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65d71-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="65d71-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d71-135">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="65d71-135">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="65d71-136">**IWMPNetwork. getProxyPort (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="65d71-136">**IWMPNetwork.getProxyPort (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="65d71-137">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="65d71-137">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





