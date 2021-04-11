---
title: comutador/LCID
description: A opção de compilador/LCID MIDL permite que você use caracteres internacionais em seus arquivos de entrada, nomes de arquivos e caminhos de diretório.
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- MIDL do comutador/LCID
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370548bb9899ce84173f2321a129aaeda1c6fe81
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293329"
---
# <a name="lcid-switch"></a><span data-ttu-id="e0710-104">comutador/LCID</span><span class="sxs-lookup"><span data-stu-id="e0710-104">/lcid switch</span></span>

<span data-ttu-id="e0710-105">A opção de compilador **/LCID** MIDL permite que você use caracteres internacionais em seus arquivos de entrada, nomes de arquivos e caminhos de diretório.</span><span class="sxs-lookup"><span data-stu-id="e0710-105">The **/lcid** MIDL compiler option lets you use international characters in your input files, file names, and directory paths.</span></span>

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a><span data-ttu-id="e0710-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="e0710-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="e0710-107">*localeID*</span><span class="sxs-lookup"><span data-stu-id="e0710-107">*localeID*</span></span> 
</dt> <dd>

<span data-ttu-id="e0710-108">Especifica o identificador de localidade de 32 bits usado no suporte ao idioma nacional do Windows.</span><span class="sxs-lookup"><span data-stu-id="e0710-108">Specifies the 32-bit locale identifier used in Windows National Language Support.</span></span> <span data-ttu-id="e0710-109">O identificador de localidade deve ser especificado em decimal.</span><span class="sxs-lookup"><span data-stu-id="e0710-109">The locale identifier should be specified in decimal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0710-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0710-110">Remarks</span></span>

<span data-ttu-id="e0710-111">Nos arquivos de entrada, você pode usar comentários localizados, cadeias de caracteres, HelpStrings e identificadores.</span><span class="sxs-lookup"><span data-stu-id="e0710-111">Within the input files, you can use localized comments, strings, helpstrings and identifiers.</span></span> <span data-ttu-id="e0710-112">Em particular, a opção **/LCID** fornece suporte completo a DBCS, para representar idiomas asiáticos, como japonês, chinês e coreano.</span><span class="sxs-lookup"><span data-stu-id="e0710-112">In particular, the **/lcid** switch provides full DBCS support, to represent Asian languages such as Japanese, Chinese, and Korean.</span></span>

> [!Note]  
> <span data-ttu-id="e0710-113">A opção **/LCID** está disponível com o MIDL versão 3.01.75 e posterior.</span><span class="sxs-lookup"><span data-stu-id="e0710-113">The **/lcid** switch is available with MIDL version 3.01.75 and later.</span></span>

 

## <a name="examples"></a><span data-ttu-id="e0710-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0710-114">Examples</span></span>

<span data-ttu-id="e0710-115">**MIDL/LCID 1041 iface. idl**</span><span class="sxs-lookup"><span data-stu-id="e0710-115">**midl /lcid 1041 iface.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="e0710-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0710-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0710-117">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="e0710-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="e0710-118">**LCID**</span><span class="sxs-lookup"><span data-stu-id="e0710-118">**lcid**</span></span>](lcid.md)
</dt> </dl>

 

 




