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
# <a name="about-ktm"></a>Sobre o KTM

O KTM (kernel Transaction Manager) é um serviço de gerenciamento de transações. Ele torna as transações disponíveis como objetos kernel e fornece serviços de gerenciamento de transações para componentes do sistema, como o [NTFS Transacional](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF).

Os tópicos a seguir descrevem os usos e os recursos do KTM:

-   [O que é uma transação?](what-is-a-transaction.md)
-   [Trabalhando com transações](programming-model.md)
-   [Escrevendo um Gerenciador de recursos](writing-a-resource-manager.md)
-   [Interoperabilidade com outros recursos do Windows](interoperability-with-other-windows-features.md)
-   [Segurança de KTM e direitos de acesso](ktm-security-and-access-rights.md)

O KTM depende do [sistema de arquivos de log comum](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) para sua operação. CLFS é um sistema de registro em log que é capaz de habilitar transações.

 

 
