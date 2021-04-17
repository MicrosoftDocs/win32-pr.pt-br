---
description: Windows Installer executa as seguintes ações durante a remoção de um aplicativo quando o pacote contém componentes isolados. Normalmente, \_ o componente compartilhado é uma DLL que é compartilhada por \_ aplicativo de componente e outros executáveis do cliente.
ms.assetid: 26343a01-9a06-43d5-bbe3-959faf51739d
title: Remoção de componentes isolados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf19769067230b82f68a35f7b9fbedcd1c56440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751423"
---
# <a name="removal-of-isolated-components"></a><span data-ttu-id="f5c40-104">Remoção de componentes isolados</span><span class="sxs-lookup"><span data-stu-id="f5c40-104">Removal of Isolated Components</span></span>

<span data-ttu-id="f5c40-105">Windows Installer executa as seguintes ações durante a remoção de um aplicativo quando o pacote contém componentes isolados.</span><span class="sxs-lookup"><span data-stu-id="f5c40-105">Windows Installer performs the following actions during the removal of an application when the package contains isolated components.</span></span> <span data-ttu-id="f5c40-106">Normalmente, \_ o componente compartilhado é uma DLL que é compartilhada por \_ aplicativo de componente e outros executáveis do cliente.</span><span class="sxs-lookup"><span data-stu-id="f5c40-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="uninstall"></a><span data-ttu-id="f5c40-107">Desinstalar</span><span class="sxs-lookup"><span data-stu-id="f5c40-107">Uninstall</span></span>

-   <span data-ttu-id="f5c40-108">Remova os arquivos do componente \_ compartilhado da pasta que contém o \_ aplicativo de componente somente se o aplicativo de componente \_ também estiver sendo removido.</span><span class="sxs-lookup"><span data-stu-id="f5c40-108">Remove the files of Component\_Shared from the folder containing Component\_Application only if Component\_Application is also being removed.</span></span>
-   <span data-ttu-id="f5c40-109">Se o bit msidbComponentAttributesSharedDllRefCount for definido na [tabela de componentes](component-table.md) , reduza o Refcount SharedDLL.</span><span class="sxs-lookup"><span data-stu-id="f5c40-109">If the msidbComponentAttributesSharedDllRefCount bit is set in the [Component table](component-table.md) decrement the SharedDLL refcount.</span></span>
-   <span data-ttu-id="f5c40-110">Remova o. Arquivo de byte zero LOCAL da pasta que contém o \_ aplicativo de componente.</span><span class="sxs-lookup"><span data-stu-id="f5c40-110">Remove the .LOCAL zero-byte file from the folder containing Component\_Application.</span></span>
-   <span data-ttu-id="f5c40-111">Remover aplicativo de componente \_ da lista de clientes do componente \_ compartilhado.</span><span class="sxs-lookup"><span data-stu-id="f5c40-111">Remove Component\_Application from the client list of Component\_Shared.</span></span>
-   <span data-ttu-id="f5c40-112">Remova todos os recursos do aplicativo de componente \_ como de costume.</span><span class="sxs-lookup"><span data-stu-id="f5c40-112">Remove all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="f5c40-113">Se houver outros produtos restantes na lista de clientes do componente \_ compartilhado:</span><span class="sxs-lookup"><span data-stu-id="f5c40-113">If there are other products remaining on the client list of Component\_Shared:</span></span>

-   <span data-ttu-id="f5c40-114">Não remova nenhum arquivo do local compartilhado do componente \_ compartilhado.</span><span class="sxs-lookup"><span data-stu-id="f5c40-114">Remove no files from the shared location of Component\_Shared.</span></span>

<span data-ttu-id="f5c40-115">Se o Refcount SharedDLL para o componente \_ compartilhado for 0 depois de ser decrementado, ou se não houver outros clientes restantes do componente \_ compartilhado:</span><span class="sxs-lookup"><span data-stu-id="f5c40-115">If the SharedDLL refcount for Component\_Shared is 0 after being decremented, or if there are no other remaining clients of Component\_Shared:</span></span>

-   <span data-ttu-id="f5c40-116">Remova os arquivos do componente \_ compartilhado do local compartilhado.</span><span class="sxs-lookup"><span data-stu-id="f5c40-116">Remove the files of Component\_Shared from the shared location.</span></span>
-   <span data-ttu-id="f5c40-117">Processar todas as ações de desinstalação com relação a esse componente.</span><span class="sxs-lookup"><span data-stu-id="f5c40-117">Process all uninstall actions with respect to this component.</span></span>

 

 



