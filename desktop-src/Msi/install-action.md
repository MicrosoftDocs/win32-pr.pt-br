---
description: A ação de instalação é uma ação de nível superior chamada para instalar ou remover componentes.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Ação de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04279ba66f189ff83146fc2010e6843c20b404d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010856"
---
# <a name="install-action"></a><span data-ttu-id="74d14-103">Ação de instalação</span><span class="sxs-lookup"><span data-stu-id="74d14-103">INSTALL Action</span></span>

<span data-ttu-id="74d14-104">A ação de instalação é uma ação de nível superior chamada para instalar ou remover componentes.</span><span class="sxs-lookup"><span data-stu-id="74d14-104">The INSTALL action is a top-level action called to install or remove components.</span></span> <span data-ttu-id="74d14-105">Essa ação consulta a [tabela InstallUISequence](installuisequence-table.md) e a [tabela InstallExecuteSequence](installexecutesequence-table.md) para que a ação seja executada, a condição para execução da ação e o lugar da ação na sequência:</span><span class="sxs-lookup"><span data-stu-id="74d14-105">This action queries the [InstallUISequence Table](installuisequence-table.md) and [InstallExecuteSequence Table](installexecutesequence-table.md) for the action to execute, the condition for action execution, and the place of the action in the sequence:</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="74d14-106">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="74d14-106">Sequence Restrictions</span></span>

<span data-ttu-id="74d14-107">Não há restrições de sequência.</span><span class="sxs-lookup"><span data-stu-id="74d14-107">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="74d14-108">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="74d14-108">ActionData Messages</span></span>

<span data-ttu-id="74d14-109">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="74d14-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="74d14-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="74d14-110">Remarks</span></span>

<span data-ttu-id="74d14-111">A ação de instalação não é chamada de dentro da sequência da tabela de ações, ela é passada para Windows Installer quando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) é chamado ou o executável de linha de comando Msiexec.exe é chamado com a opção de linha de comando '**/i**' ou quando qualquer função do instalador é chamada que pode executar uma tarefa de instalação, como [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)ou [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span><span class="sxs-lookup"><span data-stu-id="74d14-111">The INSTALL action is not called from within the action table sequence, it is passed to Windows Installer when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called, or the command line executable Msiexec.exe is called with the '**/i**' command line switch, or when any installer function is called that may perform an installation task, such as [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta), or [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span></span>

 

 



