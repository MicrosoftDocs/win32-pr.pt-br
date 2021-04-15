---
title: Referência de plug-in
description: Funções de adaptador, funções de wrapper e estruturas para criar adaptadores de plug-ins personalizados de três tipos de mecanismo, sensor e armazenamento.
ms.assetid: 1886c389-b914-4b2d-ab7e-3e163782673d
keywords:
- API de Windows Biometric Framework de API de Windows Biometric Framework, referência de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc764be98f6417d211effe1c182279d54c95d234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453711"
---
# <a name="plug-in-reference"></a><span data-ttu-id="b9194-104">Referência de plug-in</span><span class="sxs-lookup"><span data-stu-id="b9194-104">Plug-in Reference</span></span>

<span data-ttu-id="b9194-105">Os dispositivos biométricos são fabricados em uma ampla variedade de tipos e configurações.</span><span class="sxs-lookup"><span data-stu-id="b9194-105">Biometric devices are manufactured in a wide variety of types and configurations.</span></span> <span data-ttu-id="b9194-106">A Windows Biometric Framework incorpora uma arquitetura extensível que permite que você lide com essa variedade criando plug-ins personalizados. No centro dessa arquitetura, há um objeto de software chamado unidade biométrica.</span><span class="sxs-lookup"><span data-stu-id="b9194-106">The Windows Biometric Framework incorporates an extensible architecture that enables you to deal with this variety by creating custom plug-ins. At the center of this architecture is a software object called a biometric unit.</span></span> <span data-ttu-id="b9194-107">Você pode considerar uma unidade biométrica como uma abstração que representa um dispositivo biométrico para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="b9194-107">You can think of a biometric unit as an abstraction that represents a biometric device to the Framework.</span></span> <span data-ttu-id="b9194-108">Componentes de software de plug-in chamados adaptadores conectam a unidade biométrica ao hardware associado.</span><span class="sxs-lookup"><span data-stu-id="b9194-108">Plug-in software components called adapters connect the biometric unit to the associated hardware.</span></span> <span data-ttu-id="b9194-109">Há três tipos de adaptadores que você pode criar.</span><span class="sxs-lookup"><span data-stu-id="b9194-109">There are three types of adapters that you can create.</span></span> <span data-ttu-id="b9194-110">Um adaptador de mecanismo gera modelos biométricos de amostras capturadas, corresponde a amostras a modelos existentes e modelos de índices.</span><span class="sxs-lookup"><span data-stu-id="b9194-110">An engine adapter generates biometric templates from captured samples, matches samples to existing templates, and indexes templates.</span></span> <span data-ttu-id="b9194-111">Um adaptador de sensor encapsula um dispositivo biométrico e fornece uma interface padrão para configurar o sensor, capturar amostras e controlar o fluxo de dados biométricos para o mecanismo de processamento.</span><span class="sxs-lookup"><span data-stu-id="b9194-111">A sensor adapter wraps a biometric device and provides a standard interface for configuring the sensor, capturing samples, and controlling the flow of biometric data to the processing engine.</span></span> <span data-ttu-id="b9194-112">Um adaptador de armazenamento gerencia bancos de dados de modelo.</span><span class="sxs-lookup"><span data-stu-id="b9194-112">A storage adapter manages template databases.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b9194-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b9194-113">In this section</span></span>



| <span data-ttu-id="b9194-114">Tópico</span><span class="sxs-lookup"><span data-stu-id="b9194-114">Topic</span></span>                                                                 | <span data-ttu-id="b9194-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9194-115">Description</span></span>                                                                                                                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9194-116">Funções de plug-in</span><span class="sxs-lookup"><span data-stu-id="b9194-116">Plug-in Functions</span></span>](plug-in-functions.md)<br/>                 | <span data-ttu-id="b9194-117">Funções que você pode usar para criar os plug-ins de adaptador que compõem uma unidade biométrica.</span><span class="sxs-lookup"><span data-stu-id="b9194-117">Functions you can use to create the adapter plug-ins that make up a biometric unit.</span></span><br/>                                                                     |
| [<span data-ttu-id="b9194-118">Estruturas de plug-in</span><span class="sxs-lookup"><span data-stu-id="b9194-118">Plug-in Structures</span></span>](plug-in-structures.md)<br/>               | <span data-ttu-id="b9194-119">Estruturas para desenvolvimento de aplicativo cliente pela API de Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="b9194-119">Structures for client application development by the Windows Biometric Framework API.</span></span><br/>                                                                   |
| [<span data-ttu-id="b9194-120">Funções de wrapper de plug-in</span><span class="sxs-lookup"><span data-stu-id="b9194-120">Plug-in Wrapper Functions</span></span>](plug-in-wrapper-functions.md)<br/> | <span data-ttu-id="b9194-121">Funções de wrapper que permitem chamar uma função pública em qualquer adaptador anexado ao pipeline sem adquirir manualmente um ponteiro para o adaptador.</span><span class="sxs-lookup"><span data-stu-id="b9194-121">Wrapper functions that allow you to call a public function on any adapter attached to the pipeline without manually acquiring a pointer to the adapter.</span></span><br/> |



 

 

 





