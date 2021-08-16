---
description: Quando o sistema de computador é iniciado, a LSA (Autoridade de Segurança Local) carrega automaticamente todas as DLLs do SSP/AP (provedor de suporte de segurança/pacote de autenticação) registradas em seu espaço de processo. As ilustrações a seguir mostram o processo de inicialização.
ms.assetid: 2d52cbbf-9e28-4c6f-8b4c-448b73c6dbf8
title: Inicialização do modo LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4c55397e5970b8401e1429eba7d92a034e76ce0c999950131167580ded7e5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922116"
---
# <a name="lsa-mode-initialization"></a>Inicialização do modo LSA

Quando o sistema de computador é iniciado, a LSA [](../secgloss/s-gly.md)(Autoridade de Segurança [*Local)*](../secgloss/l-gly.md) carrega automaticamente todas as DLLs do pacote de autenticação do provedor de suporte de segurança / [](../secgloss/a-gly.md) registrado (SSP/AP) em seu espaço de processo. As ilustrações a seguir mostram o processo de inicialização.

> [!Note]  
> "Kerberos" representa o Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP e "Meu SSP/AP" representa um SSP/AP personalizado que contém dois pacotes de segurança personalizados.

 

![Inicialização do modo lsa](images/lsamode1.png)

Na inicialização, o LSA chama a função [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) em cada SSP/AP [](../secgloss/s-gly.md) para obter ponteiros para as funções implementadas por cada pacote de segurança na DLL. Os ponteiros de função são passados para o LSA em uma matriz de estruturas [**SECPKG \_ FUNCTION \_ TABLE.**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table)

![o lsa chama splsamodeinitialize para obter ponteiros de função](images/lsamode2.png)

Depois de receber o conjunto de [**estruturas SECPKG \_ FUNCTION \_ TABLE,**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) o LSA chama a função [**SpInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) de cada pacote de segurança. O LSA usa essa chamada de função para passar para cada pacote de segurança uma estrutura [**LSA \_ SECPKG \_ FUNCTION \_ TABLE,**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) que contém ponteiros para as funções de suporte LSA disponíveis para pacotes de segurança. Além de armazenar os ponteiros para as funções de suporte LSA, os pacotes de segurança personalizados devem usar sua implementação da função **SpInitialize** para executar qualquer processamento relacionado à inicialização.

Para ver uma lista das funções de suporte LSA disponíveis para pacotes de segurança no modo LSA, consulte Funções LSA chamadas por [SSP/APs](authentication-functions.md).

Para obter informações sobre como registrar uma DLL SSP/AP, consulte [Registrando DLLs SSP/AP](registering-ssp-ap-dlls.md).

 

 
