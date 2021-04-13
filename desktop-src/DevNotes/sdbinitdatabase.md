---
description: Abre o banco de dados Shim.
ms.assetid: ece1bd39-20a1-42e6-8e2b-1d38f7223d42
title: Função SdbInitDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbInitDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a3c63fa712aec988dbf13c4fb7f9fddbf159fdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456918"
---
# <a name="sdbinitdatabase-function"></a><span data-ttu-id="9e832-103">Função SdbInitDatabase</span><span class="sxs-lookup"><span data-stu-id="9e832-103">SdbInitDatabase function</span></span>

<span data-ttu-id="9e832-104">Abre o banco de dados Shim.</span><span class="sxs-lookup"><span data-stu-id="9e832-104">Opens the shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e832-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e832-105">Syntax</span></span>


```C++
HSDB WINAPI SdbInitDatabase(
  _In_ DWORD   dwFlags,
  _In_ LPCTSTR pszDatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="9e832-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e832-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e832-107">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e832-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e832-108">Esse parâmetro especifica o formato do caminho no parâmetro *pszDatabasePath* .</span><span class="sxs-lookup"><span data-stu-id="9e832-108">This parameter specifies the format of the path in the *pszDatabasePath* parameter.</span></span> <span data-ttu-id="9e832-109">Pode ser um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="9e832-109">It can be one of the following values.</span></span>



| <span data-ttu-id="9e832-110">Valor</span><span class="sxs-lookup"><span data-stu-id="9e832-110">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="9e832-111">Significado</span><span class="sxs-lookup"><span data-stu-id="9e832-111">Meaning</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="HID_DOS_PATHS"></span><span id="hid_dos_paths"></span><dl> <span data-ttu-id="9e832-112"><dt>**HID \_ \_Caminhos dos**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="9e832-112"><dt>**HID\_DOS\_PATHS**</dt> <dt>0x00000001</dt></span></span> </dl>                             | <span data-ttu-id="9e832-113">Um caminho de estilo MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="9e832-113">An MS-DOS style path.</span></span><br/>                                                                       |
| <span id="HID_DATABASE_FULLPATH"></span><span id="hid_database_fullpath"></span><dl> <span data-ttu-id="9e832-114"><dt>**HID \_ \_FULLPATH do banco de dados**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="9e832-114"><dt>**HID\_DATABASE\_FULLPATH**</dt> <dt>0x00000002</dt></span></span> </dl>     | <span data-ttu-id="9e832-115">Um caminho completo.</span><span class="sxs-lookup"><span data-stu-id="9e832-115">A full path.</span></span><br/>                                                                                |
| <span id="HID_NO_DATABASE"></span><span id="hid_no_database"></span><dl> <span data-ttu-id="9e832-116"><dt>**HID \_ NENHUM \_ banco de dados**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="9e832-116"><dt>**HID\_NO\_DATABASE**</dt> <dt>0x00000004</dt></span></span> </dl>                       | <span data-ttu-id="9e832-117">O parâmetro *pszDatabasePath* é ignorado e nenhum banco de dados é aberto.</span><span class="sxs-lookup"><span data-stu-id="9e832-117">The *pszDatabasePath* parameter is ignored and no database is opened.</span></span><br/>                       |
| <span id="HID_DATABASE_TYPE_MASK"></span><span id="hid_database_type_mask"></span><dl> <span data-ttu-id="9e832-118"><dt>**HID \_ \_ \_ Máscara de tipo de banco de dados**</dt> <dt>0xF00F0000</dt></span><span class="sxs-lookup"><span data-stu-id="9e832-118"><dt>**HID\_DATABASE\_TYPE\_MASK**</dt> <dt>0xF00F0000</dt></span></span> </dl> | <span data-ttu-id="9e832-119">Esse parâmetro especifica um banco de dados predefinido.</span><span class="sxs-lookup"><span data-stu-id="9e832-119">This parameter specifies a predefined database.</span></span> <span data-ttu-id="9e832-120">O parâmetro *pszDatabasePath* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="9e832-120">The *pszDatabasePath* parameter is ignored.</span></span><br/> |



 

<span data-ttu-id="9e832-121">Se *dwFlags* contiver a **\_ máscara de \_ tipo \_ de dados HID**, esse parâmetro também poderá incluir um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9e832-121">If *dwFlags* contains **HID\_DATA\_TYPE\_MASK**, this parameter can also include one of the following values.</span></span>



| <span data-ttu-id="9e832-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9e832-122">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="9e832-123">Significado</span><span class="sxs-lookup"><span data-stu-id="9e832-123">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <span data-ttu-id="9e832-124"><dt>**Sdb \_ 0x80030000 \_ de \_ Shim principal do banco de dados**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9e832-124"><dt>**SDB\_DATABASE\_MAIN\_SHIM**</dt> <dt>0x80030000</dt></span></span> </dl>          | <span data-ttu-id="9e832-125">Banco de dados de correção de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9e832-125">Application shim database.</span></span><br/>         |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <span data-ttu-id="9e832-126"><dt>**Sdb \_ 0x80020000 \_ principal \_ MSI do banco de dados**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9e832-126"><dt>**SDB\_DATABASE\_MAIN\_MSI**</dt> <dt>0x80020000</dt></span></span> </dl>             | <span data-ttu-id="9e832-127">Banco de dados MSI.</span><span class="sxs-lookup"><span data-stu-id="9e832-127">MSI database.</span></span><br/>                      |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <span data-ttu-id="9e832-128"><dt>**Sdb \_ \_Principais \_ drivers de banco de dados**</dt> <dt>0x80040000</dt></span><span class="sxs-lookup"><span data-stu-id="9e832-128"><dt>**SDB\_DATABASE\_MAIN\_DRIVERS**</dt> <dt>0x80040000</dt></span></span> </dl> | <span data-ttu-id="9e832-129">Banco de dados de drivers a serem bloqueados.</span><span class="sxs-lookup"><span data-stu-id="9e832-129">Database of drivers to be blocked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9e832-130">*pszDatabasePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e832-130">*pszDatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e832-131">O caminho para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9e832-131">The path to the database.</span></span> <span data-ttu-id="9e832-132">Esse parâmetro poderá ser **nulo** se o parâmetro *dwFlags* especificar um banco de dados predefinido.</span><span class="sxs-lookup"><span data-stu-id="9e832-132">This parameter can be **NULL** if the *dwFlags* parameter specifies a predefined database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e832-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e832-133">Return value</span></span>

<span data-ttu-id="9e832-134">A função retorna um identificador para o banco de dados aberto.</span><span class="sxs-lookup"><span data-stu-id="9e832-134">The function returns a handle to the opened database.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e832-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e832-135">Requirements</span></span>



| <span data-ttu-id="9e832-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e832-136">Requirement</span></span> | <span data-ttu-id="9e832-137">Valor</span><span class="sxs-lookup"><span data-stu-id="9e832-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e832-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e832-138">Minimum supported client</span></span><br/> | <span data-ttu-id="9e832-139">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9e832-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9e832-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e832-140">Minimum supported server</span></span><br/> | <span data-ttu-id="9e832-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9e832-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9e832-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9e832-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e832-143"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e832-143"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e832-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e832-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e832-145">**SdbGetAppPatchDir**</span><span class="sxs-lookup"><span data-stu-id="9e832-145">**SdbGetAppPatchDir**</span></span>](sdbgetapppatchdir.md)
</dt> <dt>

[<span data-ttu-id="9e832-146">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="9e832-146">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> <dt>

[<span data-ttu-id="9e832-147">**SdbReleaseMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="9e832-147">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
</dt> <dt>

[<span data-ttu-id="9e832-148">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="9e832-148">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




