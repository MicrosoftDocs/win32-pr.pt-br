---
title: Função EnumEnabledLayoutOrTip
description: Enumera todos os layouts de teclado ou serviços de texto habilitados da configuração de usuário especificada.
ms.assetid: b3c57e88-e04b-411b-9eba-83258da16773
keywords:
- Estrutura de serviços de texto da função EnumEnabledLayoutOrTip
topic_type:
- apiref
api_name:
- EnumEnabledLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b192896dd95d5ab8f306158e33a8d248793bfc10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789469"
---
# <a name="enumenabledlayoutortip-function"></a><span data-ttu-id="10f23-104">Função EnumEnabledLayoutOrTip</span><span class="sxs-lookup"><span data-stu-id="10f23-104">EnumEnabledLayoutOrTip function</span></span>

<span data-ttu-id="10f23-105">Enumera todos os layouts de teclado ou serviços de texto habilitados da configuração de usuário especificada.</span><span class="sxs-lookup"><span data-stu-id="10f23-105">Enumerates all enabled keyboard layouts or text services of the specified user setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="10f23-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10f23-106">Syntax</span></span>


```C++
UINT EnumEnabledLayoutOrTip(
  _In_opt_ LPCWSTR            pszUserReg,
  _In_opt_ LPCWSTR            pszSystemReg,
  _In_opt_ LPCWSTR            pszSoftwareReg,
  _Out_    LAYOUTORTIPPROFILE *pLayoutOrTipProfile,
  _In_     UINT               uBufLength
);
```



## <a name="parameters"></a><span data-ttu-id="10f23-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10f23-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10f23-108">*pszUserReg* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="10f23-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="10f23-109">O caminho do registro do usuário.</span><span class="sxs-lookup"><span data-stu-id="10f23-109">The registry path of the user.</span></span> <span data-ttu-id="10f23-110">Se esse parâmetro for **NULL**, hKey \_ Current \_ User será usado.</span><span class="sxs-lookup"><span data-stu-id="10f23-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="10f23-111">*pszSystemReg* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="10f23-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="10f23-112">O caminho do registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="10f23-112">The registry path of the system.</span></span> <span data-ttu-id="10f23-113">Se esse parâmetro for **NULL**, hKey \_ local \_ Machine \\ System será usado.</span><span class="sxs-lookup"><span data-stu-id="10f23-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="10f23-114">*pszSoftwareReg* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="10f23-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="10f23-115">O caminho do registro do software.</span><span class="sxs-lookup"><span data-stu-id="10f23-115">The registry path of the software.</span></span> <span data-ttu-id="10f23-116">Se esse parâmetro for **NULL**, hKey \_ local \_ Machine \\ software será usado.</span><span class="sxs-lookup"><span data-stu-id="10f23-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="10f23-117">*pLayoutOrTipProfile* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="10f23-117">*pLayoutOrTipProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10f23-118">Ponteiro para o buffer que recebe a matriz LAYOUTORTIPPROFILE.</span><span class="sxs-lookup"><span data-stu-id="10f23-118">Pointer to the buffer that receives the LAYOUTORTIPPROFILE array.</span></span>

</dd> <dt>

<span data-ttu-id="10f23-119">*uBufLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="10f23-119">*uBufLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10f23-120">O comprimento do buffer apontado por *pLayoutOrTipProfile*.</span><span class="sxs-lookup"><span data-stu-id="10f23-120">The length of the buffer pointed to by *pLayoutOrTipProfile*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10f23-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="10f23-121">Return value</span></span>

<span data-ttu-id="10f23-122">Se *pLayoutOrTipProfile* for **nulo**, o número de itens de teclado habilitados na configuração de usuário; caso contrário, o número de itens de teclado que são copiados em *pLayoutOrTipProfile*.</span><span class="sxs-lookup"><span data-stu-id="10f23-122">If *pLayoutOrTipProfile* is **NULL**, the number of keyboard items that are enabled in the user setting; otherwise, the number of keyboard items that are copied into *pLayoutOrTipProfile*.</span></span>

<span data-ttu-id="10f23-123">Para idiomas do IME (editor de método de entrada), todos os IMEs são retornados, mesmo quando apenas um IME está habilitado.</span><span class="sxs-lookup"><span data-stu-id="10f23-123">For Input Method Editor (IME) languages, all IMEs are returned, even when only one IME is enabled.</span></span> <span data-ttu-id="10f23-124">Por exemplo, se um usuário tiver o novo IME rápido do CHT habilitado, a função **EnumEnabledLayoutOrTip** retornará todos os 5 IMEs do CHT.</span><span class="sxs-lookup"><span data-stu-id="10f23-124">For example, if a user has the CHT New Quick IME enabled, the **EnumEnabledLayoutOrTip** function returns all 5 CHT IMEs.</span></span>

## <a name="remarks"></a><span data-ttu-id="10f23-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="10f23-125">Remarks</span></span>

<span data-ttu-id="10f23-126">Não há biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="10f23-126">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="10f23-127">O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada.</span><span class="sxs-lookup"><span data-stu-id="10f23-127">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="10f23-128">Consulte a [ordem de pesquisa da biblioteca de vínculo dinâmico](/windows/desktop/Dlls/dynamic-link-library-search-order) para obter informações sobre como carregar corretamente DLLs com versões diferentes do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="10f23-128">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="10f23-129">A definição de LAYOUTORTIPPROFILE é:</span><span class="sxs-lookup"><span data-stu-id="10f23-129">The definition of LAYOUTORTIPPROFILE is:</span></span>

``` syntax
typedef struct tagLAYOUTORTIPPROFILE {
    DWORD  dwProfileType;       // InputProcessor or HKL 
#define LOTP_INPUTPROCESSOR 1
#define LOTP_KEYBOARDLAYOUT 2
    LANGID langid;              // language id 
    CLSID  clsid;               // CLSID of tip 
    GUID   guidProfile;         // profile description 
    GUID   catid;               // category of tip 
    DWORD  dwSubstituteLayout;  // substitute hkl 
    DWORD  dwFlags;             // Flags 
    WCHAR  szId[MAX_PATH];      // KLID or TIP profile for string 
} LAYOUTORTIPPROFILE;
```

## <a name="requirements"></a><span data-ttu-id="10f23-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10f23-130">Requirements</span></span>



| <span data-ttu-id="10f23-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="10f23-131">Requirement</span></span> | <span data-ttu-id="10f23-132">Valor</span><span class="sxs-lookup"><span data-stu-id="10f23-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="10f23-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10f23-133">Minimum supported client</span></span><br/> | <span data-ttu-id="10f23-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10f23-134">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="10f23-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10f23-135">Minimum supported server</span></span><br/> | <span data-ttu-id="10f23-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="10f23-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="10f23-137">DLL</span><span class="sxs-lookup"><span data-stu-id="10f23-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10f23-138"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10f23-138"><dt>Input.dll</dt></span></span> </dl> |



 

