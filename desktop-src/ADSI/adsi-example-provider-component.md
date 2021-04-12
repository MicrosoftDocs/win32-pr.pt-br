---
title: Componente do provedor de exemplo ADSI
description: Active Directory escritores de provedor de interfaces de serviço encontrarão esta seção de interesse específico, pois ela descreve o componente de exemplo de provedor ADSI em detalhes.
ms.assetid: 1ca73817-7a21-4a39-b496-fc82db26ea4e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7bf960021df9a3b26f252584cad2ff3374254a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291802"
---
# <a name="adsi-example-provider-component"></a><span data-ttu-id="5e5db-103">Componente do provedor de exemplo ADSI</span><span class="sxs-lookup"><span data-stu-id="5e5db-103">ADSI Example Provider Component</span></span>

<span data-ttu-id="5e5db-104">Active Directory escritores de provedor de interfaces de serviço encontrarão esta seção de interesse específico, pois ela descreve o componente de exemplo de provedor ADSI em detalhes.</span><span class="sxs-lookup"><span data-stu-id="5e5db-104">Active Directory Service Interfaces provider writers will find this section of particular interest, because it describes the ADSI example provider component in depth.</span></span> <span data-ttu-id="5e5db-105">Os gravadores do provedor ADSI podem instalar o provedor de exemplo e usar a estrutura de código como uma base para criar sua própria implementação.</span><span class="sxs-lookup"><span data-stu-id="5e5db-105">ADSI provider writers can install the example provider and use the code framework as a basis to create their own implementation.</span></span> <span data-ttu-id="5e5db-106">Os seguintes tópicos são abordados:</span><span class="sxs-lookup"><span data-stu-id="5e5db-106">The following topics are discussed:</span></span>

<span data-ttu-id="5e5db-107">[A instalação do componente de provedor de exemplo](installing-the-example-provider-component.md) descreve como instalar o provedor de exemplo ADSI e seu diretório fictício.</span><span class="sxs-lookup"><span data-stu-id="5e5db-107">[Installing the Example Provider Component](installing-the-example-provider-component.md) describes how to install the ADSI sample provider and its mock directory.</span></span> <span data-ttu-id="5e5db-108">Esta seção inclui uma lista das configurações do registro.</span><span class="sxs-lookup"><span data-stu-id="5e5db-108">This section includes a list of the registry settings.</span></span>

<span data-ttu-id="5e5db-109">[Definição de diretório](directory-definition.md) descreve as entradas de diretório definidas pelo componente de provedor de exemplo.</span><span class="sxs-lookup"><span data-stu-id="5e5db-109">[Directory Definition](directory-definition.md) describes the directory entries defined by the example provider component.</span></span>

<span data-ttu-id="5e5db-110">O [Gerenciamento de esquema](schema-management.md) descreve como cada elemento no exemplo de serviço de diretório de componente do provedor pode ser representado por um tipo específico de Active Directory objeto.</span><span class="sxs-lookup"><span data-stu-id="5e5db-110">[Schema Management](schema-management.md) describes how each element in the example provider component directory service can be represented by a specific type of Active Directory object.</span></span>

<span data-ttu-id="5e5db-111">A [associação a um objeto Active Directory](binding-to-an-active-directory-object.md) descreve como, dada uma cadeia de caracteres ADsPath, o componente de provedor de exemplo identifica esse elemento, cria o tipo apropriado de objeto Active Directory para ele e recupera o tipo solicitado de ponteiro de interface nesse objeto para que ele passe de volta para o software cliente do ADS.</span><span class="sxs-lookup"><span data-stu-id="5e5db-111">[Binding to an Active Directory Object](binding-to-an-active-directory-object.md) describes how, given an ADsPath string, the example provider component identifies that element, creates the appropriate type of Active Directory object for it, and retrieves the requested type of interface pointer on that object to pass back to the ADs client software.</span></span>

<span data-ttu-id="5e5db-112">[Objetos de enumerador](enumerator-objects.md) lista os tipos específicos de enumerações fornecidos pelo componente de provedor de exemplo e em que código-fonte as implementações podem ser encontradas.</span><span class="sxs-lookup"><span data-stu-id="5e5db-112">[Enumerator Objects](enumerator-objects.md) lists the specific types of enumerations supplied by the example provider component and in which source code the implementations can be found.</span></span>

<span data-ttu-id="5e5db-113">[Visão geral de código](code-overview.md) fornece uma descrição em nível de tarefa de cada parte do componente de provedor de exemplo.</span><span class="sxs-lookup"><span data-stu-id="5e5db-113">[Code Overview](code-overview.md) provides a task-level description of each part of the example provider component.</span></span>

<span data-ttu-id="5e5db-114">[Detalhes do código](code-details.md) lista os módulos de software e seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5e5db-114">[Code Details](code-details.md) lists the software modules and their contents.</span></span>

 

 




