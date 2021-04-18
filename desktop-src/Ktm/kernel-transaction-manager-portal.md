---
description: Implemente o NTFS Transacional (TxF) e o registro transacional (TxR). O TxF permite operações de sistema de arquivos transacionadas no NTFS. TxR permite operações de registro transacionadas. Coordenar operações de registro e sistema de arquivos com uma transação.
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: Gerenciador de transações do kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281050461163d5fd0cde64af79e70569d613888e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751215"
---
# <a name="kernel-transaction-manager"></a><span data-ttu-id="18fed-106">Gerenciador de transações do kernel</span><span class="sxs-lookup"><span data-stu-id="18fed-106">Kernel Transaction Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="18fed-107">Finalidade</span><span class="sxs-lookup"><span data-stu-id="18fed-107">Purpose</span></span>

<span data-ttu-id="18fed-108">O KTM (kernel Transaction Manager) permite o desenvolvimento de aplicativos que usam transações.</span><span class="sxs-lookup"><span data-stu-id="18fed-108">The Kernel Transaction Manager (KTM) enables the development of applications that use transactions.</span></span> <span data-ttu-id="18fed-109">O mecanismo de transação em si está dentro do kernel, mas as transações podem ser desenvolvidas para transações de modo kernel ou de usuário e dentro de um único host ou entre hosts distribuídos.</span><span class="sxs-lookup"><span data-stu-id="18fed-109">The transaction engine itself is within the kernel, but transactions can be developed for kernel- or user-mode transactions, and within a single host or among distributed hosts.</span></span>

<span data-ttu-id="18fed-110">O KTM é usado para implementar o NTFS Transacional (TxF) e o registro transacional (TxR).</span><span class="sxs-lookup"><span data-stu-id="18fed-110">The KTM is used to implement Transactional NTFS (TxF) and Transactional Registry (TxR).</span></span> <span data-ttu-id="18fed-111">O TxF permite operações de sistema de arquivos transacionadas no sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="18fed-111">TxF allows transacted file system operations within the NTFS file system.</span></span> <span data-ttu-id="18fed-112">TxR permite operações de registro transacionadas.</span><span class="sxs-lookup"><span data-stu-id="18fed-112">TxR allows transacted registry operations.</span></span> <span data-ttu-id="18fed-113">O KTM permite que os aplicativos cliente coordenem operações de registro e sistema de arquivos com uma transação.</span><span class="sxs-lookup"><span data-stu-id="18fed-113">KTM enables client applications to coordinate file system and registry operations with a transaction.</span></span>

<span data-ttu-id="18fed-114">Para desenvolver um aplicativo que coordena transações com recursos diferentes de TxF ou TxR, primeiro você deve desenvolver um serviço de reconhecimento de transações do Win32, também chamado de Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="18fed-114">To develop an application that coordinates transactions with resources other than TxF or TxR, you must first develop a Win32 transaction-aware service, also called a resource manager.</span></span>

<span data-ttu-id="18fed-115">Os aplicativos gerenciados e COM+ devem usar seus gerenciadores de transações nativas.</span><span class="sxs-lookup"><span data-stu-id="18fed-115">Managed and COM+ applications should use their native transaction managers.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="18fed-116">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="18fed-116">Where applicable</span></span>

<span data-ttu-id="18fed-117">O KTM pode ser usado com aplicativos e gerenciadores de recursos hospedados no Windows Vista ou no Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="18fed-117">KTM can be used with applications and resource managers hosted on Windows Vista or Windows Server 2008.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="18fed-118">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="18fed-118">Developer audience</span></span>

<span data-ttu-id="18fed-119">A API de KTM foi projetada para uso por programadores C e C++.</span><span class="sxs-lookup"><span data-stu-id="18fed-119">The KTM API is designed for use by C and C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="18fed-120">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="18fed-120">Run-time requirements</span></span>

<span data-ttu-id="18fed-121">O KTM tem suporte a partir do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="18fed-121">KTM is supported starting with Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="18fed-122">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="18fed-122">In this section</span></span>



| <span data-ttu-id="18fed-123">Tópico</span><span class="sxs-lookup"><span data-stu-id="18fed-123">Topic</span></span>                                     | <span data-ttu-id="18fed-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="18fed-124">Description</span></span>                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18fed-125">Sobre</span><span class="sxs-lookup"><span data-stu-id="18fed-125">About</span></span>](about-ktm.md)<br/>         | <span data-ttu-id="18fed-126">Informações gerais sobre transações e os recursos fornecidos pelo KTM.</span><span class="sxs-lookup"><span data-stu-id="18fed-126">General information about transactions and the capabilities provided by KTM.</span></span><br/>                           |
| [<span data-ttu-id="18fed-127">Referência</span><span class="sxs-lookup"><span data-stu-id="18fed-127">Reference</span></span>](ktm-reference.md)<br/> | <span data-ttu-id="18fed-128">Documentação para as funções, estruturas de dados, enumerações e outros elementos de programação de KTM.</span><span class="sxs-lookup"><span data-stu-id="18fed-128">Documentation for the functions, data structures, enumerations, and other programming elements of KTM.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="18fed-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="18fed-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18fed-130">Sistema de Arquivos de Log Comum</span><span class="sxs-lookup"><span data-stu-id="18fed-130">Common Log File System</span></span>](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[<span data-ttu-id="18fed-131">NTFS Transacional (TxF)</span><span class="sxs-lookup"><span data-stu-id="18fed-131">Transactional NTFS (TxF)</span></span>](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

<span data-ttu-id="18fed-132">[Coordenador de Transações Distribuídas](/previous-versions/windows/desktop/ms684146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18fed-132">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span></span>
</dt> </dl>

 

