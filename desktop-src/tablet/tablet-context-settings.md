---
description: Contém informações usadas na criação de um contexto do Tablet.
ms.assetid: 10466c23-f4cb-4205-886b-d85a2f530afe
title: Estrutura de TABLET_CONTEXT_SETTINGS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_CONTEXT_SETTINGS
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9357281409ed4c48b4c6013a7a2be2997d58b094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922836"
---
# <a name="tablet_context_settings-structure"></a><span data-ttu-id="3d14e-103">Estrutura de configurações de \_ contexto do Tablet \_</span><span class="sxs-lookup"><span data-stu-id="3d14e-103">TABLET\_CONTEXT\_SETTINGS structure</span></span>

<span data-ttu-id="3d14e-104">Contém informações usadas na criação de um contexto do Tablet.</span><span class="sxs-lookup"><span data-stu-id="3d14e-104">Contains information used in creating a tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d14e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d14e-105">Syntax</span></span>


```C++
typedef struct _TABLET_CONTEXT_SETTINGS {
  ULONG cPktProps;
  GUID  *pguidPktProps;
  ULONG cPktBtns;
  GUID  *pguidPktBtns;
  DWORD *pdwBtnDnMask;
  DWORD *pdwBtnUpMask;
  LONG  lXMargin;
  LONG  lYMargin;
} TABLET_CONTEXT_SETTINGS;
```



## <a name="members"></a><span data-ttu-id="3d14e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="3d14e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3d14e-107">**cPktProps**</span><span class="sxs-lookup"><span data-stu-id="3d14e-107">**cPktProps**</span></span>
</dt> <dd>

<span data-ttu-id="3d14e-108">O número de propriedades em um pacote.</span><span class="sxs-lookup"><span data-stu-id="3d14e-108">The number of properties in a packet.</span></span>

</dd> <dt>

<span data-ttu-id="3d14e-109">**pguidPktProps**</span><span class="sxs-lookup"><span data-stu-id="3d14e-109">**pguidPktProps**</span></span>
</dt> <dd>

<span data-ttu-id="3d14e-110">Identificadores exclusivos para as propriedades do pacote.</span><span class="sxs-lookup"><span data-stu-id="3d14e-110">Unique identifiers for the packet properties.</span></span>

</dd> <dt>

<span data-ttu-id="3d14e-111">**cPktBtns**</span><span class="sxs-lookup"><span data-stu-id="3d14e-111">**cPktBtns**</span></span>
</dt> <dd>

<span data-ttu-id="3d14e-112">O número de botões.</span><span class="sxs-lookup"><span data-stu-id="3d14e-112">The number of buttons.</span></span>

</dd> <dt>

<span data-ttu-id="3d14e-113">**pguidPktBtns**</span><span class="sxs-lookup"><span data-stu-id="3d14e-113">**pguidPktBtns**</span></span>
</dt> <dd>

<span data-ttu-id="3d14e-114">Identificadores exclusivos para os botões.</span><span class="sxs-lookup"><span data-stu-id="3d14e-114">Unique identifiers for the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="3d14e-115">**pdwBtnDnMask**</span><span class="sxs-lookup"><span data-stu-id="3d14e-115">**pdwBtnDnMask**</span></span>
</dt> <dd>

<span data-ttu-id="3d14e-116">A máscara do botão para baixo.</span><span class="sxs-lookup"><span data-stu-id="3d14e-116">The button down mask.</span></span>

</dd> <dt>

<span data-ttu-id="3d14e-117">**pdwBtnUpMask**</span><span class="sxs-lookup"><span data-stu-id="3d14e-117">**pdwBtnUpMask**</span></span>
</dt> <dd>

<span data-ttu-id="3d14e-118">A máscara de botão para cima.</span><span class="sxs-lookup"><span data-stu-id="3d14e-118">The button up mask.</span></span>

</dd> <dt>

<span data-ttu-id="3d14e-119">**lXMargin**</span><span class="sxs-lookup"><span data-stu-id="3d14e-119">**lXMargin**</span></span>
</dt> <dd>

<span data-ttu-id="3d14e-120">A margem de direção X.</span><span class="sxs-lookup"><span data-stu-id="3d14e-120">The X direction margin.</span></span>

</dd> <dt>

<span data-ttu-id="3d14e-121">**lYMargin**</span><span class="sxs-lookup"><span data-stu-id="3d14e-121">**lYMargin**</span></span>
</dt> <dd>

<span data-ttu-id="3d14e-122">A margem de direção Y.</span><span class="sxs-lookup"><span data-stu-id="3d14e-122">The Y direction margin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d14e-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d14e-123">Remarks</span></span>

<span data-ttu-id="3d14e-124">Normalmente, um aplicativo obtém os valores padrão do [**método ITablet:: GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica os valores para atender às suas necessidades e, em seguida, passa a estrutura de configurações modificada para o [**método ITablet:: CreateContext**](itablet-createcontext.md).</span><span class="sxs-lookup"><span data-stu-id="3d14e-124">Typically, an application obtains the default values from the [**ITablet::GetDefaultContextSettings Method**](itablet-getdefaultcontextsettings.md), modifies values to suit their needs, and then passes the modified settings structure to the [**ITablet::CreateContext Method**](itablet-createcontext.md).</span></span>

<span data-ttu-id="3d14e-125">Essa estrutura determina quais eventos um aplicativo receberá, como eles serão processados e como eles serão entregues ao aplicativo ou ao próprio Windows.</span><span class="sxs-lookup"><span data-stu-id="3d14e-125">This structure determines what events an application will get, how they will be processed, and how they will be delivered to the application or to Windows itself.</span></span>

<span data-ttu-id="3d14e-126">As máscaras de botão, em conjunto, determinam quais tipos de eventos serão processados pelo contexto.</span><span class="sxs-lookup"><span data-stu-id="3d14e-126">The button masks together determine what kinds of events will be processed by the context.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d14e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d14e-127">Requirements</span></span>



| <span data-ttu-id="3d14e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d14e-128">Requirement</span></span> | <span data-ttu-id="3d14e-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3d14e-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="3d14e-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d14e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3d14e-131">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3d14e-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3d14e-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d14e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3d14e-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3d14e-133">None supported</span></span><br/>                                     |



 

 




