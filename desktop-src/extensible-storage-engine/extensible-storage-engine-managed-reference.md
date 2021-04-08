---
description: 'Saiba mais sobre: referência gerenciada do mecanismo de armazenamento extensível'
title: Referência gerenciada do mecanismo de armazenamento extensível
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: a1323d662cc7252ff6bda1eda53108751d3aedfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010676"
---
# <a name="extensible-storage-engine-managed-reference"></a><span data-ttu-id="889f5-103">Referência gerenciada do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="889f5-103">Extensible Storage Engine Managed Reference</span></span>

<span data-ttu-id="889f5-104">Encontre informações de referência para a biblioteca ManagedESENT.</span><span class="sxs-lookup"><span data-stu-id="889f5-104">Find reference information for the ManagedESENT library.</span></span> <span data-ttu-id="889f5-105">A biblioteca ManagedESENT fornece acesso gerenciado a ESENT, o mecanismo de banco de dados incorporável que é nativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="889f5-105">The ManagedESENT library provides managed access to ESENT, the embeddable database engine that is native to Windows.</span></span>


<span data-ttu-id="889f5-106">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="889f5-106">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="889f5-107">**Neste artigo**</span><span class="sxs-lookup"><span data-stu-id="889f5-107">**In this article**</span></span>  
<span data-ttu-id="889f5-108">Como a biblioteca ManagedESENT é diferente de ESENT?</span><span class="sxs-lookup"><span data-stu-id="889f5-108">How is the ManagedESENT library different than ESENT?</span></span>  
<span data-ttu-id="889f5-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="889f5-109">Requirements</span></span>  
<span data-ttu-id="889f5-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="889f5-110">In this section</span></span>  

## <a name="how-is-the-managedesent-library-different-than-esent"></a><span data-ttu-id="889f5-111">Como a biblioteca ManagedESENT é diferente de ESENT?</span><span class="sxs-lookup"><span data-stu-id="889f5-111">How is the ManagedESENT library different than ESENT?</span></span>

<span data-ttu-id="889f5-112">O ESENT é um mecanismo de banco de dados transacional e incorporável que permite criar aplicativos personalizados que precisam de armazenamento de dados confiável, de alto desempenho e de baixa sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="889f5-112">ESENT is an embeddable, transactional database engine that allows you to create custom applications that need reliable, high-performance, low-overhead storage of data.</span></span> <span data-ttu-id="889f5-113">O mecanismo ESENT pode ajudar com as necessidades de dados que variam de algo tão simples quanto uma tabela de hash muito grande para armazenar na memória, para algo mais complexo, como um aplicativo com tabelas, colunas e índices.</span><span class="sxs-lookup"><span data-stu-id="889f5-113">The ESENT engine can help with data needs that range from something as simple as a hash table that is too large to store in memory, to something more complex, such as an application with tables, columns, and indexes.</span></span> <span data-ttu-id="889f5-114">Para criar um aplicativo com o ESENT, use o esent.dll DLL que faz parte do sistema operacional Windows e escreva seu código com C/C++.</span><span class="sxs-lookup"><span data-stu-id="889f5-114">To create an application with ESENT, you use the esent.dll DLL that is part of the Windows operating system and write your code with C/C++.</span></span> <span data-ttu-id="889f5-115">Para obter mais informações sobre o ESENT, consulte [referência do mecanismo de armazenamento extensível](./extensible-storage-engine-reference.md).</span><span class="sxs-lookup"><span data-stu-id="889f5-115">For more information about ESENT, see [Extensible Storage Engine Reference](./extensible-storage-engine-reference.md).</span></span>

<span data-ttu-id="889f5-116">O ManagedESENT é criado com base em esent.dll, que faz parte do Windows, portanto, não há binários adicionais não gerenciados para baixar e instalar.</span><span class="sxs-lookup"><span data-stu-id="889f5-116">ManagedESENT is built on top of esent.dll, which is part of Windows, so there are no extra unmanaged binaries to download and install.</span></span> <span data-ttu-id="889f5-117">Com a biblioteca ManagedESENT, você pode criar seu aplicativo usando uma linguagem gerenciada como C \# em vez de c/C++.</span><span class="sxs-lookup"><span data-stu-id="889f5-117">With the ManagedESENT library, you can create your application by using a managed language such as C\# instead of C/C++.</span></span> <span data-ttu-id="889f5-118">A biblioteca usa o mesmo tipo e nomes de membros para expor a API ESE, portanto, se você já estiver familiarizado com a estrutura dessa API, poderá fazer a transição facilmente para essa biblioteca gerenciada.</span><span class="sxs-lookup"><span data-stu-id="889f5-118">The library uses the same type and member names to expose the ESE API, so if you are already familiar with the structure of this API, you can easily transition to this managed library.</span></span>

## <a name="requirements"></a><span data-ttu-id="889f5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="889f5-119">Requirements</span></span>

<span data-ttu-id="889f5-120">Essa biblioteca gerenciada requer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="889f5-120">This managed library requires the following:</span></span>

  - <span data-ttu-id="889f5-121">Um computador executando uma versão do Windows a partir do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="889f5-121">A computer running a version of Windows starting with Windows Vista</span></span>

  - <span data-ttu-id="889f5-122">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="889f5-122">Visual Studio 2012</span></span>

  - <span data-ttu-id="889f5-123">O .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="889f5-123">The .NET Framework 4.5</span></span>

## <a name="in-this-section"></a><span data-ttu-id="889f5-124">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="889f5-124">In this section</span></span>

  - [<span data-ttu-id="889f5-125">Microsoft. ISAM. ESENT</span><span class="sxs-lookup"><span data-stu-id="889f5-125">Microsoft.Isam.Esent</span></span>](./microsoft.isam.esent-namespace.md)

  - [<span data-ttu-id="889f5-126">Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="889f5-126">Microsoft.Isam.Esent.Interop</span></span>](./microsoft.isam.esent.interop-namespace.md)

  - [<span data-ttu-id="889f5-127">Microsoft. ISAM. ESENT. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="889f5-127">Microsoft.Isam.Esent.Interop.Server2003</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [<span data-ttu-id="889f5-128">Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="889f5-128">Microsoft.Isam.Esent.Interop.Vista</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

  - [<span data-ttu-id="889f5-129">Microsoft. ISAM. ESENT. Interop. Windows7</span><span class="sxs-lookup"><span data-stu-id="889f5-129">Microsoft.Isam.Esent.Interop.Windows7</span></span>](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [<span data-ttu-id="889f5-130">Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="889f5-130">Microsoft.Isam.Esent.Interop.Windows8</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
