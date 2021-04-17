---
description: A seção de instalação de um arquivo INF define as etapas do procedimento de instalação.
ms.assetid: 24d40dc6-ac09-4cf8-9229-f81da2925576
title: Exemplo de seção de instalação INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39c8162dbf06b87faf8a1ce432c361a28befca0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754939"
---
# <a name="inf-install-section-example"></a><span data-ttu-id="779a7-103">Exemplo de seção de instalação INF</span><span class="sxs-lookup"><span data-stu-id="779a7-103">INF Install Section Example</span></span>

<span data-ttu-id="779a7-104">A seção de **instalação** de um arquivo inf define as etapas do procedimento de instalação.</span><span class="sxs-lookup"><span data-stu-id="779a7-104">The **Install** section of an INF File defines the steps of the installation procedure.</span></span> <span data-ttu-id="779a7-105">Cada linha de uma seção de **instalação** tem duas partes.</span><span class="sxs-lookup"><span data-stu-id="779a7-105">Each line of an **Install** section has two parts.</span></span> <span data-ttu-id="779a7-106">À esquerda do sinal de igual (=) está a chave.</span><span class="sxs-lookup"><span data-stu-id="779a7-106">On the left of the equals sign (=) is the key.</span></span> <span data-ttu-id="779a7-107">No lado direito, é uma lista de um ou mais títulos de seção.</span><span class="sxs-lookup"><span data-stu-id="779a7-107">On the right hand side, is a list of one or more section titles.</span></span> <span data-ttu-id="779a7-108">A chave especifica o tipo das seções listadas à direita.</span><span class="sxs-lookup"><span data-stu-id="779a7-108">The key specifies the type of the sections that are listed on the right.</span></span> <span data-ttu-id="779a7-109">Para obter uma descrição do formato desta seção, consulte "seções e diretivas de arquivo INF" do Microsoft Windows 2000 Driver Development Kit.</span><span class="sxs-lookup"><span data-stu-id="779a7-109">For a description of this section's format see the "INF File Sections and Directives" of the Microsoft Windows 2000 Driver Development Kit.</span></span>

<span data-ttu-id="779a7-110">Veja a seguir um exemplo de uma seção de **instalação** .</span><span class="sxs-lookup"><span data-stu-id="779a7-110">The following is an example of an **Install** section.</span></span>

``` syntax
[MyInstallSection]
Copyfiles=DataFiles, ProgramFiles
Delfiles=OldFiles
UpdateInis=NewIniInfo
AddReg=NewRegistryInfo, MoreNewRegistryInfo
DelReg=OldRegistryInfo, MoreOldRegistryInfo
```

<span data-ttu-id="779a7-111">Neste exemplo, a chave **CopyFiles** é definida com os valores "DataFiles" e "ProgramFiles".</span><span class="sxs-lookup"><span data-stu-id="779a7-111">In this example the **CopyFiles** key is set to the values "DataFiles" and "ProgramFiles".</span></span> <span data-ttu-id="779a7-112">Isso especifica duas seções de **arquivos de cópia** no arquivo inf que contêm os nomes dos arquivos de origem usados por operações de cópia.</span><span class="sxs-lookup"><span data-stu-id="779a7-112">This specifies two **Copy Files** sections in the INF file that contain the names of the source files used by copying operations.</span></span> <span data-ttu-id="779a7-113">O destino dos arquivos copiados seria especificado em uma seção **DestinationDirs** no arquivo inf.</span><span class="sxs-lookup"><span data-stu-id="779a7-113">The destination for the copied files would be specified in a **DestinationDirs** section in the INF file.</span></span>

<span data-ttu-id="779a7-114">A chave **DelFiles** recebe o valor "OldFiles".</span><span class="sxs-lookup"><span data-stu-id="779a7-114">The **Delfiles** key is given the value "OldFiles".</span></span> <span data-ttu-id="779a7-115">Isso especifica uma seção **Excluir arquivos** que contém informações relevantes para operações de exclusão de arquivos.</span><span class="sxs-lookup"><span data-stu-id="779a7-115">This specifies a **Delete Files** section that contains information relevant to file deletion operations.</span></span>

<span data-ttu-id="779a7-116">A chave **UpdateInis** especifica as seções do **arquivo ini de atualização** que contêm informações sobre a atualização de entradas no arquivo ini.</span><span class="sxs-lookup"><span data-stu-id="779a7-116">The **UpdateInis** key specifies **Update INI File** sections that contain information about updating entries in the INI file.</span></span>

<span data-ttu-id="779a7-117">As chaves **AddReg** e **DelReg** especificam as seções **adicionar registro** e **Excluir registro** que contêm informações sobre como adicionar ou excluir informações do registro.</span><span class="sxs-lookup"><span data-stu-id="779a7-117">The **AddReg** and **DelReg** keys specify **Add Registry** and **Delete Registry** sections that contain information about adding or deleting registry information.</span></span>

 

 



