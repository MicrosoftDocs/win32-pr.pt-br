---
description: O WMI implementa uma técnica que permite que várias versões localizadas da mesma classe sejam armazenadas no repositório.
ms.assetid: 01e1cee5-d882-45b6-ac93-68533c2c6c9d
ms.tgt_platform: multiple
title: Localizando informações da classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9f1a7e34c3ba230655ebba4c070981a8dab901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297328"
---
# <a name="localizing-wmi-class-information"></a><span data-ttu-id="b6f72-103">Localizando informações da classe WMI</span><span class="sxs-lookup"><span data-stu-id="b6f72-103">Localizing WMI Class Information</span></span>

<span data-ttu-id="b6f72-104">O WMI implementa uma técnica que permite que várias versões localizadas da mesma classe sejam armazenadas no repositório.</span><span class="sxs-lookup"><span data-stu-id="b6f72-104">WMI implements a technique that allows multiple localized versions of the same class to be stored in the repository.</span></span>

<span data-ttu-id="b6f72-105">A definição de classe é separada nas seguintes versões:</span><span class="sxs-lookup"><span data-stu-id="b6f72-105">The class definition is separated into the following versions:</span></span>

-   <span data-ttu-id="b6f72-106">Uma versão com neutralidade de idioma que contém apenas uma definição de classe básica.</span><span class="sxs-lookup"><span data-stu-id="b6f72-106">A language-neutral version that contains only a basic class definition.</span></span>
-   <span data-ttu-id="b6f72-107">Uma versão específica a um idioma que contém informações localizadas, como descrições de propriedades específicas de uma localidade.</span><span class="sxs-lookup"><span data-stu-id="b6f72-107">A language-specific version that contains localized information, such as property descriptions that are specific to a locale.</span></span>

<span data-ttu-id="b6f72-108">As definições de classe específicas de idioma são armazenadas em um namespace filho sob o namespace que contém uma definição de classe básica neutra de linguagem.</span><span class="sxs-lookup"><span data-stu-id="b6f72-108">The language-specific class definitions are stored in a child namespace beneath the namespace that contains a language-neutral basic class definition.</span></span>

<span data-ttu-id="b6f72-109">Quando você solicita uma definição de classe localizada para uma localidade específica, o WMI combina a definição de classe básica e as informações de classe localizadas para formar uma classe localizada completa.</span><span class="sxs-lookup"><span data-stu-id="b6f72-109">When you request a localized class definition for a specific locale, WMI combines the basic class definition and the localized class information to form a complete localized class.</span></span> <span data-ttu-id="b6f72-110">Você pode obter uma versão localizada de uma classe WMI especificando uma localidade ao se conectar ao WMI e definindo um sinalizador que indica que você deseja informações localizadas.</span><span class="sxs-lookup"><span data-stu-id="b6f72-110">You can get a localized version of a WMI class by specifying a locale when you connect to WMI and setting a flag that indicates that you want localized information.</span></span> <span data-ttu-id="b6f72-111">Em seguida, o WMI mescla as informações do idioma neutro e das versões específicas do idioma da definição de classe para formar uma classe localizada.</span><span class="sxs-lookup"><span data-stu-id="b6f72-111">WMI then merges the information from the language-neutral and the language-specific versions of the class definition to form a localized class.</span></span>

<span data-ttu-id="b6f72-112">As classes WMI que contêm informações localizadas são marcadas com o qualificador de **emenda** e são chamadas de classes emendadas; uma classe oferece suporte a informações localizadas se tiver esse qualificador.</span><span class="sxs-lookup"><span data-stu-id="b6f72-112">WMI classes that contain localized information are marked with the **Amendment** qualifier and are called amended classes; a class supports localized information if it has this qualifier.</span></span> <span data-ttu-id="b6f72-113">Você pode determinar em qual localidade a classe foi localizada verificando outro qualificador chamado [**localidade**](swbemobjectpath-locale.md).</span><span class="sxs-lookup"><span data-stu-id="b6f72-113">You can determine which locale the class has been localized for by checking for another qualifier called [**Locale**](swbemobjectpath-locale.md).</span></span> <span data-ttu-id="b6f72-114">O qualificador de localidade contém um identificador de localização (LCID do Windows) que identifica uma localidade.</span><span class="sxs-lookup"><span data-stu-id="b6f72-114">The locale qualifier contains a localization identifier (Windows LCID) that identifies a locale.</span></span> <span data-ttu-id="b6f72-115">Por exemplo, a localidade para o inglês americano é 0x409.</span><span class="sxs-lookup"><span data-stu-id="b6f72-115">For example, the locale for American English is 0x409.</span></span> <span data-ttu-id="b6f72-116">Se um qualificador em uma classe corrigida contiver informações localizadas, ele conterá o tipo de qualificador **corrigido** .</span><span class="sxs-lookup"><span data-stu-id="b6f72-116">If a qualifier in an amended class contains localized information, it contains the **amended** qualifier flavor.</span></span>

<span data-ttu-id="b6f72-117">A localização do WMI inclui as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="b6f72-117">WMI localization includes the following tasks:</span></span>

-   [<span data-ttu-id="b6f72-118">Criando definições de classe localizadas</span><span class="sxs-lookup"><span data-stu-id="b6f72-118">Creating localized class definitions</span></span>](creating-localized-class-definitions.md)
-   [<span data-ttu-id="b6f72-119">Compilando arquivos MOF localizados</span><span class="sxs-lookup"><span data-stu-id="b6f72-119">Compiling localized MOF files</span></span>](compiling-localized-mof-files.md)
-   [<span data-ttu-id="b6f72-120">Localizando valores de propriedade</span><span class="sxs-lookup"><span data-stu-id="b6f72-120">Localizing property values</span></span>](localizing-property-values.md)
-   [<span data-ttu-id="b6f72-121">Recuperando classes corrigidas</span><span class="sxs-lookup"><span data-stu-id="b6f72-121">Retrieving amended classes</span></span>](retrieving-amended-classes.md)

<span data-ttu-id="b6f72-122">Para obter mais informações, consulte [Considerações sobre a classe corrigida](amended-class-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="b6f72-122">For more information, see [Amended Class Considerations](amended-class-considerations.md).</span></span>

 

 



