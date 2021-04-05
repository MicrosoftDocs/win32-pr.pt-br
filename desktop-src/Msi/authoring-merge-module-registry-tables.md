---
description: Use tabelas de registro de módulo de mesclagem de acordo com o tipo de informações de registro.
ms.assetid: 091429ff-a8f4-4e1b-929f-1559cd173c3d
title: Criando tabelas de registro do módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10e31ac82d190c87019da5bc77408b58122a523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921496"
---
# <a name="authoring-merge-module-registry-tables"></a><span data-ttu-id="12975-103">Criando tabelas de registro do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="12975-103">Authoring Merge Module Registry Tables</span></span>

<span data-ttu-id="12975-104">Use tabelas de registro de módulo de mesclagem de acordo com o tipo de informações de registro.</span><span class="sxs-lookup"><span data-stu-id="12975-104">Use Merge Module Registry tables according to the type of registry information.</span></span>

## <a name="typelib-class-appid-progid-extension-verb-or-mime-tables"></a><span data-ttu-id="12975-105">Tabelas TypeLib, Class, AppId, ProgId, extensão, verbo ou MIME</span><span class="sxs-lookup"><span data-stu-id="12975-105">TypeLib, Class, AppId, ProgId, Extension, Verb, or MIME Tables</span></span>

<span data-ttu-id="12975-106">Para bibliotecas de tipos, classes, extensões e verbos, crie informações de registro nas tabelas [TypeLib](typelib-table.md), [Class](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), de [extensão](extension-table.md), [verbo](verb-table.md)ou [MIME](mime-table.md) do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="12975-106">For type libraries, classes, extensions, and verbs, author registry information into the merge module's [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md), or [MIME](mime-table.md) tables.</span></span> <span data-ttu-id="12975-107">Se você usar a [tabela de registro](registry-table.md) para adicionar essas informações, o Windows 2000 não poderá fornecer anúncio em todo o sistema para esses componentes.</span><span class="sxs-lookup"><span data-stu-id="12975-107">If you use the [Registry table](registry-table.md) to add this information, Windows 2000 cannot provide system-wide advertisement for these components.</span></span>

<span data-ttu-id="12975-108">Os autores do módulo de mesclagem podem decidir não registrar usando a tabela de classes pelos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="12975-108">Merge module authors may decide not to register using the Class table for the following reasons:</span></span>

-   <span data-ttu-id="12975-109">Para ser registrado pela tabela de classes, o arquivo deve ser o caminho Keydo seu componente.</span><span class="sxs-lookup"><span data-stu-id="12975-109">To be registered by the Class table, the file has to be the KeyPath of its component.</span></span> <span data-ttu-id="12975-110">Isso pode exigir uma alteração inaceitável na organização dos componentes.</span><span class="sxs-lookup"><span data-stu-id="12975-110">This may require an unacceptable change in the organization of components.</span></span>
-   <span data-ttu-id="12975-111">Uma chamada COM pode disparar uma tentativa do instalador de reinstalar uma classe anunciada.</span><span class="sxs-lookup"><span data-stu-id="12975-111">A COM call may trigger an installer attempt to reinstall an advertised class.</span></span> <span data-ttu-id="12975-112">Os autores podem decidir não registrar uma classe usando a tabela de classes para evitar disparar uma reinstalação quando o computador cliente não oferecer suporte a uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="12975-112">Authors may decide not to register a class using the Class table in order to avoid triggering a reinstallation when the client computer does not support a user interface.</span></span>

## <a name="registry-table"></a><span data-ttu-id="12975-113">Tabela do registro</span><span class="sxs-lookup"><span data-stu-id="12975-113">Registry Table</span></span>

<span data-ttu-id="12975-114">Use a tabela de registro para adicionar informações de registro que não podem ser criadas em tabelas TypeLib, Class, AppId, ProgId, extensão, verbo ou MIME.</span><span class="sxs-lookup"><span data-stu-id="12975-114">Use the Registry table to add registry information that cannot be authored into the TypeLib, Class, AppId, ProgId, Extension, Verb, or MIME tables.</span></span> <span data-ttu-id="12975-115">O Windows 2000 não pode fornecer anúncio em todo o sistema para componentes que usam a tabela de registro.</span><span class="sxs-lookup"><span data-stu-id="12975-115">Windows 2000 cannot provide system-wide advertisement for components that use the Registry table.</span></span>

<span data-ttu-id="12975-116">Ao criar a tabela do registro, consulte caminhos de arquivo usando o \[ \# arquivo \] ou \[ ! \]Formato de arquivo em vez \[ de \] nome do diretório.</span><span class="sxs-lookup"><span data-stu-id="12975-116">When authoring the Registry table, refer to file paths using the \[\#File\] or \[!File\] format rather than as \[Directory\]Filename.</span></span> <span data-ttu-id="12975-117">O último formato não oferece suporte à instalação de execução da origem.</span><span class="sxs-lookup"><span data-stu-id="12975-117">The latter format does not support run-from-source installation.</span></span> <span data-ttu-id="12975-118">O formato anterior também torna os arquivos ausentes e os componentes com falha mais fáceis de detectar.</span><span class="sxs-lookup"><span data-stu-id="12975-118">The former format also makes missing files and faulty components easier to detect.</span></span>

<span data-ttu-id="12975-119">É necessário ter cuidado ao usar texto formatado na coluna de chave da tabela de registro.</span><span class="sxs-lookup"><span data-stu-id="12975-119">Care is needed when using formatted text in the Key column of the Registry table.</span></span> <span data-ttu-id="12975-120">Como Windows Installer não reinstala componentes que já estão instalados, usar texto formatado nesse campo pode fazer com que as chaves do registro sejam deixadas para trás na remoção do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="12975-120">Because Windows Installer does not reinstall components that are already installed, using formatted text in this field may cause registry keys to be left behind on application removal.</span></span>

## <a name="selfreg-table"></a><span data-ttu-id="12975-121">Tabela SelfReg</span><span class="sxs-lookup"><span data-stu-id="12975-121">SelfReg Table</span></span>

<span data-ttu-id="12975-122">Não é recomendável usar a tabela SelfReg.</span><span class="sxs-lookup"><span data-stu-id="12975-122">Using the SelfReg table is not recommended.</span></span> <span data-ttu-id="12975-123">Para obter uma lista de motivos para não usar o auto-registro, consulte a [tabela selfreg](selfreg-table.md).</span><span class="sxs-lookup"><span data-stu-id="12975-123">For a list of reasons for not using self-registration, see [SelfReg table](selfreg-table.md).</span></span> <span data-ttu-id="12975-124">Você deve usar as tabelas TypeLib, Class, AppId, ProgId, extensão, verbo e MIME sempre que possível e a tabela de registro em todos os outros casos.</span><span class="sxs-lookup"><span data-stu-id="12975-124">You should use the TypeLib, Class, AppId, ProgId, Extension, Verb, and MIME tables where possible instead and the Registry table in all other cases.</span></span>

 

 



