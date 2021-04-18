---
description: A classe LogFileEventConsumer grava cadeias de caracteres personalizadas em um arquivo de log de texto quando os eventos são entregues a ela.
ms.assetid: 8934b60e-3763-4b85-89fd-58fe6136dff6
ms.tgt_platform: multiple
title: Classe LogFileEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogFileEventConsumer
- LogFileEventConsumer.CreatorSID
- LogFileEventConsumer.MachineName
- LogFileEventConsumer.MaximumQueueSize
- LogFileEventConsumer.Filename
- LogFileEventConsumer.IsUnicode
- LogFileEventConsumer.MaximumFileSize
- LogFileEventConsumer.Name
- LogFileEventConsumer.Text
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 462989b740aaf6a6bd78968c951b7c676038cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781353"
---
# <a name="logfileeventconsumer-class"></a><span data-ttu-id="197ae-103">Classe LogFileEventConsumer</span><span class="sxs-lookup"><span data-stu-id="197ae-103">LogFileEventConsumer class</span></span>

<span data-ttu-id="197ae-104">A classe **LogFileEventConsumer** grava cadeias de caracteres personalizadas em um arquivo de log de texto quando os eventos são entregues a ela.</span><span class="sxs-lookup"><span data-stu-id="197ae-104">The **LogFileEventConsumer** class writes customized strings to a text log file when events are delivered to it.</span></span> <span data-ttu-id="197ae-105">As cadeias de caracteres são separadas por sequências de fim de linha.</span><span class="sxs-lookup"><span data-stu-id="197ae-105">The strings are separated by end-of-line sequences.</span></span> <span data-ttu-id="197ae-106">Essa classe é um dos consumidores de eventos padrão que o WMI fornece.</span><span class="sxs-lookup"><span data-stu-id="197ae-106">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="197ae-107">Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="197ae-107">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="197ae-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="197ae-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class LogFileEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  Filename;
  boolean IsUnicode;
  uint64  MaximumFileSize = 65535;
  string  Name;
  string  Text;
};
```

## <a name="members"></a><span data-ttu-id="197ae-109">Membros</span><span class="sxs-lookup"><span data-stu-id="197ae-109">Members</span></span>

<span data-ttu-id="197ae-110">A classe **LogFileEventConsumer** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="197ae-110">The **LogFileEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="197ae-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="197ae-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="197ae-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="197ae-112">Properties</span></span>

<span data-ttu-id="197ae-113">A classe **LogFileEventConsumer** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="197ae-113">The **LogFileEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="197ae-114">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="197ae-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="197ae-115">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="197ae-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="197ae-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="197ae-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="197ae-117">SID (identificador de segurança) que identifica exclusivamente o usuário que cria um filtro.</span><span class="sxs-lookup"><span data-stu-id="197ae-117">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="197ae-118">O WMI armazena o SID do usuário que cria uma instância de [**\_ \_ EventConsumer**](--eventconsumer.md) ou o SID do administrador, dependendo do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="197ae-118">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="197ae-119">Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) e [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="197ae-119">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="197ae-120">Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="197ae-120">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="197ae-121">**Filename**</span><span class="sxs-lookup"><span data-stu-id="197ae-121">**Filename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="197ae-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="197ae-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="197ae-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="197ae-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="197ae-124">Nome de um arquivo que inclui o caminho para o qual as entradas de log são acrescentadas.</span><span class="sxs-lookup"><span data-stu-id="197ae-124">Name of a file that includes the path to which the log entries are appended.</span></span> <span data-ttu-id="197ae-125">Se o arquivo não existir, o **LogFileEventConsumer** tentará criá-lo.</span><span class="sxs-lookup"><span data-stu-id="197ae-125">If the file does not exist, **LogFileEventConsumer** attempts to create it.</span></span> <span data-ttu-id="197ae-126">O consumidor falha quando o caminho não existe ou quando o usuário que cria o consumidor não tem permissões de gravação para o arquivo ou caminho.</span><span class="sxs-lookup"><span data-stu-id="197ae-126">The consumer fails when the path does not exist, or when the user who creates the consumer does not have write permissions for the file or path.</span></span>

</dd> <dt>

<span data-ttu-id="197ae-127">**Isunicode**</span><span class="sxs-lookup"><span data-stu-id="197ae-127">**IsUnicode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="197ae-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="197ae-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="197ae-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="197ae-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="197ae-130">Se for **true**, o arquivo de log será um arquivo de texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="197ae-130">If **TRUE**, the log file is a Unicode text file.</span></span> <span data-ttu-id="197ae-131">Se for **false**, o arquivo de log será um arquivo de texto de código multibyte.</span><span class="sxs-lookup"><span data-stu-id="197ae-131">If **FALSE**, the log file is a multibyte code text file.</span></span> <span data-ttu-id="197ae-132">Se o arquivo existir, essa propriedade será ignorada e a configuração de arquivo atual será usada.</span><span class="sxs-lookup"><span data-stu-id="197ae-132">If the file exists, this property is ignored and the current file setting is used.</span></span> <span data-ttu-id="197ae-133">Por exemplo, se **isunicode** for **false**, mas o arquivo existente for um arquivo Unicode, o Unicode será usado.</span><span class="sxs-lookup"><span data-stu-id="197ae-133">For example, if **IsUnicode** is **FALSE**, but the existing file is a Unicode file, then Unicode is used.</span></span> <span data-ttu-id="197ae-134">Se **isunicode** for **true**, mas o arquivo for um código multibyte, o código multibyte será usado.</span><span class="sxs-lookup"><span data-stu-id="197ae-134">If **IsUnicode** is **TRUE**, but the file is multibyte code, then multibyte code is used.</span></span>

</dd> <dt>

<span data-ttu-id="197ae-135">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="197ae-135">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="197ae-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="197ae-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="197ae-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="197ae-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="197ae-138">Nome do computador ao qual Instrumentação de Gerenciamento do Windows (WMI) envia eventos.</span><span class="sxs-lookup"><span data-stu-id="197ae-138">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="197ae-139">Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="197ae-139">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="197ae-140">**MaximumFileSize**</span><span class="sxs-lookup"><span data-stu-id="197ae-140">**MaximumFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="197ae-141">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="197ae-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="197ae-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="197ae-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="197ae-143">Tamanho máximo de um arquivo de log em bytes.</span><span class="sxs-lookup"><span data-stu-id="197ae-143">Maximum size of a log file in bytes.</span></span> <span data-ttu-id="197ae-144">Se o arquivo primário exceder seu tamanho máximo, o conteúdo será movido para um arquivo diferente e o arquivo primário será esvaziado.</span><span class="sxs-lookup"><span data-stu-id="197ae-144">If the primary file exceeds its maximum size, the contents are moved to a different file and the primary file is emptied.</span></span> <span data-ttu-id="197ae-145">Um valor de 0 (zero) significa que não há limite de tamanho.</span><span class="sxs-lookup"><span data-stu-id="197ae-145">A value of 0 (zero) means there is no size limit.</span></span> <span data-ttu-id="197ae-146">O valor padrão é 65.535 bytes.</span><span class="sxs-lookup"><span data-stu-id="197ae-146">The default value is 65,535 bytes.</span></span> <span data-ttu-id="197ae-147">O tamanho do arquivo é verificado antes de uma operação de gravação.</span><span class="sxs-lookup"><span data-stu-id="197ae-147">The size of the file is checked before a write operation.</span></span> <span data-ttu-id="197ae-148">Portanto, você pode ter um arquivo ligeiramente maior do que o limite de tamanho especificado.</span><span class="sxs-lookup"><span data-stu-id="197ae-148">Therefore, you can have a file that is slightly larger than the specified size limit.</span></span> <span data-ttu-id="197ae-149">A próxima operação de gravação o captura e inicia um novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="197ae-149">The next write operation catches it and starts a new file.</span></span>

<span data-ttu-id="197ae-150">A lista a seguir identifica a estrutura de nomenclatura para o arquivo de backup:</span><span class="sxs-lookup"><span data-stu-id="197ae-150">The following list identifies the naming structure for the backup file:</span></span>

-   <span data-ttu-id="197ae-151">Se o nome de arquivo original for 8,3, a extensão será substituída por uma cadeia de caracteres no formato "001", "002" e assim por diante com o menor número maior do que todos os números usados anteriormente e escolhidos.</span><span class="sxs-lookup"><span data-stu-id="197ae-151">If the original filename is 8.3, the extension is replaced by a string in the format of "001", "002", and so on with the smallest number larger than all the previously used and chosen numbers.</span></span> <span data-ttu-id="197ae-152">Se "999" for usado, o número escolhido será o menor número não utilizado.</span><span class="sxs-lookup"><span data-stu-id="197ae-152">If "999" is used, then the number chosen is the smallest unused number.</span></span>
-   <span data-ttu-id="197ae-153">Se o nome de arquivo original não for 8,3, uma cadeia de caracteres no formato "001", "002" e assim por diante será anexada ao nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="197ae-153">If the original filename is not 8.3, a string in the format of "001", "002", and so on is appended to the file name.</span></span>

<span data-ttu-id="197ae-154">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="197ae-154">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="197ae-155">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="197ae-155">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="197ae-156">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="197ae-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="197ae-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="197ae-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="197ae-158">Fila máxima para um consumidor específico, em bytes.</span><span class="sxs-lookup"><span data-stu-id="197ae-158">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="197ae-159">Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="197ae-159">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="197ae-160">**Nome**</span><span class="sxs-lookup"><span data-stu-id="197ae-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="197ae-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="197ae-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="197ae-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="197ae-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="197ae-163">Qualificadores: [ **chave**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="197ae-163">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="197ae-164">Nome exclusivo para este consumidor.</span><span class="sxs-lookup"><span data-stu-id="197ae-164">Unique name for this consumer.</span></span>

</dd> <dt>

<span data-ttu-id="197ae-165">**Text**</span><span class="sxs-lookup"><span data-stu-id="197ae-165">**Text**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="197ae-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="197ae-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="197ae-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="197ae-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="197ae-168">[Modelo](using-standard-string-templates.md) de cadeia de caracteres padrão para o texto de uma entrada de log.</span><span class="sxs-lookup"><span data-stu-id="197ae-168">Standard string [template](using-standard-string-templates.md) for the text of a log entry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="197ae-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="197ae-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="197ae-170">O **LogFileEventConsumer** não protege o arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="197ae-170">The **LogFileEventConsumer** does not secure the log file.</span></span> <span data-ttu-id="197ae-171">Portanto, ao configurar o **LogFileEventConsumer**, é importante especificar um diretório que seja protegido para o nível de que você precisa.</span><span class="sxs-lookup"><span data-stu-id="197ae-171">Therefore, when you configure the **LogFileEventConsumer**, it is important to specify a directory that is secured to the level that you require.</span></span>

 

<span data-ttu-id="197ae-172">A classe **LogFileEventConsumer** é derivada da classe abstrata [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="197ae-172">The **LogFileEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

## <a name="examples"></a><span data-ttu-id="197ae-173">Exemplos</span><span class="sxs-lookup"><span data-stu-id="197ae-173">Examples</span></span>

<span data-ttu-id="197ae-174">Para obter um exemplo de como usar o **LogFileEventConsumer** para criar um consumidor, consulte [gravando em um arquivo de log com base em um evento](writing-to-a-log-file-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="197ae-174">For an example of using **LogFileEventConsumer** to create a consumer, see [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="197ae-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="197ae-175">Requirements</span></span>



| <span data-ttu-id="197ae-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="197ae-176">Requirement</span></span> | <span data-ttu-id="197ae-177">Valor</span><span class="sxs-lookup"><span data-stu-id="197ae-177">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="197ae-178">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="197ae-178">Minimum supported client</span></span><br/> | <span data-ttu-id="197ae-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="197ae-179">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="197ae-180">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="197ae-180">Minimum supported server</span></span><br/> | <span data-ttu-id="197ae-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="197ae-181">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="197ae-182">Namespace</span><span class="sxs-lookup"><span data-stu-id="197ae-182">Namespace</span></span><br/>                | <span data-ttu-id="197ae-183">\\Assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="197ae-183">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="197ae-184">MOF</span><span class="sxs-lookup"><span data-stu-id="197ae-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="197ae-185"><dt>Wbemcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="197ae-185"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="197ae-186">DLL</span><span class="sxs-lookup"><span data-stu-id="197ae-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="197ae-187"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="197ae-187"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="197ae-188">Confira também</span><span class="sxs-lookup"><span data-stu-id="197ae-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="197ae-189">Classes de consumidor padrão</span><span class="sxs-lookup"><span data-stu-id="197ae-189">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="197ae-190">Gravando em um arquivo de log baseado em um evento</span><span class="sxs-lookup"><span data-stu-id="197ae-190">Writing to a Log File Based on an Event</span></span>](writing-to-a-log-file-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="197ae-191">Criando um consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="197ae-191">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="197ae-192">Recebendo eventos em todos os momentos</span><span class="sxs-lookup"><span data-stu-id="197ae-192">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="197ae-193">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="197ae-193">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

