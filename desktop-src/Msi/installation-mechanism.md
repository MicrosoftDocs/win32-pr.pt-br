---
description: 'Há duas fases para um processo de instalação bem-sucedido: aquisição e execução. Se a instalação não for bem-sucedida, poderá ocorrer uma fase de reversão.'
ms.assetid: e9cda321-6978-4f9f-aff4-ccf609c88667
title: Mecanismo de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78455cb26e7672614266453e82f1a44c44e6b14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752041"
---
# <a name="installation-mechanism"></a><span data-ttu-id="55ce1-104">Mecanismo de instalação</span><span class="sxs-lookup"><span data-stu-id="55ce1-104">Installation Mechanism</span></span>

<span data-ttu-id="55ce1-105">Há duas fases para um processo de instalação bem-sucedido: aquisição e execução.</span><span class="sxs-lookup"><span data-stu-id="55ce1-105">There are two phases to a successful installation process: acquisition and execution.</span></span> <span data-ttu-id="55ce1-106">Se a instalação não for bem-sucedida, poderá ocorrer uma fase de reversão.</span><span class="sxs-lookup"><span data-stu-id="55ce1-106">If the installation is unsuccessful, a rollback phase may occur.</span></span>

## <a name="acquisition"></a><span data-ttu-id="55ce1-107">Aquisição</span><span class="sxs-lookup"><span data-stu-id="55ce1-107">Acquisition</span></span>

<span data-ttu-id="55ce1-108">No início da fase de aquisição, um aplicativo ou um usuário instrui o instalador a instalar um recurso ou um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="55ce1-108">At the beginning of the acquisition phase, an application or a user instructs the installer to install a feature or an application.</span></span> <span data-ttu-id="55ce1-109">Em seguida, o instalador progride pelas ações especificadas nas tabelas de sequência do banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="55ce1-109">The installer then progresses through the actions specified in the sequence tables of the installation database.</span></span> <span data-ttu-id="55ce1-110">Essas ações consultam o banco de dados de instalação e geram um script que fornece um procedimento passo a passo para a execução da instalação.</span><span class="sxs-lookup"><span data-stu-id="55ce1-110">These actions query the installation database and generate a script that gives a step-by-step procedure for performing the installation.</span></span>

## <a name="execution"></a><span data-ttu-id="55ce1-111">Execução</span><span class="sxs-lookup"><span data-stu-id="55ce1-111">Execution</span></span>

<span data-ttu-id="55ce1-112">Durante a fase de execução, o instalador passa as informações para um processo com privilégios elevados e executa o script.</span><span class="sxs-lookup"><span data-stu-id="55ce1-112">During the execution phase, the installer passes the information to a process with elevated privileges and runs the script.</span></span>

## <a name="rollback"></a><span data-ttu-id="55ce1-113">Reversão</span><span class="sxs-lookup"><span data-stu-id="55ce1-113">Rollback</span></span>

<span data-ttu-id="55ce1-114">Se uma instalação não for bem-sucedida, o instalador restaurará o estado original do computador.</span><span class="sxs-lookup"><span data-stu-id="55ce1-114">If an installation is unsuccessful, the installer restores the original state of the computer.</span></span> <span data-ttu-id="55ce1-115">Quando o instalador processa o script de instalação, ele gera um script de reversão simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="55ce1-115">When the installer processes the installation script it simultaneously generates a rollback script.</span></span> <span data-ttu-id="55ce1-116">Além do script de reversão, o instalador salva uma cópia de cada arquivo que ele exclui durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="55ce1-116">In addition to the rollback script, the installer saves a copy of every file it deletes during the installation.</span></span> <span data-ttu-id="55ce1-117">Esses arquivos são mantidos em um diretório de sistema oculto.</span><span class="sxs-lookup"><span data-stu-id="55ce1-117">These files are kept in a hidden, system directory.</span></span> <span data-ttu-id="55ce1-118">Quando a instalação for concluída, o script de reversão e os arquivos salvos serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="55ce1-118">Once the installation is complete, the rollback script and the saved files are deleted.</span></span> <span data-ttu-id="55ce1-119">Para obter mais informações, consulte [Rollback Installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="55ce1-119">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

 

 



