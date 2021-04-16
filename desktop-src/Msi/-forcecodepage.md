---
description: A \_ tabela ForceCodepage é uma tabela especial usada para alterar a página de código de um pacote de instalação. Você pode determinar ou definir a página de código exportando ou importando um arquivo morto de texto chamado \_ ForceCodepage. IDT.
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132843fa092409b26811afd6a4c1f3e7cf0544f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758318"
---
# <a name="_forcecodepage"></a><span data-ttu-id="64a51-104">\_ForceCodepage</span><span class="sxs-lookup"><span data-stu-id="64a51-104">\_ForceCodepage</span></span>

<span data-ttu-id="64a51-105">A \_ tabela ForceCodepage é uma tabela especial usada para alterar a página de código de um pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="64a51-105">The \_ForceCodepage table is a special table used for changing the code page of an installation package.</span></span> <span data-ttu-id="64a51-106">Você pode determinar ou definir a página de código exportando ou importando um [arquivo morto de texto](text-archive-files.md) chamado \_ ForceCodepage. IDT.</span><span class="sxs-lookup"><span data-stu-id="64a51-106">You can determine or set the code page by exporting or importing a [text archive file](text-archive-files.md) named \_ForceCodepage.idt.</span></span>

<span data-ttu-id="64a51-107">O formato da \_ tabela ForceCodepage é 2 linhas em branco seguidas por uma terceira linha que indica a página de código numérico.</span><span class="sxs-lookup"><span data-stu-id="64a51-107">The format of the \_ForceCodepage table is 2 blank lines followed by a third line that indicates the numeric code page.</span></span> <span data-ttu-id="64a51-108">Por exemplo, um \_ arquivo de tabela ForceCodepage. IDT para um banco de dados japonês seria semelhante ao seguinte.</span><span class="sxs-lookup"><span data-stu-id="64a51-108">For example, a \_ForceCodepage table .idt file for a Japanese database would look as follows.</span></span> <span data-ttu-id="64a51-109">Nesse caso, a página de código numérico é 932.</span><span class="sxs-lookup"><span data-stu-id="64a51-109">The numeric code page in this case is 932.</span></span>

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

<span data-ttu-id="64a51-110">Para obter mais informações sobre como usar \_ o ForceCodepage para obter ou definir a página de código de um banco de dados, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="64a51-110">For more information on how to use \_ForceCodepage to get or set the code page of a database see the following topics.</span></span>

-   [<span data-ttu-id="64a51-111">Manipulação de página de código (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="64a51-111">Code Page Handling (Windows Installer)</span></span>](code-page-handling-windows-installer-.md)
-   [<span data-ttu-id="64a51-112">Determinando a página de código de um banco de dados de instalação</span><span class="sxs-lookup"><span data-stu-id="64a51-112">Determining an Installation Database's Code Page</span></span>](determining-an-installation-database-s-code-page.md)
-   [<span data-ttu-id="64a51-113">Configurando a página de código de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="64a51-113">Setting the Code Page of a Database</span></span>](setting-the-code-page-of-a-database.md)

<span data-ttu-id="64a51-114">A \_ tabela ForceCodepage é uma pseudoclasse especial usada para alterar a página de código de um pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="64a51-114">The \_ForceCodepage table is a special pseudo table used for changing the code page of an installation package.</span></span> <span data-ttu-id="64a51-115">O uso da \_ tabela ForceCodepage define incondicionalmente o banco de dados para a página de código sem executar nenhuma validação para determinar se eles atualmente podem ser convertidos na nova página de código.</span><span class="sxs-lookup"><span data-stu-id="64a51-115">Using the \_ForceCodepage table unconditionally sets the database to the code page without performing any validation as to whether the data currently in the database can be translated to the new code page.</span></span> <span data-ttu-id="64a51-116">É sempre recomendável que a alteração da página de código de um banco de dados seja iniciada com um banco de dados com neutralidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="64a51-116">It is always recommended that changing the code page of a database start with a language neutral database.</span></span>

 

 



