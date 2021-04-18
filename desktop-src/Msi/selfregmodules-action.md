---
description: A ação SelfRegModules processa todos os módulos listados na tabela SelfReg e registra todos os módulos instalados com o sistema. O instalador não registra automaticamente arquivos EXE.
ms.assetid: b139ae28-e479-4915-909d-2449244e9fd6
title: Ação SelfRegModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75895b1886fad51f36113ce6e677ba6a534ab0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753258"
---
# <a name="selfregmodules-action"></a><span data-ttu-id="9dd0b-104">Ação SelfRegModules</span><span class="sxs-lookup"><span data-stu-id="9dd0b-104">SelfRegModules Action</span></span>

<span data-ttu-id="9dd0b-105">A ação SelfRegModules processa todos os módulos listados na tabela [selfreg](selfreg-table.md) e registra todos os módulos instalados com o sistema.</span><span class="sxs-lookup"><span data-stu-id="9dd0b-105">The SelfRegModules action processes all modules listed in the [SelfReg](selfreg-table.md) table and registers all installed modules with the system.</span></span> <span data-ttu-id="9dd0b-106">O instalador não registra automaticamente arquivos EXE.</span><span class="sxs-lookup"><span data-stu-id="9dd0b-106">The installer does not self-register EXE files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="9dd0b-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="9dd0b-107">Sequence Restrictions</span></span>

<span data-ttu-id="9dd0b-108">A ação [InstallValidate](installvalidate-action.md) deve ser chamada antes de chamar a ação SelfRegModules.</span><span class="sxs-lookup"><span data-stu-id="9dd0b-108">The [InstallValidate](installvalidate-action.md) action must be called before calling the SelfRegModules action.</span></span> <span data-ttu-id="9dd0b-109">Se uma ação [InstallFiles](installfiles-action.md) for usada, ela deverá aparecer antes da ação SelfRegModules na sequência.</span><span class="sxs-lookup"><span data-stu-id="9dd0b-109">If an [InstallFiles](installfiles-action.md) action is used, it must appear before the SelfRegModules action in the sequence.</span></span> <span data-ttu-id="9dd0b-110">Como a ação SelfRegModules altera o sistema, SelfRegModules deve vir após a [ação InstallInitialize](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="9dd0b-110">Because the SelfRegModules action changes the system, SelfRegModules should come after the [InstallInitialize action](installinitialize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="9dd0b-111">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="9dd0b-111">ActionData Messages</span></span>



| <span data-ttu-id="9dd0b-112">Campo</span><span class="sxs-lookup"><span data-stu-id="9dd0b-112">Field</span></span> | <span data-ttu-id="9dd0b-113">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="9dd0b-113">Description of action data</span></span>                           |
|-------|------------------------------------------------------|
| <span data-ttu-id="9dd0b-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="9dd0b-114">\[1\]</span></span> | <span data-ttu-id="9dd0b-115">Identificador do arquivo de módulo registrado.</span><span class="sxs-lookup"><span data-stu-id="9dd0b-115">Identifier of registered module file.</span></span>                |
| <span data-ttu-id="9dd0b-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="9dd0b-116">\[2\]</span></span> | <span data-ttu-id="9dd0b-117">Identificador da pasta que contém o arquivo de módulo registrado.</span><span class="sxs-lookup"><span data-stu-id="9dd0b-117">Identifier of folder holding registered module file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9dd0b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="9dd0b-118">Remarks</span></span>

<span data-ttu-id="9dd0b-119">A ação SelfRegModules tenta chamar a função [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) do módulo agendado para ser registrado.</span><span class="sxs-lookup"><span data-stu-id="9dd0b-119">The SelfRegModules action attempts to call the [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) function of the module scheduled to be registered.</span></span> <span data-ttu-id="9dd0b-120">Essa ação é executada com privilégios elevados quando a instalação está sendo executada com privilégios elevados, como durante uma instalação por máquina.</span><span class="sxs-lookup"><span data-stu-id="9dd0b-120">This action runs with elevated privileges when the installation is being run with elevated privileges, such as during a per-machine installation.</span></span> <span data-ttu-id="9dd0b-121">Durante uma instalação por usuário, o instalador executa essa ação com privilégios de usuário.</span><span class="sxs-lookup"><span data-stu-id="9dd0b-121">During a per-user installation the installer runs this action with user privileges.</span></span>

<span data-ttu-id="9dd0b-122">Observe que você não pode especificar a ordem na qual o instalador registra DLLs de registro automático usando a [ação SelfUnRegModules](selfunregmodules-action.md).</span><span class="sxs-lookup"><span data-stu-id="9dd0b-122">Note that you cannot specify the order in which the installer registers self-registering DLLs by using the [SelfUnRegModules action](selfunregmodules-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9dd0b-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9dd0b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dd0b-124">Especificando a ordem de auto-registro</span><span class="sxs-lookup"><span data-stu-id="9dd0b-124">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
