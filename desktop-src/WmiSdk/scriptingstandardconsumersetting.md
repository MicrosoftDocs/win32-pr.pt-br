---
description: A classe singleton ScriptingStandardConsumerSetting fornece dados de registro que são comuns a todas as instâncias da classe consumidor padrão ActiveScriptEventConsumer.
ms.assetid: d217e058-3529-4173-b896-ebff3d7b05c6
ms.tgt_platform: multiple
title: Classe ScriptingStandardConsumerSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScriptingStandardConsumerSetting
- ScriptingStandardConsumerSetting.Caption
- ScriptingStandardConsumerSetting.Description
- ScriptingStandardConsumerSetting.MaximumScripts
- ScriptingStandardConsumerSetting.SettingID
- ScriptingStandardConsumerSetting.Timeout
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 43eae14eea445f546f731605c94b38e770b08691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165206"
---
# <a name="scriptingstandardconsumersetting-class"></a><span data-ttu-id="1bf14-103">Classe ScriptingStandardConsumerSetting</span><span class="sxs-lookup"><span data-stu-id="1bf14-103">ScriptingStandardConsumerSetting class</span></span>

<span data-ttu-id="1bf14-104">A classe singleton **ScriptingStandardConsumerSetting** fornece dados de registro que são comuns a todas as instâncias da classe consumidor padrão [**ActiveScriptEventConsumer**](activescripteventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="1bf14-104">The singleton **ScriptingStandardConsumerSetting** class provides registration data that is common to all instances of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) standard consumer class.</span></span> <span data-ttu-id="1bf14-105">Uma instância de **ActiveScriptEventConsumer** usa as propriedades **MaximumScripts** e **Timeout** .</span><span class="sxs-lookup"><span data-stu-id="1bf14-105">An **ActiveScriptEventConsumer** instance uses the **MaximumScripts** and **Timeout** properties.</span></span> <span data-ttu-id="1bf14-106">Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="1bf14-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="1bf14-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1bf14-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1bf14-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="1bf14-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bf14-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1bf14-109">Syntax</span></span>

``` syntax
[Singleton, AMENDMENT]
class ScriptingStandardConsumerSetting : CIM_Setting
{
  string Caption = "Scripting Standard Consumer Setting";
  string Description = "Registration data common to all instances of the Scripting Standard Consumer";
  uint32 MaximumScripts = 300;
  string SettingID = "ScriptingStandardConsumerSetting";
  uint32 Timeout = 0;
};
```

## <a name="members"></a><span data-ttu-id="1bf14-110">Membros</span><span class="sxs-lookup"><span data-stu-id="1bf14-110">Members</span></span>

<span data-ttu-id="1bf14-111">A classe **ScriptingStandardConsumerSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1bf14-111">The **ScriptingStandardConsumerSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="1bf14-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1bf14-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1bf14-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1bf14-113">Properties</span></span>

<span data-ttu-id="1bf14-114">A classe **ScriptingStandardConsumerSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1bf14-114">The **ScriptingStandardConsumerSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1bf14-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1bf14-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf14-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1bf14-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bf14-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1bf14-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bf14-118">Qualificadores: [**maxlen**](standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1bf14-118">Qualifiers: [**MaxLen**](standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1bf14-119">Uma breve descrição de um objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="1bf14-119">A short description of an object a one line string.</span></span> <span data-ttu-id="1bf14-120">Contém a cadeia de caracteres **ScriptingStandardConsumerSetting** porque esta é uma classe singleton.</span><span class="sxs-lookup"><span data-stu-id="1bf14-120">Contains the string **ScriptingStandardConsumerSetting** because this is a singleton class.</span></span>

</dd> <dt>

<span data-ttu-id="1bf14-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1bf14-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf14-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1bf14-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bf14-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1bf14-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bf14-124">Uma descrição de texto de um objeto.</span><span class="sxs-lookup"><span data-stu-id="1bf14-124">A text description of an object.</span></span>

</dd> <dt>

<span data-ttu-id="1bf14-125">**MaximumScripts**</span><span class="sxs-lookup"><span data-stu-id="1bf14-125">**MaximumScripts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf14-126">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1bf14-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1bf14-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1bf14-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1bf14-128">Número máximo de scripts que são executados antes que um consumidor inicie uma nova instância.</span><span class="sxs-lookup"><span data-stu-id="1bf14-128">Maximum number of scripts that are run before a consumer starts a new instance.</span></span> <span data-ttu-id="1bf14-129">Para limpar os vazamentos de memória de scripts, desligue o consumidor regularmente.</span><span class="sxs-lookup"><span data-stu-id="1bf14-129">To clear out memory leaks from scripts, shut down the consumer regularly.</span></span> <span data-ttu-id="1bf14-130">O valor padrão é 300.</span><span class="sxs-lookup"><span data-stu-id="1bf14-130">The default value is 300.</span></span>

</dd> <dt>

<span data-ttu-id="1bf14-131">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="1bf14-131">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf14-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1bf14-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bf14-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1bf14-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bf14-134">Qualificadores: [**maxlen**](standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="1bf14-134">Qualifiers: [**MaxLen**](standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1bf14-135">Identificador para o objeto de configuração.</span><span class="sxs-lookup"><span data-stu-id="1bf14-135">Identifier for the setting object.</span></span>

</dd> <dt>

<span data-ttu-id="1bf14-136">**Tempo Limite**</span><span class="sxs-lookup"><span data-stu-id="1bf14-136">**Timeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf14-137">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1bf14-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1bf14-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1bf14-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1bf14-139">Qualificadores: [**unidades**](standard-qualifiers.md) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="1bf14-139">Qualifiers: [**units**](standard-qualifiers.md) ("Minutes")</span></span>
</dt> </dl>

<span data-ttu-id="1bf14-140">Número máximo de minutos antes que um consumidor inicie uma nova instância.</span><span class="sxs-lookup"><span data-stu-id="1bf14-140">Maximum number of minutes before a consumer starts a new instance.</span></span> <span data-ttu-id="1bf14-141">Se for 0 (zero), a propriedade **MaximumScripts** controlará o tempo de vida do consumidor.</span><span class="sxs-lookup"><span data-stu-id="1bf14-141">If 0 (zero), the **MaximumScripts** property controls the consumer lifetime.</span></span> <span data-ttu-id="1bf14-142">O intervalo válido para **Timeout** é de 0 a 71.000 e o valor padrão é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="1bf14-142">The valid range for **Timeout** is 0 through 71,000 and the default value is 0 (zero).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1bf14-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bf14-143">Remarks</span></span>

<span data-ttu-id="1bf14-144">A única instância da classe **ScriptingStandardConsumerSetting** reside no \\ namespace raiz cimv2.</span><span class="sxs-lookup"><span data-stu-id="1bf14-144">The single instance of the **ScriptingStandardConsumerSetting** class resides in the root\\cimv2 namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bf14-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bf14-145">Requirements</span></span>



| <span data-ttu-id="1bf14-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bf14-146">Requirement</span></span> | <span data-ttu-id="1bf14-147">Valor</span><span class="sxs-lookup"><span data-stu-id="1bf14-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bf14-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bf14-148">Minimum supported client</span></span><br/> | <span data-ttu-id="1bf14-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1bf14-149">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1bf14-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bf14-150">Minimum supported server</span></span><br/> | <span data-ttu-id="1bf14-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1bf14-151">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1bf14-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="1bf14-152">Namespace</span></span><br/>                | <span data-ttu-id="1bf14-153">\\Assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="1bf14-153">Root\\subscription</span></span><br/>                                                          |
| <span data-ttu-id="1bf14-154">MOF</span><span class="sxs-lookup"><span data-stu-id="1bf14-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bf14-155"><dt>Scrcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1bf14-155"><dt>Scrcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bf14-156">DLL</span><span class="sxs-lookup"><span data-stu-id="1bf14-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bf14-157"><dt>Scrcons.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1bf14-157"><dt>Scrcons.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bf14-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bf14-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bf14-159">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="1bf14-159">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> <dt>

[<span data-ttu-id="1bf14-160">Classes de consumidor padrão</span><span class="sxs-lookup"><span data-stu-id="1bf14-160">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="1bf14-161">Executando um script com base em um evento</span><span class="sxs-lookup"><span data-stu-id="1bf14-161">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="1bf14-162">Criando um consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="1bf14-162">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="1bf14-163">Recebendo eventos em todos os momentos</span><span class="sxs-lookup"><span data-stu-id="1bf14-163">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="1bf14-164">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="1bf14-164">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

