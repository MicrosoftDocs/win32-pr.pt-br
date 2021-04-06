---
description: O operador + concatenation une duas cadeias de caracteres e retorna um objeto CHString.
ms.assetid: b7ed6379-ccfa-40f9-9607-d9033179b674
ms.tgt_platform: multiple
title: 'CHString:: Operator + (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5053a4d3059a66cb2c8e4a89a3bdd531d5f42de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662728"
---
# <a name="chstringoperator"></a><span data-ttu-id="f1cbd-103">CHString:: Operator +</span><span class="sxs-lookup"><span data-stu-id="f1cbd-103">CHString::operator+</span></span>

<span data-ttu-id="f1cbd-104">\[A classe [**CHString**](chstring.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="f1cbd-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="f1cbd-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="f1cbd-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="f1cbd-106">O operador + concatenation une duas cadeias de caracteres e retorna um objeto [**CHString**](chstring.md) .</span><span class="sxs-lookup"><span data-stu-id="f1cbd-106">The + concatenation operator joins two strings and returns a [**CHString**](chstring.md) object.</span></span>

``` syntax
friend CHString operator +(
  const CHString& str1,
  const CHString& str2 )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  WCHAR ch )
throw( CHeap_Exception );

friend CHString operator +(
  WCHAR ch,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  LPCWSTR lpsz )
throw( CHeap_Exception );

friend CHString operator +(
  LPCWSTR lpsz,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  char ch )
throw( CHeap_Exception );

friend CHString operator +(
  char ch,
  const CHString& str )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="f1cbd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1cbd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1cbd-108"><span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*Str, str1, str2*</span><span class="sxs-lookup"><span data-stu-id="f1cbd-108"><span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*str, str1, str2*</span></span>
</dt> <dd>

<span data-ttu-id="f1cbd-109">[**CHString**](chstring.md) cadeias de caracteres que são concatenadas.</span><span class="sxs-lookup"><span data-stu-id="f1cbd-109">[**CHString**](chstring.md) strings that are concatenated.</span></span>

</dd> <dt>

<span data-ttu-id="f1cbd-110"><span id="ch"></span><span id="CH"></span>*CH*</span><span class="sxs-lookup"><span data-stu-id="f1cbd-110"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="f1cbd-111">Um caractere que concatena a uma cadeia de caracteres ou uma cadeia de caracteres que se concatena a um caractere.</span><span class="sxs-lookup"><span data-stu-id="f1cbd-111">A character that concatenates to a string or a string that concatenates to a character.</span></span>

</dd> <dt>

<span data-ttu-id="f1cbd-112"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span><span class="sxs-lookup"><span data-stu-id="f1cbd-112"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span></span>
</dt> <dd>

<span data-ttu-id="f1cbd-113">Ponteiro para uma cadeia de caracteres terminada em **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f1cbd-113">Pointer to a **NULL**-terminated character string.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="f1cbd-114">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="f1cbd-114">Return Values</span></span>

<span data-ttu-id="f1cbd-115">Esse operador de concatenação retorna um objeto [**CHString**](chstring.md) que é o resultado temporário da concatenação.</span><span class="sxs-lookup"><span data-stu-id="f1cbd-115">This concatenation operator returns a [**CHString**](chstring.md) object that is the temporary result of the concatenation.</span></span> <span data-ttu-id="f1cbd-116">Esse valor de retorno torna possível combinar várias concatenações na mesma expressão.</span><span class="sxs-lookup"><span data-stu-id="f1cbd-116">This return value makes it possible to combine several concatenations in the same expression.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1cbd-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1cbd-117">Remarks</span></span>

<span data-ttu-id="f1cbd-118">Uma das duas cadeias de caracteres de argumento deve ser um objeto [**CHString**](chstring.md) ; o outro pode ser um ponteiro de caractere ou um caractere.</span><span class="sxs-lookup"><span data-stu-id="f1cbd-118">One of the two argument strings must be a [**CHString**](chstring.md) object; the other can be a character pointer or a character.</span></span> <span data-ttu-id="f1cbd-119">Lembre-se de que as exceções de memória podem ocorrer sempre que você usar o operador de concatenação porque um novo armazenamento pode ser alocado para manter dados temporários.</span><span class="sxs-lookup"><span data-stu-id="f1cbd-119">Be aware that memory exceptions can occur whenever you use the concatenation operator because new storage may be allocated to hold temporary data.</span></span>

## <a name="examples"></a><span data-ttu-id="f1cbd-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f1cbd-120">Examples</span></span>

<span data-ttu-id="f1cbd-121">O exemplo de código a seguir mostra o uso de **CHString:: Operator +**:</span><span class="sxs-lookup"><span data-stu-id="f1cbd-121">The following code example shows the use of **CHString::operator +**:</span></span>


```C++
CHString s1( L"abc" );
CHString s2( L"def" );
assert( (s1 + s2 ) == L"abcdef" );

CHString s3;
s3 = CHString( L"abc" ) + "def" ; // Correct
s3 = "abc" + "def"; // Wrong. The first argument must be a CHString.
```



## <a name="requirements"></a><span data-ttu-id="f1cbd-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1cbd-122">Requirements</span></span>



| <span data-ttu-id="f1cbd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1cbd-123">Requirement</span></span> | <span data-ttu-id="f1cbd-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f1cbd-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1cbd-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1cbd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f1cbd-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1cbd-126">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="f1cbd-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1cbd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f1cbd-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1cbd-128">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="f1cbd-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1cbd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1cbd-130"><dt>ChString. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1cbd-130"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f1cbd-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1cbd-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="f1cbd-132"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1cbd-132"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="f1cbd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f1cbd-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1cbd-134"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1cbd-134"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1cbd-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1cbd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1cbd-136">**CHString**</span><span class="sxs-lookup"><span data-stu-id="f1cbd-136">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

