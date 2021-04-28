---
description: Método SWbemServices. AssociatorsOfAsync – retorna uma coleção de objetos (classes ou instâncias) chamadas de pontos de extremidade que estão associados a um objeto especificado.
ms.assetid: 3969d90f-d39c-40f1-9328-fc1afbaa53b1
ms.tgt_platform: multiple
title: Método SWbemServices. AssociatorsOfAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4b16eed97c891b4b4f5bd283496868d99f9e0fbc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103664"
---
# <a name="swbemservicesassociatorsofasync-method"></a><span data-ttu-id="f0a88-103">Método SWbemServices. AssociatorsOfAsync</span><span class="sxs-lookup"><span data-stu-id="f0a88-103">SWbemServices.AssociatorsOfAsync method</span></span>

<span data-ttu-id="f0a88-104">O método **AssociatorsOfAsync** do objeto [**SWbemServices**](swbemservices.md) retorna uma coleção de objetos (classes ou instâncias) chamada pontos de extremidade que estão associados a um objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="f0a88-104">The **AssociatorsOfAsync** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="f0a88-105">A chamada para **AssociatorsOfAsync** retorna imediatamente, e os resultados e o status são retornados para o chamador por meio de eventos entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="f0a88-105">The call to **AssociatorsOfAsync** returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="f0a88-106">Para lidar com cada objeto retornado, crie um *objWbemSink*. Manipulador de eventos [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a88-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event handler.</span></span>

<span data-ttu-id="f0a88-107">Depois que todos os objetos chegarem, o processamento será feito no *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a88-107">After all the objects arrive, processing is done in the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span> <span data-ttu-id="f0a88-108">Esse método executa a mesma função que os ASSOCIAdores da consulta WQL executam.</span><span class="sxs-lookup"><span data-stu-id="f0a88-108">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span> <span data-ttu-id="f0a88-109">Para obter mais informações sobre como criar um coletor, consulte [recebendo um evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="f0a88-109">For more information about creating a sink, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="f0a88-110">O método é chamado no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="f0a88-110">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="f0a88-111">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f0a88-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="f0a88-112">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f0a88-112">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0a88-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0a88-113">Syntax</span></span>


```VB
SWbemServices.AssociatorsOfAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f0a88-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0a88-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0a88-115">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="f0a88-115">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="f0a88-116">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="f0a88-116">Required.</span></span> <span data-ttu-id="f0a88-117">Coletor de objeto que recebe os objetos de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f0a88-117">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="f0a88-118">Crie um objeto [**SWbemSink**](swbemsink.md) para receber os objetos.</span><span class="sxs-lookup"><span data-stu-id="f0a88-118">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="f0a88-119">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="f0a88-119">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="f0a88-120">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="f0a88-120">Required.</span></span> <span data-ttu-id="f0a88-121">Cadeia de caracteres que contém o caminho do objeto da classe ou instância de origem.</span><span class="sxs-lookup"><span data-stu-id="f0a88-121">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="f0a88-122">Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="f0a88-122">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0a88-123">*strAssocClass* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="f0a88-123">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a88-124">Cadeia de caracteres que contém uma classe de associação.</span><span class="sxs-lookup"><span data-stu-id="f0a88-124">String that contains an association class.</span></span> <span data-ttu-id="f0a88-125">Quando especificado, esse parâmetro indica que os pontos de extremidade retornados devem ser associados à origem por meio da classe de associação especificada ou de uma classe derivada dessa classe de associação.</span><span class="sxs-lookup"><span data-stu-id="f0a88-125">When specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="f0a88-126">*strResultClass* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="f0a88-126">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a88-127">Cadeia de caracteres que contém um nome de classe.</span><span class="sxs-lookup"><span data-stu-id="f0a88-127">String that contains a class name.</span></span> <span data-ttu-id="f0a88-128">Se especificado, esse parâmetro opcional indica que os pontos de extremidade retornados devem pertencer ou ser derivados da classe especificada nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f0a88-128">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f0a88-129">*strResultRole* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="f0a88-129">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a88-130">Cadeia de caracteres que contém um nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f0a88-130">String that contains a property name.</span></span> <span data-ttu-id="f0a88-131">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem reproduzir uma função específica em sua associação com o objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="f0a88-131">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="f0a88-132">A função é definida pelo nome de uma propriedade especificada (que deve ser uma propriedade de referência) de uma associação.</span><span class="sxs-lookup"><span data-stu-id="f0a88-132">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="f0a88-133">*strRole* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="f0a88-133">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a88-134">Cadeia de caracteres que contém um nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f0a88-134">String that contains a property name.</span></span> <span data-ttu-id="f0a88-135">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem participar de uma associação com o objeto de origem no qual o objeto de origem desempenha uma função específica.</span><span class="sxs-lookup"><span data-stu-id="f0a88-135">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="f0a88-136">A função é definida pelo nome de uma propriedade especificada (que deve ser uma propriedade de referência) de uma associação.</span><span class="sxs-lookup"><span data-stu-id="f0a88-136">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="f0a88-137">*bClassesOnly* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="f0a88-137">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a88-138">Valor booliano que indica se uma lista de nomes de classe deve ser retornada em vez de instâncias reais das classes.</span><span class="sxs-lookup"><span data-stu-id="f0a88-138">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="f0a88-139">Essas são as classes às quais as instâncias de ponto de extremidade pertencem.</span><span class="sxs-lookup"><span data-stu-id="f0a88-139">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="f0a88-140">O valor padrão para esse parâmetro é **false**.</span><span class="sxs-lookup"><span data-stu-id="f0a88-140">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="f0a88-141">*bSchemaOnly* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="f0a88-141">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a88-142">Valor booliano que indica se a consulta se aplica ao esquema em vez dos dados.</span><span class="sxs-lookup"><span data-stu-id="f0a88-142">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="f0a88-143">O valor padrão para esse parâmetro é **false**.</span><span class="sxs-lookup"><span data-stu-id="f0a88-143">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="f0a88-144">Ele só poderá ser definido como **true** se o parâmetro *strObjectPath* especificar o caminho do objeto de uma classe.</span><span class="sxs-lookup"><span data-stu-id="f0a88-144">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="f0a88-145">Quando definido como **true**, o conjunto de pontos de extremidade retornados representa classes que são adequadamente associadas à classe de origem no esquema.</span><span class="sxs-lookup"><span data-stu-id="f0a88-145">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="f0a88-146">*strRequiredAssocQualifier* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="f0a88-146">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a88-147">Cadeia de caracteres que contém um nome de qualificador.</span><span class="sxs-lookup"><span data-stu-id="f0a88-147">String that contains a qualifier name.</span></span> <span data-ttu-id="f0a88-148">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem ser associados ao objeto de origem por meio de uma classe de associação que inclui o qualificador especificado.</span><span class="sxs-lookup"><span data-stu-id="f0a88-148">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="f0a88-149">*strRequiredQualifier* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="f0a88-149">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a88-150">Cadeia de caracteres que contém um nome de qualificador.</span><span class="sxs-lookup"><span data-stu-id="f0a88-150">String that contains a qualifier name.</span></span> <span data-ttu-id="f0a88-151">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem incluir o qualificador especificado.</span><span class="sxs-lookup"><span data-stu-id="f0a88-151">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="f0a88-152">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="f0a88-152">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a88-153">Inteiro que especifica os sinalizadores adicionais para a operação.</span><span class="sxs-lookup"><span data-stu-id="f0a88-153">Integer that specifies the additional flags to the operation.</span></span> <span data-ttu-id="f0a88-154">O padrão para esse parâmetro é **wbemFlagDontSendStatus**.</span><span class="sxs-lookup"><span data-stu-id="f0a88-154">The default for this parameter is **wbemFlagDontSendStatus**.</span></span> <span data-ttu-id="f0a88-155">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f0a88-155">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="f0a88-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="f0a88-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="f0a88-157">Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="f0a88-157">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="f0a88-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="f0a88-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f0a88-159">Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="f0a88-159">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="f0a88-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="f0a88-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="f0a88-161">Faz com que o WMI retorne dados de alteração de classe junto com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="f0a88-161">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="f0a88-162">Para obter mais informações sobre qualificadores corrigidos, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="f0a88-162">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f0a88-163">*objWbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="f0a88-163">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a88-164">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="f0a88-164">Typically, this is undefined.</span></span> <span data-ttu-id="f0a88-165">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="f0a88-165">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="f0a88-166">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="f0a88-166">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="f0a88-167">*objWbemAsyncContext* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="f0a88-167">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a88-168">Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="f0a88-168">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="f0a88-169">Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="f0a88-169">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="f0a88-170">Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="f0a88-170">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="f0a88-171">Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a88-171">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="f0a88-172">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f0a88-172">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0a88-173">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f0a88-173">Return value</span></span>

<span data-ttu-id="f0a88-174">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f0a88-174">This method does not return a value.</span></span> <span data-ttu-id="f0a88-175">Se for bem-sucedido, o coletor receberá um evento [**OnObjectReady**](swbemsink-onobjectready.md) por instância.</span><span class="sxs-lookup"><span data-stu-id="f0a88-175">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="f0a88-176">Após a última instância, o coletor de objeto recebe um evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a88-176">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f0a88-177">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f0a88-177">Error codes</span></span>

<span data-ttu-id="f0a88-178">Após a conclusão do método **AssociatorsOfAsync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="f0a88-178">After the completion of the **AssociatorsOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="f0a88-179">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="f0a88-179">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="f0a88-180">O usuário atual não tem permissão para exibir uma ou mais das classes retornadas pela chamada.</span><span class="sxs-lookup"><span data-stu-id="f0a88-180">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="f0a88-181">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="f0a88-181">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f0a88-182">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="f0a88-182">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="f0a88-183">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="f0a88-183">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="f0a88-184">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="f0a88-184">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="f0a88-185">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="f0a88-185">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="f0a88-186">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="f0a88-186">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f0a88-187">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="f0a88-187">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="f0a88-188">O item solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="f0a88-188">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0a88-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0a88-189">Remarks</span></span>

<span data-ttu-id="f0a88-190">Essa chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f0a88-190">This call returns immediately.</span></span> <span data-ttu-id="f0a88-191">Os objetos e status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="f0a88-191">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="f0a88-192">Para processar cada objeto quando ele retornar, crie um *objWbemSink*. Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a88-192">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="f0a88-193">Depois que todos os objetos forem retornados, você poderá executar o processamento final em sua implementação do *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a88-193">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="f0a88-194">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="f0a88-194">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="f0a88-195">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f0a88-195">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="f0a88-196">Para eliminar os riscos, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="f0a88-196">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="f0a88-197">Use o parâmetro *objWbemAsyncContext* em scripts para verificar a origem de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="f0a88-197">Use the *objWbemAsyncContext* parameter in scripts to verify the source of a call.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0a88-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0a88-198">Requirements</span></span>



| <span data-ttu-id="f0a88-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0a88-199">Requirement</span></span> | <span data-ttu-id="f0a88-200">Valor</span><span class="sxs-lookup"><span data-stu-id="f0a88-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a88-201">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0a88-201">Minimum supported client</span></span><br/> | <span data-ttu-id="f0a88-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0a88-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f0a88-203">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0a88-203">Minimum supported server</span></span><br/> | <span data-ttu-id="f0a88-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0a88-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f0a88-205">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0a88-205">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0a88-206"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0a88-206"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0a88-207">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f0a88-207">Type library</span></span><br/>             | <dl> <span data-ttu-id="f0a88-208"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f0a88-208"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f0a88-209">DLL</span><span class="sxs-lookup"><span data-stu-id="f0a88-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0a88-210"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0a88-210"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f0a88-211">CLSID</span><span class="sxs-lookup"><span data-stu-id="f0a88-211">CLSID</span></span><br/>                    | <span data-ttu-id="f0a88-212">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="f0a88-212">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="f0a88-213">IID</span><span class="sxs-lookup"><span data-stu-id="f0a88-213">IID</span></span><br/>                      | <span data-ttu-id="f0a88-214">ISWbemServices de IID \_</span><span class="sxs-lookup"><span data-stu-id="f0a88-214">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="f0a88-215">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f0a88-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0a88-216">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="f0a88-216">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="f0a88-217">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="f0a88-217">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="f0a88-218">**SWbemObject. AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="f0a88-218">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="f0a88-219">**SWbemObject. referências\_**</span><span class="sxs-lookup"><span data-stu-id="f0a88-219">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="f0a88-220">**SWbemObject. ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="f0a88-220">**SWbemObject.ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)
</dt> <dt>

[<span data-ttu-id="f0a88-221">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="f0a88-221">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> <dt>

[<span data-ttu-id="f0a88-222">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="f0a88-222">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)
</dt> </dl>

 

