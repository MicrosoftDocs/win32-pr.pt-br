---
description: Quando o sistema de computador é iniciado, a autoridade de segurança local (LSA) carrega automaticamente todas as DLLs registradas do provedor de suporte de segurança/pacote de autenticação (SSP/AP) em seu espaço de processo. As ilustrações a seguir mostram o processo de inicialização.
ms.assetid: 2d52cbbf-9e28-4c6f-8b4c-448b73c6dbf8
title: Inicialização do modo LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4212a584d290e67c6465488c8398604db2c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506090"
---
# <a name="lsa-mode-initialization"></a>Inicialização do modo LSA

Quando o sistema de computador é iniciado, a [*autoridade de segurança local*](../secgloss/l-gly.md) (LSA) carrega automaticamente todas as DLLs do pacote de [](../secgloss/s-gly.md) / [*autenticação*](../secgloss/a-gly.md) do provedor de suporte de segurança registrado (SSP/AP) em seu espaço de processo. As ilustrações a seguir mostram o processo de inicialização.

> [!Note]  
> "Kerberos" representa o Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP e "My SSP/AP" representa um SSP/PA personalizado que contém dois pacotes de segurança personalizados.

 

![inicialização do modo LSA](images/lsamode1.png)

Na inicialização, a LSA chama a função [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) em cada SSP/AP para obter ponteiros para as funções implementadas por cada [*pacote de segurança*](../secgloss/s-gly.md) na dll. Os ponteiros de função são passados para a LSA em uma matriz de estruturas de [**\_ \_ tabela de função SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) .

![o LSA chama splsamodeinitialize para obter ponteiros de função](images/lsamode2.png)

Depois de receber o conjunto de estruturas de [**\_ \_ tabela de função SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) , a LSA chama a função de [**inicialização**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) de cada pacote de segurança. A LSA usa essa chamada de função para passar cada pacote de segurança de uma estrutura de [**\_ \_ \_ tabela de função SECPKG LSA**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) , que contém ponteiros para as funções de suporte do LSA disponíveis para pacotes de segurança. Além de armazenar os ponteiros para as funções de suporte do LSA, os pacotes de segurança personalizados devem usar a implementação **da função de inicialização para** executar qualquer processamento relacionado a inicializações.

Para obter uma lista das funções de suporte de LSA disponíveis para os pacotes de segurança do modo LSA, consulte [funções LSA chamadas por SSP/APS](authentication-functions.md).

Para obter informações sobre como registrar uma DLL SSP/PA, consulte [registrando DLLs SSP/PA](registering-ssp-ap-dlls.md).

 

 
