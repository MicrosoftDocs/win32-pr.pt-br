---
description: Recupera o status do cache Arquivos Offline.
ms.assetid: a8cc0dbb-0005-4e74-892e-898e2ebe0465
title: Função CSCQueryDatabaseStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCQueryDatabaseStatus
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: badd869306290609ccadeba80e6ea67ca3479be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748909"
---
# <a name="cscquerydatabasestatus-function"></a><span data-ttu-id="e6e52-103">Função CSCQueryDatabaseStatus</span><span class="sxs-lookup"><span data-stu-id="e6e52-103">CSCQueryDatabaseStatus function</span></span>

<span data-ttu-id="e6e52-104">\[Essa função não tem suporte e não deve ser usada.\]</span><span class="sxs-lookup"><span data-stu-id="e6e52-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="e6e52-105">Recupera o status do cache Arquivos Offline.</span><span class="sxs-lookup"><span data-stu-id="e6e52-105">Retrieves the status of the Offline Files cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e52-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6e52-106">Syntax</span></span>


```C++
BOOL WINAPI CSCQueryDatabaseStatus(
   ULONG *pulStatus,
   ULONG *pulErrors
);
```



## <a name="parameters"></a><span data-ttu-id="e6e52-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6e52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6e52-108">*pulStatus*</span><span class="sxs-lookup"><span data-stu-id="e6e52-108">*pulStatus*</span></span> 
</dt> <dd>

<span data-ttu-id="e6e52-109">O status.</span><span class="sxs-lookup"><span data-stu-id="e6e52-109">The status.</span></span> <span data-ttu-id="e6e52-110">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e6e52-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e6e52-111">Valor</span><span class="sxs-lookup"><span data-stu-id="e6e52-111">Value</span></span>                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="e6e52-112">Significado</span><span class="sxs-lookup"><span data-stu-id="e6e52-112">Meaning</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="FLAG_DATABASESTATUS_ENCRYPTED"></span><span id="flag_databasestatus_encrypted"></span><dl> <span data-ttu-id="e6e52-113"><dt>**Sinalizador \_ DATABASESTATUS \_ criptografado**</dt> , <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="e6e52-113"><dt>**FLAG\_DATABASESTATUS\_ENCRYPTED**</dt> <dt>0x00000002</dt></span></span> </dl>                                      | <span data-ttu-id="e6e52-114">O cache é marcado para criptografia e todos os arquivos no cache são criptografados.</span><span class="sxs-lookup"><span data-stu-id="e6e52-114">The cache is marked for encryption and all files in the cache are encrypted.</span></span><br/>                |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_ENCRYPTED"></span><span id="flag_databasestatus_partially_encrypted"></span><dl> <span data-ttu-id="e6e52-115"><dt>**Sinalizador \_ DATABASESTATUS \_ 0x00000004 parcialmente \_ criptografado**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e6e52-115"><dt>**FLAG\_DATABASESTATUS\_PARTIALLY\_ENCRYPTED**</dt> <dt>0x00000004</dt></span></span> </dl>       | <span data-ttu-id="e6e52-116">O cache é marcado para criptografia, mas alguns arquivos no cache não são criptografados.</span><span class="sxs-lookup"><span data-stu-id="e6e52-116">The cache is marked for encryption, but some files in the cache are not encrypted.</span></span><br/>          |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_UNENCRYPTED"></span><span id="flag_databasestatus_partially_unencrypted"></span><dl> <span data-ttu-id="e6e52-117"><dt>**Sinalizador \_ DATABASESTATUS \_ 0x00000004 parcialmente não \_ criptografado**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e6e52-117"><dt>**FLAG\_DATABASESTATUS\_PARTIALLY\_UNENCRYPTED**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="e6e52-118">O cache não está marcado para criptografia, mas nem todos os arquivos no cache foram descriptografados.</span><span class="sxs-lookup"><span data-stu-id="e6e52-118">The cache is not marked for encryption, but not all files in the cache have been decrypted.</span></span><br/> |
| <span id="FLAG_DATABASESTATUS_UNENCRYPTED"></span><span id="flag_databasestatus_unencrypted"></span><dl> <span data-ttu-id="e6e52-119"><dt>**Sinalizador \_ DATABASESTATUS não \_ criptografado**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="e6e52-119"><dt>**FLAG\_DATABASESTATUS\_UNENCRYPTED**</dt> <dt>0x00000000</dt></span></span> </dl>                                | <span data-ttu-id="e6e52-120">O cache não está marcado para criptografia e todos os arquivos no cache foram descriptografados.</span><span class="sxs-lookup"><span data-stu-id="e6e52-120">The cache is not marked for encryption and all files in the cache have been decrypted.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="e6e52-121">*pulErrors*</span><span class="sxs-lookup"><span data-stu-id="e6e52-121">*pulErrors*</span></span> 
</dt> <dd>

<span data-ttu-id="e6e52-122">Esse parâmetro é um valor diferente de zero se houver um erro de banco de dados interno ou 0 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="e6e52-122">This parameter is a nonzero value if there is an internal database error or 0 otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6e52-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6e52-123">Return value</span></span>

<span data-ttu-id="e6e52-124">Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="e6e52-124">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6e52-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6e52-125">Remarks</span></span>

<span data-ttu-id="e6e52-126">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e6e52-126">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6e52-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6e52-127">Requirements</span></span>



| <span data-ttu-id="e6e52-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6e52-128">Requirement</span></span> | <span data-ttu-id="e6e52-129">Valor</span><span class="sxs-lookup"><span data-stu-id="e6e52-129">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e52-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e6e52-130">DLL</span></span><br/> | <dl> <span data-ttu-id="e6e52-131"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6e52-131"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6e52-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6e52-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e52-133">**CSCIsCSCEnabled**</span><span class="sxs-lookup"><span data-stu-id="e6e52-133">**CSCIsCSCEnabled**</span></span>](csciscscenabled.md)
</dt> </dl>

 

 
