---
description: A definição de interface a seguir é fornecida como um padrão que pode ser seguido durante o desenvolvimento de um provedor de serviço de cartão inteligente.
ms.assetid: 68cc0bbe-ce8e-4da1-b907-596caa95a39c
title: Interface ISCardFileAccess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: fcfcdc75bcf10b922a242574bfabe267c949fa52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828959"
---
# <a name="iscardfileaccess-interface"></a><span data-ttu-id="be246-103">Interface ISCardFileAccess</span><span class="sxs-lookup"><span data-stu-id="be246-103">ISCardFileAccess interface</span></span>

<span data-ttu-id="be246-104">\[A interface **ISCardFileAccess** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="be246-104">\[The **ISCardFileAccess** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="be246-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="be246-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="be246-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="be246-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="be246-107">A definição de interface a seguir é fornecida como um padrão que pode ser seguido durante o desenvolvimento de um [*provedor de serviço*](../secgloss/c-gly.md)de [*cartão inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="be246-107">The following interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="be246-108">A interface **ISCardFileAccess** pode ser usada para implementar uma interface de alto nível para um sistema de arquivos baseado em cartão com um sistema de arquivos de cartão subjacente com base na estrutura definida no ISO/IEC 7816-4.</span><span class="sxs-lookup"><span data-stu-id="be246-108">The **ISCardFileAccess** interface can be used to implement a high-level interface to a card-based file system with an underlying card file system based on the structure defined in ISO/IEC 7816-4.</span></span> <span data-ttu-id="be246-109">Outras implementações são possíveis, mas isso deve ser o mais comum.</span><span class="sxs-lookup"><span data-stu-id="be246-109">Other implementations are possible, but this is expected to be the most common.</span></span>

<span data-ttu-id="be246-110">A interface **ISCardFileAccess** pode ser usada para expor entidades do sistema de arquivos de uma maneira muito familiar para os desenvolvedores de aplicativos no ambiente do PC.</span><span class="sxs-lookup"><span data-stu-id="be246-110">The **ISCardFileAccess** interface can be used to expose file system entities in a manner very familiar to application developers in the PC environment.</span></span> <span data-ttu-id="be246-111">Ele fornece mecanismos para localizar arquivos específicos e executar operações comuns, como seleção, leitura, gravação, criação e exclusão.</span><span class="sxs-lookup"><span data-stu-id="be246-111">It provides mechanisms for locating specific files and performing common operations such as selecting, reading, writing, creating and deleting.</span></span> <span data-ttu-id="be246-112">Ele encapsula e mascara muitos dos detalhes de baixo nível envolvidos na execução dessas operações no nível do cartão.</span><span class="sxs-lookup"><span data-stu-id="be246-112">It encapsulates and masks much of the low-level detail involved in performing these operations at the card level.</span></span>

<span data-ttu-id="be246-113">Veja a seguir um uso típico da interface **ISCardFileAccess** .</span><span class="sxs-lookup"><span data-stu-id="be246-113">Following is a typical use of the **ISCardFileAccess** interface.</span></span> <span data-ttu-id="be246-114">Nesse caso, a interface **ISCardFileAccess** é usada para selecionar, abrir e gravar em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="be246-114">In this case, the **ISCardFileAccess** interface is used to select, open, and write to a file.</span></span>

<span data-ttu-id="be246-115">**Para gravar em um arquivo**</span><span class="sxs-lookup"><span data-stu-id="be246-115">**To write to a file**</span></span>

1.  <span data-ttu-id="be246-116">Chame [**ISCardManage:: createfileaccess**](iscardmanage-createfileaccess.md) para criar uma interface **ISCardFileAccess** .</span><span class="sxs-lookup"><span data-stu-id="be246-116">Call [**ISCardManage::CreateFileAccess**](iscardmanage-createfileaccess.md) to create an **ISCardFileAccess** interface.</span></span>
2.  <span data-ttu-id="be246-117">Chame [**Open**](iscardfileaccess-open.md) para selecionar e abrir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="be246-117">Call [**Open**](iscardfileaccess-open.md) to select and open the file.</span></span>
3.  <span data-ttu-id="be246-118">Chamar [**gravação**](iscardfileaccess-write.md).</span><span class="sxs-lookup"><span data-stu-id="be246-118">Call [**Write**](iscardfileaccess-write.md).</span></span>
4.  <span data-ttu-id="be246-119">Chame [**fechar**](iscardfileaccess-close.md).</span><span class="sxs-lookup"><span data-stu-id="be246-119">Call [**Close**](iscardfileaccess-close.md).</span></span>
5.  <span data-ttu-id="be246-120">Libere a interface **ISCardFileAccess** .</span><span class="sxs-lookup"><span data-stu-id="be246-120">Release the **ISCardFileAccess** interface.</span></span>

## <a name="members"></a><span data-ttu-id="be246-121">Membros</span><span class="sxs-lookup"><span data-stu-id="be246-121">Members</span></span>

<span data-ttu-id="be246-122">A interface **ISCardFileAccess** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="be246-122">The **ISCardFileAccess** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="be246-123">**ISCardFileAccess** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="be246-123">**ISCardFileAccess** also has these types of members:</span></span>

-   [<span data-ttu-id="be246-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="be246-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="be246-125">Métodos</span><span class="sxs-lookup"><span data-stu-id="be246-125">Methods</span></span>

<span data-ttu-id="be246-126">A interface **ISCardFileAccess** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="be246-126">The **ISCardFileAccess** interface has these methods.</span></span>



| <span data-ttu-id="be246-127">Método</span><span class="sxs-lookup"><span data-stu-id="be246-127">Method</span></span>                                                              | <span data-ttu-id="be246-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="be246-128">Description</span></span>                                                                                                                                  |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be246-129">**ChangeDir**</span><span class="sxs-lookup"><span data-stu-id="be246-129">**ChangeDir**</span></span>](iscardfileaccess-changedir.md)                     | <span data-ttu-id="be246-130">Altera o diretório do cartão inteligente atual para o novo diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="be246-130">Changes the current smart card directory to the new specified directory.</span></span><br/>                                                          |
| [<span data-ttu-id="be246-131">**Inclui**</span><span class="sxs-lookup"><span data-stu-id="be246-131">**Close**</span></span>](iscardfileaccess-close.md)                             | <span data-ttu-id="be246-132">Fecha o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="be246-132">Closes the specified file.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="be246-133">**Criada**</span><span class="sxs-lookup"><span data-stu-id="be246-133">**Create**</span></span>](iscardfileaccess-create.md)                           | <span data-ttu-id="be246-134">Cria um arquivo em um determinado local dentro do sistema de arquivos ICC.</span><span class="sxs-lookup"><span data-stu-id="be246-134">Creates a file at a given location within the ICC file system.</span></span><br/>                                                                    |
| [<span data-ttu-id="be246-135">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="be246-135">**Delete**</span></span>](iscardfileaccess-delete.md)                           | <span data-ttu-id="be246-136">Exclui um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="be246-136">Deletes a specified file.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="be246-137">**Diretório**</span><span class="sxs-lookup"><span data-stu-id="be246-137">**Directory**</span></span>](iscardfileaccess-directory.md)                     | <span data-ttu-id="be246-138">Recupera uma lista de arquivos.</span><span class="sxs-lookup"><span data-stu-id="be246-138">Retrieves a list of files.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="be246-139">**GetCurrentDir**</span><span class="sxs-lookup"><span data-stu-id="be246-139">**GetCurrentDir**</span></span>](iscardfileaccess-getcurrentdir.md)             | <span data-ttu-id="be246-140">Retorna um caminho absoluto para o diretório selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="be246-140">Returns an absolute path to the currently selected directory.</span></span><br/>                                                                     |
| [<span data-ttu-id="be246-141">**GetFileCapabilities**</span><span class="sxs-lookup"><span data-stu-id="be246-141">**GetFileCapabilities**</span></span>](iscardfileaccess-getfilecapabilities.md) | <span data-ttu-id="be246-142">Recupera recursos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="be246-142">Retrieves file capabilities.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="be246-143">**GetProperties**</span><span class="sxs-lookup"><span data-stu-id="be246-143">**GetProperties**</span></span>](iscardfileaccess-getproperties.md)             | <span data-ttu-id="be246-144">Recupera os dados primitivos referenciados por marcas para o objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="be246-144">Retrieves the primitive data referred by tags for the specified object.</span></span><br/>                                                           |
| [<span data-ttu-id="be246-145">**Invalidar**</span><span class="sxs-lookup"><span data-stu-id="be246-145">**Invalidate**</span></span>](iscardfileaccess-invalidate.md)                   | <span data-ttu-id="be246-146">Torna o arquivo especificado inválido.</span><span class="sxs-lookup"><span data-stu-id="be246-146">Makes the specified file not valid.</span></span><br/>                                                                                               |
| [<span data-ttu-id="be246-147">**Abrir**</span><span class="sxs-lookup"><span data-stu-id="be246-147">**Open**</span></span>](iscardfileaccess-open.md)                               | <span data-ttu-id="be246-148">Abre o arquivo especificado para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="be246-148">Opens the specified file for further use.</span></span><br/>                                                                                         |
| [<span data-ttu-id="be246-149">**Ler**</span><span class="sxs-lookup"><span data-stu-id="be246-149">**Read**</span></span>](iscardfileaccess-read.md)                               | <span data-ttu-id="be246-150">Lê e retorna os dados especificados de um determinado arquivo.</span><span class="sxs-lookup"><span data-stu-id="be246-150">Reads and returns the specified data from a given file.</span></span><br/>                                                                           |
| [<span data-ttu-id="be246-151">**Rehabilitate**</span><span class="sxs-lookup"><span data-stu-id="be246-151">**Rehabilitate**</span></span>](iscardfileaccess-rehabilitate.md)               | <span data-ttu-id="be246-152">Cria um arquivo (EF ou DF), que anteriormente não é válido usando o comando Invalidate, acessível pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="be246-152">Makes a file (EF or DF), which has been previously made not valid by using the Invalidate command, accessible by the application.</span></span><br/> |
| [<span data-ttu-id="be246-153">**Seek**</span><span class="sxs-lookup"><span data-stu-id="be246-153">**Seek**</span></span>](iscardfileaccess-seek.md)                               | <span data-ttu-id="be246-154">Seleciona o objeto do qual a permissão de leitura/gravação será feita.</span><span class="sxs-lookup"><span data-stu-id="be246-154">Selects the object from which read/write permission will be done.</span></span><br/>                                                                 |
| [<span data-ttu-id="be246-155">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="be246-155">**SetProperties**</span></span>](iscardfileaccess-setproperties.md)             | <span data-ttu-id="be246-156">Define os dados primitivos referenciados por marcas para o objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="be246-156">Sets the primitive data referred by tags for the specified object.</span></span><br/>                                                                |
| [<span data-ttu-id="be246-157">**Gravar**</span><span class="sxs-lookup"><span data-stu-id="be246-157">**Write**</span></span>](iscardfileaccess-write.md)                             | <span data-ttu-id="be246-158">Grava dados em um arquivo aberto atual.</span><span class="sxs-lookup"><span data-stu-id="be246-158">Writes data to a current opened file.</span></span><br/>                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="be246-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be246-159">Requirements</span></span>



| <span data-ttu-id="be246-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="be246-160">Requirement</span></span> | <span data-ttu-id="be246-161">Valor</span><span class="sxs-lookup"><span data-stu-id="be246-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="be246-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be246-162">Minimum supported client</span></span><br/> | <span data-ttu-id="be246-163">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="be246-163">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="be246-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be246-164">Minimum supported server</span></span><br/> | <span data-ttu-id="be246-165">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="be246-165">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="be246-166">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="be246-166">End of client support</span></span><br/>    | <span data-ttu-id="be246-167">Windows XP</span><span class="sxs-lookup"><span data-stu-id="be246-167">Windows XP</span></span><br/>                                |
| <span data-ttu-id="be246-168">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="be246-168">End of server support</span></span><br/>    | <span data-ttu-id="be246-169">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="be246-169">Windows Server 2003</span></span><br/>                       |



 

 
