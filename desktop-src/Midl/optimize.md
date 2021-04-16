---
title: otimizar atributo
description: O atributo \ Optimize \ ACF é usado para ajustar o nível de gradação para o marshaling de dados.
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- otimizar o atributo MIDL
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6025c40465ecf2e8fe7a33dcda50ece07d34b9d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105750020"
---
# <a name="optimize-attribute"></a><span data-ttu-id="42464-104">otimizar atributo</span><span class="sxs-lookup"><span data-stu-id="42464-104">optimize attribute</span></span>

<span data-ttu-id="42464-105">O atributo **\[ Optimize \]** ACF é usado para ajustar o nível de gradação de dados de marshaling.</span><span class="sxs-lookup"><span data-stu-id="42464-105">The **\[optimize\]** ACF attribute is used to fine tune the level of gradation for marshaling data.</span></span>

> [!Note]  
> <span data-ttu-id="42464-106">Essa palavra-chave é superceeded e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="42464-106">This keyword is superceeded and should not be used.</span></span> <span data-ttu-id="42464-107">Compilações de MIDL atuais devem usar [**/Oicf**](-oi.md)[**/robust**](-robust.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="42464-107">Current MIDL compilations should use [**/Oicf**](-oi.md)[**/robust**](-robust.md) instead.</span></span>

 

``` syntax
optimize ("optimization-options")
```

## <a name="parameters"></a><span data-ttu-id="42464-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42464-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42464-109">*otimização – opções*</span><span class="sxs-lookup"><span data-stu-id="42464-109">*optimization-options*</span></span> 
</dt> <dd>

<span data-ttu-id="42464-110">Especifica o método de marshaling de dados.</span><span class="sxs-lookup"><span data-stu-id="42464-110">Specifies the method of marshaling data.</span></span> <span data-ttu-id="42464-111">Use "s" para o marshaling de modo misto ou "i" para o marshaling interpretado.</span><span class="sxs-lookup"><span data-stu-id="42464-111">Use either "s" for mixed-mode marshaling or "i" for interpreted marshaling.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42464-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="42464-112">Remarks</span></span>

<span data-ttu-id="42464-113">Esta versão do RPC fornece dois métodos para empacotamento de dados: modo misto ("s") e interpretado ("i").</span><span class="sxs-lookup"><span data-stu-id="42464-113">This version of RPC provides two methods for marshaling data: mixed-mode ("s") and interpreted ("i").</span></span> <span data-ttu-id="42464-114">Esses métodos correspondem às opções de linha de comando [**/os**](-os.md) e [**/Oi**](-oi.md) .</span><span class="sxs-lookup"><span data-stu-id="42464-114">These methods correspond to the [**/Os**](-os.md) and [**/Oi**](-oi.md) command-line switches.</span></span> <span data-ttu-id="42464-115">O método interpretado realiza marshaling de dados completamente offline.</span><span class="sxs-lookup"><span data-stu-id="42464-115">The interpreted method marshals data completely offline.</span></span> <span data-ttu-id="42464-116">Embora isso possa reduzir consideravelmente o tamanho do stub, o desempenho pode ser afetado.</span><span class="sxs-lookup"><span data-stu-id="42464-116">While this can reduce the size of the stub considerably, performance can be affected.</span></span>

<span data-ttu-id="42464-117">Se o desempenho for uma preocupação, o método de modo misto poderá ser a melhor abordagem.</span><span class="sxs-lookup"><span data-stu-id="42464-117">If performance is a concern, the mixed-mode method can be the best approach.</span></span> <span data-ttu-id="42464-118">O modo misto permite que o compilador MIDL faça a determinação entre quais dados serão empacotados embutidos e que serão empacotados por uma chamada para uma biblioteca de vínculo dinâmico offline.</span><span class="sxs-lookup"><span data-stu-id="42464-118">Mixed-mode allows the MIDL compiler to make the determination between which data will be marshaled inline and which will be marshaled by a call to an offline dynamic-link library.</span></span> <span data-ttu-id="42464-119">Se muitos procedimentos usarem os mesmos tipos de dados, um único procedimento poderá ser chamado repetidamente para empacotar os dados.</span><span class="sxs-lookup"><span data-stu-id="42464-119">If many procedures use the same data types, a single procedure can be called repeatedly to marshal the data.</span></span> <span data-ttu-id="42464-120">Dessa forma, os dados mais adequados para o marshaling embutido são processados em linha, enquanto outros dados podem ser empacotados com mais eficiência offline.</span><span class="sxs-lookup"><span data-stu-id="42464-120">In this way, data that is most suited to inline marshaling is processed inline while other data can be more efficiently marshaled offline.</span></span>

<span data-ttu-id="42464-121">Observe que o atributo **\[ Optimize \]** pode ser usado como um atributo de interface ou como um atributo de operação.</span><span class="sxs-lookup"><span data-stu-id="42464-121">Note that the **\[optimize\]** attribute can be used as an interface attribute or as an operation attribute.</span></span> <span data-ttu-id="42464-122">Se ele for usado como um atributo de interface, ele definirá o padrão para a interface inteira, substituindo opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="42464-122">If it is used as an interface attribute, it sets the default for the entire interface, overriding command-line switches.</span></span> <span data-ttu-id="42464-123">No entanto, se ele for usado como um atributo de operação, ele afetará apenas essa operação, substituindo as opções de linha de comando e o padrão da interface.</span><span class="sxs-lookup"><span data-stu-id="42464-123">If, however, it is used as an operation attribute, it affects only that operation, overriding command-line switches and the interface default.</span></span>

## <a name="examples"></a><span data-ttu-id="42464-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="42464-124">Examples</span></span>

``` syntax
optimize ("s") HRESULT FasterProcedure(...); 
optimize ("i") HRESULT SmallerProcedure(...);
```

## <a name="see-also"></a><span data-ttu-id="42464-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="42464-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42464-126">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="42464-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="42464-127">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="42464-127">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="42464-128">**/Os**</span><span class="sxs-lookup"><span data-stu-id="42464-128">**/Os**</span></span>](-os.md)
</dt> <dt>

[<span data-ttu-id="42464-129">**/robust**</span><span class="sxs-lookup"><span data-stu-id="42464-129">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




