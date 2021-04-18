---
description: O compilador formato MOF (MOF) dá suporte a dois estilos de comentário usando dois estilos diferentes de delimitadores de comentário.
ms.assetid: 5ab71b45-7ed1-44c4-8710-6b833b0afb80
ms.tgt_platform: multiple
title: Criando um comentário
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d0e7cf2484fef018c62c8c47d9c55d245191681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788759"
---
# <a name="creating-a-comment"></a><span data-ttu-id="9fb51-103">Criando um comentário</span><span class="sxs-lookup"><span data-stu-id="9fb51-103">Creating a Comment</span></span>

<span data-ttu-id="9fb51-104">O compilador formato MOF (MOF) dá suporte a dois estilos de comentário usando dois estilos diferentes de delimitadores de comentário.</span><span class="sxs-lookup"><span data-stu-id="9fb51-104">The Managed Object Format (MOF) compiler supports two styles of comment using two different styles of comment delimiters.</span></span>

<span data-ttu-id="9fb51-105">A tabela a seguir lista os delimitadores que são usados para comentários e o efeito que os delimitadores têm no código.</span><span class="sxs-lookup"><span data-stu-id="9fb51-105">The following table lists the delimiters that are used for comments and the effect that the delimiters have in the code.</span></span>



| <span data-ttu-id="9fb51-106">Delimitador</span><span class="sxs-lookup"><span data-stu-id="9fb51-106">Delimiter</span></span>   | <span data-ttu-id="9fb51-107">Marcas</span><span class="sxs-lookup"><span data-stu-id="9fb51-107">Marks</span></span>                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | <span data-ttu-id="9fb51-108">Início de um comentário que termina no final da linha.</span><span class="sxs-lookup"><span data-stu-id="9fb51-108">Start of a comment that terminates at the end of the line.</span></span>                                    |
| <span data-ttu-id="9fb51-109">/\* e \*/</span><span class="sxs-lookup"><span data-stu-id="9fb51-109">/\* and \*/</span></span> | <span data-ttu-id="9fb51-110">Início e fim de um comentário que pode abranger várias linhas ou apenas uma parte de uma linha.</span><span class="sxs-lookup"><span data-stu-id="9fb51-110">Beginning and end of a comment that may span multiple lines or only span a portion of a line.</span></span> |



 

<span data-ttu-id="9fb51-111">Como nas linguagens de programação C e C++, você deve usar o delimitador//somente com comentários de linha única, mas usar os delimitadores/ \* e \* /com comentários de linha única ou de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="9fb51-111">As in the C and C++ programming languages, you must use the // delimiter with single-line comments only, but use the /\* and \*/ delimiters with either single-line or multiple-line comments.</span></span>

<span data-ttu-id="9fb51-112">O exemplo de código a seguir descreve os dois estilos de delimitador.</span><span class="sxs-lookup"><span data-stu-id="9fb51-112">The following code example describes the two delimiter styles.</span></span>

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a><span data-ttu-id="9fb51-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9fb51-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fb51-114">Criando classes formato MOF (MOF)</span><span class="sxs-lookup"><span data-stu-id="9fb51-114">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



