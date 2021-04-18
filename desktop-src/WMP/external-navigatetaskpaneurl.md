---
title: Método external. NavigateTaskPaneURL
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Método external. NavigateTaskPaneURL
ms.assetid: c3a888c0-6589-4d21-9d47-37372d9069f4
keywords:
- Método NavigateTaskPaneURL Windows Media Player
- Método NavigateTaskPaneURL Windows Media Player, classe externa
- Classe externa Windows Media Player, método NavigateTaskPaneURL
topic_type:
- apiref
api_name:
- External.NavigateTaskPaneURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e70558c7616738f67d9dc1d6d29eca15e5c30d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759703"
---
# <a name="externalnavigatetaskpaneurl-method"></a><span data-ttu-id="23b66-107">Método external. NavigateTaskPaneURL</span><span class="sxs-lookup"><span data-stu-id="23b66-107">External.NavigateTaskPaneURL method</span></span>

> [!Note]  
> <span data-ttu-id="23b66-108">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="23b66-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="23b66-109">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="23b66-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="23b66-110">O método **NavigateTaskPaneURL** abre uma página da Web no painel de tarefas especificado e altera o foco para o painel especificado.</span><span class="sxs-lookup"><span data-stu-id="23b66-110">The **NavigateTaskPaneURL** method opens a webpage in the specified task pane, and changes focus to the specified pane.</span></span>

## <a name="syntax"></a><span data-ttu-id="23b66-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23b66-111">Syntax</span></span>


```JScript
External.NavigateTaskPaneURL(
  bstrKeyName,
  bstrTaskPane,
  bstrParams
)
```



## <a name="parameters"></a><span data-ttu-id="23b66-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23b66-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23b66-113">*bstrKeyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23b66-113">*bstrKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23b66-114">**Cadeia de caracteres** que contém o nome da chave para a loja online.</span><span class="sxs-lookup"><span data-stu-id="23b66-114">**String** containing the key name for the online store.</span></span> <span data-ttu-id="23b66-115">(obrigatório)</span><span class="sxs-lookup"><span data-stu-id="23b66-115">(required)</span></span>

</dd> <dt>

<span data-ttu-id="23b66-116">*bstrTaskPane* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23b66-116">*bstrTaskPane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23b66-117">**Cadeia de caracteres** que contém o nome do painel de tarefas no qual a página da Web é aberta.</span><span class="sxs-lookup"><span data-stu-id="23b66-117">**String** containing the name of the task pane in which the webpage opens.</span></span> <span data-ttu-id="23b66-118">(obrigatório)</span><span class="sxs-lookup"><span data-stu-id="23b66-118">(required)</span></span>

</dd> <dt>

<span data-ttu-id="23b66-119">*bstrParams* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23b66-119">*bstrParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23b66-120">**Cadeia de caracteres** que contém os parâmetros da cadeia de caracteres de consulta a serem acrescentados à URL especificada pelo elemento **Navigate** do documento serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="23b66-120">**String** containing the query string parameters to append to the URL specified by the **Navigate** element of the ServiceInfo document.</span></span> <span data-ttu-id="23b66-121">(opcional)</span><span class="sxs-lookup"><span data-stu-id="23b66-121">(optional)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23b66-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23b66-122">Return value</span></span>

<span data-ttu-id="23b66-123">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="23b66-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="23b66-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="23b66-124">Remarks</span></span>

<span data-ttu-id="23b66-125">Navegar para um painel que sua loja online não suporta pode fazer com que o repositório online atual seja alterado.</span><span class="sxs-lookup"><span data-stu-id="23b66-125">Navigating to a pane that your online store does not support may cause the current online store to change.</span></span>

<span data-ttu-id="23b66-126">O valor especificado para *bstrParams* é válido somente quando **NavigateTaskPaneURL** é chamado a partir de páginas da Web fornecidas pela loja online.</span><span class="sxs-lookup"><span data-stu-id="23b66-126">The value specified for *bstrParams* is valid only when **NavigateTaskPaneURL** is called from webpages provided by the online store.</span></span>

<span data-ttu-id="23b66-127">A tabela a seguir lista os valores válidos para *bstrTaskPane* e o painel de tarefas associado para cada um.</span><span class="sxs-lookup"><span data-stu-id="23b66-127">The following table lists of valid values for *bstrTaskPane* and the associated task pane for each.</span></span>



| <span data-ttu-id="23b66-128">Valor</span><span class="sxs-lookup"><span data-stu-id="23b66-128">Value</span></span>            | <span data-ttu-id="23b66-129">Painel de Tarefas</span><span class="sxs-lookup"><span data-stu-id="23b66-129">Task Pane</span></span>                      |
|------------------|--------------------------------|
| <span data-ttu-id="23b66-130">**ServiceTask1**</span><span class="sxs-lookup"><span data-stu-id="23b66-130">**ServiceTask1**</span></span> | <span data-ttu-id="23b66-131">Primeiro painel de tarefas da loja online.</span><span class="sxs-lookup"><span data-stu-id="23b66-131">First online store task pane.</span></span>  |
| <span data-ttu-id="23b66-132">**ServiceTask2**</span><span class="sxs-lookup"><span data-stu-id="23b66-132">**ServiceTask2**</span></span> | <span data-ttu-id="23b66-133">Segundo painel de tarefas da loja online.</span><span class="sxs-lookup"><span data-stu-id="23b66-133">Second online store task pane.</span></span> |
| <span data-ttu-id="23b66-134">**ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="23b66-134">**ServiceTask3**</span></span> | <span data-ttu-id="23b66-135">Terceiro painel de tarefas da loja online.</span><span class="sxs-lookup"><span data-stu-id="23b66-135">Third online store task pane.</span></span>  |



 

<span data-ttu-id="23b66-136">O código da página da Web deve especificar um valor para [external. SelectedTaskPane](external-selectedtaskpane.md) ao carregar para garantir que o botão correto do painel de tarefas seja realçado após a conclusão da navegação.</span><span class="sxs-lookup"><span data-stu-id="23b66-136">Your webpage code should specify a value for [External.SelectedTaskPane](external-selectedtaskpane.md) when loading to ensure that the correct task pane button is highlighted after navigation is completed.</span></span>

## <a name="examples"></a><span data-ttu-id="23b66-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="23b66-137">Examples</span></span>

<span data-ttu-id="23b66-138">O código de exemplo a seguir mostra como o **NavigateTaskPaneURL** cria a URL da página da Web a ser exibida para **ServiceTask1**.</span><span class="sxs-lookup"><span data-stu-id="23b66-138">The following example code shows how **NavigateTaskPaneURL** creates the URL of the webpage to display for **ServiceTask1**.</span></span>

<span data-ttu-id="23b66-139">Exemplo do elemento **Navigate** :</span><span class="sxs-lookup"><span data-stu-id="23b66-139">Example of the **Navigate** element:</span></span>


```XML
<Navigate
    BaseURL = "https://www.proseware.com/online store/html/navigate.asp">
</Navigate>
```



<span data-ttu-id="23b66-140">Exemplo de chamada para o método **NavigateTaskPaneURL** :</span><span class="sxs-lookup"><span data-stu-id="23b66-140">Example call to the **NavigateTaskPaneURL** method:</span></span>


```XML
external.NavigateTaskPaneURL("Proseware", "ServiceTask1", "Pane=Store");
```



<span data-ttu-id="23b66-141">Exemplo de URL resultante usada para a página da Web exibida em **ServiceTask1**:</span><span class="sxs-lookup"><span data-stu-id="23b66-141">Example of resulting URL used for the webpage displayed in **ServiceTask1**:</span></span>


```XML
https://www.proseware.com/online store/html/navigate.asp?Pane=Store
```



## <a name="requirements"></a><span data-ttu-id="23b66-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23b66-142">Requirements</span></span>



| <span data-ttu-id="23b66-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="23b66-143">Requirement</span></span> | <span data-ttu-id="23b66-144">Valor</span><span class="sxs-lookup"><span data-stu-id="23b66-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23b66-145">Versão</span><span class="sxs-lookup"><span data-stu-id="23b66-145">Version</span></span><br/> | <span data-ttu-id="23b66-146">Windows Media Player 10 ou posterior</span><span class="sxs-lookup"><span data-stu-id="23b66-146">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="23b66-147">DLL</span><span class="sxs-lookup"><span data-stu-id="23b66-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="23b66-148"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23b66-148"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23b66-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="23b66-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23b66-150">**Objeto externo para lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="23b66-150">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="23b66-151">**External. SelectedTaskPane**</span><span class="sxs-lookup"><span data-stu-id="23b66-151">**External.SelectedTaskPane**</span></span>](external-selectedtaskpane.md)
</dt> </dl>

 

 





