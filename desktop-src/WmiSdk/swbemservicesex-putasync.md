---
description: Salva um objeto de forma assíncrona em um namespace. Quando bem-sucedida, esse método envia um evento OnCompleted para o objeto SWbemSink que é especificado como um parâmetro de entrada.
ms.assetid: 27da0c60-6dae-482d-a9bf-1aab016d3ae8
ms.tgt_platform: multiple
title: Método SWbemServicesEx. PutAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 06f470ed6f8cbd497ba3d3a3a77c5a8b4e5748c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011344"
---
# <a name="swbemservicesexputasync-method"></a><span data-ttu-id="6223f-104">Método SWbemServicesEx. PutAsync</span><span class="sxs-lookup"><span data-stu-id="6223f-104">SWbemServicesEx.PutAsync method</span></span>

<span data-ttu-id="6223f-105">O método **PutAsync** do objeto [**SWbemServicesEx**](swbemservicesex.md) salva um objeto de forma assíncrona em um namespace.</span><span class="sxs-lookup"><span data-stu-id="6223f-105">The **PutAsync** method of the [**SWbemServicesEx**](swbemservicesex.md) object saves an object asynchronously to a namespace.</span></span> <span data-ttu-id="6223f-106">Quando bem-sucedida, esse método envia um evento [**OnCompleted**](swbemsink-oncompleted.md) para o objeto [**SWbemSink**](swbemsink.md) que é especificado como um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="6223f-106">When successful, this method sends an [**OnCompleted**](swbemsink-oncompleted.md) event to the [**SWbemSink**](swbemsink.md) object that is specified as an input parameter.</span></span>

<span data-ttu-id="6223f-107">Esse método é chamado no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="6223f-107">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="6223f-108">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="6223f-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="6223f-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6223f-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6223f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6223f-110">Syntax</span></span>


```VB
SWbemServicesEx.PutAsync( _
  ByVal objWbemSink, _
  ByVal ojbWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6223f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6223f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6223f-112">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="6223f-112">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="6223f-113">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="6223f-113">Required.</span></span> <span data-ttu-id="6223f-114">Coletor de objeto que recebe os objetos de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="6223f-114">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="6223f-115">Crie um objeto [**SWbemSink**](swbemsink.md) para receber os objetos.</span><span class="sxs-lookup"><span data-stu-id="6223f-115">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="6223f-116">*ojbWbemObject*</span><span class="sxs-lookup"><span data-stu-id="6223f-116">*ojbWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="6223f-117">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="6223f-117">Required.</span></span> <span data-ttu-id="6223f-118">O novo objeto a ser colocado no namespace.</span><span class="sxs-lookup"><span data-stu-id="6223f-118">The new object to be put in the namespace.</span></span> <span data-ttu-id="6223f-119">Esse pode ser um objeto criado recentemente ou um objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="6223f-119">This may be a newly created object or a modified object.</span></span>

</dd> <dt>

<span data-ttu-id="6223f-120">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="6223f-120">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6223f-121">Esse parâmetro determina se a chamada cria ou atualiza o objeto e se a chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="6223f-121">This parameter determines whether the call creates or updates the object and whether the call returns immediately.</span></span> <span data-ttu-id="6223f-122">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6223f-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="6223f-123"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="6223f-123"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="6223f-124">Permite que uma classe seja atualizada quando não há classes derivadas e nenhuma instância para a classe.</span><span class="sxs-lookup"><span data-stu-id="6223f-124">Allows a class to be updated when there are no derived classes and no instances for the class.</span></span> <span data-ttu-id="6223f-125">Ele também permite atualizações em todos os casos quando a alteração é apenas para qualificadores não importantes, por exemplo, o qualificador de **Descrição** .</span><span class="sxs-lookup"><span data-stu-id="6223f-125">It also allows updates in all cases when the change is only to unimportant qualifiers, for example, the **Description** qualifier.</span></span> <span data-ttu-id="6223f-126">Esse é o comportamento padrão para essa chamada e é usado para compatibilidade com as versões anteriores do WMI.</span><span class="sxs-lookup"><span data-stu-id="6223f-126">This is the default behavior for this call, and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="6223f-127">Se a classe tiver instâncias, a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="6223f-127">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="6223f-128"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="6223f-128"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="6223f-129">Permite atualizações de classes mesmo quando há classes filhas e a alteração não causa conflitos com as classes filhas.</span><span class="sxs-lookup"><span data-stu-id="6223f-129">Allows updates of classes even when there are child classes and the change does not cause conflicts with the child classes.</span></span> <span data-ttu-id="6223f-130">Use esse sinalizador ao adicionar uma nova propriedade a uma classe base que não é mencionada anteriormente em nenhuma das classes filhas.</span><span class="sxs-lookup"><span data-stu-id="6223f-130">Use this flag when adding a new property to a base class that is not mentioned previously in any of the child classes.</span></span> <span data-ttu-id="6223f-131">Se a classe tiver instâncias, a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="6223f-131">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="6223f-132"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="6223f-132"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="6223f-133">Esse sinalizador força as atualizações de classes quando existem classes filhas conflitantes.</span><span class="sxs-lookup"><span data-stu-id="6223f-133">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="6223f-134">Por exemplo, esse sinalizador força uma atualização quando um qualificador de classe é definido em uma classe filho e a classe base tenta adicionar o mesmo qualificador em conflito com o existente.</span><span class="sxs-lookup"><span data-stu-id="6223f-134">For example, this flag forces an update when a class qualifier is defined in a child class, and the base class tries to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="6223f-135">No modo de força, esse conflito é resolvido com a exclusão do qualificador conflitante na classe filho.</span><span class="sxs-lookup"><span data-stu-id="6223f-135">In the force mode, this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="6223f-136">Se a classe tiver instâncias, a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="6223f-136">If the class has instances, the update fails.</span></span>

<span data-ttu-id="6223f-137">O uso do modo Force para atualizar uma classe estática causa a exclusão de todas as instâncias dessa classe.</span><span class="sxs-lookup"><span data-stu-id="6223f-137">The use of the force mode to update a static class causes the deletion of all instances of that class.</span></span> <span data-ttu-id="6223f-138">Uma atualização forçada em uma classe de provedor não exclui instâncias da classe.</span><span class="sxs-lookup"><span data-stu-id="6223f-138">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="6223f-139"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="6223f-139"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="6223f-140">Faz com que a classe ou instância seja criada se não existir, ou substituída, se já existir.</span><span class="sxs-lookup"><span data-stu-id="6223f-140">Causes the class or instance to be created if it does not exist, or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="6223f-141"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="6223f-141"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="6223f-142">Usado somente para criação.</span><span class="sxs-lookup"><span data-stu-id="6223f-142">Used for creation only.</span></span> <span data-ttu-id="6223f-143">A chamada falhará se a classe ou instância já existir.</span><span class="sxs-lookup"><span data-stu-id="6223f-143">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="6223f-144"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="6223f-144"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="6223f-145">Faz com que essa chamada seja atualizada.</span><span class="sxs-lookup"><span data-stu-id="6223f-145">Causes this call to update.</span></span> <span data-ttu-id="6223f-146">A classe ou instância deve existir para que a chamada seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6223f-146">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="6223f-147"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="6223f-147"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="6223f-148">Faz com que a chamada retorne imediatamente.</span><span class="sxs-lookup"><span data-stu-id="6223f-148">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="6223f-149"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="6223f-149"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="6223f-150">Faz com que essa chamada seja bloqueada até que a consulta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="6223f-150">Causes this call to block until the query is complete.</span></span> <span data-ttu-id="6223f-151">Esse sinalizador chama o método no modo síncrono.</span><span class="sxs-lookup"><span data-stu-id="6223f-151">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="6223f-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="6223f-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="6223f-153">Faz com que o WMI grave dados de alteração de classe e a definição da classe base.</span><span class="sxs-lookup"><span data-stu-id="6223f-153">Causes WMI to write class amendment data and the base class definition.</span></span> <span data-ttu-id="6223f-154">Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="6223f-154">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6223f-155">*objWbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="6223f-155">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6223f-156">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="6223f-156">Typically, this is undefined.</span></span> <span data-ttu-id="6223f-157">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que presta a solicitação.</span><span class="sxs-lookup"><span data-stu-id="6223f-157">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="6223f-158">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="6223f-158">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="6223f-159">*objWbemAsyncContext* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="6223f-159">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6223f-160">Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="6223f-160">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="6223f-161">Use esse parâmetro para fazer várias chamadas assíncronas usando o mesmo coletor de objeto.</span><span class="sxs-lookup"><span data-stu-id="6223f-161">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="6223f-162">Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="6223f-162">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="6223f-163">Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="6223f-163">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="6223f-164">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="6223f-164">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6223f-165">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6223f-165">Return value</span></span>

<span data-ttu-id="6223f-166">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6223f-166">This method does not return a value.</span></span> <span data-ttu-id="6223f-167">Se a chamada for bem-sucedida, o evento [**OnObjectPut**](swbemsink-onobjectput.md) do coletor de objeto fornecido receberá um objeto [**SWbemObjectPath**](swbemobjectpath.md) , que contém o caminho do objeto da instância ou classe que foi confirmada com êxito no WMI.</span><span class="sxs-lookup"><span data-stu-id="6223f-167">If the call is successful, the [**OnObjectPut**](swbemsink-onobjectput.md) event of the supplied object sink receives an [**SWbemObjectPath**](swbemobjectpath.md) object, which contains the object path of the instance or class that is successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6223f-168">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6223f-168">Error codes</span></span>

<span data-ttu-id="6223f-169">Após a conclusão do método **PutAsync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="6223f-169">After the completion of the **PutAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="6223f-170">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="6223f-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="6223f-171">O usuário atual não tem permissão para atualizar uma instância da classe especificada.</span><span class="sxs-lookup"><span data-stu-id="6223f-171">Current user does not have the permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="6223f-172">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="6223f-172">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="6223f-173">O sinalizador **wbemChangeFlagCreateOnly** foi especificado, mas a instância já existe.</span><span class="sxs-lookup"><span data-stu-id="6223f-173">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6223f-174">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="6223f-174">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="6223f-175">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="6223f-175">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="6223f-176">**wbemErrIllegalNull** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="6223f-176">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="6223f-177">Um valor NULL foi especificado para uma propriedade que não pode ser nula.</span><span class="sxs-lookup"><span data-stu-id="6223f-177">A value of Null was specified for a property that cannot be Null.</span></span> <span data-ttu-id="6223f-178">Um exemplo de tal propriedade é um marcado por um qualificador de **chave**, **indexado** ou **não \_ nulo** .</span><span class="sxs-lookup"><span data-stu-id="6223f-178">An example of such a property is one marked by a **Key**, **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="6223f-179">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="6223f-179">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="6223f-180">A instância especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="6223f-180">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6223f-181">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="6223f-181">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="6223f-182">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="6223f-182">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6223f-183">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="6223f-183">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="6223f-184">O sinalizador **wbemChangeFlagUpdateOnly** foi especificado, mas a instância ou classe não existe.</span><span class="sxs-lookup"><span data-stu-id="6223f-184">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="6223f-185">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="6223f-185">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="6223f-186">As propriedades obrigatórias para classes não foram definidas.</span><span class="sxs-lookup"><span data-stu-id="6223f-186">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="6223f-187">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="6223f-187">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="6223f-188">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="6223f-188">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6223f-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="6223f-189">Remarks</span></span>

<span data-ttu-id="6223f-190">Essa chamada retorna imediatamente, e os resultados e o status são retornados ao chamador por meio de eventos entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="6223f-190">This call returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="6223f-191">Para lidar com cada objeto quando ele chega, crie um *objWbemSink*. Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="6223f-191">To handle each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="6223f-192">Qualquer processamento feito após a chegada de todos os objetos é feito em uma sub-rotina para o *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="6223f-192">Any processing done after all the objects arrive is done in a subroutine for the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="6223f-193">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="6223f-193">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="6223f-194">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6223f-194">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="6223f-195">Para eliminar os riscos, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="6223f-195">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6223f-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6223f-196">Requirements</span></span>



| <span data-ttu-id="6223f-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="6223f-197">Requirement</span></span> | <span data-ttu-id="6223f-198">Valor</span><span class="sxs-lookup"><span data-stu-id="6223f-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6223f-199">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6223f-199">Minimum supported client</span></span><br/> | <span data-ttu-id="6223f-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6223f-200">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6223f-201">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6223f-201">Minimum supported server</span></span><br/> | <span data-ttu-id="6223f-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6223f-202">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6223f-203">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6223f-203">Header</span></span><br/>                   | <dl> <span data-ttu-id="6223f-204"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6223f-204"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6223f-205">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6223f-205">Type library</span></span><br/>             | <dl> <span data-ttu-id="6223f-206"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6223f-206"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6223f-207">DLL</span><span class="sxs-lookup"><span data-stu-id="6223f-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6223f-208"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6223f-208"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6223f-209">CLSID</span><span class="sxs-lookup"><span data-stu-id="6223f-209">CLSID</span></span><br/>                    | <span data-ttu-id="6223f-210">\_ISWBEMSERVICESEX CLSID</span><span class="sxs-lookup"><span data-stu-id="6223f-210">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="6223f-211">IID</span><span class="sxs-lookup"><span data-stu-id="6223f-211">IID</span></span><br/>                      | <span data-ttu-id="6223f-212">ISWbemServicesEx de IID \_</span><span class="sxs-lookup"><span data-stu-id="6223f-212">IID\_ISWbemServicesEx</span></span><br/>                                                        |



 

