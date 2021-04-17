---
description: Procura um arquivo no cache Arquivos Offline que atenda aos critérios especificados.
ms.assetid: 09de6c55-fc37-4c0a-b5a0-ea73f06793d5
title: Função CSCFindFirstFileW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindFirstFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: f8cad9caf78b44f40a4126307db6deb0f71dfd1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748694"
---
# <a name="cscfindfirstfilew-function"></a><span data-ttu-id="58de5-103">Função CSCFindFirstFileW</span><span class="sxs-lookup"><span data-stu-id="58de5-103">CSCFindFirstFileW function</span></span>

<span data-ttu-id="58de5-104">\[Essa função não tem suporte e não deve ser usada.\]</span><span class="sxs-lookup"><span data-stu-id="58de5-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="58de5-105">Procura um arquivo no cache Arquivos Offline que atenda aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="58de5-105">Searches for a file in the Offline Files cache that meets the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="58de5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58de5-106">Syntax</span></span>


```C++
HANDLE WINAPI CSCFindFirstFileW(
  _In_  LPCWSTR          lpszFileName,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _Out_ FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a><span data-ttu-id="58de5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58de5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58de5-108">*lpszFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="58de5-108">*lpszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58de5-109">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um caminho ou diretório UNC válido.</span><span class="sxs-lookup"><span data-stu-id="58de5-109">A pointer to a null-terminated string that specifies a valid UNC directory or path.</span></span>

</dd> <dt>

<span data-ttu-id="58de5-110">*lpFind32* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="58de5-110">*lpFind32* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58de5-111">Um ponteiro para a estrutura de [**\_ \_ dados de localização do Win32**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) que recebe informações sobre o arquivo ou subdiretório.</span><span class="sxs-lookup"><span data-stu-id="58de5-111">A pointer to the [**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) structure that receives information about the file or subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="58de5-112">*lpdwStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="58de5-112">*lpdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58de5-113">Um código NTSTATUS que indica o status da chamada.</span><span class="sxs-lookup"><span data-stu-id="58de5-113">An NTSTATUS code that indicates the status of the call.</span></span>

</dd> <dt>

<span data-ttu-id="58de5-114">*lpdwPinCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="58de5-114">*lpdwPinCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58de5-115">Esse parâmetro será diferente de zero se o arquivo tiver sido disponibilizado offline ou 0 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="58de5-115">This parameter is nonzero if the file has been made available offline or 0 otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="58de5-116">*lpdwHintFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="58de5-116">*lpdwHintFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58de5-117">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="58de5-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="58de5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="58de5-118">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="58de5-119">Significado</span><span class="sxs-lookup"><span data-stu-id="58de5-119">Meaning</span></span>                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <span data-ttu-id="58de5-120"><dt>**Sinalizador \_ \_Usuário de \_ PIN \_ de dica de CSC**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="58de5-120"><dt>**FLAG\_CSC\_HINT\_PIN\_USER**</dt> <dt>0x01</dt></span></span> </dl>                                | <span data-ttu-id="58de5-121">Um usuário tornou o arquivo disponível offline.</span><span class="sxs-lookup"><span data-stu-id="58de5-121">A user has made the file available offline.</span></span><br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <span data-ttu-id="58de5-122"><dt>**Sinalizador \_ PIN de dica de CSC \_ \_ \_ herdar o \_ usuário**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="58de5-122"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_USER**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="58de5-123">Um usuário tornou o pai disponível offline e marcou o pai de modo que seus filhos estejam disponíveis offline.</span><span class="sxs-lookup"><span data-stu-id="58de5-123">A user has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <span data-ttu-id="58de5-124"><dt>**Sinalizador \_ O \_ PIN da dica de CSC \_ herda o \_ \_ sistema**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="58de5-124"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_SYSTEM**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="58de5-125">Uma política de administrador ou de grupo tornou o pai disponível offline e marcou o pai de modo que seus filhos estejam disponíveis offline.</span><span class="sxs-lookup"><span data-stu-id="58de5-125">An administrator or group policy has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <span data-ttu-id="58de5-126"><dt>**Sinalizador \_ O \_ \_ \_ sistema de PIN de dica do CSC**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="58de5-126"><dt>**FLAG\_CSC\_HINT\_PIN\_SYSTEM**</dt> <dt>0x10</dt></span></span> </dl>                          | <span data-ttu-id="58de5-127">Um administrador ou política de grupo disponibilizou o arquivo offline.</span><span class="sxs-lookup"><span data-stu-id="58de5-127">An administrator or group policy has made the file available offline.</span></span><br/>                                                                      |



 

</dd> <dt>

<span data-ttu-id="58de5-128">*lpOrgFileTime* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="58de5-128">*lpOrgFileTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58de5-129">Um ponteiro para uma estrutura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) para receber as informações de data e hora do arquivo ou subdiretório.</span><span class="sxs-lookup"><span data-stu-id="58de5-129">A pointer to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to receive the date and time information for the file or subdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58de5-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58de5-130">Return value</span></span>

<span data-ttu-id="58de5-131">Se a função for realizada com sucesso, o valor de retorno será um identificador de pesquisa usado em uma chamada subsequente para [**CSCFindNextFileW**](cscfindnextfilew.md) ou [**CSCFindClose**](cscfindclose.md).</span><span class="sxs-lookup"><span data-stu-id="58de5-131">If the function succeeds, the return value is a search handle used in a subsequent call to [**CSCFindNextFileW**](cscfindnextfilew.md) or [**CSCFindClose**](cscfindclose.md).</span></span>

<span data-ttu-id="58de5-132">Se a função falhar, o valor retornado será **INVALID\_HANDLE\_VALUE**.</span><span class="sxs-lookup"><span data-stu-id="58de5-132">If the function fails, the return value is **INVALID\_HANDLE\_VALUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="58de5-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="58de5-133">Remarks</span></span>

<span data-ttu-id="58de5-134">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="58de5-134">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="58de5-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58de5-135">Requirements</span></span>



| <span data-ttu-id="58de5-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="58de5-136">Requirement</span></span> | <span data-ttu-id="58de5-137">Valor</span><span class="sxs-lookup"><span data-stu-id="58de5-137">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58de5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="58de5-138">DLL</span></span><br/> | <dl> <span data-ttu-id="58de5-139"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58de5-139"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
