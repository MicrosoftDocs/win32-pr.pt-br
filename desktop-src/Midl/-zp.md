---
title: Comutador/ZP
description: O comutador/ZP é o mesmo que a opção/Pack.
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- MIDL do comutador/ZP
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553d99dee7dd08218680fc0b43e6e12237c4f8fa
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638455"
---
# <a name="zp-switch"></a><span data-ttu-id="91eaf-104">Comutador/ZP</span><span class="sxs-lookup"><span data-stu-id="91eaf-104">/Zp switch</span></span>

<span data-ttu-id="91eaf-105">O comutador **/ZP** é o mesmo que a opção [**/Pack**](-pack.md) .</span><span class="sxs-lookup"><span data-stu-id="91eaf-105">The **/Zp** switch is the same as the [**/pack**](-pack.md) option.</span></span>

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a><span data-ttu-id="91eaf-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="91eaf-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="91eaf-107">*nível de embalagem \_*</span><span class="sxs-lookup"><span data-stu-id="91eaf-107">*packing\_level*</span></span> 
</dt> <dd>

<span data-ttu-id="91eaf-108">Especifica o nível de empacotamento das estruturas no sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="91eaf-108">Specifies the packing level of structures in the target system.</span></span> <span data-ttu-id="91eaf-109">O valor de nível de embalagem pode ser definido como 1, 2, 4 ou 8.</span><span class="sxs-lookup"><span data-stu-id="91eaf-109">The packing-level value can be set to 1, 2, 4, or 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91eaf-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="91eaf-110">Remarks</span></span>

<span data-ttu-id="91eaf-111">A opção **/ZP** designa o nível de empacotamento das estruturas no sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="91eaf-111">The **/Zp** switch designates the packing level of structures in the target system.</span></span> <span data-ttu-id="91eaf-112">O valor de nível de embalagem corresponde ao valor de opção **/ZP** usado pelo compilador C/C++ da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="91eaf-112">The packing-level value corresponds to the **/Zp** option value used by the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="91eaf-113">Para obter mais informações, consulte a documentação de programação do Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="91eaf-113">For more information, see your Microsoft C/C++ programming documentation.</span></span>

<span data-ttu-id="91eaf-114">Especifique o mesmo nível de embalagem ao invocar o compilador MIDL e o compilador C.</span><span class="sxs-lookup"><span data-stu-id="91eaf-114">Specify the same packing level when you invoke the MIDL compiler and the C compiler.</span></span>

<span data-ttu-id="91eaf-115">O nível de empacotamento padrão usado quando nem a opção **/ZP** nem [**/Pack**](-pack.md) é especificada é 8 em todos os ambientes de compilação.</span><span class="sxs-lookup"><span data-stu-id="91eaf-115">The default packing level used when neither the **/Zp** nor [**/pack**](-pack.md) switch is specified is 8 in all build environments.</span></span>

> [!Note]  
> <span data-ttu-id="91eaf-116">Não use **/Zp1** ou **/ZP2** em plataformas MIPS ou Alpha e não use **/Zp4** ou **/Zp8** em plataformas de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="91eaf-116">Do not use **/Zp1** or **/Zp2** on MIPS or Alpha platforms and do not use **/Zp4** or **/Zp8** on 16-bit platforms.</span></span> <span data-ttu-id="91eaf-117">Dependendo do tipo de dados e do local da memória atribuído pelo compilador C em tempo de execução, isso pode resultar em uma exceção de desalinhamento de dados em plataformas MIPS e Alpha.</span><span class="sxs-lookup"><span data-stu-id="91eaf-117">Depending on the data type and memory location assigned by the C compiler at run time, this can result in a data misalignment exception on MIPS and Alpha platforms.</span></span> <span data-ttu-id="91eaf-118">Em plataformas MS-DOS, o compilador C não garantirá o alinhamento em 4 ou 8 e, portanto, o aplicativo poderá ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="91eaf-118">On MS-DOS platforms, the C compiler will not ensure the alignment at 4 or 8, and so the application may terminate.</span></span>

 

## <a name="examples"></a><span data-ttu-id="91eaf-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91eaf-119">Examples</span></span>

<span data-ttu-id="91eaf-120">**MIDL/Zp4 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="91eaf-120">**midl /Zp4 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="91eaf-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="91eaf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91eaf-122">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="91eaf-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="91eaf-123">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="91eaf-123">**/pack**</span></span>](-pack.md)
</dt> </dl>

 

 




