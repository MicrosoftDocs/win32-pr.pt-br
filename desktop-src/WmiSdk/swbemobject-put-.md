---
description: O \_ método Put de SWbemObject cria ou atualiza uma instância ou um objeto de classe para instrumentação de gerenciamento do Windows (WMI). Você pode usar esse método depois de modificar qualquer propriedade ou método em um SWbemObject e suas alterações são gravadas no WMI.
ms.assetid: c636ff95-9f3e-4ba9-adf3-30b981be02a4
ms.tgt_platform: multiple
title: Método de SWbemObject.Put_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Put_
- ISWbemObject.Put_
- ISWbemObject.Put_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9f5ca9b79c9def8f209da37e0ef1cfddefa0dbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785283"
---
# <a name="swbemobjectput_-method"></a><span data-ttu-id="19425-104">Método SWbemObject. put \_</span><span class="sxs-lookup"><span data-stu-id="19425-104">SWbemObject.Put\_ method</span></span>

<span data-ttu-id="19425-105">O **método \_ Put** de [**SWbemObject**](swbemobject.md) cria ou atualiza uma instância ou um objeto de classe para instrumentação de gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="19425-105">The **Put\_** method of [**SWbemObject**](swbemobject.md) creates or updates an instance or a class object to Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="19425-106">Você pode usar esse método depois de modificar qualquer propriedade ou método em um **SWbemObject** e suas alterações são gravadas no WMI.</span><span class="sxs-lookup"><span data-stu-id="19425-106">You can use this method after you modify any properties or methods in an **SWbemObject**, and your changes are written to WMI.</span></span>

<span data-ttu-id="19425-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="19425-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="19425-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19425-108">Syntax</span></span>


```VB
objObjectPath = .Put_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="19425-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19425-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19425-110">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="19425-110">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19425-111">Esse parâmetro determina se a chamada cria ou atualiza a classe ou instância e se a chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="19425-111">This parameter determines if the call creates or updates the class or instance and if the call returns immediately.</span></span> <span data-ttu-id="19425-112">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="19425-112">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="19425-113"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemChangeFlagUpdateCompatible \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="19425-113"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>\*\*\*\*wbemChangeFlagUpdateCompatible\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="19425-114">Permite que uma classe seja atualizada se não houver classes derivadas e não houver nenhuma instância para essa classe.</span><span class="sxs-lookup"><span data-stu-id="19425-114">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="19425-115">Ele também permitirá atualizações em todos os casos se a alteração for apenas para qualificadores não importantes (por exemplo, o qualificador de **Descrição** ).</span><span class="sxs-lookup"><span data-stu-id="19425-115">It also allows updates in all cases if the change is just to unimportant qualifiers (for example, the **Description** qualifier).</span></span> <span data-ttu-id="19425-116">Esse é o comportamento padrão para essa chamada e é usado para compatibilidade com as versões anteriores do WMI.</span><span class="sxs-lookup"><span data-stu-id="19425-116">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="19425-117">Se a classe tiver instâncias, a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="19425-117">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="19425-118"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemChangeFlagUpdateSafeMode \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="19425-118"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>\*\*\*\*wbemChangeFlagUpdateSafeMode\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="19425-119">Permite atualizações de classes, mesmo se houver classes filhas, se a alteração não causar conflitos com classes filhas.</span><span class="sxs-lookup"><span data-stu-id="19425-119">Allows updates of classes even if there are child classes if the change does not cause any conflicts with child classes.</span></span> <span data-ttu-id="19425-120">Você pode usar esse sinalizador ao adicionar uma nova propriedade a uma classe base que não foi mencionada anteriormente em nenhuma das classes filhas.</span><span class="sxs-lookup"><span data-stu-id="19425-120">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="19425-121">Se a classe tiver instâncias, a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="19425-121">If the class has instances the update fails.</span></span> <span data-ttu-id="19425-122">Se a classe tiver instâncias, a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="19425-122">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="19425-123"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>WbemChangeFlagUpdateForceMode \* \* \* \* (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="19425-123"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>\*\*\*\*WbemChangeFlagUpdateForceMode\*\*\*\* (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="19425-124">Esse sinalizador força as atualizações de classes quando existem classes filhas conflitantes.</span><span class="sxs-lookup"><span data-stu-id="19425-124">This flag forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="19425-125">Por exemplo, esse sinalizador forçará uma atualização se um qualificador de classe tiver sido definido em uma classe filho e a classe base tentar adicionar o mesmo qualificador e estiver em conflito com o existente.</span><span class="sxs-lookup"><span data-stu-id="19425-125">For example, this flag will force an update if a class qualifier was defined in a child class, and the base class tries to add the same qualifier and in conflict with the existing one.</span></span> <span data-ttu-id="19425-126">No modo de força, esse conflito seria resolvido com a exclusão do qualificador conflitante na classe filho.</span><span class="sxs-lookup"><span data-stu-id="19425-126">In force mode this conflict would be resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="19425-127">Se a classe tiver instâncias, a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="19425-127">If the class has instances the update will fail.</span></span>

<span data-ttu-id="19425-128">O uso do modo Force para atualizar uma classe estática resulta na exclusão de todas as instâncias dessa classe.</span><span class="sxs-lookup"><span data-stu-id="19425-128">Using force mode to update a static class results in the deletion of all instances of that class.</span></span> <span data-ttu-id="19425-129">Uma atualização forçada em uma classe de provedor não exclui instâncias da classe.</span><span class="sxs-lookup"><span data-stu-id="19425-129">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="19425-130"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemChangeFlagCreateOrUpdate \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="19425-130"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>\*\*\*\*wbemChangeFlagCreateOrUpdate\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="19425-131">Faz com que a classe ou instância seja criada se ela não existir ou substituída se já existir.</span><span class="sxs-lookup"><span data-stu-id="19425-131">Causes the class or instance to be created if it does not exist or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="19425-132"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemChangeFlagCreateOnly \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="19425-132"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>\*\*\*\*wbemChangeFlagCreateOnly\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="19425-133">Usado somente para criação.</span><span class="sxs-lookup"><span data-stu-id="19425-133">Used for creation only.</span></span> <span data-ttu-id="19425-134">A chamada falhará se a classe ou instância já existir.</span><span class="sxs-lookup"><span data-stu-id="19425-134">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="19425-135"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemChangeFlagUpdateOnly \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="19425-135"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>\*\*\*\*wbemChangeFlagUpdateOnly\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="19425-136">Faz com que essa chamada seja atualizada.</span><span class="sxs-lookup"><span data-stu-id="19425-136">Causes this call to update.</span></span> <span data-ttu-id="19425-137">A classe ou instância deve existir para que a chamada seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="19425-137">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="19425-138"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="19425-138"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="19425-139">Faz com que a chamada retorne imediatamente.</span><span class="sxs-lookup"><span data-stu-id="19425-139">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="19425-140"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="19425-140"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="19425-141">Faz com que essa chamada seja bloqueada até que a consulta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="19425-141">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="19425-142"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="19425-142"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="19425-143">Faz com que o WMI grave dados de emenda de classe, bem como a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="19425-143">Causes WMI to write class amendment data as well as the base class definition.</span></span> <span data-ttu-id="19425-144">Para obter mais informações sobre qualificadores corrigidos, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="19425-144">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="19425-145">*objwbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="19425-145">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19425-146">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="19425-146">Typically, this is undefined.</span></span> <span data-ttu-id="19425-147">Caso contrário, esse é um objeto [**SWbemObjectPath**](swbemobjectpath.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="19425-147">Otherwise, this is an [**SWbemObjectPath**](swbemobjectpath.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="19425-148">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="19425-148">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19425-149">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19425-149">Return value</span></span>

<span data-ttu-id="19425-150">Se a chamada for bem-sucedida, um objeto [**SWbemObjectPath**](swbemobjectpath.md) será retornado.</span><span class="sxs-lookup"><span data-stu-id="19425-150">If the call is successful, an [**SWbemObjectPath**](swbemobjectpath.md) object is returned.</span></span> <span data-ttu-id="19425-151">Este objeto contém o caminho do objeto da instância ou classe que foi confirmada com êxito no WMI.</span><span class="sxs-lookup"><span data-stu-id="19425-151">This object contains the object path of the instance or class that has been successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="19425-152">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="19425-152">Error codes</span></span>

<span data-ttu-id="19425-153">Após a conclusão do método **Put \_** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="19425-153">After the completion of the **Put\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="19425-154">**wbemErrAccessDenied** -2147749891</span><span class="sxs-lookup"><span data-stu-id="19425-154">**wbemErrAccessDenied** - 2147749891</span></span>
</dt> <dd>

<span data-ttu-id="19425-155">O usuário atual não tem permissão para atualizar uma instância da classe especificada.</span><span class="sxs-lookup"><span data-stu-id="19425-155">Current user does not have permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="19425-156">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="19425-156">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="19425-157">O sinalizador **wbemChangeFlagCreateOnly** foi especificado, mas a instância já existe.</span><span class="sxs-lookup"><span data-stu-id="19425-157">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="19425-158">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="19425-158">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="19425-159">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="19425-159">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="19425-160">**wbemErrIllegalNull** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="19425-160">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="19425-161">Um valor de **nada** foi especificado para uma propriedade que pode não ser **nada**.</span><span class="sxs-lookup"><span data-stu-id="19425-161">A value of **Nothing** was specified for a property that may not be **Nothing**.</span></span> <span data-ttu-id="19425-162">Um exemplo de tal propriedade é um marcado por um qualificador de **chave,** **indexado** ou **não \_ nulo** .</span><span class="sxs-lookup"><span data-stu-id="19425-162">An example of such a property is one marked by a **Key,** **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="19425-163">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="19425-163">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="19425-164">A instância especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="19425-164">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="19425-165">**wbemErrInvalidParameter** -0x80041008</span><span class="sxs-lookup"><span data-stu-id="19425-165">**wbemErrInvalidParameter** - 0x80041008</span></span>
</dt> <dd>

<span data-ttu-id="19425-166">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="19425-166">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="19425-167">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="19425-167">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="19425-168">O sinalizador **wbemChangeFlagUpdateOnly** foi especificado, mas a instância ou classe não existe.</span><span class="sxs-lookup"><span data-stu-id="19425-168">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="19425-169">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="19425-169">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="19425-170">As propriedades obrigatórias para classes não foram definidas.</span><span class="sxs-lookup"><span data-stu-id="19425-170">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="19425-171">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="19425-171">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="19425-172">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="19425-172">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19425-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19425-173">Requirements</span></span>



| <span data-ttu-id="19425-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="19425-174">Requirement</span></span> | <span data-ttu-id="19425-175">Valor</span><span class="sxs-lookup"><span data-stu-id="19425-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19425-176">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19425-176">Minimum supported client</span></span><br/> | <span data-ttu-id="19425-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19425-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19425-178">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19425-178">Minimum supported server</span></span><br/> | <span data-ttu-id="19425-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19425-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19425-180">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19425-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="19425-181"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="19425-181"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="19425-182">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="19425-182">Type library</span></span><br/>             | <dl> <span data-ttu-id="19425-183"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="19425-183"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="19425-184">DLL</span><span class="sxs-lookup"><span data-stu-id="19425-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19425-185"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19425-185"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="19425-186">CLSID</span><span class="sxs-lookup"><span data-stu-id="19425-186">CLSID</span></span><br/>                    | <span data-ttu-id="19425-187">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="19425-187">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="19425-188">IID</span><span class="sxs-lookup"><span data-stu-id="19425-188">IID</span></span><br/>                      | <span data-ttu-id="19425-189">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="19425-189">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="19425-190">Confira também</span><span class="sxs-lookup"><span data-stu-id="19425-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19425-191">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="19425-191">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="19425-192">**SWbemObjectPath. Class**</span><span class="sxs-lookup"><span data-stu-id="19425-192">**SWbemObjectPath.Class**</span></span>](swbemobjectpath-class.md)
</dt> <dt>

[<span data-ttu-id="19425-193">**SWbemProperty**</span><span class="sxs-lookup"><span data-stu-id="19425-193">**SWbemProperty**</span></span>](swbemproperty.md)
</dt> <dt>

[<span data-ttu-id="19425-194">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="19425-194">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

