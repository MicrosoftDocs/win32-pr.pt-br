---
description: Para reproduzir o exemplo, você precisa copiar ou criar com uma ferramenta de software, um arquivo de banco de dados Windows Installer.
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: Importando um banco de dados em branco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b654b0de118013e8f211a9b06e896cc3f486faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170426"
---
# <a name="importing-a-blank-database"></a><span data-ttu-id="f0df4-103">Importando um banco de dados em branco</span><span class="sxs-lookup"><span data-stu-id="f0df4-103">Importing a Blank Database</span></span>

<span data-ttu-id="f0df4-104">Para reproduzir o exemplo, você precisa copiar ou criar com uma ferramenta de software, um arquivo de banco de dados Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f0df4-104">To reproduce the sample you need to copy, or create with a software tool, a Windows Installer database file.</span></span> <span data-ttu-id="f0df4-105">Um banco de dados de instalação totalmente em branco, Schema.msi, é fornecido com os [componentes de SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="f0df4-105">A totally blank installation database, Schema.msi, is provided with the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="f0df4-106">O SDK também fornece um banco de dados parcialmente em branco, uisample.msi, que contém as tabelas de sequência sugeridas e os requisitos necessários para uma interface de usuário simples.</span><span class="sxs-lookup"><span data-stu-id="f0df4-106">The SDK also provides a partially blank database, uisample.msi, that contains the suggested sequence tables and data required for a simple user interface.</span></span> <span data-ttu-id="f0df4-107">Faça uma cópia do uisample.msi e mova-o para o mesmo diretório que contém a pasta do bloco de notas que você criou no [planejamento da instalação](planning-the-installation.md).</span><span class="sxs-lookup"><span data-stu-id="f0df4-107">Make a copy of uisample.msi and move it into the same directory containing the Notepad folder you created in [Planning the Installation](planning-the-installation.md).</span></span> <span data-ttu-id="f0df4-108">Renomeie o arquivo MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="f0df4-108">Rename the file MNP2000.msi.</span></span> <span data-ttu-id="f0df4-109">O arquivo de banco de dados de instalação e os arquivos de origem devem estar localizados na raiz do mesmo diretório.</span><span class="sxs-lookup"><span data-stu-id="f0df4-109">The installation database file and the source files must both be located at the root of the same directory.</span></span> <span data-ttu-id="f0df4-110">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f0df4-110">For example:</span></span>

<span data-ttu-id="f0df4-111">C: \\MNP2000.msi de exemplo \\</span><span class="sxs-lookup"><span data-stu-id="f0df4-111">C:\\Sample\\MNP2000.msi</span></span>

<span data-ttu-id="f0df4-112">C: \\ bloco de notas de exemplo </span><span class="sxs-lookup"><span data-stu-id="f0df4-112">C:\\Sample\\Notepad</span></span>\\\\

<span data-ttu-id="f0df4-113">Se você não usar Uisample.msi, deverá obter um banco de dados em branco, como Schema.msi e inserir informações para a instalação usando uma ferramenta de edição de banco de dados, como o orca, que é fornecido com o SDK ou outro editor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f0df4-113">If you do not use Uisample.msi, then you must obtain a blank database, such as Schema.msi, and enter information for the installation using a database editing tool such as Orca, which is provided with the SDK, or another database editor.</span></span>

[<span data-ttu-id="f0df4-114">Continuar</span><span class="sxs-lookup"><span data-stu-id="f0df4-114">Continue</span></span>](specifying-directory-structure.md)

 

 



