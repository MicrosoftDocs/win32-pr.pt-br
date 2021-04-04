---
title: comutador/savePP
description: Quando a diretiva/savePP é especificada, o compilador MIDL não exclui a saída do pré-processador C/C++.
ms.assetid: 65a687a5-55ec-4e76-bcfc-38c0a317b85b
keywords:
- MIDL do comutador/savePP
topic_type:
- apiref
api_name:
- /savePP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d3ab7032768cacfab6415548a09def453ab4f9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006563"
---
# <a name="savepp-switch"></a><span data-ttu-id="31ae3-104">comutador/savePP</span><span class="sxs-lookup"><span data-stu-id="31ae3-104">/savePP switch</span></span>

<span data-ttu-id="31ae3-105">Quando a diretiva **/savePP** é especificada, o compilador MIDL não exclui a saída do pré-processador C/C++.</span><span class="sxs-lookup"><span data-stu-id="31ae3-105">When the **/savePP** directive is specified, the MIDL compiler does not delete the output of the C/C++ preprocessor.</span></span>

``` syntax
midl /savePP
```

## <a name="switch-options"></a><span data-ttu-id="31ae3-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="31ae3-106">Switch Options</span></span>

<span data-ttu-id="31ae3-107">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="31ae3-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="31ae3-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="31ae3-108">Remarks</span></span>

<span data-ttu-id="31ae3-109">Essa opção permite aos desenvolvedores discernir o que está sendo analisado pelo compilador MIDL e é útil para a depuração.</span><span class="sxs-lookup"><span data-stu-id="31ae3-109">This switch enables developers to discern what is being parsed by the MIDL compiler, and is useful for debugging.</span></span> <span data-ttu-id="31ae3-110">A saída do pré-processador é gravada em um ou mais arquivos temporários no diretório indicado pela variável de ambiente TEMP.</span><span class="sxs-lookup"><span data-stu-id="31ae3-110">The output of the preprocessor is written to one or more temporary files in the directory indicated by the TEMP environment variable.</span></span> <span data-ttu-id="31ae3-111">O nome do arquivo de saída, ou arquivos, segue uma Convenção de nomenclatura de MID \* . tmp.</span><span class="sxs-lookup"><span data-stu-id="31ae3-111">The name of the output file, or files, follows a naming convention of MID\*.tmp.</span></span> <span data-ttu-id="31ae3-112">Observe que uma única compilação pode gerar vários fluxos de entrada pré-processados; Isso ocorre porque a importação de um arquivo IDL, em oposição ao uso de **\# include**, faz com que um pré-processador separado seja executado.</span><span class="sxs-lookup"><span data-stu-id="31ae3-112">Note that a single compile may generate several preprocessed input streams; this is because importing an IDL file, as opposed to using **\#include**, causes a separate preprocessor run.</span></span>

## <a name="see-also"></a><span data-ttu-id="31ae3-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="31ae3-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ae3-114">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="31ae3-114">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="31ae3-115">**/cpp \_ aceitar**</span><span class="sxs-lookup"><span data-stu-id="31ae3-115">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="31ae3-116">/// \_ /nocpp</span><span class="sxs-lookup"><span data-stu-id="31ae3-116">/no\_cpp, /nocpp</span></span>](-no-cpp-nocpp.md)
</dt> </dl>

 

 




