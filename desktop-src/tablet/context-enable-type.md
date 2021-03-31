---
description: Indica se as mensagens de contexto devem ser enviadas para o procedimento de janela da janela de propriedade.
ms.assetid: 57ecf10a-8a02-4353-b916-9080ebc0b270
title: Enumeração de CONTEXT_ENABLE_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONTEXT_ENABLE_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: cd741eeff1cc3e2ce055a84dd646c3aa2563f217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662940"
---
# <a name="context_enable_type-enumeration"></a><span data-ttu-id="bad12-103">\_Enumeração de tipo de habilitação de contexto \_</span><span class="sxs-lookup"><span data-stu-id="bad12-103">CONTEXT\_ENABLE\_TYPE enumeration</span></span>

<span data-ttu-id="bad12-104">Indica se as mensagens de contexto devem ser enviadas para o procedimento de janela da janela de propriedade.</span><span class="sxs-lookup"><span data-stu-id="bad12-104">Indicates whether context messages should be sent to the owning window's window procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="bad12-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bad12-105">Syntax</span></span>


```C++
typedef enum _CONTEXT_ENABLE_TYPE { 
  CONTEXT_ENABLE   = 1,
  CONTEXT_DISABLE  = 2
} CONTEXT_ENABLE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="bad12-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="bad12-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bad12-107"><span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**\_habilitação de contexto**</span><span class="sxs-lookup"><span data-stu-id="bad12-107"><span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**CONTEXT\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="bad12-108">O contexto do Tablet deve ser habilitado, o que resulta em mensagens de contexto sendo enviadas para o procedimento de janela da janela de propriedade.</span><span class="sxs-lookup"><span data-stu-id="bad12-108">The tablet context should be enabled, resulting in context messages being sent to the owning window's window procedure.</span></span>

</dd> <dt>

<span data-ttu-id="bad12-109"><span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**\_desabilitar contexto**</span><span class="sxs-lookup"><span data-stu-id="bad12-109"><span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**CONTEXT\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="bad12-110">O contexto do Tablet deve ser desabilitado, impedindo que outras mensagens de contexto sejam enviadas para o procedimento de janela da janela de propriedade ou coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="bad12-110">The tablet context should be disabled, preventing any further context messages from being sent to the owning window's window procedure or event sink.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bad12-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bad12-111">Requirements</span></span>



| <span data-ttu-id="bad12-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="bad12-112">Requirement</span></span> | <span data-ttu-id="bad12-113">Valor</span><span class="sxs-lookup"><span data-stu-id="bad12-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="bad12-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bad12-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bad12-115">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bad12-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bad12-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bad12-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bad12-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bad12-117">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="bad12-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="bad12-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bad12-119">**Método ITablet:: CreateContext**</span><span class="sxs-lookup"><span data-stu-id="bad12-119">**ITablet::CreateContext Method**</span></span>](itablet-createcontext.md)
</dt> </dl>

 

 




