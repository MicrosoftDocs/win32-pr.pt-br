---
description: O operador de concatenação + = une caracteres ao final desta cadeia de caracteres. O operador aceita outro objeto CHString, um ponteiro de caractere ou um único caractere.
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: 'CHString:: Operator + = (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683ca6b6264169cd156e89c3447c63fa59f03585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772589"
---
# <a name="chstringoperator"></a><span data-ttu-id="80cdb-104">CHString:: Operator + =</span><span class="sxs-lookup"><span data-stu-id="80cdb-104">CHString::operator+=</span></span>

<span data-ttu-id="80cdb-105">\[A classe [**CHString**](chstring.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="80cdb-105">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="80cdb-106">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="80cdb-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="80cdb-107">O operador de concatenação + = une caracteres ao final desta cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="80cdb-107">The += concatenation operator joins characters to the end of this string.</span></span> <span data-ttu-id="80cdb-108">O operador aceita outro objeto [**CHString**](chstring.md) , um ponteiro de caractere ou um único caractere.</span><span class="sxs-lookup"><span data-stu-id="80cdb-108">The operator accepts another [**CHString**](chstring.md) object, a character pointer, or a single character.</span></span>

``` syntax
const CHString& operator +=(
  const CHString& string )
throw( CHeap_Exception );

const CHString& operator +=(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator +=(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString operator +=(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="80cdb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80cdb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80cdb-110"><span id="string"></span><span id="STRING"></span>*Strings*</span><span class="sxs-lookup"><span data-stu-id="80cdb-110"><span id="string"></span><span id="STRING"></span>*string*</span></span>
</dt> <dd>

<span data-ttu-id="80cdb-111">Uma cadeia de caracteres [**CHString**](chstring.md) que concatena a esta cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="80cdb-111">A [**CHString**](chstring.md) string that concatenates to this string.</span></span>

</dd> <dt>

<span data-ttu-id="80cdb-112"><span id="ch"></span><span id="CH"></span>*CH*</span><span class="sxs-lookup"><span data-stu-id="80cdb-112"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="80cdb-113">Um caractere para concatenar a esta cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="80cdb-113">A character to concatenate to this string.</span></span>

</dd> <dt>

<span data-ttu-id="80cdb-114"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span><span class="sxs-lookup"><span data-stu-id="80cdb-114"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span></span>
</dt> <dd>

<span data-ttu-id="80cdb-115">Ponteiro para uma cadeia de caracteres terminada em **nulo** para concatenar a esta cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="80cdb-115">Pointer to a **NULL**-terminated string to concatenate to this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80cdb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="80cdb-116">Remarks</span></span>

<span data-ttu-id="80cdb-117">Lembre-se de que as exceções de memória podem ocorrer sempre que você usar esse operador de concatenação porque um novo armazenamento pode ser alocado para caracteres adicionados a esse objeto [**CHString**](chstring.md) .</span><span class="sxs-lookup"><span data-stu-id="80cdb-117">Be aware that memory exceptions can occur whenever you use this concatenation operator because new storage may be allocated for characters added to this [**CHString**](chstring.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="80cdb-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="80cdb-118">Examples</span></span>

<span data-ttu-id="80cdb-119">O exemplo a seguir mostra o uso de **CHString:: Operator + =**:</span><span class="sxs-lookup"><span data-stu-id="80cdb-119">The following example shows the use of **CHString::operator +=**:</span></span>


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
```



## <a name="requirements"></a><span data-ttu-id="80cdb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80cdb-120">Requirements</span></span>



| <span data-ttu-id="80cdb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="80cdb-121">Requirement</span></span> | <span data-ttu-id="80cdb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="80cdb-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80cdb-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80cdb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="80cdb-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80cdb-124">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="80cdb-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80cdb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="80cdb-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80cdb-126">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="80cdb-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80cdb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="80cdb-128"><dt>ChString. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80cdb-128"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="80cdb-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80cdb-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="80cdb-130"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80cdb-130"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="80cdb-131">DLL</span><span class="sxs-lookup"><span data-stu-id="80cdb-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80cdb-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80cdb-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80cdb-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="80cdb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80cdb-134">**CHString**</span><span class="sxs-lookup"><span data-stu-id="80cdb-134">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

