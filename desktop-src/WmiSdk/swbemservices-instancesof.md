---
description: Cria um enumerador que retorna as instâncias de uma classe especificada de acordo com os critérios de seleção especificados pelo usuário.
ms.assetid: 6465a981-f98e-4ece-a9b6-9da8ae618bc6
ms.tgt_platform: multiple
title: Método SWbemServices. InstancesOf (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOf
- ISWbemServices.InstancesOf
- ISWbemServices.InstancesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2386b52160b1e2a08c5a345b67922ed24afc44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837165"
---
# <a name="swbemservicesinstancesof-method"></a><span data-ttu-id="47076-103">Método SWbemServices. InstancesOf</span><span class="sxs-lookup"><span data-stu-id="47076-103">SWbemServices.InstancesOf method</span></span>

<span data-ttu-id="47076-104">O método **InstancesOf** do objeto [**SWbemServices**](swbemservices.md) cria um enumerador que retorna as instâncias de uma classe especificada de acordo com os critérios de seleção especificados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="47076-104">The **InstancesOf** method of the [**SWbemServices**](swbemservices.md) object creates an enumerator that returns the instances of a specified class according to the user-specified selection criteria.</span></span> <span data-ttu-id="47076-105">Esse método implementa uma consulta simples.</span><span class="sxs-lookup"><span data-stu-id="47076-105">This method implements a simple query.</span></span> <span data-ttu-id="47076-106">Consultas mais complexas podem exigir o uso de [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="47076-106">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="47076-107">O método é chamado no modo semisynchronous.</span><span class="sxs-lookup"><span data-stu-id="47076-107">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="47076-108">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="47076-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="47076-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="47076-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="47076-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47076-110">Syntax</span></span>


```VB
objWbemObjectSet = .InstancesOf( _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="47076-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47076-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47076-112">*strClass*</span><span class="sxs-lookup"><span data-stu-id="47076-112">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="47076-113">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="47076-113">Required.</span></span> <span data-ttu-id="47076-114">Cadeia de caracteres que contém o nome da classe para a qual as instâncias são desejadas.</span><span class="sxs-lookup"><span data-stu-id="47076-114">String that contains the name of the class for which instances are desired.</span></span> <span data-ttu-id="47076-115">Este parâmetro não pode ficar em branco.</span><span class="sxs-lookup"><span data-stu-id="47076-115">This parameter cannot be blank.</span></span>

</dd> <dt>

<span data-ttu-id="47076-116">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="47076-116">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="47076-117">Esse parâmetro determina o quão detalhado a chamada enumera e se essa chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="47076-117">This parameter determines how detailed the call enumerates and if this call returns immediately.</span></span> <span data-ttu-id="47076-118">O valor padrão para esse parâmetro é **wbemFlagReturnImmediately**.</span><span class="sxs-lookup"><span data-stu-id="47076-118">The default value for this parameter is **wbemFlagReturnImmediately**.</span></span> <span data-ttu-id="47076-119">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="47076-119">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="47076-120"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="47076-120"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="47076-121">Faz com que um enumerador somente de encaminhamento seja retornado.</span><span class="sxs-lookup"><span data-stu-id="47076-121">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="47076-122">Enumeradores de somente encaminhamento são geralmente muito mais rápidos e usam menos memória do que enumeradores convencionais, mas não permitem chamadas para [**SWbemObject. \_ clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="47076-122">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="47076-123"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="47076-123"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="47076-124">Faz com que o WMI retenha ponteiros para objetos da enumeração até que o cliente libere o enumerador.</span><span class="sxs-lookup"><span data-stu-id="47076-124">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="47076-125"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="47076-125"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="47076-126">Valor padrão para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="47076-126">Default value for this parameter.</span></span> <span data-ttu-id="47076-127">Esse sinalizador faz com que a chamada retorne imediatamente.</span><span class="sxs-lookup"><span data-stu-id="47076-127">This flag causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="47076-128"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="47076-128"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="47076-129">Faz com que essa chamada seja bloqueada até que a consulta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="47076-129">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="47076-130">Esse sinalizador chama o método no modo síncrono.</span><span class="sxs-lookup"><span data-stu-id="47076-130">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="47076-131"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="47076-131"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="47076-132">Força a enumeração a incluir apenas subclasses imediatas da classe pai especificada.</span><span class="sxs-lookup"><span data-stu-id="47076-132">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="47076-133"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="47076-133"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="47076-134">Valor padrão para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="47076-134">Default value for this parameter.</span></span> <span data-ttu-id="47076-135">Esse valor força a enumeração a incluir todas as classes na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="47076-135">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="47076-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="47076-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="47076-137">Faz com que o WMI retorne dados de alteração de classe com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="47076-137">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="47076-138">Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="47076-138">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="47076-139">*objWbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="47076-139">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="47076-140">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="47076-140">Typically, this is undefined.</span></span> <span data-ttu-id="47076-141">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="47076-141">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="47076-142">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="47076-142">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47076-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47076-143">Return value</span></span>

<span data-ttu-id="47076-144">Se for bem-sucedido, o método retornará um [**SWbemObjectSet**](swbemobjectset.md).</span><span class="sxs-lookup"><span data-stu-id="47076-144">If successful, the method returns an [**SWbemObjectSet**](swbemobjectset.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="47076-145">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="47076-145">Error codes</span></span>

<span data-ttu-id="47076-146">Após a conclusão do método **InstancesOf** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="47076-146">Upon the completion of the **InstancesOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="47076-147">Um enumerador retornado com zero elementos não é um erro.</span><span class="sxs-lookup"><span data-stu-id="47076-147">A returned enumerator with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="47076-148">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="47076-148">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="47076-149">O usuário atual não tem permissão para exibir instâncias da classe especificada.</span><span class="sxs-lookup"><span data-stu-id="47076-149">Current user does not have the permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="47076-150">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="47076-150">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="47076-151">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="47076-151">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="47076-152">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="47076-152">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="47076-153">A classe especificada não é válida.</span><span class="sxs-lookup"><span data-stu-id="47076-153">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="47076-154">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="47076-154">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="47076-155">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="47076-155">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="47076-156">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="47076-156">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="47076-157">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="47076-157">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47076-158">Comentários</span><span class="sxs-lookup"><span data-stu-id="47076-158">Remarks</span></span>

<span data-ttu-id="47076-159">O método **InstancesOf** só funciona para objetos de classe.</span><span class="sxs-lookup"><span data-stu-id="47076-159">The **InstancesOf** method only works for class objects.</span></span>

<span data-ttu-id="47076-160">Por padrão, o InstancesOf executa uma recuperação profunda.</span><span class="sxs-lookup"><span data-stu-id="47076-160">By default, InstancesOf performs a deep retrieval.</span></span> <span data-ttu-id="47076-161">Ou seja, InstancesOf recupera todas as instâncias do recurso gerenciado que você identifica e todas as instâncias de todas as subclasses definidas abaixo da classe de destino.</span><span class="sxs-lookup"><span data-stu-id="47076-161">That is, InstancesOf retrieves all instances of the managed resource you identify and all instances of all the subclasses defined beneath the target class.</span></span> <span data-ttu-id="47076-162">Por exemplo, o script a seguir recupera todos os recursos modelados por todas as classes dinâmicas definidas sob a \_ classe abstrata do serviço CIM.</span><span class="sxs-lookup"><span data-stu-id="47076-162">For example, the following script retrieves all of the resources modeled by all of the dynamic classes defined beneath the CIM\_Service abstract class.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("CIM_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Object Path: " & objSWbemObject.Path_.Path
Next
```



<span data-ttu-id="47076-163">Se você executar esse script, obterá informações de volta.</span><span class="sxs-lookup"><span data-stu-id="47076-163">If you run this script, you will get information back.</span></span> <span data-ttu-id="47076-164">No entanto, essas informações não serão limitadas aos serviços instalados em um computador.</span><span class="sxs-lookup"><span data-stu-id="47076-164">However, this information will not be limited to the services installed on a computer.</span></span> <span data-ttu-id="47076-165">Em vez disso, ele incluirá informações de todas as classes filhas do [**\_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service), incluindo [**Win32 \_ SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) e [**Win32 \_ ApplicationService**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="47076-165">Instead, it will include information from all child classes of [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), including [**Win32\_SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver) and [**Win32\_ApplicationService**](/previous-versions/windows/desktop/legacy/aa394068(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="47076-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47076-166">Requirements</span></span>



| <span data-ttu-id="47076-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="47076-167">Requirement</span></span> | <span data-ttu-id="47076-168">Valor</span><span class="sxs-lookup"><span data-stu-id="47076-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47076-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47076-169">Minimum supported client</span></span><br/> | <span data-ttu-id="47076-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47076-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="47076-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47076-171">Minimum supported server</span></span><br/> | <span data-ttu-id="47076-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47076-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="47076-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47076-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="47076-174"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="47076-174"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="47076-175">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="47076-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="47076-176"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="47076-176"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="47076-177">DLL</span><span class="sxs-lookup"><span data-stu-id="47076-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47076-178"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47076-178"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="47076-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="47076-179">CLSID</span></span><br/>                    | <span data-ttu-id="47076-180">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="47076-180">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="47076-181">IID</span><span class="sxs-lookup"><span data-stu-id="47076-181">IID</span></span><br/>                      | <span data-ttu-id="47076-182">ISWbemServices de IID \_</span><span class="sxs-lookup"><span data-stu-id="47076-182">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="47076-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="47076-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47076-184">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="47076-184">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="47076-185">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="47076-185">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

