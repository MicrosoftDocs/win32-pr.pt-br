---
title: Erros e avisos do compilador MIDL
description: Ao usar o compilador MIDL, erros e avisos podem ser causados pelo uso impróprio das opções de linha de comando ou pelo conteúdo dos arquivos IDL e ACF.
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- MIDL linguagem IDL da Microsoft, referência
- MIDL do compilador MIDL, erros
- MIDL do compilador, erros
- MIDL de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae531528f83f3731b4449c7aba012f3228edd9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822156"
---
# <a name="midl-compiler-errors-and-warnings"></a><span data-ttu-id="e102a-107">Erros e avisos do compilador MIDL</span><span class="sxs-lookup"><span data-stu-id="e102a-107">MIDL Compiler Errors and Warnings</span></span>

<span data-ttu-id="e102a-108">Ao usar o compilador MIDL, erros e avisos podem ser causados pelo uso impróprio das opções de linha de comando ou pelo conteúdo dos arquivos IDL e ACF.</span><span class="sxs-lookup"><span data-stu-id="e102a-108">When using the MIDL compiler, errors and warnings can be caused by improper use of the command-line switches or by the content of the IDL and ACF files.</span></span> <span data-ttu-id="e102a-109">Se o erro for devido à inserção inadequada das opções de linha de comando, uma mensagem de erro ou de aviso poderá especificar o nome de uma ou mais opções do modo de compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="e102a-109">If the error is due to improperly entering the command-line switches, an error or warning message may specify the name of one or more MIDL compiler mode switches.</span></span> <span data-ttu-id="e102a-110">Por exemplo, você pode incluir certos atributos de ACF em um arquivo IDL ao usar a opção **/ \_ configuração de aplicativo** , mas esse arquivo IDL gerará um erro se você compilar sem usar a opção/**\_ configuração de aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="e102a-110">For example, you can include certain ACF attributes in an IDL file when you use the /**app\_config** switch, but that IDL file will generate an error if you compile without using the /**app\_config** switch.</span></span>

<span data-ttu-id="e102a-111">Os erros nos arquivos IDL e ACF se enquadram em duas categorias: erros capturados pelo pré-processador e erros reconhecidos pelo compilador.</span><span class="sxs-lookup"><span data-stu-id="e102a-111">Errors in the IDL and ACF files fall into two categories: errors caught by the preprocessor and errors recognized by the compiler.</span></span> <span data-ttu-id="e102a-112">Esta seção lista o pré-processador de MIDL e as mensagens de erro do compilador.</span><span class="sxs-lookup"><span data-stu-id="e102a-112">This section lists the MIDL preprocessor and compiler error messages.</span></span> <span data-ttu-id="e102a-113">Ele também descreve seus formatos e causas.</span><span class="sxs-lookup"><span data-stu-id="e102a-113">It also describes their formats and causes.</span></span>

-   [<span data-ttu-id="e102a-114">Formatos de mensagem de erro e de aviso</span><span class="sxs-lookup"><span data-stu-id="e102a-114">Error and Warning Message Formats</span></span>](error-and-warning-message-formats.md)
-   [<span data-ttu-id="e102a-115">Erros de pré-processador</span><span class="sxs-lookup"><span data-stu-id="e102a-115">Preprocessor Errors</span></span>](preprocessor-errors.md)
-   [<span data-ttu-id="e102a-116">Erros do compilador</span><span class="sxs-lookup"><span data-stu-id="e102a-116">Compiler Errors</span></span>](compiler-errors.md)

 

 




