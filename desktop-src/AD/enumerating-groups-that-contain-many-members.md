---
title: Enumerando grupos que contêm muitos membros
description: Os membros de um grupo são armazenados em um atributo com vários valores chamado membro.
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- Enumerando grupos que contêm muitos membros Active Directory
- grupos Active Directory, enumerando grupos com muitos membros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2d9a5c9abc6e77ac72672379789d1028f92c3f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084450"
---
# <a name="enumerating-groups-that-contain-many-members"></a><span data-ttu-id="27e06-105">Enumerando grupos que contêm muitos membros</span><span class="sxs-lookup"><span data-stu-id="27e06-105">Enumerating Groups That Contain Many Members</span></span>

<span data-ttu-id="27e06-106">Os membros de um grupo são armazenados em um atributo com vários valores chamado **membro**.</span><span class="sxs-lookup"><span data-stu-id="27e06-106">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="27e06-107">O atributo **Member** pode conter um grande número de valores.</span><span class="sxs-lookup"><span data-stu-id="27e06-107">The **member** attribute can contain a large number of values.</span></span> <span data-ttu-id="27e06-108">A enumeração de membros pode ser ineficiente quando o número de valores em um atributo com vários valores se torna grande.</span><span class="sxs-lookup"><span data-stu-id="27e06-108">Enumerating members can be inefficient when the number of values in a multi-valued attribute becomes large.</span></span> <span data-ttu-id="27e06-109">O servidor também limitará o número máximo de valores que podem ser recuperados em uma única consulta.</span><span class="sxs-lookup"><span data-stu-id="27e06-109">The server will also limit the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="27e06-110">Isso significa que, se um grupo pode ter mais membros do que pode ser fornecido pelo servidor, a única maneira de enumerar todos os membros é usar a recuperação incremental de dados, conhecida como *recuperação de intervalo*.</span><span class="sxs-lookup"><span data-stu-id="27e06-110">This means that if a group may have more members than can be supplied by the server, the only way to enumerate all members is to use incremental retrieval of data, known as *range retrieval*.</span></span>

<span data-ttu-id="27e06-111">A recuperação de intervalo envolve a solicitação de um número limitado de valores de atributo em uma única consulta.</span><span class="sxs-lookup"><span data-stu-id="27e06-111">Range retrieval involves requesting a limited number of attribute values in a single query.</span></span> <span data-ttu-id="27e06-112">O número de valores solicitados deve ser menor ou igual ao número máximo de valores com suporte pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="27e06-112">The number of values requested must be less than, or equal to, the maximum number of values supported by the server.</span></span> <span data-ttu-id="27e06-113">Para reduzir o número de vezes que a consulta deve entrar em contato com o servidor, o número de valores solicitados deve ser o mais próximo possível, para esse máximo.</span><span class="sxs-lookup"><span data-stu-id="27e06-113">To reduce the number of times the query must contact the server, the number of values requested should be as close, as possible, to this maximum.</span></span> <span data-ttu-id="27e06-114">Para permitir que um aplicativo funcione corretamente com todos os servidores, um número máximo de 1000 deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="27e06-114">To enable an application to work correctly with all servers, a maximum number of 1000 should be used.</span></span>

<span data-ttu-id="27e06-115">A versão do servidor que fornece os dados solicitados determina o número máximo de valores que podem ser recuperados em uma única consulta.</span><span class="sxs-lookup"><span data-stu-id="27e06-115">The version of the server that supplies the requested data determines the maximum number of values that can be retrieved in a single query.</span></span> <span data-ttu-id="27e06-116">A tabela a seguir lista a versão do servidor e o número máximo de valores que podem ser recuperados em uma única consulta.</span><span class="sxs-lookup"><span data-stu-id="27e06-116">The following table lists the server version and the maximum number of values that can be retrieved in a single query.</span></span>



| <span data-ttu-id="27e06-117">Versão do sistema operacional do servidor</span><span class="sxs-lookup"><span data-stu-id="27e06-117">Server operating system version</span></span> | <span data-ttu-id="27e06-118">Valores máximos recuperados</span><span class="sxs-lookup"><span data-stu-id="27e06-118">Maximum values retrieved</span></span> |
|---------------------------------|--------------------------|
| <span data-ttu-id="27e06-119">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="27e06-119">Windows 2000</span></span>                    | <span data-ttu-id="27e06-120">1000</span><span class="sxs-lookup"><span data-stu-id="27e06-120">1000</span></span>                     |
| <span data-ttu-id="27e06-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27e06-121">Windows Server 2003</span></span>             | <span data-ttu-id="27e06-122">1500</span><span class="sxs-lookup"><span data-stu-id="27e06-122">1500</span></span>                     |



 

<span data-ttu-id="27e06-123">Para obter mais informações sobre como recuperar intervalos de valores de atributo com ADSI, consulte [recuperação de intervalo de atributo](/windows/desktop/ADSI/attribute-range-retrieval).</span><span class="sxs-lookup"><span data-stu-id="27e06-123">For more information about retrieving ranges of attribute values with ADSI, see [Attribute Range Retrieval](/windows/desktop/ADSI/attribute-range-retrieval).</span></span>

<span data-ttu-id="27e06-124">Para obter mais informações sobre como recuperar intervalos de valores de atributo com [System. DirectoryServices](/dotnet/api/system.directoryservices), consulte [enumerando Membros em um grupo grande](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="27e06-124">For more information about retrieving ranges of attribute values with [System.DirectoryServices](/dotnet/api/system.directoryservices), see [Enumerating Members in a Large Group](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).</span></span>

 

 