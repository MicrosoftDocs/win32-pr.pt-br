---
description: A classe CommandLineEventConsumer inicia um processo arbitrário no sistema local quando um evento é entregue a ele.
ms.assetid: 0dcae783-1722-45a4-b5d4-3fcf455dacf8
ms.tgt_platform: multiple
title: Classe CommandLineEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommandLineEventConsumer
- CommandLineEventConsumer.CreatorSID
- CommandLineEventConsumer.MachineName
- CommandLineEventConsumer.MaximumQueueSize
- CommandLineEventConsumer.CommandLineTemplate
- CommandLineEventConsumer.CreateNewConsole
- CommandLineEventConsumer.CreateNewProcessGroup
- CommandLineEventConsumer.CreateSeparateWowVdm
- CommandLineEventConsumer.CreateSharedWowVdm
- CommandLineEventConsumer.DesktopName
- CommandLineEventConsumer.ExecutablePath
- CommandLineEventConsumer.FillAttributes
- CommandLineEventConsumer.ForceOffFeedback
- CommandLineEventConsumer.ForceOnFeedback
- CommandLineEventConsumer.KillTimeout
- CommandLineEventConsumer.Name
- CommandLineEventConsumer.Priority
- CommandLineEventConsumer.RunInteractively
- CommandLineEventConsumer.ShowWindowCommand
- CommandLineEventConsumer.UseDefaultErrorMode
- CommandLineEventConsumer.WindowTitle
- CommandLineEventConsumer.WorkingDirectory
- CommandLineEventConsumer.XCoordinate
- CommandLineEventConsumer.XNumCharacters
- CommandLineEventConsumer.XSize
- CommandLineEventConsumer.YCoordinate
- CommandLineEventConsumer.YNumCharacters
- CommandLineEventConsumer.YSize
- CommandLineEventConsumer.FillAttribute
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 1784ba116417f6ed94aed2249a797cf8de4b3527
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187935"
---
# <a name="commandlineeventconsumer-class"></a><span data-ttu-id="9cbfb-103">Classe CommandLineEventConsumer</span><span class="sxs-lookup"><span data-stu-id="9cbfb-103">CommandLineEventConsumer class</span></span>

<span data-ttu-id="9cbfb-104">A classe **CommandLineEventConsumer** inicia um processo arbitrário no sistema local quando um evento é entregue a ele.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-104">The **CommandLineEventConsumer** class starts an arbitrary process in the local system when an event is delivered to it.</span></span> <span data-ttu-id="9cbfb-105">Essa classe é um dos consumidores de eventos padrão que o WMI fornece.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="9cbfb-106">Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="9cbfb-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

> [!Note]  
> <span data-ttu-id="9cbfb-107">Ao usar a classe **CommandLineEventConsumer** , proteja o executável que você deseja iniciar.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-107">When using the **CommandLineEventConsumer** class, secure the executable that you want to start.</span></span> <span data-ttu-id="9cbfb-108">Se o executável não estiver em um local seguro, ou protegido com uma ACL (lista de controle de acesso) forte, um usuário não autorizado poderá substituir seu executável por um executável mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-108">If the executable is not in a secure location, or secured with a strong access control list (ACL), an unauthorized user can replace your executable with a malicious executable.</span></span> <span data-ttu-id="9cbfb-109">Para obter mais informações sobre ACLs, visite a seção segurança do SDK (Software Development Kit) do Microsoft Windows e veja [criando um descritor de segurança para um novo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="9cbfb-109">For more information about ACLs, visit the Security section of the Microsoft Windows Software Development Kit (SDK), and see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9cbfb-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cbfb-110">Syntax</span></span>

``` syntax
[AMENDMENT]
class CommandLineEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  CommandLineTemplate;
  boolean CreateNewConsole = False;
  boolean CreateNewProcessGroup = True;
  boolean CreateSeparateWowVdm = False;
  boolean CreateSharedWowVdm = False;
  string  DesktopName;
  string  ExecutablePath;
  uint32  FillAttributes;
  boolean ForceOffFeedback = False;
  boolean ForceOnFeedback = False;
  uint32  KillTimeout = 0;
  string  Name;
  sint32  Priority = 0x20;
  boolean RunInteractively = False;
  uint32  ShowWindowCommand;
  boolean UseDefaultErrorMode = False;
  string  WindowTitle;
  string  WorkingDirectory;
  uint32  XCoordinate;
  uint32  XNumCharacters;
  uint32  XSize;
  uint32  YCoordinate;
  uint32  YNumCharacters;
  uint32  YSize;
  uint32  FillAttribute;
};
```

## <a name="members"></a><span data-ttu-id="9cbfb-111">Membros</span><span class="sxs-lookup"><span data-stu-id="9cbfb-111">Members</span></span>

<span data-ttu-id="9cbfb-112">A classe **CommandLineEventConsumer** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9cbfb-112">The **CommandLineEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="9cbfb-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9cbfb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9cbfb-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9cbfb-114">Properties</span></span>

<span data-ttu-id="9cbfb-115">A classe **CommandLineEventConsumer** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-115">The **CommandLineEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9cbfb-116">**CommandLineTemplate**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-116">**CommandLineTemplate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-119">Modelo de cadeia de caracteres padrão que especifica o processo a ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-119">Standard string template that specifies the process to be started.</span></span> <span data-ttu-id="9cbfb-120">Essa propriedade pode ser **nula** e a propriedade **ExecutablePath** é usada como a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-120">This property can be **NULL**, and the **ExecutablePath** property is used as the command line.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-121">**CreateNewConsole**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-121">**CreateNewConsole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-122">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-124">Não usado.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-124">Not used.</span></span> <span data-ttu-id="9cbfb-125">Se um valor for atribuído a essa propriedade, uma mensagem de rastreamento será gerada.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-125">If a value is assigned to this property, a tracing message is generated.</span></span> <span data-ttu-id="9cbfb-126">Para obter mais informações, consulte [rastreando a atividade WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="9cbfb-126">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-127">**CreateNewProcessGroup**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-127">**CreateNewProcessGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-130">Se for **true**, o novo processo será o processo raiz de um novo grupo de processos.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-130">If **True**, the new process is the root process of a new process group.</span></span> <span data-ttu-id="9cbfb-131">O grupo de processos inclui todos os processos que são descendentes desse processo raiz.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-131">The process group includes all processes that are descendants of this root process.</span></span> <span data-ttu-id="9cbfb-132">O identificador de processo do novo grupo de processos é o mesmo que esse identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-132">The process identifier of the new process group is the same as this process identifier.</span></span> <span data-ttu-id="9cbfb-133">Os grupos de processos são usados pelo método [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) para habilitar o envio de um sinal de CTRL + C ou Ctrl + Break para um grupo de processos de console.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-133">Process groups are used by the [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) method to enable sending a CTRL+C or CTRL+BREAK signal to a group of console processes.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-134">**CreateSeparateWowVdm**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-134">**CreateSeparateWowVdm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-135">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-137">Se **for true**, o novo processo será executado em uma VDM (máquina virtual dos) privada.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-137">If **True**, the new process runs in a private Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="9cbfb-138">Isso só é válido ao iniciar um aplicativo em execução em um sistema operacional Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-138">This is only valid when starting an application running on a 16-bit Windows operating system.</span></span> <span data-ttu-id="9cbfb-139">Se definido como **false**, todos os aplicativos executados em um sistema operacional Windows de 16 bits executarão como threads em um único VDM compartilhado.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-139">If set to **False**, all applications running on a 16-bit Windows operating system run as threads in a single, shared VDM.</span></span> <span data-ttu-id="9cbfb-140">Para obter mais informações, consulte a seção comentários deste tópico.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-140">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-141">**CreateSharedWowVdm**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-141">**CreateSharedWowVdm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-142">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-144">Se **for true**, o método [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) executará o novo processo no VDM (computador virtual dos) compartilhado.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-144">If **True**, the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method runs the new process in the shared Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="9cbfb-145">Essa propriedade pode substituir a opção DefaultSeparateVDM na seção do Windows de Win.ini se definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-145">This property can override the DefaultSeparateVDM switch in the Windows section of Win.ini if set to **True**.</span></span> <span data-ttu-id="9cbfb-146">Para obter mais informações, consulte a seção comentários deste tópico.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-146">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-147">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-147">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-148">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-148">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-150">SID (identificador de segurança) que identifica exclusivamente o usuário que cria um filtro.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-150">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="9cbfb-151">O WMI armazena o SID do usuário que cria uma instância de [**\_ \_ EventConsumer**](--eventconsumer.md) ou o SID do administrador, dependendo do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-151">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="9cbfb-152">Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) e [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="9cbfb-152">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="9cbfb-153">Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="9cbfb-153">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-154">**Área de trabalho**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-154">**DesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-157">Não usado.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-157">Not used.</span></span> <span data-ttu-id="9cbfb-158">Se um valor for atribuído a essa propriedade, uma mensagem de rastreamento será gerada.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-158">If a value is assigned to this property a tracing message is generated.</span></span> <span data-ttu-id="9cbfb-159">Para obter mais informações, consulte [rastreando a atividade WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="9cbfb-159">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-160">**ExecutablePath**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-160">**ExecutablePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-163">Módulo a ser executado.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-163">Module to execute.</span></span> <span data-ttu-id="9cbfb-164">A cadeia de caracteres pode especificar o caminho completo e o nome de arquivo do módulo a ser executado, ou pode especificar um nome parcial.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-164">The string can specify the full path and file name of the module to execute, or it can specify a partial name.</span></span> <span data-ttu-id="9cbfb-165">Se um nome parcial for especificado, a unidade atual e o diretório atual serão assumidos.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-165">If a partial name is specified, the current drive and current directory are assumed.</span></span>

<span data-ttu-id="9cbfb-166">A propriedade **ExecutablePath** pode ser **nula**.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-166">The **ExecutablePath** property can be **NULL**.</span></span> <span data-ttu-id="9cbfb-167">Nesse caso, o nome do módulo deve ser o primeiro token com delimitação de espaço em branco no valor da propriedade **CommandLineTemplate** .</span><span class="sxs-lookup"><span data-stu-id="9cbfb-167">In that case, the module name must be the first white space-delimited token in the **CommandLineTemplate** property value.</span></span> <span data-ttu-id="9cbfb-168">Se estiver usando um nome de arquivo longo que contenha um espaço, use cadeias de caracteres entre aspas para indicar onde o nome do arquivo termina e os argumentos começam a esclarecer o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-168">If using a long file name that contains a space, use quoted strings to indicate where the file name ends and the arguments begin to clarify the file name.</span></span>

> [!Note]  
> <span data-ttu-id="9cbfb-169">Como a propriedade **CommandLineTemplate** pode ser um modelo em que o módulo a ser executado é fornecido por uma variável, uma propriedade **ExecutablePath** **nula** permite o módulo especificado no parâmetro a ser executado e, em seguida, está fora do seu controle.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-169">Because the **CommandLineTemplate** property can be a template where the module to execute is supplied by a variable, a **NULL** **ExecutablePath** property permits the module that is specified in the parameter to execute, and then it is out of your control.</span></span> <span data-ttu-id="9cbfb-170">Sempre defina a propriedade **ExecutablePath** no registro **CommandLineEventConsumer** para incluir o executável necessário, que evita a substituição por parâmetros de eventos.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-170">Always set the **ExecutablePath** property in the **CommandLineEventConsumer** registration to include the required executable, which avoids overwriting by events parameters.</span></span> <span data-ttu-id="9cbfb-171">Se você precisar usar um modelo e uma variável para especificar o módulo a ser executado, tenha cuidado com quem recebe privilégio de gravação completa no namespace.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-171">If you must use a template and variable to specify the module to execute, be careful about who is granted full write privilege in the namespace.</span></span>

 

</dd> <dt>

<span data-ttu-id="9cbfb-172">**Fillattribute**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-172">**FillAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-173">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-175">Especifica o texto inicial e as cores do plano de fundo se uma nova janela do console for criada em um aplicativo de console</span><span class="sxs-lookup"><span data-stu-id="9cbfb-175">Specifies the initial text and background colors if a new console window is created in a console application</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-176">**FillAttributes**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-176">**FillAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-177">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9cbfb-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-179">Texto inicial e cores de plano de fundo, se uma nova janela de console for criada em um aplicativo de console.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-179">Initial text and background colors, if a new console window is created in a console application.</span></span> <span data-ttu-id="9cbfb-180">Essa propriedade é ignorada em um aplicativo de GUI.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-180">This property is ignored in a GUI application.</span></span> <span data-ttu-id="9cbfb-181">O valor pode ser qualquer combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-181">The value can be any combination of the following values.</span></span>

<dt>

<span data-ttu-id="9cbfb-182">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-182">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="9cbfb-183">primeiro plano azul</span><span class="sxs-lookup"><span data-stu-id="9cbfb-183">blue foreground</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-184">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-184">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="9cbfb-185">primeiro plano verde</span><span class="sxs-lookup"><span data-stu-id="9cbfb-185">green foreground</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-186">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-186">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="9cbfb-187">primeiro plano vermelho</span><span class="sxs-lookup"><span data-stu-id="9cbfb-187">red foreground</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-188">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-188">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="9cbfb-189">intensidade do primeiro plano</span><span class="sxs-lookup"><span data-stu-id="9cbfb-189">foreground intensity</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-190">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-190">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="9cbfb-191">plano de fundo azul</span><span class="sxs-lookup"><span data-stu-id="9cbfb-191">blue background</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-192">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-192">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="9cbfb-193">plano de fundo verde</span><span class="sxs-lookup"><span data-stu-id="9cbfb-193">green background</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-194">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-194">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="9cbfb-195">plano de fundo vermelho</span><span class="sxs-lookup"><span data-stu-id="9cbfb-195">red background</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-196">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-196">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="9cbfb-197">intensidade do plano de fundo</span><span class="sxs-lookup"><span data-stu-id="9cbfb-197">background intensity</span></span>

</dd> </dl>

<span data-ttu-id="9cbfb-198">Por exemplo, as seguintes combinações produzem texto vermelho em um plano de fundo branco:</span><span class="sxs-lookup"><span data-stu-id="9cbfb-198">For example, the following combinations produce red text on a white background:</span></span>


```mof
0x4 | 0x40 | 0x20 | 0x10
```



  <span data-ttu-id="9cbfb-199">ou</span><span class="sxs-lookup"><span data-stu-id="9cbfb-199">or</span></span>  


```mof
0x74
```



</dd> <dt>

<span data-ttu-id="9cbfb-200">**ForceOffFeedback**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-200">**ForceOffFeedback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-201">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-203">Se for **true**, o cursor de comentários será forçado enquanto o processo estiver sendo iniciado.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-203">If **True**, the feedback cursor is forced off while the process is starting.</span></span> <span data-ttu-id="9cbfb-204">O cursor normal é exibido.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-204">The normal cursor is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-205">**ForceOnFeedback**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-205">**ForceOnFeedback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-206">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-208">Se for **true**, o cursor estará no modo de comentários por dois segundos após o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) ser chamado.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-208">If **True**, the cursor is in feedback mode for two seconds after [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) is called.</span></span> <span data-ttu-id="9cbfb-209">Durante esses dois segundos, se o processo fizer a primeira chamada de GUI, o sistema fornecerá cinco mais segundos para o processo.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-209">During those two seconds, if the process makes the first GUI call, the system gives five more seconds to the process.</span></span> <span data-ttu-id="9cbfb-210">Durante esses cinco segundos, se o processo mostrar uma janela, o sistema fornecerá outros cinco segundos para o processo concluir o desenho da janela.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-210">During those five seconds, if the process shows a window, the system gives another five seconds to the process to finish drawing the window.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-211">**KillTimeout**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-211">**KillTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-212">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-214">Número, em segundos, que o serviço WMI aguarda antes de eliminar um processo 0 (zero) indica que um processo não deve ser eliminado.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-214">Number, in seconds, that the WMI service waits before killing a process 0 (zero) indicates a process is not to be killed.</span></span> <span data-ttu-id="9cbfb-215">A eliminação de um processo impede que um processo seja executado indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-215">Killing a process prevents a process from running indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-216">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-216">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-219">Nome do computador ao qual Instrumentação de Gerenciamento do Windows (WMI) envia eventos.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-219">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="9cbfb-220">Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="9cbfb-220">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-221">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-221">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-222">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-224">Fila máxima para um consumidor específico, em bytes.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-224">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="9cbfb-225">Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="9cbfb-225">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-226">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-229">Qualificadores: [ **chave**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-229">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-230">Nome exclusivo de um consumidor.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-230">Unique name of a consumer.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-231">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-231">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-232">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-232">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-234">Agendamento do nível de prioridade dos threads do processo.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-234">Scheduling priority level of the process threads.</span></span> <span data-ttu-id="9cbfb-235">A lista a seguir lista os níveis de prioridade disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-235">The following list lists the priority levels available.</span></span>

<dt>

<span data-ttu-id="9cbfb-236">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-236">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="9cbfb-237">Indica um processo normal sem necessidade de agendamento.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-237">Indicates a normal process without scheduling needs.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-238">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-238">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="9cbfb-239">Indica um processo cujos threads são executados somente quando o sistema está ocioso e são admitidos pelos threads de qualquer processo em execução em uma classe de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-239">Indicates a process whose threads run only when the system is idle, and are preempted by the threads of any process running in a higher priority class.</span></span> <span data-ttu-id="9cbfb-240">Um exemplo é uma proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-240">An example is a screen saver.</span></span> <span data-ttu-id="9cbfb-241">A classe de prioridade ociosa é herdada por processos filho.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-241">The idle priority class is inherited by child processes.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-242">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-242">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="9cbfb-243">Indica um processo que executa tarefas de alta prioridade e de tempo crítico.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-243">Indicates a process that performs high-priority, time critical tasks.</span></span> <span data-ttu-id="9cbfb-244">Os threads de um processo de classe de alta prioridade sobrecapturam os threads de processos de classe de prioridade normal ou de prioridade ociosa.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-244">The threads of a high-priority class process preempts the threads of normal-priority or idle-priority class processes.</span></span> <span data-ttu-id="9cbfb-245">Um exemplo é o Lista de Tarefas, que deve responder rapidamente quando chamado pelo usuário, independentemente da carga no sistema.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-245">An example is the Task List, which must respond quickly when called by the user regardless of the load on the system.</span></span> <span data-ttu-id="9cbfb-246">Use extrema atenção ao usar a classe de alta prioridade, porque um aplicativo vinculado à CPU com uma classe de alta prioridade pode usar quase todos os ciclos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-246">Use extreme care when using the high-priority class, because a CPU-bound application with a high-priority class can use nearly all available cycles.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-247">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-247">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="9cbfb-248">Indica um processo que tem a maior prioridade possível.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-248">Indicates a process that has the highest possible priority.</span></span> <span data-ttu-id="9cbfb-249">Os threads de um processo de classe de prioridade em tempo real apropriam os threads de todos os outros processos, incluindo processos do sistema operacional que executam tarefas importantes.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-249">The threads of a real-time priority class process preempt the threads of all other processes, including operating system processes that perform important tasks.</span></span> <span data-ttu-id="9cbfb-250">Por exemplo, um processo em tempo real executado por mais de um breve intervalo pode fazer com que os caches de disco não sejam liberados ou fazer com que o mouse não responda.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-250">For example, a real-time process that executes for more than a brief interval can cause disk caches not to flush, or cause the mouse to be unresponsive.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9cbfb-251">**RunInteractively**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-251">**RunInteractively**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-252">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-254">Se **for true**, o processo será iniciado no WinStation interativo.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-254">If **True**, the process is launched in the interactive WinStation.</span></span> <span data-ttu-id="9cbfb-255">Se **for false**, o processo será iniciado no serviço padrão WinStation.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-255">If **False**, the process is launched in the default service WinStation.</span></span> <span data-ttu-id="9cbfb-256">Essa propriedade substitui a propriedade **desktopname** .</span><span class="sxs-lookup"><span data-stu-id="9cbfb-256">This property overrides the **DesktopName** property.</span></span> <span data-ttu-id="9cbfb-257">Essa propriedade só é usada localmente e somente se o usuário interativo for o mesmo usuário que configurou o consumidor.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-257">This property is only used locally, and only if the interactive user is the same user who set up the consumer.</span></span>

<span data-ttu-id="9cbfb-258">A partir do Windows Vista, o processo que executa a instância **CommandLineEventConsumer** é iniciado na conta **LocalSystem** e está na sessão 0.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-258">Starting with Windows Vista, the process running the **CommandLineEventConsumer** instance is started under the **LocalSystem** account and is in session 0.</span></span> <span data-ttu-id="9cbfb-259">Os serviços executados na sessão 0 não podem interagir com sessões de usuário.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-259">Services which run in session 0 cannot interact with user sessions.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-260">**ShowWindowCommand**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-260">**ShowWindowCommand**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-261">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-263">Estado de exibição da janela.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-263">Window show state.</span></span> <span data-ttu-id="9cbfb-264">Pode ser qualquer um dos valores que podem ser especificados no parâmetro *nCmdShow* para a função de [janela](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="9cbfb-264">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-265">**UseDefaultErrorMode**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-265">**UseDefaultErrorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-266">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-268">Se **for true**, o modo de erro padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-268">If **True**, the default error mode is used.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-269">**WindowTitle**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-269">**WindowTitle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-270">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-271">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-272">Título que aparece na barra de título do processo.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-272">Title that appears on the title bar of the process.</span></span> <span data-ttu-id="9cbfb-273">Essa propriedade é ignorada para aplicativos de GUI.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-273">This property is ignored for GUI applications.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-274">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-274">**WorkingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-275">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-277">Diretório de trabalho para este processo.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-277">Working directory for this process.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-278">**XCoordinate**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-278">**XCoordinate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-279">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-281">X-deslocamento, em pixels, da borda esquerda da tela até a borda esquerda da janela, se uma nova janela for criada.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-281">X-offset, in pixels, from the left edge of the screen to the left edge of the window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-282">**XNumCharacters**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-282">**XNumCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-283">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-285">Largura do buffer de tela, em colunas de caracteres, se uma nova janela de console for criada.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-285">Screen buffer width, in character columns, if a new console window is created.</span></span> <span data-ttu-id="9cbfb-286">Essa propriedade é ignorada em um processo de GUI.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-286">This property is ignored in a GUI process.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-287">**XSize**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-287">**XSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-288">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-290">Largura, em pixels, de uma nova janela, se uma nova janela for criada.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-290">Width, in pixels, of a new window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-291">**YCoordinate**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-291">**YCoordinate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-292">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-294">Deslocamento Y, em pixels, da borda superior da tela até a borda superior da janela, se uma nova janela for criada.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-294">Y-offset, in pixels, from the top edge of the screen to the top edge of the window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-295">**YNumCharacters**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-295">**YNumCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-296">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-297">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-298">Altura do buffer de tela, em linhas de caracteres, se uma nova janela de console for criada.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-298">Screen buffer height, in character rows, if a new console window is created.</span></span> <span data-ttu-id="9cbfb-299">Essa propriedade é ignorada em um processo de GUI.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-299">This property is ignored in a GUI process.</span></span>

</dd> <dt>

<span data-ttu-id="9cbfb-300">**YSize**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-300">**YSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cbfb-301">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9cbfb-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9cbfb-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cbfb-303">Altura, em pixels, da nova janela, se uma nova janela for criada.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-303">Height, in pixels, of the new window, if a new window is created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9cbfb-304">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cbfb-304">Remarks</span></span>

<span data-ttu-id="9cbfb-305">A classe **CommandLineEventConsumer** é derivada da classe abstrata [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="9cbfb-305">The **CommandLineEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

<span data-ttu-id="9cbfb-306">A propriedade **CreateSeparateWowVdm** indica se o novo processo é executado em uma VDM (máquina virtual de dos) privada.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-306">The **CreateSeparateWowVdm** property indicates whether or not the new process runs in a private Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="9cbfb-307">A vantagem de executar separadamente é que uma falha só encerra o VDM.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-307">The advantage of running separately is that a crash only terminates the single VDM.</span></span> <span data-ttu-id="9cbfb-308">Programas executados em VDMs distintos continuam a funcionar normalmente, e os aplicativos baseados no Windows de 16 bits executados em VDMs separados têm filas de entrada separadas.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-308">Programs running in distinct VDMs continue to function normally, and the 16-bit Windows-based applications running in separate VDMs have separate input queues.</span></span> <span data-ttu-id="9cbfb-309">Isso significa que, se um aplicativo parar de responder momentaneamente, os aplicativos em VDMs separados continuarão a receber a entrada.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-309">This means that if one application stops responding momentarily, the applications in separate VDMs continue to receive input.</span></span> <span data-ttu-id="9cbfb-310">A desvantagem de executar separadamente é que ela leva muito mais memória para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-310">The disadvantage of running separately is that it takes significantly more memory to do so.</span></span> <span data-ttu-id="9cbfb-311">Você deve definir essa propriedade como **true** somente se o usuário solicitar que aplicativos baseados no Windows de 16 bits sejam executados em seu próprio VDM.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-311">You should set this property to **True** only if the user requests that 16-bit Windows-based applications run in their own VDM.</span></span>

> [!Note]  
> <span data-ttu-id="9cbfb-312">O **CommandLineEventConsumer** usa o método [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) internamente e passa as propriedades **ExecutablePath** e **CommandLineTemplate** como os parâmetros *lpApplicationName* e *lpCommandLine* .</span><span class="sxs-lookup"><span data-stu-id="9cbfb-312">The **CommandLineEventConsumer** uses the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method internally, and passes the **ExecutablePath** and **CommandLineTemplate** properties as the *lpApplicationName* and *lpCommandLine* parameters.</span></span> <span data-ttu-id="9cbfb-313">O exemplo de código de formato MOF (MOF) a seguir não usa **CommandLineEventConsumer** corretamente.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-313">The following Managed Object Format (MOF) code example does not use **CommandLineEventConsumer** correctly.</span></span>

 


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\scripts\\MyScript.js param1 param2";
};
```



<span data-ttu-id="9cbfb-314">O método [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) passa *lpCommandLine* como `argv[0]` , `argv[1]` e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-314">The [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method passes *lpCommandLine* as `argv[0]`, `argv[1]`, and so on.</span></span> <span data-ttu-id="9cbfb-315">Como `argv[0]` para aplicativos de 16 bits usados para serem reservados para o nome do arquivo executável, o código MOF anterior resulta no processo que está sendo criado, como se o comando a seguir fosse inserido no prompt de comando: **c: \\ Windows \\ System32 \\cscript.exe param1 param2**.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-315">Because `argv[0]` for 16-bit applications used to be reserved for the executable file name, the previous MOF code results in the process being created as though the following command is entered at the command prompt: **c:\\windows\\system32\\cscript.exe param1 param2**.</span></span>

<span data-ttu-id="9cbfb-316">O comando anterior não é bem sucedido porque Cscript.exe não examina `argv[0]` e, portanto, não reconhece que ele não contém seu próprio nome, mas algo mais ("c: \\ \\ scripts \\ \\MyScript.js").</span><span class="sxs-lookup"><span data-stu-id="9cbfb-316">The previous command does not succeed because Cscript.exe does not look at `argv[0]`, and so it does not recognize that it does not contain its own name, but something else ("c:\\\\scripts\\\\MyScript.js").</span></span> <span data-ttu-id="9cbfb-317">O exemplo a seguir identifica o uso recomendado de **CommandLineEventConsumer**.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-317">The following example identifies the recommended use of **CommandLineEventConsumer**.</span></span>


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\windows\\system32\\cscript.exe"
    "C:\\scripts\\MyScript.js param1 param2";
};
```



<span data-ttu-id="9cbfb-318">O uso anterior de **CommandLineEventConsumer** resulta no processo criado como se o comando a seguir tivesse sido inserido no prompt de comando: **c: \\ Windows \\ system32 \\cscript.exe c: \\ scripts \\MyScript.js param1 param2**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-318">The previous use of **CommandLineEventConsumer** results in the process created as though the following command was entered at the command prompt: **c:\\windows\\system32\\cscript.exe c:\\scripts\\MyScript.js param1 param2**</span></span>

<span data-ttu-id="9cbfb-319">Como "c: \\ \\ scripts \\ \\MyScript.js" é agora `argv[1]` , ele é visto por Cscript.exe e o comando é bem sucedido.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-319">Because "c:\\\\scripts\\\\MyScript.js" is now `argv[1]`, it is seen by Cscript.exe and the command succeeds.</span></span>

<span data-ttu-id="9cbfb-320">Para obter mais informações, consulte a função [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="9cbfb-320">For more information, see the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="9cbfb-321">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9cbfb-321">Examples</span></span>

<span data-ttu-id="9cbfb-322">Para obter um exemplo de como usar o **CommandLineEventConsumer** para criar um consumidor, consulte [executando um programa da linha de comando com base em um evento](running-a-program-from-the-command-line-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="9cbfb-322">For an example of using **CommandLineEventConsumer** to create a consumer, see [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9cbfb-323">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cbfb-323">Requirements</span></span>



| <span data-ttu-id="9cbfb-324">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cbfb-324">Requirement</span></span> | <span data-ttu-id="9cbfb-325">Valor</span><span class="sxs-lookup"><span data-stu-id="9cbfb-325">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cbfb-326">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cbfb-326">Minimum supported client</span></span><br/> | <span data-ttu-id="9cbfb-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cbfb-327">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9cbfb-328">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cbfb-328">Minimum supported server</span></span><br/> | <span data-ttu-id="9cbfb-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cbfb-329">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9cbfb-330">Namespace</span><span class="sxs-lookup"><span data-stu-id="9cbfb-330">Namespace</span></span><br/>                | <span data-ttu-id="9cbfb-331">\\Assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="9cbfb-331">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="9cbfb-332">MOF</span><span class="sxs-lookup"><span data-stu-id="9cbfb-332">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9cbfb-333"><dt>Wbemcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9cbfb-333"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="9cbfb-334">DLL</span><span class="sxs-lookup"><span data-stu-id="9cbfb-334">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cbfb-335"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cbfb-335"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cbfb-336">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cbfb-336">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cbfb-337">Classes de consumidor padrão</span><span class="sxs-lookup"><span data-stu-id="9cbfb-337">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="9cbfb-338">Monitorando e respondendo a eventos com consumidores padrão</span><span class="sxs-lookup"><span data-stu-id="9cbfb-338">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="9cbfb-339">Criando um consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="9cbfb-339">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="9cbfb-340">Recebendo eventos em todos os momentos</span><span class="sxs-lookup"><span data-stu-id="9cbfb-340">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="9cbfb-341">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="9cbfb-341">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

