---
description: Descreve os dados de objeto do coletor de exibição incluídos em uma notificação ou resultado da notificação.
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: Estrutura de WFD_DISPLAY_SINK_OBJECT_HEADER (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: cdefd6b0b91fefb0f42a6e37e7584f7cd966884b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828234"
---
# <a name="wfd_display_sink_object_header-structure"></a><span data-ttu-id="f8977-103">\_Estrutura de \_ cabeçalho de objeto do coletor de vídeo WFD \_ \_</span><span class="sxs-lookup"><span data-stu-id="f8977-103">WFD\_DISPLAY\_SINK\_OBJECT\_HEADER structure</span></span>

<span data-ttu-id="f8977-104">A estrutura do **cabeçalho do objeto do \_ coletor de vídeo \_ \_ \_ WFD** descreve os dados do objeto do coletor de vídeo incluídos em uma notificação ou resultado da notificação.</span><span class="sxs-lookup"><span data-stu-id="f8977-104">The **WFD\_DISPLAY\_SINK\_OBJECT\_HEADER** structure describes the display sink object data included in a notification or notification result.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8977-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8977-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Length;
} WFD_DISPLAY_SINK_OBJECT_HEADER, *PWFD_DISPLAY_SINK_OBJECT_HEADER;
```



## <a name="members"></a><span data-ttu-id="f8977-106">Membros</span><span class="sxs-lookup"><span data-stu-id="f8977-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f8977-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f8977-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="f8977-108">O tipo do objeto do coletor de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f8977-108">The type of the display sink object.</span></span> <span data-ttu-id="f8977-109">Você pode usar o **tipo de objeto do coletor de vídeo WFD do identificador \_ \_ \_ \_ \_ padrão** que é definido como o valor 1.</span><span class="sxs-lookup"><span data-stu-id="f8977-109">You can use the identifier **WFD\_DISPLAY\_SINK\_OBJECT\_TYPE\_DEFAULT** which is defined as the value 1.</span></span>

</dd> <dt>

<span data-ttu-id="f8977-110">**Revisão**</span><span class="sxs-lookup"><span data-stu-id="f8977-110">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="f8977-111">A versão de revisão do objeto do coletor de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f8977-111">The revision version of the display sink object.</span></span> <span data-ttu-id="f8977-112">Você pode usar a **revisão de objeto do coletor de exibição WFD do identificador \_ \_ \_ \_ \_ versão \_ 1** , que é definida como o valor 1.</span><span class="sxs-lookup"><span data-stu-id="f8977-112">You can use the identifier **WFD\_DISPLAY\_SINK\_OBJECT\_REVISION\_VERSION\_1** which is defined as the value 1.</span></span>

</dd> <dt>

<span data-ttu-id="f8977-113">**Comprimento**</span><span class="sxs-lookup"><span data-stu-id="f8977-113">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="f8977-114">O comprimento dos dados no resultado da notificação ou da notificação.</span><span class="sxs-lookup"><span data-stu-id="f8977-114">The length of the data in the notification or notification result.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8977-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8977-115">Requirements</span></span>



| <span data-ttu-id="f8977-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8977-116">Requirement</span></span> | <span data-ttu-id="f8977-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f8977-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f8977-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8977-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f8977-119">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f8977-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f8977-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8977-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f8977-121">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="f8977-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f8977-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8977-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8977-123"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8977-123"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




