---
title: Método IWMPNetwork getProxySettings
description: O método getProxySettings retorna informações sobre as configurações de proxy para um protocolo.
ms.assetid: eda4829a-4869-4557-8fe9-8061a1e0f586
keywords:
- método getProxySettings Windows Media Player
- método getProxySettings Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, método getProxySettings
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d970160c07c90e84585c87ed1abf740fbe3c6318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756342"
---
# <a name="iwmpnetworkgetproxysettings-method"></a><span data-ttu-id="5fd31-106">Método IWMPNetwork:: getProxySettings</span><span class="sxs-lookup"><span data-stu-id="5fd31-106">IWMPNetwork::getProxySettings method</span></span>

<span data-ttu-id="5fd31-107">O método **getProxySettings** retorna informações sobre as configurações de proxy para um protocolo.</span><span class="sxs-lookup"><span data-stu-id="5fd31-107">The **getProxySettings** method returns information about the proxy settings for a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fd31-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fd31-108">Syntax</span></span>


```CSharp
public System.Int32 getProxySettings(
  System.String bstrProtocol
);
```


```VB

Public Function getProxySettings( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxySettings
```





## <a name="parameters"></a><span data-ttu-id="5fd31-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fd31-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fd31-110">*bstrProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fd31-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fd31-111">Um **System. String** que é o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="5fd31-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="5fd31-112">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="5fd31-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fd31-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5fd31-113">Return value</span></span>

<span data-ttu-id="5fd31-114">Um **System. Int32** que é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5fd31-114">A **System.Int32** that is one of the following values.</span></span>



| <span data-ttu-id="5fd31-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5fd31-115">Value</span></span> | <span data-ttu-id="5fd31-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="5fd31-116">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5fd31-117">0</span><span class="sxs-lookup"><span data-stu-id="5fd31-117">0</span></span>     | <span data-ttu-id="5fd31-118">Um servidor proxy não está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="5fd31-118">A proxy server is not being used.</span></span>                                                |
| <span data-ttu-id="5fd31-119">1</span><span class="sxs-lookup"><span data-stu-id="5fd31-119">1</span></span>     | <span data-ttu-id="5fd31-120">As configurações de proxy para o navegador atual estão sendo usadas (válidas somente para HTTP).</span><span class="sxs-lookup"><span data-stu-id="5fd31-120">The proxy settings for the current browser are being used (valid only for HTTP).</span></span> |
| <span data-ttu-id="5fd31-121">2</span><span class="sxs-lookup"><span data-stu-id="5fd31-121">2</span></span>     | <span data-ttu-id="5fd31-122">As configurações de proxy especificadas manualmente estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="5fd31-122">The manually specified proxy settings are being used.</span></span>                            |
| <span data-ttu-id="5fd31-123">3</span><span class="sxs-lookup"><span data-stu-id="5fd31-123">3</span></span>     | <span data-ttu-id="5fd31-124">As configurações de proxy estão sendo detectadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5fd31-124">The proxy settings are being auto-detected.</span></span>                                      |



 

## <a name="remarks"></a><span data-ttu-id="5fd31-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="5fd31-125">Remarks</span></span>

<span data-ttu-id="5fd31-126">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="5fd31-126">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="5fd31-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5fd31-127">Examples</span></span>

<span data-ttu-id="5fd31-128">O exemplo de código a seguir usa **getProxySettings** para exibir uma mensagem, que fornece informações sobre as configurações de proxy atuais do Player, em um rótulo.</span><span class="sxs-lookup"><span data-stu-id="5fd31-128">The following code example uses **getProxySettings** to display a message, which gives information about the current proxy settings of the Player, in a label.</span></span> <span data-ttu-id="5fd31-129">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="5fd31-129">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Retrieve a number representing the current proxy settings.
int proxySetting = player.network.getProxySettings("MMS");

// Display the message that corresponds to the current settings.
switch(proxySetting)
{
    case 0:
    proxySettingsLabel.Text = "A proxy server is not being used";
    break;

    case 1: 
    proxySettingsLabel.Text = "The proxy settings for the current browser are being used.";
    break;

    case 2:
    proxySettingsLabel.Text = "The manually specified proxy settings are being used.";
    break;

    case 3:
    proxySettingsLabel.Text = "The proxy settings are being auto-detected.";
    break;

    default:
    proxySettingsLabel.Text = "Unable to determine proxy setting, try again.";
    break;
}
```


```VB

' Retrieve a number representing the current proxy settings.
Dim proxySetting As Integer = player.network.getProxySettings(&quot;MMS&quot;)

&#39; Display the message that corresponds to the current settings.
Select Case proxySetting

    Case 0
        proxySettingsLabel.Text = &quot;A proxy server is not being used&quot;

    Case 1
        proxySettingsLabel.Text = &quot;The proxy settings for the current browser are being used.&quot;

    Case 2
        proxySettingsLabel.Text = &quot;The manually specified proxy settings are being used.&quot;

    Case 3
        proxySettingsLabel.Text = &quot;The proxy settings are being auto-detected.&quot;

    Case Else
        proxySettingsLabel.Text = &quot;Unable to determine proxy setting, try again.&quot;

End Select
```





## <a name="requirements"></a><span data-ttu-id="5fd31-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fd31-130">Requirements</span></span>



| <span data-ttu-id="5fd31-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fd31-131">Requirement</span></span> | <span data-ttu-id="5fd31-132">Valor</span><span class="sxs-lookup"><span data-stu-id="5fd31-132">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd31-133">Versão</span><span class="sxs-lookup"><span data-stu-id="5fd31-133">Version</span></span><br/>   | <span data-ttu-id="5fd31-134">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="5fd31-134">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5fd31-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="5fd31-135">Namespace</span></span><br/> | <span data-ttu-id="5fd31-136">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5fd31-136">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5fd31-137">Assembly</span><span class="sxs-lookup"><span data-stu-id="5fd31-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5fd31-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5fd31-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fd31-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fd31-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fd31-140">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5fd31-140">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5fd31-141">**IWMPNetwork. setProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5fd31-141">**IWMPNetwork.setProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)
</dt> </dl>

 

 





