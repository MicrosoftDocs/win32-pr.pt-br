---
title: Erro. método Webhelp
description: O método WebHelp inicia a página de ajuda da Web do Windows Media Player para exibir mais informações sobre o primeiro erro na fila de erros (índice zero). | Erro. método Webhelp
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- método WebHelp do Windows Media Player
- método WebHelp do Windows Media Player, classe de erro
- Classe de erro Windows Media Player, método Webhelp
topic_type:
- apiref
api_name:
- Error.webHelp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862376be956bc8b37a778f5c9d1d2238c876208d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763351"
---
# <a name="errorwebhelp-method"></a><span data-ttu-id="31414-107">Erro. método Webhelp</span><span class="sxs-lookup"><span data-stu-id="31414-107">Error.webHelp method</span></span>

<span data-ttu-id="31414-108">O método **WebHelp** inicia a página de ajuda da Web do Windows Media Player para exibir mais informações sobre o primeiro erro na fila de erros (índice zero).</span><span class="sxs-lookup"><span data-stu-id="31414-108">The **webHelp** method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="31414-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31414-109">Syntax</span></span>


```JScript
Error.webHelp()
```



## <a name="parameters"></a><span data-ttu-id="31414-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31414-110">Parameters</span></span>

<span data-ttu-id="31414-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="31414-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="31414-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31414-112">Return value</span></span>

<span data-ttu-id="31414-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="31414-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="31414-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="31414-114">Remarks</span></span>

<span data-ttu-id="31414-115">As páginas de ajuda da Web sempre contêm as informações mais recentes e mais detalhadas sobre erros do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="31414-115">The Web Help pages always contain the latest and most detailed information about Windows Media Player errors.</span></span> <span data-ttu-id="31414-116">Esse método transfere automaticamente as outras informações necessárias pela ajuda da Web, como a versão do sistema operacional que está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="31414-116">This method automatically transfers the other information needed by Web Help, such as the operating system version being used.</span></span>

<span data-ttu-id="31414-117">Para acessar as páginas de ajuda da Web diretamente, use o seguinte código de erro e links do centro de suporte.</span><span class="sxs-lookup"><span data-stu-id="31414-117">To access the Web Help pages directly, use the following error code and support center links.</span></span>

-   [<span data-ttu-id="31414-118">Informações de código de erro do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="31414-118">Windows Media Player Error Code Information</span></span>](https://support.microsoft.com/kb/886273)
-   [<span data-ttu-id="31414-119">Centro de soluções do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="31414-119">Windows Media Player Solution Center</span></span>](https://support.microsoft.com/ph/7763#tab0)

<span data-ttu-id="31414-120">**Windows Media Player 10 Mobile:** Esse método sempre tem sucesso, mas não executa a operação pretendida.</span><span class="sxs-lookup"><span data-stu-id="31414-120">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="examples"></a><span data-ttu-id="31414-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="31414-121">Examples</span></span>

<span data-ttu-id="31414-122">O exemplo a seguir cria um elemento de botão HTML que inicia a página de ajuda da Web do Microsoft Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="31414-122">The following example creates an HTML BUTTON element that launches the Microsoft Windows Media Player Web Help page.</span></span> <span data-ttu-id="31414-123">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="31414-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  
       NAME = "WHBUTTON"  
       VALUE = "More Info"

OnClick = "Player.error.webHelp();

">

```



## <a name="requirements"></a><span data-ttu-id="31414-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31414-124">Requirements</span></span>



| <span data-ttu-id="31414-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="31414-125">Requirement</span></span> | <span data-ttu-id="31414-126">Valor</span><span class="sxs-lookup"><span data-stu-id="31414-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="31414-127">Versão</span><span class="sxs-lookup"><span data-stu-id="31414-127">Version</span></span><br/> | <span data-ttu-id="31414-128">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="31414-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="31414-129">DLL</span><span class="sxs-lookup"><span data-stu-id="31414-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="31414-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31414-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31414-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="31414-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31414-132">**Objeto Error**</span><span class="sxs-lookup"><span data-stu-id="31414-132">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





