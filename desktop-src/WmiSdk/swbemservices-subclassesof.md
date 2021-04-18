---
description: Retorna um objeto SWbemObjectSet.
ms.assetid: cfe08956-7215-4e2e-a279-6e86f14e5c27
ms.tgt_platform: multiple
title: Método SWbemServices. SubclassesOf (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOf
- ISWbemServices.SubclassesOf
- ISWbemServices.SubclassesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e8c23dee5ee3f0a1cf5babe37d0ccb6aa0a3ac7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763112"
---
# <a name="swbemservicessubclassesof-method"></a><span data-ttu-id="81735-103">Método SWbemServices. SubclassesOf</span><span class="sxs-lookup"><span data-stu-id="81735-103">SWbemServices.SubclassesOf method</span></span>

<span data-ttu-id="81735-104">O método **SubclassesOf** do objeto [**SWbemServices**](swbemservices.md) retorna um objeto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="81735-104">The **SubclassesOf** method of the [**SWbemServices**](swbemservices.md) object returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="81735-105">Esse objeto é uma coleção de subclasses de uma classe especificada.</span><span class="sxs-lookup"><span data-stu-id="81735-105">This object is a collection of subclasses of a specified class.</span></span> <span data-ttu-id="81735-106">Os itens na coleção retornada podem ser obtidos usando métodos de coleta padrão.</span><span class="sxs-lookup"><span data-stu-id="81735-106">Items in the returned collection can be obtained using standard collection methods.</span></span> <span data-ttu-id="81735-107">Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="81735-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="81735-108">Esse método funciona apenas para objetos de classe.</span><span class="sxs-lookup"><span data-stu-id="81735-108">This method only works for class objects.</span></span>

<span data-ttu-id="81735-109">O método é chamado no modo semisynchronous.</span><span class="sxs-lookup"><span data-stu-id="81735-109">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="81735-110">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="81735-110">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="81735-111">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="81735-111">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="81735-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81735-112">Syntax</span></span>


```VB
objWbemObjectSet = .SubclassesOf( _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="81735-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81735-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81735-114">*strSuperclass* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="81735-114">*strSuperclass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="81735-115">Especifica um nome de classe pai.</span><span class="sxs-lookup"><span data-stu-id="81735-115">Specifies a parent class name.</span></span> <span data-ttu-id="81735-116">Somente as subclasses dessa classe retornam no enumerador.</span><span class="sxs-lookup"><span data-stu-id="81735-116">Only subclasses of this class return in the enumerator.</span></span> <span data-ttu-id="81735-117">Se você deixar esse parâmetro em branco e, se *iFlags* for **wbemQueryFlagShallow**, somente as classes de nível superior serão retornadas (ou seja, classes que não têm nenhuma classe pai).</span><span class="sxs-lookup"><span data-stu-id="81735-117">If you leave this parameter blank, and if *iFlags* is **wbemQueryFlagShallow**, only the top-level classes are returned (that is, classes that have no parent class).</span></span> <span data-ttu-id="81735-118">Se esse parâmetro estiver em branco e *iFlags* for **wbemQueryFlagDeep** , todas as classes no namespace serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="81735-118">If this parameter is blank and *iFlags* is **wbemQueryFlagDeep** all classes within the namespace are returned.</span></span>

</dd> <dt>

<span data-ttu-id="81735-119">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="81735-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="81735-120">Determina o quão detalhado a chamada enumera.</span><span class="sxs-lookup"><span data-stu-id="81735-120">Determines how detailed the call enumerates.</span></span> <span data-ttu-id="81735-121">Os valores padrão para esse parâmetro são **wbemFlagReturnImmediately** e **wbemQueryFlagDeep**.</span><span class="sxs-lookup"><span data-stu-id="81735-121">The default values for this parameter are **wbemFlagReturnImmediately** and **wbemQueryFlagDeep**.</span></span> <span data-ttu-id="81735-122">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="81735-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="81735-123"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="81735-123"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="81735-124">Força a enumeração a incluir apenas subclasses imediatas da classe pai especificada.</span><span class="sxs-lookup"><span data-stu-id="81735-124">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="81735-125"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="81735-125"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="81735-126">Padrão para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="81735-126">Default for this parameter.</span></span> <span data-ttu-id="81735-127">Esse valor força a enumeração recursiva em todas as subclasses derivadas da classe pai especificada.</span><span class="sxs-lookup"><span data-stu-id="81735-127">This value forces recursive enumeration into all subclasses that are derived from the specified parent class.</span></span> <span data-ttu-id="81735-128">A classe pai não é retornada na enumeração.</span><span class="sxs-lookup"><span data-stu-id="81735-128">The parent class is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="81735-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="81735-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="81735-130">Faz com que a chamada retorne imediatamente.</span><span class="sxs-lookup"><span data-stu-id="81735-130">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="81735-131"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="81735-131"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="81735-132">Faz com que essa chamada seja bloqueada até que a chamada seja concluída.</span><span class="sxs-lookup"><span data-stu-id="81735-132">Causes this call to block until the call has completed.</span></span> <span data-ttu-id="81735-133">Esse sinalizador chama o método no modo síncrono.</span><span class="sxs-lookup"><span data-stu-id="81735-133">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="81735-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="81735-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="81735-135">Faz com que o WMI retorne dados de alteração de classe com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="81735-135">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="81735-136">Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="81735-136">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="81735-137">*objWbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="81735-137">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="81735-138">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="81735-138">Typically, this is undefined.</span></span> <span data-ttu-id="81735-139">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="81735-139">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider servicing the request.</span></span> <span data-ttu-id="81735-140">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="81735-140">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81735-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81735-141">Return value</span></span>

<span data-ttu-id="81735-142">Se o método for bem-sucedido, um objeto [**SWbemObjectSet**](swbemobjectset.md) será retornado.</span><span class="sxs-lookup"><span data-stu-id="81735-142">If the method is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="81735-143">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="81735-143">Error codes</span></span>

<span data-ttu-id="81735-144">Após a conclusão do método **SubclassesOf** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="81735-144">After the completion of the **SubclassesOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="81735-145">Uma coleção retornada com zero elementos não é um erro.</span><span class="sxs-lookup"><span data-stu-id="81735-145">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="81735-146">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="81735-146">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="81735-147">O usuário atual não tem permissão para exibir uma ou mais das classes retornadas pela chamada.</span><span class="sxs-lookup"><span data-stu-id="81735-147">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="81735-148">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="81735-148">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="81735-149">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="81735-149">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="81735-150">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="81735-150">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="81735-151">A classe especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="81735-151">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="81735-152">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="81735-152">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="81735-153">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="81735-153">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="81735-154">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="81735-154">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="81735-155">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="81735-155">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="81735-156">Exemplos</span><span class="sxs-lookup"><span data-stu-id="81735-156">Examples</span></span>

<span data-ttu-id="81735-157">O exemplo do PowerShell a seguir mostra como recuperar as subclasses de uma classe em um sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="81735-157">The following PowerShell sample shows how to retrieve the subclasses of a class on a remote system.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="81735-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81735-158">Requirements</span></span>



| <span data-ttu-id="81735-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="81735-159">Requirement</span></span> | <span data-ttu-id="81735-160">Valor</span><span class="sxs-lookup"><span data-stu-id="81735-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81735-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81735-161">Minimum supported client</span></span><br/> | <span data-ttu-id="81735-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81735-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81735-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81735-163">Minimum supported server</span></span><br/> | <span data-ttu-id="81735-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81735-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81735-165">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81735-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="81735-166"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="81735-166"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="81735-167">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="81735-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="81735-168"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="81735-168"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="81735-169">DLL</span><span class="sxs-lookup"><span data-stu-id="81735-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81735-170"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81735-170"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="81735-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="81735-171">CLSID</span></span><br/>                    | <span data-ttu-id="81735-172">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="81735-172">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="81735-173">IID</span><span class="sxs-lookup"><span data-stu-id="81735-173">IID</span></span><br/>                      | <span data-ttu-id="81735-174">ISWbemServices de IID \_</span><span class="sxs-lookup"><span data-stu-id="81735-174">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="81735-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="81735-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81735-176">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="81735-176">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="81735-177">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="81735-177">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




