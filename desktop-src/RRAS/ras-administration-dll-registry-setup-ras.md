---
title: Configuração do registro da DLL de administração do RAS
description: O programa de instalação para uma DLL de administração de RAS de terceiros deve registrar a DLL com o RAS, fornecendo informações sob a chave a seguir no registro.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aed28fc41334c161a11ce5575b6395c4bb5da5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498789"
---
# <a name="ras-administration-dll-registry-setup"></a><span data-ttu-id="0d305-103">Configuração do registro da DLL de administração do RAS</span><span class="sxs-lookup"><span data-stu-id="0d305-103">RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="0d305-104">O programa de instalação para uma DLL de administração de RAS de terceiros deve registrar a DLL com o RAS, fornecendo informações sob a chave a seguir no registro.</span><span class="sxs-lookup"><span data-stu-id="0d305-104">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="0d305-105">Para registrar a DLL, defina os valores a seguir nessa chave.</span><span class="sxs-lookup"><span data-stu-id="0d305-105">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="0d305-106">Nome do valor</span><span class="sxs-lookup"><span data-stu-id="0d305-106">Value name</span></span>    | <span data-ttu-id="0d305-107">Dados do valor</span><span class="sxs-lookup"><span data-stu-id="0d305-107">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="0d305-108">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="0d305-108">*DisplayName*</span></span> | <span data-ttu-id="0d305-109">Uma cadeia de caracteres **reg \_ sz** que contém o nome de exibição amigável da dll.</span><span class="sxs-lookup"><span data-stu-id="0d305-109">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="0d305-110">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="0d305-110">*DLLPath*</span></span>     | <span data-ttu-id="0d305-111">Uma cadeia de caracteres **reg \_ sz** que contém o caminho completo da dll.</span><span class="sxs-lookup"><span data-stu-id="0d305-111">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="0d305-112">Por exemplo, a entrada de registro para uma DLL de administração de RAS de uma empresa fictícia chamada proeletromagnéticon, Inc. pode ser:</span><span class="sxs-lookup"><span data-stu-id="0d305-112">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="0d305-113">*DisplayName* : **reg \_ sz** : dll de administração de Ras proeletromagnético</span><span class="sxs-lookup"><span data-stu-id="0d305-113">*DisplayName* : **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="0d305-114">*DLLPath* : **reg \_ sz** : C: \\ NT \\ System32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="0d305-114">*DLLPath* : **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="0d305-115">O programa de instalação para uma DLL de administração de RAS também deve fornecer a funcionalidade de remoção/desinstalação.</span><span class="sxs-lookup"><span data-stu-id="0d305-115">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="0d305-116">Se um usuário remover a DLL, o programa de instalação deverá excluir as entradas do registro da DLL.</span><span class="sxs-lookup"><span data-stu-id="0d305-116">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 




