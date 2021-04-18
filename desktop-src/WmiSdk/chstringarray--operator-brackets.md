---
description: Esses operadores de subscrito definem ou obtêm o elemento no índice especificado. Esses operadores são um substituto conveniente para os métodos SetAt e GetAt.
ms.assetid: 93b10bef-908e-4c5e-aac3-b13051b2e7c9
ms.tgt_platform: multiple
title: 'CHStringArray:: operator [] (ChStrArr. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92b30768b9d013bfca672548a7c58b0eeffb455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780423"
---
# <a name="chstringarrayoperator--"></a><span data-ttu-id="5e59a-104">Operador \[ CHStringArray:: \]</span><span class="sxs-lookup"><span data-stu-id="5e59a-104">CHStringArray::operator \[ \]</span></span>

<span data-ttu-id="5e59a-105">\[A classe [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="5e59a-105">\[The [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="5e59a-106">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="5e59a-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="5e59a-107">Esses operadores de subscrito definem ou obtêm o elemento no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="5e59a-107">These subscript operators set or get the element at the specified index.</span></span> <span data-ttu-id="5e59a-108">Esses operadores são um substituto conveniente para os métodos [**SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) e [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) .</span><span class="sxs-lookup"><span data-stu-id="5e59a-108">These operators are a convenient substitute for the [**SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) and [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) methods.</span></span>

``` syntax
CHString& operator []( 
  int nIndex
);

CHString operator []( 
  int nIndex
) const;
```

## <a name="parameters"></a><span data-ttu-id="5e59a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e59a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e59a-110"><span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*</span><span class="sxs-lookup"><span data-stu-id="5e59a-110"><span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*</span></span>
</dt> <dd>

<span data-ttu-id="5e59a-111">Um índice inteiro que é maior ou igual a zero e menor ou igual ao valor retornado por [ **GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)</span><span class="sxs-lookup"><span data-stu-id="5e59a-111">An integer index that is greater than or equal to zero and less than or equal to the value returned by [**GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="5e59a-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="5e59a-112">Return Values</span></span>

<span data-ttu-id="5e59a-113">Os operadores de subscrito retornam o elemento de ponteiro [**CHString**](chstring.md) atualmente neste índice.</span><span class="sxs-lookup"><span data-stu-id="5e59a-113">The subscript operators return the [**CHString**](chstring.md) pointer element currently at this index.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e59a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e59a-114">Remarks</span></span>

<span data-ttu-id="5e59a-115">Você pode usar o primeiro operador, que chama matrizes que não são **const**, no lado direito (r-value) ou à esquerda (l-Value) de uma instrução de atribuição.</span><span class="sxs-lookup"><span data-stu-id="5e59a-115">You can use the first operator, which calls for arrays that are not **const**, on either the right (r-value) or the left (l-value) side of an assignment statement.</span></span> <span data-ttu-id="5e59a-116">O segundo, que chama matrizes **const** , pode ser usado somente à direita.</span><span class="sxs-lookup"><span data-stu-id="5e59a-116">The second, which calls for **const** arrays, can be used only on the right.</span></span>

<span data-ttu-id="5e59a-117">A versão de depuração da biblioteca é declarada se o subscrito (no lado esquerdo ou direito de uma instrução de atribuição) está fora dos limites.</span><span class="sxs-lookup"><span data-stu-id="5e59a-117">The debug version of the library asserts if the subscript (either on the left or right side of an assignment statement) is out of bounds.</span></span>

## <a name="examples"></a><span data-ttu-id="5e59a-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5e59a-118">Examples</span></span>

<span data-ttu-id="5e59a-119">O exemplo de código a seguir mostra o uso de [**CHStringArray: \[ \] : Operator**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5e59a-119">The following code example shows the use of [**CHStringArray::operator \[\]**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).</span></span>


```C++
CHStringArray array;
CHString s;

array.Add( L"String 1" ); // Element 0 
array.Add( L"String 2" ); // Element 1 
s = array[0]; // Get element 0
assert( s == L"String 1" ); 

array[0] = L"String 3"; // Replace element 0 
assert( array[0] == L"String 3" );
```



## <a name="requirements"></a><span data-ttu-id="5e59a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e59a-120">Requirements</span></span>



| <span data-ttu-id="5e59a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e59a-121">Requirement</span></span> | <span data-ttu-id="5e59a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5e59a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e59a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e59a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5e59a-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e59a-124">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="5e59a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e59a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5e59a-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e59a-126">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="5e59a-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e59a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e59a-128"><dt>ChStrArr. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e59a-128"><dt>ChStrArr.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5e59a-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5e59a-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="5e59a-130"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e59a-130"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="5e59a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5e59a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e59a-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e59a-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e59a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e59a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e59a-134">**CHStringArray:: Adicionar**</span><span class="sxs-lookup"><span data-stu-id="5e59a-134">**CHStringArray::Add**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
</dt> <dt>

<span data-ttu-id="5e59a-135">[**CHStringArray::GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span><span class="sxs-lookup"><span data-stu-id="5e59a-135">[**CHStringArray::GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span></span>
</dt> <dt>

<span data-ttu-id="5e59a-136">[**CHStringArray::SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="5e59a-136">[**CHStringArray::SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span></span>
</dt> </dl>

