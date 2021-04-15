---
title: Método setproxyname do IWMPNetwork
description: O método setproxyname especifica o nome do servidor proxy a ser usado. | Método setproxyname do IWMPNetwork
ms.assetid: a3b0f53a-d81a-4e6d-9cac-7047433246ae
keywords:
- método setproxyname do Windows Media Player
- método setproxyname Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork do Windows Media Player, método setproxyname
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9759f37dd4c0e171c09afaea4dfde0993c7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747282"
---
# <a name="iwmpnetworksetproxyname-method"></a><span data-ttu-id="4f2ca-107">Método IWMPNetwork:: setproxyname</span><span class="sxs-lookup"><span data-stu-id="4f2ca-107">IWMPNetwork::setProxyName method</span></span>

<span data-ttu-id="4f2ca-108">O método **Setproxyname** especifica o nome do servidor proxy a ser usado.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-108">The **setProxyName** method specifies the name of the proxy server to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f2ca-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f2ca-109">Syntax</span></span>


```CSharp
public void setProxyName(
  System.String bstrProtocol,
  System.String bstrProxyName
);
```


```VB

Public Sub setProxyName( _
  ByVal bstrProtocol As System.String, _
  ByVal bstrProxyName As System.String _
)
Implements IWMPNetwork.setProxyName
```





## <a name="parameters"></a><span data-ttu-id="4f2ca-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f2ca-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f2ca-111">*bstrProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f2ca-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f2ca-112">Um **System. String** que é o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="4f2ca-113">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="4f2ca-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f2ca-114">*bstrProxyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f2ca-114">*bstrProxyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f2ca-115">Um **System. String** que é o nome do servidor proxy a ser usado.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-115">A **System.String** that is the name of the proxy server to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f2ca-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f2ca-116">Return value</span></span>

<span data-ttu-id="4f2ca-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f2ca-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f2ca-118">Remarks</span></span>

<span data-ttu-id="4f2ca-119">Esse método não tem efeito, a menos que o valor recuperado de **IWMPNetwork. getProxySettings** seja 2 (use as configurações manuais).</span><span class="sxs-lookup"><span data-stu-id="4f2ca-119">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="4f2ca-120">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="4f2ca-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4f2ca-121">Examples</span></span>

<span data-ttu-id="4f2ca-122">O exemplo de código a seguir usa **Setproxyname** para especificar o nome do servidor proxy do Windows Media Player para o protocolo MMS.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-122">The following code example uses **setProxyName** to specify the name of the Windows Media Player proxy server for the MMS protocol.</span></span> <span data-ttu-id="4f2ca-123">O novo nome é recuperado de uma caixa de texto quando um botão é clicado.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-123">The new name is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="4f2ca-124">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="4f2ca-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setProxyName_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy name.
        string proxyname = nameText.Text;

        // Set the proxy name.
        player.network.setProxyName("MMS", proxyname);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyName.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy name.
        Dim proxyname As String = nameText.Text

        &#39; Set the proxy name.
        player.network.setProxyName(&quot;MMS&quot;, proxyname)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4f2ca-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f2ca-125">Requirements</span></span>



| <span data-ttu-id="4f2ca-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f2ca-126">Requirement</span></span> | <span data-ttu-id="4f2ca-127">Valor</span><span class="sxs-lookup"><span data-stu-id="4f2ca-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f2ca-128">Versão</span><span class="sxs-lookup"><span data-stu-id="4f2ca-128">Version</span></span><br/>   | <span data-ttu-id="4f2ca-129">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="4f2ca-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4f2ca-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f2ca-130">Namespace</span></span><br/> | <span data-ttu-id="4f2ca-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4f2ca-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="4f2ca-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4f2ca-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4f2ca-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f2ca-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f2ca-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f2ca-135">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-135">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4f2ca-136">**IWMPNetwork. getproxyname (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-136">**IWMPNetwork.getProxyName (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4f2ca-137">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4f2ca-137">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





