---
title: Atributos de tipo de ponteiro
description: Os atributos a seguir especificam as características dos ponteiros.
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- MIDL, atributos, tipo de ponteiro de IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71371fff80d541242fcdc41d6c8adcc93dcdb754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637187"
---
# <a name="pointer-type-attributes"></a><span data-ttu-id="81eb2-104">Atributos de tipo de ponteiro</span><span class="sxs-lookup"><span data-stu-id="81eb2-104">Pointer Type Attributes</span></span>

<span data-ttu-id="81eb2-105">Os atributos a seguir especificam as características dos ponteiros.</span><span class="sxs-lookup"><span data-stu-id="81eb2-105">The following attributes specify the characteristics of pointers.</span></span>



| <span data-ttu-id="81eb2-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="81eb2-106">Attribute</span></span>                                   | <span data-ttu-id="81eb2-107">Uso</span><span class="sxs-lookup"><span data-stu-id="81eb2-107">Usage</span></span>                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81eb2-108">**ptr**</span><span class="sxs-lookup"><span data-stu-id="81eb2-108">**ptr**</span></span>](ptr.md)                          | <span data-ttu-id="81eb2-109">Designa um ponteiro como um ponteiro completo, com todos os recursos de um ponteiro de linguagem C, incluindo alias.</span><span class="sxs-lookup"><span data-stu-id="81eb2-109">Designates a pointer as a full pointer, with all the capabilities of a C-language pointer, including aliasing.</span></span>                                                                                       |
| [<span data-ttu-id="81eb2-110">**ref**</span><span class="sxs-lookup"><span data-stu-id="81eb2-110">**ref**</span></span>](ref.md)                          | <span data-ttu-id="81eb2-111">Designa o tipo mais simples de ponteiro no MIDL — um que simplesmente fornece o endereço de alguns dados.</span><span class="sxs-lookup"><span data-stu-id="81eb2-111">Designates the simplest type of pointer in MIDL—one that simply provides the address of some data.</span></span> <span data-ttu-id="81eb2-112">Ponteiros de referência nunca podem ser nulos.</span><span class="sxs-lookup"><span data-stu-id="81eb2-112">Reference pointers can never be null.</span></span>                                                             |
| [<span data-ttu-id="81eb2-113">**diferente**</span><span class="sxs-lookup"><span data-stu-id="81eb2-113">**unique**</span></span>](unique.md)                    | <span data-ttu-id="81eb2-114">Permite que um ponteiro seja nulo, mas não oferece suporte a aliases.</span><span class="sxs-lookup"><span data-stu-id="81eb2-114">Lets a pointer be null, but does not support aliasing.</span></span>                                                                                                                                               |
| [<span data-ttu-id="81eb2-115">**padrão de ponteiro \_**</span><span class="sxs-lookup"><span data-stu-id="81eb2-115">**pointer\_default**</span></span>](pointer-default.md) | <span data-ttu-id="81eb2-116">Aplicado a uma interface para especificar o tipo de ponteiro padrão para todos os ponteiros nessa interface, exceto para ponteiros de parâmetro de nível superior, que são automaticamente padronizados para ponteiros de [**referência**](ref.md) .</span><span class="sxs-lookup"><span data-stu-id="81eb2-116">Applied to an interface to specify the default pointer type for all pointers in that interface, except for top-level parameter pointers, which automatically default to [**ref**](ref.md) pointers.</span></span> |
| [<span data-ttu-id="81eb2-117">**IID \_ é**</span><span class="sxs-lookup"><span data-stu-id="81eb2-117">**iid\_is**</span></span>](iid-is.md)                   | <span data-ttu-id="81eb2-118">Fornece o identificador de interface da interface COM que é o objeto do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="81eb2-118">Provides the interface identifier of the COM interface that is the object of the pointer.</span></span>                                                                                                            |
| [<span data-ttu-id="81eb2-119">**Strings**</span><span class="sxs-lookup"><span data-stu-id="81eb2-119">**string**</span></span>](string.md)                    | <span data-ttu-id="81eb2-120">Especifica que o ponteiro aponta para uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="81eb2-120">Specifies that the pointer points to a string.</span></span>                                                                                                                                                       |



 

 

 




