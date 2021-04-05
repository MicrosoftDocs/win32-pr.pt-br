---
description: O operador de atribuição CHString (=) reinicializa um objeto CHString existente com novos dados.
ms.assetid: 6864aacf-ac18-4b5a-be3e-3a0d8bb31e74
ms.tgt_platform: multiple
title: 'CHString:: Operator = (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9abfa9ea2b72aa8f6830d9fb6388861c8c3b82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011128"
---
# <a name="chstringoperator"></a><span data-ttu-id="d88a0-103">CHString:: Operator =</span><span class="sxs-lookup"><span data-stu-id="d88a0-103">CHString::operator=</span></span>

<span data-ttu-id="d88a0-104">\[A classe [**CHString**](chstring.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="d88a0-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="d88a0-105">As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]</span><span class="sxs-lookup"><span data-stu-id="d88a0-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="d88a0-106">O operador de atribuição [**CHString**](chstring.md) (=) reinicializa um objeto CHString existente com novos dados.</span><span class="sxs-lookup"><span data-stu-id="d88a0-106">The [**CHString**](chstring.md) assignment (=) operator reinitializes an existing CHString object with new data.</span></span>

``` syntax
const CHString& operator =(
  const CHString& stringSrc )
throw( CHeap_Exception );

const CHString& operator =(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator =(
  const unsigned char* psz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  CHString *p )
throw( CHeap_Exception );

const CHString& operator =(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="d88a0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d88a0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d88a0-108"><span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*, *p*</span><span class="sxs-lookup"><span data-stu-id="d88a0-108"><span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*, *p*</span></span>
</dt> <dd>

<span data-ttu-id="d88a0-109">Atribui uma cadeia de caracteres [**CHString**](chstring.md) a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="d88a0-109">Assigns a [**CHString**](chstring.md) string to this object.</span></span>

</dd> <dt>

<span data-ttu-id="d88a0-110"><span id="ch"></span><span id="CH"></span>*CH*</span><span class="sxs-lookup"><span data-stu-id="d88a0-110"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="d88a0-111">Atribui um caractere a este objeto.</span><span class="sxs-lookup"><span data-stu-id="d88a0-111">Assigns a character to this object.</span></span>

</dd> <dt>

<span data-ttu-id="d88a0-112"><span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *psz*</span><span class="sxs-lookup"><span data-stu-id="d88a0-112"><span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *psz*</span></span>
</dt> <dd>

<span data-ttu-id="d88a0-113">Atribui uma cadeia de caracteres terminada em **nulo** para este objeto.</span><span class="sxs-lookup"><span data-stu-id="d88a0-113">Assigns a **NULL**-terminated string to this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d88a0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d88a0-114">Remarks</span></span>

<span data-ttu-id="d88a0-115">Se a cadeia de caracteres de destino (ou seja, o lado esquerdo) já for grande o suficiente para armazenar os novos dados, nenhuma alocação de memória nova será executada.</span><span class="sxs-lookup"><span data-stu-id="d88a0-115">If the destination string (that is, the left side) is already large enough to store the new data, no new memory allocation is performed.</span></span> <span data-ttu-id="d88a0-116">No entanto, as exceções de memória podem ocorrer sempre que você usar o operador de atribuição, pois um novo armazenamento geralmente é alocado para conter o objeto [**CHString**](chstring.md) resultante.</span><span class="sxs-lookup"><span data-stu-id="d88a0-116">However, memory exceptions can occur whenever you use the assignment operator because new storage is often allocated to hold the resulting [**CHString**](chstring.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="d88a0-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d88a0-117">Examples</span></span>

<span data-ttu-id="d88a0-118">O exemplo de código a seguir mostra o uso de **CHString:: Operator =**:</span><span class="sxs-lookup"><span data-stu-id="d88a0-118">The following code example shows the use of **CHString::operator =**:</span></span>


```C++
CHString s1, s2;        // Empty CHString objects

s1 = L"cat";            // s1 = "cat"
s2 = s1;                // s1 and s2 each = "cat"
s1 = L"the " + s1;      // Or expressions
s1 = 'x';               // Or just individual characters
```



## <a name="requirements"></a><span data-ttu-id="d88a0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d88a0-119">Requirements</span></span>



| <span data-ttu-id="d88a0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d88a0-120">Requirement</span></span> | <span data-ttu-id="d88a0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d88a0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d88a0-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d88a0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d88a0-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d88a0-123">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="d88a0-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d88a0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d88a0-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d88a0-125">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="d88a0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d88a0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d88a0-127"><dt>ChString. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d88a0-127"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d88a0-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d88a0-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="d88a0-129"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d88a0-129"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="d88a0-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d88a0-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d88a0-131"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d88a0-131"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d88a0-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d88a0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d88a0-133">**CHString**</span><span class="sxs-lookup"><span data-stu-id="d88a0-133">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

