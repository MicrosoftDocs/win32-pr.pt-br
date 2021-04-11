---
description: O NTFS Transacional (TxF) integra as transações no sistema de arquivos NTFS, o que torna mais fácil para os desenvolvedores e administradores de aplicativos lidar normalmente com erros e preservar a integridade dos dados.
ms.assetid: 52341315-0412-4a87-aca0-9adea7aae62f
title: Sobre o NTFS Transacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf8cd99dfb1ff18ef7da88d3b3c7b0a647417e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296377"
---
# <a name="about-transactional-ntfs"></a><span data-ttu-id="6310f-103">Sobre o NTFS Transacional</span><span class="sxs-lookup"><span data-stu-id="6310f-103">About Transactional NTFS</span></span>

<span data-ttu-id="6310f-104">\[A Microsoft recomenda enfaticamente que os desenvolvedores utilizem meios alternativos para atender às necessidades do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6310f-104">\[Microsoft strongly recommends developers utilize alternative means to achieve your application s needs.</span></span> <span data-ttu-id="6310f-105">Muitos cenários para os quais o TxF foi desenvolvido podem ser obtidos por meio de técnicas mais simples e mais prontamente disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6310f-105">Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques.</span></span> <span data-ttu-id="6310f-106">Além disso, o TxF pode não estar disponível em versões futuras do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6310f-106">Furthermore, TxF may not be available in future versions of Microsoft Windows.</span></span> <span data-ttu-id="6310f-107">Para obter mais informações e alternativas para o TxF, consulte [alternativas para usar o NTFS Transacional](deprecation-of-txf.md).\]</span><span class="sxs-lookup"><span data-stu-id="6310f-107">For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](deprecation-of-txf.md).\]</span></span>

<span data-ttu-id="6310f-108">O NTFS Transacional (TxF) integra as transações no sistema de arquivos NTFS, o que torna mais fácil para os desenvolvedores e administradores de aplicativos lidar normalmente com erros e preservar a integridade dos dados.</span><span class="sxs-lookup"><span data-stu-id="6310f-108">Transactional NTFS (TxF) integrates transactions into the NTFS file system, which makes it easier for application developers and administrators to gracefully handle errors and preserve data integrity.</span></span>

<span data-ttu-id="6310f-109">O TxF pode participar de transações distribuídas que o [Coordenador de transações distribuídas (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) coordena, que permite que você use o TxF para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6310f-109">TxF can participate in distributed transactions that the [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) coordinates, which allows you to use TxF for the following:</span></span>

-   <span data-ttu-id="6310f-110">Transações que abrangem vários repositórios de dados, por exemplo, uma única transação para operações de arquivo e SQL</span><span class="sxs-lookup"><span data-stu-id="6310f-110">Transactions that span multiple data stores, for example, a single transaction for file and SQL operations</span></span>
-   <span data-ttu-id="6310f-111">Transações que abrangem vários computadores, por exemplo, uma única transação para atualizações de arquivo em vários computadores</span><span class="sxs-lookup"><span data-stu-id="6310f-111">Transactions that span multiple computers, for example, a single transaction for file updates on multiple computers</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6310f-112">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6310f-112">In this section</span></span>



| <span data-ttu-id="6310f-113">Tópico</span><span class="sxs-lookup"><span data-stu-id="6310f-113">Topic</span></span>                                                                                                                 | <span data-ttu-id="6310f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="6310f-114">Description</span></span>                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6310f-115">Quando usar o NTFS Transacional</span><span class="sxs-lookup"><span data-stu-id="6310f-115">When to Use Transactional NTFS</span></span>](when-to-use-transactional-ntfs.md)<br/>                                       | <span data-ttu-id="6310f-116">Use o NTFS transacional para manter a integridade dos dados.</span><span class="sxs-lookup"><span data-stu-id="6310f-116">Use Transactional NTFS to maintain data integrity.</span></span><br/>                                                                        |
| [<span data-ttu-id="6310f-117">Implantando o NTFS Transacional</span><span class="sxs-lookup"><span data-stu-id="6310f-117">Deploying Transactional NTFS</span></span>](deploying-transactional-ntfs.md)<br/>                                           | <span data-ttu-id="6310f-118">Controle de cache em NTFS Transacional.</span><span class="sxs-lookup"><span data-stu-id="6310f-118">Caching control in Transactional NTFS.</span></span><br/>                                                                                    |
| [<span data-ttu-id="6310f-119">Como usar o NTFS Transacional</span><span class="sxs-lookup"><span data-stu-id="6310f-119">How to Use Transactional NTFS</span></span>](how-to-use-transactional-ntfs.md)<br/>                                         | <span data-ttu-id="6310f-120">Gerenciando identificadores de arquivo transacionais em NTFS Transacional.</span><span class="sxs-lookup"><span data-stu-id="6310f-120">Managing transacted file handles in Transactional NTFS.</span></span><br/>                                                                   |
| [<span data-ttu-id="6310f-121">Conceitos básicos do TxF</span><span class="sxs-lookup"><span data-stu-id="6310f-121">Basic TxF Concepts</span></span>](txf-basic-concepts.md)<br/>                                                               | <span data-ttu-id="6310f-122">Descreve a consistência de leitura confirmada, isolamento de confirmação de leitura e conceitos de bloqueio transacional em NTFS Transacional.</span><span class="sxs-lookup"><span data-stu-id="6310f-122">Describes read-committed consistency, read-committed isolation, and transactional locking concepts in Transactional NTFS.</span></span><br/> |
| [<span data-ttu-id="6310f-123">Considerações de programação para NTFS Transacional</span><span class="sxs-lookup"><span data-stu-id="6310f-123">Programming Considerations for Transactional NTFS</span></span>](programming-considerations-for-transacted-fileio-.md)<br/> | <span data-ttu-id="6310f-124">Descreve várias considerações de programação para NTFS Transacional.</span><span class="sxs-lookup"><span data-stu-id="6310f-124">Describes various programming considerations for Transactional NTFS.</span></span><br/>                                                      |
| [<span data-ttu-id="6310f-125">Considerações de desempenho para NTFS Transacional</span><span class="sxs-lookup"><span data-stu-id="6310f-125">Performance Considerations for Transactional NTFS</span></span>](performance-considerations-for-transactional-ntfs.md)<br/> | <span data-ttu-id="6310f-126">Recomendações para transações de sistema de arquivos ideais.</span><span class="sxs-lookup"><span data-stu-id="6310f-126">Recommendations for optimal file system transactions.</span></span><br/>                                                                     |



 

 

