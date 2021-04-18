---
title: Método WebHelp do IWMPError
description: O método WebHelp inicia a página de ajuda da Web do Windows Media Player para exibir mais informações sobre o primeiro erro na fila de erros (índice zero). | Método WebHelp do IWMPError
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- método WebHelp do Windows Media Player
- método WebHelp do Windows Media Player, interface IWMPError
- Interface IWMPError Windows Media Player, método Webhelp
topic_type:
- apiref
api_name:
- IWMPError.webHelp
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9b0cd48d45ac5e5e5d77d0150b8acdf13347e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764524"
---
# <a name="iwmperrorwebhelp-method"></a><span data-ttu-id="fd154-107">Método IWMPError:: Webhelp</span><span class="sxs-lookup"><span data-stu-id="fd154-107">IWMPError::webHelp method</span></span>

<span data-ttu-id="fd154-108">O método **WebHelp** inicia a página de ajuda da Web do Windows Media Player para exibir mais informações sobre o primeiro erro na fila de erros (índice zero).</span><span class="sxs-lookup"><span data-stu-id="fd154-108">The **webHelp** method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd154-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd154-109">Syntax</span></span>


```CSharp
public void webHelp();
```


```VB

Public Sub webHelp()
Implements IWMPError.webHelp
```





## <a name="parameters"></a><span data-ttu-id="fd154-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd154-110">Parameters</span></span>

<span data-ttu-id="fd154-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fd154-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fd154-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fd154-112">Return value</span></span>

<span data-ttu-id="fd154-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fd154-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd154-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd154-114">Remarks</span></span>

<span data-ttu-id="fd154-115">As páginas de ajuda da Web sempre contêm as informações mais recentes e mais detalhadas sobre erros do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fd154-115">The Web Help pages always contain the latest and most detailed information about Windows Media Player errors.</span></span> <span data-ttu-id="fd154-116">Esse método transfere automaticamente as outras informações necessárias pela ajuda da Web, como a versão do sistema operacional que está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="fd154-116">This method automatically transfers the other information needed by Web Help, such as the operating system version being used.</span></span>

<span data-ttu-id="fd154-117">Para acessar as páginas de ajuda da Web diretamente, use os seguintes links de código de erro e centro de suporte:</span><span class="sxs-lookup"><span data-stu-id="fd154-117">To access the Web Help pages directly, use the following error code and support center links:</span></span>

-   [<span data-ttu-id="fd154-118">Informações de código de erro do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="fd154-118">Windows Media Player Error Code Information</span></span>](https://support.microsoft.com/kb/886273)
-   [<span data-ttu-id="fd154-119">Centro de soluções do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="fd154-119">Windows Media Player Solution Center</span></span>](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a><span data-ttu-id="fd154-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fd154-120">Examples</span></span>

<span data-ttu-id="fd154-121">O exemplo a seguir cria um botão que inicia a página de ajuda da Web do Microsoft Windows Media Player no navegador.</span><span class="sxs-lookup"><span data-stu-id="fd154-121">The following example creates a button that launches the Microsoft Windows Media Player Web Help page in the browser.</span></span> <span data-ttu-id="fd154-122">O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="fd154-122">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void webHelpButton_Click(object sender, System.EventArgs e)
{
    // Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp();
}
```


```VB

Public Sub webHelpButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles webHelpButton.Click

    &#39; Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="fd154-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd154-123">Requirements</span></span>



| <span data-ttu-id="fd154-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd154-124">Requirement</span></span> | <span data-ttu-id="fd154-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fd154-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd154-126">Versão</span><span class="sxs-lookup"><span data-stu-id="fd154-126">Version</span></span><br/>   | <span data-ttu-id="fd154-127">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="fd154-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fd154-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd154-128">Namespace</span></span><br/> | <span data-ttu-id="fd154-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fd154-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fd154-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="fd154-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fd154-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fd154-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd154-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd154-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd154-133">**Interface IWMPError (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fd154-133">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





