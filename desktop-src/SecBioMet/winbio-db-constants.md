---
title: Constantes de WINBIO_DB (WinBio \_ Types. h)
description: Especifique o banco de dados a ser usado para um pool do sistema.
ms.assetid: 2cffa455-5834-4a35-b8d8-f9d1feddcaa1
topic_type:
- apiref
api_name:
- WINBIO_DB_DEFAULT
- WINBIO_DB_BOOTSTRAP
- WINBIO_DB_ONCHIP
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20503e1dc3cd7b5e47651889dd9c67777614593c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085785"
---
# <a name="winbio_db-constants"></a><span data-ttu-id="8db92-103">Constantes do WINBIO \_ DB</span><span class="sxs-lookup"><span data-stu-id="8db92-103">WINBIO\_DB Constants</span></span>

<span data-ttu-id="8db92-104">As constantes a seguir podem ser usadas ao chamar [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para especificar o banco de dados a ser usado para um pool do sistema.</span><span class="sxs-lookup"><span data-stu-id="8db92-104">The following constants can be used when calling [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) to specify the database to be used for a system pool.</span></span>



| <span data-ttu-id="8db92-105">Constante</span><span class="sxs-lookup"><span data-stu-id="8db92-105">Constant</span></span>                                                                                                                                                                         | <span data-ttu-id="8db92-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="8db92-106">Description</span></span>                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <span data-ttu-id="8db92-107"><dt>**padrão do WINBIO \_ DB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8db92-107"><dt>**WINBIO\_DB\_DEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="8db92-108">Cada unidade biométrica no pool de sensores usa o banco de dados padrão especificado na configuração de unidade biométrica padrão.</span><span class="sxs-lookup"><span data-stu-id="8db92-108">Each biometric unit in the sensor pool uses the default database specified in the default biometric unit configuration.</span></span><br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <span data-ttu-id="8db92-109"><dt>**inicialização do WINBIO \_ DB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8db92-109"><dt>**WINBIO\_DB\_BOOTSTRAP**</dt></span></span> </dl> | <span data-ttu-id="8db92-110">Pode ser usado para cenários antes de iniciar o Windows.</span><span class="sxs-lookup"><span data-stu-id="8db92-110">Can be used for scenarios prior to starting Windows.</span></span> <span data-ttu-id="8db92-111">Normalmente, o banco de dados faz parte do chip do sensor ou faz parte do BIOS e só pode ser usado para registro e exclusão de modelo.</span><span class="sxs-lookup"><span data-stu-id="8db92-111">Typically, the database is part of the sensor chip or is part of the BIOS and can only be used for template enrollment and deletion.</span></span><br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <span data-ttu-id="8db92-112"><dt>**WINBIO \_ DB \_ OnChip**</dt></span><span class="sxs-lookup"><span data-stu-id="8db92-112"><dt>**WINBIO\_DB\_ONCHIP**</dt></span></span> </dl>          | <span data-ttu-id="8db92-113">O banco de dados reside no chip do sensor.</span><span class="sxs-lookup"><span data-stu-id="8db92-113">The database resides on the sensor chip.</span></span><br/>                                                                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="8db92-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8db92-114">Requirements</span></span>



| <span data-ttu-id="8db92-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8db92-115">Requirement</span></span> | <span data-ttu-id="8db92-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8db92-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8db92-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8db92-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8db92-118">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8db92-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="8db92-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8db92-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8db92-120">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="8db92-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8db92-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8db92-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8db92-122"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8db92-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8db92-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8db92-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db92-124">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="8db92-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





