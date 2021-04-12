---
description: As chaves do registro podem ser gravadas no registro do sistema depois que todos os componentes selecionados e seus arquivos relacionados tiverem sido instalados.
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: Modificando o registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6ff79ce340b0487c179cb37e44dff9f42e4be8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297354"
---
# <a name="modifying-the-registry"></a><span data-ttu-id="9b422-103">Modificando o registro</span><span class="sxs-lookup"><span data-stu-id="9b422-103">Modifying the Registry</span></span>

<span data-ttu-id="9b422-104">As chaves do registro podem ser gravadas no registro do sistema depois que todos os componentes selecionados e seus arquivos relacionados tiverem sido instalados.</span><span class="sxs-lookup"><span data-stu-id="9b422-104">Registry keys can be written to the system registry once all selected components and their related files have been installed.</span></span> <span data-ttu-id="9b422-105">As ações padrão relacionadas à modificação do registro devem ser sequenciadas após as ações padrão de instalação de arquivo, pois as chaves do registro não podem ser gravadas, a menos que o componente e o arquivo correspondentes tenham sido instalados com êxito.</span><span class="sxs-lookup"><span data-stu-id="9b422-105">The standard actions related to modifying the registry must be sequenced after the file installation standard actions because registry keys cannot be written unless the corresponding component and file have been successfully installed.</span></span>

<span data-ttu-id="9b422-106">A [ação RegisterClassInfo](registerclassinfo-action.md) acessa a [tabela de classes](class-table.md) para registrar as informações de classe com dos componentes instalados.</span><span class="sxs-lookup"><span data-stu-id="9b422-106">The [RegisterClassInfo action](registerclassinfo-action.md) accesses the [Class table](class-table.md) to register the COM class information of the installed components.</span></span>

<span data-ttu-id="9b422-107">A [ação RegisterExtensionInfo](registerextensioninfo-action.md) consulta a [tabela de extensão](extension-table.md) e a [tabela de verbos](verb-table.md) e registra as extensões correspondentes e as informações de verbo de comando com o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9b422-107">The [RegisterExtensionInfo action](registerextensioninfo-action.md) queries the [Extension table](extension-table.md) and [Verb table](verb-table.md) and registers the corresponding extensions and command-verb information with the operating system.</span></span>

<span data-ttu-id="9b422-108">A [ação RegisterProgIdInfo](registerprogidinfo-action.md) gerencia o registro de informações de ProgID de OLE com o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9b422-108">The [RegisterProgIdInfo action](registerprogidinfo-action.md) manages the registration of OLE ProgId information with the operating system.</span></span>

<span data-ttu-id="9b422-109">A [ação RegisterMIMEInfo](registermimeinfo-action.md) processa a [tabela MIME](mime-table.md) para registrar a associação entre um tipo de contexto MIME, a extensão de nome de arquivo e o CLSID.</span><span class="sxs-lookup"><span data-stu-id="9b422-109">The [RegisterMIMEInfo action](registermimeinfo-action.md) processes the [MIME table](mime-table.md) to register the association between a MIME context type, the file name extension, and the CLSID.</span></span>

<span data-ttu-id="9b422-110">A [ação WriteRegistryValues](writeregistryvalues-action.md) processa a [tabela do registro](registry-table.md) e grava as chaves para todos os componentes que foram instalados localmente ou para serem executados a partir da origem.</span><span class="sxs-lookup"><span data-stu-id="9b422-110">The [WriteRegistryValues action](writeregistryvalues-action.md) processes the [Registry table](registry-table.md) and writes the keys for all components that have been either installed locally or to run from source.</span></span> <span data-ttu-id="9b422-111">A tabela de registro permite que as chaves sejam gravadas nas seções de **classe HKEY, \_ \_ raiz**, **HKEY \_ Current \_ User**, **HKEY \_ local \_ Machine** e **HKEY \_ Users** Registry.</span><span class="sxs-lookup"><span data-stu-id="9b422-111">The Registry table allows keys to be written to the **HKEY\_CLASSES\_ROOT**, **HKEY\_CURRENT\_USER**, **HKEY\_LOCAL\_MACHINE**, and **HKEY\_USERS** registry hives.</span></span>

<span data-ttu-id="9b422-112">A [ação RemoveRegistryValues](removeregistryvalues-action.md) remove as chaves que foram marcadas para serem excluídas na coluna Name da [tabela de registro](registry-table.md) ou na [tabela RemoveRegistry](removeregistry-table.md).</span><span class="sxs-lookup"><span data-stu-id="9b422-112">The [RemoveRegistryValues action](removeregistryvalues-action.md) removes the keys that have been marked to be deleted in the Name column of the [Registry table](registry-table.md) or the [RemoveRegistry Table](removeregistry-table.md).</span></span>

<span data-ttu-id="9b422-113">A [ação RegisterTypeLibraries](registertypelibraries-action.md) processa a [tabela Typelib](typelib-table.md) e registra as bibliotecas de tipos instaladas com o sistema.</span><span class="sxs-lookup"><span data-stu-id="9b422-113">The [RegisterTypeLibraries action](registertypelibraries-action.md) processes the [TypeLib table](typelib-table.md) and registers the installed type libraries with the system.</span></span>

 

 



