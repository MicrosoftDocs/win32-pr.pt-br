---
description: Uma página de código é uma tabela interna que o sistema operacional usa para mapear símbolos (letras, numerais e caracteres de pontuação) para um número de caractere.
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: Verificando a página de código do banco de dados de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ea9513ec80413e00a9f3f4c1232a06704f83e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757527"
---
# <a name="checking-the-installation-database-code-page"></a><span data-ttu-id="4b873-103">Verificando a página de código do banco de dados de instalação</span><span class="sxs-lookup"><span data-stu-id="4b873-103">Checking the Installation Database Code Page</span></span>

<span data-ttu-id="4b873-104">Uma *página de código* é uma tabela interna que o sistema operacional usa para mapear símbolos (letras, numerais e caracteres de pontuação) para um número de caractere.</span><span class="sxs-lookup"><span data-stu-id="4b873-104">A *code page* is an internal table that the operating system uses to map symbols (letters, numerals, and punctuation characters) to a character number.</span></span> <span data-ttu-id="4b873-105">Páginas de código diferentes fornecem suporte para os conjuntos de caracteres usados em diferentes países ou regiões.</span><span class="sxs-lookup"><span data-stu-id="4b873-105">Different code pages provide support for the character sets used in different countries or regions.</span></span> <span data-ttu-id="4b873-106">As páginas de código são referenciadas por número; por exemplo, a página de código 932 representa o conjunto de caracteres japoneses e a página de código 950 representa um dos conjuntos de caracteres chineses.</span><span class="sxs-lookup"><span data-stu-id="4b873-106">Code pages are referred to by number; for example, code page 932 represents the Japanese character set, and code page 950 represents one of the Chinese character sets.</span></span> <span data-ttu-id="4b873-107">Consulte [localizando as tabelas Error e ActionText](localizing-the-error-and-actiontext-tables.md) para obter uma lista de páginas de código ASCII.</span><span class="sxs-lookup"><span data-stu-id="4b873-107">See [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md) for a list of ASCII code pages.</span></span>

<span data-ttu-id="4b873-108">A mesma página de código ASCII, 1252, pode ser usada para inglês e francês.</span><span class="sxs-lookup"><span data-stu-id="4b873-108">The same ASCII code page, 1252, may be used for English and French.</span></span> <span data-ttu-id="4b873-109">Portanto, a página de código para o banco de dados MNP2000.msi (inglês) não precisa ser redefinida para alterar a instalação para francês.</span><span class="sxs-lookup"><span data-stu-id="4b873-109">Therefore the code page for the database MNP2000.msi (English) does not need to be reset to change the installation to French.</span></span>

<span data-ttu-id="4b873-110">Para obter mais informações sobre como definir a página de código, consulte [manipulação de página de código (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="4b873-110">For more information about setting the code page see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

[<span data-ttu-id="4b873-111">Continuar</span><span class="sxs-lookup"><span data-stu-id="4b873-111">Continue</span></span>](importing-localized-error-and-actiontext-tables.md)

 

 



