---
description: Depois de criar uma extensão de snap-in de anexo, você deve registrá-la para o MMC e os snap-ins de configuração de segurança para localizá-los e usá-los.
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: Registrando uma extensão de snap-in de anexo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7726131325433aa920ff22c9b71a4f7184000a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789484"
---
# <a name="registering-an-attachment-snap-in-extension"></a><span data-ttu-id="008b9-103">Registrando uma extensão de snap-in de anexo</span><span class="sxs-lookup"><span data-stu-id="008b9-103">Registering an Attachment Snap-in Extension</span></span>

<span data-ttu-id="008b9-104">Depois de criar uma extensão de snap-in de anexo, você deve registrá-la para o MMC e os snap-ins de configuração de segurança para localizá-los e usá-los.</span><span class="sxs-lookup"><span data-stu-id="008b9-104">After you create an attachment snap-in extension, you must register it in order for the MMC and the Security Configuration snap-ins to locate and use it.</span></span>

<span data-ttu-id="008b9-105">Seu snap-in de anexo deve estender o namespace de snap-ins de configuração de segurança adicionando seu próprio nó, conforme descrito no procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="008b9-105">Your attachment snap-in must extend the Security Configuration snap-ins namespace by adding its own node as described in the following procedure.</span></span>

<span data-ttu-id="008b9-106">**Para instalar e registrar a extensão de snap-in de anexo**</span><span class="sxs-lookup"><span data-stu-id="008b9-106">**To install and register the attachment snap-in extension**</span></span>

1.  <span data-ttu-id="008b9-107">Registre a extensão do snap-in na seguinte chave do registro.</span><span class="sxs-lookup"><span data-stu-id="008b9-107">Register the snap-in extension under the following registry key.</span></span> <span data-ttu-id="008b9-108">Não crie uma chave autônoma no snap-in; extensões de snap-ins de anexo só devem ser extensões.</span><span class="sxs-lookup"><span data-stu-id="008b9-108">Do not create a StandAlone key under the snap-in; attachment snap-ins extensions must only be extensions.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             MMC
                SnapIns
    ```

2.  <span data-ttu-id="008b9-109">Registre a extensão de snap-in de anexo nas seguintes subchaves.</span><span class="sxs-lookup"><span data-stu-id="008b9-109">Register the attachment snap-in extension under the following subkeys.</span></span> <span data-ttu-id="008b9-110">Isso pode ser feito como parte das implementações de função **DllRegisterServer** e **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="008b9-110">This can be done as part of your **DllRegisterServer** and **DllUnregisterServer** function implementations.</span></span>

    <span data-ttu-id="008b9-111">Namespace de [modelos de segurança](security-templates.md) :</span><span class="sxs-lookup"><span data-stu-id="008b9-111">[Security Templates](security-templates.md) namespace:</span></span>

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   24a7f717-1f0c-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

    <span data-ttu-id="008b9-112">[Configuração de segurança e namespace de análise](security-configuration-and-analysis.md) :</span><span class="sxs-lookup"><span data-stu-id="008b9-112">[Security Configuration and Analysis](security-configuration-and-analysis.md) namespace:</span></span>

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   678050c7-1ff8-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

 

 



