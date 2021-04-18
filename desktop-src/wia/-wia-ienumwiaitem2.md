---
description: Usado por aplicativos para enumerar objetos IWiaItem2 na pasta atual da árvore de itens.
ms.assetid: a82298e0-fbe7-4ef5-99c5-18ff60538e03
title: Interface IEnumWiaItem2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: f6e41b3172793f696a9ea3c2d319bdee6ca3d691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752608"
---
# <a name="ienumwiaitem2-interface"></a><span data-ttu-id="3a9b4-103">Interface IEnumWiaItem2</span><span class="sxs-lookup"><span data-stu-id="3a9b4-103">IEnumWiaItem2 interface</span></span>

<span data-ttu-id="3a9b4-104">Usado por aplicativos para enumerar objetos [**IWiaItem2**](-wia-iwiaitem2.md) na pasta atual da árvore de itens.</span><span class="sxs-lookup"><span data-stu-id="3a9b4-104">Used by applications to enumerate [**IWiaItem2**](-wia-iwiaitem2.md) objects in the item tree's current folder.</span></span>

## <a name="members"></a><span data-ttu-id="3a9b4-105">Membros</span><span class="sxs-lookup"><span data-stu-id="3a9b4-105">Members</span></span>

<span data-ttu-id="3a9b4-106">A interface **IEnumWiaItem2** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3a9b4-106">The **IEnumWiaItem2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3a9b4-107">**IEnumWiaItem2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3a9b4-107">**IEnumWiaItem2** also has these types of members:</span></span>

-   [<span data-ttu-id="3a9b4-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="3a9b4-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3a9b4-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="3a9b4-109">Methods</span></span>

<span data-ttu-id="3a9b4-110">A interface **IEnumWiaItem2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3a9b4-110">The **IEnumWiaItem2** interface has these methods.</span></span>



| <span data-ttu-id="3a9b4-111">Método</span><span class="sxs-lookup"><span data-stu-id="3a9b4-111">Method</span></span>                                          | <span data-ttu-id="3a9b4-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a9b4-112">Description</span></span>                                                                                                                    |
|:------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a9b4-113">**8i**</span><span class="sxs-lookup"><span data-stu-id="3a9b4-113">**Clone**</span></span>](-wia-ienumwiaitem2-clone.md)       | <span data-ttu-id="3a9b4-114">Cria uma instância adicional da interface **IEnumWiaItem2** e envia de volta um ponteiro para ela.</span><span class="sxs-lookup"><span data-stu-id="3a9b4-114">Creates an additional instance of the **IEnumWiaItem2** interface and sends back a pointer to it.</span></span> <br/>                  |
| [<span data-ttu-id="3a9b4-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="3a9b4-115">**GetCount**</span></span>](-wia-ienumwiaitem2-getcount.md) | <span data-ttu-id="3a9b4-116">Retorna o número de elementos armazenados por este enumerador.</span><span class="sxs-lookup"><span data-stu-id="3a9b4-116">Returns the number of elements stored by this enumerator.</span></span> <br/>                                                          |
| [<span data-ttu-id="3a9b4-117">**Avançar**</span><span class="sxs-lookup"><span data-stu-id="3a9b4-117">**Next**</span></span>](-wia-ienumwiaitem2-next.md)         | <span data-ttu-id="3a9b4-118">Preenche uma matriz de ponteiros para interfaces [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="3a9b4-118">Fills an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span><br/>                                       |
| [<span data-ttu-id="3a9b4-119">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="3a9b4-119">**Reset**</span></span>](-wia-ienumwiaitem2-reset.md)       | <span data-ttu-id="3a9b4-120">Redefine a referência de enumeração para o primeiro objeto [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="3a9b4-120">Resets the enumeration reference to the first [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span> <br/>                          |
| [<span data-ttu-id="3a9b4-121">**Ignorar**</span><span class="sxs-lookup"><span data-stu-id="3a9b4-121">**Skip**</span></span>](-wia-ienumwiaitem2-skip.md)         | <span data-ttu-id="3a9b4-122">Ignora o número especificado de itens durante uma enumeração de objetos [**IWiaItem2**](-wia-iwiaitem2.md) disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3a9b4-122">Skips the specified number of items during an enumeration of available [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3a9b4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a9b4-123">Requirements</span></span>



| <span data-ttu-id="3a9b4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a9b4-124">Requirement</span></span> | <span data-ttu-id="3a9b4-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3a9b4-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a9b4-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a9b4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3a9b4-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a9b4-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3a9b4-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a9b4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3a9b4-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3a9b4-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3a9b4-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a9b4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a9b4-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a9b4-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a9b4-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="3a9b4-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3a9b4-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3a9b4-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 
