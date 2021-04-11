---
description: Para habilitar a funcionalidade do instalador, um aplicativo deve chamar várias funções quando ele estiver sendo inicializado.
ms.assetid: cfeaf9b9-f772-49f9-8b6f-e7fd0c93cc9f
title: Inicializando um aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221c5d97f0febb23ba73f98605ee6ec0e853940c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169185"
---
# <a name="initializing-an-application"></a><span data-ttu-id="3cd80-103">Inicializando um aplicativo</span><span class="sxs-lookup"><span data-stu-id="3cd80-103">Initializing an Application</span></span>

<span data-ttu-id="3cd80-104">Para habilitar a funcionalidade do instalador, um aplicativo deve chamar várias funções quando ele estiver sendo inicializado.</span><span class="sxs-lookup"><span data-stu-id="3cd80-104">To enable installer functionality, an application must call a number of functions when it is initializing.</span></span> <span data-ttu-id="3cd80-105">Para obter mais informações, consulte [mecanismo de instalação](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="3cd80-105">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span> <span data-ttu-id="3cd80-106">As etapas a seguir descrevem como usar o instalador para inicializar um aplicativo:</span><span class="sxs-lookup"><span data-stu-id="3cd80-106">The following steps describe how to use the installer to initialize an application:</span></span>

<span data-ttu-id="3cd80-107">**Para inicializar um aplicativo**</span><span class="sxs-lookup"><span data-stu-id="3cd80-107">**To initialize an application**</span></span>

1.  <span data-ttu-id="3cd80-108">Chame a função [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) para que o aplicativo possa se identificar para o instalador.</span><span class="sxs-lookup"><span data-stu-id="3cd80-108">Call the [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) function so the application can identify itself to the installer.</span></span>

    <span data-ttu-id="3cd80-109">O código do produto é um parâmetro necessário para muitas funções do instalador.</span><span class="sxs-lookup"><span data-stu-id="3cd80-109">The product code is a required parameter for many installer functions.</span></span>

2.  <span data-ttu-id="3cd80-110">Chame a função [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) para coletar informações do usuário na primeira vez que o aplicativo for iniciado.</span><span class="sxs-lookup"><span data-stu-id="3cd80-110">Call the [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) function to collect user information the first time the application starts.</span></span>

    <span data-ttu-id="3cd80-111">Se a chamada para [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) falhar, chame a função [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) para coletar informações do usuário.</span><span class="sxs-lookup"><span data-stu-id="3cd80-111">If the call to [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) fails, call the [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) function to collect user information.</span></span>

3.  <span data-ttu-id="3cd80-112">Exiba uma interface do usuário padrão, se necessário, chamando a função [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) .</span><span class="sxs-lookup"><span data-stu-id="3cd80-112">Display a default user interface, if necessary, by calling the [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) function.</span></span>

    <span data-ttu-id="3cd80-113">Para criar sua própria interface de usuário, registre-a com o instalador chamando a função [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) .</span><span class="sxs-lookup"><span data-stu-id="3cd80-113">To author your own user interface, register it with the installer by calling the [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) function.</span></span>

4.  <span data-ttu-id="3cd80-114">Chame a função [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) para definir o nível de log.</span><span class="sxs-lookup"><span data-stu-id="3cd80-114">Call the [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) function to set the logging level.</span></span>
5.  <span data-ttu-id="3cd80-115">Apresente ao usuário os recursos disponíveis enumerando os recursos do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3cd80-115">Present the user with available features by enumerating the features of your application.</span></span> <span data-ttu-id="3cd80-116">Você pode enumerar recursos das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="3cd80-116">You can enumerate features in the following ways:</span></span>
    -   <span data-ttu-id="3cd80-117">Consulte o recurso do instalador por recurso.</span><span class="sxs-lookup"><span data-stu-id="3cd80-117">Query the installer feature-by-feature.</span></span> <span data-ttu-id="3cd80-118">Por exemplo, antes que o aplicativo desenhe um botão ou um item de menu, o aplicativo chama a função [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) para que o instalador possa verificar se o recurso está disponível.</span><span class="sxs-lookup"><span data-stu-id="3cd80-118">For example, before the application draws a button or a menu item, the application calls the [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) function so the installer can check that the feature is available.</span></span>
    -   <span data-ttu-id="3cd80-119">Enumere todos os recursos disponíveis de uma vez chamando a função [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) .</span><span class="sxs-lookup"><span data-stu-id="3cd80-119">Enumerate all of the available features at once by calling the [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) function.</span></span> <span data-ttu-id="3cd80-120">Para usar essa função, o aplicativo deve chamar **MsiEnumFeatures** repetidamente enquanto incrementa um índice.</span><span class="sxs-lookup"><span data-stu-id="3cd80-120">To use this function, the application must call **MsiEnumFeatures** repeatedly while incrementing an index.</span></span>
6.  <span data-ttu-id="3cd80-121">Obtenha informações detalhadas sobre a instalação atual chamando as seguintes funções de enumeração repetidamente, incrementando uma variável de índice para cada chamada:</span><span class="sxs-lookup"><span data-stu-id="3cd80-121">Get detailed information about the current installation by calling the following enumeration functions repeatedly, incrementing an index variable for each call:</span></span>

    -   <span data-ttu-id="3cd80-122">Chame a função [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) para enumerar os produtos registrados com o instalador.</span><span class="sxs-lookup"><span data-stu-id="3cd80-122">Call the [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) function to enumerate products registered with the installer.</span></span>
    -   <span data-ttu-id="3cd80-123">Chame a função [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) para enumerar componentes.</span><span class="sxs-lookup"><span data-stu-id="3cd80-123">Call the [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) function to enumerate components.</span></span>
    -   <span data-ttu-id="3cd80-124">Chame a função [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) para enumerar qualificadores de componentes.</span><span class="sxs-lookup"><span data-stu-id="3cd80-124">Call the [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) function to enumerate component qualifiers.</span></span>
    -   <span data-ttu-id="3cd80-125">Chame a função [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) para enumerar os produtos para um componente específico.</span><span class="sxs-lookup"><span data-stu-id="3cd80-125">Call the [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) function to enumerate the products for a particular component.</span></span>

    <span data-ttu-id="3cd80-126">Se o valor de retorno em uma função de enumeração for um erro de \_ êxito, ainda haverá mais itens a serem enumerados e a função deverá ser chamada novamente com uma variável de índice incrementada.</span><span class="sxs-lookup"><span data-stu-id="3cd80-126">If the return value on an enumeration function is ERROR\_SUCCESS, there are still more items to be enumerated and the function should be called again with an incremented index variable.</span></span> <span data-ttu-id="3cd80-127">Se o valor de retorno for \_ um erro de não \_ mais \_ itens, todos os itens foram enumerados e a função não deve ser chamada novamente.</span><span class="sxs-lookup"><span data-stu-id="3cd80-127">If the return value is ERROR\_NO\_MORE\_ITEMS, then all of the items have been enumerated, and the function should not be called again.</span></span>

 

 



