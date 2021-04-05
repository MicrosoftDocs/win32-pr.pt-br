---
title: Elemento opcode (OpcodeListType)
description: Contém um valor numérico que identifica a atividade ou um ponto dentro de uma atividade que o aplicativo estava executando quando ele gerou o evento (por exemplo, inicialização ou fechamento).
ms.assetid: 8c5cfbd3-6a74-452c-a12f-41d663426e2c
keywords:
- EventLog do elemento opcode
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9d02b77b4a36bac26d52d7bf8d849eab8731d27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086338"
---
# <a name="opcode-opcodelisttype-element"></a><span data-ttu-id="6d5c7-104">Elemento opcode (OpcodeListType)</span><span class="sxs-lookup"><span data-stu-id="6d5c7-104">opcode (OpcodeListType) Element</span></span>

<span data-ttu-id="6d5c7-105">Contém um valor numérico que identifica a atividade ou um ponto dentro de uma atividade que o aplicativo estava executando quando ele gerou o evento (por exemplo, inicialização ou fechamento).</span><span class="sxs-lookup"><span data-stu-id="6d5c7-105">Contains a numeric value that identifies the activity or a point within an activity that the application was performing when it raised the event (for example, initialization or closing).</span></span>

``` syntax
<xs:element name="opcode"
    type="OpcodeType"
 />
```

<span data-ttu-id="6d5c7-106">O elemento **opcode** é definido pelo tipo complexo [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6d5c7-106">The **opcode** element is defined by the [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d5c7-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d5c7-107">Requirements</span></span>



| <span data-ttu-id="6d5c7-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d5c7-108">Requirement</span></span> | <span data-ttu-id="6d5c7-109">Valor</span><span class="sxs-lookup"><span data-stu-id="6d5c7-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6d5c7-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d5c7-110">Minimum supported client</span></span><br/> | <span data-ttu-id="6d5c7-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6d5c7-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6d5c7-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d5c7-112">Minimum supported server</span></span><br/> | <span data-ttu-id="6d5c7-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6d5c7-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d5c7-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d5c7-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="6d5c7-115">**Elementos pai**</span><span class="sxs-lookup"><span data-stu-id="6d5c7-115">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="6d5c7-116">**opcodes (TaskType)**</span><span class="sxs-lookup"><span data-stu-id="6d5c7-116">**opcodes (TaskType)**</span></span>](eventmanifestschema-opcodes-tasktype-element.md)
</dt> <dt>

[<span data-ttu-id="6d5c7-117">**opcodes (ProviderType)**</span><span class="sxs-lookup"><span data-stu-id="6d5c7-117">**opcodes (ProviderType)**</span></span>](eventmanifestschema-opcodes-providertype-element.md)
</dt> <dt>

[<span data-ttu-id="6d5c7-118">**opcodes (MetadataType)**</span><span class="sxs-lookup"><span data-stu-id="6d5c7-118">**opcodes (MetadataType)**</span></span>](eventmanifestschema-opcodes-metadatatype-element.md)
</dt> </dl>

 

 





