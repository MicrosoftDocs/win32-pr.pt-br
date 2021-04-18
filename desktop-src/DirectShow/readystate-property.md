---
description: A propriedade ReadyState recupera o ReadyState do objeto MSWebDVD.
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: Propriedade ReadyState (Ocidl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- READYSTATE
api_type:
- HeaderDef
api_location:
- ocidl.h
ms.openlocfilehash: a52b20349c58e8bd44458266da6a0a33ea149c98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757008"
---
# <a name="readystate-property"></a><span data-ttu-id="dad13-103">Propriedade ReadyState</span><span class="sxs-lookup"><span data-stu-id="dad13-103">ReadyState Property</span></span>

> [!Note]  
> <span data-ttu-id="dad13-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dad13-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="dad13-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="dad13-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="dad13-106">A `ReadyState` propriedade recupera o ReadyState do objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="dad13-106">The `ReadyState` property retrieves the ReadyState of the **MSWebDVD** object.</span></span>

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a><span data-ttu-id="dad13-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="dad13-107">Return Value</span></span>

<span data-ttu-id="dad13-108">Retorna um valor inteiro que representa o ReadyState do controle.</span><span class="sxs-lookup"><span data-stu-id="dad13-108">Returns an integer value representing the control's ReadyState.</span></span>



| <span data-ttu-id="dad13-109">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="dad13-109">Return code</span></span> | <span data-ttu-id="dad13-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="dad13-110">Description</span></span>                                               |
|-------------|-----------------------------------------------------------|
| <span data-ttu-id="dad13-111">0</span><span class="sxs-lookup"><span data-stu-id="dad13-111">0</span></span>           | <span data-ttu-id="dad13-112">Estado de inicialização padrão.</span><span class="sxs-lookup"><span data-stu-id="dad13-112">Default initialization state.</span></span>                             |
| <span data-ttu-id="dad13-113">1</span><span class="sxs-lookup"><span data-stu-id="dad13-113">1</span></span>           | <span data-ttu-id="dad13-114">O objeto está carregando suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dad13-114">Object is loading its properties.</span></span>                         |
| <span data-ttu-id="dad13-115">2</span><span class="sxs-lookup"><span data-stu-id="dad13-115">2</span></span>           | <span data-ttu-id="dad13-116">O objeto foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="dad13-116">Object has been initialized.</span></span>                              |
| <span data-ttu-id="dad13-117">3</span><span class="sxs-lookup"><span data-stu-id="dad13-117">3</span></span>           | <span data-ttu-id="dad13-118">O objeto é interativo, mas nem todos os seus dados estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="dad13-118">Object is interactive, but not all its data is available.</span></span> |
| <span data-ttu-id="dad13-119">4</span><span class="sxs-lookup"><span data-stu-id="dad13-119">4</span></span>           | <span data-ttu-id="dad13-120">O objeto recebeu todos os seus dados.</span><span class="sxs-lookup"><span data-stu-id="dad13-120">Object has received all its data.</span></span>                         |



 

## <a name="remarks"></a><span data-ttu-id="dad13-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="dad13-121">Remarks</span></span>

<span data-ttu-id="dad13-122">Esta propriedade é somente leitura sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="dad13-122">This property is read-only with no default value.</span></span>

<span data-ttu-id="dad13-123">Qualquer objeto inserido em uma página da Web expõe a `ReadyState` propriedade.</span><span class="sxs-lookup"><span data-stu-id="dad13-123">Any object embedded in a Web page exposes the `ReadyState` property.</span></span>

## <a name="requirements"></a><span data-ttu-id="dad13-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dad13-124">Requirements</span></span>



| <span data-ttu-id="dad13-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="dad13-125">Requirement</span></span> | <span data-ttu-id="dad13-126">Valor</span><span class="sxs-lookup"><span data-stu-id="dad13-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dad13-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dad13-127">Header</span></span><br/> | <dl> <span data-ttu-id="dad13-128"><dt>Ocidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dad13-128"><dt>Ocidl.h</dt></span></span> </dl> |



 

 




