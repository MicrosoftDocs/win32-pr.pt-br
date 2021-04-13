---
title: Herança de tipo de Pointer-Attribute
description: De acordo com a especificação do DCE, cada arquivo IDL deve definir atributos para seus ponteiros.
ms.assetid: ab8821ce-d52a-42bf-aa5e-582bb24adf93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182b7d46774484a9520424fd82bcff2d7103aa3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366530"
---
# <a name="pointer-attribute-type-inheritance"></a><span data-ttu-id="f5c29-103">Herança de tipo de Pointer-Attribute</span><span class="sxs-lookup"><span data-stu-id="f5c29-103">Pointer-Attribute Type Inheritance</span></span>

<span data-ttu-id="f5c29-104">De acordo com a especificação do DCE, cada arquivo IDL deve definir atributos para seus ponteiros.</span><span class="sxs-lookup"><span data-stu-id="f5c29-104">According to the DCE specification, each IDL file must define attributes for its pointers.</span></span> <span data-ttu-id="f5c29-105">Se um atributo explícito não for atribuído a um ponteiro, o ponteiro usará o valor especificado pela \[ palavra-chave [ \_ default do ponteiro](/windows/desktop/Midl/pointer-default) \] .</span><span class="sxs-lookup"><span data-stu-id="f5c29-105">If an explicit attribute is not assigned to a pointer, the pointer uses the value specified by the \[ [pointer\_default](/windows/desktop/Midl/pointer-default)\] keyword.</span></span> <span data-ttu-id="f5c29-106">Algumas implementações de DCE não permitem ponteiros sem atributo.</span><span class="sxs-lookup"><span data-stu-id="f5c29-106">Some DCE implementations do not allow unattributed pointers.</span></span> <span data-ttu-id="f5c29-107">Se um ponteiro não tiver um atributo explícito, o arquivo IDL deverá ter uma especificação de **\[ ponteiro \_ padrão \]** para que o atributo de ponteiro possa ser definido.</span><span class="sxs-lookup"><span data-stu-id="f5c29-107">If a pointer does not have an explicit attribute, the IDL file must have a **\[pointer\_default\]** specification so that the pointer attribute can be set.</span></span>

<span data-ttu-id="f5c29-108">No modo padrão (extensões da Microsoft), você pode especificar o atributo de um ponteiro no arquivo IDL que importa o arquivo IDL de definição.</span><span class="sxs-lookup"><span data-stu-id="f5c29-108">In default (Microsoft-extensions) mode, you can specify a pointer's attribute in the IDL file that imports the defining IDL file.</span></span> <span data-ttu-id="f5c29-109">Os ponteiros definidos em um arquivo IDL podem herdar atributos que são especificados em outros arquivos IDL.</span><span class="sxs-lookup"><span data-stu-id="f5c29-109">Pointers defined in one IDL file can inherit attributes that are specified in other IDL files.</span></span> <span data-ttu-id="f5c29-110">Além disso, no modo padrão, os arquivos IDL podem incluir ponteiros não atributos.</span><span class="sxs-lookup"><span data-stu-id="f5c29-110">Also, in default mode, IDL files can include unattributed pointers.</span></span> <span data-ttu-id="f5c29-111">Se nem os arquivos IDL base nem importados especificarem um atributo de ponteiro ou **\[ \_ padrão \] de ponteiro**, os ponteiros não atributo serão interpretados como ponteiros exclusivos.</span><span class="sxs-lookup"><span data-stu-id="f5c29-111">If neither the base nor the imported IDL files specify a pointer attribute or **\[pointer\_default\]**, unattributed pointers are interpreted as unique pointers.</span></span>

<span data-ttu-id="f5c29-112">O compilador MIDL atribui atributos de ponteiro a ponteiros usando as seguintes regras de prioridade (1 é a mais alta).</span><span class="sxs-lookup"><span data-stu-id="f5c29-112">The MIDL compiler assigns pointer attributes to pointers using the following priority rules (1 is highest).</span></span>



| <span data-ttu-id="f5c29-113">Prioridade</span><span class="sxs-lookup"><span data-stu-id="f5c29-113">Priority</span></span> | <span data-ttu-id="f5c29-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5c29-114">Description</span></span>                                                                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c29-115">1</span><span class="sxs-lookup"><span data-stu-id="f5c29-115">1</span></span>        | <span data-ttu-id="f5c29-116">Atributos de ponteiro explícitos são aplicados ao ponteiro na definição ou no site de uso.</span><span class="sxs-lookup"><span data-stu-id="f5c29-116">Explicit pointer attributes are applied to the pointer at the definition or use site.</span></span>                                      |
| <span data-ttu-id="f5c29-117">2</span><span class="sxs-lookup"><span data-stu-id="f5c29-117">2</span></span>        | <span data-ttu-id="f5c29-118">O padrão é o atributo de **\[ ponteiro \_ padrão \]** no arquivo IDL que define o tipo.</span><span class="sxs-lookup"><span data-stu-id="f5c29-118">The default is the **\[pointer\_default\]** attribute in the IDL file that defines the type.</span></span>                               |
| <span data-ttu-id="f5c29-119">3</span><span class="sxs-lookup"><span data-stu-id="f5c29-119">3</span></span>        | <span data-ttu-id="f5c29-120">O padrão é o atributo de **\[ ponteiro \_ padrão \]** no arquivo IDL que importa o tipo.</span><span class="sxs-lookup"><span data-stu-id="f5c29-120">The default is the **\[pointer\_default\]** attribute in the IDL file that imports the type.</span></span>                               |
| <span data-ttu-id="f5c29-121">4</span><span class="sxs-lookup"><span data-stu-id="f5c29-121">4</span></span>        | <span data-ttu-id="f5c29-122">O padrão é \[ [PTR](/windows/desktop/Midl/ptr) \] no modo de compatibilidade com DCE ou \[ [exclusivo](/windows/desktop/Midl/unique) \] no modo de extensões da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f5c29-122">The default is \[ [ptr](/windows/desktop/Midl/ptr)\] in DCE-compatibility mode, or \[ [unique](/windows/desktop/Midl/unique)\] in Microsoft-extensions mode.</span></span> |



 

 

 