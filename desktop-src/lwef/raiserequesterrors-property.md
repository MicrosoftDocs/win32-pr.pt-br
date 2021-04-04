---
title: Propriedade RaiseRequestErrors
description: Propriedade RaiseRequestErrors
ms.assetid: 60eb4478-526e-492a-8fb3-d1e54eff9868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9e559f999db663a8a9f5874f6d16a10e1e78ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104162242"
---
# <a name="raiserequesterrors-property"></a><span data-ttu-id="2eeff-103">Propriedade RaiseRequestErrors</span><span class="sxs-lookup"><span data-stu-id="2eeff-103">RaiseRequestErrors Property</span></span>

<span data-ttu-id="2eeff-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2eeff-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2eeff-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="2eeff-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2eeff-106">Retorna ou define se erros de solicitações são gerados.</span><span class="sxs-lookup"><span data-stu-id="2eeff-106">Returns or sets whether errors for requests are raised.</span></span>

</dd> <dt>

<span data-ttu-id="2eeff-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="2eeff-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2eeff-108">\*Agent \* \* *. RaiseRequestErrors* \*  \[  =  *booliano*\]</span><span class="sxs-lookup"><span data-stu-id="2eeff-108">*agent\*\*\*.RaiseRequestErrors*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="2eeff-109">Parte</span><span class="sxs-lookup"><span data-stu-id="2eeff-109">Part</span></span>      | <span data-ttu-id="2eeff-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="2eeff-110">Description</span></span>                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eeff-111">*booleano*</span><span class="sxs-lookup"><span data-stu-id="2eeff-111">*boolean*</span></span> | <span data-ttu-id="2eeff-112">Um valor booliano que determina se erros em solicitações são gerados.</span><span class="sxs-lookup"><span data-stu-id="2eeff-112">A Boolean value that determines whether errors in requests are raised.</span></span><br/> <span data-ttu-id="2eeff-113">Erros de solicitação **true** (padrão) são gerados.</span><span class="sxs-lookup"><span data-stu-id="2eeff-113">**True**    (Default) Request errors are raised.</span></span> <br/> <span data-ttu-id="2eeff-114">**Falso**     Os erros de solicitação não são gerados.</span><span class="sxs-lookup"><span data-stu-id="2eeff-114">**False**     Request errors are not raised.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2eeff-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2eeff-115">Remarks</span></span>

<span data-ttu-id="2eeff-116">Essa propriedade permite que você determine se o servidor gera erros que ocorrem com métodos que dão suporte a objetos de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="2eeff-116">This property enables you to determine whether the server raises errors that occur with methods that support [**Request**](/windows/desktop/lwef/the-request-object) objects.</span></span> <span data-ttu-id="2eeff-117">Por exemplo, se você especificar um nome de animação que não exista em um método [**Play**](play-method.md), o servidor gerará um erro (exibindo a mensagem de erro), a menos que você defina essa propriedade como **false**.</span><span class="sxs-lookup"><span data-stu-id="2eeff-117">For example, if you specify an animation name that does not exist in a [**Play**](play-method.md)method, the server raises an error (displaying the error message) unless you set this property to **False**.</span></span>

<span data-ttu-id="2eeff-118">Pode ser útil para linguagens de programação que não fornecem recuperação quando um erro é gerado.</span><span class="sxs-lookup"><span data-stu-id="2eeff-118">It may be useful for programming languages that do not provide recovery when an error is raised.</span></span> <span data-ttu-id="2eeff-119">No entanto, tenha cuidado ao definir essa propriedade como **false**, pois pode ser mais difícil encontrar erros em seu código.</span><span class="sxs-lookup"><span data-stu-id="2eeff-119">However, use care when setting this property to **False**, because it might be harder to find errors in your code.</span></span>

 

