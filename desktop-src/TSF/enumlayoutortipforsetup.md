---
title: Função EnumLayoutOrTipForSetup
description: Enumera os layouts de teclado instalados e os serviços de texto da interface do usuário da instalação ou do OOBE.
ms.assetid: 3c6fc11c-36a5-4718-b584-b7f98f1b4180
keywords:
- Estrutura de serviços de texto da função EnumLayoutOrTipForSetup
topic_type:
- apiref
api_name:
- EnumLayoutOrTipForSetup
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c9a65e0d966684329996e4f5d23370592250a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105767780"
---
# <a name="enumlayoutortipforsetup-function"></a><span data-ttu-id="312cf-104">Função EnumLayoutOrTipForSetup</span><span class="sxs-lookup"><span data-stu-id="312cf-104">EnumLayoutOrTipForSetup function</span></span>

<span data-ttu-id="312cf-105">Enumera os layouts de teclado instalados e os serviços de texto da interface do usuário da instalação ou do OOBE.</span><span class="sxs-lookup"><span data-stu-id="312cf-105">Enumerates the installed keyboard layouts and text services of the setup UI or OOBE.</span></span>

## <a name="syntax"></a><span data-ttu-id="312cf-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="312cf-106">Syntax</span></span>


```C++
UINT CALLBACK EnumLayoutOrTipForSetup(
  _In_  LANGID      langid,
  _Out_ LAYOUTORTIP *pLayoutOrTip,
  _In_  UINT        uBufLength,
  _In_  DWORD       dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="312cf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="312cf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="312cf-108">*LangID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="312cf-108">*langid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="312cf-109">A ID de idioma do item a ser enumerado.</span><span class="sxs-lookup"><span data-stu-id="312cf-109">The language id of the item to be enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="312cf-110">*pLayoutOrTip* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="312cf-110">*pLayoutOrTip* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="312cf-111">Ponteiro para o buffer que recebe a matriz de estruturas LAYOUTORTIP.</span><span class="sxs-lookup"><span data-stu-id="312cf-111">Pointer to the buffer that receives the array of LAYOUTORTIP structures.</span></span> <span data-ttu-id="312cf-112">Isso pode ser **nulo** para obter o número de itens.</span><span class="sxs-lookup"><span data-stu-id="312cf-112">This can be **NULL** to get the number of items.</span></span>

</dd> <dt>

<span data-ttu-id="312cf-113">*uBufLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="312cf-113">*uBufLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="312cf-114">O comprimento do buffer apontado por *pLayoutOrTip*.</span><span class="sxs-lookup"><span data-stu-id="312cf-114">The length of the buffer pointed to by *pLayoutOrTip*.</span></span> <span data-ttu-id="312cf-115">Isso será ignorado se *pLayoutOrTip* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="312cf-115">This is ignored if *pLayoutOrTip* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="312cf-116">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="312cf-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="312cf-117">Não usado.</span><span class="sxs-lookup"><span data-stu-id="312cf-117">Not used.</span></span> <span data-ttu-id="312cf-118">Isso deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="312cf-118">This must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="312cf-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="312cf-119">Return value</span></span>

<span data-ttu-id="312cf-120">Se *pLayoutOrTip* for **nulo**, o número de itens de teclado que são registrados no sistema; caso contrário, o número de itens de teclado que são copiados em *pLayoutOrTip*.</span><span class="sxs-lookup"><span data-stu-id="312cf-120">If *pLayoutOrTip* is **NULL**, the number of keyboard items that are registered in System; otherwise, the number of keyboard items that are copied into *pLayoutOrTip*.</span></span>

## <a name="remarks"></a><span data-ttu-id="312cf-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="312cf-121">Remarks</span></span>

<span data-ttu-id="312cf-122">Não há biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="312cf-122">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="312cf-123">O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada.</span><span class="sxs-lookup"><span data-stu-id="312cf-123">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="312cf-124">Consulte a [ordem de pesquisa da biblioteca de vínculo dinâmico](/windows/desktop/Dlls/dynamic-link-library-search-order) para obter informações sobre como carregar corretamente DLLs com versões diferentes do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="312cf-124">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="312cf-125">A definição de LAYOUTORTIP é:</span><span class="sxs-lookup"><span data-stu-id="312cf-125">The definition of LAYOUTORTIP is:</span></span>

``` syntax
typedef struct tagLAYOUTORTIP {
    DWORD dwFlags;
#define LOT_DEFAULT    0x0001 // If this is on, this is a default item. 
#define LOT_DISABLED   0x0002 // if this is on, this is not enabled. 
    WCHAR szId[MAX_PATH]; // Id of the keyboard item in the string format. 
    WCHAR szName[MAX_PATH]; // The description of the keyboard item. 
} LAYOUTORTIP;
```

## <a name="requirements"></a><span data-ttu-id="312cf-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="312cf-126">Requirements</span></span>



| <span data-ttu-id="312cf-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="312cf-127">Requirement</span></span> | <span data-ttu-id="312cf-128">Valor</span><span class="sxs-lookup"><span data-stu-id="312cf-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="312cf-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="312cf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="312cf-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="312cf-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="312cf-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="312cf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="312cf-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="312cf-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="312cf-133">DLL</span><span class="sxs-lookup"><span data-stu-id="312cf-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="312cf-134"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="312cf-134"><dt>Input.dll</dt></span></span> </dl> |



 

