---
title: Constantes de WINBIO_BIR_DATA_FLAGS (WinBio \_ Types. h)
description: Especifique a condição dos dados.
ms.assetid: F6F7F68A-3294-4AF8-A1A7-C6A869A2CC3C
topic_type:
- apiref
api_name:
- WINBIO_DATA_FLAG_PRIVACY
- WINBIO_DATA_FLAG_INTEGRITY
- WINBIO_DATA_FLAG_SIGNED
- WINBIO_DATA_FLAG_RAW
- WINBIO_DATA_FLAG_INTERMEDIATE
- WINBIO_DATA_FLAG_PROCESSED
- WINBIO_DATA_FLAG_OPTION_MASK_PRESENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8195cf17040c35b9e42f8977b36c5ddc6f2ea33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369918"
---
# <a name="winbio_bir_data_flags-constants"></a><span data-ttu-id="40a69-103">\_Constantes de \_ sinalizadores de dados WINBIO Bir \_</span><span class="sxs-lookup"><span data-stu-id="40a69-103">WINBIO\_BIR\_DATA\_FLAGS Constants</span></span>

<span data-ttu-id="40a69-104">As constantes a seguir são usadas pelo membro **dataFlags** da estrutura de [**\_ \_ cabeçalho WINBIO Bir**](winbio-bir-header.md) .</span><span class="sxs-lookup"><span data-stu-id="40a69-104">The following constants are used by the **DataFlags** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure.</span></span>



| <span data-ttu-id="40a69-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="40a69-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="40a69-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="40a69-106">Description</span></span>                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <span data-ttu-id="40a69-107"><dt>**WINBIO \_ \_Sinalizador de \_ privacidade de dados**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="40a69-107"><dt>**WINBIO\_DATA\_FLAG\_PRIVACY**</dt> <dt>0x02</dt></span></span> </dl>                                       | <span data-ttu-id="40a69-108">Os dados estão criptografados.</span><span class="sxs-lookup"><span data-stu-id="40a69-108">The data is encrypted.</span></span><br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <span data-ttu-id="40a69-109"><dt>**WINBIO \_ \_ \_ Integridade de sinalizador de dados**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="40a69-109"><dt>**WINBIO\_DATA\_FLAG\_INTEGRITY**</dt> <dt>0x01</dt></span></span> </dl>                                 | <span data-ttu-id="40a69-110">Os dados são assinados digitalmente ou protegidos por um MAC (código de autenticação de mensagens).</span><span class="sxs-lookup"><span data-stu-id="40a69-110">The data is digitally signed or is protected by a message authentication code (MAC).</span></span><br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <span data-ttu-id="40a69-111"><dt>**WINBIO \_ Sinalizador de dados 0x04 \_ \_ assinado**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="40a69-111"><dt>**WINBIO\_DATA\_FLAG\_SIGNED**</dt> <dt>0x04</dt></span></span> </dl>                                          | <span data-ttu-id="40a69-112">Se esse sinalizador e o sinalizador de **\_ integridade do \_ sinalizador \_ de dados WINBIO** estiverem definidos, os dados serão assinados.</span><span class="sxs-lookup"><span data-stu-id="40a69-112">If this flag and the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag are set, the data is signed.</span></span> <span data-ttu-id="40a69-113">Se esse sinalizador não for definido, mas o sinalizador de **\_ integridade do \_ sinalizador \_ de dados WINBIO** for definido, um Mac será calculado nos dados.</span><span class="sxs-lookup"><span data-stu-id="40a69-113">If this flag is not set but the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag is set, a MAC is computed on the data.</span></span><br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <span data-ttu-id="40a69-114"><dt>**WINBIO \_ 0x20 de sinalizador de dados \_ \_ brutos**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="40a69-114"><dt>**WINBIO\_DATA\_FLAG\_RAW**</dt> <dt>0x20</dt></span></span> </dl>                                                   | <span data-ttu-id="40a69-115">Os dados estão no formato com o qual foram capturados.</span><span class="sxs-lookup"><span data-stu-id="40a69-115">The data is in the format with which it was captured.</span></span><br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <span data-ttu-id="40a69-116"><dt>**WINBIO \_ Sinalizador de dados \_ \_ intermediário**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="40a69-116"><dt>**WINBIO\_DATA\_FLAG\_INTERMEDIATE**</dt> <dt>0x40</dt></span></span> </dl>                        | <span data-ttu-id="40a69-117">Os dados não são brutos, mas não foram completamente processados.</span><span class="sxs-lookup"><span data-stu-id="40a69-117">The data is not raw but has not been completely processed.</span></span><br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <span data-ttu-id="40a69-118"><dt>**WINBIO \_ Sinalizador de dados \_ \_ processado**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="40a69-118"><dt>**WINBIO\_DATA\_FLAG\_PROCESSED**</dt> <dt>0x80</dt></span></span> </dl>                                 | <span data-ttu-id="40a69-119">Os dados foram processados.</span><span class="sxs-lookup"><span data-stu-id="40a69-119">The data has been processed.</span></span><br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <span data-ttu-id="40a69-120"><dt>**WINBIO \_ Máscara de opção de sinalizador de dados \_ \_ \_ \_ presente**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="40a69-120"><dt>**WINBIO\_DATA\_FLAG\_OPTION\_MASK\_PRESENT**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="40a69-121">A máscara do sinalizador.</span><span class="sxs-lookup"><span data-stu-id="40a69-121">The flag mask.</span></span> <span data-ttu-id="40a69-122">Esse valor é sempre um (1).</span><span class="sxs-lookup"><span data-stu-id="40a69-122">This value is always one (1).</span></span><br/>                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="40a69-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40a69-123">Requirements</span></span>



| <span data-ttu-id="40a69-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="40a69-124">Requirement</span></span> | <span data-ttu-id="40a69-125">Valor</span><span class="sxs-lookup"><span data-stu-id="40a69-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40a69-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40a69-126">Minimum supported client</span></span><br/> | <span data-ttu-id="40a69-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="40a69-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="40a69-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40a69-128">Minimum supported server</span></span><br/> | <span data-ttu-id="40a69-129">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="40a69-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="40a69-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40a69-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="40a69-131"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40a69-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40a69-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="40a69-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40a69-133">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="40a69-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





