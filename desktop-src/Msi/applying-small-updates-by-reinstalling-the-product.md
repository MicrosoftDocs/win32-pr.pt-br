---
description: Uma pequena atualização pode ser aplicada a um aplicativo por meio da reinstalação completa ou parcial do aplicativo da linha de comando ou de um programa.
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: Aplicando pequenas atualizações reinstalando o produto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27b97ff0274baac5a4ec30df244394a609ed525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921513"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a><span data-ttu-id="bedba-103">Aplicando pequenas atualizações reinstalando o produto</span><span class="sxs-lookup"><span data-stu-id="bedba-103">Applying Small Updates by Reinstalling the Product</span></span>

<span data-ttu-id="bedba-104">Uma pequena atualização pode ser aplicada a um aplicativo por meio da reinstalação completa ou parcial do aplicativo da linha de comando ou de um programa.</span><span class="sxs-lookup"><span data-stu-id="bedba-104">A small update can be applied to an application by completely or partially reinstalling the application from the command line or from a program.</span></span>

<span data-ttu-id="bedba-105">**Para propagar a pequena atualização para os usuários atuais (esta é uma reinstalação completa) da linha de comando**</span><span class="sxs-lookup"><span data-stu-id="bedba-105">**To propagate the small update to current users (this is a complete reinstall) from the command line**</span></span>

1.  <span data-ttu-id="bedba-106">Na linha de comando, use: **msiexec/fvomus \[** _caminho para o arquivo. msi atualizado_ *_\]_* ou **msiexec \[ /i** _caminho para atualizado o arquivo. msi_ *_\] reinstalar = todos os REINSTALLMODE = vomus_*.</span><span class="sxs-lookup"><span data-stu-id="bedba-106">From the command line use either: **msiexec /fvomus \[**_path to updated .msi file_*_\]_* or **msiexec /I \[**_path to updated .msi file_*_\] REINSTALL=ALL REINSTALLMODE=vomus_*.</span></span>
2.  <span data-ttu-id="bedba-107">O arquivo. msi atualizado é armazenado em cache no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="bedba-107">The updated .msi file is cached on the user's computer.</span></span> <span data-ttu-id="bedba-108">Observe que não é possível que o usuário reinstale o produto usando Adicionar/remover programas porque o arquivo. msi atualizado ainda não está no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="bedba-108">Note that it is not possible for the user to reinstall the product using Add/Remove Programs because the updated .msi file is not yet on the user's computer.</span></span>

<span data-ttu-id="bedba-109">**Para propagar uma pequena atualização para os usuários atuais (esta é uma reinstalação completa) de um programa**</span><span class="sxs-lookup"><span data-stu-id="bedba-109">**To propagate a small update to current users (this is a complete reinstall) from a program**</span></span>

1.  <span data-ttu-id="bedba-110">A partir de um programa, chame [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) e especifique o pacote REINSTALLMODE \_ , o REINSTALLMODE \_ FILEOLDERVERSION, o REINSTALLMODE \_ MACHINEDATA, o o \_ UserData e o \_ atalho REINSTALLMODE</span><span class="sxs-lookup"><span data-stu-id="bedba-110">From a program, call [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) and specify REINSTALLMODE\_PACKAGE, REINSTALLMODE\_FILEOLDERVERSION, REINSTALLMODE\_MACHINEDATA, REINSTALLMODE\_USERDATA, and REINSTALLMODE\_SHORTCUT</span></span>
2.  <span data-ttu-id="bedba-111">O arquivo. msi atualizado é armazenado em cache no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="bedba-111">The updated .msi file is cached on the user's computer.</span></span>

<span data-ttu-id="bedba-112">O método a seguir inicia uma reinstalação somente de recursos ou componentes afetados pela atualização pequena.</span><span class="sxs-lookup"><span data-stu-id="bedba-112">The following method launches a reinstallation of only those features or components that are affected by the small update.</span></span>

<span data-ttu-id="bedba-113">**Para propagar uma pequena atualização para os usuários atuais (esta é uma reinstalação parcial)**</span><span class="sxs-lookup"><span data-stu-id="bedba-113">**To propagate a small update to current users (this is a partial reinstall)**</span></span>

1.  <span data-ttu-id="bedba-114">Obtenha uma lista dos nomes de recursos e componentes afetados pela atualização pequena.</span><span class="sxs-lookup"><span data-stu-id="bedba-114">Obtain a list of the names of features and components that are affected by the small update.</span></span>
2.  <span data-ttu-id="bedba-115">No prompt de comando, use: **msiexec \[ /i** _caminho para atualizado o arquivo. msi_ *_\] reinstalar = \[_* lista _\] de recursos_ **REINSTALLMODE = vomus**.</span><span class="sxs-lookup"><span data-stu-id="bedba-115">From the command prompt use: **msiexec /I \[**_path to updated .msi file_*_\] REINSTALL=\[_*_Feature list\]_ **REINSTALLMODE=vomus**.</span></span>
3.  <span data-ttu-id="bedba-116">O arquivo. msi atualizado é armazenado em cache no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="bedba-116">The updated .msi file is cached on the user's computer.</span></span>

 

 



