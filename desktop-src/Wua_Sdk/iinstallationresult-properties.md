---
description: A interface IInstallationResult define as propriedades a seguir.
ms.assetid: bd6cd5ae-2e43-4ac3-8ce7-ac80b7fc5cb8
title: Propriedades de IInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78783b6758ab30d6a77c07cd71111486f3a7343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010550"
---
# <a name="iinstallationresult-properties"></a><span data-ttu-id="34147-103">Propriedades de IInstallationResult</span><span class="sxs-lookup"><span data-stu-id="34147-103">IInstallationResult Properties</span></span>

<span data-ttu-id="34147-104">A interface [**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) define as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="34147-104">The [**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) interface defines the following properties.</span></span>



| <span data-ttu-id="34147-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="34147-105">Property</span></span>                                                     | <span data-ttu-id="34147-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="34147-106">Description</span></span>                                                                                                                            |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34147-107">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="34147-107">**HResult**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_hresult)               | <span data-ttu-id="34147-108">Obtém o **HRESULT** da exceção, se houver, que é gerado durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="34147-108">Gets the **HRESULT** of the exception, if any, that is raised during the installation.</span></span>                                                 |
| [<span data-ttu-id="34147-109">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="34147-109">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_rebootrequired) | <span data-ttu-id="34147-110">Obtém um valor booliano que indica se você deve reiniciar o computador para concluir a instalação ou desinstalação de uma atualização.</span><span class="sxs-lookup"><span data-stu-id="34147-110">Gets a Boolean value that indicates whether you must restart the computer to complete the installation or uninstallation of an update.</span></span> |
| [<span data-ttu-id="34147-111">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="34147-111">**ResultCode**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_resultcode)         | <span data-ttu-id="34147-112">Obtém um valor de [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) que especifica o resultado de uma operação em uma atualização.</span><span class="sxs-lookup"><span data-stu-id="34147-112">Gets an [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) value that specifies the result of an operation on an update.</span></span>               |



 

 

 



