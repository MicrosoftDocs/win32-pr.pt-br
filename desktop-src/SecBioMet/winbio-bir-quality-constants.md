---
title: Constantes de WINBIO_BIR_QUALITY (WinBio \_ Types. h)
description: Especifique a qualidade relativa dos dados biométricos no BIR se um valor inteiro de 0 a 100 não tiver sido especificado.
ms.assetid: A42AA21B-9AA5-4DB6-B58F-0776BEC63E6C
topic_type:
- apiref
api_name:
- WINBIO_DATA_QUALITY_NOT_SET
- WINBIO_DATA_QUALITY_NOT_SUPPORTED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1eb0881672c9e3bf51214cff93cb3f68d802b04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086393"
---
# <a name="winbio_bir_quality-constants"></a><span data-ttu-id="5ebb7-103">WINBIO \_ \_ constantes de qualidade Bir</span><span class="sxs-lookup"><span data-stu-id="5ebb7-103">WINBIO\_BIR\_QUALITY Constants</span></span>

<span data-ttu-id="5ebb7-104">Os sinalizadores a seguir são usados pelo membro **dataquality** da estrutura [**de \_ \_ cabeçalho WINBIO Bir**](winbio-bir-header.md) para especificar a qualidade relativa dos dados biométricos no Bir se um valor inteiro de 0 a 100 não tiver sido especificado.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-104">The following flags are used by the **DataQuality** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure to specify the relative quality of biometric data in the BIR if an integer value from 0 to 100 has not been specified.</span></span>



| <span data-ttu-id="5ebb7-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="5ebb7-105">Constant/value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="5ebb7-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ebb7-106">Description</span></span>                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <span data-ttu-id="5ebb7-107"><dt>**WINBIO \_ Qualidade de dados \_ \_ não \_ definida**</dt> <dt> 1</dt></span><span class="sxs-lookup"><span data-stu-id="5ebb7-107"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SET**</dt> <dt> 1</dt></span></span> </dl>                   | <span data-ttu-id="5ebb7-108">As medições de qualidade são suportadas pelo criador do BIR, mas nenhum valor é definido no BIR.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-108">Quality measurements are supported by the BIR creator, but no value is set in the BIR.</span></span><br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <span data-ttu-id="5ebb7-109"><dt>**WINBIO \_ Qualidade de dados \_ \_ não \_ suportada**</dt> <dt> 2</dt></span><span class="sxs-lookup"><span data-stu-id="5ebb7-109"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SUPPORTED**</dt> <dt> 2</dt></span></span> </dl> | <span data-ttu-id="5ebb7-110">As medições de qualidade não são suportadas pelo criador do BIR.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-110">Quality measurements are not supported by the BIR creator.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="5ebb7-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ebb7-111">Requirements</span></span>



| <span data-ttu-id="5ebb7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ebb7-112">Requirement</span></span> | <span data-ttu-id="5ebb7-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5ebb7-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ebb7-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ebb7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5ebb7-115">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5ebb7-115">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="5ebb7-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ebb7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5ebb7-117">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="5ebb7-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5ebb7-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ebb7-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ebb7-119"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ebb7-119"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ebb7-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ebb7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ebb7-121">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="5ebb7-121">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





