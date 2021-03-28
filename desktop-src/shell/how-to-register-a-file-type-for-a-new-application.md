---
description: Se você planeja associar um ou mais tipos de arquivo a um novo aplicativo, deve definir um ProgID para cada tipo de arquivo que você deseja associar ao aplicativo.
ms.assetid: 997600C9-5264-44EC-BAEC-CB5CEEA0BD14
title: Como registrar um tipo de arquivo para um novo aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728cc48075ab1c2631f0a950059da65ae326ae79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967894"
---
# <a name="how-to-register-a-file-type-for-a-new-application"></a><span data-ttu-id="2045d-103">Como registrar um tipo de arquivo para um novo aplicativo</span><span class="sxs-lookup"><span data-stu-id="2045d-103">How to Register a File Type for a New Application</span></span>

<span data-ttu-id="2045d-104">Se você planeja associar um ou mais tipos de arquivo a um novo aplicativo, deve definir um ProgID para cada tipo de arquivo que você deseja associar ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2045d-104">If you plan to associate one or more file types with a new application, you must define a ProgID for each file type that you want to associate with the application.</span></span>

<span data-ttu-id="2045d-105">Para criar um ProgID para cada tipo de arquivo exclusivo que seu aplicativo manipula, use estas etapas.</span><span class="sxs-lookup"><span data-stu-id="2045d-105">To create a ProgID for each unique file type that your application handles, use these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="2045d-106">Instruções</span><span class="sxs-lookup"><span data-stu-id="2045d-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="2045d-107">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="2045d-107">Step 1:</span></span>

<span data-ttu-id="2045d-108">Observe que alguns tipos de arquivo têm várias extensões que apontam para o mesmo ProgID; por exemplo:</span><span class="sxs-lookup"><span data-stu-id="2045d-108">Note that some file types have multiple extensions that point to the same ProgID; for example:</span></span>

-   <span data-ttu-id="2045d-109">**HKEY \_ CLASSES \_ raiz** \\ **app. jpeg** (seu ProgID)</span><span class="sxs-lookup"><span data-stu-id="2045d-109">**HKEY\_CLASSES\_ROOT**\\**App.jpeg** (your ProgID)</span></span>
-   <span data-ttu-id="2045d-110">**HKEY \_ CLASSES \_ root** \\ **. jpg** = app. jpeg (os mapeamentos de tipo de arquivo)</span><span class="sxs-lookup"><span data-stu-id="2045d-110">**HKEY\_CLASSES\_ROOT**\\ **.jpg** = App.jpeg (the file type mappings)</span></span>
-   <span data-ttu-id="2045d-111">**HKEY \_ CLASSES \_ raiz** \\ **. jpeg** = app. jpeg</span><span class="sxs-lookup"><span data-stu-id="2045d-111">**HKEY\_CLASSES\_ROOT**\\ **.jpeg** = App.jpeg</span></span>

### <a name="step-2"></a><span data-ttu-id="2045d-112">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="2045d-112">Step 2:</span></span>

<span data-ttu-id="2045d-113">Remova os valores de ProgID ao instalar e desinstalar o programa.</span><span class="sxs-lookup"><span data-stu-id="2045d-113">Remove the ProgID values when you install and uninstall your program.</span></span>

### <a name="step-3"></a><span data-ttu-id="2045d-114">Etapa 3:</span><span class="sxs-lookup"><span data-stu-id="2045d-114">Step 3:</span></span>

<span data-ttu-id="2045d-115">Deixe os mapeamentos de tipo de arquivo inalterados no momento da desinstalação.</span><span class="sxs-lookup"><span data-stu-id="2045d-115">Leave the file type mappings unchanged at uninstall time.</span></span> <span data-ttu-id="2045d-116">Isso funciona porque os mapeamentos de tipo de arquivo são armazenados por usuário em \_ classe HKEY \_ root \\ . ext, e o sistema identifica o caso em que o valor ProgID está ausente e o ignora.</span><span class="sxs-lookup"><span data-stu-id="2045d-116">Doing so works because file type mappings are stored per user in HKEY\_CLASSES\_ROOT\\.ext, and the system identifies the case where the ProgID value is missing and ignores it.</span></span> <span data-ttu-id="2045d-117">Deixar os mapeamentos de tipo de arquivo inalterados evita a necessidade de ter um código condicional que só remove o mapeamento de tipo de arquivo se o valor ainda aponta para o ProgID.</span><span class="sxs-lookup"><span data-stu-id="2045d-117">Leaving file type mappings unchanged avoids the need to have conditional code that only removes the file type mapping if the value still points to your ProgID.</span></span> <span data-ttu-id="2045d-118">É importante evitar isso nos casos em que ele pode ter sido alterado por outro aplicativo e, portanto, não é possível remover facilmente o valor.</span><span class="sxs-lookup"><span data-stu-id="2045d-118">It is important to avoid doing so in cases where it might have been changed by another application and you thus cannot easily remove the value.</span></span>

### <a name="step-4"></a><span data-ttu-id="2045d-119">Etapa 4:</span><span class="sxs-lookup"><span data-stu-id="2045d-119">Step 4:</span></span>

<span data-ttu-id="2045d-120">Especifique um valor exclusivo para a descrição do tipo de arquivo de cada ProgID de tipo de arquivo seguindo um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="2045d-120">Specify a unique value for the file type description of each file type ProgID by doing one of the following:</span></span>

-   <span data-ttu-id="2045d-121">Deixe o valor padrão do ProgID vazio, caso em que o sistema usa o arquivo. ext.</span><span class="sxs-lookup"><span data-stu-id="2045d-121">Leave the default value of the ProgID empty, in which case the system uses the .ext file.</span></span>
-   <span data-ttu-id="2045d-122">Forneça um valor localizado via FriendlyTypeName e, para compatibilidade com aplicativos antigos que lêem o registro diretamente, certifique-se de fornecer o valor padrão do ProgID como a descrição do tipo de arquivo (ou seja, use o mesmo valor que é referenciado pelo FriendlyTypeName no recurso em inglês).</span><span class="sxs-lookup"><span data-stu-id="2045d-122">Provide a localized value via FriendlyTypeName and, for compatibility with old applications that read the registry directly, be sure to provide the default value of the ProgID as the file type description (that is, use the same value that is referred to by the FriendlyTypeName in the English resource).</span></span>

## <a name="remarks"></a><span data-ttu-id="2045d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="2045d-123">Remarks</span></span>

<span data-ttu-id="2045d-124">Se você planeja associar o arquivo a um aplicativo existente, localize um ProgID de aplicativo no registro.</span><span class="sxs-lookup"><span data-stu-id="2045d-124">If you plan to associate the file with an existing application, locate an application ProgID in the registry.</span></span> <span data-ttu-id="2045d-125">Para obter mais informações, consulte [tipos de arquivo](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="2045d-125">For more information, see [File Types](fa-file-types.md).</span></span>

 

 



