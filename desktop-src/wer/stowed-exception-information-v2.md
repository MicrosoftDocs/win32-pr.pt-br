---
title: Estrutura de STOWED_EXCEPTION_INFORMATION_V2
description: Contém informações de exceção dedevidas.
ms.assetid: 79267974-EE1B-4427-A6D6-265F6BC5D73A
keywords:
- Estrutura de STOWED_EXCEPTION_INFORMATION_V2 Relatório de Erros do Windows
- Ponteiro de estrutura de PSTOWED_EXCEPTION_INFORMATION_V2 Relatório de Erros do Windows
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_V2
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefd313f0edcc122708f141cd65418beaade03a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782622"
---
# <a name="stowed_exception_information_v2-structure"></a><span data-ttu-id="4cc9e-105">\_ \_ Estrutura v2 de informações de exceção dedevida \_</span><span class="sxs-lookup"><span data-stu-id="4cc9e-105">STOWED\_EXCEPTION\_INFORMATION\_V2 structure</span></span>

<span data-ttu-id="4cc9e-106">Contém informações de exceção dedevidas.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-106">Contains stowed exception info.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cc9e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4cc9e-107">Syntax</span></span>


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_V2 {
  STOWED_EXCEPTION_INFORMATION_HEADER Header;
  HRESULT                             ResultCode;
  struct {
    DWORD ExceptionForm  :2;
    DWORD ThreadId  :30;
  };
  union {
    struct {
      PVOID ExceptionAddress;
      ULONG StackTraceWordSize;
      ULONG StackTraceWords;
      PVOID StackTrace;
    };
    struct {
      PWSTR ErrorText;
    };
  };
  ULONG                               NestedExceptionType;
  PVOID                               NestedException;
} STOWED_EXCEPTION_INFORMATION_V2, *PSTOWED_EXCEPTION_INFORMATION_V2;
```



## <a name="members"></a><span data-ttu-id="4cc9e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4cc9e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4cc9e-109">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-109">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="4cc9e-110">Tipo: **[ **\_ \_ \_ cabeçalho de informações de exceção dedevida**](stowed-exception-information-header.md)**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-110">Type: **[**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4cc9e-111">A estrutura de [**cabeçalho de \_ informações de exceção \_ \_ dedevida**](stowed-exception-information-header.md) que contém informações para esta estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-111">The [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md) structure that contains info for this parent structure.</span></span>

</dd> <dt>

<span data-ttu-id="4cc9e-112">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-112">**ResultCode**</span></span>
</dt> <dd>

<span data-ttu-id="4cc9e-113">Tipo: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-113">Type: **[**HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4cc9e-114">O código [**HRESULT**](/windows/desktop/WinProg/windows-data-types) para a exceção de dedevida.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-114">The [**HRESULT**](/windows/desktop/WinProg/windows-data-types) code for the stowed exception.</span></span>

</dd> <dt>

<span data-ttu-id="4cc9e-115">**ExceptionForm**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-115">**ExceptionForm**</span></span>
</dt> <dd>

<span data-ttu-id="4cc9e-116">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-116">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4cc9e-117">Um valor de 2 bits que identifica a forma da exceção.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-117">A 2-bit value that identifies the form of the exception.</span></span>



| <span data-ttu-id="4cc9e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4cc9e-118">Value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="4cc9e-119">Significado</span><span class="sxs-lookup"><span data-stu-id="4cc9e-119">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_FORM_BINARY"></span><span id="stowed_exception_form_binary"></span><dl> <span data-ttu-id="4cc9e-120">Em <dt>**DEdevido \_ Formato de exceção \_ \_ Binary**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="4cc9e-120"><dt>**STOWED\_EXCEPTION\_FORM\_BINARY**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="4cc9e-121">Esse valor indica que a forma da exceção é binária.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-121">This value indicates that the form of the exception is binary.</span></span><br/> |
| <span id="STOWED_EXCEPTION_FORM_TEXT"></span><span id="stowed_exception_form_text"></span><dl> <span data-ttu-id="4cc9e-122">Em <dt>**DEdevido \_ \_ \_ Texto de formulário de exceção**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="4cc9e-122"><dt>**STOWED\_EXCEPTION\_FORM\_TEXT**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="4cc9e-123">Esse valor indica que a forma da exceção é texto.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-123">This value indicates that the form of the exception is text.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="4cc9e-124">**ThreadId**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-124">**ThreadId**</span></span>
</dt> <dd>

<span data-ttu-id="4cc9e-125">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-125">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4cc9e-126">Um valor de 30 bits que identifica o thread que gerou a exceção.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-126">A 30-bit value that identifies the thread that raised the exception.</span></span> <span data-ttu-id="4cc9e-127">O valor é deslocado para a direita em 2 bits quando ele é armazenado.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-127">The value is shifted to the right by 2 bits when it's stored.</span></span> <span data-ttu-id="4cc9e-128">Para convertê-lo de volta em uma ID de thread válida, mude o valor para a esquerda por 2.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-128">To convert it back to a valid thread ID, shift the value to the left by 2.</span></span> <span data-ttu-id="4cc9e-129">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="4cc9e-129">For example:</span></span>

``` syntax
DWORD ActualThreadId = (StowedException.ThreadId << 2);
```

</dd> <dt>

<span data-ttu-id="4cc9e-130">(*struct sem nome*)</span><span class="sxs-lookup"><span data-stu-id="4cc9e-130">(*unnamed struct*)</span></span>
</dt> <dd>

<span data-ttu-id="4cc9e-131">Os membros dessa estrutura aninhada serão válidos somente se o membro **ExceptionForm** estiver definido como **binário de \_ \_ formulário de \_ exceção dedevida**.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-131">The members of this nested structure are valid only if the **ExceptionForm** member is set to **STOWED\_EXCEPTION\_FORM\_BINARY**.</span></span>

<dl> <dt>

<span data-ttu-id="4cc9e-132">**ExceptionAddress**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-132">**ExceptionAddress**</span></span>
</dt> <dd>

<span data-ttu-id="4cc9e-133">Tipo: **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-133">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4cc9e-134">Um ponteiro que contém o endereço de exceção.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-134">A pointer that contains the exception address.</span></span>

</dd> <dt>

<span data-ttu-id="4cc9e-135">**StackTraceWordSize**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-135">**StackTraceWordSize**</span></span>
</dt> <dd>

<span data-ttu-id="4cc9e-136">Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-136">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4cc9e-137">Tamanho, em bytes, de cada palavra no rastreamento de pilha para o qual o membro de **StackTrace** aponta.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-137">Size, in bytes, of each word in the stack trace that the **StackTrace** member points to.</span></span> <span data-ttu-id="4cc9e-138">Esse valor é definido como 4 para plataformas de 32 bits e 8 para plataformas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-138">This value is set to 4 for 32-bit platforms and 8 for 64-bit platforms.</span></span>

</dd> <dt>

<span data-ttu-id="4cc9e-139">**StackTraceWords**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-139">**StackTraceWords**</span></span>
</dt> <dd>

<span data-ttu-id="4cc9e-140">Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-140">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4cc9e-141">O número de palavras no rastreamento de pilha para o qual o membro de **StackTrace** aponta.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-141">The number of words in the stack trace that the **StackTrace** member points to.</span></span> <span data-ttu-id="4cc9e-142">O número de palavras é igual ao número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-142">The number of words is equal to the number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="4cc9e-143">**Pilha**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-143">**StackTrace**</span></span>
</dt> <dd>

<span data-ttu-id="4cc9e-144">Tipo: **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-144">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4cc9e-145">Um ponteiro para um bloco de memória que contém o rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-145">A pointer to a memory block that contains the stack trace.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4cc9e-146">(*struct sem nome*)</span><span class="sxs-lookup"><span data-stu-id="4cc9e-146">(*unnamed struct*)</span></span>
</dt> <dd>

<span data-ttu-id="4cc9e-147">O membro dessa estrutura aninhada será válido somente se o membro **ExceptionForm** estiver definido como **texto de \_ \_ formulário de \_ exceção dedevido**.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-147">The member of this nested structure is valid only if the **ExceptionForm** member is set to **STOWED\_EXCEPTION\_FORM\_TEXT**.</span></span>

<dl> <dt>

<span data-ttu-id="4cc9e-148">**ErrorText**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-148">**ErrorText**</span></span>
</dt> <dd>

<span data-ttu-id="4cc9e-149">Tipo: **[ **PWSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-149">Type: **[**PWSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4cc9e-150">Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o texto de erro da exceção.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-150">A pointer to a null-terminated string that contains the error text of the exception.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4cc9e-151">**NestedExceptionType**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-151">**NestedExceptionType**</span></span>
</dt> <dd>

<span data-ttu-id="4cc9e-152">Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-152">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4cc9e-153">Um valor de 32 bits que especifica o tipo de objeto ao qual o membro **aninhaexception** aponta.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-153">A 32-bit value that specifies the type of object that the **NestedException** member points to.</span></span> <span data-ttu-id="4cc9e-154">Defina o valor com esta macro de definição de tipo de permuta de bytes que assume little-endian:</span><span class="sxs-lookup"><span data-stu-id="4cc9e-154">Define the value with this byte swap type-definition macro that assumes little-endian:</span></span>

``` syntax
#define STOWED_EXCEPTION_NESTED_TYPE(t) ((((((ULONG)(t)) >> 24) & 0xFF) <<  0) | \
                                         (((((ULONG)(t)) >> 16) & 0xFF) <<  8) | \
                                         (((((ULONG)(t)) >>  8) & 0xFF) << 16) | \
                                         (((((ULONG)(t)) >>  0) & 0xFF) << 24))
```

<span data-ttu-id="4cc9e-155">Aqui estão algumas definições de tipo comuns:</span><span class="sxs-lookup"><span data-stu-id="4cc9e-155">Here are some common type definitions:</span></span>



| <span data-ttu-id="4cc9e-156">Valor</span><span class="sxs-lookup"><span data-stu-id="4cc9e-156">Value</span></span>                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="4cc9e-157">Significado</span><span class="sxs-lookup"><span data-stu-id="4cc9e-157">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_NESTED_TYPE_NONE"></span><span id="stowed_exception_nested_type_none"></span><dl> <span data-ttu-id="4cc9e-158">Em <dt>**DEdevido \_ EXCEÇÃO \_ de \_ tipo \_ aninhado None**</dt> <dt>(0x00000000)</dt></span><span class="sxs-lookup"><span data-stu-id="4cc9e-158"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_NONE**</dt> <dt>(0x00000000)</dt></span></span> </dl>                                  | <span data-ttu-id="4cc9e-159">Esse valor especifica que não há nenhum objeto de exceção aninhado.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-159">This value specifies that there is no nested exception object.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_WIN32"></span><span id="stowed_exception_nested_type_win32"></span><dl> <span data-ttu-id="4cc9e-160">Em <dt>**DEdevido \_ EXCEÇÃO tipo \_ aninhado \_ \_**</dt> exceção <dt> \_ \_ \_ de tipo aninhado do Win32 (' W32E ')</dt></span><span class="sxs-lookup"><span data-stu-id="4cc9e-160"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_WIN32**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('W32E')</dt></span></span> </dl>    | <span data-ttu-id="4cc9e-161">Esse valor especifica que o membro **aninhaexception** aponta para um objeto de [**\_ registro de exceção**](/windows/desktop/api/winnt/ns-winnt-exception_record) .</span><span class="sxs-lookup"><span data-stu-id="4cc9e-161">This value specifies that the **NestedException** member points to an [**EXCEPTION\_RECORD**](/windows/desktop/api/winnt/ns-winnt-exception_record) object.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_STOWED"></span><span id="stowed_exception_nested_type_stowed"></span><dl> <span data-ttu-id="4cc9e-162">Em <dt>**DEdevido \_ \_ \_ \_ tipo ANINHAdo de exceção**</dt> o <dt> \_ \_ tipo aninhado de exceção dedevida \_ (' Coloque ')</dt></span><span class="sxs-lookup"><span data-stu-id="4cc9e-162"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_STOWED**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('STOW')</dt></span></span> </dl> | <span data-ttu-id="4cc9e-163">Esse valor especifica que o membro **aninhaexception** aponta para outro objeto de exceção dedevida.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-163">This value specifies that the **NestedException** member points to another stowed exception object.</span></span> <span data-ttu-id="4cc9e-164">O outro objeto de exceção envidado pode ser um objeto **v2 de \_ \_ informações \_ de exceção** devidada ou uma versão diferente com um membro de **cabeçalho** válido, ou seja, um membro de **cabeçalho** que contém um cabeçalho de [**\_ \_ informações \_ de exceção dedevida**](stowed-exception-information-header.md)válido.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-164">The other stowed exception object can be a **STOWED\_EXCEPTION\_INFORMATION\_V2** object or a different version with a valid **Header** member, that is, a **Header** member that contains a valid [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md).</span></span><br/> |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_CLR"></span><span id="stowed_exception_nested_type_clr"></span><dl> <span data-ttu-id="4cc9e-165">Em <dt>**DEdevido \_ EXCEÇÃO tipo aninhado \_ \_ \_ CLR**</dt> <dt> \_ \_ \_ (' CLR1 ')</dt></span><span class="sxs-lookup"><span data-stu-id="4cc9e-165"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_CLR**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('CLR1')</dt></span></span> </dl>          | <span data-ttu-id="4cc9e-166">Esse valor especifica que o membro **aninhaexception** aponta para um objeto de exceção ' CLR1 '.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-166">This value specifies that the **NestedException** member points to a 'CLR1' exception object.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_LEO"></span><span id="stowed_exception_nested_type_leo"></span><dl> <span data-ttu-id="4cc9e-167">Em <dt>**DEdevido \_ EXCEÇÃO tipo aninhado \_ \_ \_ Leo**</dt> <dt> \_ de exceptioned \_ \_ Type (' LEO1 ')</dt></span><span class="sxs-lookup"><span data-stu-id="4cc9e-167"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_LEO**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('LEO1')</dt></span></span> </dl>          | <span data-ttu-id="4cc9e-168">Esse valor especifica que o membro **aninhaexception** aponta para um objeto de exceção de idioma.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-168">This value specifies that the **NestedException** member points to a language exception object.</span></span><br/>                                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="4cc9e-169">**Aninhaexception**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-169">**NestedException**</span></span>
</dt> <dd>

<span data-ttu-id="4cc9e-170">Tipo: **[ **pVoid**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-170">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="4cc9e-171">Um ponteiro para um tipo de exceção aninhada.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-171">A pointer to a nested exception type.</span></span> <span data-ttu-id="4cc9e-172">O tipo de objeto é indicado pelo membro **NestedExceptionType** .</span><span class="sxs-lookup"><span data-stu-id="4cc9e-172">The type of object is indicated by the **NestedExceptionType** member.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4cc9e-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="4cc9e-173">Remarks</span></span>

<span data-ttu-id="4cc9e-174">Em **DEdevido \_ \_As informações \_ de exceção v2** e o [**cabeçalho de \_ \_ informações \_ de exceção dedevida**](stowed-exception-information-header.md) não são definidas atualmente em um cabeçalho disponível publicamente, portanto, você precisa defini-las no código-fonte antes de usá-las.</span><span class="sxs-lookup"><span data-stu-id="4cc9e-174">**STOWED\_EXCEPTION\_INFORMATION\_V2** and [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md) currently aren't defined in a header that is publicly available so you need to define them in your source code before you use them.</span></span>

<span data-ttu-id="4cc9e-175">A estrutura de informações de exceção devidada **\_ \_ \_ v1** é idêntica a essa estrutura, exceto que ela não contém os membros **NestedExceptionType** e **aninhaexception** .</span><span class="sxs-lookup"><span data-stu-id="4cc9e-175">The **STOWED\_EXCEPTION\_INFORMATION\_V1** structure is identical to this structure except it doesn't contain the **NestedExceptionType** and **NestedException** members.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cc9e-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cc9e-176">Requirements</span></span>



| <span data-ttu-id="4cc9e-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cc9e-177">Requirement</span></span> | <span data-ttu-id="4cc9e-178">Valor</span><span class="sxs-lookup"><span data-stu-id="4cc9e-178">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4cc9e-179">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cc9e-179">Minimum supported client</span></span><br/> | <span data-ttu-id="4cc9e-180">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4cc9e-180">Windows 8.1 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4cc9e-181">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cc9e-181">Minimum supported server</span></span><br/> | <span data-ttu-id="4cc9e-182">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="4cc9e-182">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="4cc9e-183">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4cc9e-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cc9e-184"><dt>Nenhuma</dt></span><span class="sxs-lookup"><span data-stu-id="4cc9e-184"><dt>None</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cc9e-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="4cc9e-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc9e-186">**registro de exceção \_**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-186">**EXCEPTION\_RECORD**</span></span>](/windows/desktop/api/winnt/ns-winnt-exception_record)
</dt> <dt>

[<span data-ttu-id="4cc9e-187">**cabeçalho de \_ informações de exceção DEdevida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4cc9e-187">**STOWED\_EXCEPTION\_INFORMATION\_HEADER**</span></span>](stowed-exception-information-header.md)
</dt> </dl>

 

