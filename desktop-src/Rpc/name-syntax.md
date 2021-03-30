---
title: Sintaxe do nome
description: RPC (chamada de procedimento remoto) e sintaxe de nome.
ms.assetid: eb370106-bd88-4c21-b287-7b2b174185d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d024130a5b8a873c6bfbb2194542344953625d5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916455"
---
# <a name="name-syntax"></a><span data-ttu-id="ccc65-103">Sintaxe do nome</span><span class="sxs-lookup"><span data-stu-id="ccc65-103">Name Syntax</span></span>

<span data-ttu-id="ccc65-104">O Microsoft RPC aceita nomes que estão em conformidade com a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="ccc65-104">Microsoft RPC accepts names that conform to the following syntax:</span></span>

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a><span data-ttu-id="ccc65-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccc65-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccc65-106"><span id="name"></span><span id="NAME"></span>nomes</span><span class="sxs-lookup"><span data-stu-id="ccc65-106"><span id="name"></span><span id="NAME"></span>name</span></span>
</dt> <dd>

<span data-ttu-id="ccc65-107">Especifica um identificador que pode conter qualquer caractere, exceto o caractere de delimitação de barra (/).</span><span class="sxs-lookup"><span data-stu-id="ccc65-107">Specifies an identifier that can contain any character except the delimiting slash (/) character.</span></span>

</dd> <dt>

<span data-ttu-id="ccc65-108"><span id="domainname"></span><span id="DOMAINNAME"></span>DomainName</span><span class="sxs-lookup"><span data-stu-id="ccc65-108"><span id="domainname"></span><span id="DOMAINNAME"></span>domainname</span></span>
</dt> <dd>

<span data-ttu-id="ccc65-109">Especifica o nome do domínio.</span><span class="sxs-lookup"><span data-stu-id="ccc65-109">Specifies the name of the domain.</span></span>

</dd> </dl>

<span data-ttu-id="ccc65-110">Um parâmetro que seleciona o tipo de sintaxe de nome e a cadeia de caracteres que especifica o nome é fornecido para muitas das funções de RPC da interface de serviço de nome (NSI).</span><span class="sxs-lookup"><span data-stu-id="ccc65-110">A parameter that selects the name-syntax type and the string that specifies the name are supplied to many of the name service interface (NSI) RPC functions.</span></span>

<span data-ttu-id="ccc65-111">Somente um nome-tipo de sintaxe é suportado pelo Microsoft RPC, conforme especificado pela sintaxe constante \_ RPC \_ C \_ ns \_ DCE.</span><span class="sxs-lookup"><span data-stu-id="ccc65-111">Only one name-syntax type is supported by Microsoft RPC, as specified by the constant RPC\_C\_NS\_SYNTAX\_DCE.</span></span> <span data-ttu-id="ccc65-112">Essa constante é definida no arquivo de cabeçalho RPCNSI. H.</span><span class="sxs-lookup"><span data-stu-id="ccc65-112">This constant is defined in the header file RPCNSI.H.</span></span>

<span data-ttu-id="ccc65-113">A sintaxe de nome especificada pela \_ sintaxe RPC C \_ ns \_ \_ é uma extensão da sintaxe do nome do uso do \_ serviço de diretório de célula (CDs) do DCE.</span><span class="sxs-lookup"><span data-stu-id="ccc65-113">The name syntax specified by RPC\_C\_NS\_SYNTAX\_DCE is an extension of the OSF\_DCE Cell Directory Service (CDS) name syntax.</span></span> <span data-ttu-id="ccc65-114">A capacidade de especificar um nome de domínio representa uma extensão para essa sintaxe.</span><span class="sxs-lookup"><span data-stu-id="ccc65-114">The ability to specify a domain name represents an extension to that syntax.</span></span> <span data-ttu-id="ccc65-115">Não há nenhum limite absoluto para o número de nomes que podem ser separados por caracteres de barra, desde que a cadeia de caracteres geral tenha menos de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ccc65-115">There is no absolute limit on the number of names that can be separated by slash characters as long as the overall string is less than 256 characters.</span></span>

<span data-ttu-id="ccc65-116">As barras permitem que você especifique uma estrutura lógica para o nome, mas elas não correspondem a uma estrutura lógica nos próprios objetos.</span><span class="sxs-lookup"><span data-stu-id="ccc65-116">The slashes allow you to specify a logical structure to the name, but they do not correspond to a logical structure in the objects themselves.</span></span>

 

 




