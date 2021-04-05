---
title: Constantes BFT (Ntdsbcli. h)
description: As constantes BFT são usadas como sinalizadores de bits para identificar diferentes tipos de arquivo em um Active Directory Domain Services backup.
ms.assetid: 3658a657-d9e3-4fbf-9120-4b0205b81a36
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- BFT_LOG_DIRECTORY
- BFT_DATABASE_DIRECTORY
- BFT_DIRECTORY
- BFT_LOG
- BFT_LOG_DIR
- BFT_CHECKPOINT_DIR
- BFT_NTDS_DATABASE
- BFT_PATCH_FILE
- BFT_UNKNOWN
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9607b5e61e5689d8895b39a11aa7e813fc7fcbe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918293"
---
# <a name="bft-constants"></a><span data-ttu-id="e7fb4-103">Constantes BFT</span><span class="sxs-lookup"><span data-stu-id="e7fb4-103">BFT Constants</span></span>

<span data-ttu-id="e7fb4-104">As constantes BFT são usadas como sinalizadores de bits para identificar diferentes tipos de arquivo em um Active Directory Domain Services backup.</span><span class="sxs-lookup"><span data-stu-id="e7fb4-104">The BFT constants are used as bit flags to identify different file types in an Active Directory Domain Services backup.</span></span>

<dl> <dt>

<span data-ttu-id="e7fb4-105"><span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**\_diretório de log \_ do BFT**</span><span class="sxs-lookup"><span data-stu-id="e7fb4-105"><span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**BFT\_LOG\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7fb4-106">0x20</span><span class="sxs-lookup"><span data-stu-id="e7fb4-106">0x20</span></span>
</dt> <dt>



<span data-ttu-id="e7fb4-107">O arquivo pertence ao diretório de log.</span><span class="sxs-lookup"><span data-stu-id="e7fb4-107">The file belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7fb4-108"><span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**\_diretório de banco de dados BFT \_**</span><span class="sxs-lookup"><span data-stu-id="e7fb4-108"><span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**BFT\_DATABASE\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7fb4-109">0x40</span><span class="sxs-lookup"><span data-stu-id="e7fb4-109">0x40</span></span>
</dt> <dt>



<span data-ttu-id="e7fb4-110">O arquivo pertence ao diretório do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e7fb4-110">The file belongs in the database directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7fb4-111"><span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**\_diretório BFT**</span><span class="sxs-lookup"><span data-stu-id="e7fb4-111"><span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**BFT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7fb4-112">0x80</span><span class="sxs-lookup"><span data-stu-id="e7fb4-112">0x80</span></span>
</dt> <dt>



<span data-ttu-id="e7fb4-113">O caminho especificado é um diretório e não um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e7fb4-113">The path specified is a directory and not a file name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7fb4-114"><span id="BFT_LOG"></span><span id="bft_log"></span>**LOG do BFT \_**</span><span class="sxs-lookup"><span data-stu-id="e7fb4-114"><span id="BFT_LOG"></span><span id="bft_log"></span>**BFT\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7fb4-115">0x21</span><span class="sxs-lookup"><span data-stu-id="e7fb4-115">0x21</span></span>
</dt> <dt>



<span data-ttu-id="e7fb4-116">Especifica um arquivo de log que pertence ao diretório de log.</span><span class="sxs-lookup"><span data-stu-id="e7fb4-116">Specifies a log file that belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7fb4-117"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**Dir. de log do BFT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e7fb4-117"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT\_LOG\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7fb4-118">0x22</span><span class="sxs-lookup"><span data-stu-id="e7fb4-118">0x22</span></span>
</dt> <dt>



<span data-ttu-id="e7fb4-119">O arquivo é o caminho do diretório de log.</span><span class="sxs-lookup"><span data-stu-id="e7fb4-119">The file is the path of the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7fb4-120"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT de \_ ponto de verificação de \_ diretório**</span><span class="sxs-lookup"><span data-stu-id="e7fb4-120"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT\_CHECKPOINT\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7fb4-121">0x23</span><span class="sxs-lookup"><span data-stu-id="e7fb4-121">0x23</span></span>
</dt> <dt>



<span data-ttu-id="e7fb4-122">O arquivo é o caminho do diretório de ponto de verificação.</span><span class="sxs-lookup"><span data-stu-id="e7fb4-122">The file is the path of the checkpoint directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7fb4-123"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_banco de \_ dados NTDS BFT**</span><span class="sxs-lookup"><span data-stu-id="e7fb4-123"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7fb4-124">0x44</span><span class="sxs-lookup"><span data-stu-id="e7fb4-124">0x44</span></span>
</dt> <dt>



<span data-ttu-id="e7fb4-125">O arquivo é um banco de dados de serviço de diretório que pertence ao diretório do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e7fb4-125">The file is a directory service database that belongs in the database directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7fb4-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_arquivo de patch do BFT \_**</span><span class="sxs-lookup"><span data-stu-id="e7fb4-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT\_PATCH\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7fb4-127">0x25</span><span class="sxs-lookup"><span data-stu-id="e7fb4-127">0x25</span></span>
</dt> <dt>



<span data-ttu-id="e7fb4-128">O arquivo é um arquivo de patch que pertence ao diretório de log.</span><span class="sxs-lookup"><span data-stu-id="e7fb4-128">The file is a patch file that belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7fb4-129"><span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="e7fb4-129"><span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7fb4-130">0x0F</span><span class="sxs-lookup"><span data-stu-id="e7fb4-130">0x0F</span></span>
</dt> <dt>



<span data-ttu-id="e7fb4-131">O arquivo não pode ser reconhecido.</span><span class="sxs-lookup"><span data-stu-id="e7fb4-131">The file cannot be recognized.</span></span> <span data-ttu-id="e7fb4-132">O arquivo não coincide com os nomes de arquivo e tipos de arquivo conhecidos.</span><span class="sxs-lookup"><span data-stu-id="e7fb4-132">The file does not coincide with the known file names and file types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7fb4-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7fb4-133">Requirements</span></span>



| <span data-ttu-id="e7fb4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7fb4-134">Requirement</span></span> | <span data-ttu-id="e7fb4-135">Valor</span><span class="sxs-lookup"><span data-stu-id="e7fb4-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7fb4-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7fb4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e7fb4-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7fb4-137">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="e7fb4-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7fb4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e7fb4-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7fb4-139">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="e7fb4-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7fb4-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7fb4-141"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7fb4-141"><dt>Ntdsbcli.h</dt></span></span> </dl> |



 

 





