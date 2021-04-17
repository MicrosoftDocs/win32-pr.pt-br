---
description: A ação InstallODBC instala os drivers, os tradutores e as fontes de dados na tabela ODBCDriver, na tabela ODBCTranslator e na tabela ODBCDataSource.
ms.assetid: fbcf1fdc-5aef-4431-93fe-3ed02748b5ff
title: Ação InstallODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac9becd2a528646805f4201cfb415a6bc61bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812918"
---
# <a name="installodbc-action"></a><span data-ttu-id="a554c-103">Ação InstallODBC</span><span class="sxs-lookup"><span data-stu-id="a554c-103">InstallODBC Action</span></span>

<span data-ttu-id="a554c-104">A ação InstallODBC instala os drivers, os tradutores e as fontes de dados na tabela [ODBCDriver](odbcdriver-table.md), na tabela [ODBCTranslator](odbctranslator-table.md)e na [tabela ODBCDataSource](odbcdatasource-table.md).</span><span class="sxs-lookup"><span data-stu-id="a554c-104">The InstallODBC action installs the drivers, translators, and data sources in the [ODBCDriver Table](odbcdriver-table.md), [ODBCTranslator Table](odbctranslator-table.md), and [ODBCDataSource Table](odbcdatasource-table.md).</span></span> <span data-ttu-id="a554c-105">Se um driver ou tradutor já existir, a ação InstallODBC fará as chamadas SQL necessárias para a instalação.</span><span class="sxs-lookup"><span data-stu-id="a554c-105">If a driver or translator already exists, the InstallODBC action makes SQL calls necessary for the installation.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a554c-106">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="a554c-106">Sequence Restrictions</span></span>

<span data-ttu-id="a554c-107">A ação InstallODBC não copia nem remove arquivos e deve ser posterior a ações que copiam ou removem arquivos.</span><span class="sxs-lookup"><span data-stu-id="a554c-107">The InstallODBC action does not copy or remove files, and must be after actions that copy or remove files.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a554c-108">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="a554c-108">ActionData Messages</span></span>

<span data-ttu-id="a554c-109">A tabela a seguir identifica as mensagens ActionData para cada driver instalado.</span><span class="sxs-lookup"><span data-stu-id="a554c-109">The following table identifies the ActionData messages for each installed driver.</span></span>



| <span data-ttu-id="a554c-110">Campo</span><span class="sxs-lookup"><span data-stu-id="a554c-110">Field</span></span>       | <span data-ttu-id="a554c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a554c-111">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="a554c-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a554c-112">\[1\]</span></span>       | <span data-ttu-id="a554c-113">Descrição do driver.</span><span class="sxs-lookup"><span data-stu-id="a554c-113">Driver description.</span></span> <span data-ttu-id="a554c-114">A chave do driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="a554c-114">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="a554c-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a554c-115">\[2\]</span></span>       | <span data-ttu-id="a554c-116">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="a554c-116">ComponentId.</span></span>                                                             |
| <span data-ttu-id="a554c-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="a554c-117">\[3\]</span></span>       | <span data-ttu-id="a554c-118">Pasta.</span><span class="sxs-lookup"><span data-stu-id="a554c-118">Folder.</span></span>                                                                  |
| <span data-ttu-id="a554c-119">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="a554c-119">\[4, 5, …\]</span></span> | <span data-ttu-id="a554c-120">Pares de atributo e valor de [odbcattribute](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="a554c-120">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

<span data-ttu-id="a554c-121">A tabela a seguir identifica as mensagens ActionData para cada tradutor instalado.</span><span class="sxs-lookup"><span data-stu-id="a554c-121">The following table identifies the ActionData messages for each installed translator.</span></span>



| <span data-ttu-id="a554c-122">Campo</span><span class="sxs-lookup"><span data-stu-id="a554c-122">Field</span></span>       | <span data-ttu-id="a554c-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="a554c-123">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="a554c-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a554c-124">\[1\]</span></span>       | <span data-ttu-id="a554c-125">Descrição do driver.</span><span class="sxs-lookup"><span data-stu-id="a554c-125">Driver description.</span></span> <span data-ttu-id="a554c-126">A chave do driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="a554c-126">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="a554c-127">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a554c-127">\[2\]</span></span>       | <span data-ttu-id="a554c-128">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="a554c-128">ComponentId.</span></span>                                                             |
| <span data-ttu-id="a554c-129">\[3\]</span><span class="sxs-lookup"><span data-stu-id="a554c-129">\[3\]</span></span>       | <span data-ttu-id="a554c-130">Pasta.</span><span class="sxs-lookup"><span data-stu-id="a554c-130">Folder.</span></span>                                                                  |
| <span data-ttu-id="a554c-131">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="a554c-131">\[4, 5, …\]</span></span> | <span data-ttu-id="a554c-132">Pares de atributo e valor de [odbcattribute](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="a554c-132">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

<span data-ttu-id="a554c-133">A tabela a seguir identifica as mensagens ActionData para cada fonte de dados instalada.</span><span class="sxs-lookup"><span data-stu-id="a554c-133">The following table identifies the ActionData messages for each installed data source.</span></span>



| <span data-ttu-id="a554c-134">Campo</span><span class="sxs-lookup"><span data-stu-id="a554c-134">Field</span></span>       | <span data-ttu-id="a554c-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="a554c-135">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="a554c-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a554c-136">\[1\]</span></span>       | <span data-ttu-id="a554c-137">Descrição do driver.</span><span class="sxs-lookup"><span data-stu-id="a554c-137">Driver description.</span></span> <span data-ttu-id="a554c-138">A chave do driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="a554c-138">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="a554c-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a554c-139">\[2\]</span></span>       | <span data-ttu-id="a554c-140">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="a554c-140">ComponentId.</span></span>                                                             |
| <span data-ttu-id="a554c-141">\[3\]</span><span class="sxs-lookup"><span data-stu-id="a554c-141">\[3\]</span></span>       | <span data-ttu-id="a554c-142">Registro: ODBC \_ Add \_ DSN ou ODBC \_ Add \_ Sys \_ DSN.</span><span class="sxs-lookup"><span data-stu-id="a554c-142">Registration: ODBC\_ADD\_DSN or ODBC\_ADD\_SYS\_DSN.</span></span>                     |
| <span data-ttu-id="a554c-143">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="a554c-143">\[4, 5, …\]</span></span> | <span data-ttu-id="a554c-144">Pares de atributo e valor de [odbcattribute](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="a554c-144">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a554c-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="a554c-145">Remarks</span></span>

<span data-ttu-id="a554c-146">O Gerenciador de driver ODBC deve ser criado no pacote do Microsoft Installer e um componente chamado ODBCDriverManager deve ser incluído.</span><span class="sxs-lookup"><span data-stu-id="a554c-146">The ODBC Driver Manager must be authored in the Microsoft Installer package and a component named ODBCDriverManager must be included.</span></span> <span data-ttu-id="a554c-147">O Gerenciador é instalado, se necessário.</span><span class="sxs-lookup"><span data-stu-id="a554c-147">The manager is installed if necessary.</span></span>

<span data-ttu-id="a554c-148">Para renomear o componente, defina uma propriedade chamada ODBCDriverManager como o novo nome do componente.</span><span class="sxs-lookup"><span data-stu-id="a554c-148">To rename the component, set a property named ODBCDriverManager to the new name of the component.</span></span> <span data-ttu-id="a554c-149">Se um Gerenciador de driver ODBC de 64 bits for instalado, o componente que o transporta deve ser nomeado ODBCDriverManager64.</span><span class="sxs-lookup"><span data-stu-id="a554c-149">If a 64-bit ODBC Driver Manager is to be installed, the component that carries it should be named ODBCDriverManager64.</span></span>

-   <span data-ttu-id="a554c-150">A ação InstallODBC consulta a [tabela ODBCDataSource](odbcdatasource-table.md) e a [tabela ODBCSourceAttribute](odbcsourceattribute-table.md) para cada fonte de dados a ser instalada e os atributos da fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="a554c-150">The InstallODBC action queries the [ODBCDataSource Table](odbcdatasource-table.md) and the [ODBCSourceAttribute Table](odbcsourceattribute-table.md) for each data source to be installed, and the attributes of the data source.</span></span>
-   <span data-ttu-id="a554c-151">A ação InstallODBC consulta a [tabela ODBCDriver](odbcdriver-table.md) e a [tabela ODBCTranslator](odbctranslator-table.md) para cada driver e tradutor selecionado para instalação.</span><span class="sxs-lookup"><span data-stu-id="a554c-151">The InstallODBC action queries the [ODBCDriver Table](odbcdriver-table.md) and the [ODBCTranslator Table](odbctranslator-table.md) for each driver and translator that is selected for installation.</span></span>
-   <span data-ttu-id="a554c-152">A ação InstallODBC consulta a [tabela odbcattribute](odbcattribute-table.md) para obter os atributos dos drivers e tradutores.</span><span class="sxs-lookup"><span data-stu-id="a554c-152">The InstallODBC action queries the [ODBCAttribute Table](odbcattribute-table.md) for the attributes of the drivers and translators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a554c-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a554c-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a554c-154">Exemplos de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="a554c-154">Windows Installer Examples</span></span>](windows-installer-examples.md)
</dt> </dl>

 

 



