---
description: O \_ método PutAsync de SWbemObject cria ou atualiza de forma assíncrona uma instância ou um objeto de classe para instrumentação de gerenciamento do Windows (WMI).
ms.assetid: ff738412-fcca-4e4a-a178-0d1d391ec99b
ms.tgt_platform: multiple
title: Método de SWbemObject.PutAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.PutAsync_
- ISWbemObject.PutAsync_
- ISWbemObject.PutAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3530c3883763773f53bec81aeee8b0d199170133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171792"
---
# <a name="swbemobjectputasync_-method"></a><span data-ttu-id="f1bc3-103">Método SWbemObject. PutAsync \_</span><span class="sxs-lookup"><span data-stu-id="f1bc3-103">SWbemObject.PutAsync\_ method</span></span>

<span data-ttu-id="f1bc3-104">O **método \_ PutAsync** de [**SWbemObject**](swbemobject.md) cria ou atualiza de forma assíncrona uma instância ou um objeto de classe para instrumentação de gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f1bc3-104">The **PutAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously creates or updates an instance or class object to Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="f1bc3-105">Você pode usar esse método depois de modificar qualquer propriedade ou método em **SWbemObject** e suas alterações são gravadas no WMI.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-105">You can use this method after you modify any properties or methods in **SWbemObject**, and your changes are written to WMI.</span></span>

<span data-ttu-id="f1bc3-106">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f1bc3-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f1bc3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1bc3-107">Syntax</span></span>


```VB
SWbemObject.PutAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f1bc3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1bc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1bc3-109">*objWbemSink* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f1bc3-109">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-110">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-110">Required.</span></span> <span data-ttu-id="f1bc3-111">Coletor de objeto que recebe de forma assíncrona o resultado da operação **Put** .</span><span class="sxs-lookup"><span data-stu-id="f1bc3-111">Object sink that asynchronously receives the result of the **put** operation.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-112">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f1bc3-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-113">Determina se a chamada cria ou atualiza a classe ou instância e se a chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-113">Determines if the call creates or updates the class or instance and if the call returns immediately.</span></span> <span data-ttu-id="f1bc3-114">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-114">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span data-ttu-id="f1bc3-115"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemChangeFlagUpdateCompatible \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="f1bc3-115"><span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>\*\*\*\*wbemChangeFlagUpdateCompatible\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f1bc3-116">Permite que uma classe seja atualizada se não houver classes derivadas e não houver nenhuma instância para essa classe.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-116">Allows a class to be updated if there are no derived classes and there are no instances for that class.</span></span> <span data-ttu-id="f1bc3-117">Ele também permite atualizações em todos os casos se a alteração for apenas para qualificadores não importantes (por exemplo, o qualificador de **Descrição** ).</span><span class="sxs-lookup"><span data-stu-id="f1bc3-117">It also allows updates in all cases if the change is just to unimportant qualifiers (for example the **Description** qualifier).</span></span> <span data-ttu-id="f1bc3-118">Esse é o comportamento padrão para essa chamada e é usado para compatibilidade com as versões anteriores do WMI.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-118">This is the default behavior for this call and is used for compatibility with previous versions of WMI.</span></span> <span data-ttu-id="f1bc3-119">Se a classe tiver instâncias, a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-119">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span data-ttu-id="f1bc3-120"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemChangeFlagUpdateSafeMode \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="f1bc3-120"><span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>\*\*\*\*wbemChangeFlagUpdateSafeMode\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="f1bc3-121">Permite atualizações de classes, mesmo se houver classes filhas, se a alteração não causar conflitos com classes filhas.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-121">Allows updates of classes, even if there are child classes, if the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="f1bc3-122">Você pode usar esse sinalizador ao adicionar uma nova propriedade a uma classe base que não foi mencionada anteriormente em nenhuma das classes filhas.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-122">You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="f1bc3-123">Se a classe tiver instâncias, a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-123">If the class has instances the update fails.</span></span>

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span data-ttu-id="f1bc3-124"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>WbemChangeFlagUpdateForceMode \* \* \* \* (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="f1bc3-124"><span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>\*\*\*\*WbemChangeFlagUpdateForceMode\*\*\*\* (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="f1bc3-125">Força atualizações de classes quando existem classes filhas conflitantes.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-125">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="f1bc3-126">Por exemplo, esse sinalizador força uma atualização se um qualificador de classe foi definido em uma classe filho e a classe base tenta adicionar o mesmo qualificador em conflito com o existente.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-126">For example, this flag forces an update if a class qualifier was defined in a child class, and the base class attempts to add the same qualifier in conflict with the existing one.</span></span> <span data-ttu-id="f1bc3-127">Em forçar modo, esse conflito é resolvido com a exclusão do qualificador conflitante na classe filho.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-127">In force mode this conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="f1bc3-128">Se a classe tiver instâncias, a atualização falhará.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-128">If the class has instances the update fails.</span></span>

<span data-ttu-id="f1bc3-129">O uso do modo Force para atualizar uma classe estática resulta na exclusão de todas as instâncias dessa classe.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-129">Using force mode to update a static class results in the deletion of all instances of that class.</span></span> <span data-ttu-id="f1bc3-130">Uma atualização forçada em uma classe de provedor não exclui instâncias da classe.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-130">A forced update on a provider class does not delete instances of the class.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span data-ttu-id="f1bc3-131"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemChangeFlagCreateOrUpdate \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="f1bc3-131"><span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>\*\*\*\*wbemChangeFlagCreateOrUpdate\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f1bc3-132">Faz com que a classe ou instância seja criada se ela não existir ou substituída se já existir.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-132">Causes the class or instance to be created if it does not exist or overwritten if it exists already.</span></span>

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span data-ttu-id="f1bc3-133"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemChangeFlagCreateOnly \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="f1bc3-133"><span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>\*\*\*\*wbemChangeFlagCreateOnly\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="f1bc3-134">Usado somente para criação.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-134">Used for creation only.</span></span> <span data-ttu-id="f1bc3-135">A chamada falhará se a classe ou instância já existir.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-135">The call fails if the class or instance already exists.</span></span>

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span data-ttu-id="f1bc3-136"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemChangeFlagUpdateOnly \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="f1bc3-136"><span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>\*\*\*\*wbemChangeFlagUpdateOnly\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="f1bc3-137">Faz com que essa chamada seja atualizada.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-137">Causes this call to update.</span></span> <span data-ttu-id="f1bc3-138">A classe ou instância deve existir para que a chamada seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-138">The class or instance must exist for the call to be successful.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="f1bc3-139"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="f1bc3-139"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="f1bc3-140">Faz com que a chamada retorne imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-140">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="f1bc3-141"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="f1bc3-141"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f1bc3-142">Faz com que essa chamada seja bloqueada até que a consulta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-142">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="f1bc3-143"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="f1bc3-143"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="f1bc3-144">Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**SWbemSink. OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-144">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="f1bc3-145"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="f1bc3-145"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f1bc3-146">Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-146">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="f1bc3-147"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="f1bc3-147"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="f1bc3-148">Faz com que o WMI grave dados de alteração de classe junto com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-148">Causes WMI to write class amendment data along with the base class definition.</span></span> <span data-ttu-id="f1bc3-149">Para obter mais informações sobre qualificadores corrigidos, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="f1bc3-149">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f1bc3-150">*objWbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f1bc3-150">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-151">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-151">Typically, this is undefined.</span></span> <span data-ttu-id="f1bc3-152">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-152">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="f1bc3-153">Um provedor que dá suporte ou requer essas informações deve documentar os nomes de valores reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-153">A provider that supports or requires this information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-154">*objWbemAsyncContext* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f1bc3-154">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-155">Esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-155">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="f1bc3-156">Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-156">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="f1bc3-157">Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-157">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="f1bc3-158">Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="f1bc3-158">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="f1bc3-159">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f1bc3-159">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1bc3-160">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1bc3-160">Return value</span></span>

<span data-ttu-id="f1bc3-161">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-161">This method does not return a value.</span></span> <span data-ttu-id="f1bc3-162">Se a chamada for bem-sucedida, o evento [**OnObjectPut**](swbemsink-onobjectput.md) do coletor de objeto fornecido receberá um objeto [**SWbemObjectPath**](swbemobjectpath.md) , contendo o caminho do objeto da instância ou classe que está confirmada com êxito no WMI.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-162">If the call is successful, the [**OnObjectPut**](swbemsink-onobjectput.md) event of the supplied object sink receives an [**SWbemObjectPath**](swbemobjectpath.md) object, containing the object path of the instance or class that is successfully committed to WMI.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f1bc3-163">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f1bc3-163">Error codes</span></span>

<span data-ttu-id="f1bc3-164">Após a conclusão do método **PutAsync \_** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-164">After the completion of the **PutAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="f1bc3-165">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="f1bc3-165">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-166">O usuário atual não tem permissão para atualizar uma instância da classe especificada.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-166">Current user does not have permission to update an instance of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-167">**wbemErrAlreadyExists** -2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="f1bc3-167">**wbemErrAlreadyExists** - 2147749913 (0x80041019)</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-168">O sinalizador **wbemChangeFlagCreateOnly** foi especificado, mas a instância já existe.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-168">The **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-169">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="f1bc3-169">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-170">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-170">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-171">**wbemErrIllegalNull** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="f1bc3-171">**wbemErrIllegalNull** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-172">Um valor de **nada** foi especificado para uma propriedade que pode não ser **nada**.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-172">A value of **Nothing** was specified for a property that may not be **Nothing**.</span></span> <span data-ttu-id="f1bc3-173">Um exemplo de tal propriedade é um que é marcado por um qualificador de **chave**, **indexado** ou **não \_ nulo** .</span><span class="sxs-lookup"><span data-stu-id="f1bc3-173">An example of such a property is one that is marked by a **Key**, **Indexed**, or **Not\_Null** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-174">**wbemErrInvalidObject** -2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="f1bc3-174">**wbemErrInvalidObject** - 2147749908 (0x80041014)</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-175">A instância especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-175">The specified instance is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-176">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="f1bc3-176">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-177">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-177">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-178">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="f1bc3-178">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-179">O sinalizador **wbemChangeFlagUpdateOnly** foi especificado, mas a instância ou classe não existe.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-179">The **wbemChangeFlagUpdateOnly** flag was specified, but the instance or class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-180">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="f1bc3-180">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-181">As propriedades obrigatórias para classes não foram definidas.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-181">Required properties for classes have not all been set.</span></span>

</dd> <dt>

<span data-ttu-id="f1bc3-182">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="f1bc3-182">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="f1bc3-183">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-183">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1bc3-184">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1bc3-184">Remarks</span></span>

<span data-ttu-id="f1bc3-185">Essa chamada retorna imediatamente, e o resultado da operação **Put** é retornado para o chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-185">This call returns immediately, and the result of the **put** operation is returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="f1bc3-186">Implemente o *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-186">Implement the *objWbemSink*.</span></span> <span data-ttu-id="f1bc3-187">Método [**OnObjectPut**](swbemsink-onobjectput.md) para obter o caminho do objeto da instância ou da classe que é gravada no repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-187">[**OnObjectPut**](swbemsink-onobjectput.md) method to obtain the object path of the instance or class that is written to the WMI repository.</span></span> <span data-ttu-id="f1bc3-188">Para obter mais informações sobre métodos de coletor, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f1bc3-188">For more information about sink methods, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="f1bc3-189">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-189">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="f1bc3-190">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-190">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="f1bc3-191">Para eliminar os riscos, use semisynchronous ou comunicação síncrona.</span><span class="sxs-lookup"><span data-stu-id="f1bc3-191">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="f1bc3-192">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f1bc3-192">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1bc3-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1bc3-193">Requirements</span></span>



| <span data-ttu-id="f1bc3-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1bc3-194">Requirement</span></span> | <span data-ttu-id="f1bc3-195">Valor</span><span class="sxs-lookup"><span data-stu-id="f1bc3-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1bc3-196">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1bc3-196">Minimum supported client</span></span><br/> | <span data-ttu-id="f1bc3-197">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1bc3-197">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1bc3-198">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1bc3-198">Minimum supported server</span></span><br/> | <span data-ttu-id="f1bc3-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1bc3-199">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1bc3-200">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1bc3-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1bc3-201"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1bc3-201"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1bc3-202">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f1bc3-202">Type library</span></span><br/>             | <dl> <span data-ttu-id="f1bc3-203"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f1bc3-203"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f1bc3-204">DLL</span><span class="sxs-lookup"><span data-stu-id="f1bc3-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1bc3-205"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1bc3-205"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f1bc3-206">CLSID</span><span class="sxs-lookup"><span data-stu-id="f1bc3-206">CLSID</span></span><br/>                    | <span data-ttu-id="f1bc3-207">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="f1bc3-207">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="f1bc3-208">IID</span><span class="sxs-lookup"><span data-stu-id="f1bc3-208">IID</span></span><br/>                      | <span data-ttu-id="f1bc3-209">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="f1bc3-209">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="f1bc3-210">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1bc3-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1bc3-211">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="f1bc3-211">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="f1bc3-212">**SWbemObjectPath. Class**</span><span class="sxs-lookup"><span data-stu-id="f1bc3-212">**SWbemObjectPath.Class**</span></span>](swbemobjectpath-class.md)
</dt> <dt>

[<span data-ttu-id="f1bc3-213">**SWbemProperty**</span><span class="sxs-lookup"><span data-stu-id="f1bc3-213">**SWbemProperty**</span></span>](swbemproperty.md)
</dt> <dt>

[<span data-ttu-id="f1bc3-214">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="f1bc3-214">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

