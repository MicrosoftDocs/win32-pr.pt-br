---
description: Especifica o tipo de processo que é identificado na estrutura de \_ saída D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ .
ms.assetid: 8878905e-f55b-4dbc-9608-da0082daf673
title: Enumeração de D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1b2fdb7384ff868b02f54650de9662b297ce39db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089765"
---
# <a name="d3dauthenticatedchannel_processidentifiertype-enumeration"></a><span data-ttu-id="74131-103">\_Enumeração D3DAUTHENTICATEDCHANNEL PROCESSIDENTIFIERTYPE</span><span class="sxs-lookup"><span data-stu-id="74131-103">D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE enumeration</span></span>

<span data-ttu-id="74131-104">Especifica o tipo de processo que é identificado na estrutura [**de \_ \_ saída D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) .</span><span class="sxs-lookup"><span data-stu-id="74131-104">Specifies the type of process that is identified in the [**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="74131-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="74131-105">Syntax</span></span>


```C++
typedef enum  { 
  PROCESSIDTYPE_UNKNOWN  = 0,
  PROCESSIDTYPE_DWM      = 1,
  PROCESSIDTYPE_HANDLE   = 2
} D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE;
```



## <a name="constants"></a><span data-ttu-id="74131-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="74131-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="74131-107"><span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDtype \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="74131-107"><span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDTYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="74131-108">Tipo de processo desconhecido.</span><span class="sxs-lookup"><span data-stu-id="74131-108">Unknown process type.</span></span>

</dd> <dt>

<span data-ttu-id="74131-109"><span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**DWM do PROCESSIDtype \_**</span><span class="sxs-lookup"><span data-stu-id="74131-109"><span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**PROCESSIDTYPE\_DWM**</span></span>
</dt> <dd>

<span data-ttu-id="74131-110">Processo de Gerenciador de Janelas da Área de Trabalho (DWM).</span><span class="sxs-lookup"><span data-stu-id="74131-110">Desktop Window Manager (DWM) process.</span></span>

</dd> <dt>

<span data-ttu-id="74131-111"><span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**identificador de PROCESSIDtype \_**</span><span class="sxs-lookup"><span data-stu-id="74131-111"><span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**PROCESSIDTYPE\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="74131-112">Identificador para um processo.</span><span class="sxs-lookup"><span data-stu-id="74131-112">Handle to a process.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74131-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74131-113">Requirements</span></span>



| <span data-ttu-id="74131-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="74131-114">Requirement</span></span> | <span data-ttu-id="74131-115">Valor</span><span class="sxs-lookup"><span data-stu-id="74131-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74131-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74131-116">Minimum supported client</span></span><br/> | <span data-ttu-id="74131-117">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="74131-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="74131-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74131-118">Minimum supported server</span></span><br/> | <span data-ttu-id="74131-119">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="74131-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="74131-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74131-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="74131-121"><dt>D3d9types. h (incluir D3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74131-121"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74131-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="74131-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74131-123">Enumerações de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="74131-123">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> </dl>

 

 




