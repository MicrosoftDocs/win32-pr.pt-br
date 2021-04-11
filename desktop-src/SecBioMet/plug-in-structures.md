---
title: Estruturas de plug-in
description: Estruturas para desenvolvimento de aplicativo cliente pela API de Windows Biometric Framework.
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- API do Windows Biometric Framework API Windows Biometric Framework, estruturas de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193b5a99f30c76e8e6e2ab7ebf0242cf56905816
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292607"
---
# <a name="plug-in-structures"></a><span data-ttu-id="a5847-104">Estruturas de plug-in</span><span class="sxs-lookup"><span data-stu-id="a5847-104">Plug-in Structures</span></span>

<span data-ttu-id="a5847-105">As estruturas a seguir têm suporte para o desenvolvimento de aplicativos cliente pela API Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="a5847-105">The following structures are supported for client application development by the Windows Biometric Framework API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a5847-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a5847-106">In this section</span></span>



| <span data-ttu-id="a5847-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="a5847-107">Topic</span></span>                                                                                                | <span data-ttu-id="a5847-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a5847-108">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5847-109">**\_política de conta do WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="a5847-109">**WINBIO\_ACCOUNT\_POLICY**</span></span>](winbio-account-policy.md)<br/>                                  | <span data-ttu-id="a5847-110">Contém uma política de antifalsificação padrão ou específica da conta.</span><span class="sxs-lookup"><span data-stu-id="a5847-110">Contains either a default or account-specific antispoofing policy.</span></span><br/>                                                         |
| [<span data-ttu-id="a5847-111">**\_versão da \_ interface do adaptador WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="a5847-111">**WINBIO\_ADAPTER\_INTERFACE\_VERSION**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | <span data-ttu-id="a5847-112">Contém um número de versão principal e secundária usado nas tabelas do mecanismo, do sensor e da interface do adaptador de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a5847-112">Contains a major and minor version number used in the engine, sensor, and storage adapter interface tables.</span></span><br/>                |
| [<span data-ttu-id="a5847-113">**\_interface do mecanismo do WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="a5847-113">**WINBIO\_ENGINE\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | <span data-ttu-id="a5847-114">Contém ponteiros para suas funções de adaptador de mecanismo personalizadas.</span><span class="sxs-lookup"><span data-stu-id="a5847-114">Contains pointers to your custom engine adapter functions.</span></span><br/>                                                                 |
| [<span data-ttu-id="a5847-115">**\_parâmetros de \_ registro ESTENDIdo WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="a5847-115">**WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS**</span></span>](winbio-extended-enrollment-parameters.md)<br/> | <span data-ttu-id="a5847-116">Contém informações adicionais que um adaptador de mecanismo precisa para criar um modelo de registro.</span><span class="sxs-lookup"><span data-stu-id="a5847-116">Contains additional information that an engine adapter needs to create an enrollment template.</span></span> <br/>                            |
| [<span data-ttu-id="a5847-117">**PIPELINE de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="a5847-117">**WINBIO\_PIPELINE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | <span data-ttu-id="a5847-118">Contém informações de contexto compartilhado usadas pelos componentes do sensor, do mecanismo e do adaptador de armazenamento em uma única unidade biométrica.</span><span class="sxs-lookup"><span data-stu-id="a5847-118">Contains shared context information used by the sensor, engine, and storage adapter components in a single biometric unit.</span></span><br/> |
| [<span data-ttu-id="a5847-119">**\_interface do sensor WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="a5847-119">**WINBIO\_SENSOR\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | <span data-ttu-id="a5847-120">Contém ponteiros para as funções do adaptador do sensor personalizado.</span><span class="sxs-lookup"><span data-stu-id="a5847-120">Contains pointers to your custom sensor adapter functions.</span></span><br/>                                                                 |
| [<span data-ttu-id="a5847-121">**\_interface de armazenamento WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="a5847-121">**WINBIO\_STORAGE\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | <span data-ttu-id="a5847-122">Contém ponteiros para suas funções de adaptador de armazenamento personalizadas.</span><span class="sxs-lookup"><span data-stu-id="a5847-122">Contains pointers to your custom storage adapter functions.</span></span><br/>                                                                |
| [<span data-ttu-id="a5847-123">**\_registro de armazenamento WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="a5847-123">**WINBIO\_STORAGE\_RECORD**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | <span data-ttu-id="a5847-124">Contém um modelo biométrico e dados associados em um formato padrão.</span><span class="sxs-lookup"><span data-stu-id="a5847-124">Contains a biometric template and associated data in a standard format.</span></span><br/>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="a5847-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5847-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5847-126">Referência de plug-in</span><span class="sxs-lookup"><span data-stu-id="a5847-126">Plug-in Reference</span></span>](plug-in-reference.md)
</dt> <dt>

[<span data-ttu-id="a5847-127">Funções de plug-in</span><span class="sxs-lookup"><span data-stu-id="a5847-127">Plug-in Functions</span></span>](plug-in-functions.md)
</dt> <dt>

[<span data-ttu-id="a5847-128">**WbioQueryEngineInterface**</span><span class="sxs-lookup"><span data-stu-id="a5847-128">**WbioQueryEngineInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)
</dt> <dt>

[<span data-ttu-id="a5847-129">**WbioQuerySensorInterface**</span><span class="sxs-lookup"><span data-stu-id="a5847-129">**WbioQuerySensorInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)
</dt> <dt>

[<span data-ttu-id="a5847-130">**WbioQueryStorageInterface**</span><span class="sxs-lookup"><span data-stu-id="a5847-130">**WbioQueryStorageInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)
</dt> </dl>

 

 





