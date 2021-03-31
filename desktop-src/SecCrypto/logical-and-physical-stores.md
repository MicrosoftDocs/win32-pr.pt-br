---
description: As lojas de sistema padrão, incluindo MY, CA e ROOT, são implementadas como repositórios de coleta lógica com um número de repositórios físicos predefinidos como armazenamentos de membros.
ms.assetid: 1d82b94b-4842-454a-aca4-823cd264ac52
title: Repositórios lógicos e físicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a5441bac91e39b7f4c124daecd3a6a569c323c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647309"
---
# <a name="logical-and-physical-stores"></a>Repositórios lógicos e físicos

As lojas de sistema padrão, incluindo MY, CA e ROOT, são implementadas como repositórios de coleta lógica com um número de repositórios físicos predefinidos como armazenamentos de membros. Os repositórios físicos de membros de um repositório do sistema são abertos automaticamente quando o armazenamento do sistema é aberto. Um usuário pode adicionar armazenamentos físicos adicionais a qualquer coleção de armazenamento do sistema. A função CryptoAPI [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore) adiciona um novo repositório físico a uma coleção de armazenamento do sistema. [**CertUnregisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregisterphysicalstore) Desassocia um repositório físico de um armazenamento de sistema lógico. O [**CertRegisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore) cria um novo repositório do sistema em um HKEY do registro, enquanto o [**CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore) remove um repositório do sistema do registro.

No CryptoAPI, os repositórios de sistema são repositórios lógicos com repositórios físicos associados. Todos os certificados em um armazenamento de sistema existente permanecem disponíveis e a adição física de novos certificados é feita nos armazenamentos físicos que compõem o armazenamento do sistema lógico.

Os usuários que preferem continuar a usar os armazenamentos físicos do sistema e não converter em repositórios lógicos podem abrir os repositórios do sistema com o provedor de registro do sistema do Prov do CERT \_ Store \_ \_ \_ . Esse provedor continuará a usar cada repositório do sistema como um repositório físico único.

As funções [**CertEnumSystemStoreLocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation), [**CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore)e [**CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore) listam locais de armazenamento do sistema, armazenamentos do sistema disponíveis e todos os repositórios físicos que são membros de um repositório do sistema.

Os repositórios do sistema também podem ser realocados. Por padrão, um repositório do sistema é aberto em relação a uma subchave do registro após um padrão predefinido. Para obter mais informações, consulte [locais da loja do sistema](system-store-locations.md). A configuração \_ do \_ sinalizador de realocação do repositório do sistema de CERT \_ \_ no parâmetro *dwFlags* passado para [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) coloca um repositório do sistema no registro em uma subchave do Registro especificada pelo usuário em vez do predefinido.

 

 



