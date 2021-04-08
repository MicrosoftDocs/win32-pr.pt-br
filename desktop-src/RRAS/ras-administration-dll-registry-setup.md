---
title: Sobre a configuração do registro da DLL de administração do RAS
description: O programa de instalação para uma DLL de administração de RAS de terceiros deve registrar a DLL com o RAS, fornecendo informações sob a chave a seguir no registro.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- Administração de RAS RRAS, configuração do registro de DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf487f792a4add9ebf61e8f866b9f0577fb468d
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103823474"
---
# <a name="about-ras-administration-dll-registry-setup"></a><span data-ttu-id="50370-104">Sobre a configuração do registro da DLL de administração do RAS</span><span class="sxs-lookup"><span data-stu-id="50370-104">About RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="50370-105">O programa de instalação para uma DLL de administração de RAS de terceiros deve registrar a DLL com o RAS, fornecendo informações sob a chave a seguir no registro.</span><span class="sxs-lookup"><span data-stu-id="50370-105">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="50370-106">Para registrar a DLL, defina os valores a seguir nessa chave.</span><span class="sxs-lookup"><span data-stu-id="50370-106">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="50370-107">Nome do valor</span><span class="sxs-lookup"><span data-stu-id="50370-107">Value name</span></span>    | <span data-ttu-id="50370-108">Dados do valor</span><span class="sxs-lookup"><span data-stu-id="50370-108">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="50370-109">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="50370-109">*DisplayName*</span></span> | <span data-ttu-id="50370-110">Uma cadeia de caracteres **reg \_ sz** que contém o nome de exibição amigável da dll.</span><span class="sxs-lookup"><span data-stu-id="50370-110">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="50370-111">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="50370-111">*DLLPath*</span></span>     | <span data-ttu-id="50370-112">Uma cadeia de caracteres **reg \_ sz** que contém o caminho completo da dll.</span><span class="sxs-lookup"><span data-stu-id="50370-112">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="50370-113">Como o RAS dá suporte a várias DLLs de administração de RAS, o valor de registro **DLLPath** pode conter uma lista delimitada por ponto-e-vírgula de caminhos.</span><span class="sxs-lookup"><span data-stu-id="50370-113">Because RAS supports multiple RAS Administration DLLs, the registry value **DLLPath** can contain a semi-colon delimited list of paths.</span></span> <span data-ttu-id="50370-114">Por exemplo, a entrada de registro para uma DLL de administração de RAS de uma empresa fictícia chamada proeletromagnéticon, Inc., pode ser a seguinte:</span><span class="sxs-lookup"><span data-stu-id="50370-114">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc., might be the following:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="50370-115">*DisplayName*: **reg \_ sz** : dll de administração de Ras proeletromagnético</span><span class="sxs-lookup"><span data-stu-id="50370-115">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="50370-116">*DLLPath*: **reg \_ sz** : C: \\ NT \\ System32 \\ntwkadm.dll; C: \\ NT \\ System32 \\ntwkadm2.dll</span><span class="sxs-lookup"><span data-stu-id="50370-116">*DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll; C:\\nt\\system32\\ntwkadm2.dll</span></span>

<span data-ttu-id="50370-117">O RAS chama as DLLs na ordem em que estão listadas nesse valor de registro.</span><span class="sxs-lookup"><span data-stu-id="50370-117">RAS calls the DLLs in the order in which they are listed in this registry value.</span></span> <span data-ttu-id="50370-118">O valor *DisplayName* do registro ainda contém apenas um único nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="50370-118">The registry value *DisplayName* still contains only a single display name.</span></span>

<span data-ttu-id="50370-119">O programa de instalação para uma DLL de administração de RAS também deve fornecer a funcionalidade de remoção e desinstalação.</span><span class="sxs-lookup"><span data-stu-id="50370-119">The setup program for a RAS administration DLL must also provide remove and uninstall functionality.</span></span> <span data-ttu-id="50370-120">Se um usuário remover a DLL, o programa de instalação deverá excluir as entradas do registro para a DLL.</span><span class="sxs-lookup"><span data-stu-id="50370-120">If a user removes the DLL, the setup program must delete the registry entries for the DLL.</span></span>

<span data-ttu-id="50370-121">**Windows 2000/NT:** O RAS dá suporte a apenas uma DLL de administração de RAS, portanto, o valor de registro **DLLPath** não pode conter uma lista delimitada por ponto-e-vírgula de caminhos.</span><span class="sxs-lookup"><span data-stu-id="50370-121">**Windows 2000/NT:** RAS supports only one RAS Administration DLL, so the registry value **DLLPath** cannot contain a semi-colon delimited list of paths.</span></span>

 

 




