---
description: Lista os tipos de dados usados pelas DLLs de anexo de configuração de segurança e suas funções de suporte.
ms.assetid: 1d3bdf0d-320c-4b25-9e9b-fda134876979
title: Tipos de dados de gerenciamento de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7efedb32ab545b903c61819042e32b7d83dbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753387"
---
# <a name="security-management-data-types"></a><span data-ttu-id="35b61-103">Tipos de dados de gerenciamento de segurança</span><span class="sxs-lookup"><span data-stu-id="35b61-103">Security Management Data Types</span></span>

<span data-ttu-id="35b61-104">Os tipos de dados de gerenciamento de segurança incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="35b61-104">The security management data types include the following:</span></span>

-   [<span data-ttu-id="35b61-105">Tipos de dados de anexo</span><span class="sxs-lookup"><span data-stu-id="35b61-105">Attachment Data Types</span></span>](#attachment-data-types)
-   [<span data-ttu-id="35b61-106">Tipos de dados de política LSA</span><span class="sxs-lookup"><span data-stu-id="35b61-106">LSA Policy Data Types</span></span>](#lsa-policy-data-types)

## <a name="attachment-data-types"></a><span data-ttu-id="35b61-107">Tipos de dados de anexo</span><span class="sxs-lookup"><span data-stu-id="35b61-107">Attachment Data Types</span></span>

<span data-ttu-id="35b61-108">Os tipos de dados a seguir são usados pelas DLLs de anexo de configuração de segurança e suas funções de suporte.</span><span class="sxs-lookup"><span data-stu-id="35b61-108">The following data types are used by the Security Configuration attachment DLLs and their supporting functions.</span></span>



| <span data-ttu-id="35b61-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="35b61-109">Data type</span></span>                                                    | <span data-ttu-id="35b61-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="35b61-110">Description</span></span>                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35b61-111">**\_contexto de enumeração do SCE \_**</span><span class="sxs-lookup"><span data-stu-id="35b61-111">**SCE\_ENUMERATION\_CONTEXT**</span></span>](sce-enumeration-context.md) | <span data-ttu-id="35b61-112">Usado pela função [**de \_ \_ informações de consulta PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) para navegar pelo banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="35b61-112">Used by the [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) function to navigate through the security database.</span></span>                                                                                                                                              |
| [<span data-ttu-id="35b61-113">**identificador do SCE \_**</span><span class="sxs-lookup"><span data-stu-id="35b61-113">**SCE\_HANDLE**</span></span>](sce-handle.md)                            | <span data-ttu-id="35b61-114">Usado por [**\_ \_ informações de consulta PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) e [**PFSCE \_ definir \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) informações para passar informações entre o anexo e o banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="35b61-114">Used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) to pass information between the attachment and the security database.</span></span>                                                                                 |
| [<span data-ttu-id="35b61-115">**SCESTATUS**</span><span class="sxs-lookup"><span data-stu-id="35b61-115">**SCESTATUS**</span></span>](scestatus.md)                               | <span data-ttu-id="35b61-116">O tipo de dados é usado pela API do conjunto de ferramentas de configuração de segurança para retornar informações sobre os resultados de uma chamada de função.</span><span class="sxs-lookup"><span data-stu-id="35b61-116">Data type is used by the Security Configuration tool set API to return information about the results of a function call.</span></span>                                                                                                                                    |
| [<span data-ttu-id="35b61-117">**identificador de SCESVC \_**</span><span class="sxs-lookup"><span data-stu-id="35b61-117">**SCESVC\_HANDLE**</span></span>](scesvc-handle.md)                      | <span data-ttu-id="35b61-118">Usado por métodos das interfaces [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) e [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) para passar informações entre o snap-in de configuração de segurança e a extensão do snap-in.</span><span class="sxs-lookup"><span data-stu-id="35b61-118">Used by methods of the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) and [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interfaces to pass information between the Security Configuration snap-in and the snap-in extension.</span></span> |
| [<span data-ttu-id="35b61-119">**\_tipo de informação SCESVC \_**</span><span class="sxs-lookup"><span data-stu-id="35b61-119">**SCESVC\_INFO\_TYPE**</span></span>](/windows/desktop/api/Scesvc/ne-scesvc-scesvc_info_type)               | <span data-ttu-id="35b61-120">A enumeração é usada pelas informações de [**consulta do PFSCE \_ \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) e pelo [**PFSCE \_ set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) para indicar o tipo de informações solicitadas ou passadas para o banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="35b61-120">Enumeration is used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) to indicate the type of information requested from or passed to the security database.</span></span>                                                 |



 

## <a name="lsa-policy-data-types"></a><span data-ttu-id="35b61-121">Tipos de dados de política LSA</span><span class="sxs-lookup"><span data-stu-id="35b61-121">LSA Policy Data Types</span></span>

<span data-ttu-id="35b61-122">Os tipos de dados a seguir são usados pelas funções de gerenciamento de política do LSA.</span><span class="sxs-lookup"><span data-stu-id="35b61-122">The following data types are used by the LSA policy management functions.</span></span>



| <span data-ttu-id="35b61-123">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="35b61-123">Data type</span></span>                                                  | <span data-ttu-id="35b61-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="35b61-124">Description</span></span>                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="35b61-125">**\_identificador de enumeração LSA \_**</span><span class="sxs-lookup"><span data-stu-id="35b61-125">**LSA\_ENUMERATION\_HANDLE**</span></span>](lsa-enumeration-handle.md) | <span data-ttu-id="35b61-126">Usado para rastrear enumerações nas quais várias chamadas de função são necessárias.</span><span class="sxs-lookup"><span data-stu-id="35b61-126">Used to track enumerations in which multiple function calls are required.</span></span> |
| [<span data-ttu-id="35b61-127">**identificador de LSA \_**</span><span class="sxs-lookup"><span data-stu-id="35b61-127">**LSA\_HANDLE**</span></span>](lsa-handle.md)                          | <span data-ttu-id="35b61-128">Identificador para um objeto de [**política**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="35b61-128">Handle to a [**Policy**](policy-object.md) object.</span></span>                       |



 

 

 
