---
title: AccNameLengthTooLong
description: AccNameLengthTooLong
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1efcb2b7d13c83a5972cb6e100d70500f9c5ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811590"
---
# <a name="accnamelengthtoolong"></a><span data-ttu-id="62f49-103">AccNameLengthTooLong</span><span class="sxs-lookup"><span data-stu-id="62f49-103">AccNameLengthTooLong</span></span>

## <a name="text"></a><span data-ttu-id="62f49-104">Texto</span><span class="sxs-lookup"><span data-stu-id="62f49-104">Text</span></span>

<span data-ttu-id="62f49-105">O nome do elemento não deve retornar uma cadeia de caracteres com mais de um {0} caractere</span><span class="sxs-lookup"><span data-stu-id="62f49-105">Element's name should not return a string longer than {0} character</span></span>

## <a name="type"></a><span data-ttu-id="62f49-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="62f49-106">Type</span></span>

<span data-ttu-id="62f49-107">Erro</span><span class="sxs-lookup"><span data-stu-id="62f49-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="62f49-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="62f49-108">Description</span></span>

<span data-ttu-id="62f49-109">O nome de um elemento contém muitos caracteres.</span><span class="sxs-lookup"><span data-stu-id="62f49-109">The name of an element contains too many characters.</span></span> <span data-ttu-id="62f49-110">Por exemplo, o método [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) usado para recuperar o nome MSAA de um elemento retorna uma cadeia de caracteres maior que o limite de 32000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="62f49-110">For example, the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method used to retrieve the MSAA name of an element returns a string greater than the limit of 32000 characters.</span></span>

<span data-ttu-id="62f49-111">Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque um elemento pode ter um nome não-pronunciado e não intuitivo.</span><span class="sxs-lookup"><span data-stu-id="62f49-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="62f49-112">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="62f49-112">Possible causes</span></span>

<span data-ttu-id="62f49-113">O elemento ou seu pai tem um nome ou rótulo atribuído incorretamente.</span><span class="sxs-lookup"><span data-stu-id="62f49-113">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62f49-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62f49-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62f49-115">**IAccessible:: obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="62f49-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="62f49-116">Propriedade Name</span><span class="sxs-lookup"><span data-stu-id="62f49-116">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




