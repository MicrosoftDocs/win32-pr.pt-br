---
title: comutador/Pack
description: O comutador/Pack é o mesmo que a opção/ZP.
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- MIDL do comutador/Pack
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c807846148d81e0e59620046d9f24380fe647c11
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006664"
---
# <a name="pack-switch"></a><span data-ttu-id="b0302-104">comutador/Pack</span><span class="sxs-lookup"><span data-stu-id="b0302-104">/pack switch</span></span>

<span data-ttu-id="b0302-105">O comutador **/Pack** é o mesmo que a opção [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="b0302-105">The **/pack** switch is the same as the [**/Zp**](-zp.md) option.</span></span>

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a><span data-ttu-id="b0302-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="b0302-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="b0302-107">*nível de embalagem \_*</span><span class="sxs-lookup"><span data-stu-id="b0302-107">*packing\_level*</span></span> 
</dt> <dd>

<span data-ttu-id="b0302-108">Especifica o nível de empacotamento das estruturas no sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="b0302-108">Specifies the packing level of structures in the target system.</span></span> <span data-ttu-id="b0302-109">O valor de nível de embalagem pode ser definido como 1, 2, 4 ou 8.</span><span class="sxs-lookup"><span data-stu-id="b0302-109">The packing-level value can be set to 1, 2, 4, or 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0302-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0302-110">Remarks</span></span>

<span data-ttu-id="b0302-111">A opção **/Pack** designa o nível de empacotamento das estruturas no sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="b0302-111">The **/pack** switch designates the packing level of structures in the target system.</span></span> <span data-ttu-id="b0302-112">O valor de nível de embalagem corresponde ao valor de opção [**/ZP**](-zp.md) usado pelo compilador Microsoft C/C++ versão 7,0.</span><span class="sxs-lookup"><span data-stu-id="b0302-112">The packing-level value corresponds to the [**/Zp**](-zp.md) option value used by the Microsoft C/C++ version 7.0 compiler.</span></span> <span data-ttu-id="b0302-113">Para obter mais informações, consulte a documentação de programação do Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="b0302-113">For more information, see your Microsoft C/C++ programming documentation.</span></span>

<span data-ttu-id="b0302-114">Especifique o mesmo nível de embalagem ao invocar o compilador MIDL e o compilador C.</span><span class="sxs-lookup"><span data-stu-id="b0302-114">Specify the same packing level when you invoke the MIDL compiler and the C compiler.</span></span> <span data-ttu-id="b0302-115">O nível de empacotamento padrão usado quando nem a opção [**/ZP**](-zp.md) nem **/Pack** é especificada é 8, em todos os ambientes de compilação.</span><span class="sxs-lookup"><span data-stu-id="b0302-115">The default packing level used when neither the [**/Zp**](-zp.md) nor **/pack** switch is specified is 8, in both all build environments.</span></span>

<span data-ttu-id="b0302-116">Para obter uma discussão sobre os perigos potenciais no uso de níveis de embalagem não padrão, consulte o tópico da ajuda do [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="b0302-116">For a discussion of the potential dangers in using nonstandard packing levels, see the [**/Zp**](-zp.md) help topic.</span></span>

## <a name="examples"></a><span data-ttu-id="b0302-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b0302-117">Examples</span></span>

<span data-ttu-id="b0302-118">**MIDL/Pack 2 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="b0302-118">**midl /pack 2 filename.idl**</span></span>

<span data-ttu-id="b0302-119">**MIDL/Pack 8 bar. idl**</span><span class="sxs-lookup"><span data-stu-id="b0302-119">**midl /pack 8 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="b0302-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0302-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0302-121">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="b0302-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="b0302-122">**/env**</span><span class="sxs-lookup"><span data-stu-id="b0302-122">**/env**</span></span>](-env.md)
</dt> <dt>

[<span data-ttu-id="b0302-123">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="b0302-123">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




