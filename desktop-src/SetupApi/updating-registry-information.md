---
description: Depois que a fila for confirmada com êxito, você precisará atualizar as informações do registro para o produto que você está instalando.
ms.assetid: 32161538-c1bd-41a0-bb4f-a32883fe8285
title: Atualizando informações do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa6a77f231f3a4fe754b589e3f20ed67e78e548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922422"
---
# <a name="updating-registry-information"></a><span data-ttu-id="325bd-103">Atualizando informações do registro</span><span class="sxs-lookup"><span data-stu-id="325bd-103">Updating Registry Information</span></span>

<span data-ttu-id="325bd-104">Depois que a fila for confirmada com êxito, você precisará atualizar as informações do registro para o produto que você está instalando.</span><span class="sxs-lookup"><span data-stu-id="325bd-104">After the queue has successfully committed, you will need to update registry information for the product you are installing.</span></span> <span data-ttu-id="325bd-105">É recomendável aguardar até que todas as operações de cópia de arquivo necessárias tenham sido concluídas com êxito antes de alterar as informações do registro.</span><span class="sxs-lookup"><span data-stu-id="325bd-105">It is recommended that you wait until all necessary file copy operations have been successfully completed before altering registry information.</span></span>

<span data-ttu-id="325bd-106">Uma maneira de atualizar o registro é chamar [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) com os \_ sinalizadores de INIFILES, registro mais giratório ou INI2REG de rotação mais fácil \_ \_ especificados.</span><span class="sxs-lookup"><span data-stu-id="325bd-106">One way to update the registry is to call [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) with the SPINST\_INIFILES, SPINST\_REGISTRY, or SPINST\_INI2REG flags specified.</span></span> <span data-ttu-id="325bd-107">Esses sinalizadores podem ser combinados em uma chamada para **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="325bd-107">These flags can be combined in one call to **SetupInstallFromInfSection**.</span></span>

<span data-ttu-id="325bd-108">O exemplo a seguir usa mais de \_ ^ arquivos de aceleração ^ \_ para indicar que a função deve processar todas as operações listadas, exceto as operações de arquivo.</span><span class="sxs-lookup"><span data-stu-id="325bd-108">The following example uses SPINST\_ALL^SPINST\_FILES to indicate that the function should process all of the listed operations except file operations.</span></span> <span data-ttu-id="325bd-109">Como apenas as operações INI, registro e arquivo são listadas na seção **instalar** , esse é um método abreviado de especificar a função deve processar todas as operações ini e de registro.</span><span class="sxs-lookup"><span data-stu-id="325bd-109">Since only INI, registry, and file operations are listed in the **Install** section, this is a shorthand method of specifying the function should process all INI and registry operations.</span></span>

<span data-ttu-id="325bd-110">O exemplo a seguir mostra como instalar informações de registro usando a função **SetupInstallFromINFSection** .</span><span class="sxs-lookup"><span data-stu-id="325bd-110">The following example shows how to install registry information using the **SetupInstallFromINFSection** function.</span></span>

``` syntax
Test = SetupInstallFromINFSection (
     NULL,                     //Window to own any dialog boxes
                               //created 
     MyInf,                    //INF file containing the section 
     MySection,                //the section to install
     SPINST_ALL ^ SPINST_FILES,//which installation operations 
                               //to process
     NULL,                     //the relative root key
     NULL,                     //the source root path
     0,                        //copy style
     NULL,                     //Message handler routine
     NULL,                     //Context
     NULL,                     //Device info set
     NULL                      //device info data
);
```

<span data-ttu-id="325bd-111">No exemplo, *OwnerWindow* é **nulo** porque apenas as operações de arquivo geram caixas de diálogo e, portanto, uma janela pai não é necessária.</span><span class="sxs-lookup"><span data-stu-id="325bd-111">In the example, *OwnerWindow* is **NULL** because only file operations generate dialog boxes, and thus a parent window is not needed.</span></span> <span data-ttu-id="325bd-112">"MyInf" é o arquivo INF que contém a seção a ser processada.</span><span class="sxs-lookup"><span data-stu-id="325bd-112">"MyInf" is the INF file containing the section to process.</span></span> <span data-ttu-id="325bd-113">O parâmetro "MySection" especifica a seção a ser instalada.</span><span class="sxs-lookup"><span data-stu-id="325bd-113">The parameter, "MySection", specifies the section to be installed.</span></span> <span data-ttu-id="325bd-114">Os sinalizadores combinados, \_ todos os arquivos de rotação de ^ mais ^ \_ , especificam quais operações de instalação processar, nesse caso, todas as operações, exceto operações de arquivo.</span><span class="sxs-lookup"><span data-stu-id="325bd-114">The combined flags, SPINST\_ALL ^ SPINST\_FILES, specify which installation operations to process, in this case, all operations except file operations.</span></span> <span data-ttu-id="325bd-115">O caminho raiz de origem é especificado como "A: \\ ".</span><span class="sxs-lookup"><span data-stu-id="325bd-115">The source root path is specified as "A:\\".</span></span>

<span data-ttu-id="325bd-116">Como nenhuma operação de cópia está sendo processada, os parâmetros *CopyFlags*, *MsgHandler*, *Context*, *DeviceInfoSet* e *DeviceInfoData* não são especificados.</span><span class="sxs-lookup"><span data-stu-id="325bd-116">Since no copy operations are being processed, the *CopyFlags*, *MsgHandler*, *Context*, *DeviceInfoSet*, and *DeviceInfoData* parameters are not specified.</span></span>

 

 



