---
title: Processamento de territórios e manipulação de atributos
description: O processamento de territórios, que também é conhecido como manipulação de atributos, refere-se à transformação do nome do usuário que está solicitando acesso.
ms.assetid: 52963eda-ea95-4307-8924-d4143bc1f53d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd630fd683342c45ab35161bf2c740ac7e8a6fa2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641416"
---
# <a name="realms-processing-and-attribute-manipulation"></a><span data-ttu-id="e7f34-103">Processamento de territórios e manipulação de atributos</span><span class="sxs-lookup"><span data-stu-id="e7f34-103">Realms Processing and Attribute Manipulation</span></span>

> [!Note]  
> <span data-ttu-id="e7f34-104">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e7f34-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="e7f34-105">O conteúdo deste tópico aplica-se ao IAS e ao NPS.</span><span class="sxs-lookup"><span data-stu-id="e7f34-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="e7f34-106">Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.</span><span class="sxs-lookup"><span data-stu-id="e7f34-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="e7f34-107">O processamento de territórios, que também é conhecido como manipulação de atributos, refere-se à transformação do nome do usuário que está solicitando acesso.</span><span class="sxs-lookup"><span data-stu-id="e7f34-107">Realms processing, which is also known as attribute manipulation, refers to transforming the name of the user requesting access.</span></span> <span data-ttu-id="e7f34-108">A ID de estação de chamada e a ID de estação chamada também podem ser manipuladas.</span><span class="sxs-lookup"><span data-stu-id="e7f34-108">The calling-station ID and called-station ID can also be manipulated.</span></span> <span data-ttu-id="e7f34-109">As regras de processamento de territórios são parte da coleção de atributos do perfil de proxy.</span><span class="sxs-lookup"><span data-stu-id="e7f34-109">The realms-processing rules are part of the Proxy profile attributes collection.</span></span>

<span data-ttu-id="e7f34-110">Para cada manipulação, você precisa criar dois atributos [de regra de manipulação](/windows/desktop/Nps/sdo-manipulation-rule) .</span><span class="sxs-lookup"><span data-stu-id="e7f34-110">For each manipulation, you need to create two [Manipulation-Rule](/windows/desktop/Nps/sdo-manipulation-rule) attributes.</span></span> <span data-ttu-id="e7f34-111">Cada um desses atributos é um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e7f34-111">Each of these attributes is a string value.</span></span> <span data-ttu-id="e7f34-112">A primeira regra contém uma expressão regular que representa o padrão a ser correspondido.</span><span class="sxs-lookup"><span data-stu-id="e7f34-112">The first rule contains a regular expression representing the pattern to match.</span></span> <span data-ttu-id="e7f34-113">A segunda regra contém uma expressão regular que representa o texto de substituição.</span><span class="sxs-lookup"><span data-stu-id="e7f34-113">The second rule contains a regular expression representing the replacement text.</span></span> <span data-ttu-id="e7f34-114">Você também deve criar um atributo [de destino Manipulation](/windows/desktop/Nps/sdo-manipulation-target) .</span><span class="sxs-lookup"><span data-stu-id="e7f34-114">You must also create a [Manipulation-Target](/windows/desktop/Nps/sdo-manipulation-target) attribute.</span></span> <span data-ttu-id="e7f34-115">Esse atributo é uma enumeração que especifica qual parte das informações do usuário deve ser manipulada.</span><span class="sxs-lookup"><span data-stu-id="e7f34-115">This attribute is an enumeration that specifies which part of the user's information to manipulate.</span></span>

<span data-ttu-id="e7f34-116">A ordem na qual os atributos são criados é importante.</span><span class="sxs-lookup"><span data-stu-id="e7f34-116">The order in which the attributes are created is important.</span></span> <span data-ttu-id="e7f34-117">O NPS processa os atributos na ordem em que foram criados.</span><span class="sxs-lookup"><span data-stu-id="e7f34-117">NPS processes the attributes in the order in which they were created.</span></span>

<span data-ttu-id="e7f34-118">A tabela a seguir mostra um exemplo de um conjunto de atributos de manipulação.</span><span class="sxs-lookup"><span data-stu-id="e7f34-118">The following table shows an example of a set of manipulation attributes.</span></span>



| <span data-ttu-id="e7f34-119">Nome</span><span class="sxs-lookup"><span data-stu-id="e7f34-119">Name</span></span>                 | <span data-ttu-id="e7f34-120">Type</span><span class="sxs-lookup"><span data-stu-id="e7f34-120">Type</span></span>         | <span data-ttu-id="e7f34-121">Valor da cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="e7f34-121">String Value</span></span>     |
|----------------------|--------------|------------------|
| <span data-ttu-id="e7f34-122">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="e7f34-122">msManipulationRule</span></span>   | <span data-ttu-id="e7f34-123">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7f34-123">**VT\_BSTR**</span></span> | <span data-ttu-id="e7f34-124">"@company.com"</span><span class="sxs-lookup"><span data-stu-id="e7f34-124">"@company.com"</span></span>   |
| <span data-ttu-id="e7f34-125">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="e7f34-125">msManipulationRule</span></span>   | <span data-ttu-id="e7f34-126">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7f34-126">**VT\_BSTR**</span></span> | <span data-ttu-id="e7f34-127">"@microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="e7f34-127">"@microsoft.com"</span></span> |
| <span data-ttu-id="e7f34-128">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="e7f34-128">msManipulationRule</span></span>   | <span data-ttu-id="e7f34-129">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7f34-129">**VT\_BSTR**</span></span> | <span data-ttu-id="e7f34-130">"^.+@"</span><span class="sxs-lookup"><span data-stu-id="e7f34-130">"^.+@"</span></span>           |
| <span data-ttu-id="e7f34-131">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="e7f34-131">msManipulationRule</span></span>   | <span data-ttu-id="e7f34-132">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="e7f34-132">**VT\_BSTR**</span></span> | <span data-ttu-id="e7f34-133">"guest@"</span><span class="sxs-lookup"><span data-stu-id="e7f34-133">"guest@"</span></span>         |
| <span data-ttu-id="e7f34-134">msManipulationTarget</span><span class="sxs-lookup"><span data-stu-id="e7f34-134">msManipulationTarget</span></span> | <span data-ttu-id="e7f34-135">**\_I4 VT**</span><span class="sxs-lookup"><span data-stu-id="e7f34-135">**VT\_I4**</span></span>   | <span data-ttu-id="e7f34-136">"1"</span><span class="sxs-lookup"><span data-stu-id="e7f34-136">"1"</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="e7f34-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7f34-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7f34-138">Hierarquia de modelo de objeto</span><span class="sxs-lookup"><span data-stu-id="e7f34-138">Object Model Hierarchy</span></span>](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[<span data-ttu-id="e7f34-139">Atributos com suporte a SDO</span><span class="sxs-lookup"><span data-stu-id="e7f34-139">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> <dt>

[<span data-ttu-id="e7f34-140">Criando uma política de solicitação de conexão</span><span class="sxs-lookup"><span data-stu-id="e7f34-140">Creating a Connection Request Policy</span></span>](/windows/desktop/Nps/sdo-creating-a-connection-request-policy)
</dt> <dt>

[<span data-ttu-id="e7f34-141">**ISdoCollection**</span><span class="sxs-lookup"><span data-stu-id="e7f34-141">**ISdoCollection**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[<span data-ttu-id="e7f34-142">**ISdoDictionaryOld**</span><span class="sxs-lookup"><span data-stu-id="e7f34-142">**ISdoDictionaryOld**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold)
</dt> <dt>

[<span data-ttu-id="e7f34-143">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="e7f34-143">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 