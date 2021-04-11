---
description: A interface IUpdateInstallationResult define as propriedades a seguir.
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: Propriedades de IUpdateInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b2e2792215d8d927d6e6157c82e37193e74d2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164607"
---
# <a name="iupdateinstallationresult-properties"></a><span data-ttu-id="10488-103">Propriedades de IUpdateInstallationResult</span><span class="sxs-lookup"><span data-stu-id="10488-103">IUpdateInstallationResult Properties</span></span>

<span data-ttu-id="10488-104">A interface [**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) define as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="10488-104">The [**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) interface defines the following properties.</span></span>



| <span data-ttu-id="10488-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="10488-105">Property</span></span>                                                           | <span data-ttu-id="10488-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="10488-106">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10488-107">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="10488-107">**HResult**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | <span data-ttu-id="10488-108">Obtém o valor de exceção **HRESULT** que é gerado durante a operação em uma atualização.</span><span class="sxs-lookup"><span data-stu-id="10488-108">Gets the **HRESULT** exception value that is raised during the operation on an update.</span></span>                                            |
| [<span data-ttu-id="10488-109">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="10488-109">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | <span data-ttu-id="10488-110">Obtém um valor booliano que indica se uma reinicialização do sistema é necessária em um computador para concluir a instalação de uma atualização.</span><span class="sxs-lookup"><span data-stu-id="10488-110">Gets a Boolean value that indicates whether a system restart is required on a computer to complete the installation of an update.</span></span> |
| [<span data-ttu-id="10488-111">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="10488-111">**ResultCode**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | <span data-ttu-id="10488-112">Obtém um valor de [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) que especifica o resultado de uma operação em uma atualização.</span><span class="sxs-lookup"><span data-stu-id="10488-112">Gets an [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) value that specifies the result of an operation on an update.</span></span>          |



 

 

 



