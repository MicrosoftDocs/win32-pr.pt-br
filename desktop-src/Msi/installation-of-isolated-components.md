---
description: Windows Installer executa as seguintes ações durante a instalação de um aplicativo quando o pacote contém componentes isolados. Normalmente, \_ o componente compartilhado é uma DLL que é compartilhada por \_ aplicativo de componente e outros executáveis do cliente.
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: Instalação de componentes isolados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c1b9a7e21c212474701409e887d0afd5517774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647716"
---
# <a name="installation-of-isolated-components"></a><span data-ttu-id="ecda1-104">Instalação de componentes isolados</span><span class="sxs-lookup"><span data-stu-id="ecda1-104">Installation of Isolated Components</span></span>

<span data-ttu-id="ecda1-105">Windows Installer executa as seguintes ações durante a instalação de um aplicativo quando o pacote contém componentes isolados.</span><span class="sxs-lookup"><span data-stu-id="ecda1-105">Windows Installer performs the following actions during installation of an application when the package contains isolated components.</span></span> <span data-ttu-id="ecda1-106">Normalmente, \_ o componente compartilhado é uma DLL que é compartilhada por \_ aplicativo de componente e outros executáveis do cliente.</span><span class="sxs-lookup"><span data-stu-id="ecda1-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="installation"></a><span data-ttu-id="ecda1-107">Instalação</span><span class="sxs-lookup"><span data-stu-id="ecda1-107">Installation</span></span>

-   <span data-ttu-id="ecda1-108">Copie os arquivos do componente \_ compartilhado para a mesma pasta que o \_ aplicativo de componente somente se o aplicativo de componente \_ também estiver sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="ecda1-108">Copy the files of Component\_Shared into the same folder as Component\_Application only if Component\_Application is also being installed.</span></span>
-   <span data-ttu-id="ecda1-109">Crie um arquivo de byte zero com o nome de arquivo curto do arquivo de chave do \_ aplicativo de componente.</span><span class="sxs-lookup"><span data-stu-id="ecda1-109">Create a zero-byte file with the short file name of the key file of Component\_Application.</span></span> <span data-ttu-id="ecda1-110">Localize esse arquivo na mesma pasta que o aplicativo de componente \_ .</span><span class="sxs-lookup"><span data-stu-id="ecda1-110">Locate this file in the same folder as Component\_Application.</span></span> <span data-ttu-id="ecda1-111">Acrescente a extensão. LOCAL para esse nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ecda1-111">Append the extension .LOCAL to this file name.</span></span>
-   <span data-ttu-id="ecda1-112">Aumente o Refcount SharedDLL se o bit msidbComponentAttributesSharedDllRefCount estiver definido na coluna atributos da tabela de [componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="ecda1-112">Increment the SharedDLL refcount if the msidbComponentAttributesSharedDllRefCount bit is set in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="ecda1-113">Registre o \_ aplicativo componente como um cliente do componente \_ compartilhado e registre um caminho de chave apontando para o local compartilhado do componente \_ compartilhado.</span><span class="sxs-lookup"><span data-stu-id="ecda1-113">Register Component\_Application as a client of Component\_Shared and register a key path pointing to the shared location of Component\_Shared.</span></span>
-   <span data-ttu-id="ecda1-114">Instale todos os recursos do aplicativo de componente \_ como de costume.</span><span class="sxs-lookup"><span data-stu-id="ecda1-114">Install all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="ecda1-115">Se o componente \_ compartilhado ou seu arquivo de chave já estiver instalado no computador, não copie os arquivos para o local compartilhado do componente \_ compartilhado.</span><span class="sxs-lookup"><span data-stu-id="ecda1-115">If Component\_Shared or its key file is already installed on the computer do not copy files to the shared location of Component\_Shared.</span></span>

<span data-ttu-id="ecda1-116">Se \_ o componente compartilhado ou seu arquivo de chave ainda não estiver instalado no computador:</span><span class="sxs-lookup"><span data-stu-id="ecda1-116">If Component\_Shared or its key file is not yet installed on the computer:</span></span>

-   <span data-ttu-id="ecda1-117">Copie os arquivos do componente \_ compartilhado para o local compartilhado.</span><span class="sxs-lookup"><span data-stu-id="ecda1-117">Copy the files of Component\_Shared to the shared location.</span></span>
-   <span data-ttu-id="ecda1-118">Processar todas as ações de instalação para componente \_ compartilhado.</span><span class="sxs-lookup"><span data-stu-id="ecda1-118">Process all install actions for Component\_Shared.</span></span>
-   <span data-ttu-id="ecda1-119">Se o componente \_ compartilhado for um componente com, registre o caminho com completo, de modo que a sintaxe \[ $Component \] e \[ \# FileKey \] apontem para o local compartilhado do componente \_ compartilhado.</span><span class="sxs-lookup"><span data-stu-id="ecda1-119">If Component\_Shared is a COM component, register the full COM path such that the syntax \[$Component\] and \[\#FileKey\] point to the shared location of Component\_Shared.</span></span>

 

 



