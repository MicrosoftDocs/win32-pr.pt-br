---
description: Essa classe é a classe de tipo de evento para ALPC enviar eventos de mensagem. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 7f12259b-f737-4bef-9dea-2ffe3517e0da
title: Classe ALPC_Send_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Send_Message
- ALPC_Send_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: c9437626341f0ac57136645d40a8389436e8af1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090800"
---
# <a name="alpc_send_message-class"></a><span data-ttu-id="843b6-104">Classe de mensagem de \_ envio ALPC \_</span><span class="sxs-lookup"><span data-stu-id="843b6-104">ALPC\_Send\_Message class</span></span>

<span data-ttu-id="843b6-105">Essa classe é a classe de tipo de evento para ALPC enviar eventos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="843b6-105">This class is the event type class for ALPC send message events.</span></span>

<span data-ttu-id="843b6-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="843b6-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="843b6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="843b6-107">Syntax</span></span>

``` syntax
[EventType(33), EventTypeName("ALPC-Send-Message")]
class ALPC_Send_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="843b6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="843b6-108">Members</span></span>

<span data-ttu-id="843b6-109">A classe de **\_ \_ mensagem de envio ALPC** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="843b6-109">The **ALPC\_Send\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="843b6-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="843b6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="843b6-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="843b6-111">Properties</span></span>

<span data-ttu-id="843b6-112">A classe de **\_ \_ mensagem de envio ALPC** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="843b6-112">The **ALPC\_Send\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="843b6-113">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="843b6-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="843b6-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="843b6-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="843b6-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="843b6-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="843b6-116">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="843b6-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="843b6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="843b6-117">Requirements</span></span>



| <span data-ttu-id="843b6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="843b6-118">Requirement</span></span> | <span data-ttu-id="843b6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="843b6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="843b6-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="843b6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="843b6-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="843b6-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="843b6-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="843b6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="843b6-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="843b6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




