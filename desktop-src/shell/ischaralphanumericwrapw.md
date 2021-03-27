---
description: Determina se um caractere é um caractere alfabético ou numérico.
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: Função IsCharAlphaNumericWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCharAlphaNumericWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bf7f1b4db54cc5374214ff45b51579556dc22062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967543"
---
# <a name="ischaralphanumericwrapw-function"></a><span data-ttu-id="9f1f5-103">Função IsCharAlphaNumericWrapW</span><span class="sxs-lookup"><span data-stu-id="9f1f5-103">IsCharAlphaNumericWrapW function</span></span>

<span data-ttu-id="9f1f5-104">\[O **IsCharAlphaNumericWrapW** está disponível para uso no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9f1f5-104">\[**IsCharAlphaNumericWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="9f1f5-105">Ele não estará disponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="9f1f5-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="9f1f5-106">Você deve usar [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) em seu lugar.\]</span><span class="sxs-lookup"><span data-stu-id="9f1f5-106">You should use [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in its place.\]</span></span>

<span data-ttu-id="9f1f5-107">Determina se um caractere é um caractere alfabético ou numérico.</span><span class="sxs-lookup"><span data-stu-id="9f1f5-107">Determines whether a character is either an alphabetical or a numeric character.</span></span> <span data-ttu-id="9f1f5-108">Essa determinação se baseia na semântica do idioma selecionado pelo usuário durante a instalação ou por meio do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="9f1f5-108">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span>

> [!Note]  
> <span data-ttu-id="9f1f5-109">**IsCharAlphaNumericWrapW** é um wrapper para a função **IsCharAlphaNumericW** .</span><span class="sxs-lookup"><span data-stu-id="9f1f5-109">**IsCharAlphaNumericWrapW** is a wrapper for the **IsCharAlphaNumericW** function.</span></span> <span data-ttu-id="9f1f5-110">Consulte a página [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) para ver mais observações de uso.</span><span class="sxs-lookup"><span data-stu-id="9f1f5-110">See the [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9f1f5-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f1f5-111">Syntax</span></span>


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a><span data-ttu-id="9f1f5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f1f5-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f1f5-113">*ch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9f1f5-113">*ch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f1f5-114">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="9f1f5-114">Type: **WCHAR**</span></span>

<span data-ttu-id="9f1f5-115">O caractere Unicode a ser testado.</span><span class="sxs-lookup"><span data-stu-id="9f1f5-115">The Unicode character to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f1f5-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f1f5-116">Return value</span></span>

<span data-ttu-id="9f1f5-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="9f1f5-117">Type: **BOOL**</span></span>

<span data-ttu-id="9f1f5-118">Se o caractere for alfanumérico, o valor de retorno será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="9f1f5-118">If the character is alphanumeric, the return value is nonzero.</span></span>

<span data-ttu-id="9f1f5-119">Se o caractere não for alfanumérico, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="9f1f5-119">If the character is not alphanumeric, the return value is zero.</span></span> <span data-ttu-id="9f1f5-120">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="9f1f5-120">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f1f5-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f1f5-121">Remarks</span></span>

<span data-ttu-id="9f1f5-122">O **IsCharAlphaNumericWrapW** fornece a capacidade de usar cadeias de caracteres Unicode em sistemas operacionais anteriores ao Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9f1f5-122">**IsCharAlphaNumericWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="9f1f5-123">O método preferencial é usar [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) em conjunto com a camada Microsoft para Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="9f1f5-123">The preferred method is to use [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="9f1f5-124">**IsCharAlphaNumericWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 28.</span><span class="sxs-lookup"><span data-stu-id="9f1f5-124">**IsCharAlphaNumericWrapW** must be called directly from Shlwapi.dll, using ordinal 28.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f1f5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f1f5-125">Requirements</span></span>



| <span data-ttu-id="9f1f5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f1f5-126">Requirement</span></span> | <span data-ttu-id="9f1f5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9f1f5-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f1f5-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f1f5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9f1f5-129">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9f1f5-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f1f5-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f1f5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9f1f5-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9f1f5-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9f1f5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9f1f5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f1f5-133"><dt>Shlwapi.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9f1f5-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f1f5-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f1f5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f1f5-135">**IsCharAlphaNumeric**</span><span class="sxs-lookup"><span data-stu-id="9f1f5-135">**IsCharAlphaNumeric**</span></span>](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
