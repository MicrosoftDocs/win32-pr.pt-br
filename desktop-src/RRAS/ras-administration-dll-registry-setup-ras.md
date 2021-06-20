---
title: Configuração do registro da DLL de administração do RAS
description: Entenda os requisitos para registrar uma DLL de administração de serviço de acesso remoto (RAS) de terceiros com o RAS.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0af8e4b189de69f254429c18beb4756e01ad56
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406709"
---
# <a name="ras-administration-dll-registry-setup"></a><span data-ttu-id="fc50d-103">Configuração do registro da DLL de administração do RAS</span><span class="sxs-lookup"><span data-stu-id="fc50d-103">RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="fc50d-104">O programa de instalação para uma DLL de administração de RAS de terceiros deve registrar a DLL com o RAS, fornecendo informações sob a chave a seguir no registro.</span><span class="sxs-lookup"><span data-stu-id="fc50d-104">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="fc50d-105">Para registrar a DLL, defina os valores a seguir nessa chave.</span><span class="sxs-lookup"><span data-stu-id="fc50d-105">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="fc50d-106">Nome do valor</span><span class="sxs-lookup"><span data-stu-id="fc50d-106">Value name</span></span>    | <span data-ttu-id="fc50d-107">Dados do valor</span><span class="sxs-lookup"><span data-stu-id="fc50d-107">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="fc50d-108">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="fc50d-108">*DisplayName*</span></span> | <span data-ttu-id="fc50d-109">Uma cadeia de caracteres **reg \_ sz** que contém o nome de exibição amigável da dll.</span><span class="sxs-lookup"><span data-stu-id="fc50d-109">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="fc50d-110">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="fc50d-110">*DLLPath*</span></span>     | <span data-ttu-id="fc50d-111">Uma cadeia de caracteres **reg \_ sz** que contém o caminho completo da dll.</span><span class="sxs-lookup"><span data-stu-id="fc50d-111">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="fc50d-112">Por exemplo, a entrada de registro para uma DLL de administração de RAS de uma empresa fictícia chamada proeletromagnéticon, Inc. pode ser:</span><span class="sxs-lookup"><span data-stu-id="fc50d-112">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="fc50d-113">*DisplayName* : **reg \_ sz** : dll de administração de Ras proeletromagnético</span><span class="sxs-lookup"><span data-stu-id="fc50d-113">*DisplayName* : **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="fc50d-114">*DLLPath* : **reg \_ sz** : C: \\ NT \\ System32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="fc50d-114">*DLLPath* : **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="fc50d-115">O programa de instalação para uma DLL de administração de RAS também deve fornecer a funcionalidade de remoção/desinstalação.</span><span class="sxs-lookup"><span data-stu-id="fc50d-115">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="fc50d-116">Se um usuário remover a DLL, o programa de instalação deverá excluir as entradas do registro da DLL.</span><span class="sxs-lookup"><span data-stu-id="fc50d-116">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 




