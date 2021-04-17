---
description: Monitor de Rede ou a DLL do analisador podem formatar os dados que são exibidos no painel de detalhes da interface do usuário do Monitor de Rede.
ms.assetid: 60ab9253-ec0f-4c97-a475-ce2a74d469c4
title: Formatar os dados exibidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017946dab9db443cf7083109dd75ccee1f6d278a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501353"
---
# <a name="formatting-displayed-data"></a><span data-ttu-id="3ba74-103">Formatar os dados exibidos</span><span class="sxs-lookup"><span data-stu-id="3ba74-103">Formatting Displayed Data</span></span>

<span data-ttu-id="3ba74-104">Monitor de Rede ou a DLL do analisador podem formatar os dados que são exibidos no painel de detalhes da interface do usuário do Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="3ba74-104">Network Monitor or your parser DLL can format the data that is displayed in the details pane of the Network Monitor UI.</span></span>

<span data-ttu-id="3ba74-105">O Monitor de Rede fornece um formatador genérico que fornece os serviços básicos necessários para exibir a maioria dos tipos de dados existentes em um protocolo.</span><span class="sxs-lookup"><span data-stu-id="3ba74-105">Network Monitor provides a generic formatter that provides the basic services needed to display most data types that exist within a protocol.</span></span> <span data-ttu-id="3ba74-106">No entanto, o formatador genérico não oferece suporte a todos os tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="3ba74-106">However, the generic formatter does not support all data types.</span></span> <span data-ttu-id="3ba74-107">Por exemplo, o formatador genérico não oferece suporte ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="3ba74-107">For example, the generic formatter does not support the following:</span></span>

-   <span data-ttu-id="3ba74-108">Vários tipos de endereço.</span><span class="sxs-lookup"><span data-stu-id="3ba74-108">Several address types.</span></span>
-   <span data-ttu-id="3ba74-109">Nomes amigáveis de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="3ba74-109">Source and destination-friendly names.</span></span>
-   <span data-ttu-id="3ba74-110">Identificadores de objeto.</span><span class="sxs-lookup"><span data-stu-id="3ba74-110">Object identifiers.</span></span>
-   <span data-ttu-id="3ba74-111">Tipos de dados inteiros grandes.</span><span class="sxs-lookup"><span data-stu-id="3ba74-111">Large integer data types.</span></span>
-   <span data-ttu-id="3ba74-112">Tipos de dados inteiros pequenos de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="3ba74-112">Variable length small integer data types.</span></span>

<span data-ttu-id="3ba74-113">O exemplo a seguir identifica duas cadeias de caracteres formatadas para a propriedade de ID de privilégio.</span><span class="sxs-lookup"><span data-stu-id="3ba74-113">The following example identifies two formatted strings for the Privilege ID property.</span></span>

-   <span data-ttu-id="3ba74-114">A primeira linha de código mostra a saída do formatador genérico.</span><span class="sxs-lookup"><span data-stu-id="3ba74-114">The first line of code shows the output of the generic formatter.</span></span> <span data-ttu-id="3ba74-115">A saída é baseada no tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3ba74-115">The output is based on the data type.</span></span>
-   <span data-ttu-id="3ba74-116">A segunda linha de código mostra a saída de um formatador personalizado com uma cadeia de caracteres para os dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="3ba74-116">The second line of code shows the output of a custom formatter with a string to the property data.</span></span>

``` syntax
Privilege ID (PID) = 0x0029
Privilege ID   (PID) = 0x0029   The Process has privileges
```

> [!Note]  
> <span data-ttu-id="3ba74-117">Quando possível, use o formatador genérico para exibir seus dados, pois ele permite controlar o tamanho da DLL do analisador e fornece melhores recursos de plataforma cruzada para a DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="3ba74-117">When possible, use the generic formatter to display your data because it allows you to control the size of your parser DLL, and provides better cross-platform capabilities for your parser DLL.</span></span>

 

 

 



