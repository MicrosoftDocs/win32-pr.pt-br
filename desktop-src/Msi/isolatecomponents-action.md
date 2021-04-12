---
description: A ação IsolateComponents instala uma cópia de um componente (normalmente uma DLL compartilhada) em um local privado para uso por um aplicativo específico (normalmente um. exe).
ms.assetid: 3f39ad5d-5539-48cc-8369-bd4d3127fbdd
title: Ação IsolateComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fe36f8c30e67591662ca2fce6c0b0ac2150ebb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297445"
---
# <a name="isolatecomponents-action"></a><span data-ttu-id="1a983-103">Ação IsolateComponents</span><span class="sxs-lookup"><span data-stu-id="1a983-103">IsolateComponents Action</span></span>

<span data-ttu-id="1a983-104">A ação IsolateComponents instala uma cópia de um componente (normalmente uma DLL compartilhada) em um local privado para uso por um aplicativo específico (normalmente um. exe).</span><span class="sxs-lookup"><span data-stu-id="1a983-104">The IsolateComponents action installs a copy of a component (commonly a shared DLL) into a private location for use by a specific application (typically an .exe).</span></span> <span data-ttu-id="1a983-105">Isso isola o aplicativo de outras cópias do componente que podem ser instaladas em um local compartilhado no computador.</span><span class="sxs-lookup"><span data-stu-id="1a983-105">This isolates the application from other copies of the component that may be installed to a shared location on the computer.</span></span> <span data-ttu-id="1a983-106">Para obter mais informações, consulte [componentes isolados](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="1a983-106">For more information, see [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="1a983-107">A ação refere-se a cada registro da [tabela IsolatedComponent](isolatedcomponent-table.md) e associa os arquivos do componente listado no \_ campo compartilhado do componente ao componente listado no \_ campo aplicativo de componente.</span><span class="sxs-lookup"><span data-stu-id="1a983-107">The action refers to each record of the [IsolatedComponent table](isolatedcomponent-table.md) and associates the files of the component listed in the Component\_Shared field with the component listed in the Component\_Application field.</span></span> <span data-ttu-id="1a983-108">O instalador instala os arquivos do componente \_ compartilhado no mesmo diretório que o aplicativo de componente \_ .</span><span class="sxs-lookup"><span data-stu-id="1a983-108">The installer installs the files of Component\_Shared into the same directory as Component\_Application.</span></span> <span data-ttu-id="1a983-109">O instalador gera um arquivo nesse diretório, com comprimento de zero bytes, com o nome do nome de arquivo curto para o aplicativo de componente \_ (normalmente, esse é o mesmo nome de arquivo que o. exe) acrescentado com. local.</span><span class="sxs-lookup"><span data-stu-id="1a983-109">The installer generates a file in this directory, zero bytes in length, having the short filename name of the key file for Component\_Application (typically this is the same file name as the .exe) appended with .local.</span></span> <span data-ttu-id="1a983-110">A ação IsolatedComponent não afeta a instalação do aplicativo de componente \_ .</span><span class="sxs-lookup"><span data-stu-id="1a983-110">The IsolatedComponent action does not affect the installation of Component\_Application.</span></span> <span data-ttu-id="1a983-111">A desinstalação do \_ aplicativo de componente também remove os \_ arquivos compartilhados do componente e o arquivo. local do diretório.</span><span class="sxs-lookup"><span data-stu-id="1a983-111">Uninstalling Component\_Application also removes the Component\_Shared files and the .local file from the directory.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="1a983-112">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="1a983-112">Sequence Restrictions</span></span>

<span data-ttu-id="1a983-113">A ação IsolateComponents pode ser usada somente na [tabela InstallUISequence](installuisequence-table.md) e na [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="1a983-113">The IsolateComponents action can be used only in the [InstallUISequence table](installuisequence-table.md) and the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="1a983-114">Essa ação deve vir após a [ação CostInitialize](costinitialize-action.md) e antes da [ação CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="1a983-114">This action must come after the [CostInitialize action](costinitialize-action.md) and before the [CostFinalize action](costfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="1a983-115">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="1a983-115">ActionData Messages</span></span>

<span data-ttu-id="1a983-116">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="1a983-116">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a983-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a983-117">Remarks</span></span>

<span data-ttu-id="1a983-118">Se a coluna condição da ação IsolateComponents for avaliada como true ou for deixada em branco, o instalador isolará todos os componentes listados na [tabela IsolatedComponent](isolatedcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="1a983-118">If the Condition column for the IsolateComponents action evaluates to True, or is left blank, the installer isolates all the components listed in the [IsolatedComponent table](isolatedcomponent-table.md).</span></span> <span data-ttu-id="1a983-119">Se a coluna Condition for avaliada como false, o instalador ignorará a tabela IsolatedComponent e compartilhará os componentes de forma usual.</span><span class="sxs-lookup"><span data-stu-id="1a983-119">If the Condition column evaluates to False, the installer ignores the IsolatedComponent table and shares the components usual.</span></span> <span data-ttu-id="1a983-120">A propriedade [**RedirectedDllSupport**](redirecteddllsupport.md) pode ser usada para condição dessa ação.</span><span class="sxs-lookup"><span data-stu-id="1a983-120">The [**RedirectedDllSupport**](redirecteddllsupport.md) property may be used to condition this action.</span></span> <span data-ttu-id="1a983-121">Para obter mais informações, consulte [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="1a983-121">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



