---
description: A ação de administrador é uma ação de nível superior usada para executar instalações administrativas.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: Ação de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00106c9ab7877918e122f1ec9bd201fe30bb68b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828084"
---
# <a name="admin-action"></a><span data-ttu-id="e7169-103">Ação de administrador</span><span class="sxs-lookup"><span data-stu-id="e7169-103">ADMIN Action</span></span>

<span data-ttu-id="e7169-104">A ação de administrador é uma ação de nível superior usada para executar [instalações administrativas](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="e7169-104">The ADMIN action is a top-level action used to perform [administrative installations](administrative-installation.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e7169-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="e7169-105">Sequence Restrictions</span></span>

<span data-ttu-id="e7169-106">Não há restrições de sequência.</span><span class="sxs-lookup"><span data-stu-id="e7169-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e7169-107">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="e7169-107">ActionData Messages</span></span>

<span data-ttu-id="e7169-108">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="e7169-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7169-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7169-109">Remarks</span></span>

<span data-ttu-id="e7169-110">A ação de administrador não é chamada de dentro da sequência da tabela de ações, Windows Installer executa essa ação quando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) é chamado com o parâmetro *szCommandLine* definido como "action = admin" ou o executável de linha de comando Msiexec.exe é chamado com a opção de linha de comando "/a".</span><span class="sxs-lookup"><span data-stu-id="e7169-110">The ADMIN action is not called from within the action table sequence, Windows Installer executes this action when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called with the *szCommandLine* parameter set to "ACTION=ADMIN" or the command line executable Msiexec.exe is called with the '/a' command line switch.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7169-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7169-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7169-112">Tabela AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="e7169-112">AdminUISequence Table</span></span>](adminuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="e7169-113">Tabela AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="e7169-113">AdminExecuteSequence Table</span></span>](adminexecutesequence-table.md)
</dt> </dl>

 

 



