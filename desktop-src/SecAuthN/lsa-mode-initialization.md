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
# <a name="lsa-mode-initialization"></a><span data-ttu-id="343d9-104">Inicialização do modo LSA</span><span class="sxs-lookup"><span data-stu-id="343d9-104">LSA Mode Initialization</span></span>

<span data-ttu-id="343d9-105">Quando o sistema de computador é iniciado, a [*autoridade de segurança local*](../secgloss/l-gly.md) (LSA) carrega automaticamente todas as DLLs do pacote de [](../secgloss/s-gly.md) / [*autenticação*](../secgloss/a-gly.md) do provedor de suporte de segurança registrado (SSP/AP) em seu espaço de processo.</span><span class="sxs-lookup"><span data-stu-id="343d9-105">When the computer system is started, the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) automatically loads all registered [*security support provider*](../secgloss/s-gly.md)/[*authentication package*](../secgloss/a-gly.md) (SSP/AP) DLLs into its process space.</span></span> <span data-ttu-id="343d9-106">As ilustrações a seguir mostram o processo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="343d9-106">The following illustrations show the initialization process.</span></span>

> [!Note]  
> <span data-ttu-id="343d9-107">"Kerberos" representa o Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP e "My SSP/AP" representa um SSP/PA personalizado que contém dois pacotes de segurança personalizados.</span><span class="sxs-lookup"><span data-stu-id="343d9-107">"Kerberos" represents the Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP, and "My SSP/AP" represents a custom SSP/AP that contains two custom security packages.</span></span>

 

![inicialização do modo LSA](images/lsamode1.png)

<span data-ttu-id="343d9-109">Na inicialização, a LSA chama a função [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) em cada SSP/AP para obter ponteiros para as funções implementadas por cada [*pacote de segurança*](../secgloss/s-gly.md) na dll.</span><span class="sxs-lookup"><span data-stu-id="343d9-109">At startup, the LSA calls the [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) function in each SSP/AP to obtain pointers to the functions implemented by each [*security package*](../secgloss/s-gly.md) in the DLL.</span></span> <span data-ttu-id="343d9-110">Os ponteiros de função são passados para a LSA em uma matriz de estruturas de [**\_ \_ tabela de função SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) .</span><span class="sxs-lookup"><span data-stu-id="343d9-110">The function pointers are passed to the LSA in an array of [**SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) structures.</span></span>

![o LSA chama splsamodeinitialize para obter ponteiros de função](images/lsamode2.png)

<span data-ttu-id="343d9-112">Depois de receber o conjunto de estruturas de [**\_ \_ tabela de função SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) , a LSA chama a função de [**inicialização**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) de cada pacote de segurança.</span><span class="sxs-lookup"><span data-stu-id="343d9-112">After receiving the set of [**SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) structures, the LSA calls each security package's [**SpInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) function.</span></span> <span data-ttu-id="343d9-113">A LSA usa essa chamada de função para passar cada pacote de segurança de uma estrutura de [**\_ \_ \_ tabela de função SECPKG LSA**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) , que contém ponteiros para as funções de suporte do LSA disponíveis para pacotes de segurança.</span><span class="sxs-lookup"><span data-stu-id="343d9-113">The LSA uses this function call to pass each security package an [**LSA\_SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) structure, which contains pointers to the LSA support functions available to security packages.</span></span> <span data-ttu-id="343d9-114">Além de armazenar os ponteiros para as funções de suporte do LSA, os pacotes de segurança personalizados devem usar a implementação **da função de inicialização para** executar qualquer processamento relacionado a inicializações.</span><span class="sxs-lookup"><span data-stu-id="343d9-114">In addition to storing the pointers to the LSA support functions, custom security packages should use their implementation of the **SpInitialize** function to perform any initialization-related processing.</span></span>

<span data-ttu-id="343d9-115">Para obter uma lista das funções de suporte de LSA disponíveis para os pacotes de segurança do modo LSA, consulte [funções LSA chamadas por SSP/APS](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="343d9-115">For a list of the LSA support functions available to LSA-mode security packages, see [LSA Functions Called by SSP/APs](authentication-functions.md).</span></span>

<span data-ttu-id="343d9-116">Para obter informações sobre como registrar uma DLL SSP/PA, consulte [registrando DLLs SSP/PA](registering-ssp-ap-dlls.md).</span><span class="sxs-lookup"><span data-stu-id="343d9-116">For information about registering an SSP/AP DLL, see [Registering SSP/AP DLLs](registering-ssp-ap-dlls.md).</span></span>

 

 
