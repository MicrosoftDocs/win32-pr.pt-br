---
description: Depois de ter um identificador para um arquivo INF, você pode recuperar informações dele de várias maneiras. Funções como SetupGetInfInformation, SetupQueryInfFileInformation e SetupQueryInfVersionInformation recuperam informações sobre o próprio arquivo INF.
ms.assetid: e64c9576-ad62-4ebd-8d30-4e4e0da3b8c5
title: Recuperando informações de um arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cfb1a52fd004b1d812e4a01320a5bdd2bbeca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754938"
---
# <a name="retrieving-information-from-an-inf-file"></a><span data-ttu-id="c8fba-104">Recuperando informações de um arquivo INF</span><span class="sxs-lookup"><span data-stu-id="c8fba-104">Retrieving Information From an INF File</span></span>

<span data-ttu-id="c8fba-105">Depois de ter um identificador para um arquivo INF, você pode recuperar informações dele de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="c8fba-105">After you have a handle to an INF file, you can retrieve information from it in a variety of ways.</span></span> <span data-ttu-id="c8fba-106">Funções como [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa), [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)e [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa) recuperam informações sobre o próprio arquivo inf.</span><span class="sxs-lookup"><span data-stu-id="c8fba-106">Functions such as [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa), [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa), and [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa) retrieve information about the INF file itself.</span></span>

<span data-ttu-id="c8fba-107">Outras funções como [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) e [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha) adquirem informações sobre os arquivos de origem e os diretórios de destino.</span><span class="sxs-lookup"><span data-stu-id="c8fba-107">Other functions such as [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) and [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha) acquire information about the source files and target directories.</span></span>

<span data-ttu-id="c8fba-108">Funções de nível baixo, como [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta) e [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda) , permitem que você acesse diretamente as informações armazenadas em uma linha ou campo de um arquivo inf.</span><span class="sxs-lookup"><span data-stu-id="c8fba-108">Low-level functions like [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta) and [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda) enable you to directly access information stored in a line or field of an INF file.</span></span> <span data-ttu-id="c8fba-109">Essas funções são usadas internamente pelas funções de nível superior, mas também estão disponíveis caso você precise acessar informações de INF no nível de linha ou de campo.</span><span class="sxs-lookup"><span data-stu-id="c8fba-109">These functions are used internally by the higher-level functions, but are also available should you need to access INF information at the line or field level.</span></span>

 

 



