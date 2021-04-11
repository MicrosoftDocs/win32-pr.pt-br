---
title: comutador/oldtlb
description: A opção/oldtlb instrui o compilador MIDL a gerar uma biblioteca de tipos de formato antigo.
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- MIDL do comutador/oldtlb
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a08e468d0acff16aa1df4a45fcacafeb676b00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365899"
---
# <a name="oldtlb-switch"></a><span data-ttu-id="42b64-104">comutador/oldtlb</span><span class="sxs-lookup"><span data-stu-id="42b64-104">/oldtlb switch</span></span>

<span data-ttu-id="42b64-105">A opção **/oldtlb** instrui o compilador MIDL a gerar uma biblioteca de tipos de formato antigo.</span><span class="sxs-lookup"><span data-stu-id="42b64-105">The **/oldtlb** switch directs the MIDL compiler to generate an old-format type library.</span></span>

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a><span data-ttu-id="42b64-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="42b64-106">Switch Options</span></span>

<span data-ttu-id="42b64-107">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="42b64-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="42b64-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="42b64-108">Remarks</span></span>

<span data-ttu-id="42b64-109">A opção **/oldtlb** substitui o padrão e direciona o compilador MIDL para gerar bibliotecas de tipo de formato antigo mesmo em versões atuais do Windows usando [createtypelib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) em vez de [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).</span><span class="sxs-lookup"><span data-stu-id="42b64-109">The **/oldtlb** switch overrides the default and directs the MIDL compiler to generate old-format type libraries even on current versions of Windows by using [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) instead of [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).</span></span>

## <a name="examples"></a><span data-ttu-id="42b64-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="42b64-110">Examples</span></span>

<span data-ttu-id="42b64-111">**MIDL/oldtlb filename. idl**</span><span class="sxs-lookup"><span data-stu-id="42b64-111">**midl /oldtlb filename.idl**</span></span>

<span data-ttu-id="42b64-112">**MIDL/oldtlb myoldodl. odl**</span><span class="sxs-lookup"><span data-stu-id="42b64-112">**midl /oldtlb myoldodl.odl**</span></span>

## <a name="see-also"></a><span data-ttu-id="42b64-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="42b64-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42b64-114">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="42b64-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="42b64-115">**/newtlb**</span><span class="sxs-lookup"><span data-stu-id="42b64-115">**/newtlb**</span></span>](-newtlb.md)
</dt> </dl>

 

 