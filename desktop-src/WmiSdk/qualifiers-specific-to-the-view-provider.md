---
description: O a seguir lista os qualificadores usam para definir as classes do provedor de exibição.
ms.assetid: 31a6af2d-33da-44f2-86d7-c467dd2f3e00
ms.tgt_platform: multiple
title: Qualificadores específicos para o provedor de exibição
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 76f28e4ba3433c168e1d0bf86887ee93df953444
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170887"
---
# <a name="qualifiers-specific-to-the-view-provider"></a><span data-ttu-id="cbbbd-103">Qualificadores específicos para o provedor de exibição</span><span class="sxs-lookup"><span data-stu-id="cbbbd-103">Qualifiers Specific to the View Provider</span></span>

<span data-ttu-id="cbbbd-104">O a seguir lista os qualificadores usam para definir as classes do provedor de exibição.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-104">The following lists the qualifiers use to define View Provider classes.</span></span>

> [!Note]  
> <span data-ttu-id="cbbbd-105">A classe View Provider dá suporte apenas a nomes NetBIOS ao usar referências remotas.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-105">The View provider class only supports NetBIOS names when using remote references.</span></span> <span data-ttu-id="cbbbd-106">Se você usar um endereço IP ou um nome DNS em uma referência remota, a conexão falhará com um erro 0x800706BA.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-106">If you use an IP address or a DNS name in a remote reference, then the connection fails with a 0x800706ba error.</span></span>

 

<dt>

<span data-ttu-id="cbbbd-107"><span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Encaminhe**</span><span class="sxs-lookup"><span data-stu-id="cbbbd-107"><span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Direct**</span></span>
</dt> <dd>

<span data-ttu-id="cbbbd-108">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cbbbd-108">Data type: **boolean**</span></span>

<span data-ttu-id="cbbbd-109">Usado com propriedades de associação de exibição para impedir que referências de associação sejam mapeadas para uma referência de exibição.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-109">Used with view association properties to prevent association references from being mapped to a view reference.</span></span>

<span data-ttu-id="cbbbd-110">O exemplo a seguir define a propriedade **GroupComponent** como uma referência de associação que não está mapeada na referência de exibição.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-110">The following example defines the property **GroupComponent** as an association reference that is not mapped in the view reference.</span></span>


```mof
[Direct, key, PropertySources
{"GroupComponent"}]
```



</dd> <dt>

<span data-ttu-id="cbbbd-111"><span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**</span><span class="sxs-lookup"><span data-stu-id="cbbbd-111"><span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**</span></span>
</dt> <dd>

<span data-ttu-id="cbbbd-112">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cbbbd-112">Data type: **boolean**</span></span>

<span data-ttu-id="cbbbd-113">Valor padrão para uma propriedade de classe de exibição baseada em uma propriedade de classe de origem com um valor padrão diferente.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-113">Default value for a view class property based on a source class property with a different default value.</span></span> <span data-ttu-id="cbbbd-114">A classe de origem subjacente é implícita pela exibição.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-114">The underlying source class is implied by the view.</span></span>

<span data-ttu-id="cbbbd-115">Por exemplo, a classe de origem [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) tem uma propriedade [booleana](boolean.md) **RunRepeatedly** que indica se o trabalho deve ser executado periodicamente ou apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-115">For example, the source class [**Win32\_ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) has a [boolean](boolean.md) property **RunRepeatedly** that indicates whether the job is to be carried out periodically or one time only.</span></span> <span data-ttu-id="cbbbd-116">O valor padrão de **RunRepeatedly** não é verdadeiro para o **Win32 \_ ScheduledJob**, mas é verdadeiro para a classe de exibição.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-116">The default value of **RunRepeatedly** is not True for **Win32\_ScheduledJob**, but is True for the view class.</span></span>


```mof
#pragma namespace("\\\\.\\root\\ns_view")
[Union,
ViewSources{"select * from Win32_ScheduledJob where RunRepeatedly=True"},
ViewSpaces{"\\\\.\\root\\cimv2"},
dynamic,provider("MS_VIEW_INSTANCE_PROVIDER")]
Class View_PeriodicJob
{
 [key, PropertySources{"JobId"}]
 uint32 JobId;
 [PropertySources{"Command"}]
 string Command;
 [HiddenDefault,PropertySources{"RunRepeatedly"}]
 boolean Repeat = True;
};
```



</dd> <dt>

<span data-ttu-id="cbbbd-117"><span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**Junção**</span><span class="sxs-lookup"><span data-stu-id="cbbbd-117"><span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**JoinOn**</span></span>
</dt> <dd>

<span data-ttu-id="cbbbd-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cbbbd-118">Data type: **string**</span></span>

<span data-ttu-id="cbbbd-119">Define como as instâncias de classe de origem são unidas em classes de exibição de junção.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-119">Defines how source class instances are joined in join view classes.</span></span> <span data-ttu-id="cbbbd-120">O exemplo a seguir mostra como usar o qualificador **Join** para unir duas classes de origem.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-120">The following example shows how to use the **JoinOn** qualifier to join two source classes.</span></span>


```mof
JoinOn("Win32Perf_RawProcess.IDProcess = Win32Perf_RawThread.IDProcess")
```



</dd> <dt>

<span data-ttu-id="cbbbd-121"><span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**Método**</span><span class="sxs-lookup"><span data-stu-id="cbbbd-121"><span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**MethodSource**</span></span>
</dt> <dd>

<span data-ttu-id="cbbbd-122">Tipo de dados: **matriz de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cbbbd-122">Data type: **string array**</span></span>

<span data-ttu-id="cbbbd-123">Método de origem a ser executado para o método de exibição.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-123">Source method to execute for the view method.</span></span> <span data-ttu-id="cbbbd-124">Para obter uma sintaxe semelhante, consulte [qualificador PropertySources](propertysources-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="cbbbd-124">For similar syntax, see [PropertySources Qualifier](propertysources-qualifier.md).</span></span> <span data-ttu-id="cbbbd-125">A assinatura do método deve corresponder exatamente à assinatura da classe de origem.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-125">The signature of the method must match the signature of the source class exactly.</span></span> <span data-ttu-id="cbbbd-126">Copie a assinatura do método do arquivo MOF que define a classe de origem.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-126">Copy the method signature from the MOF file that defines the source class.</span></span> <span data-ttu-id="cbbbd-127">O exemplo a seguir define um método do método [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) do [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="cbbbd-127">The example below defines a method from the [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) method of [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):</span></span>


```mof
[implemented, MethodSource
{"ClearEventlog"}]
  uint32   VClearEventlog([in] string ArchiveFileName);
```



<span data-ttu-id="cbbbd-128">Este qualificador só é válido quando é usado com exibições de União.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-128">This qualifier is only valid when it is used with union views.</span></span>

</dd> <dt>

<span data-ttu-id="cbbbd-129"><span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="cbbbd-129"><span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="cbbbd-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cbbbd-130">Data type: **string**</span></span>

<span data-ttu-id="cbbbd-131">Consulta WQL para filtrar instâncias depois que elas tiverem sido Unidas em uma classe de junção.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-131">WQL query to filter instances after they have been joined in a join class.</span></span>

</dd> <dt>

<span data-ttu-id="cbbbd-132"><span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="cbbbd-132"><span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="cbbbd-133">Tipo de dados: **matriz de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cbbbd-133">Data type: **string array**</span></span>

<span data-ttu-id="cbbbd-134">Propriedades de origem das quais uma propriedade de classe de exibição obtém dados.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-134">Source properties from which a view class property gets data.</span></span>

</dd> <dt>

<span data-ttu-id="cbbbd-135"><span id="Union"></span><span id="union"></span><span id="UNION"></span>**Unida**</span><span class="sxs-lookup"><span data-stu-id="cbbbd-135"><span id="Union"></span><span id="union"></span><span id="UNION"></span>**Union**</span></span>
</dt> <dd>

<span data-ttu-id="cbbbd-136">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cbbbd-136">Data type: **boolean**</span></span>

<span data-ttu-id="cbbbd-137">Indica se você está definindo uma classe Union.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-137">Indicates whether you are defining a union class.</span></span> <span data-ttu-id="cbbbd-138">As exibições de União contêm instâncias baseadas na União de instâncias de origem.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-138">Union views contain instances based on the union of source instances.</span></span> <span data-ttu-id="cbbbd-139">Por exemplo, você pode declarar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cbbbd-139">For example, you might declare the following:</span></span>


```mof
Union, ViewSources{"SELECT Handle, Name, CreationDate FROM Win32_Process", 
                   "SELECT Caption, Name, ProcessHandle FROM Win32_Thread"}.
```



</dd> <dt>

<span data-ttu-id="cbbbd-140"><span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="cbbbd-140"><span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="cbbbd-141">Tipo de dados: **matriz de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cbbbd-141">Data type: **string array**</span></span>

<span data-ttu-id="cbbbd-142">Conjunto de consultas de linguagem WQL (WQL) que definem as instâncias de origem e as propriedades usadas em uma classe de exibição específica.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-142">Set of WMI Query Language (WQL) queries that define the source instances and properties used in a specific view class.</span></span> <span data-ttu-id="cbbbd-143">A correspondência posicional de todos os qualificadores de matriz é importante.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-143">Positional correspondence of all the array qualifiers is important.</span></span>

</dd> <dt>

<span data-ttu-id="cbbbd-144"><span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="cbbbd-144"><span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="cbbbd-145">Tipo de dados: **matriz de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cbbbd-145">Data type: **string array**</span></span>

<span data-ttu-id="cbbbd-146">Namespaces em que as instâncias de origem estão localizadas.</span><span class="sxs-lookup"><span data-stu-id="cbbbd-146">Namespaces where the source instances are located.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cbbbd-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbbbd-147">Requirements</span></span>



| <span data-ttu-id="cbbbd-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbbbd-148">Requirement</span></span> | <span data-ttu-id="cbbbd-149">Valor</span><span class="sxs-lookup"><span data-stu-id="cbbbd-149">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="cbbbd-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbbbd-150">Minimum supported client</span></span><br/> | <span data-ttu-id="cbbbd-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbbbd-151">Windows Vista</span></span><br/>       |
| <span data-ttu-id="cbbbd-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbbbd-152">Minimum supported server</span></span><br/> | <span data-ttu-id="cbbbd-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbbbd-153">Windows Server 2008</span></span><br/> |



 

