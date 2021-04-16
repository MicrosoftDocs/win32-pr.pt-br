---
description: Remove um pacote de exceção.
ms.assetid: d590d0f8-c9b2-4973-999b-99bbf94d4928
title: Função UninstallComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UninstallComponent
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: a541f51b030c9be7a26d573794e4df3a7cfc6f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751376"
---
# <a name="uninstallcomponent-function"></a><span data-ttu-id="bd686-103">Função UninstallComponent</span><span class="sxs-lookup"><span data-stu-id="bd686-103">UninstallComponent function</span></span>

<span data-ttu-id="bd686-104">Remove um pacote de exceção.</span><span class="sxs-lookup"><span data-stu-id="bd686-104">Removes an exception package.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd686-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd686-105">Syntax</span></span>


```C++
void UninstallComponent(
  _In_opt_ const GUID  *CompGuid,
  _In_           DWORD Flags,
  _In_opt_       INT   VerMajor,
  _In_opt_       INT   VerMinor,
  _In_opt_       INT   VerBuild,
  _In_opt_       INT   VerQFE
);
```



## <a name="parameters"></a><span data-ttu-id="bd686-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd686-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd686-107">*CompGuid* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bd686-107">*CompGuid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd686-108">O GUID do componente de exceção que está sendo desinstalado.</span><span class="sxs-lookup"><span data-stu-id="bd686-108">The GUID of the exception component being uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="bd686-109">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="bd686-109">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd686-110">Os sinalizadores usados para controlar os comportamentos de instalação.</span><span class="sxs-lookup"><span data-stu-id="bd686-110">The flags used to control installation behaviors.</span></span> <span data-ttu-id="bd686-111">Esse parâmetro pode ser uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bd686-111">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="bd686-112">Valor</span><span class="sxs-lookup"><span data-stu-id="bd686-112">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="bd686-113">Significado</span><span class="sxs-lookup"><span data-stu-id="bd686-113">Meaning</span></span>                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <span data-ttu-id="bd686-114"><dt>**sinalizadores de COMP \_ \_ NOUI**</dt></span><span class="sxs-lookup"><span data-stu-id="bd686-114"><dt>**COMP\_FLAGS\_NOUI**</dt></span></span> </dl>                                          | <span data-ttu-id="bd686-115">Suprime toda a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="bd686-115">Suppresses all UI.</span></span><br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <span data-ttu-id="bd686-116"><dt>**sinalizadores de COMP \_ \_ Atualizar \_ dllcache**</dt></span><span class="sxs-lookup"><span data-stu-id="bd686-116"><dt>**COMP\_FLAGS\_UPDATE\_DLLCACHE**</dt></span></span> </dl>        | <span data-ttu-id="bd686-117">Força o diretório DLLCACHE a ser atualizado quando um arquivo do sistema é atualizado.</span><span class="sxs-lookup"><span data-stu-id="bd686-117">Forces the DLLCACHE directory to be updated when a system file is updated.</span></span><br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <span data-ttu-id="bd686-118"><dt>**os \_ sinalizadores de comp \_ usam o \_ \_ cache Svcpack**</dt></span><span class="sxs-lookup"><span data-stu-id="bd686-118"><dt>**COMP\_FLAGS\_USE\_SVCPACK\_CACHE**</dt></span></span> </dl> | <span data-ttu-id="bd686-119">Usa arquivos armazenados em cache por um Windows service pack instalar para substituir arquivos submetidos a backup.</span><span class="sxs-lookup"><span data-stu-id="bd686-119">Uses files cached by a Windows service pack install to supersede files backed up.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bd686-120">*VerMajor* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bd686-120">*VerMajor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd686-121">A versão principal do componente de exceção a ser desinstalada.</span><span class="sxs-lookup"><span data-stu-id="bd686-121">The major version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="bd686-122">*Verminor* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bd686-122">*VerMinor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd686-123">A versão secundária do componente de exceção a ser desinstalada.</span><span class="sxs-lookup"><span data-stu-id="bd686-123">The minor version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="bd686-124">*VerBuild* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bd686-124">*VerBuild* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd686-125">A versão de compilação do componente de exceção a ser desinstalada.</span><span class="sxs-lookup"><span data-stu-id="bd686-125">The build version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="bd686-126">*VerQFE* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bd686-126">*VerQFE* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd686-127">A revisão do hotfix do componente de exceção a ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="bd686-127">The hotfix revision of the Exception component to be uninstalled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd686-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bd686-128">Return value</span></span>

<span data-ttu-id="bd686-129">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bd686-129">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd686-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd686-130">Remarks</span></span>

<span data-ttu-id="bd686-131">Os pacotes de exceção são arquivos de sistema do Windows que são liberados fora de uma versão completa do Windows do pacote e que atualizam os arquivos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="bd686-131">Exception packages are Windows system files that are released outside of a full package Windows release and that update operating-system files.</span></span> <span data-ttu-id="bd686-132">Os pacotes de exceção são criados somente por equipes de sistema operacional que receberam autorização para atualizar os arquivos de sistema do Windows.</span><span class="sxs-lookup"><span data-stu-id="bd686-132">Exception packages are authored only by operating-system teams that have been granted authorization to update Windows system files.</span></span>

<span data-ttu-id="bd686-133">Para instalar e desinstalar arquivos que não são protegidos pela proteção de arquivos do Windows, use as funções documentadas em [funções gerais de instalação](https://msdn.microsoft.com/library/ms794585.aspx).</span><span class="sxs-lookup"><span data-stu-id="bd686-133">To install and uninstall files that are not protected by Windows File Protection, use the functions documented in [General Setup Functions](https://msdn.microsoft.com/library/ms794585.aspx).</span></span> <span data-ttu-id="bd686-134">Para instalar drivers de dispositivo, os dispositivos de vendas devem usar funções documentadas em [funções de instalação de dispositivo](https://msdn.microsoft.com/library/ms792954.aspx) e funções de [Configuration Manager PNP](https://msdn.microsoft.com/library/ms790838.aspx).</span><span class="sxs-lookup"><span data-stu-id="bd686-134">To install device drivers, venders should use functions documented in [Device Installation Functions](https://msdn.microsoft.com/library/ms792954.aspx) and [PnP Configuration Manager Functions](https://msdn.microsoft.com/library/ms790838.aspx).</span></span>

<span data-ttu-id="bd686-135">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="bd686-135">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd686-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd686-136">Requirements</span></span>



| <span data-ttu-id="bd686-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd686-137">Requirement</span></span> | <span data-ttu-id="bd686-138">Valor</span><span class="sxs-lookup"><span data-stu-id="bd686-138">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd686-139">DLL</span><span class="sxs-lookup"><span data-stu-id="bd686-139">DLL</span></span><br/> | <dl> <span data-ttu-id="bd686-140"><dt>Msoobci.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd686-140"><dt>Msoobci.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd686-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd686-141">See also</span></span>

<dl> <span data-ttu-id="bd686-142"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="bd686-142"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="bd686-143">**InstallComponentW**</span><span class="sxs-lookup"><span data-stu-id="bd686-143">**InstallComponentW**</span></span>](installcomponentw.md)
</dt> </dl>

 

 
