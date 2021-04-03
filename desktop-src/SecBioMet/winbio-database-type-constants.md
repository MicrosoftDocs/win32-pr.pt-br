---
title: Constantes de WINBIO_DATABASE_TYPE (WinBio \_ Types. h)
description: Sinalizadores que podem ser usados para o membro Attributes da \_ estrutura de esquema de armazenamento WINBIO \_ .
ms.assetid: 07e7e91c-3ca6-41cd-a2c7-ac43bb5156a6
topic_type:
- apiref
api_name:
- WINBIO_DATABASE_TYPE_MASK
- WINBIO_DATABASE_TYPE_FILE
- WINBIO_DATABASE_TYPE_DBMS
- WINBIO_DATABASE_TYPE_ONCHIP
- WINBIO_DATABASE_TYPE_SMARTCARD
- WINBIO_DATABASE_FLAG_MASK
- WINBIO_DATABASE_FLAG_REMOVABLE
- WINBIO_DATABASE_FLAG_REMOTE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acd67f49c5fa689fb4418789aae7c4d6c9a305a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644656"
---
# <a name="winbio_database_type-constants"></a><span data-ttu-id="bf85d-103">\_Constantes de tipo de banco de dados WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="bf85d-103">WINBIO\_DATABASE\_TYPE Constants</span></span>

<span data-ttu-id="bf85d-104">Os sinalizadores a seguir podem ser usados para o membro **Attributes** da estrutura de [**\_ \_ esquema de armazenamento WINBIO**](winbio-storage-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="bf85d-104">The following flags can be used for the **Attributes** member of the [**WINBIO\_STORAGE\_SCHEMA**](winbio-storage-schema.md) structure.</span></span>



| <span data-ttu-id="bf85d-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="bf85d-105">Constant/value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="bf85d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf85d-106">Description</span></span>                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <span data-ttu-id="bf85d-107"><dt>**WINBIO \_ \_ \_ Máscara de tipo de banco de dados**</dt> <dt>0x0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="bf85d-107"><dt>**WINBIO\_DATABASE\_TYPE\_MASK**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                | <span data-ttu-id="bf85d-108">Representa uma máscara para todos os \_ bits de tipo \_ .</span><span class="sxs-lookup"><span data-stu-id="bf85d-108">Represents a mask for all of the \_TYPE\_ bits.</span></span><br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <span data-ttu-id="bf85d-109"><dt>**WINBIO \_ \_ \_ Arquivo de tipo de banco de dados**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="bf85d-109"><dt>**WINBIO\_DATABASE\_TYPE\_FILE**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="bf85d-110">O banco de dados está contido em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="bf85d-110">The database is contained in a file.</span></span><br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <span data-ttu-id="bf85d-111"><dt>**WINBIO \_ Tipo de banco de dados \_ \_ DBMS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="bf85d-111"><dt>**WINBIO\_DATABASE\_TYPE\_DBMS**</dt> <dt>0x00000002</dt></span></span> </dl>                | <span data-ttu-id="bf85d-112">O banco de dados é gerenciado por um componente de DBMS (sistema de gerenciamento de banco de dados) externo, como Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bf85d-112">The database is managed by an external database management system (DBMS) component, such as Microsoft SQL Server.</span></span><br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <span data-ttu-id="bf85d-113"><dt>**WINBIO \_ Tipo de banco de dados \_ \_ OnChip**</dt> <dt>0x00000003</dt></span><span class="sxs-lookup"><span data-stu-id="bf85d-113"><dt>**WINBIO\_DATABASE\_TYPE\_ONCHIP**</dt> <dt>0x00000003</dt></span></span> </dl>          | <span data-ttu-id="bf85d-114">O banco de dados reside no sensor biométrico.</span><span class="sxs-lookup"><span data-stu-id="bf85d-114">The database resides on the biometric sensor.</span></span><br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <span data-ttu-id="bf85d-115"><dt>**WINBIO \_ \_ \_ Cartão inteligente de tipo de banco de dados**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="bf85d-115"><dt>**WINBIO\_DATABASE\_TYPE\_SMARTCARD**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="bf85d-116">O banco de dados reside em um cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="bf85d-116">The database resides on a smart card.</span></span><br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <span data-ttu-id="bf85d-117"><dt>**WINBIO \_ \_ \_ Máscara de sinalizador de banco de dados**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="bf85d-117"><dt>**WINBIO\_DATABASE\_FLAG\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl>                | <span data-ttu-id="bf85d-118">Representa uma máscara para todos os \_ bits de sinalizador \_ .</span><span class="sxs-lookup"><span data-stu-id="bf85d-118">Represents a mask for all of the \_FLAG\_ bits.</span></span><br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <span data-ttu-id="bf85d-119"><dt>**WINBIO \_ 0x00010000 \_ \_ removível do sinalizador de banco de dados**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bf85d-119"><dt>**WINBIO\_DATABASE\_FLAG\_REMOVABLE**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="bf85d-120">A mídia de armazenamento que contém o banco de dados pode ser fisicamente removida do computador.</span><span class="sxs-lookup"><span data-stu-id="bf85d-120">The storage medium containing the database can be physically removed from the computer.</span></span><br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <span data-ttu-id="bf85d-121"><dt>**WINBIO \_ 0x00020000 \_ \_ remoto do sinalizador de banco de dados**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bf85d-121"><dt>**WINBIO\_DATABASE\_FLAG\_REMOTE**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="bf85d-122">O banco de dados reside em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="bf85d-122">The database resides on a remote computer.</span></span><br/>                                                                        |



## <a name="requirements"></a><span data-ttu-id="bf85d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf85d-123">Requirements</span></span>



| <span data-ttu-id="bf85d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf85d-124">Requirement</span></span> | <span data-ttu-id="bf85d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="bf85d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf85d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf85d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bf85d-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bf85d-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="bf85d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf85d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bf85d-129">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="bf85d-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="bf85d-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf85d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf85d-131"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf85d-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf85d-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf85d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf85d-133">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="bf85d-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





