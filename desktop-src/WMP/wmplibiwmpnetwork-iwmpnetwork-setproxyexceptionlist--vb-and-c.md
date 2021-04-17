---
title: Método IWMPNetwork setProxyExceptionList
description: O método setProxyExceptionList especifica a lista de exceções de proxy. | Método IWMPNetwork setProxyExceptionList
ms.assetid: a7a5e9ad-f71f-431e-9a53-b56456778104
keywords:
- método setProxyExceptionList Windows Media Player
- método setProxyExceptionList Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, método setProxyExceptionList
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dad011dee8e1199e6111be60acfec41d85d1e58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761926"
---
# <a name="iwmpnetworksetproxyexceptionlist-method"></a><span data-ttu-id="128d5-107">Método IWMPNetwork:: setProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="128d5-107">IWMPNetwork::setProxyExceptionList method</span></span>

<span data-ttu-id="128d5-108">O método **setProxyExceptionList** especifica a lista de exceções de proxy.</span><span class="sxs-lookup"><span data-stu-id="128d5-108">The **setProxyExceptionList** method specifies the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="128d5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="128d5-109">Syntax</span></span>


```CSharp
public void setProxyExceptionList(
  System.String bstrProtocol,
  System.String pbstrExceptionList
);
```


```VB

Public Sub setProxyExceptionList( _
  ByVal bstrProtocol As System.String, _
  ByVal pbstrExceptionList As System.String _
)
Implements IWMPNetwork.setProxyExceptionList
```





## <a name="parameters"></a><span data-ttu-id="128d5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="128d5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="128d5-111">*bstrProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="128d5-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="128d5-112">Um **System. String** que é o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="128d5-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="128d5-113">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="128d5-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="128d5-114">*pbstrExceptionList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="128d5-114">*pbstrExceptionList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="128d5-115">Um **System. String** que é uma lista delimitada por ponto-e-vírgula de hosts para os quais o servidor proxy é ignorado.</span><span class="sxs-lookup"><span data-stu-id="128d5-115">A **System.String** that is a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="128d5-116">Espaços à esquerda e à direita não devem estar presentes.</span><span class="sxs-lookup"><span data-stu-id="128d5-116">Leading and trailing spaces should not be present.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="128d5-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="128d5-117">Return value</span></span>

<span data-ttu-id="128d5-118">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="128d5-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="128d5-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="128d5-119">Remarks</span></span>

<span data-ttu-id="128d5-120">Esta é uma lista de computadores, domínios e/ou endereços que irão ignorar o servidor proxy quando a parte do host da URL de destino corresponder a uma entrada na lista.</span><span class="sxs-lookup"><span data-stu-id="128d5-120">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="128d5-121">O \* caractere pode ser usado como um caractere curinga para listar entradas.</span><span class="sxs-lookup"><span data-stu-id="128d5-121">The \* character can be used as a wildcard character for listing entries.</span></span> <span data-ttu-id="128d5-122">Por exemplo, \* . com corresponderia a todos os hosts no domínio com, enquanto 67. \* corresponderia a todos os hosts da classe 67 uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="128d5-122">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="128d5-123">Esse método não tem efeito, a menos que o valor recuperado de **IWMPNetwork. getProxySettings** seja 2 (use as configurações manuais).</span><span class="sxs-lookup"><span data-stu-id="128d5-123">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="128d5-124">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="128d5-124">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="128d5-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="128d5-125">Examples</span></span>

<span data-ttu-id="128d5-126">O exemplo de código a seguir usa **setProxyExceptionList** para especificar uma lista de hosts para os quais o servidor proxy é ignorado ao usar o protocolo MMS.</span><span class="sxs-lookup"><span data-stu-id="128d5-126">The following code example uses **setProxyExceptionList** to specify a list of hosts for which the proxy server is bypassed when using the MMS protocol.</span></span> <span data-ttu-id="128d5-127">A nova lista é recuperada de uma caixa de texto quando um botão é clicado.</span><span class="sxs-lookup"><span data-stu-id="128d5-127">The new list is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="128d5-128">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="128d5-128">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setExList_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new exception list.
        string proxyxlist = exListText.Text;

        // Set the exception list.
        player.network.setProxyExceptionList("MMS", proxyxlist);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setExList_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setExList.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new exception list.
        Dim proxyxlist As String = exListText.Text

        &#39; Set the exception list.
        player.network.setProxyExceptionList(&quot;MMS&quot;, proxyxlist)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="128d5-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="128d5-129">Requirements</span></span>



| <span data-ttu-id="128d5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="128d5-130">Requirement</span></span> | <span data-ttu-id="128d5-131">Valor</span><span class="sxs-lookup"><span data-stu-id="128d5-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="128d5-132">Versão</span><span class="sxs-lookup"><span data-stu-id="128d5-132">Version</span></span><br/>   | <span data-ttu-id="128d5-133">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="128d5-133">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="128d5-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="128d5-134">Namespace</span></span><br/> | <span data-ttu-id="128d5-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="128d5-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="128d5-136">Assembly</span><span class="sxs-lookup"><span data-stu-id="128d5-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="128d5-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="128d5-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="128d5-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="128d5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="128d5-139">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="128d5-139">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="128d5-140">**IWMPNetwork. getProxyExceptionList (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="128d5-140">**IWMPNetwork.getProxyExceptionList (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="128d5-141">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="128d5-141">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





