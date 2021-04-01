---
description: Para determinar a página de código de um banco de dados, chame MsiDatabaseExport com hDatabase definido como o identificador do banco de dados e szTableName definido como \_ ForceCodepage.
ms.assetid: afa3fbd9-9f54-4f72-ab5d-cb0dbbd9946c
title: Determinando a página de código de um banco de dados de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212978cbce0e73ae495a0ed10ea9070cce6bd374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829004"
---
# <a name="determining-an-installation-databases-code-page"></a><span data-ttu-id="9c8a6-103">Determinando a página de código de um banco de dados de instalação</span><span class="sxs-lookup"><span data-stu-id="9c8a6-103">Determining an Installation Database's Code Page</span></span>

<span data-ttu-id="9c8a6-104">Para determinar a página de código de um banco de dados, chame [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) com *hDatabase* definido como o identificador do banco de dados e *szTableName* definido como \_ ForceCodepage.</span><span class="sxs-lookup"><span data-stu-id="9c8a6-104">To determine the code page of a database, call [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) with *hDatabase* set to the handle of the database and *szTableName* set to \_ForceCodepage.</span></span> <span data-ttu-id="9c8a6-105">Isso exporta um arquivo de texto com uma extensão. IDT.</span><span class="sxs-lookup"><span data-stu-id="9c8a6-105">This exports a text file with an .idt extension.</span></span> <span data-ttu-id="9c8a6-106">As duas primeiras linhas desse arquivo estão em branco.</span><span class="sxs-lookup"><span data-stu-id="9c8a6-106">The first two lines of this file are blank.</span></span> <span data-ttu-id="9c8a6-107">A terceira linha é o número da página de código ANSI, seguido por uma guia, seguida pelo nome \_ ForceCodepage.</span><span class="sxs-lookup"><span data-stu-id="9c8a6-107">The third line is the ANSI code page number, followed by a tab, followed by the name \_ForceCodepage.</span></span> <span data-ttu-id="9c8a6-108">Consulte também [manipulação de página de código de tabelas importadas e exportadas](code-page-handling-of-imported-and-exported-tables.md).</span><span class="sxs-lookup"><span data-stu-id="9c8a6-108">See also [Code Page Handling of Imported and Exported Tables](code-page-handling-of-imported-and-exported-tables.md).</span></span>

<span data-ttu-id="9c8a6-109">Um exemplo de como determinar a página de código usando o [**método Export**](database-export.md) é fornecido no SDK do Windows Installer como parte do WiLangId.vbs do utilitário.</span><span class="sxs-lookup"><span data-stu-id="9c8a6-109">An example of determining the code page by using the [**Export method**](database-export.md) is provided in the Windows Installer SDK as a part of the utility WiLangId.vbs.</span></span> <span data-ttu-id="9c8a6-110">Para obter mais informações sobre como usar WiLangId.vbs consulte o tópico: [gerenciar idioma e página de código](manage-language-and-codepage.md).</span><span class="sxs-lookup"><span data-stu-id="9c8a6-110">For more information about using WiLangId.vbs see the topic: [Manage Language and Codepage](manage-language-and-codepage.md).</span></span>

 

 



