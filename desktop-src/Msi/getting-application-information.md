---
description: O banco de dados do produto contém informações sobre um produto. Para obter mais informações sobre como obter informações de produto com funções de enumeração, consulte Inicializando um aplicativo.
ms.assetid: 528c915c-296c-4620-8105-0b5d543e56a5
title: Obtendo informações do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dce842f057efb65b6d0db3ad0407a19bf08435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921250"
---
# <a name="getting-application-information"></a><span data-ttu-id="fc8e3-104">Obtendo informações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="fc8e3-104">Getting Application Information</span></span>

<span data-ttu-id="fc8e3-105">O banco de dados do produto contém informações sobre um produto.</span><span class="sxs-lookup"><span data-stu-id="fc8e3-105">The product database contains information about a product.</span></span> <span data-ttu-id="fc8e3-106">Para obter mais informações sobre como obter informações de produto com funções de enumeração, consulte [inicializando um aplicativo](initializing-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="fc8e3-106">For more information on obtaining product information with enumeration functions, see [Initializing an Application](initializing-an-application.md).</span></span>

<span data-ttu-id="fc8e3-107">**Para obter informações sobre o produto**</span><span class="sxs-lookup"><span data-stu-id="fc8e3-107">**To get product information**</span></span>

1.  <span data-ttu-id="fc8e3-108">Verifique se um produto está instalado chamando a função [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) .</span><span class="sxs-lookup"><span data-stu-id="fc8e3-108">Verify that a product is installed by calling the [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) function.</span></span>
2.  <span data-ttu-id="fc8e3-109">Abra o banco de dados e obtenha um identificador para ele chamando a função [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) .</span><span class="sxs-lookup"><span data-stu-id="fc8e3-109">Open the database and obtain a handle to it by calling the [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) function.</span></span>

    <span data-ttu-id="fc8e3-110">Se o banco de dados estiver contido em um pacote de instalação, chame a função [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) .</span><span class="sxs-lookup"><span data-stu-id="fc8e3-110">If the database is contained in an installation package, call the [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) function.</span></span>

3.  <span data-ttu-id="fc8e3-111">Use o identificador aberto para obter propriedades do produto com a função [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) e para obter informações descritivas de recursos com a função [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) .</span><span class="sxs-lookup"><span data-stu-id="fc8e3-111">Use the open handle to obtain product properties with the [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) function, and to obtain descriptive feature information with the [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) function.</span></span>

    <span data-ttu-id="fc8e3-112">Se você quiser obter informações de produto usando o código do produto, em vez de usar o identificador de banco de dados aberto, chame a função [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) em vez de [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).</span><span class="sxs-lookup"><span data-stu-id="fc8e3-112">If you want to obtain product information using the product code, rather than using the open database handle, call the [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) function instead of [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).</span></span>

4.  <span data-ttu-id="fc8e3-113">Feche um identificador de instalação aberta chamando a função [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) .</span><span class="sxs-lookup"><span data-stu-id="fc8e3-113">Close an open installation handle by calling the [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) function.</span></span>

    <span data-ttu-id="fc8e3-114">A função [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) é uma função de diagnóstico e não deve ser usada para fechar os identificadores que você sabe que estão abertos.</span><span class="sxs-lookup"><span data-stu-id="fc8e3-114">The [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) function is a diagnostic function and should not be used to close handles you know to be open.</span></span> <span data-ttu-id="fc8e3-115">É aceitável chamar a função **MsiCloseAllHandles** quando o aplicativo é fechado para garantir que todos os identificadores tenham sido fechados.</span><span class="sxs-lookup"><span data-stu-id="fc8e3-115">It is acceptable to call the **MsiCloseAllHandles** function when the application closes to ensure that all handles have been closed.</span></span>

 

 



