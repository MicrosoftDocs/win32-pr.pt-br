---
description: Retorna um objeto SWbemObjectPath que contém o caminho do objeto para o qual os dados foram gravados.
ms.assetid: 1a9a718d-875d-4102-9d9d-3d10be162f58
ms.tgt_platform: multiple
title: Método SWbemServicesEx. put (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.Put
- ISWbemServicesEx.Put
- ISWbemServicesEx.Put
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e495a38262e6b6f7dd8b67424b74db74c025be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761543"
---
# <a name="swbemservicesexput-method"></a><span data-ttu-id="75b6d-103">Método SWbemServicesEx. put</span><span class="sxs-lookup"><span data-stu-id="75b6d-103">SWbemServicesEx.Put method</span></span>

<span data-ttu-id="75b6d-104">O método **Put** do objeto [**SWbemServicesEx**](swbemservicesex.md) salva o objeto no namespace associado ao objeto e retorna um objeto [**SWbemObjectPath**](swbemobjectpath.md) que contém o caminho do objeto no qual os dados foram gravados.</span><span class="sxs-lookup"><span data-stu-id="75b6d-104">The **Put** method of the [**SWbemServicesEx**](swbemservicesex.md) object saves the object to the namespace bound to the object and returns an [**SWbemObjectPath**](swbemobjectpath.md) object that contains the path of the object to which the data was written.</span></span>

<span data-ttu-id="75b6d-105">Esse método é chamado no modo semisynchronous.</span><span class="sxs-lookup"><span data-stu-id="75b6d-105">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="75b6d-106">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="75b6d-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="75b6d-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="75b6d-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="75b6d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75b6d-108">Syntax</span></span>


```VB
objObjectPath = .Put( _
  ByVal objWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="75b6d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75b6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75b6d-110">*objWbemObject*</span><span class="sxs-lookup"><span data-stu-id="75b6d-110">*objWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="75b6d-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="75b6d-111">Required.</span></span> <span data-ttu-id="75b6d-112">O novo objeto a ser colocado no namespace.</span><span class="sxs-lookup"><span data-stu-id="75b6d-112">The new object to be put in the namespace.</span></span> <span data-ttu-id="75b6d-113">Pode ser um objeto criado recentemente ou um objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="75b6d-113">This can be either a newly created object or a modified object.</span></span>

</dd> <dt>

<span data-ttu-id="75b6d-114">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="75b6d-114">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="75b6d-115">Esse parâmetro determina se a chamada cria ou atualiza o objeto e se a chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="75b6d-115">This parameter determines if the call creates or updates the object and if the call returns immediately.</span></span> <span data-ttu-id="75b6d-116">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="75b6d-116">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="75b6d-117"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="75b6d-117"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="75b6d-118">Permite que uma classe seja atualizada se não houver classes derivadas e não houver nenhuma instância para essa classe.</span><span class="sxs-lookup"><span data-stu-id="75b6d-118">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="75b6d-119">Ele também permitirá atualizações em todos os casos se a alteração for apenas para qualificadores não importantes (por exemplo, o qualificador de **Descrição** ).</span><span class="sxs-lookup"><span data-stu-id="75b6d-119">It also allows updates in all cases if the change is only to unimportant qualifiers (for example, the **Description** qualifier).</span></span> <span data-ttu-id="75b6d-120">Esse é o comportamento padrão para essa chamada e é usado para compatibilidade com as versões anteriores do WMI.</span><span class="sxs-lookup"><span data-stu-id="75b6d-120">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="75b6d-121">Se a classe tiver instâncias, a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="75b6d-121">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="75b6d-122"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="75b6d-122"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="75b6d-123">Permite atualizações de classes, mesmo se houver classes filhas, quando a alteração não causar conflitos com classes filhas.</span><span class="sxs-lookup"><span data-stu-id="75b6d-123">Allows updates of classes even if there are child classes, when the change does not cause any conflicts with child classes.</span></span> <span data-ttu-id="75b6d-124">Você pode usar esse sinalizador ao adicionar uma nova propriedade a uma classe base que não foi mencionada anteriormente em nenhuma das classes filhas.</span><span class="sxs-lookup"><span data-stu-id="75b6d-124">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="75b6d-125">Se a classe tiver instâncias, a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="75b6d-125">If the class has instances, the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="75b6d-126"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="75b6d-126"><span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="75b6d-127">Esse sinalizador força as atualizações de classes quando existem classes filhas conflitantes.</span><span class="sxs-lookup"><span data-stu-id="75b6d-127">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="75b6d-128">Por exemplo, esse sinalizador força uma atualização se um qualificador de classe foi definido em uma classe filho e a classe base tenta adicionar o mesmo qualificador em conflito com o existente.</span><span class="sxs-lookup"><span data-stu-id="75b6d-128">For example, this flag forces an update if a class qualifier was defined in a child class, and the base class tries to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="75b6d-129">No modo de força, esse conflito é resolvido com a exclusão do qualificador conflitante na classe filho.</span><span class="sxs-lookup"><span data-stu-id="75b6d-129">In the force mode, this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="75b6d-130">Se a classe tiver instâncias, a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="75b6d-130">If the class has instances, the update fails.</span></span>

<span data-ttu-id="75b6d-131">O uso do modo Force para atualizar uma classe estática causa a exclusão de todas as instâncias dessa classe.</span><span class="sxs-lookup"><span data-stu-id="75b6d-131">The use of the force mode to update a static class causes the deletion of all instances of that class.</span></span> <span data-ttu-id="75b6d-132">Uma atualização forçada em uma classe de provedor não exclui instâncias da classe.</span><span class="sxs-lookup"><span data-stu-id="75b6d-132">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="75b6d-133"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="75b6d-133"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="75b6d-134">Faz com que a classe ou instância seja criada se não existir, ou substituída, se já existir.</span><span class="sxs-lookup"><span data-stu-id="75b6d-134">Causes the class or instance to be created if it does not exist, or overwritten if it already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="75b6d-135"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="75b6d-135"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="75b6d-136">Usado somente para criação.</span><span class="sxs-lookup"><span data-stu-id="75b6d-136">Used for creation only.</span></span> <span data-ttu-id="75b6d-137">A chamada falhará se a classe ou instância já existir.</span><span class="sxs-lookup"><span data-stu-id="75b6d-137">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="75b6d-138"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="75b6d-138"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="75b6d-139">Faz com que essa chamada faça apenas uma atualização.</span><span class="sxs-lookup"><span data-stu-id="75b6d-139">Causes this call to only do an update.</span></span> <span data-ttu-id="75b6d-140">A classe ou instância deve existir para que a chamada seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="75b6d-140">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="75b6d-141"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="75b6d-141"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="75b6d-142">Faz com que a chamada retorne imediatamente.</span><span class="sxs-lookup"><span data-stu-id="75b6d-142">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="75b6d-143"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="75b6d-143"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="75b6d-144">Faz com que essa chamada seja bloqueada até que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="75b6d-144">Causes this call to block until the operation has completed.</span></span> <span data-ttu-id="75b6d-145">Esse sinalizador chama o método no modo síncrono.</span><span class="sxs-lookup"><span data-stu-id="75b6d-145">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="75b6d-146"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="75b6d-146"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="75b6d-147">Faz com que o WMI grave dados de emenda de classe, bem como a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="75b6d-147">Causes WMI to write class amendment data as well as the base class definition.</span></span> <span data-ttu-id="75b6d-148">Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="75b6d-148">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="75b6d-149">*objWbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="75b6d-149">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="75b6d-150">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="75b6d-150">Typically, this is undefined.</span></span> <span data-ttu-id="75b6d-151">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que presta a solicitação.</span><span class="sxs-lookup"><span data-stu-id="75b6d-151">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="75b6d-152">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="75b6d-152">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75b6d-153">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75b6d-153">Return value</span></span>

<span data-ttu-id="75b6d-154">Se a chamada for bem-sucedida, um objeto [**SWbemObjectPath**](swbemobjectpath.md) será retornado.</span><span class="sxs-lookup"><span data-stu-id="75b6d-154">If the call is successful, an [**SWbemObjectPath**](swbemobjectpath.md) object is returned.</span></span> <span data-ttu-id="75b6d-155">Este objeto contém o caminho do objeto da instância ou classe que foi confirmada com êxito no WMI.</span><span class="sxs-lookup"><span data-stu-id="75b6d-155">This object contains the object path of the instance or class that has been successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="75b6d-156">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="75b6d-156">Error codes</span></span>

<span data-ttu-id="75b6d-157">Após a conclusão do método **Put** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="75b6d-157">After the completion of the **Put** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="75b6d-158">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="75b6d-158">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="75b6d-159">O usuário atual não tem a permissão para a operação.</span><span class="sxs-lookup"><span data-stu-id="75b6d-159">Current user does not have the permission for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="75b6d-160">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="75b6d-160">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="75b6d-161">O sinalizador **wbemChangeFlagCreateOnly** foi especificado, mas a instância já existe.</span><span class="sxs-lookup"><span data-stu-id="75b6d-161">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="75b6d-162">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="75b6d-162">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="75b6d-163">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="75b6d-163">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="75b6d-164">**wbemErrIllegalNull** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="75b6d-164">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="75b6d-165">Um valor **NULL** foi especificado para uma propriedade que não pode ser **nula**.</span><span class="sxs-lookup"><span data-stu-id="75b6d-165">A value of **NULL** was specified for a property that cannot be **NULL**.</span></span> <span data-ttu-id="75b6d-166">Um exemplo de tal propriedade é um marcado por um qualificador de [**chave**](standard-qualifiers.md), **indexado** ou **não \_ nulo** .</span><span class="sxs-lookup"><span data-stu-id="75b6d-166">An example of such a property is one marked by a [**Key**](standard-qualifiers.md), **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="75b6d-167">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="75b6d-167">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="75b6d-168">O objeto especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="75b6d-168">The specified object is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="75b6d-169">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="75b6d-169">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="75b6d-170">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="75b6d-170">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="75b6d-171">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="75b6d-171">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="75b6d-172">O sinalizador **wbemChangeFlagUpdateOnly** foi especificado, mas a instância ou classe não existe.</span><span class="sxs-lookup"><span data-stu-id="75b6d-172">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="75b6d-173">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="75b6d-173">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="75b6d-174">As propriedades obrigatórias para classes não foram definidas.</span><span class="sxs-lookup"><span data-stu-id="75b6d-174">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="75b6d-175">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="75b6d-175">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="75b6d-176">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="75b6d-176">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75b6d-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75b6d-177">Requirements</span></span>



| <span data-ttu-id="75b6d-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="75b6d-178">Requirement</span></span> | <span data-ttu-id="75b6d-179">Valor</span><span class="sxs-lookup"><span data-stu-id="75b6d-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75b6d-180">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75b6d-180">Minimum supported client</span></span><br/> | <span data-ttu-id="75b6d-181">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75b6d-181">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75b6d-182">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75b6d-182">Minimum supported server</span></span><br/> | <span data-ttu-id="75b6d-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75b6d-183">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75b6d-184">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75b6d-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="75b6d-185"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="75b6d-185"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="75b6d-186">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="75b6d-186">Type library</span></span><br/>             | <dl> <span data-ttu-id="75b6d-187"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="75b6d-187"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="75b6d-188">DLL</span><span class="sxs-lookup"><span data-stu-id="75b6d-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75b6d-189"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75b6d-189"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="75b6d-190">CLSID</span><span class="sxs-lookup"><span data-stu-id="75b6d-190">CLSID</span></span><br/>                    | <span data-ttu-id="75b6d-191">\_ISWBEMSERVICESEX CLSID</span><span class="sxs-lookup"><span data-stu-id="75b6d-191">CLSID\_ISWbemServicesEx</span></span><br/>                                                      |
| <span data-ttu-id="75b6d-192">IID</span><span class="sxs-lookup"><span data-stu-id="75b6d-192">IID</span></span><br/>                      | <span data-ttu-id="75b6d-193">ISWbemServicesEx de IID \_</span><span class="sxs-lookup"><span data-stu-id="75b6d-193">IID\_ISWbemServicesEx</span></span><br/>                                                        |



 

 




