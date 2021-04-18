---
description: Atualiza os dados para objetos que têm dados fornecidos por um provedor de desempenho, como as classes de contador de desempenho. Você pode obter dados atualizados mais rapidamente e sem uma chamada para SWbemServices. get \_ .
ms.assetid: 6aeaa336-fb98-4eda-b746-fc958198d8ae
ms.tgt_platform: multiple
title: Método de SWbemObjectEx.Refresh_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 904e2b7f9b256596555c8396a699220108d4f37b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771304"
---
# <a name="swbemobjectexrefresh_-method"></a><span data-ttu-id="f526a-104">Método SWbemObjectEx. Refresh \_</span><span class="sxs-lookup"><span data-stu-id="f526a-104">SWbemObjectEx.Refresh\_ method</span></span>

<span data-ttu-id="f526a-105">O **método \_ Refresh** de [**SWbemObjectEx**](swbemobjectex.md) atualiza os dados de objetos que têm dados fornecidos por um provedor de desempenho, como as [classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span><span class="sxs-lookup"><span data-stu-id="f526a-105">The **Refresh\_** method of [**SWbemObjectEx**](swbemobjectex.md) updates the data for objects that have data supplied by a performance provider, such as the [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="f526a-106">Você pode obter dados atualizados mais rapidamente e sem uma chamada para [**SWbemServices. get \_**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="f526a-106">You can obtain updated data more quickly and without a call to [**SWbemServices.Get\_**](swbemservices-get.md).</span></span>

<span data-ttu-id="f526a-107">Para obter mais informações sobre essa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f526a-107">For more information about this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f526a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f526a-108">Syntax</span></span>


```VB
SWbemObjectEx.Refresh_( _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f526a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f526a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f526a-110">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f526a-110">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f526a-111">Sinalizadores de operação reservados que, se especificados, devem ser 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="f526a-111">Reserved operation flags which, if specified, must be 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="f526a-112">*objWbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f526a-112">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f526a-113">Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que define o contexto para a operação.</span><span class="sxs-lookup"><span data-stu-id="f526a-113">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that sets context for the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f526a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f526a-114">Return value</span></span>

<span data-ttu-id="f526a-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f526a-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f526a-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f526a-116">Error codes</span></span>

<span data-ttu-id="f526a-117">Após a conclusão do **método \_ Refresh** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="f526a-117">After completion of the **Refresh\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="f526a-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="f526a-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f526a-119">O provedor falhou internamente, embora a operação fosse válida.</span><span class="sxs-lookup"><span data-stu-id="f526a-119">The provider failed internally, even though the operation was valid.</span></span>

</dd> <dt>

<span data-ttu-id="f526a-120">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="f526a-120">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="f526a-121">O formato solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="f526a-121">The requested format was not found.</span></span>

</dd> <dt>

<span data-ttu-id="f526a-122">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="f526a-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="f526a-123">Um dos parâmetros para a chamada não está correto.</span><span class="sxs-lookup"><span data-stu-id="f526a-123">One of the parameters to the call is not correct.</span></span>

</dd> <dt>

<span data-ttu-id="f526a-124">**wbemErrRefresherBusy** -2147749975 (0x80041057)</span><span class="sxs-lookup"><span data-stu-id="f526a-124">**wbemErrRefresherBusy** - 2147749975 (0x80041057)</span></span>
</dt> <dd>

<span data-ttu-id="f526a-125">O atualizador está ocupado com outra operação.</span><span class="sxs-lookup"><span data-stu-id="f526a-125">The refresher is busy with another operation.</span></span>

</dd> <dt>

<span data-ttu-id="f526a-126">**wbemPartialResults** -2147745808 (0x80040010)</span><span class="sxs-lookup"><span data-stu-id="f526a-126">**wbemPartialResults** - 2147745808 (0x80040010)</span></span>
</dt> <dd>

<span data-ttu-id="f526a-127">Nem todos os objetos, enumeradores ou atualizadores aninhados foram atualizados com êxito.</span><span class="sxs-lookup"><span data-stu-id="f526a-127">Not all of the objects, enumerators, or nested refreshers were successfully updated.</span></span> <span data-ttu-id="f526a-128">Esse retorno não é um erro, mas uma indicação de que a operação estava incompleta.</span><span class="sxs-lookup"><span data-stu-id="f526a-128">This return is not an error but an indication that the operation was incomplete.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f526a-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f526a-129">Examples</span></span>

<span data-ttu-id="f526a-130">O exemplo de código de script a seguir mostra como obter contadores de desempenho brutos e cooked para o processo do sistema.</span><span class="sxs-lookup"><span data-stu-id="f526a-130">The following script code example shows how to obtain both raw and cooked performance counters for the system process.</span></span> <span data-ttu-id="f526a-131">Os objetos são atualizados a cada dois segundos e as propriedades são exibidas.</span><span class="sxs-lookup"><span data-stu-id="f526a-131">The objects are refreshed every two seconds and the properties displayed.</span></span>


```VB
' Get the performance counter instance for the System process
set PerfRaw = GetObject( _
    "winmgmts:win32_perfrawdata_perfproc_process.name='system'")
set PerfCooked = GetObject( _
    "winmgmts:win32_perfformatteddata_perfproc_process.name='system'")

' Display some properties in a loop
for I = 1 to 5
    Wscript.Echo "HandleCount = "& PerfRaw.HandleCount & _
         " Raw ThreadCount = " & PerfRaw.ThreadCount & _
        " Cooked ThreadCount = " & PerfCooked.ThreadCount
    
    Wscript.Sleep 2000
    
' Refresh the objects
    PerfRaw.Refresh_
    PerfCooked.Refresh_
next
```



## <a name="requirements"></a><span data-ttu-id="f526a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f526a-132">Requirements</span></span>



| <span data-ttu-id="f526a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f526a-133">Requirement</span></span> | <span data-ttu-id="f526a-134">Valor</span><span class="sxs-lookup"><span data-stu-id="f526a-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f526a-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f526a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f526a-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f526a-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f526a-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f526a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f526a-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f526a-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f526a-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f526a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="f526a-140"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f526a-140"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f526a-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f526a-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="f526a-142"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f526a-142"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f526a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f526a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f526a-144"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f526a-144"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f526a-145">CLSID</span><span class="sxs-lookup"><span data-stu-id="f526a-145">CLSID</span></span><br/>                    | <span data-ttu-id="f526a-146">\_SWBEMOBJECTEX CLSID</span><span class="sxs-lookup"><span data-stu-id="f526a-146">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="f526a-147">IID</span><span class="sxs-lookup"><span data-stu-id="f526a-147">IID</span></span><br/>                      | <span data-ttu-id="f526a-148">ISWbemObjectEx de IID \_</span><span class="sxs-lookup"><span data-stu-id="f526a-148">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="f526a-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="f526a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f526a-150">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="f526a-150">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="f526a-151">Monitorando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="f526a-151">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

