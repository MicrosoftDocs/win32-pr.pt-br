---
description: O NTFS Transacional (TxF) permite que as operações de arquivo em um volume do sistema de arquivos NTFS sejam executadas em uma transação.
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: NTFS Transacional (TxF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7553bfc7cae0b5389762527f0ac726c674a6a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501280"
---
# <a name="transactional-ntfs-txf"></a><span data-ttu-id="d6216-103">NTFS Transacional (TxF)</span><span class="sxs-lookup"><span data-stu-id="d6216-103">Transactional NTFS (TxF)</span></span>

<span data-ttu-id="d6216-104">\[A Microsoft recomenda enfaticamente que os desenvolvedores utilizem meios alternativos para atender às necessidades do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6216-104">\[Microsoft strongly recommends developers utilize alternative means to achieve your application s needs.</span></span> <span data-ttu-id="d6216-105">Muitos cenários para os quais o TxF foi desenvolvido podem ser obtidos por meio de técnicas mais simples e mais prontamente disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d6216-105">Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques.</span></span> <span data-ttu-id="d6216-106">Além disso, o TxF pode não estar disponível em versões futuras do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d6216-106">Furthermore, TxF may not be available in future versions of Microsoft Windows.</span></span> <span data-ttu-id="d6216-107">Para obter mais informações e alternativas para o TxF, consulte [alternativas para usar o NTFS Transacional](deprecation-of-txf.md).\]</span><span class="sxs-lookup"><span data-stu-id="d6216-107">For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](deprecation-of-txf.md).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="d6216-108">Finalidade</span><span class="sxs-lookup"><span data-stu-id="d6216-108">Purpose</span></span>

<span data-ttu-id="d6216-109">O NTFS Transacional (TxF) permite que as operações de arquivo em um volume do sistema de arquivos NTFS sejam executadas em uma transação.</span><span class="sxs-lookup"><span data-stu-id="d6216-109">Transactional NTFS (TxF) allows file operations on an NTFS file system volume to be performed in a transaction.</span></span> <span data-ttu-id="d6216-110">As transações de TxF aumentam a confiabilidade do aplicativo protegendo a integridade dos dados entre falhas e simplificam o desenvolvimento de aplicativos, reduzindo muito a quantidade de código de tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="d6216-110">TxF transactions increase application reliability by protecting data integrity across failures and simplify application development by greatly reducing the amount of error handling code.</span></span>

<span data-ttu-id="d6216-111">O TxF usa a estrutura de transação fornecida pelo KTM ( [kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal) ).</span><span class="sxs-lookup"><span data-stu-id="d6216-111">TxF uses the transaction framework provided by the [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal) (KTM).</span></span> <span data-ttu-id="d6216-112">Isso permite que as operações de arquivo TxF façam parte de uma transação que envolve outras fontes de dados, como SQL Server e registro transacionado (TxR).</span><span class="sxs-lookup"><span data-stu-id="d6216-112">This allows TxF file operations to be part of a transaction involving other data sources such as SQL Server and Transacted Registry (TxR).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="d6216-113">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="d6216-113">Where applicable</span></span>

<span data-ttu-id="d6216-114">Um aplicativo pode usar o TxF para preservar a integridade dos dados em disco causados por condições de erro inesperadas e ajudar a resolver cenários de usuário simultâneos do sistema de arquivos isolando suas alterações de outros enquanto as alterações estão sendo feitas.</span><span class="sxs-lookup"><span data-stu-id="d6216-114">An application can use TxF to preserve the integrity of data on disk caused by unexpected error conditions and help resolve concurrent file-system user scenarios by isolating your changes from others while the changes are being made.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="d6216-115">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="d6216-115">Developer audience</span></span>

<span data-ttu-id="d6216-116">Antes de usar o TxF, você deve ter um conhecimento funcional das transações usando o KTM ou o [Coordenador de transações distribuídas (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d6216-116">Before using TxF, you should have a working knowledge of transactions using either KTM or [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d6216-117">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="d6216-117">Run-time requirements</span></span>

<span data-ttu-id="d6216-118">O TxF está disponível a partir do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d6216-118">TxF is available starting with Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d6216-119">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d6216-119">In this section</span></span>



| <span data-ttu-id="d6216-120">Tópico</span><span class="sxs-lookup"><span data-stu-id="d6216-120">Topic</span></span>                                                    | <span data-ttu-id="d6216-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6216-121">Description</span></span>                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6216-122">Sobre</span><span class="sxs-lookup"><span data-stu-id="d6216-122">About</span></span>](about-transactional-ntfs.md)<br/>         | <span data-ttu-id="d6216-123">Informações gerais sobre o NTFS Transacional.</span><span class="sxs-lookup"><span data-stu-id="d6216-123">General information about Transactional NTFS.</span></span><br/>                                                   |
| [<span data-ttu-id="d6216-124">Referência</span><span class="sxs-lookup"><span data-stu-id="d6216-124">Reference</span></span>](transactional-ntfs-reference.md)<br/> | <span data-ttu-id="d6216-125">Documentação para as funções, estruturas de dados, enumerações e outros elementos de programação.</span><span class="sxs-lookup"><span data-stu-id="d6216-125">Documentation for the functions, data structures, enumerations, and other programming elements.</span></span><br/> |



 

 

