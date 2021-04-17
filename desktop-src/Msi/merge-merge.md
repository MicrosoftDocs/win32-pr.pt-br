---
description: O método Merge do objeto Merge executa uma mesclagem do banco de dados atual e do módulo atual.
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: Método Merge. Merge (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Merge
- IMsmMerge.Merge
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: f33a0ba8218ae38d8fb31cefb6910f5b2c16484d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751436"
---
# <a name="mergemerge-method"></a><span data-ttu-id="a8ed6-103">Método Merge. Merge</span><span class="sxs-lookup"><span data-stu-id="a8ed6-103">Merge.Merge method</span></span>

<span data-ttu-id="a8ed6-104">O método **Merge** do objeto [**Merge**](merge-object.md) executa uma mesclagem do banco de dados atual e do módulo atual.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-104">The **Merge** method of the [**Merge**](merge-object.md) object executes a merge of the current database and current module.</span></span> <span data-ttu-id="a8ed6-105">A mesclagem anexa os componentes no módulo ao recurso identificado pelo *recurso*.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-105">The merge attaches the components in the module to the feature identified by *Feature*.</span></span> <span data-ttu-id="a8ed6-106">A raiz da árvore de diretórios do módulo é redirecionada para o local fornecido pelo *RedirectDir*.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-106">The root of the module's directory tree is redirected to the location given by *RedirectDir*.</span></span>

<span data-ttu-id="a8ed6-107">O método **Merge** só pode ser chamado uma vez para mesclar uma combinação específica de arquivos. msi e. msm.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-107">The **Merge** method can only be called once to merge a particular combination of .msi and .msm files.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8ed6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8ed6-108">Syntax</span></span>


```JScript
Merge.Merge(
  Feature,
  RedirectDir
)
```



## <a name="parameters"></a><span data-ttu-id="a8ed6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8ed6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8ed6-110">*Recurso*</span><span class="sxs-lookup"><span data-stu-id="a8ed6-110">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ed6-111">O nome de um recurso no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-111">The name of a feature in the database.</span></span>

</dd> <dt>

<span data-ttu-id="a8ed6-112">*RedirectDir*</span><span class="sxs-lookup"><span data-stu-id="a8ed6-112">*RedirectDir*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ed6-113">A chave de uma entrada na [tabela de diretório](directory-table.md) do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-113">The key of an entry in the [Directory table](directory-table.md) of the database.</span></span> <span data-ttu-id="a8ed6-114">Esse parâmetro pode ser nulo ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-114">This parameter may be null or an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8ed6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8ed6-115">Return value</span></span>

<span data-ttu-id="a8ed6-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8ed6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8ed6-117">Remarks</span></span>

<span data-ttu-id="a8ed6-118">Quando a mesclagem for concluída, os componentes no módulo serão anexados ao recurso identificado pelo *recurso*.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-118">Once the merge is complete, components in the module are attached to the feature identified by *Feature*.</span></span> <span data-ttu-id="a8ed6-119">Esse recurso não é criado e deve ser um recurso existente.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-119">This feature is not created and must be an existing feature.</span></span> <span data-ttu-id="a8ed6-120">Observe que o método **Merge** obtém todas as referências de recurso no módulo e substitui a referência de recurso para todas as ocorrências do GUID NULL no banco de dados do módulo.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-120">Note that the **Merge** method gets all the feature references in the module and substitutes the feature reference for all occurrences of the null GUID in the module database.</span></span> <span data-ttu-id="a8ed6-121">Para obter mais informações, consulte [fazendo referência a recursos em módulos de mesclagem](referencing-features-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="a8ed6-121">For more information, see [Referencing Features in Merge Modules](referencing-features-in-merge-modules.md).</span></span>

<span data-ttu-id="a8ed6-122">O módulo pode ser anexado a recursos adicionais usando o método [**Connect**](merge-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="a8ed6-122">The module may be attached to additional features using the [**Connect**](merge-connect.md) method.</span></span> <span data-ttu-id="a8ed6-123">Observe que chamar o método **Connect** somente cria associações de componente de recurso.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-123">Note that calling the **Connect** method only creates feature-component associations.</span></span> <span data-ttu-id="a8ed6-124">Ele não modifica as linhas que já foram mescladas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-124">It does not modify the rows that have already been merged in to the database.</span></span>

<span data-ttu-id="a8ed6-125">As alterações feitas no banco de dados são salvas se e somente se o método [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) for chamado com *BCommit* definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-125">Changes made to the database are saved if and only if the [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) method is called with *bCommit* set to **TRUE**.</span></span>

<span data-ttu-id="a8ed6-126">Se ocorrerem conflitos de mesclagem, incluindo exclusões, eles serão colocados no enumerador de erros para recuperação posterior, mas não causará falha na mesclagem.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-126">If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail.</span></span> <span data-ttu-id="a8ed6-127">Os erros podem ser recuperados por meio da propriedade [**Errors**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="a8ed6-127">Errors may be retrieved through the [**Errors**](error-object.md) property.</span></span> <span data-ttu-id="a8ed6-128">Erros e mensagens informativas são postados no arquivo de log atual.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-128">Errors and informational messages are posted to the current log file.</span></span>

### <a name="c"></a><span data-ttu-id="a8ed6-129">C++</span><span class="sxs-lookup"><span data-stu-id="a8ed6-129">C++</span></span>

<span data-ttu-id="a8ed6-130">Consulte [**mesclar**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) função.</span><span class="sxs-lookup"><span data-stu-id="a8ed6-130">See [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8ed6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8ed6-131">Requirements</span></span>



| <span data-ttu-id="a8ed6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8ed6-132">Requirement</span></span> | <span data-ttu-id="a8ed6-133">Valor</span><span class="sxs-lookup"><span data-stu-id="a8ed6-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ed6-134">Versão</span><span class="sxs-lookup"><span data-stu-id="a8ed6-134">Version</span></span><br/> | <span data-ttu-id="a8ed6-135">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a8ed6-135">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="a8ed6-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8ed6-136">Header</span></span><br/>  | <dl> <span data-ttu-id="a8ed6-137"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8ed6-137"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8ed6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a8ed6-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="a8ed6-139"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8ed6-139"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
