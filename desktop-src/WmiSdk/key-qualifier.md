---
description: O qualificador de chave indica se a propriedade faz parte do identificador de namespace.
ms.assetid: 838d295f-e812-4e46-99a4-d2714a0ae8dc
ms.tgt_platform: multiple
title: Qualificador de chave
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Key
api_type:
- NA
api_location: ''
ms.openlocfilehash: affc9f4be594723700a65c9c92f8ae37ffead265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662763"
---
# <a name="key-qualifier"></a><span data-ttu-id="acc64-103">Qualificador de chave</span><span class="sxs-lookup"><span data-stu-id="acc64-103">Key Qualifier</span></span>

<span data-ttu-id="acc64-104">O qualificador de **chave** indica se a propriedade faz parte do identificador de namespace.</span><span class="sxs-lookup"><span data-stu-id="acc64-104">The **Key** qualifier indicates whether the property is part of the namespace handle.</span></span> <span data-ttu-id="acc64-105">Se mais de uma propriedade tiver o qualificador de **chave** , todas essas propriedades formarão coletivamente a chave (uma chave composta).</span><span class="sxs-lookup"><span data-stu-id="acc64-105">If more than one property has the **Key** qualifier, then all such properties collectively form the key (a compound key).</span></span> <span data-ttu-id="acc64-106">Quando agrupadas, as propriedades de chave devem fornecer uma referência exclusiva para cada instância de classe.</span><span class="sxs-lookup"><span data-stu-id="acc64-106">When taken together, the key properties must supply a unique reference for each class instance.</span></span> <span data-ttu-id="acc64-107">Se esse qualificador for colocado em uma propriedade, somente o valor **true** será permitido.</span><span class="sxs-lookup"><span data-stu-id="acc64-107">If this qualifier is placed on a property, only the value **TRUE** is allowed.</span></span>

<span data-ttu-id="acc64-108">Você pode usar qualquer tipo de propriedade, exceto o seguinte:</span><span class="sxs-lookup"><span data-stu-id="acc64-108">You can use any property type except for the following:</span></span>

-   <span data-ttu-id="acc64-109">Matrizes</span><span class="sxs-lookup"><span data-stu-id="acc64-109">Arrays</span></span>
-   <span data-ttu-id="acc64-110">Números de ponto flutuante e real</span><span class="sxs-lookup"><span data-stu-id="acc64-110">Real and floating-point numbers</span></span>
-   <span data-ttu-id="acc64-111">Objetos inseridos</span><span class="sxs-lookup"><span data-stu-id="acc64-111">Embedded objects</span></span>
-   <span data-ttu-id="acc64-112">Caracteres inferiores a ASCII 32 (ou seja, caracteres de espaço em branco)</span><span class="sxs-lookup"><span data-stu-id="acc64-112">Characters lower than ASCII 32 (that is, white space characters)</span></span>
-   <span data-ttu-id="acc64-113">Cadeias de caracteres do tipo **char16** ou cadeias de caracteres definidas como chaves devem conter valores maiores que U + 0020.</span><span class="sxs-lookup"><span data-stu-id="acc64-113">Character strings of type **char16** or character strings that are defined as keys must contain values greater than U+0020.</span></span> <span data-ttu-id="acc64-114">Isso ocorre porque o WMI usa valores de chave em caminhos de objeto e você não pode usar caracteres não imprimíveis em um caminho de objeto.</span><span class="sxs-lookup"><span data-stu-id="acc64-114">This is because WMI uses key values in object paths, and you cannot use nonprinting characters in an object path.</span></span>

<span data-ttu-id="acc64-115">Quando uma classe pai especifica uma chave, todas as classes derivadas da classe pai herdam essa chave.</span><span class="sxs-lookup"><span data-stu-id="acc64-115">When a parent class specifies a key, all classes derived from the parent class inherit that key.</span></span> <span data-ttu-id="acc64-116">As classes derivadas não podem alterar a chave herdada nem definir nenhuma nova propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="acc64-116">The derived classes cannot alter the inherited key or define any new key property.</span></span> <span data-ttu-id="acc64-117">No entanto, quando você deriva uma subclasse de uma classe abstrata sem uma chave, você pode introduzir uma chave na subclasse.</span><span class="sxs-lookup"><span data-stu-id="acc64-117">However, when you derive a subclass from an abstract class without a key, you can introduce a key in the subclass.</span></span>

<span data-ttu-id="acc64-118">Todas as classes que definem mais de uma instância devem especificar uma chave.</span><span class="sxs-lookup"><span data-stu-id="acc64-118">All classes that define more than one instance must specify a key.</span></span> <span data-ttu-id="acc64-119">Como as classes abstratas não definem nenhuma instância, elas não precisam especificar chaves.</span><span class="sxs-lookup"><span data-stu-id="acc64-119">Because abstract classes do not define any instances, they do not need to specify keys.</span></span> <span data-ttu-id="acc64-120">Como as classes singleton definem apenas uma instância, elas não podem especificar chaves.</span><span class="sxs-lookup"><span data-stu-id="acc64-120">Because singleton classes define only one instance, they cannot specify keys.</span></span>

<span data-ttu-id="acc64-121">As chaves são gravadas uma vez na instanciação do objeto e não devem ser modificadas posteriormente.</span><span class="sxs-lookup"><span data-stu-id="acc64-121">Keys are written one time at object instantiation and must not be modified later.</span></span> <span data-ttu-id="acc64-122">Não faz sentido aplicar um valor padrão a uma propriedade qualificada por chave.</span><span class="sxs-lookup"><span data-stu-id="acc64-122">It does not make sense to apply a default value to a key-qualified property.</span></span>

## <a name="requirements"></a><span data-ttu-id="acc64-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acc64-123">Requirements</span></span>



| <span data-ttu-id="acc64-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="acc64-124">Requirement</span></span> | <span data-ttu-id="acc64-125">Valor</span><span class="sxs-lookup"><span data-stu-id="acc64-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="acc64-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acc64-126">Minimum supported client</span></span><br/> | <span data-ttu-id="acc64-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="acc64-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="acc64-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acc64-128">Minimum supported server</span></span><br/> | <span data-ttu-id="acc64-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acc64-129">Windows Server 2008</span></span><br/> |



 

 




