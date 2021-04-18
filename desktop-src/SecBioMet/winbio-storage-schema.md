---
title: Estrutura de WINBIO_STORAGE_SCHEMA (WinBio \_ Types. h)
description: Descreve os recursos de um adaptador de armazenamento biométrico.
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_STORAGE_SCHEMA
- Ponteiro de estrutura de PWINBIO_STORAGE_SCHEMA Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_STORAGE_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28db23d55a7b3e43caaae5a88ca4bbf32fdf1178
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105778697"
---
# <a name="winbio_storage_schema-structure"></a><span data-ttu-id="bef29-105">Estrutura de esquema de \_ armazenamento WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="bef29-105">WINBIO\_STORAGE\_SCHEMA structure</span></span>

<span data-ttu-id="bef29-106">A estrutura de **\_ \_ esquema de armazenamento do WINBIO** descreve os recursos de um adaptador de armazenamento biométrico.</span><span class="sxs-lookup"><span data-stu-id="bef29-106">The **WINBIO\_STORAGE\_SCHEMA** structure describes the capabilities of a biometric storage adapter.</span></span> <span data-ttu-id="bef29-107">Essa estrutura é usada pela função [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) .</span><span class="sxs-lookup"><span data-stu-id="bef29-107">This structure is used by the [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="bef29-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bef29-108">Syntax</span></span>


```C++
typedef struct _WINBIO_STORAGE_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           DatabaseId;
  WINBIO_UUID           DataFormat;
  ULONG                 Attributes;
  WINBIO_STRING         FilePath;
  WINBIO_STRING         ConnectionString;
} WINBIO_STORAGE_SCHEMA, *PWINBIO_STORAGE_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="bef29-109">Membros</span><span class="sxs-lookup"><span data-stu-id="bef29-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="bef29-110">**BiometricFactor**</span><span class="sxs-lookup"><span data-stu-id="bef29-110">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="bef29-111">O tipo de medição biométrica salva no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bef29-111">The type of biometric measurement saved in the database.</span></span>

</dd> <dt>

<span data-ttu-id="bef29-112">**DatabaseId**</span><span class="sxs-lookup"><span data-stu-id="bef29-112">**DatabaseId**</span></span>
</dt> <dd>

<span data-ttu-id="bef29-113">Um GUID que identifica o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bef29-113">A GUID that identifies the database.</span></span>

</dd> <dt>

<span data-ttu-id="bef29-114">**DataFormat**</span><span class="sxs-lookup"><span data-stu-id="bef29-114">**DataFormat**</span></span>
</dt> <dd>

<span data-ttu-id="bef29-115">Um GUID que identifica o formato dos modelos no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bef29-115">A GUID that identifies the format of the templates in the database.</span></span>

</dd> <dt>

<span data-ttu-id="bef29-116">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="bef29-116">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="bef29-117">Informações sobre as características do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bef29-117">Information about the characteristics of the database.</span></span> <span data-ttu-id="bef29-118">Isso pode ser uma **ou** uma das constantes a seguir.</span><span class="sxs-lookup"><span data-stu-id="bef29-118">This can be a bitwise **OR** of the following constants.</span></span>



| <span data-ttu-id="bef29-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bef29-119">Value</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="bef29-120">Significado</span><span class="sxs-lookup"><span data-stu-id="bef29-120">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <span data-ttu-id="bef29-121"><dt>**WINBIO \_ \_ \_ Máscara de sinalizador de banco de dados**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="bef29-121"><dt>**WINBIO\_DATABASE\_FLAG\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl>                | <span data-ttu-id="bef29-122">Representa uma máscara para os bits de sinalizador.</span><span class="sxs-lookup"><span data-stu-id="bef29-122">Represents a mask for the flag bits.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <span data-ttu-id="bef29-123"><dt>**WINBIO \_ 0x00020000 \_ \_ remoto do sinalizador de banco de dados**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bef29-123"><dt>**WINBIO\_DATABASE\_FLAG\_REMOTE**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="bef29-124">O banco de dados reside em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="bef29-124">The database resides on a remote computer.</span></span><br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <span data-ttu-id="bef29-125"><dt>**WINBIO \_ 0x00010000 \_ \_ removível do sinalizador de banco de dados**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bef29-125"><dt>**WINBIO\_DATABASE\_FLAG\_REMOVABLE**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="bef29-126">O banco de dados reside em uma unidade removível.</span><span class="sxs-lookup"><span data-stu-id="bef29-126">The database resides on a removable drive.</span></span><br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <span data-ttu-id="bef29-127"><dt>**WINBIO \_ Tipo de banco de dados \_ \_ DBMS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="bef29-127"><dt>**WINBIO\_DATABASE\_TYPE\_DBMS**</dt> <dt>0x00000002</dt></span></span> </dl>                | <span data-ttu-id="bef29-128">O banco de dados é gerenciado por um sistema de gerenciamento de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bef29-128">The database is managed by a database management system.</span></span><br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <span data-ttu-id="bef29-129"><dt>**WINBIO \_ \_ \_ Arquivo de tipo de banco de dados**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="bef29-129"><dt>**WINBIO\_DATABASE\_TYPE\_FILE**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="bef29-130">O banco de dados está contido em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="bef29-130">The database is contained in a file.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <span data-ttu-id="bef29-131"><dt>**WINBIO \_ \_ \_ Máscara de tipo de banco de dados**</dt> <dt>0x0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="bef29-131"><dt>**WINBIO\_DATABASE\_TYPE\_MASK**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                | <span data-ttu-id="bef29-132">Representa uma máscara para o tipo bits.</span><span class="sxs-lookup"><span data-stu-id="bef29-132">Represents a mask for the type bits.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <span data-ttu-id="bef29-133"><dt>**WINBIO \_ Tipo de banco de dados \_ \_ OnChip**</dt> <dt>0x00000003</dt></span><span class="sxs-lookup"><span data-stu-id="bef29-133"><dt>**WINBIO\_DATABASE\_TYPE\_ONCHIP**</dt> <dt>0x00000003</dt></span></span> </dl>          | <span data-ttu-id="bef29-134">O banco de dados reside no sensor biométrico.</span><span class="sxs-lookup"><span data-stu-id="bef29-134">The database resides on the biometric sensor.</span></span><br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <span data-ttu-id="bef29-135"><dt>**WINBIO \_ \_ \_ Cartão inteligente de tipo de banco de dados**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="bef29-135"><dt>**WINBIO\_DATABASE\_TYPE\_SMARTCARD**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="bef29-136">O banco de dados reside em um cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="bef29-136">The database resides on a smart card.</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="bef29-137">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="bef29-137">**FilePath**</span></span>
</dt> <dd>

<span data-ttu-id="bef29-138">O caminho e o nome do arquivo do banco de dados se ele residir no disco do computador.</span><span class="sxs-lookup"><span data-stu-id="bef29-138">The path and file name of the database if it resides on the computer disk.</span></span>

</dd> <dt>

<span data-ttu-id="bef29-139">**ConnectionString**</span><span class="sxs-lookup"><span data-stu-id="bef29-139">**ConnectionString**</span></span>
</dt> <dd>

<span data-ttu-id="bef29-140">Um valor de cadeia de caracteres que pode ser enviado a um servidor de banco de dados para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bef29-140">A string value that can be sent to a database server to identify the database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bef29-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bef29-141">Requirements</span></span>



| <span data-ttu-id="bef29-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="bef29-142">Requirement</span></span> | <span data-ttu-id="bef29-143">Valor</span><span class="sxs-lookup"><span data-stu-id="bef29-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bef29-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bef29-144">Minimum supported client</span></span><br/> | <span data-ttu-id="bef29-145">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bef29-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="bef29-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bef29-146">Minimum supported server</span></span><br/> | <span data-ttu-id="bef29-147">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="bef29-147">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="bef29-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bef29-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="bef29-149"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bef29-149"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bef29-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="bef29-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bef29-151">Estruturas de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="bef29-151">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="bef29-152">**WinBioEnumDatabases**</span><span class="sxs-lookup"><span data-stu-id="bef29-152">**WinBioEnumDatabases**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





