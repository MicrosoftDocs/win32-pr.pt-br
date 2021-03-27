---
description: Essa classe é a classe de tipo de evento para ALPC aguardar eventos de resposta. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 9aaa2c93-41cc-4025-80f9-b7740a37c4d8
title: Classe ALPC_Wait_For_Reply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_Reply
- ALPC_Wait_For_Reply.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 898077511db25ec7f53bc075ecb845d04e540626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967445"
---
# <a name="alpc_wait_for_reply-class"></a><span data-ttu-id="b1ea3-104">ALPC \_ aguardar \_ a \_ classe de resposta</span><span class="sxs-lookup"><span data-stu-id="b1ea3-104">ALPC\_Wait\_For\_Reply class</span></span>

<span data-ttu-id="b1ea3-105">Essa classe é a classe de tipo de evento para ALPC aguardar eventos de resposta.</span><span class="sxs-lookup"><span data-stu-id="b1ea3-105">This class is the event type class for ALPC wait for reply events.</span></span>

<span data-ttu-id="b1ea3-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="b1ea3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1ea3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1ea3-107">Syntax</span></span>

``` syntax
[EventType(35), EventTypeName("ALPC-Wait-For-Reply")]
class ALPC_Wait_For_Reply : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="b1ea3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b1ea3-108">Members</span></span>

<span data-ttu-id="b1ea3-109">A **\_ espera \_ do ALPC para \_** a classe Reply tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b1ea3-109">The **ALPC\_Wait\_For\_Reply** class has these types of members:</span></span>

-   [<span data-ttu-id="b1ea3-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b1ea3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1ea3-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b1ea3-111">Properties</span></span>

<span data-ttu-id="b1ea3-112">A **\_ espera \_ do ALPC para \_** a classe Reply tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b1ea3-112">The **ALPC\_Wait\_For\_Reply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1ea3-113">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="b1ea3-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ea3-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1ea3-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1ea3-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ea3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1ea3-116">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b1ea3-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1ea3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1ea3-117">Requirements</span></span>



| <span data-ttu-id="b1ea3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1ea3-118">Requirement</span></span> | <span data-ttu-id="b1ea3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b1ea3-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b1ea3-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1ea3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b1ea3-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1ea3-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b1ea3-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1ea3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b1ea3-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b1ea3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




