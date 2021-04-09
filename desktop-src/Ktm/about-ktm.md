---
description: O KTM (kernel Transaction Manager) é um serviço de gerenciamento de transações. Ele torna as transações disponíveis como objetos kernel e fornece serviços de gerenciamento de transações para componentes do sistema, como o NTFS Transacional (TxF).
ms.assetid: 85a79698-a1ae-45a4-805e-25175034fa65
title: Sobre o KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1c477c7f9ae54b86fcee03435310416b38ea8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011728"
---
# <a name="about-ktm"></a><span data-ttu-id="a9436-104">Sobre o KTM</span><span class="sxs-lookup"><span data-stu-id="a9436-104">About KTM</span></span>

<span data-ttu-id="a9436-105">O KTM (kernel Transaction Manager) é um serviço de gerenciamento de transações.</span><span class="sxs-lookup"><span data-stu-id="a9436-105">Kernel Transaction Manager (KTM) is a transaction management service.</span></span> <span data-ttu-id="a9436-106">Ele torna as transações disponíveis como objetos kernel e fornece serviços de gerenciamento de transações para componentes do sistema, como o [NTFS Transacional](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF).</span><span class="sxs-lookup"><span data-stu-id="a9436-106">It makes transactions available as kernel objects and provides transaction management services to system components such as [Transactional NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF).</span></span>

<span data-ttu-id="a9436-107">Os tópicos a seguir descrevem os usos e os recursos do KTM:</span><span class="sxs-lookup"><span data-stu-id="a9436-107">The following topics describe the uses and features of KTM:</span></span>

-   [<span data-ttu-id="a9436-108">O que é uma transação?</span><span class="sxs-lookup"><span data-stu-id="a9436-108">What is a Transaction?</span></span>](what-is-a-transaction.md)
-   [<span data-ttu-id="a9436-109">Trabalhando com transações</span><span class="sxs-lookup"><span data-stu-id="a9436-109">Working With Transactions</span></span>](programming-model.md)
-   [<span data-ttu-id="a9436-110">Escrevendo um Gerenciador de recursos</span><span class="sxs-lookup"><span data-stu-id="a9436-110">Writing a Resource Manager</span></span>](writing-a-resource-manager.md)
-   [<span data-ttu-id="a9436-111">Interoperabilidade com outros recursos do Windows</span><span class="sxs-lookup"><span data-stu-id="a9436-111">Interoperability With Other Windows Features</span></span>](interoperability-with-other-windows-features.md)
-   [<span data-ttu-id="a9436-112">Segurança de KTM e direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="a9436-112">KTM Security and Access Rights</span></span>](ktm-security-and-access-rights.md)

<span data-ttu-id="a9436-113">O KTM depende do [sistema de arquivos de log comum](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) para sua operação.</span><span class="sxs-lookup"><span data-stu-id="a9436-113">KTM relies on the [Common Log File System](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) for its operation.</span></span> <span data-ttu-id="a9436-114">CLFS é um sistema de registro em log que é capaz de habilitar transações.</span><span class="sxs-lookup"><span data-stu-id="a9436-114">CLFS is a logging system that is capable of enabling transactions.</span></span>

 

 
