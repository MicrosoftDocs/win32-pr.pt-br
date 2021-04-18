---
description: O método MergeEx do objeto de mesclagem é equivalente à função Merge, exceto pelo fato de que ele usa um argumento extra.
ms.assetid: 83b6d62b-d176-42ac-b513-d1c2e562965c
title: Método Merge. MergeEx (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.MergeEx
- IMsmMerge.MergeEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 12accfcbc87877300b803ae90d8c924802410e9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757387"
---
# <a name="mergemergeex-method"></a><span data-ttu-id="3cb18-103">Método Merge. MergeEx</span><span class="sxs-lookup"><span data-stu-id="3cb18-103">Merge.MergeEx method</span></span>

<span data-ttu-id="3cb18-104">O método **MergeEx** do objeto de [**mesclagem**](merge-object.md) é equivalente à função [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) , exceto pelo fato de que ele usa um argumento extra.</span><span class="sxs-lookup"><span data-stu-id="3cb18-104">The **MergeEx** method of the [**Merge**](merge-object.md) object is equivalent to the [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) function, except that it takes an extra argument.</span></span> <span data-ttu-id="3cb18-105">O argumento *pConfiguration* é uma interface implementada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="3cb18-105">The *pConfiguration* argument is an interface implemented by the client.</span></span> <span data-ttu-id="3cb18-106">O argumento pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="3cb18-106">The argument may be null.</span></span> <span data-ttu-id="3cb18-107">A presença desse argumento indica que o cliente é capaz de dar suporte à funcionalidade de configuração, mas não obriga o cliente a fornecer dados de configuração para qualquer item configurável específico.</span><span class="sxs-lookup"><span data-stu-id="3cb18-107">The presence of this argument indicates that the client is capable of supporting the configuration functionality, but does not obligate the client to provide configuration data for any specific configurable item.</span></span>

<span data-ttu-id="3cb18-108">O método [**Merge**](merge-merge.md) executa uma mesclagem do banco de dados atual e do módulo atual.</span><span class="sxs-lookup"><span data-stu-id="3cb18-108">The [**Merge**](merge-merge.md) method executes a merge of the current database and current module.</span></span> <span data-ttu-id="3cb18-109">A mesclagem anexa os componentes no módulo ao recurso identificado pelo *recurso*.</span><span class="sxs-lookup"><span data-stu-id="3cb18-109">The merge attaches the components in the module to the feature identified by *Feature*.</span></span> <span data-ttu-id="3cb18-110">A raiz da árvore de diretórios do módulo é redirecionada para o local fornecido pelo *RedirectDir*.</span><span class="sxs-lookup"><span data-stu-id="3cb18-110">The root of the module's directory tree is redirected to the location given by *RedirectDir*.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cb18-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3cb18-111">Syntax</span></span>


```JScript
Merge.MergeEx(
  Feature,
  RedirectDir,
  pConfiguration
)
```



## <a name="parameters"></a><span data-ttu-id="3cb18-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3cb18-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cb18-113">*Recurso*</span><span class="sxs-lookup"><span data-stu-id="3cb18-113">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="3cb18-114">O nome de um recurso no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3cb18-114">The name of a feature in the database.</span></span>

</dd> <dt>

<span data-ttu-id="3cb18-115">*RedirectDir*</span><span class="sxs-lookup"><span data-stu-id="3cb18-115">*RedirectDir*</span></span> 
</dt> <dd>

<span data-ttu-id="3cb18-116">A chave de uma entrada na [tabela de diretório](directory-table.md) do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3cb18-116">The key of an entry in the [Directory table](directory-table.md) of the database.</span></span> <span data-ttu-id="3cb18-117">Esse parâmetro pode ser nulo ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="3cb18-117">This parameter may be null or an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="3cb18-118">*pConfiguration*</span><span class="sxs-lookup"><span data-stu-id="3cb18-118">*pConfiguration*</span></span> 
</dt> <dd>

<span data-ttu-id="3cb18-119">O argumento *pConfiguration* é uma interface implementada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="3cb18-119">The *pConfiguration* argument is an interface implemented by the client.</span></span> <span data-ttu-id="3cb18-120">O argumento pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="3cb18-120">The argument may be null.</span></span> <span data-ttu-id="3cb18-121">A presença desse argumento indica que o cliente é capaz de dar suporte à funcionalidade de configuração, mas não obriga o cliente a fornecer dados de configuração para qualquer item configurável específico.</span><span class="sxs-lookup"><span data-stu-id="3cb18-121">The presence of this argument indicates that the client is capable of supporting the configuration functionality, but does not obligate the client to provide configuration data for any specific configurable item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cb18-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3cb18-122">Return value</span></span>

<span data-ttu-id="3cb18-123">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3cb18-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cb18-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="3cb18-124">Remarks</span></span>

<span data-ttu-id="3cb18-125">Quando a mesclagem for concluída, os componentes no módulo serão anexados ao recurso identificado pelo *recurso*.</span><span class="sxs-lookup"><span data-stu-id="3cb18-125">Once the merge is complete, components in the module are attached to the feature identified by *Feature*.</span></span> <span data-ttu-id="3cb18-126">Esse recurso não é criado e deve ser um recurso existente.</span><span class="sxs-lookup"><span data-stu-id="3cb18-126">This feature is not created and must be an existing feature.</span></span> <span data-ttu-id="3cb18-127">O módulo pode ser anexado a recursos adicionais usando o método [**Connect**](merge-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="3cb18-127">The module may be attached to additional features using the [**Connect**](merge-connect.md) method.</span></span>

<span data-ttu-id="3cb18-128">As alterações feitas no banco de dados são salvas se e somente se o método [**CloseDatabase**](merge-closedatabase.md) for chamado com *BCommit* definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="3cb18-128">Changes made to the database are saved if and only if the [**CloseDatabase**](merge-closedatabase.md) method is called with *bCommit* set to **TRUE**.</span></span>

<span data-ttu-id="3cb18-129">Se ocorrerem conflitos de mesclagem, incluindo exclusões, eles serão colocados no enumerador de erros para recuperação posterior, mas não causará falha na mesclagem.</span><span class="sxs-lookup"><span data-stu-id="3cb18-129">If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail.</span></span> <span data-ttu-id="3cb18-130">Os erros podem ser recuperados por meio da propriedade [**Errors**](merge-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="3cb18-130">Errors may be retrieved through the [**Errors**](merge-errors.md) property.</span></span> <span data-ttu-id="3cb18-131">Erros e mensagens informativas são postados no arquivo de log atual.</span><span class="sxs-lookup"><span data-stu-id="3cb18-131">Errors and informational messages are posted to the current log file.</span></span>

<span data-ttu-id="3cb18-132">Quando a mesclagem falha devido a uma configuração de módulo incorreta, a função [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) retorna E \_ falha.</span><span class="sxs-lookup"><span data-stu-id="3cb18-132">When the merge fails because of an incorrect module configuration the [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) function returns E\_FAIL.</span></span> <span data-ttu-id="3cb18-133">Isso inclui esses erros msmErrorType: **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem** e **msmErrorDataRequestFailed**.</span><span class="sxs-lookup"><span data-stu-id="3cb18-133">This includes these msmErrorType errors: **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem**, and **msmErrorDataRequestFailed**.</span></span> <span data-ttu-id="3cb18-134">Esses erros fazem com que a mesclagem pare imediatamente quando o erro é encontrado.</span><span class="sxs-lookup"><span data-stu-id="3cb18-134">These errors cause the merge to stop immediately when the error is encountered.</span></span> <span data-ttu-id="3cb18-135">O objeto de erro ainda é adicionado ao enumerador quando **MergeEx** retorna E \_ falha.</span><span class="sxs-lookup"><span data-stu-id="3cb18-135">The error object is still added to the enumerator when **MergeEx** returns E\_FAIL.</span></span> <span data-ttu-id="3cb18-136">Para obter mais informações sobre erros de msmErrorType, consulte a [**\_ função obter tipo (objeto de erro)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).</span><span class="sxs-lookup"><span data-stu-id="3cb18-136">For more information about msmErrorType errors, see [**get\_Type Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).</span></span> <span data-ttu-id="3cb18-137">Todos os outros erros fazem com que **MergeEx** retorne S \_ false e faça com que a mesclagem continue.</span><span class="sxs-lookup"><span data-stu-id="3cb18-137">All other errors cause **MergeEx** to return S\_FALSE and cause the merge to continue.</span></span>

### <a name="c"></a><span data-ttu-id="3cb18-138">C++</span><span class="sxs-lookup"><span data-stu-id="3cb18-138">C++</span></span>

<span data-ttu-id="3cb18-139">Consulte a função [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) .</span><span class="sxs-lookup"><span data-stu-id="3cb18-139">See [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb18-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cb18-140">Requirements</span></span>



| <span data-ttu-id="3cb18-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cb18-141">Requirement</span></span> | <span data-ttu-id="3cb18-142">Valor</span><span class="sxs-lookup"><span data-stu-id="3cb18-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb18-143">Versão</span><span class="sxs-lookup"><span data-stu-id="3cb18-143">Version</span></span><br/> | <span data-ttu-id="3cb18-144">Mergemod.dll 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="3cb18-144">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="3cb18-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3cb18-145">Header</span></span><br/>  | <dl> <span data-ttu-id="3cb18-146"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cb18-146"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="3cb18-147">DLL</span><span class="sxs-lookup"><span data-stu-id="3cb18-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="3cb18-148"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cb18-148"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
