---
description: A estrutura de PROTOCOLtable contém uma lista de protocolos.
ms.assetid: dad2b228-5916-44fe-b78e-ebc6507dc555
title: Estrutura de PROTOCOLtable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3ad79beca7ce79611747a02704ffc05da5fc3d4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759356"
---
# <a name="protocoltable-structure"></a><span data-ttu-id="94122-103">Estrutura de PROTOCOLtable</span><span class="sxs-lookup"><span data-stu-id="94122-103">PROTOCOLTABLE structure</span></span>

<span data-ttu-id="94122-104">A estrutura de **protocoltable** contém uma lista de protocolos.</span><span class="sxs-lookup"><span data-stu-id="94122-104">The **PROTOCOLTABLE** structure contains a list of protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="94122-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94122-105">Syntax</span></span>


```C++
typedef struct _PROTOCOLTABLE {
  DWORD     nProtocols;
  HPROTOCOL hProtocol[1];
} PROTOCOLTABLE;
```



## <a name="members"></a><span data-ttu-id="94122-106">Membros</span><span class="sxs-lookup"><span data-stu-id="94122-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="94122-107">**nProtocols**</span><span class="sxs-lookup"><span data-stu-id="94122-107">**nProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="94122-108">Número de protocolos habilitados.</span><span class="sxs-lookup"><span data-stu-id="94122-108">Number of protocols that are enabled.</span></span>

</dd> <dt>

<span data-ttu-id="94122-109">**hProtocol**</span><span class="sxs-lookup"><span data-stu-id="94122-109">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="94122-110">Matriz de identificadores para protocolos habilitados.</span><span class="sxs-lookup"><span data-stu-id="94122-110">Array of handles to enabled protocols.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94122-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94122-111">Requirements</span></span>



| <span data-ttu-id="94122-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="94122-112">Requirement</span></span> | <span data-ttu-id="94122-113">Valor</span><span class="sxs-lookup"><span data-stu-id="94122-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="94122-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94122-114">Minimum supported client</span></span><br/> | <span data-ttu-id="94122-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="94122-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="94122-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94122-116">Minimum supported server</span></span><br/> | <span data-ttu-id="94122-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="94122-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="94122-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="94122-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="94122-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="94122-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




