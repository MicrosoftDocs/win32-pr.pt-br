---
title: Constantes de WINBIO_ENG_CAP (WinBio \_ Types. h)
description: Especifique os recursos do mecanismo genérico.
ms.assetid: 31C4E8AF-6EF8-43FF-A944-D7363A26BB1A
topic_type:
- apiref
api_name:
- WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT
- WINBIO_ENG_CAP_SPOOF_DETECTION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d69db9f0e15ca0d50aa5ca134fdc74904dec85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645193"
---
# <a name="winbio_eng_cap-constants"></a><span data-ttu-id="7dfcb-103">\_Constantes do \_ Cap WINBIO ENG</span><span class="sxs-lookup"><span data-stu-id="7dfcb-103">WINBIO\_ENG\_CAP Constants</span></span>

<span data-ttu-id="7dfcb-104">As constantes a seguir são valores de **\_ recursos WINBIO** que podem ser usados para especificar recursos genéricos do componente do mecanismo que está conectado a uma unidade biométrica específica.</span><span class="sxs-lookup"><span data-stu-id="7dfcb-104">The following constants are **WINBIO\_CAPABILITIES** values that can be used to specify generic capabilities of the engine component that is connected to a specific biometric unit.</span></span> <span data-ttu-id="7dfcb-105">Você especifica esses recursos no membro **GenericEngineCapabilities** da estrutura [**de \_ \_ \_ informações do mecanismo estendido WINBIO**](winbio-extended-engine-info.md) .</span><span class="sxs-lookup"><span data-stu-id="7dfcb-105">You specify these capabilities in **GenericEngineCapabilities** member of the [**WINBIO\_EXTENDED\_ENGINE\_INFO**](winbio-extended-engine-info.md) structure.</span></span>



| <span data-ttu-id="7dfcb-106">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="7dfcb-106">Constant/value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="7dfcb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7dfcb-107">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span id="WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT"></span><span id="winbio_eng_cap_iterative_improvement"></span><dl> <span data-ttu-id="7dfcb-108"><dt>**WINBIO \_ \_ \_ \_ Aperfeiçoamento interativo do Cap de ENG**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="7dfcb-108"><dt>**WINBIO\_ENG\_CAP\_ITERATIVE\_IMPROVEMENT**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="7dfcb-109">O componente de mecanismo biométrico pode executar melhorias iterativas.</span><span class="sxs-lookup"><span data-stu-id="7dfcb-109">The biometric engine component can perform iterative improvement.</span></span><br/> |
| <span id="WINBIO_ENG_CAP_SPOOF_DETECTION"></span><span id="winbio_eng_cap_spoof_detection"></span><dl> <span data-ttu-id="7dfcb-110"><dt>**WINBIO \_ \_Detecção de \_ spoof \_ de capacidade de ENG**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="7dfcb-110"><dt>**WINBIO\_ENG\_CAP\_SPOOF\_DETECTION**</dt> <dt>0x00000002</dt></span></span> </dl>                   | <span data-ttu-id="7dfcb-111">O componente de mecanismo biométrico pode executar a detecção de falsificação.</span><span class="sxs-lookup"><span data-stu-id="7dfcb-111">The biometric engine component can perform spoof detection.</span></span><br/>       |



## <a name="requirements"></a><span data-ttu-id="7dfcb-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7dfcb-112">Requirements</span></span>



| <span data-ttu-id="7dfcb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dfcb-113">Requirement</span></span> | <span data-ttu-id="7dfcb-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7dfcb-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dfcb-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7dfcb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7dfcb-116">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7dfcb-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="7dfcb-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7dfcb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7dfcb-118">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="7dfcb-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7dfcb-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7dfcb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dfcb-120"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7dfcb-120"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





