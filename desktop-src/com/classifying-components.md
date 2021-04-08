---
title: Classificando componentes
description: Classificando componentes
ms.assetid: 4d805532-96c9-400d-b78a-f8d0d9bdbf83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ea1547c219a44262fdeaf7edb02f65c7a3aac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822868"
---
# <a name="classifying-components"></a><span data-ttu-id="62be7-103">Classificando componentes</span><span class="sxs-lookup"><span data-stu-id="62be7-103">Classifying Components</span></span>

<span data-ttu-id="62be7-104">Embora um cliente possa navegar pela lista de CLSIDs no registro e selecionar um componente a ser usado, carregar cada componente no registro e consultá-lo para suas interfaces com suporte é muito demorado.</span><span class="sxs-lookup"><span data-stu-id="62be7-104">While a client is able to browse through the list of CLSIDs in the registry and select a component to use, loading each component in the registry and querying it for its supported interfaces is very time-consuming.</span></span> <span data-ttu-id="62be7-105">Para determinar se um componente dá suporte às interfaces necessárias antes de criar uma instância do componente, um método para classificar os componentes em categorias foi desenvolvido.</span><span class="sxs-lookup"><span data-stu-id="62be7-105">To determine whether a component supports the interfaces required before creating an instance of the component, a method to classify components into categories was developed.</span></span>

<span data-ttu-id="62be7-106">Uma categoria de componente é um conjunto de interfaces que foram atribuídas a um GUID chamado CATID.</span><span class="sxs-lookup"><span data-stu-id="62be7-106">A component category is a set of interfaces that have been assigned a GUID named CATID.</span></span> <span data-ttu-id="62be7-107">Os componentes que implementam todas as interfaces em uma categoria de componente se registram como membros dessa categoria de componente.</span><span class="sxs-lookup"><span data-stu-id="62be7-107">Components that implement all of the interfaces in a component category register themselves as members of that component category.</span></span> <span data-ttu-id="62be7-108">Os componentes que pertencem a uma determinada categoria de componente podem ser selecionados no registro.</span><span class="sxs-lookup"><span data-stu-id="62be7-108">Components that belong to a certain component category can then be selected from the registry.</span></span> <span data-ttu-id="62be7-109">Ao se registrar como um membro de uma categoria de componente, o componente está garantindo que ele dê suporte a todas as interfaces de membro na categoria de componente.</span><span class="sxs-lookup"><span data-stu-id="62be7-109">By registering itself as a member of a component category, the component is guaranteeing that it supports all of the member interfaces in the component category.</span></span>

<span data-ttu-id="62be7-110">Um componente pode ser membro de muitas categorias.</span><span class="sxs-lookup"><span data-stu-id="62be7-110">A component can be a member of many categories.</span></span> <span data-ttu-id="62be7-111">Ele não está limitado a interfaces de suporte em uma categoria de componente.</span><span class="sxs-lookup"><span data-stu-id="62be7-111">It is not limited to supporting interfaces in a component category.</span></span> <span data-ttu-id="62be7-112">Ele pode dar suporte a qualquer interface, além daquelas em uma categoria de componente.</span><span class="sxs-lookup"><span data-stu-id="62be7-112">It can support any interface, in addition to those in a component category.</span></span>

<span data-ttu-id="62be7-113">Ao contrário do registro padrão de componentes, nos quais os desenvolvedores devem escrever código que registra objetos manualmente, as categorias de componentes automatizam grande parte desse trabalho.</span><span class="sxs-lookup"><span data-stu-id="62be7-113">In contrast to the standard registration of components, in which developers must write code that manually registers objects, component categories automates much of this work.</span></span> <span data-ttu-id="62be7-114">Os seis métodos da interface [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) definem categorias de componentes e registram objetos que as implementam ou exigem.</span><span class="sxs-lookup"><span data-stu-id="62be7-114">The six methods of the [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) interface define component categories and register objects that implement or require them.</span></span> <span data-ttu-id="62be7-115">O objeto do [Gerenciador de categorias de componentes](the-component-categories-manager.md) implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="62be7-115">The [Component Categories Manager](the-component-categories-manager.md) object implements this interface.</span></span> <span data-ttu-id="62be7-116">Consulte **ICatRegister** e [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) para obter informações adicionais sobre como usar categorias de componentes.</span><span class="sxs-lookup"><span data-stu-id="62be7-116">See **ICatRegister** and [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) for additional information on using component categories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62be7-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62be7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62be7-118">Registrando aplicativos COM</span><span class="sxs-lookup"><span data-stu-id="62be7-118">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 




