---
description: Cria um perfil de usuário para um usuário especificado.
ms.assetid: e4ea4032-d8d3-45c1-b2e5-7fef52a8a869
title: Função CreateUserProfileEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateUserProfileEx
- CreateUserProfileExA
- CreateUserProfileExW
api_type:
- DllExport
api_location:
- Userenv.dll
ms.openlocfilehash: 8dbb76293fda769ec720221ca1bfa4474af1620c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104968790"
---
# <a name="createuserprofileex-function"></a><span data-ttu-id="42fa1-103">Função CreateUserProfileEx</span><span class="sxs-lookup"><span data-stu-id="42fa1-103">CreateUserProfileEx function</span></span>

<span data-ttu-id="42fa1-104">\[Essa função não está disponível no Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="42fa1-104">\[This function is not available as of Windows Vista.\]</span></span>

<span data-ttu-id="42fa1-105">Cria um perfil de usuário para um usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="42fa1-105">Creates a user profile for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="42fa1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42fa1-106">Syntax</span></span>


```C++
BOOL WINAPI CreateUserProfileEx(
  _In_      PSID    pSid,
  _In_      LPCTSTR lpUserName,
  _In_opt_  LPCTSTR lpUserHive,
  _Out_opt_ LPTSTR  lpProfileDir,
  _In_      DWORD   dwDirSize,
  _In_      BOOL    bWin9xUpg
);
```



## <a name="parameters"></a><span data-ttu-id="42fa1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42fa1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42fa1-108">*psid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42fa1-108">*pSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42fa1-109">Tipo: **PSID**</span><span class="sxs-lookup"><span data-stu-id="42fa1-109">Type: **PSID**</span></span>

<span data-ttu-id="42fa1-110">O SID do novo usuário.</span><span class="sxs-lookup"><span data-stu-id="42fa1-110">The SID of the new user.</span></span>

</dd> <dt>

<span data-ttu-id="42fa1-111">*lpUserName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42fa1-111">*lpUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42fa1-112">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="42fa1-112">Type: **LPCTSTR**</span></span>

<span data-ttu-id="42fa1-113">Ponteiro para um buffer que contém o nome de usuário do novo usuário.</span><span class="sxs-lookup"><span data-stu-id="42fa1-113">Pointer to a buffer that contains the user name of the new user.</span></span>

</dd> <dt>

<span data-ttu-id="42fa1-114">*lpUserHive* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="42fa1-114">*lpUserHive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42fa1-115">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="42fa1-115">Type: **LPCTSTR**</span></span>

<span data-ttu-id="42fa1-116">Ponteiro para um buffer que contém o [hive do registro](../sysinfo/registry-hives.md) a ser usado.</span><span class="sxs-lookup"><span data-stu-id="42fa1-116">Pointer to a buffer that contains the [registry hive](../sysinfo/registry-hives.md) to use.</span></span> <span data-ttu-id="42fa1-117">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="42fa1-117">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42fa1-118">*lpProfileDir* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="42fa1-118">*lpProfileDir* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42fa1-119">Tipo: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="42fa1-119">Type: **LPTSTR**</span></span>

<span data-ttu-id="42fa1-120">Ponteiro para um buffer que, quando essa função retorna, recebe o caminho do diretório de perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="42fa1-120">Pointer to a buffer that, when this function returns, receives the user's profile directory path.</span></span> <span data-ttu-id="42fa1-121">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="42fa1-121">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42fa1-122">*dwDirSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42fa1-122">*dwDirSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42fa1-123">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="42fa1-123">Type: **DWORD**</span></span>

<span data-ttu-id="42fa1-124">Tamanho do buffer especificado por *lpProfileDir*, em TCHARs.</span><span class="sxs-lookup"><span data-stu-id="42fa1-124">Size of the buffer specified by *lpProfileDir*, in TCHARs.</span></span>

</dd> <dt>

<span data-ttu-id="42fa1-125">*bWin9xUpg* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42fa1-125">*bWin9xUpg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42fa1-126">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="42fa1-126">Type: **BOOL**</span></span>

<span data-ttu-id="42fa1-127">**True** se o perfil do usuário estiver sendo criado como parte de uma migração de perfil do Windows 9x; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="42fa1-127">**TRUE** if the user profile is being created as part of a profile migration from Windows 9x; otherwise, **FALSE**.</span></span>

<span data-ttu-id="42fa1-128">Quando **true**, o perfil do usuário é configurado no diretório de perfil padrão — normalmente C: \\ Documents and Settings \\ *username*.</span><span class="sxs-lookup"><span data-stu-id="42fa1-128">When **TRUE**, the user profile is set up in the default profile directory—normally C:\\Documents and Settings\\*UserName*.</span></span> <span data-ttu-id="42fa1-129">Se esse diretório já existir, ele será usado.</span><span class="sxs-lookup"><span data-stu-id="42fa1-129">If that directory already exists, it is used.</span></span> <span data-ttu-id="42fa1-130">Se não tiver, ele será criado.</span><span class="sxs-lookup"><span data-stu-id="42fa1-130">If it does not, it is created.</span></span>

<span data-ttu-id="42fa1-131">Se **for false**, o diretório de perfil padrão será criado se ele não existir.</span><span class="sxs-lookup"><span data-stu-id="42fa1-131">If **FALSE**, the default profile directory is created if it does not exist.</span></span> <span data-ttu-id="42fa1-132">Se o diretório de perfil padrão já existir, um novo diretório será criado para esse perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="42fa1-132">If the default profile directory already exists, a new directory is created for this user profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42fa1-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42fa1-133">Return value</span></span>

<span data-ttu-id="42fa1-134">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="42fa1-134">Type: **BOOL**</span></span>

<span data-ttu-id="42fa1-135">Retorna **true** se o novo perfil de usuário foi criado com êxito; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="42fa1-135">Returns **TRUE** if the new user profile was created successfully; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="42fa1-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="42fa1-136">Remarks</span></span>

<span data-ttu-id="42fa1-137">Essa função não é declarada nos cabeçalhos Software Development Kit (SDK) e não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="42fa1-137">This function is not declared in the software development kit (SDK) headers and has no associated import library.</span></span> <span data-ttu-id="42fa1-138">Você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular a Userenv.dll.</span><span class="sxs-lookup"><span data-stu-id="42fa1-138">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to link to Userenv.dll.</span></span> <span data-ttu-id="42fa1-139">A versão ANSI da função, **CreateUserProfileExA** , é referenciada de Userenv.dll como ordinal 153.</span><span class="sxs-lookup"><span data-stu-id="42fa1-139">The ANSI version of the function, **CreateUserProfileExA** is referenced from Userenv.dll as ordinal 153.</span></span> <span data-ttu-id="42fa1-140">A versão Unicode, **CreateUserProfileExW** , é referenciada como ordinal 154.</span><span class="sxs-lookup"><span data-stu-id="42fa1-140">The Unicode version, **CreateUserProfileExW** is referenced as ordinal 154.</span></span>

## <a name="requirements"></a><span data-ttu-id="42fa1-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42fa1-141">Requirements</span></span>



| <span data-ttu-id="42fa1-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="42fa1-142">Requirement</span></span> | <span data-ttu-id="42fa1-143">Valor</span><span class="sxs-lookup"><span data-stu-id="42fa1-143">Value</span></span> |
|-----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42fa1-144">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="42fa1-144">End of client support</span></span><br/>  | <span data-ttu-id="42fa1-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="42fa1-145">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="42fa1-146">DLL</span><span class="sxs-lookup"><span data-stu-id="42fa1-146">DLL</span></span><br/>                    | <dl> <span data-ttu-id="42fa1-147"><dt>Userenv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42fa1-147"><dt>Userenv.dll</dt></span></span> </dl> |
| <span data-ttu-id="42fa1-148">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="42fa1-148">Unicode and ANSI names</span></span><br/> | <span data-ttu-id="42fa1-149">**CreateUserProfileExW** (Unicode) e **CreateUserProfileExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="42fa1-149">**CreateUserProfileExW** (Unicode) and **CreateUserProfileExA** (ANSI)</span></span><br/>      |



 

 
