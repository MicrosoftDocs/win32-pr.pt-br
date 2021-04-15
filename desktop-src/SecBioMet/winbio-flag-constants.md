---
title: Constantes de WINBIO_FLAG (WinBio \_ Types. h)
description: Especifique a configuração da unidade biométrica e as características de acesso para a nova sessão.
ms.assetid: 82b57023-6c27-433d-bf13-f136f501fc60
topic_type:
- apiref
api_name:
- WINBIO_FLAG_DEFAULT
- WINBIO_FLAG_BASIC
- WINBIO_FLAG_ADVANCED
- WINBIO_FLAG_RAW
- WINBIO_FLAG_MAINTENANCE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed632b5f15cc3d6a7ac6b0c6c70a2b3431b73db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369344"
---
# <a name="winbio_flag-constants"></a><span data-ttu-id="c1d75-103">\_Constantes de sinalizador WINBIO</span><span class="sxs-lookup"><span data-stu-id="c1d75-103">WINBIO\_FLAG Constants</span></span>

<span data-ttu-id="c1d75-104">As constantes a seguir podem ser usadas na função [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para especificar a configuração de unidade biométrica e as características de acesso para a nova sessão.</span><span class="sxs-lookup"><span data-stu-id="c1d75-104">The following constants can be used in the [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) function to specify biometric unit configuration and access characteristics for the new session.</span></span>



| <span data-ttu-id="c1d75-105">Constante</span><span class="sxs-lookup"><span data-stu-id="c1d75-105">Constant</span></span>                                                                                                                                                                                     | <span data-ttu-id="c1d75-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1d75-106">Description</span></span>                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <span data-ttu-id="c1d75-107"><dt>**\_padrão de sinalizador WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d75-107"><dt>**WINBIO\_FLAG\_DEFAULT**</dt></span></span> </dl>             | <span data-ttu-id="c1d75-108">Sinalizador de configuração do sensor.</span><span class="sxs-lookup"><span data-stu-id="c1d75-108">Sensor configuration flag.</span></span> <span data-ttu-id="c1d75-109">As unidades biométricas operam da maneira especificada durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="c1d75-109">The biometric units operate in the manner specified during installation.</span></span><br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <span data-ttu-id="c1d75-110"><dt>**\_sinalizador WINBIO \_ básico**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d75-110"><dt>**WINBIO\_FLAG\_BASIC**</dt></span></span> </dl>                   | <span data-ttu-id="c1d75-111">Sinalizador de configuração do sensor.</span><span class="sxs-lookup"><span data-stu-id="c1d75-111">Sensor configuration flag.</span></span> <span data-ttu-id="c1d75-112">As unidades biométricas operam apenas como dispositivos básicos de captura.</span><span class="sxs-lookup"><span data-stu-id="c1d75-112">The biometric units operate only as basic capture devices.</span></span><br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <span data-ttu-id="c1d75-113"><dt>**\_sinalizador WINBIO \_ avançado**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d75-113"><dt>**WINBIO\_FLAG\_ADVANCED**</dt></span></span> </dl>          | <span data-ttu-id="c1d75-114">Sinalizador de configuração do sensor.</span><span class="sxs-lookup"><span data-stu-id="c1d75-114">Sensor configuration flag.</span></span> <span data-ttu-id="c1d75-115">As unidades biométricas usam recursos internos de processamento e armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c1d75-115">The biometric units use internal processing and storage capabilities.</span></span><br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <span data-ttu-id="c1d75-116"><dt>**WINBIO de \_ sinalizador \_ bruto**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d75-116"><dt>**WINBIO\_FLAG\_RAW**</dt></span></span> </dl>                         | <span data-ttu-id="c1d75-117">Sinalizador de acesso desejado.</span><span class="sxs-lookup"><span data-stu-id="c1d75-117">Desired access flag.</span></span> <span data-ttu-id="c1d75-118">O aplicativo cliente captura dados biométricos brutos usando [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span><span class="sxs-lookup"><span data-stu-id="c1d75-118">The client application captures raw biometric data using [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span></span><br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <span data-ttu-id="c1d75-119"><dt>**\_manutenção do sinalizador WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d75-119"><dt>**WINBIO\_FLAG\_MAINTENANCE**</dt></span></span> </dl> | <span data-ttu-id="c1d75-120">Sinalizador de acesso desejado.</span><span class="sxs-lookup"><span data-stu-id="c1d75-120">Desired access flag.</span></span> <span data-ttu-id="c1d75-121">O cliente executa operações de controle definidas pelo fornecedor em uma unidade biométrica chamando [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span><span class="sxs-lookup"><span data-stu-id="c1d75-121">The client performs vendor-defined control operations on a biometric unit by calling [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c1d75-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1d75-122">Requirements</span></span>



| <span data-ttu-id="c1d75-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1d75-123">Requirement</span></span> | <span data-ttu-id="c1d75-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c1d75-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d75-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1d75-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c1d75-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c1d75-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="c1d75-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1d75-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c1d75-128">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="c1d75-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c1d75-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1d75-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1d75-130"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1d75-130"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1d75-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1d75-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1d75-132">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="c1d75-132">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





