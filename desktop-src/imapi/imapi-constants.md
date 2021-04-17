---
title: Constantes do IMAPi
description: O IMAPi define as constantes a seguir.
ms.assetid: 3ae67227-1cee-4e9c-a7fe-228de596030a
topic_type:
- apiref
api_name:
- IMAPI_SECTOR_SIZE
- IMAPI_SECTORS_PER_SECOND_AT_1X_CD
- IMAPI_SECTORS_PER_SECOND_AT_1X_DVD
- IMAPI_SECTORS_PER_SECOND_AT_1X_BD
api_location:
- Imapi2.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb8c6ac1d855509e67ce5e066410f107172d2ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105790400"
---
# <a name="imapi-constants"></a><span data-ttu-id="180c0-103">Constantes do IMAPi</span><span class="sxs-lookup"><span data-stu-id="180c0-103">IMAPI Constants</span></span>

<span data-ttu-id="180c0-104">O IMAPi define as constantes a seguir.</span><span class="sxs-lookup"><span data-stu-id="180c0-104">IMAPI defines the following constants.</span></span>



| <span data-ttu-id="180c0-105">Constante</span><span class="sxs-lookup"><span data-stu-id="180c0-105">Constant</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="180c0-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="180c0-106">Description</span></span>                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span id="IMAPI_SECTOR_SIZE"></span><span id="imapi_sector_size"></span><dl> <span data-ttu-id="180c0-107"><dt>**tamanho do \_ setor IMAPI \_**</dt></span><span class="sxs-lookup"><span data-stu-id="180c0-107"><dt>**IMAPI\_SECTOR\_SIZE**</dt></span></span> </dl>                                                        | <span data-ttu-id="180c0-108">Número de bytes em um setor.</span><span class="sxs-lookup"><span data-stu-id="180c0-108">Number of bytes in a sector.</span></span><br/>                                                  |
| <span id="IMAPI_SECTORS_PER_SECOND_AT_1X_CD"></span><span id="imapi_sectors_per_second_at_1x_cd"></span><dl> <span data-ttu-id="180c0-109"><dt>**\_Setores de IMAPI \_ por \_ segundo \_ em \_ CD de 1x \_**</dt></span><span class="sxs-lookup"><span data-stu-id="180c0-109"><dt>**IMAPI\_SECTORS\_PER\_SECOND\_AT\_1X\_CD**</dt></span></span> </dl>    | <span data-ttu-id="180c0-110">Taxa base de velocidade em que um CD gira, medido em setores por segundo.</span><span class="sxs-lookup"><span data-stu-id="180c0-110">Base rate of speed that a CD spins, measured in sectors per second.</span></span><br/>           |
| <span id="IMAPI_SECTORS_PER_SECOND_AT_1X_DVD"></span><span id="imapi_sectors_per_second_at_1x_dvd"></span><dl> <span data-ttu-id="180c0-111"><dt>**\_Setores IMAPI \_ por \_ segundo \_ em \_ 1x \_ DVD**</dt></span><span class="sxs-lookup"><span data-stu-id="180c0-111"><dt>**IMAPI\_SECTORS\_PER\_SECOND\_AT\_1X\_DVD**</dt></span></span> </dl> | <span data-ttu-id="180c0-112">Taxa base de velocidade em que um DVD gira, medido em setores por segundo.</span><span class="sxs-lookup"><span data-stu-id="180c0-112">Base rate of speed that a DVD spins, measured in sectors per second.</span></span><br/>          |
| <span id="IMAPI_SECTORS_PER_SECOND_AT_1X_BD"></span><span id="imapi_sectors_per_second_at_1x_bd"></span><dl> <span data-ttu-id="180c0-113"><dt>**\_Setores IMAPI \_ por \_ segundo \_ em \_ 1x \_ BD**</dt></span><span class="sxs-lookup"><span data-stu-id="180c0-113"><dt>**IMAPI\_SECTORS\_PER\_SECOND\_AT\_1X\_BD**</dt></span></span> </dl>    | <span data-ttu-id="180c0-114">Taxa base de velocidade que um disco Blu-Ray gira, medido em setores por segundo.</span><span class="sxs-lookup"><span data-stu-id="180c0-114">Base rate of speed that a Blu-ray disc spins, measured in sectors per second.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="180c0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="180c0-115">Requirements</span></span>



| <span data-ttu-id="180c0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="180c0-116">Requirement</span></span> | <span data-ttu-id="180c0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="180c0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="180c0-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="180c0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="180c0-119">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP2\]</span><span class="sxs-lookup"><span data-stu-id="180c0-119">Windows Vista, Windows XP with SP2 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="180c0-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="180c0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="180c0-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="180c0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="180c0-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="180c0-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="180c0-123"><dt>Imapi2. idl</dt></span><span class="sxs-lookup"><span data-stu-id="180c0-123"><dt>Imapi2.idl</dt></span></span> </dl> |



 

 





