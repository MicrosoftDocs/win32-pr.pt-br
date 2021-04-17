---
description: Executa um script predefinido em uma linguagem de script arbitrária quando um evento é entregue a ele.
ms.assetid: 2c0aa216-4255-49ff-9bbd-d6c62b5b9139
ms.tgt_platform: multiple
title: Classe ActiveScriptEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActiveScriptEventConsumer
- ActiveScriptEventConsumer.CreatorSID
- ActiveScriptEventConsumer.KillTimeout
- ActiveScriptEventConsumer.MachineName
- ActiveScriptEventConsumer.MaximumQueueSize
- ActiveScriptEventConsumer.Name
- ActiveScriptEventConsumer.ScriptingEngine
- ActiveScriptEventConsumer.ScriptFileName
- ActiveScriptEventConsumer.ScriptText
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 11e2886fd5d0804946433e102e24617df768dcec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811971"
---
# <a name="activescripteventconsumer-class"></a><span data-ttu-id="58721-103">Classe ActiveScriptEventConsumer</span><span class="sxs-lookup"><span data-stu-id="58721-103">ActiveScriptEventConsumer class</span></span>

<span data-ttu-id="58721-104">A classe **ActiveScriptEventConsumer** executa um script predefinido em uma linguagem de script arbitrária quando um evento é entregue a ele.</span><span class="sxs-lookup"><span data-stu-id="58721-104">The **ActiveScriptEventConsumer** class runs a predefined script in an arbitrary scripting language when an event is delivered to it.</span></span> <span data-ttu-id="58721-105">Essa classe é um dos consumidores de eventos padrão que o WMI fornece.</span><span class="sxs-lookup"><span data-stu-id="58721-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="58721-106">Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="58721-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>


```cmd
Mofcomp -n:root\<namespace> scrcons.mof
```



<span data-ttu-id="58721-107">Você pode configurar o desempenho de todas as instâncias do **ActiveScriptEventConsumer** em um sistema definindo os valores da propriedade [**Timeout**](scriptingstandardconsumersetting.md) ou **MaximumScripts** na instância única de **ScriptingStandardConsumerSetting**.</span><span class="sxs-lookup"><span data-stu-id="58721-107">You can configure the performance of all instances of **ActiveScriptEventConsumer** on a system by setting the values of either the [**Timeout**](scriptingstandardconsumersetting.md) or **MaximumScripts** property in the single instance of **ScriptingStandardConsumerSetting**.</span></span>

## <a name="syntax"></a><span data-ttu-id="58721-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58721-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class ActiveScriptEventConsumer : __EventConsumer
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  uint32 KillTimeout = 0;
  string MachineName;
  uint32 MaximumQueueSize;
  string Name;
  string ScriptingEngine;
  string ScriptFileName;
  string ScriptText;
};
```

## <a name="members"></a><span data-ttu-id="58721-109">Membros</span><span class="sxs-lookup"><span data-stu-id="58721-109">Members</span></span>

<span data-ttu-id="58721-110">A classe **ActiveScriptEventConsumer** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="58721-110">The **ActiveScriptEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="58721-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="58721-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58721-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="58721-112">Properties</span></span>

<span data-ttu-id="58721-113">A classe **ActiveScriptEventConsumer** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="58721-113">The **ActiveScriptEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58721-114">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="58721-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58721-115">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="58721-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="58721-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58721-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58721-117">Matriz que representa o identificador de segurança (SID), que identifica exclusivamente o criador do consumidor de evento de script ativo.</span><span class="sxs-lookup"><span data-stu-id="58721-117">Array that represents the security identifier (SID), which uniquely identifies the creator of the Active Script Event consumer.</span></span> <span data-ttu-id="58721-118">Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="58721-118">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="58721-119">**KillTimeout**</span><span class="sxs-lookup"><span data-stu-id="58721-119">**KillTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58721-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58721-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58721-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58721-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58721-122">Número, em segundos, que o script tem permissão para ser executado.</span><span class="sxs-lookup"><span data-stu-id="58721-122">Number, in seconds, that the script is allowed to run.</span></span> <span data-ttu-id="58721-123">Se 0 (zero), que é o padrão, o script não será encerrado.</span><span class="sxs-lookup"><span data-stu-id="58721-123">If 0 (zero), which is the default, the script is not terminated.</span></span>

</dd> <dt>

<span data-ttu-id="58721-124">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="58721-124">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58721-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58721-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58721-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58721-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58721-127">Nome do computador para o qual o WMI envia eventos.</span><span class="sxs-lookup"><span data-stu-id="58721-127">Name of the computer to which WMI sends events.</span></span> <span data-ttu-id="58721-128">Por convenção de consumidores padrão da Microsoft, o consumidor de scripts não pode ser executado remotamente.</span><span class="sxs-lookup"><span data-stu-id="58721-128">By convention of Microsoft standard consumers, the script consumer cannot be run remotely.</span></span> <span data-ttu-id="58721-129">Os consumidores de terceiros também podem usar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="58721-129">Third-party consumers can also use this property.</span></span> <span data-ttu-id="58721-130">Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="58721-130">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="58721-131">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="58721-131">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58721-132">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58721-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58721-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58721-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58721-134">Máximo de fila, em bytes, para o consumidor de evento de script ativo.</span><span class="sxs-lookup"><span data-stu-id="58721-134">Maximum queue, in bytes, for the Active Script Event consumer.</span></span> <span data-ttu-id="58721-135">Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="58721-135">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="58721-136">**Nome**</span><span class="sxs-lookup"><span data-stu-id="58721-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58721-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58721-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58721-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="58721-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="58721-139">Qualificadores: [ **chave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="58721-139">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="58721-140">Identificador exclusivo para o consumidor do evento.</span><span class="sxs-lookup"><span data-stu-id="58721-140">Unique identifier for the event consumer.</span></span> <span data-ttu-id="58721-141">Se você renomear o consumidor, o resultado será dois consumidores iguais que têm nomes diferentes.</span><span class="sxs-lookup"><span data-stu-id="58721-141">If you rename the consumer, the result is two equal consumers that have different names.</span></span>

</dd> <dt>

<span data-ttu-id="58721-142">**ScriptFileName**</span><span class="sxs-lookup"><span data-stu-id="58721-142">**ScriptFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58721-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58721-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58721-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58721-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58721-145">Nome do arquivo do qual o texto do script é lido, pretendido como uma alternativa para especificar o texto do script na propriedade **ScriptText** .</span><span class="sxs-lookup"><span data-stu-id="58721-145">Name of the file from which the script text is read, intended as an alternative to specifying the text of the script in the **ScriptText** property.</span></span> <span data-ttu-id="58721-146">Essa propriedade deverá ser **nula** se a propriedade **ScriptText** não for **nula**.</span><span class="sxs-lookup"><span data-stu-id="58721-146">This property must be **NULL** if the **ScriptText** property is not **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="58721-147">Quando você especifica o **ScriptFileName**, é importante proteger o executável que você está iniciando.</span><span class="sxs-lookup"><span data-stu-id="58721-147">When you specify the **ScriptFileName**, it is important to secure the executable that you are launching.</span></span> <span data-ttu-id="58721-148">Se o executável não estiver em um local seguro ou protegido com uma ACL (lista de controle de acesso) forte, qualquer pessoa poderá substituir o executável por um diferente.</span><span class="sxs-lookup"><span data-stu-id="58721-148">If the executable is not in a secure location or secured with a strong access control list (ACL), anyone can replace the executable with a different one.</span></span> <span data-ttu-id="58721-149">Para obter mais informações sobre ACLs, consulte [criando um descritor de segurança (SD) para um novo objeto em C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="58721-149">For more information about ACLs, see [Creating a Security Descriptor (SD) for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="58721-150">**ScriptingEngine**</span><span class="sxs-lookup"><span data-stu-id="58721-150">**ScriptingEngine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58721-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58721-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58721-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58721-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58721-153">Nome do mecanismo de script a ser usado, por exemplo, "VBScript".</span><span class="sxs-lookup"><span data-stu-id="58721-153">Name of the scripting engine to use, for example, "VBScript".</span></span> <span data-ttu-id="58721-154">Esta propriedade não pode ser **nula**.</span><span class="sxs-lookup"><span data-stu-id="58721-154">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="58721-155">**ScriptText**</span><span class="sxs-lookup"><span data-stu-id="58721-155">**ScriptText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58721-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58721-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58721-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58721-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58721-158">Texto do script expresso em uma linguagem conhecida pelo mecanismo de script.</span><span class="sxs-lookup"><span data-stu-id="58721-158">Text of the script that is expressed in a language known to the scripting engine.</span></span> <span data-ttu-id="58721-159">Essa propriedade deverá ser **nula** se a propriedade **ScriptFileName** não for **nula**.</span><span class="sxs-lookup"><span data-stu-id="58721-159">This property must be **NULL** if the **ScriptFileName** property is not **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58721-160">Comentários</span><span class="sxs-lookup"><span data-stu-id="58721-160">Remarks</span></span>

<span data-ttu-id="58721-161">Essa classe é derivada da classe abstrata [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="58721-161">This class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span> <span data-ttu-id="58721-162">Ele está localizado no namespace da \\ assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="58721-162">It is located in the root\\subscription namespace.</span></span>

<span data-ttu-id="58721-163">Quando o texto de um script é especificado na instância do consumidor de eventos, o script tem acesso à instância de evento na variável de ambiente de script **TargetEvent**.</span><span class="sxs-lookup"><span data-stu-id="58721-163">When the text of a script is specified in the event consumer instance, the script has access to the event instance in the script environment variable **TargetEvent**.</span></span>

<span data-ttu-id="58721-164">Os scripts são executados no contexto de segurança LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="58721-164">The scripts run in the LocalSystem security context.</span></span> <span data-ttu-id="58721-165">Como medida de segurança, somente um administrador do sistema local ou um administrador de domínio pode configurar o consumidor de scripts.</span><span class="sxs-lookup"><span data-stu-id="58721-165">As a security measure, only a local system administrator or a domain administrator can configure the scripting consumer.</span></span> <span data-ttu-id="58721-166">Os direitos de acesso não são verificados até o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="58721-166">Access rights are not checked until run time.</span></span> <span data-ttu-id="58721-167">Depois que o consumidor é configurado, qualquer usuário pode disparar o evento que faz o script.</span><span class="sxs-lookup"><span data-stu-id="58721-167">After the consumer is configured, any user can trigger the event that causes the script to .</span></span>

<span data-ttu-id="58721-168">A falha ao carregar o mecanismo de script ou a análise e validação do script é considerada uma falha.</span><span class="sxs-lookup"><span data-stu-id="58721-168">Failure to load the scripting engine or parse and validate the script is considered a failure.</span></span> <span data-ttu-id="58721-169">Os códigos de retorno de erro do script e o encerramento do script usando um tempo limite também são considerados falhas.</span><span class="sxs-lookup"><span data-stu-id="58721-169">Error return codes from the script and terminating the script by using a time-out are also considered failures.</span></span>

<span data-ttu-id="58721-170">O **ScriptText** ou o **ScriptFileName** não deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="58721-170">Either **ScriptText** or **ScriptFileName** must be not **NULL**.</span></span> <span data-ttu-id="58721-171">Se ambas as propriedades forem **nulas** ou não **nulas**, um erro será gerado.</span><span class="sxs-lookup"><span data-stu-id="58721-171">If both properties are **NULL** or not **NULL**, an error is generated.</span></span>

<span data-ttu-id="58721-172">Quando o WMI é executado como um serviço, os scripts executados por **ActiveScriptEventConsumer** não geram a saída da tela.</span><span class="sxs-lookup"><span data-stu-id="58721-172">When WMI is run as a service, scripts run by **ActiveScriptEventConsumer** do not generate screen output.</span></span> <span data-ttu-id="58721-173">Scripts que usam **MsgBox** são executados, mas não exibem informações na tela.</span><span class="sxs-lookup"><span data-stu-id="58721-173">Scripts that use **MsgBox** do run, but they do not display information on the screen.</span></span> <span data-ttu-id="58721-174">Não há suporte para a execução do serviço WMI como um arquivo executável, mas o WMI permite que os scripts que usam a função **MsgBox** exibam a saída ou aceitem a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="58721-174">Running the WMI service as an executable file is not supported, but WMI allows scripts that use the **MsgBox** function to display output or accept user input.</span></span> <span data-ttu-id="58721-175">Nenhum dos métodos fornecidos pelo objeto [WScript](/previous-versions//at5ydy31(v=vs.85)) pode ser usado porque **ActiveScriptEventConsumer** não usa o WSH (Windows Script Host).</span><span class="sxs-lookup"><span data-stu-id="58721-175">None of the methods provided by the [WScript](/previous-versions//at5ydy31(v=vs.85)) object can be used because **ActiveScriptEventConsumer** does not use Windows Script Host (WSH).</span></span>

## <a name="examples"></a><span data-ttu-id="58721-176">Exemplos</span><span class="sxs-lookup"><span data-stu-id="58721-176">Examples</span></span>

<span data-ttu-id="58721-177">O exemplo de [criar registro de evento WMI permanente para monitorar arquivos](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) no PowerShell na galeria do TechNet usa **ActiveScriptEventConsumer** como parte de um script complexo para configurar um registro de evento do WMI permanente.</span><span class="sxs-lookup"><span data-stu-id="58721-177">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **ActiveScriptEventConsumer** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="58721-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58721-178">Requirements</span></span>



| <span data-ttu-id="58721-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="58721-179">Requirement</span></span> | <span data-ttu-id="58721-180">Valor</span><span class="sxs-lookup"><span data-stu-id="58721-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58721-181">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58721-181">Minimum supported client</span></span><br/> | <span data-ttu-id="58721-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58721-182">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="58721-183">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58721-183">Minimum supported server</span></span><br/> | <span data-ttu-id="58721-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58721-184">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="58721-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="58721-185">Namespace</span></span><br/>                | <span data-ttu-id="58721-186">\\Assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="58721-186">Root\\subscription</span></span><br/>                                                          |
| <span data-ttu-id="58721-187">MOF</span><span class="sxs-lookup"><span data-stu-id="58721-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58721-188"><dt>Scrcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58721-188"><dt>Scrcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="58721-189">DLL</span><span class="sxs-lookup"><span data-stu-id="58721-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58721-190"><dt>Scrcons.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58721-190"><dt>Scrcons.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58721-191">Confira também</span><span class="sxs-lookup"><span data-stu-id="58721-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58721-192">Classes de consumidor padrão</span><span class="sxs-lookup"><span data-stu-id="58721-192">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="58721-193">Executando um script com base em um evento</span><span class="sxs-lookup"><span data-stu-id="58721-193">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="58721-194">Recebendo eventos em todos os momentos</span><span class="sxs-lookup"><span data-stu-id="58721-194">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="58721-195">Criando um consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="58721-195">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="58721-196">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="58721-196">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> <dt>

[<span data-ttu-id="58721-197">**ScriptingStandardConsumerSetting**</span><span class="sxs-lookup"><span data-stu-id="58721-197">**ScriptingStandardConsumerSetting**</span></span>](scriptingstandardconsumersetting.md)
</dt> </dl>

 

