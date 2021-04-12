---
description: A classe SMTPEventConsumer envia uma mensagem de email usando o protocolo SMTP sempre que um evento é entregue a ele.
ms.assetid: 42178360-9e22-4cd1-9b72-5f6b0d7e6c9c
ms.tgt_platform: multiple
title: Classe SMTPEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMTPEventConsumer
- SMTPEventConsumer.CreatorSID
- SMTPEventConsumer.MachineName
- SMTPEventConsumer.MaximumQueueSize
- SMTPEventConsumer.BccLine
- SMTPEventConsumer.CcLine
- SMTPEventConsumer.FromLine
- SMTPEventConsumer.HeaderFields
- SMTPEventConsumer.Message
- SMTPEventConsumer.Name
- SMTPEventConsumer.ReplyToLine
- SMTPEventConsumer.SMTPServer
- SMTPEventConsumer.Subject
- SMTPEventConsumer.ToLine
api_type:
- DllExport
api_location:
- Smtpcons.dll
ms.openlocfilehash: 76c7fad3b5cb4bbf6c3c0c03689607ba64fbcc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171794"
---
# <a name="smtpeventconsumer-class"></a><span data-ttu-id="c978e-103">Classe SMTPEventConsumer</span><span class="sxs-lookup"><span data-stu-id="c978e-103">SMTPEventConsumer class</span></span>

<span data-ttu-id="c978e-104">A classe **SMTPEventConsumer** envia uma mensagem de email usando o protocolo SMTP sempre que um evento é entregue a ele.</span><span class="sxs-lookup"><span data-stu-id="c978e-104">The **SMTPEventConsumer** class sends an email message by using Simple Mail Transfer Protocol (SMTP) each time an event is delivered to it.</span></span> <span data-ttu-id="c978e-105">Um servidor SMTP deve existir na rede.</span><span class="sxs-lookup"><span data-stu-id="c978e-105">An SMTP server must exist on the network.</span></span> <span data-ttu-id="c978e-106">A classe SMTPEventConsumer não dá suporte a anexos.</span><span class="sxs-lookup"><span data-stu-id="c978e-106">The SMTPEventConsumer class does not support attachments.</span></span> <span data-ttu-id="c978e-107">A codificação da mensagem de email deve ser US-ASCII.</span><span class="sxs-lookup"><span data-stu-id="c978e-107">The encoding of the email message must be US-ASCII.</span></span>

<span data-ttu-id="c978e-108">Essa classe é um dos consumidores de eventos padrão que o WMI fornece.</span><span class="sxs-lookup"><span data-stu-id="c978e-108">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="c978e-109">Para obter um exemplo de como usar o **SMTPEventConsumer** para criar um consumidor, consulte [enviando email com base em um evento](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="c978e-109">For an example of using **SMTPEventConsumer** to create a consumer, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span> <span data-ttu-id="c978e-110">Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="c978e-110">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="c978e-111">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c978e-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c978e-112">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="c978e-112">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c978e-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c978e-113">Syntax</span></span>

``` syntax
[AMENDMENT]
class SMTPEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  string BccLine;
  string CcLine;
  string FromLine;
  string HeaderFields[];
  string Message;
  string Name;
  string ReplyToLine;
  string SMTPServer;
  string Subject;
  string ToLine;
};
```

## <a name="members"></a><span data-ttu-id="c978e-114">Membros</span><span class="sxs-lookup"><span data-stu-id="c978e-114">Members</span></span>

<span data-ttu-id="c978e-115">A classe **SMTPEventConsumer** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c978e-115">The **SMTPEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="c978e-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c978e-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c978e-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c978e-117">Properties</span></span>

<span data-ttu-id="c978e-118">A classe **SMTPEventConsumer** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c978e-118">The **SMTPEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c978e-119">**BccLine**</span><span class="sxs-lookup"><span data-stu-id="c978e-119">**BccLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c978e-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c978e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c978e-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c978e-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c978e-122">Uma lista de endereços, separados por vírgula ou ponto-e-vírgula, no formato de um modelo de cadeia de caracteres padrão ao qual a mensagem é enviada como uma cópia carbono oculta.</span><span class="sxs-lookup"><span data-stu-id="c978e-122">A list of addresses, separated by a comma or semicolon, in the format of a standard string template to which the message is sent as a blind carbon copy.</span></span> <span data-ttu-id="c978e-123">Para obter mais informações, consulte a seção comentários deste tópico.</span><span class="sxs-lookup"><span data-stu-id="c978e-123">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="c978e-124">**CcLine**</span><span class="sxs-lookup"><span data-stu-id="c978e-124">**CcLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c978e-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c978e-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c978e-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c978e-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c978e-127">Uma lista de endereços, separados por vírgula ou ponto-e-vírgula, no formato de um modelo de cadeia de caracteres padrão para o qual a mensagem é enviada como uma cópia carbono.</span><span class="sxs-lookup"><span data-stu-id="c978e-127">A list of addresses, separated by a comma or semicolon, in the format of a standard string template to which the message is sent as a carbon copy.</span></span> <span data-ttu-id="c978e-128">Para obter mais informações, consulte a seção comentários deste tópico.</span><span class="sxs-lookup"><span data-stu-id="c978e-128">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="c978e-129">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="c978e-129">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c978e-130">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="c978e-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c978e-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c978e-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c978e-132">SID (identificador de segurança) que identifica exclusivamente o usuário que cria um filtro.</span><span class="sxs-lookup"><span data-stu-id="c978e-132">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="c978e-133">O WMI armazena o SID do usuário que cria uma instância de [**\_ \_ EventConsumer**](--eventconsumer.md) ou o SID do administrador, dependendo do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c978e-133">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="c978e-134">Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) e [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="c978e-134">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="c978e-135">Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="c978e-135">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="c978e-136">**A partir de**</span><span class="sxs-lookup"><span data-stu-id="c978e-136">**FromLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c978e-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c978e-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c978e-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c978e-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c978e-139">Da linha de uma mensagem de email no formato de um modelo de cadeia de caracteres padrão.</span><span class="sxs-lookup"><span data-stu-id="c978e-139">From line of an email message in the format of a standard string template.</span></span> <span data-ttu-id="c978e-140">Se for **NULL**, uma linha from será construída na forma de "winmgmt@*MachineName*".</span><span class="sxs-lookup"><span data-stu-id="c978e-140">If **NULL**, a From line is constructed in the form of "WinMgmt@*MachineName*".</span></span>

</dd> <dt>

<span data-ttu-id="c978e-141">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="c978e-141">**HeaderFields**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c978e-142">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c978e-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c978e-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c978e-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c978e-144">Matriz de campos de cabeçalho que são inseridos em uma mensagem de email sem interpretação.</span><span class="sxs-lookup"><span data-stu-id="c978e-144">Array of header fields that are inserted into an email message without interpretation.</span></span>

</dd> <dt>

<span data-ttu-id="c978e-145">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="c978e-145">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c978e-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c978e-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c978e-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c978e-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c978e-148">Nome do computador ao qual Instrumentação de Gerenciamento do Windows (WMI) envia eventos.</span><span class="sxs-lookup"><span data-stu-id="c978e-148">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="c978e-149">Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="c978e-149">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="c978e-150">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="c978e-150">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c978e-151">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c978e-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c978e-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c978e-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c978e-153">Fila máxima para um consumidor específico, em bytes.</span><span class="sxs-lookup"><span data-stu-id="c978e-153">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="c978e-154">Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="c978e-154">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="c978e-155">**Message**</span><span class="sxs-lookup"><span data-stu-id="c978e-155">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c978e-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c978e-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c978e-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c978e-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c978e-158">Modelo de cadeia de caracteres padrão que contém o corpo de uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="c978e-158">Standard string template that contains the body of an email message.</span></span>

</dd> <dt>

<span data-ttu-id="c978e-159">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c978e-159">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c978e-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c978e-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c978e-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c978e-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c978e-162">Qualificadores: [ **chave**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="c978e-162">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="c978e-163">Identificador exclusivo para o consumidor do evento.</span><span class="sxs-lookup"><span data-stu-id="c978e-163">Unique identifier for the event consumer.</span></span>

</dd> <dt>

<span data-ttu-id="c978e-164">**ReplyToLine**</span><span class="sxs-lookup"><span data-stu-id="c978e-164">**ReplyToLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c978e-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c978e-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c978e-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c978e-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c978e-167">Linha de resposta de uma mensagem de email no formato de um modelo de cadeia de caracteres padrão.</span><span class="sxs-lookup"><span data-stu-id="c978e-167">Reply-to line of an email message in the format of a standard string template.</span></span> <span data-ttu-id="c978e-168">Se **NULL**, nenhuma linha de resposta será usada.</span><span class="sxs-lookup"><span data-stu-id="c978e-168">If **NULL**, no Reply-to line is used.</span></span>

</dd> <dt>

<span data-ttu-id="c978e-169">**SMTPServer**</span><span class="sxs-lookup"><span data-stu-id="c978e-169">**SMTPServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c978e-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c978e-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c978e-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c978e-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c978e-172">Nome do servidor SMTP por meio do qual um email é enviado.</span><span class="sxs-lookup"><span data-stu-id="c978e-172">Name of the SMTP server through which an email is sent.</span></span> <span data-ttu-id="c978e-173">Os nomes permitidos são um endereço IP ou um DNS ou um nome NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="c978e-173">Permissible names are an IP address, or a DNS or NetBIOS name.</span></span> <span data-ttu-id="c978e-174">Esta propriedade não pode ser **nula**.</span><span class="sxs-lookup"><span data-stu-id="c978e-174">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c978e-175">**Entidade**</span><span class="sxs-lookup"><span data-stu-id="c978e-175">**Subject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c978e-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c978e-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c978e-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c978e-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c978e-178">Modelo de cadeia de caracteres padrão que contém o assunto de uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="c978e-178">Standard string template that contains the subject of an email message.</span></span>

</dd> <dt>

<span data-ttu-id="c978e-179">**ToLine**</span><span class="sxs-lookup"><span data-stu-id="c978e-179">**ToLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c978e-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c978e-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c978e-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c978e-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c978e-182">Uma lista de endereços, separados por vírgula ou ponto-e-vírgula, no formato de um modelo de cadeia de caracteres padrão que identifica onde a mensagem deve ser enviada.</span><span class="sxs-lookup"><span data-stu-id="c978e-182">A list of addresses, separated by a comma or semicolon, in the format of a standard string template that identifies where the message is to be sent.</span></span> <span data-ttu-id="c978e-183">Para obter mais informações, consulte a seção comentários deste tópico.</span><span class="sxs-lookup"><span data-stu-id="c978e-183">For more information, see the Remarks section of this topic.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c978e-184">Comentários</span><span class="sxs-lookup"><span data-stu-id="c978e-184">Remarks</span></span>

<span data-ttu-id="c978e-185">A classe SMTPEventConsumer é derivada da classe abstrata [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="c978e-185">The SMTPEventConsumer class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

<span data-ttu-id="c978e-186">Algumas das propriedades **ToLine**, **CcLine** ou **BccLine** podem ser **nulas**, mas elas não podem ser **nulas**.</span><span class="sxs-lookup"><span data-stu-id="c978e-186">Some of the **ToLine**, **CcLine**, or **BccLine** properties can be **NULL**, but they cannot all be **NULL**.</span></span>

<span data-ttu-id="c978e-187">Receber um código de retorno de erro do serviço SMTP é considerado uma falha.</span><span class="sxs-lookup"><span data-stu-id="c978e-187">Receiving an error return code from the SMTP service is considered a failure.</span></span>

## <a name="examples"></a><span data-ttu-id="c978e-188">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c978e-188">Examples</span></span>

<span data-ttu-id="c978e-189">Para obter um exemplo de como usar o **SMTPEventConsumer** para criar um consumidor, consulte [enviando email com base em um evento](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="c978e-189">For an example of using **SMTPEventConsumer** to create a consumer, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span> <span data-ttu-id="c978e-190">Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="c978e-190">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c978e-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c978e-191">Requirements</span></span>



| <span data-ttu-id="c978e-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="c978e-192">Requirement</span></span> | <span data-ttu-id="c978e-193">Valor</span><span class="sxs-lookup"><span data-stu-id="c978e-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c978e-194">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c978e-194">Minimum supported client</span></span><br/> | <span data-ttu-id="c978e-195">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c978e-195">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c978e-196">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c978e-196">Minimum supported server</span></span><br/> | <span data-ttu-id="c978e-197">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c978e-197">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c978e-198">Namespace</span><span class="sxs-lookup"><span data-stu-id="c978e-198">Namespace</span></span><br/>                | <span data-ttu-id="c978e-199">\\Assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="c978e-199">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="c978e-200">MOF</span><span class="sxs-lookup"><span data-stu-id="c978e-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c978e-201"><dt>Smtpcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c978e-201"><dt>Smtpcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="c978e-202">DLL</span><span class="sxs-lookup"><span data-stu-id="c978e-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c978e-203"><dt>Smtpcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c978e-203"><dt>Smtpcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c978e-204">Confira também</span><span class="sxs-lookup"><span data-stu-id="c978e-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c978e-205">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="c978e-205">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> <dt>

[<span data-ttu-id="c978e-206">Classes de consumidor padrão</span><span class="sxs-lookup"><span data-stu-id="c978e-206">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="c978e-207">Enviando email com base em um evento</span><span class="sxs-lookup"><span data-stu-id="c978e-207">Sending Email Based on an Event</span></span>](sending-e-mail-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="c978e-208">Criando um consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="c978e-208">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="c978e-209">Recebendo eventos em todos os momentos</span><span class="sxs-lookup"><span data-stu-id="c978e-209">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

 




