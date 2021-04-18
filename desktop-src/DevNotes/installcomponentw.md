---
description: Instala um pacote de exceção.
ms.assetid: c4c3c01c-9aaf-42cd-a690-13e2113b15b3
title: Função InstallComponentW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallComponentW
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: 4d262322be6084429f03d5725f61c0e0f7140871
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749865"
---
# <a name="installcomponentw-function"></a><span data-ttu-id="284c2-103">Função InstallComponentW</span><span class="sxs-lookup"><span data-stu-id="284c2-103">InstallComponentW function</span></span>

<span data-ttu-id="284c2-104">Instala um pacote de exceção.</span><span class="sxs-lookup"><span data-stu-id="284c2-104">Installs an exception package.</span></span>

## <a name="syntax"></a><span data-ttu-id="284c2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="284c2-105">Syntax</span></span>


```C++
void InstallComponentW(
  _In_           LPCWSTR InfPath,
  _In_opt_ const GUID    *CompGuid,
  _In_           DWORD   Flags,
  _In_opt_       INT     VerMajor,
  _In_opt_       INT     VerMinor,
  _In_opt_       INT     VerBuild,
  _In_opt_       INT     VerQFE,
  _In_opt_       LPCWSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="284c2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="284c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="284c2-107">*InfPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="284c2-107">*InfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="284c2-108">O caminho para o INF de exceção a ser processado.</span><span class="sxs-lookup"><span data-stu-id="284c2-108">The path to the exception INF to process.</span></span>

</dd> <dt>

<span data-ttu-id="284c2-109">*CompGuid* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="284c2-109">*CompGuid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="284c2-110">O GUID do componente de exceção que está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="284c2-110">The GUID of the exception component being installed.</span></span>

</dd> <dt>

<span data-ttu-id="284c2-111">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="284c2-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="284c2-112">Os sinalizadores usados para controlar os comportamentos de instalação.</span><span class="sxs-lookup"><span data-stu-id="284c2-112">The flags used to control installation behaviors.</span></span> <span data-ttu-id="284c2-113">Esse parâmetro pode ser uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="284c2-113">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="284c2-114">Valor</span><span class="sxs-lookup"><span data-stu-id="284c2-114">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="284c2-115">Significado</span><span class="sxs-lookup"><span data-stu-id="284c2-115">Meaning</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <span data-ttu-id="284c2-116"><dt>**Comp \_ SINALIZADORES/ \_ força**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="284c2-116"><dt>**COMP\_FLAGS\_FORCE**</dt> <dt>0x00000020</dt></span></span> </dl>                             | <span data-ttu-id="284c2-117">Ignora a verificação de versão nas substituições de arquivo.</span><span class="sxs-lookup"><span data-stu-id="284c2-117">Skips the version check on file replacements.</span></span><br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <span data-ttu-id="284c2-118"><dt>**Comp \_ os sinalizadores \_ precisam ser \_ desinstalados**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="284c2-118"><dt>**COMP\_FLAGS\_NEEDS\_UNINSTALL**</dt> <dt></dt></span></span> </dl>        | <span data-ttu-id="284c2-119">Faça backup de arquivos que são atualizados para serem usados por uma desinstalação do componente.</span><span class="sxs-lookup"><span data-stu-id="284c2-119">Back up files that are updated to be used by an uninstall of the component.</span></span><br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <span data-ttu-id="284c2-120"><dt>**Comp \_ SINALIZADORES \_ sem \_ substituição**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="284c2-120"><dt>**COMP\_FLAGS\_NO\_OVERWRITE**</dt> <dt></dt></span></span> </dl>                 | <span data-ttu-id="284c2-121">Ignora o backup de arquivos se a versão do componente de exceção é igual a um componente instalado.</span><span class="sxs-lookup"><span data-stu-id="284c2-121">Skips backing up files if the Exception component version is the same as an installed component.</span></span> <span data-ttu-id="284c2-122">Esse sinalizador é usado em um cenário de reinstalação.</span><span class="sxs-lookup"><span data-stu-id="284c2-122">This flag is used in a reinstallation scenario.</span></span><br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <span data-ttu-id="284c2-123"><dt>**Comp \_ SINALIZADORES \_ NOUI**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="284c2-123"><dt>**COMP\_FLAGS\_NOUI**</dt> <dt>0x00000002</dt></span></span> </dl>                                | <span data-ttu-id="284c2-124">Suprime toda a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="284c2-124">Suppresses all UI.</span></span><br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <span data-ttu-id="284c2-125"><dt>**Comp \_ SINALIZADORES de \_ atualização de \_ dllcache**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="284c2-125"><dt>**COMP\_FLAGS\_UPDATE\_DLLCACHE**</dt> <dt></dt></span></span> </dl>        | <span data-ttu-id="284c2-126">Força o diretório DLLCACHE a ser atualizado quando um arquivo do sistema é atualizado.</span><span class="sxs-lookup"><span data-stu-id="284c2-126">Forces the DLLCACHE directory to be updated when a system file is updated.</span></span><br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <span data-ttu-id="284c2-127"><dt>**Comp \_ SINALIZADORES \_ usam \_ \_ cache Svcpack**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="284c2-127"><dt>**COMP\_FLAGS\_USE\_SVCPACK\_CACHE**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="284c2-128">Usa arquivos armazenados em cache por um Windows service pack instalar para substituir arquivos submetidos a backup.</span><span class="sxs-lookup"><span data-stu-id="284c2-128">Uses files cached by a Windows service pack install to supersede files backed up.</span></span><br/>                                                                |



 

</dd> <dt>

<span data-ttu-id="284c2-129">*VerMajor* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="284c2-129">*VerMajor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="284c2-130">A versão principal do componente de exceção.</span><span class="sxs-lookup"><span data-stu-id="284c2-130">The major version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="284c2-131">*Verminor* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="284c2-131">*VerMinor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="284c2-132">A versão secundária do componente de exceção.</span><span class="sxs-lookup"><span data-stu-id="284c2-132">The minor version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="284c2-133">*VerBuild* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="284c2-133">*VerBuild* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="284c2-134">A versão de compilação do componente de exceção.</span><span class="sxs-lookup"><span data-stu-id="284c2-134">The build version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="284c2-135">*VerQFE* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="284c2-135">*VerQFE* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="284c2-136">A revisão do hotfix do componente de exceção.</span><span class="sxs-lookup"><span data-stu-id="284c2-136">The hotfix revision of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="284c2-137">*Nome* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="284c2-137">*Name* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="284c2-138">A cadeia de caracteres descritiva do componente mostrado pela caixa de diálogo proteção de arquivo do Windows se o sistema operacional detectar que um arquivo protegido de proteção de arquivo do Windows está danificado, adulterado ou corrompido.</span><span class="sxs-lookup"><span data-stu-id="284c2-138">The descriptive string of the component shown by the Windows File Protection dialog box if the operating system detects that a Windows File Protection protect file is damaged, tampered with, or corrupted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="284c2-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="284c2-139">Return value</span></span>

<span data-ttu-id="284c2-140">Essa função retorna um valor **HRESULT** (S \_ OK ou um código de falha).</span><span class="sxs-lookup"><span data-stu-id="284c2-140">This function returns an **HRESULT** value (S\_OK or a failure code).</span></span> <span data-ttu-id="284c2-141">Um código de falha pode ser verificado em relação a um valor de 0x20000100 para determinar se a falha ocorre porque uma reinicialização é necessária.</span><span class="sxs-lookup"><span data-stu-id="284c2-141">A failure code can be checked against a value of 0x20000100 to determine whether the failure is because a reboot is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="284c2-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="284c2-142">Remarks</span></span>

<span data-ttu-id="284c2-143">Os pacotes de exceção são arquivos de sistema do Windows que são liberados fora de uma versão completa do Windows do pacote e que atualizam os arquivos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="284c2-143">Exception packages are Windows system files that are released outside of a full package Windows release and that update operating-system files.</span></span> <span data-ttu-id="284c2-144">Os pacotes de exceção são criados somente por equipes de sistema operacional que receberam autorização para atualizar os arquivos de sistema do Windows.</span><span class="sxs-lookup"><span data-stu-id="284c2-144">Exception packages are authored only by operating-system teams that have been granted authorization to update Windows system files.</span></span>

<span data-ttu-id="284c2-145">Para instalar e desinstalar arquivos que não são protegidos pela proteção de arquivos do Windows, use as funções documentadas em [funções gerais de instalação](https://msdn.microsoft.com/library/ms794585.aspx).</span><span class="sxs-lookup"><span data-stu-id="284c2-145">To install and uninstall files that are not protected by Windows File Protection, use the functions documented in [General Setup Functions](https://msdn.microsoft.com/library/ms794585.aspx).</span></span> <span data-ttu-id="284c2-146">Para instalar drivers de dispositivo, os dispositivos de vendas devem usar funções documentadas em [funções de instalação de dispositivo](https://msdn.microsoft.com/library/ms792954.aspx) e funções de [Configuration Manager PNP](https://msdn.microsoft.com/library/ms790838.aspx).</span><span class="sxs-lookup"><span data-stu-id="284c2-146">To install device drivers, venders should use functions documented in [Device Installation Functions](https://msdn.microsoft.com/library/ms792954.aspx) and [PnP Configuration Manager Functions](https://msdn.microsoft.com/library/ms790838.aspx).</span></span>

<span data-ttu-id="284c2-147">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="284c2-147">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="284c2-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="284c2-148">Requirements</span></span>



| <span data-ttu-id="284c2-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="284c2-149">Requirement</span></span> | <span data-ttu-id="284c2-150">Valor</span><span class="sxs-lookup"><span data-stu-id="284c2-150">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="284c2-151">DLL</span><span class="sxs-lookup"><span data-stu-id="284c2-151">DLL</span></span><br/> | <dl> <span data-ttu-id="284c2-152"><dt>Msoobci.dll</dt></span><span class="sxs-lookup"><span data-stu-id="284c2-152"><dt>Msoobci.dll</dt></span></span> </dl> |



 

 
