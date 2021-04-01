---
title: Exemplos de alterações incompatíveis
description: Ao lidar com alterações incompatíveis, a norma de prática é a seguinte, uma vez que qualquer alteração pode ser incompatível retroativamente, a menos que seja muito bem compreendida.
ms.assetid: 5b893d79-b81d-4ede-8d49-71d85219c497
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9498e5c71c7ce9690da0969f234fbb9d094eca50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005673"
---
# <a name="examples-of-incompatible-changes"></a><span data-ttu-id="affd9-103">Exemplos de alterações incompatíveis</span><span class="sxs-lookup"><span data-stu-id="affd9-103">Examples of Incompatible Changes</span></span>

<span data-ttu-id="affd9-104">Ao lidar com alterações incompatíveis, a boa regra geral é a seguinte: qualquer alteração pode ser incompatível com versões anteriores, a menos que seja muito bem compreendida.</span><span class="sxs-lookup"><span data-stu-id="affd9-104">When dealing with incompatible changes, the unfortunate rule of thumb is as follows: any change can be backward incompatible, unless it is very well understood.</span></span> <span data-ttu-id="affd9-105">Esta regra requer conhecimento das regras de NDR.</span><span class="sxs-lookup"><span data-stu-id="affd9-105">This rule requires knowledge of NDR rules.</span></span> <span data-ttu-id="affd9-106">Se você não souber qual é o NDR, não faça modificações.</span><span class="sxs-lookup"><span data-stu-id="affd9-106">If you do not know what the NDR is, do not make modifications.</span></span> <span data-ttu-id="affd9-107">Exemplos de alterações que normalmente resultam em uma violação de acesso no aplicativo ou uma exceção de dados stub inválidos \_ \_ \_ levantados pelo mecanismo de marshaling são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="affd9-107">Examples of changes that typically result in an access violation in the application, or a BAD\_STUB\_DATA\_EXCEPTION raised by the marshaling engine, are as follows:</span></span>

-   <span data-ttu-id="affd9-108">Adicionar um novo método no meio de métodos antigos.</span><span class="sxs-lookup"><span data-stu-id="affd9-108">Adding a new method in the middle of old methods.</span></span>
-   <span data-ttu-id="affd9-109">Adicionando ou removendo parâmetros de um método.</span><span class="sxs-lookup"><span data-stu-id="affd9-109">Adding or removing parameters from a method.</span></span>
-   <span data-ttu-id="affd9-110">Alterar um atributo, por exemplo, um atributo de ponteiro: alterando \[ ref \] para \[ Unique \] ou \[ PTR \] ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="affd9-110">Changing an attribute, for example a pointer attribute: changing \[ref\] to \[unique\] or \[ptr\] or vice versa.</span></span> <span data-ttu-id="affd9-111">Cada tipo de ponteiro tem uma representação de conexão diferente.</span><span class="sxs-lookup"><span data-stu-id="affd9-111">Each pointer type has a different wire representation.</span></span>
-   <span data-ttu-id="affd9-112">Alterar o tamanho dos dados: de curto para longo, de char para WCHAR \_ t (Unicode), adicionando um campo a uma estrutura, alterando o tamanho de uma matriz de tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="affd9-112">Changing the size of the data: from short to long, from char to wchar\_t (unicode), adding a field to a structure, changing the size of a fixed size array.</span></span>
-   <span data-ttu-id="affd9-113">Adicionar braços de União a uma União com uma cláusula padrão.</span><span class="sxs-lookup"><span data-stu-id="affd9-113">Adding union arms to a union with a default clause.</span></span>

<span data-ttu-id="affd9-114">Algumas alterações traiçoeiros ou incompatibilidades indesejadas entre um cliente e um servidor podem ocorrer da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="affd9-114">Some insidious changes or unintended mismatches between a client and a server may occur as follows:</span></span>

-   <span data-ttu-id="affd9-115">Modificar um membro de um tipo composto, como uma estrutura ou uma matriz.</span><span class="sxs-lookup"><span data-stu-id="affd9-115">Modifying a member of a compound type, like a structure or an array.</span></span> <span data-ttu-id="affd9-116">Por exemplo, se uma \_ ID do cliente for alterada de um integral para um GUID, uma estrutura de registro de cliente \_ com o \_ campo ID do cliente se tornará incompatível.</span><span class="sxs-lookup"><span data-stu-id="affd9-116">For example, if a CLIENT\_ID changes from an integral to a GUID, a CLIENT\_RECORD structure with the CLIENT\_ID field becomes incompatible.</span></span> <span data-ttu-id="affd9-117">Isso pode ser difícil de detectar se estiver em cascata por vários níveis de inserção para um tipo de parâmetro remoto real.</span><span class="sxs-lookup"><span data-stu-id="affd9-117">This may be difficult to detect if cascaded through several levels of embedding to an actual remote parameter type.</span></span>
-   <span data-ttu-id="affd9-118">Modificando um tipo importado.</span><span class="sxs-lookup"><span data-stu-id="affd9-118">Modifying an imported type.</span></span> <span data-ttu-id="affd9-119">O tipo pode ser proveniente de um componente diferente que não é remoto diretamente, portanto, a alteração foi considerada compatível.</span><span class="sxs-lookup"><span data-stu-id="affd9-119">The type may be coming from a different component that does not remote directly, hence the change was thought to be compatible.</span></span>
-   <span data-ttu-id="affd9-120">Usar \# ifdef em um arquivo IDL é uma má ideia para ifdef definições de tipo em um arquivo IDL — é um desastre aguardando a ocorrência.</span><span class="sxs-lookup"><span data-stu-id="affd9-120">Using \#ifdef in an IDL file is a bad idea to ifdef type definitions in an IDL file—it is disaster waiting to happen.</span></span> <span data-ttu-id="affd9-121">Inevitavelmente, devido à compilação ou a outros problemas, um cliente é compilado com um conjunto diferente de definições do que o servidor e acaba sendo incompatível.</span><span class="sxs-lookup"><span data-stu-id="affd9-121">Inevitably, due to build or other glitches, a client is compiled with a different set of defines than the server, and they end up being incompatible.</span></span>

 

 




