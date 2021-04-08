---
description: Windows Installer executa as seguintes ações durante a reinstalação de um aplicativo quando o pacote contém componentes isolados. Normalmente, \_ o componente compartilhado é uma DLL que é compartilhada por \_ aplicativo de componente e outros executáveis do cliente.
ms.assetid: 65909b47-dc09-4e9a-920a-9cb3f55b2e67
title: Reinstalação de componentes isolados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad1c7fb53eb09e96882209f7738e95be9b4a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828244"
---
# <a name="reinstallation-of-isolated-components"></a><span data-ttu-id="b8905-104">Reinstalação de componentes isolados</span><span class="sxs-lookup"><span data-stu-id="b8905-104">Reinstallation of Isolated Components</span></span>

<span data-ttu-id="b8905-105">Windows Installer executa as seguintes ações durante a reinstalação de um aplicativo quando o pacote contém componentes isolados.</span><span class="sxs-lookup"><span data-stu-id="b8905-105">Windows Installer performs the following actions during reinstallation of an application when the package contains isolated components.</span></span> <span data-ttu-id="b8905-106">Normalmente, \_ o componente compartilhado é uma DLL que é compartilhada por \_ aplicativo de componente e outros executáveis do cliente.</span><span class="sxs-lookup"><span data-stu-id="b8905-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="reinstallation"></a><span data-ttu-id="b8905-107">Reinstalação</span><span class="sxs-lookup"><span data-stu-id="b8905-107">Reinstallation</span></span>

-   <span data-ttu-id="b8905-108">Reinstale os arquivos do componente \_ compartilhado na mesma pasta que o aplicativo de componente \_ somente se o aplicativo de componente \_ também estiver sendo reinstalado.</span><span class="sxs-lookup"><span data-stu-id="b8905-108">Reinstall of the files of Component\_Shared into the same folder as Component\_Application only if Component\_Application is also being reinstalled.</span></span>
-   <span data-ttu-id="b8905-109">Não incrementar a lista de componentes compartilhados do cliente \_ e não incrementar a contagem de SharedDLL.</span><span class="sxs-lookup"><span data-stu-id="b8905-109">Do not increment the client list of Component\_Shared and do not increment the SharedDLL count.</span></span>
-   <span data-ttu-id="b8905-110">Recrie o arquivo de byte zero com o nome de arquivo curto do arquivo de chave do \_ aplicativo de componente.</span><span class="sxs-lookup"><span data-stu-id="b8905-110">Recreate the zero-byte file with the short file name of the key file of Component\_Application.</span></span> <span data-ttu-id="b8905-111">Esse arquivo deve estar localizado na mesma pasta que \_ o aplicativo de componente e ter a extensão. LOCAL.</span><span class="sxs-lookup"><span data-stu-id="b8905-111">This file must be located in the same folder as Component\_Application and have the extension .LOCAL.</span></span>
-   <span data-ttu-id="b8905-112">Reinstale todos os recursos do aplicativo de componente \_ como de costume.</span><span class="sxs-lookup"><span data-stu-id="b8905-112">Reinstall all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="b8905-113">Se o Refcount SharedDLL para o componente \_ compartilhado for maior que 1, ou se outros produtos permanecerem na lista de componentes \_ compartilhados do cliente:</span><span class="sxs-lookup"><span data-stu-id="b8905-113">If the SharedDLL refcount for Component\_Shared is more than 1, or if other products remain on the client list of Component\_Shared:</span></span>

-   <span data-ttu-id="b8905-114">Reinstale nenhum arquivo no local compartilhado do componente \_ compartilhado.</span><span class="sxs-lookup"><span data-stu-id="b8905-114">Reinstall no files to the shared location of Component\_Shared.</span></span>

<span data-ttu-id="b8905-115">Se o Refcount SharedDLL para o componente \_ compartilhado for igual a 1 ou se não houver nenhum outro cliente restante do componente \_ compartilhado:</span><span class="sxs-lookup"><span data-stu-id="b8905-115">If the SharedDLL refcount for Component\_Shared equals 1, or if there are no other remaining clients of Component\_Shared:</span></span>

-   <span data-ttu-id="b8905-116">Reinstale os arquivos do componente \_ compartilhado no local compartilhado usando as [regras de controle de versão de arquivo](file-versioning-rules.md).</span><span class="sxs-lookup"><span data-stu-id="b8905-116">Reinstall of the files of Component\_Shared into the shared location using the [File Versioning Rules](file-versioning-rules.md).</span></span>
-   <span data-ttu-id="b8905-117">Processar todas as ações de reinstalação para componente \_ compartilhado.</span><span class="sxs-lookup"><span data-stu-id="b8905-117">Process all reinstall actions for Component\_Shared.</span></span>
-   <span data-ttu-id="b8905-118">Se o componente \_ compartilhado for um componente com, registre o caminho com completo, de modo que as sintaxes do instalador \[ $Component \] e \[ \# FileKey \] apontem para o local compartilhado do componente \_ compartilhado.</span><span class="sxs-lookup"><span data-stu-id="b8905-118">If Component\_Shared is a COM component, register the full COM path such that the installer syntaxes \[$Component\] and \[\#FileKey\] point to the shared location of Component\_Shared.</span></span>

 

 



