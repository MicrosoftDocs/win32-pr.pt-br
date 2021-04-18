---
description: Continua uma operação de pesquisa de arquivo.
ms.assetid: 5b1a8f67-7fce-4ba5-918d-826bdaca1947
title: Função CSCFindNextFileW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindNextFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 50b387a1ff99a95fcbe0fae8fe8ad93d14c335b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756219"
---
# <a name="cscfindnextfilew-function"></a><span data-ttu-id="8195b-103">Função CSCFindNextFileW</span><span class="sxs-lookup"><span data-stu-id="8195b-103">CSCFindNextFileW function</span></span>

<span data-ttu-id="8195b-104">\[Essa função não tem suporte e não deve ser usada.\]</span><span class="sxs-lookup"><span data-stu-id="8195b-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="8195b-105">Continua uma operação de pesquisa de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8195b-105">Continues a file search operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8195b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8195b-106">Syntax</span></span>


```C++
BOOL WINAPI CSCFindNextFileW(
  _In_  HANDLE           hFind,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _In_  FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a><span data-ttu-id="8195b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8195b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8195b-108">*hFind* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8195b-108">*hFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8195b-109">Um identificador de pesquisa retornado pela função [**CSCFindFirstFileW**](cscfindfirstfilew.md) .</span><span class="sxs-lookup"><span data-stu-id="8195b-109">A search handle returned by the [**CSCFindFirstFileW**](cscfindfirstfilew.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="8195b-110">*lpFind32* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8195b-110">*lpFind32* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8195b-111">Um ponteiro para a estrutura de [**\_ \_ dados de localização do Win32**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) que recebe informações sobre o arquivo ou subdiretório.</span><span class="sxs-lookup"><span data-stu-id="8195b-111">A pointer to the [**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) structure that receives information about the file or subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="8195b-112">*lpdwStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8195b-112">*lpdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8195b-113">Um código NTSTATUS que indica o status da chamada.</span><span class="sxs-lookup"><span data-stu-id="8195b-113">An NTSTATUS code that indicates the status of the call.</span></span>

</dd> <dt>

<span data-ttu-id="8195b-114">*lpdwPinCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8195b-114">*lpdwPinCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8195b-115">Esse parâmetro será diferente de zero se o arquivo tiver sido disponibilizado offline ou 0 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="8195b-115">This parameter is nonzero if the file has been made available offline or 0 otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="8195b-116">*lpdwHintFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8195b-116">*lpdwHintFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8195b-117">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8195b-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="8195b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8195b-118">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="8195b-119">Significado</span><span class="sxs-lookup"><span data-stu-id="8195b-119">Meaning</span></span>                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <span data-ttu-id="8195b-120"><dt>**Sinalizador \_ \_Usuário de \_ PIN \_ de dica de CSC**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8195b-120"><dt>**FLAG\_CSC\_HINT\_PIN\_USER**</dt> <dt>0x01</dt></span></span> </dl>                                | <span data-ttu-id="8195b-121">Um usuário tornou o arquivo disponível offline.</span><span class="sxs-lookup"><span data-stu-id="8195b-121">A user has made the file available offline.</span></span><br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <span data-ttu-id="8195b-122"><dt>**Sinalizador \_ PIN de dica de CSC \_ \_ \_ herdar o \_ usuário**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="8195b-122"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_USER**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="8195b-123">Um usuário tornou o pai disponível offline e marcou o pai de modo que seus filhos estejam disponíveis offline.</span><span class="sxs-lookup"><span data-stu-id="8195b-123">A user has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <span data-ttu-id="8195b-124"><dt>**Sinalizador \_ O \_ PIN da dica de CSC \_ herda o \_ \_ sistema**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="8195b-124"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_SYSTEM**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="8195b-125">Uma política de administrador ou de grupo tornou o pai disponível offline e marcou o pai de modo que seus filhos estejam disponíveis offline.</span><span class="sxs-lookup"><span data-stu-id="8195b-125">An administrator or group policy has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <span data-ttu-id="8195b-126"><dt>**Sinalizador \_ O \_ \_ \_ sistema de PIN de dica do CSC**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="8195b-126"><dt>**FLAG\_CSC\_HINT\_PIN\_SYSTEM**</dt> <dt>0x10</dt></span></span> </dl>                          | <span data-ttu-id="8195b-127">Um administrador ou política de grupo disponibilizou o arquivo offline.</span><span class="sxs-lookup"><span data-stu-id="8195b-127">An administrator or group policy has made the file available offline.</span></span><br/>                                                                      |



 

</dd> <dt>

<span data-ttu-id="8195b-128">*lpOrgFileTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8195b-128">*lpOrgFileTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8195b-129">Um ponteiro para uma estrutura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) para receber as informações de data e hora do arquivo ou subdiretório.</span><span class="sxs-lookup"><span data-stu-id="8195b-129">A pointer to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to receive the date and time information for the file or subdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8195b-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8195b-130">Return value</span></span>

<span data-ttu-id="8195b-131">Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="8195b-131">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8195b-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="8195b-132">Remarks</span></span>

<span data-ttu-id="8195b-133">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="8195b-133">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8195b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8195b-134">Requirements</span></span>



| <span data-ttu-id="8195b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="8195b-135">Requirement</span></span> | <span data-ttu-id="8195b-136">Valor</span><span class="sxs-lookup"><span data-stu-id="8195b-136">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8195b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8195b-137">DLL</span></span><br/> | <dl> <span data-ttu-id="8195b-138"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8195b-138"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
