---
description: Você pode aplicar a atualização pequena a uma imagem de origem administrativa do MNP2000.msi instalando o patch de exemplo MNP2000. msp criado na geração de um pacote de patch.
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: Aplicando um pacote de patch a uma instalação administrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e0645bdd2c472e725a3a5eeef22693aa35b8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921517"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a><span data-ttu-id="c3fd4-103">Aplicando um pacote de patch a uma instalação administrativa</span><span class="sxs-lookup"><span data-stu-id="c3fd4-103">Applying a Patch Package to an Administrative Installation</span></span>

<span data-ttu-id="c3fd4-104">Você pode aplicar a atualização pequena a uma imagem de origem administrativa do MNP2000.msi instalando o patch de exemplo MNP2000. msp criado na [geração de um pacote de patch](generating-a-patch-package.md).</span><span class="sxs-lookup"><span data-stu-id="c3fd4-104">You may apply the small update to an administrative source image of MNP2000.msi by installing the sample patch MNP2000.msp created in [Generating a Patch Package](generating-a-patch-package.md).</span></span> <span data-ttu-id="c3fd4-105">A atualização pode ser propagada para os usuários solicitando que eles reinstalem o aplicativo da nova imagem de origem administrativa.</span><span class="sxs-lookup"><span data-stu-id="c3fd4-105">The update can then be propagated to users by requesting that they reinstall the application from the new administrative source image.</span></span>

<span data-ttu-id="c3fd4-106">Um administrador pode usar a seguinte linha de comando para atualizar a imagem de origem administrativa localizada em//Server/MNP2000.msi para uma nova imagem de origem que seja a mesma produzida por uma instalação administrativa de um CD-ROM totalmente atualizado.</span><span class="sxs-lookup"><span data-stu-id="c3fd4-106">An administrator can use the following command line to update the administrative source image located at //server/MNP2000.msi to a new source image that is the same as would be produced by an administrative installation from a fully updated CD-ROM.</span></span>

<span data-ttu-id="c3fd4-107">**msiexec/a//Server/MNP2000.msi/p MNP2000. msp**</span><span class="sxs-lookup"><span data-stu-id="c3fd4-107">**msiexec /a //server/MNP2000.msi /p MNP2000.msp**</span></span>

<span data-ttu-id="c3fd4-108">Os membros do grupo de trabalho usando MNP2000, em seguida, devem reinstalar o aplicativo da nova imagem de origem administrativa para receber a atualização.</span><span class="sxs-lookup"><span data-stu-id="c3fd4-108">Members of the workgroup using MNP2000 then must reinstall the application from the new administrative source image to receive the update.</span></span>

<span data-ttu-id="c3fd4-109">Para reinstalar completamente os aplicativos e armazenar em cache o arquivo. msi atualizado no computador do usuário, os usuários podem inserir um dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3fd4-109">To completely reinstall the applications and cache the updated .msi file on the user's computer, users may enter either of the following commands.</span></span>

<span data-ttu-id="c3fd4-110">**msiexec/fvomus//Server/MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="c3fd4-110">**msiexec /fvomus //server/MNP2000.msi**</span></span>

<span data-ttu-id="c3fd4-111">**msiexec/I//Server/MNP2000.msi reinstalar = todas as reinstalaçãomode = vomus**</span><span class="sxs-lookup"><span data-stu-id="c3fd4-111">**msiexec /I //server/MNP2000.msi REINSTALL=ALL REINSTALLMODE=vomus**</span></span>

<span data-ttu-id="c3fd4-112">Para reinstalar apenas o recurso de concerto atualizado e armazenar em cache o arquivo. msi atualizado no computador do usuário, os usuários podem digitar o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3fd4-112">To reinstall only the updated Concert feature and cache the updated .msi file on the user's computer, users may enter the following command.</span></span>

<span data-ttu-id="c3fd4-113">**msiexec/I//Server/MNP2000.msi reinstalar = Concert REINSTALLMODE = vomus**</span><span class="sxs-lookup"><span data-stu-id="c3fd4-113">**msiexec /I //server/MNP2000.msi REINSTALL=Concert REINSTALLMODE=vomus**</span></span>

## <a name="next-example"></a><span data-ttu-id="c3fd4-114">Próximo exemplo</span><span class="sxs-lookup"><span data-stu-id="c3fd4-114">Next example</span></span>

[<span data-ttu-id="c3fd4-115">Um exemplo de localização</span><span class="sxs-lookup"><span data-stu-id="c3fd4-115">A Localization Example</span></span>](a-localization-example.md)

 

 



