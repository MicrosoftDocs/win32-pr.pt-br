---
description: Essa classe é a classe de tipo de evento para ALPC receber eventos de mensagem. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 6aa98240-e559-47b6-ae55-5a6379e08077
title: Classe ALPC_Receive_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Receive_Message
- ALPC_Receive_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 886d3595caa283d5b09939a506952633d2350d41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967449"
---
# <a name="alpc_receive_message-class"></a><span data-ttu-id="b1f4e-104">Classe de mensagem de \_ recebimento ALPC \_</span><span class="sxs-lookup"><span data-stu-id="b1f4e-104">ALPC\_Receive\_Message class</span></span>

<span data-ttu-id="b1f4e-105">Essa classe é a classe de tipo de evento para ALPC receber eventos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b1f4e-105">This class is the event type class for ALPC receive message events.</span></span>

<span data-ttu-id="b1f4e-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="b1f4e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1f4e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1f4e-107">Syntax</span></span>

``` syntax
[EventType(34), EventTypeName("ALPC-Receive-Message")]
class ALPC_Receive_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="b1f4e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b1f4e-108">Members</span></span>

<span data-ttu-id="b1f4e-109">A classe de **\_ \_ mensagem de recebimento ALPC** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b1f4e-109">The **ALPC\_Receive\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="b1f4e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b1f4e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1f4e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b1f4e-111">Properties</span></span>

<span data-ttu-id="b1f4e-112">A classe de **\_ \_ mensagem de recebimento ALPC** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b1f4e-112">The **ALPC\_Receive\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1f4e-113">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="b1f4e-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1f4e-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1f4e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1f4e-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1f4e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1f4e-116">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b1f4e-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1f4e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1f4e-117">Requirements</span></span>



| <span data-ttu-id="b1f4e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1f4e-118">Requirement</span></span> | <span data-ttu-id="b1f4e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b1f4e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b1f4e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1f4e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b1f4e-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1f4e-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b1f4e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1f4e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b1f4e-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b1f4e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




