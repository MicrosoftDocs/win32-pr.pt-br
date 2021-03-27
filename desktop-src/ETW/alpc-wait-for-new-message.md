---
description: Essa classe é a classe de tipo de evento para ALPC aguardar novos eventos de mensagem. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 7f7fa4b8-ed12-49a0-a84e-37f66af4f5f1
title: Classe ALPC_Wait_For_New_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_New_Message
- ALPC_Wait_For_New_Message.IsServerPort
- ALPC_Wait_For_New_Message.PortName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75cbda11a2a27eec811f8ff47966d12c6a86cf07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967446"
---
# <a name="alpc_wait_for_new_message-class"></a><span data-ttu-id="ccb90-104">ALPC \_ aguardar \_ a \_ nova \_ classe de mensagem</span><span class="sxs-lookup"><span data-stu-id="ccb90-104">ALPC\_Wait\_For\_New\_Message class</span></span>

<span data-ttu-id="ccb90-105">Essa classe é a classe de tipo de evento para ALPC aguardar novos eventos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ccb90-105">This class is the event type class for ALPC wait for new message events.</span></span>

<span data-ttu-id="ccb90-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="ccb90-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccb90-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccb90-107">Syntax</span></span>

``` syntax
[EventType(36), EventTypeName("ALPC-Wait-For-New-Message")]
class ALPC_Wait_For_New_Message : ALPC
{
  uint32 IsServerPort;
  string PortName;
};
```

## <a name="members"></a><span data-ttu-id="ccb90-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ccb90-108">Members</span></span>

<span data-ttu-id="ccb90-109">A classe de **\_ espera ALPC \_ de \_ nova \_ mensagem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ccb90-109">The **ALPC\_Wait\_For\_New\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="ccb90-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ccb90-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ccb90-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ccb90-111">Properties</span></span>

<span data-ttu-id="ccb90-112">A classe de **\_ espera ALPC \_ de \_ nova \_ mensagem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ccb90-112">The **ALPC\_Wait\_For\_New\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ccb90-113">**IsServerPort**</span><span class="sxs-lookup"><span data-stu-id="ccb90-113">**IsServerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccb90-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ccb90-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ccb90-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ccb90-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccb90-116">Indica se a porta é uma porta de servidor.</span><span class="sxs-lookup"><span data-stu-id="ccb90-116">Indicates if the port is a server port.</span></span>

</dd> <dt>

<span data-ttu-id="ccb90-117">**Portaname**</span><span class="sxs-lookup"><span data-stu-id="ccb90-117">**PortName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccb90-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ccb90-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccb90-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ccb90-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccb90-120">Cadeia de caracteres que contém o nome da porta na qual o ALPC está aguardando.</span><span class="sxs-lookup"><span data-stu-id="ccb90-120">String that contains the name of the port on which ALPC is waiting.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ccb90-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccb90-121">Requirements</span></span>



| <span data-ttu-id="ccb90-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccb90-122">Requirement</span></span> | <span data-ttu-id="ccb90-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ccb90-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ccb90-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccb90-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ccb90-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ccb90-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ccb90-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccb90-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ccb90-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ccb90-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




