---
title: Propriedade HasOtherClients
description: Propriedade HasOtherClients
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3434cec191d2bec93d501847df064a8dbbf3e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005548"
---
# <a name="hasotherclients-property"></a><span data-ttu-id="b2db0-103">Propriedade HasOtherClients</span><span class="sxs-lookup"><span data-stu-id="b2db0-103">HasOtherClients Property</span></span>

<span data-ttu-id="b2db0-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b2db0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b2db0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="b2db0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b2db0-106">Retorna se o caractere especificado está sendo usado por outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b2db0-106">Returns whether the specified character is in use by other applications.</span></span>

</dd> <dt>

<span data-ttu-id="b2db0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="b2db0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b2db0-108">*agente* do. **Caracteres ("***characterid***"). HasOtherClients**</span><span class="sxs-lookup"><span data-stu-id="b2db0-108">*agent*.**Characters("***CharacterID***").HasOtherClients**</span></span>



| <span data-ttu-id="b2db0-109">Valor</span><span class="sxs-lookup"><span data-stu-id="b2db0-109">Value</span></span>     | <span data-ttu-id="b2db0-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2db0-110">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="b2db0-111">**Verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="b2db0-111">**True**</span></span>  | <span data-ttu-id="b2db0-112">O caractere tem outros clientes.</span><span class="sxs-lookup"><span data-stu-id="b2db0-112">The character has other clients.</span></span>           |
| <span data-ttu-id="b2db0-113">**Falso**</span><span class="sxs-lookup"><span data-stu-id="b2db0-113">**False**</span></span> | <span data-ttu-id="b2db0-114">O caractere não tem outros clientes.</span><span class="sxs-lookup"><span data-stu-id="b2db0-114">The character does not have other clients.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2db0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2db0-115">Remarks</span></span>

<span data-ttu-id="b2db0-116">Você pode usar essa propriedade para determinar se seu aplicativo é o único ou o último cliente do caractere, quando mais de um aplicativo está compartilhando (carregado) o mesmo caractere.</span><span class="sxs-lookup"><span data-stu-id="b2db0-116">You can use this property to determine whether your application is the only or last client of the character, when more than one application is sharing (has loaded) the same character.</span></span>

 

 




