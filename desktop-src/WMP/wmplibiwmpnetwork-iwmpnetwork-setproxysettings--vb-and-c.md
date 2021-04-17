---
title: Método IWMPNetwork setProxySettings
description: O método setProxySettings especifica as configurações de proxy para um protocolo.
ms.assetid: 6e410812-a06c-4911-8291-1d654fcd281a
keywords:
- método setProxySettings Windows Media Player
- método setProxySettings Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, método setProxySettings
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7fc36c12335cf97ad7bff34924850155f2fd747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748506"
---
# <a name="iwmpnetworksetproxysettings-method"></a><span data-ttu-id="da661-106">Método IWMPNetwork:: setProxySettings</span><span class="sxs-lookup"><span data-stu-id="da661-106">IWMPNetwork::setProxySettings method</span></span>

<span data-ttu-id="da661-107">O método **setProxySettings** especifica as configurações de proxy para um protocolo.</span><span class="sxs-lookup"><span data-stu-id="da661-107">The **setProxySettings** method specifies the proxy settings for a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="da661-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da661-108">Syntax</span></span>


```CSharp
public void setProxySettings(
  System.String bstrProtocol,
  System.Int32 lProxySetting
);
```


```VB

Public Sub setProxySettings( _
  ByVal bstrProtocol As System.String, _
  ByVal lProxySetting As System.Int32 _
)
Implements IWMPNetwork.setProxySettings
```





## <a name="parameters"></a><span data-ttu-id="da661-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da661-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da661-110">*bstrProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="da661-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da661-111">Um **System. String** que é o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="da661-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="da661-112">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="da661-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="da661-113">*lProxySetting* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="da661-113">*lProxySetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da661-114">Um **System. Int32** que é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="da661-114">A **System.Int32** that is one of the following values.</span></span>



| <span data-ttu-id="da661-115">Valor</span><span class="sxs-lookup"><span data-stu-id="da661-115">Value</span></span> | <span data-ttu-id="da661-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="da661-116">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="da661-117">0</span><span class="sxs-lookup"><span data-stu-id="da661-117">0</span></span>     | <span data-ttu-id="da661-118">Não use um servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="da661-118">Do not use a proxy server.</span></span>                                           |
| <span data-ttu-id="da661-119">1</span><span class="sxs-lookup"><span data-stu-id="da661-119">1</span></span>     | <span data-ttu-id="da661-120">Use as configurações de proxy do navegador atual (válido somente para HTTP).</span><span class="sxs-lookup"><span data-stu-id="da661-120">Use the proxy settings of the current browser (valid only for HTTP).</span></span> |
| <span data-ttu-id="da661-121">2</span><span class="sxs-lookup"><span data-stu-id="da661-121">2</span></span>     | <span data-ttu-id="da661-122">Use as configurações de proxy especificadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="da661-122">Use the manually specified proxy settings.</span></span>                           |
| <span data-ttu-id="da661-123">3</span><span class="sxs-lookup"><span data-stu-id="da661-123">3</span></span>     | <span data-ttu-id="da661-124">Detectar automaticamente as configurações de proxy.</span><span class="sxs-lookup"><span data-stu-id="da661-124">Auto-detect the proxy settings.</span></span>                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da661-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da661-125">Return value</span></span>

<span data-ttu-id="da661-126">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="da661-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da661-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="da661-127">Remarks</span></span>

<span data-ttu-id="da661-128">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="da661-128">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="da661-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="da661-129">Examples</span></span>

<span data-ttu-id="da661-130">O exemplo de código a seguir usa uma caixa de listagem para permitir que o usuário defina a configuração de proxy do Windows Media Player para o protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="da661-130">The following code example uses a list box to allow the user to set the Windows Media Player proxy setting for the HTTP protocol.</span></span> <span data-ttu-id="da661-131">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="da661-131">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Load the list box with the proxy settings in order so that their index in the
// list box matches their value.
proxySettings.Items.Add("Do not use a proxy server.  (Value = 0)");                                             
proxySettings.Items.Add("Use the proxy settings of the current browser. Valid for HTTP only.  (Value = 1)");
proxySettings.Items.Add("Use the manually specified proxy settings.  (Value = 2)");
proxySettings.Items.Add("Auto-detect the proxy settings.  (Value = 3)");                                       

// Change the proxy setting for the HTTP protocol when the user makes a list box selection.
private void proxySettings_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the setting from the ListBox
    int setting = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Change the proxy setting. 
    player.network.setProxySettings("HTTP", setting);
}
```


```VB

' Load the list box with the proxy settings in order so that their index in the
&#39; list box matches their value.
proxySettings.Items.Add(&quot;Do not use a proxy server.  (Value = 0)&quot;)
proxySettings.Items.Add(&quot;Use the proxy settings of the current browser. Valid for HTTP only.  (Value = 1)&quot;)
proxySettings.Items.Add(&quot;Use the manually specified proxy settings.  (Value = 2)&quot;)
proxySettings.Items.Add(&quot;Auto-detect the proxy settings.  (Value = 3)&quot;)

&#39; Change the proxy setting for the HTTP protocol when the user makes a list box selection.
Public Sub proxySettings_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles proxySettings.SelectedIndexChanged

    &#39; Store the index of the setting from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim setting As Integer = lb.SelectedIndex

    &#39; Change the proxy setting. 
    player.network.setProxySettings(&quot;HTTP&quot;, setting)
    
End Sub
```





## <a name="requirements"></a><span data-ttu-id="da661-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da661-132">Requirements</span></span>



| <span data-ttu-id="da661-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="da661-133">Requirement</span></span> | <span data-ttu-id="da661-134">Valor</span><span class="sxs-lookup"><span data-stu-id="da661-134">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da661-135">Versão</span><span class="sxs-lookup"><span data-stu-id="da661-135">Version</span></span><br/>   | <span data-ttu-id="da661-136">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="da661-136">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="da661-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="da661-137">Namespace</span></span><br/> | <span data-ttu-id="da661-138">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="da661-138">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="da661-139">Assembly</span><span class="sxs-lookup"><span data-stu-id="da661-139">Assembly</span></span><br/>  | <dl> <span data-ttu-id="da661-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="da661-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da661-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="da661-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da661-142">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="da661-142">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="da661-143">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="da661-143">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





