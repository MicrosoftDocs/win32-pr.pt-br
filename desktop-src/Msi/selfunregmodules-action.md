---
description: A ação SelfUnregModules cancela o registro de todos os módulos listados na tabela SelfReg que estão agendados para serem desinstalados. O instalador não registra automaticamente. Arquivos EXE.
ms.assetid: fa5a5abb-ecd4-434c-b176-83cdca280a13
title: Ação SelfUnregModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3a0d98d8a8afe45b9b78f5c8af8ca2f84b2244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751836"
---
# <a name="selfunregmodules-action"></a><span data-ttu-id="03d86-104">Ação SelfUnregModules</span><span class="sxs-lookup"><span data-stu-id="03d86-104">SelfUnregModules Action</span></span>

<span data-ttu-id="03d86-105">A ação SelfUnregModules cancela o registro de todos os módulos listados na [tabela selfreg](selfreg-table.md) que estão agendados para serem desinstalados.</span><span class="sxs-lookup"><span data-stu-id="03d86-105">The SelfUnregModules action unregisters all modules listed in the [SelfReg table](selfreg-table.md) that are scheduled to be uninstalled.</span></span> <span data-ttu-id="03d86-106">O instalador não registra automaticamente. Arquivos EXE.</span><span class="sxs-lookup"><span data-stu-id="03d86-106">The installer does not self-register .EXE files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="03d86-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="03d86-107">Sequence Restrictions</span></span>

<span data-ttu-id="03d86-108">A ação [InstallValidate](installvalidate-action.md) deve aparecer antes da ação SelfUnregModules na sequência.</span><span class="sxs-lookup"><span data-stu-id="03d86-108">The [InstallValidate](installvalidate-action.md) action must appear before the SelfUnregModules action in the sequence.</span></span> <span data-ttu-id="03d86-109">Se uma ação [SelfRegModules](selfregmodules-action.md) for usada, ela deverá aparecer após a ação SelfUnregModules na sequência.</span><span class="sxs-lookup"><span data-stu-id="03d86-109">If a [SelfRegModules](selfregmodules-action.md) action is used it must appear after the SelfUnregModules action in the sequence.</span></span> <span data-ttu-id="03d86-110">Se uma [ação removes](removefiles-action.md) for usada, ela deverá aparecer após a ação SelfUnregModules na sequência.</span><span class="sxs-lookup"><span data-stu-id="03d86-110">If a [RemoveFiles action](removefiles-action.md) is used it must appear after the SelfUnregModules action in the sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="03d86-111">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="03d86-111">ActionData Messages</span></span>



| <span data-ttu-id="03d86-112">Campo</span><span class="sxs-lookup"><span data-stu-id="03d86-112">Field</span></span> | <span data-ttu-id="03d86-113">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="03d86-113">Description of action data</span></span>                             |
|-------|--------------------------------------------------------|
| <span data-ttu-id="03d86-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="03d86-114">\[1\]</span></span> | <span data-ttu-id="03d86-115">Identificador do arquivo de módulo não registrado.</span><span class="sxs-lookup"><span data-stu-id="03d86-115">Identifier of unregistered module file.</span></span>                |
| <span data-ttu-id="03d86-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="03d86-116">\[2\]</span></span> | <span data-ttu-id="03d86-117">Identificador da pasta que contém o arquivo de módulo não registrado.</span><span class="sxs-lookup"><span data-stu-id="03d86-117">Identifier of folder holding unregistered module file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="03d86-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="03d86-118">Remarks</span></span>

<span data-ttu-id="03d86-119">A ação SelfUnregModules tenta chamar a função [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) do módulo cujo registro deve ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="03d86-119">The SelfUnregModules action attempts to call the [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) function of the module that is to be unregistered.</span></span> <span data-ttu-id="03d86-120">Essa ação é executada com privilégios elevados quando a instalação está sendo executada com privilégios elevados, como durante uma instalação por máquina.</span><span class="sxs-lookup"><span data-stu-id="03d86-120">This action runs with elevated privileges when the installation is being run with elevated privileges, such as during a per-machine installation.</span></span> <span data-ttu-id="03d86-121">Durante uma instalação por usuário, o instalador executa essa ação com privilégios de usuário.</span><span class="sxs-lookup"><span data-stu-id="03d86-121">During a per-user installation, the installer runs this action with user privileges.</span></span>

<span data-ttu-id="03d86-122">Observe que você não pode especificar a ordem na qual o instalador cancela o registro de DLLs de registro automático usando a ação SelfUnRegModules.</span><span class="sxs-lookup"><span data-stu-id="03d86-122">Note that you cannot specify the order in which the installer unregisters self-registering DLLs by using the SelfUnRegModules action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03d86-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03d86-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03d86-124">Especificando a ordem de auto-registro</span><span class="sxs-lookup"><span data-stu-id="03d86-124">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
