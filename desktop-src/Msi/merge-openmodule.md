---
description: O método OpenModule do objeto de mesclagem abre um módulo de mesclagem Windows Installer no modo somente leitura. Um módulo deve ser aberto antes que possa ser mesclado com um banco de dados de instalação.
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: Método Merge. OpenModule (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenModule
- IMsmMerge.OpenModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9d83a9331c91817f70c49ecf74c7171c5e627be6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757792"
---
# <a name="mergeopenmodule-method"></a><span data-ttu-id="8a944-104">Método Merge. OpenModule</span><span class="sxs-lookup"><span data-stu-id="8a944-104">Merge.OpenModule method</span></span>

<span data-ttu-id="8a944-105">O método **OpenModule** do objeto de [**mesclagem**](merge-object.md) abre um módulo de mesclagem Windows Installer no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8a944-105">The **OpenModule** method of the [**Merge**](merge-object.md) object opens a Windows Installer merge module in read-only mode.</span></span> <span data-ttu-id="8a944-106">Um módulo deve ser aberto antes que possa ser mesclado com um banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="8a944-106">A module must be opened before it can be merged with an installation database.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a944-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a944-107">Syntax</span></span>


```JScript
Merge.OpenModule(
  FileName,
  Language
)
```



## <a name="parameters"></a><span data-ttu-id="8a944-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a944-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a944-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="8a944-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="8a944-110">Nome de arquivo totalmente qualificado apontando para um módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="8a944-110">Fully qualified file name pointing to a merge module.</span></span>

</dd> <dt>

<span data-ttu-id="8a944-111">*Idioma*</span><span class="sxs-lookup"><span data-stu-id="8a944-111">*Language*</span></span> 
</dt> <dd>

<span data-ttu-id="8a944-112">Um identificador de idioma válido (LANGid).</span><span class="sxs-lookup"><span data-stu-id="8a944-112">A valid language identifier (LANGID).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a944-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a944-113">Return value</span></span>

<span data-ttu-id="8a944-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8a944-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a944-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a944-115">Remarks</span></span>

<span data-ttu-id="8a944-116">Essa função abre o módulo de mesclagem no modo somente leitura e exclui outros programas de gravar no módulo de mesclagem até que o método [**CloseModule**](merge-closemodule.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="8a944-116">This function opens the merge module in read-only mode and excludes other programs from writing to the merge module until the [**CloseModule**](merge-closemodule.md) method is called.</span></span>

<span data-ttu-id="8a944-117">O instalador tenta abrir o módulo no idioma especificado por *idioma* ou em uma linguagem mais geral.</span><span class="sxs-lookup"><span data-stu-id="8a944-117">The installer attempts to open the module in the language specified by *Language*, or a more general language.</span></span> <span data-ttu-id="8a944-118">Por exemplo, se o *idioma* for especificado como 1033, um módulo com um idioma padrão de 1033, 9 ou 0 pode ser aberto em seu idioma padrão.</span><span class="sxs-lookup"><span data-stu-id="8a944-118">For example, if *Language* is specified as 1033, a module with a default language of 1033, 9, or 0 can be opened in its default language.</span></span> <span data-ttu-id="8a944-119">Um valor de *idioma* 9 abre módulos com um idioma padrão de 9 ou 0.</span><span class="sxs-lookup"><span data-stu-id="8a944-119">A *Language* value of 9 opens modules with a default language of 9 or 0.</span></span> <span data-ttu-id="8a944-120">Se o idioma padrão do módulo não atender aos requisitos especificados, será feita uma tentativa de transformar o módulo no idioma solicitado.</span><span class="sxs-lookup"><span data-stu-id="8a944-120">If the default language of the module does not meet the specified requirements, an attempt is made to transform the module to the requested language.</span></span> <span data-ttu-id="8a944-121">Se isso falhar, o módulo será transformado em linguagens cada vez mais gerais, até a linguagem neutra.</span><span class="sxs-lookup"><span data-stu-id="8a944-121">If that fails, the module is transformed to increasingly general languages, all the way to language neutral.</span></span> <span data-ttu-id="8a944-122">Se nenhuma das transformações for bem-sucedida, o módulo não será aberto.</span><span class="sxs-lookup"><span data-stu-id="8a944-122">If none of the transforms succeed, the module fails to open.</span></span> <span data-ttu-id="8a944-123">Nesse caso, um erro é adicionado à lista de erros do tipo msmErrorLanguageUnsupported.</span><span class="sxs-lookup"><span data-stu-id="8a944-123">In this case, an error is added to the error list of type msmErrorLanguageUnsupported.</span></span> <span data-ttu-id="8a944-124">Se houver um erro ao transformar o módulo no idioma desejado, um erro será adicionado à lista de erros do tipo msmErrorLanguageFailed.</span><span class="sxs-lookup"><span data-stu-id="8a944-124">If there is an error transforming the module to the desired language, an error is added to the error list of type msmErrorLanguageFailed.</span></span> <span data-ttu-id="8a944-125">Para obter detalhes, consulte a propriedade [**Type**](error-type.md) do objeto [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="8a944-125">For details, see the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span> <span data-ttu-id="8a944-126">A abertura de um módulo de mesclagem limpa todos os erros que ainda não foram recuperados.</span><span class="sxs-lookup"><span data-stu-id="8a944-126">Opening a merge module clears any errors that have not already been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="8a944-127">C++</span><span class="sxs-lookup"><span data-stu-id="8a944-127">C++</span></span>

<span data-ttu-id="8a944-128">Consulte a função [**AbrirMódulo**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) .</span><span class="sxs-lookup"><span data-stu-id="8a944-128">See [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a944-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a944-129">Requirements</span></span>



| <span data-ttu-id="8a944-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a944-130">Requirement</span></span> | <span data-ttu-id="8a944-131">Valor</span><span class="sxs-lookup"><span data-stu-id="8a944-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a944-132">Versão</span><span class="sxs-lookup"><span data-stu-id="8a944-132">Version</span></span><br/> | <span data-ttu-id="8a944-133">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8a944-133">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="8a944-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a944-134">Header</span></span><br/>  | <dl> <span data-ttu-id="8a944-135"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a944-135"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a944-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8a944-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="8a944-137"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a944-137"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
