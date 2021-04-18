---
title: Comutador/os
description: A opção/os especifica o método de modo misto para empacotar o código de stub passado entre o cliente e o servidor.
ms.assetid: dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb
keywords:
- MIDL do comutador/os
topic_type:
- apiref
api_name:
- /Os
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbbef54501e195c91bdcc0cec8045f2eec763820
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105758454"
---
# <a name="os-switch"></a><span data-ttu-id="dd043-104">Comutador/os</span><span class="sxs-lookup"><span data-stu-id="dd043-104">/Os switch</span></span>

<span data-ttu-id="dd043-105">A opção **/os** especifica o método de modo misto para empacotar o código de stub passado entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="dd043-105">The **/Os** switch specifies the mixed-mode method to marshal stub code passed between client and server.</span></span>

``` syntax
midl /Os
```

## <a name="switch-options"></a><span data-ttu-id="dd043-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="dd043-106">Switch Options</span></span>

<span data-ttu-id="dd043-107">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dd043-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd043-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd043-108">Remarks</span></span>

<span data-ttu-id="dd043-109">Há problemas importantes a serem considerados antes de decidir sobre o método de empacotamento de código.</span><span class="sxs-lookup"><span data-stu-id="dd043-109">There are important issues to consider before deciding on the method for marshaling code.</span></span> <span data-ttu-id="dd043-110">Esses problemas se preocupam com o tamanho e o desempenho.</span><span class="sxs-lookup"><span data-stu-id="dd043-110">These issues concern size and performance.</span></span> <span data-ttu-id="dd043-111">O compilador MIDL fornece dois métodos para empacotamento de código: modo misto (**/os**) e totalmente interpretado ([**/Oi**](-oi.md)).</span><span class="sxs-lookup"><span data-stu-id="dd043-111">The MIDL compiler provides two methods for marshaling code: mixed-mode (**/Os**) and fully-interpreted ([**/Oi**](-oi.md)).</span></span> <span data-ttu-id="dd043-112">O método totalmente interpretado realiza marshaling de dados completamente offline.</span><span class="sxs-lookup"><span data-stu-id="dd043-112">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="dd043-113">Isso reduz consideravelmente o tamanho do código stub, mas também resulta em desempenho reduzido.</span><span class="sxs-lookup"><span data-stu-id="dd043-113">This reduces the size of the stub code considerably, but it also results in decreased performance.</span></span>

<span data-ttu-id="dd043-114">Use o modo padrão MIDL **/Oicf** /robust para todas as finalidades além da compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="dd043-114">Use MIDL default mode **/Oicf** /robust for all purposes other than backward compatibility.</span></span> <span data-ttu-id="dd043-115">Esse modo é o modo padrão seguro do compilador MIDL; qualquer outro modo deve ser usado somente após uma consideração cuidadosa da implicação de segurança, percebendo que extensões futuras serão implementadas somente para o modo padrão.</span><span class="sxs-lookup"><span data-stu-id="dd043-115">This mode is the secure standard mode of MIDL compiler; any other mode should be used only after careful consideration to the security implication, realizing that future extensions will only be implemented for default mode.</span></span> <span data-ttu-id="dd043-116">No modo misto, o compilador empacota alguns parâmetros embutidos nos stubs gerados.</span><span class="sxs-lookup"><span data-stu-id="dd043-116">In mixed mode, the compiler marshals some parameters inline in the generated stubs.</span></span> <span data-ttu-id="dd043-117">Embora isso resulte em um tamanho maior de stub, ele também pode oferecer maior desempenho.</span><span class="sxs-lookup"><span data-stu-id="dd043-117">While this results in larger stub size, it also may offer increased performance.</span></span>

<span data-ttu-id="dd043-118">O MIDL fornece suporte completo para matrizes multidimensionais e ponteiros de dimensionamento multidimensional somente no modo [**/Oicf**](-oi.md) .</span><span class="sxs-lookup"><span data-stu-id="dd043-118">MIDL provides full support for multidimensional arrays and multidimensional-sized pointers only in [**/Oicf**](-oi.md) mode.</span></span> <span data-ttu-id="dd043-119">Nos modos **/os** e **/Oi** , o compilador oferece suporte a casos simples, como matrizes de tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="dd043-119">In **/Os** and **/Oi** modes, the compiler supports simple cases, such as fixed-size arrays.</span></span> <span data-ttu-id="dd043-120">O uso de matrizes multidimensionais nos modos **/os** ou **/Oi** pode resultar em parâmetros que não são empacotados corretamente.</span><span class="sxs-lookup"><span data-stu-id="dd043-120">Using multidimensional arrays in **/Os** or **/Oi** modes can result in parameters that are not marshaled correctly.</span></span> <span data-ttu-id="dd043-121">A Microsoft recomenda que você use a opção de linha de comando **/Oicf** quando sua interface define parâmetros que são matrizes multidimensionais ou ponteiros com dimensionamento multidimensional.</span><span class="sxs-lookup"><span data-stu-id="dd043-121">Microsoft recommends that you use the **/Oicf** command line switch when your interface defines parameters that are multidimensional arrays or multidimensional-sized pointers.</span></span>

<span data-ttu-id="dd043-122">Para definir melhor o nível de gradação em como os dados são empacotados, esta versão do RPC fornece um \[ [](optimize.md) \] atributo optimize.</span><span class="sxs-lookup"><span data-stu-id="dd043-122">To further define the level of gradation in how data is marshaled, this version of RPC provides an \[[**optimize**](optimize.md)\] attribute.</span></span> <span data-ttu-id="dd043-123">Esse atributo é usado como um atributo de interface ACF ou atributo de operação para selecionar o modo de marshaling.</span><span class="sxs-lookup"><span data-stu-id="dd043-123">This attribute is used as an ACF interface attribute or operation attribute to select the marshaling mode.</span></span>

## <a name="examples"></a><span data-ttu-id="dd043-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dd043-124">Examples</span></span>

<span data-ttu-id="dd043-125">**MIDL/os filename. idl**</span><span class="sxs-lookup"><span data-stu-id="dd043-125">**midl /Os filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="dd043-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd043-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd043-127">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="dd043-127">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="dd043-128">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="dd043-128">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="dd043-129">**formato**</span><span class="sxs-lookup"><span data-stu-id="dd043-129">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="dd043-130">**\_opção de formato de/// \_**</span><span class="sxs-lookup"><span data-stu-id="dd043-130">**/no\_format\_opt**</span></span>](-no-format-opt.md)
</dt> </dl>

 

 




