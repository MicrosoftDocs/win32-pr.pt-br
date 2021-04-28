---
description: SWbemServices.Exemétodo cQuery – executa uma consulta para recuperar objetos.
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cQuery (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQuery
- ISWbemServices.ExecQuery
- ISWbemServices.ExecQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3009d2dc88e9987a3559da91eed1aa5aa1b248f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098325"
---
# <a name="swbemservicesexecquery-method"></a><span data-ttu-id="6f206-103">SWbemServices.Exemétodo cQuery</span><span class="sxs-lookup"><span data-stu-id="6f206-103">SWbemServices.ExecQuery method</span></span>

<span data-ttu-id="6f206-104">O método **ExecQuery** do objeto [**SWbemServices**](swbemservices.md) executa uma consulta para recuperar objetos.</span><span class="sxs-lookup"><span data-stu-id="6f206-104">The **ExecQuery** method of the [**SWbemServices**](swbemservices.md) object executes a query to retrieve objects.</span></span> <span data-ttu-id="6f206-105">Esses objetos estão disponíveis por meio da coleção [**SWbemObjectSet**](swbemobjectset.md) retornada.</span><span class="sxs-lookup"><span data-stu-id="6f206-105">These objects are available through the returned [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span>

<span data-ttu-id="6f206-106">Esse método é chamado no modo semisynchronous.</span><span class="sxs-lookup"><span data-stu-id="6f206-106">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="6f206-107">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="6f206-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="6f206-108">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6f206-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f206-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f206-109">Syntax</span></span>


```VB
objWbemObjectSet = .ExecQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6f206-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f206-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f206-111">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="6f206-111">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="6f206-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="6f206-112">Required.</span></span> <span data-ttu-id="6f206-113">Cadeia de caracteres que contém o texto da consulta.</span><span class="sxs-lookup"><span data-stu-id="6f206-113">String that contains the text of the query.</span></span> <span data-ttu-id="6f206-114">Este parâmetro não pode ficar em branco.</span><span class="sxs-lookup"><span data-stu-id="6f206-114">This parameter cannot be blank.</span></span> <span data-ttu-id="6f206-115">Para obter mais informações sobre como criar cadeias de caracteres de consulta do WMI, consulte [consultando com WQL](querying-with-wql.md) e a referência [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="6f206-115">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="6f206-116">*strQueryLanguage* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="6f206-116">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f206-117">Cadeia de caracteres que contém a linguagem de consulta a ser usada.</span><span class="sxs-lookup"><span data-stu-id="6f206-117">String that contains the query language to be used.</span></span> <span data-ttu-id="6f206-118">Se especificado, esse valor deve ser "WQL".</span><span class="sxs-lookup"><span data-stu-id="6f206-118">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="6f206-119">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="6f206-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f206-120">Inteiro que determina o comportamento da consulta e determina se essa chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="6f206-120">Integer that determines the behavior of the query and determines whether this call returns immediately.</span></span> <span data-ttu-id="6f206-121">O valor padrão para esse parâmetro é **wbemFlagReturnImmediately**.</span><span class="sxs-lookup"><span data-stu-id="6f206-121">The default value for this parameter is **wbemFlagReturnImmediately**.</span></span> <span data-ttu-id="6f206-122">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6f206-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="6f206-123"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="6f206-123"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="6f206-124">Faz com que um enumerador somente de encaminhamento seja retornado.</span><span class="sxs-lookup"><span data-stu-id="6f206-124">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="6f206-125">Enumeradores de somente encaminhamento são geralmente muito mais rápidos e usam menos memória do que enumeradores convencionais, mas não permitem chamadas para [**SWbemObject. \_ clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="6f206-125">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="6f206-126"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="6f206-126"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="6f206-127">Faz com que o WMI retenha ponteiros para objetos da enumeração até que o cliente libere o enumerador.</span><span class="sxs-lookup"><span data-stu-id="6f206-127">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="6f206-128"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="6f206-128"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="6f206-129">Faz com que a chamada retorne imediatamente.</span><span class="sxs-lookup"><span data-stu-id="6f206-129">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="6f206-130"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="6f206-130"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="6f206-131">Faz com que essa chamada seja bloqueada até que a consulta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="6f206-131">Causes this call to block until the query is complete.</span></span> <span data-ttu-id="6f206-132">Esse sinalizador chama o método no modo síncrono.</span><span class="sxs-lookup"><span data-stu-id="6f206-132">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span data-ttu-id="6f206-133"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="6f206-133"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>\*\*\*\*wbemQueryFlagPrototype\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="6f206-134">Usado para protótipos.</span><span class="sxs-lookup"><span data-stu-id="6f206-134">Used for prototyping.</span></span> <span data-ttu-id="6f206-135">Esse sinalizador impede que a consulta ocorra e retorna um objeto parecido com um objeto de resultado típico.</span><span class="sxs-lookup"><span data-stu-id="6f206-135">This flag stops the query from happening and returns an object that looks like a typical result object.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="6f206-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="6f206-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="6f206-137">Faz com que o WMI retorne dados de alteração de classe com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="6f206-137">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="6f206-138">Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="6f206-138">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6f206-139">*objWbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="6f206-139">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f206-140">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="6f206-140">Typically, this is undefined.</span></span> <span data-ttu-id="6f206-141">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="6f206-141">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="6f206-142">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="6f206-142">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f206-143">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6f206-143">Return value</span></span>

<span data-ttu-id="6f206-144">Se nenhum erro ocorrer, esse método retornará um objeto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="6f206-144">If no error occurs, this method returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="6f206-145">Esta é uma coleção de objetos que contém o conjunto de resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="6f206-145">This is an object collection that contains the result set of the query.</span></span> <span data-ttu-id="6f206-146">O chamador pode examinar a coleção usando a implementação de coleções para a linguagem de programação que você está usando.</span><span class="sxs-lookup"><span data-stu-id="6f206-146">The caller can examine the collection using the implementation of collections for the programming language you are using.</span></span> <span data-ttu-id="6f206-147">Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="6f206-147">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="6f206-148">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6f206-148">Error codes</span></span>

<span data-ttu-id="6f206-149">Após a conclusão do método **ExecQuery** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="6f206-149">After the completion of the **ExecQuery** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object can contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="6f206-150">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="6f206-150">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="6f206-151">O usuário atual não tem permissão para exibir o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="6f206-151">Current user does not have the permission to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="6f206-152">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="6f206-152">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="6f206-153">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="6f206-153">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="6f206-154">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="6f206-154">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="6f206-155">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="6f206-155">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="6f206-156">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="6f206-156">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="6f206-157">Sintaxe de consulta inválida.</span><span class="sxs-lookup"><span data-stu-id="6f206-157">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6f206-158">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="6f206-158">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="6f206-159">Não há suporte para a linguagem de consulta solicitada.</span><span class="sxs-lookup"><span data-stu-id="6f206-159">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6f206-160">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="6f206-160">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="6f206-161">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="6f206-161">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f206-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f206-162">Remarks</span></span>

<span data-ttu-id="6f206-163">**ExecQuery** é uma das chamadas mais comumente usadas para recuperar informações de WMI.</span><span class="sxs-lookup"><span data-stu-id="6f206-163">**ExecQuery** is one of the most commonly-used calls to retrieve WMI information.</span></span> <span data-ttu-id="6f206-164">Uma chamada padrão para **ExecQuery** é semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="6f206-164">A standard call to **ExecQuery** looks like the following:</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```



<span data-ttu-id="6f206-165">Observe que você cria o objeto [**SWbemServices**](swbemservices.md) com um moniker que representa o namespace e a segurança apropriados e, em seguida, faz a chamada de **ExecQuery** através do serviço.</span><span class="sxs-lookup"><span data-stu-id="6f206-165">Note that you create the [**SWbemServices**](swbemservices.md) object with a moniker that represents the appropriate namespace and security, then make the **ExecQuery** call through the service.</span></span> <span data-ttu-id="6f206-166">Para obter uma discussão mais completa, consulte [criando um script WMI](creating-a-wmi-script.md) e [enumerando o WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6f206-166">For a more complete discussion, see [Creating a WMI Script](creating-a-wmi-script.md) and [Enumerating WMI](enumerating-wmi.md).</span></span>

<span data-ttu-id="6f206-167">Como o método [**InstancesOf**](swbemservices-instancesof.md) , o método **ExecQuery** sempre retorna uma coleção [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="6f206-167">Like the [**InstancesOf**](swbemservices-instancesof.md) method, the **ExecQuery** method always returns an [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span> <span data-ttu-id="6f206-168">Portanto, o script WMI deve enumerar os retornos de ExecQuery da coleção para acessar cada instância de recurso gerenciado na coleção, como mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="6f206-168">Thus your WMI script must enumerate the collection ExecQuery returns in order to access each managed resource instance in the collection, as shown here:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="6f206-169">Outros métodos [**SWbemServices**](swbemservices.md) que retornam [**um SWbemObjectSet**](swbemobjectset.md) incluem [**AssociatorsOf**](swbemservices-associatorsof.md), [**References**](swbemservices-referencesto.md)e [**SubclassesOf**](swbemservices-subclassesof.md).</span><span class="sxs-lookup"><span data-stu-id="6f206-169">Other [**SWbemServices**](swbemservices.md) methods that return an [**SWbemObjectSet**](swbemobjectset.md) include [**AssociatorsOf**](swbemservices-associatorsof.md), [**ReferencesTo**](swbemservices-referencesto.md), and [**SubclassesOf**](swbemservices-subclassesof.md).</span></span>

<span data-ttu-id="6f206-170">Não é um erro para a consulta retornar um conjunto de resultados vazio.</span><span class="sxs-lookup"><span data-stu-id="6f206-170">It is not an error for the query to return an empty result set.</span></span> <span data-ttu-id="6f206-171">O método **ExecQuery** retorna propriedades de chave, independentemente de a propriedade de chave ser solicitada ou não no argumento *strQuery* .</span><span class="sxs-lookup"><span data-stu-id="6f206-171">The **ExecQuery** method returns key properties whether or not the key property is requested in the *strQuery* argument.</span></span> <span data-ttu-id="6f206-172">Se ocorrer um erro ao executar esse método e você não usar o sinalizador **wbemFlagReturnImmediately** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) não será definido até que você tente acessar o conjunto de objetos retornado.</span><span class="sxs-lookup"><span data-stu-id="6f206-172">If an error occurs when executing this method and you do not use the **wbemFlagReturnImmediately** flag, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object is not set until you attempt to access the returned object set.</span></span> <span data-ttu-id="6f206-173">No entanto, se você usar o sinalizador **wbemFlagReturnWhenComplete** , o objeto Err será definido quando o método **ExecQuery** for chamado.</span><span class="sxs-lookup"><span data-stu-id="6f206-173">However, if you use the **wbemFlagReturnWhenComplete** flag, the Err object is set when the **ExecQuery** method is called.</span></span>

<span data-ttu-id="6f206-174">Há limites para o número de palavras-chave **and** e **or** que podem ser usadas em consultas WQL.</span><span class="sxs-lookup"><span data-stu-id="6f206-174">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="6f206-175">Grandes números de palavras-chave WQL que são usadas em uma consulta complexa podem fazer com que o WMI retorne o código de erro de **\_ \_ \_ violação E de cota de WBEM** como um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6f206-175">Large numbers of WQL keywords that are used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="6f206-176">O limite de palavras-chave WQL depende da complexidade da consulta.</span><span class="sxs-lookup"><span data-stu-id="6f206-176">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="6f206-177">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6f206-177">Examples</span></span>

<span data-ttu-id="6f206-178">O exemplo de código VBScript a seguir localiza todas as unidades de disco no computador local e exibe a ID do dispositivo e o tipo da unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="6f206-178">The following VBScript code example locates all the disk drives on the local computer and displays the device ID and the type of the disk drive.</span></span>


```VB
Set colDisks = GetObject( _
    "Winmgmts:").ExecQuery("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
 
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo "No root directory. Drive type could not be determined."
        Case 2
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Removable drive" 
        Case 3
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Local hard disk" 
        Case 4
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Network disk" 
        Case 5
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Compact disk" 
        Case 6
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = RAM disk" 
        Case Else
            Wscript.Echo "Drive type could not be determined."
    End Select
Next
```



## <a name="requirements"></a><span data-ttu-id="6f206-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f206-179">Requirements</span></span>



| <span data-ttu-id="6f206-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f206-180">Requirement</span></span> | <span data-ttu-id="6f206-181">Valor</span><span class="sxs-lookup"><span data-stu-id="6f206-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f206-182">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f206-182">Minimum supported client</span></span><br/> | <span data-ttu-id="6f206-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f206-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f206-184">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f206-184">Minimum supported server</span></span><br/> | <span data-ttu-id="6f206-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f206-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f206-186">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6f206-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f206-187"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f206-187"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f206-188">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6f206-188">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f206-189"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6f206-189"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6f206-190">DLL</span><span class="sxs-lookup"><span data-stu-id="6f206-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f206-191"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f206-191"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6f206-192">CLSID</span><span class="sxs-lookup"><span data-stu-id="6f206-192">CLSID</span></span><br/>                    | <span data-ttu-id="6f206-193">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="6f206-193">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="6f206-194">IID</span><span class="sxs-lookup"><span data-stu-id="6f206-194">IID</span></span><br/>                      | <span data-ttu-id="6f206-195">ISWbemServices de IID \_</span><span class="sxs-lookup"><span data-stu-id="6f206-195">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="6f206-196">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6f206-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f206-197">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="6f206-197">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="6f206-198">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="6f206-198">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> <dt>

[<span data-ttu-id="6f206-199">Consultando com WQL</span><span class="sxs-lookup"><span data-stu-id="6f206-199">Querying with WQL</span></span>](querying-with-wql.md)
</dt> <dt>

[<span data-ttu-id="6f206-200">Criando um script WMI</span><span class="sxs-lookup"><span data-stu-id="6f206-200">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> <dt>

[<span data-ttu-id="6f206-201">Enumerando o WMI</span><span class="sxs-lookup"><span data-stu-id="6f206-201">Enumerating WMI</span></span>](enumerating-wmi.md)
</dt> </dl>

 

