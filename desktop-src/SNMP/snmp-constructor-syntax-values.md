---
title: Valores de sintaxe do Construtor SNMP (SNMP. h)
description: Os valores de sintaxe do Construtor SNMP descrevem os tipos que são compatíveis com o padrão de codificação (ASN. 1) de notação de sintaxe abstrata.
ms.assetid: 8e3b6e00-51cf-4e39-a68e-dcf8fbe8ab3b
topic_type:
- apiref
api_name:
- ASN_SEQUENCE
- ASN_SEQUENCEOF
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484e58d7a92a3c75408db3160362d84e7891b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085434"
---
# <a name="snmp-constructor-syntax-values"></a><span data-ttu-id="52d8f-103">Valores de sintaxe do Construtor SNMP</span><span class="sxs-lookup"><span data-stu-id="52d8f-103">SNMP Constructor Syntax Values</span></span>

<span data-ttu-id="52d8f-104">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="52d8f-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="52d8f-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="52d8f-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="52d8f-106">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="52d8f-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="52d8f-107">Os valores de sintaxe do Construtor SNMP descrevem os tipos que são compatíveis com o padrão de codificação (ASN. 1) de notação de sintaxe abstrata.</span><span class="sxs-lookup"><span data-stu-id="52d8f-107">The SNMP Constructor Syntax Values describe types that are compliant with the Abstract Syntax Notation One (ASN.1) encoding standard.</span></span>



| <span data-ttu-id="52d8f-108">Constante</span><span class="sxs-lookup"><span data-stu-id="52d8f-108">Constant</span></span>                                                                                                                                                         | <span data-ttu-id="52d8f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="52d8f-109">Description</span></span>                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="ASN_SEQUENCE"></span><span id="asn_sequence"></span><dl> <span data-ttu-id="52d8f-110"><dt>**\_sequência ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="52d8f-110"><dt>**ASN\_SEQUENCE**</dt></span></span> </dl>       | <span data-ttu-id="52d8f-111">Indica que a mensagem é uma sequência ASN.</span><span class="sxs-lookup"><span data-stu-id="52d8f-111">Indicates that the message is an ASN sequence.</span></span><br/> |
| <span id="ASN_SEQUENCEOF"></span><span id="asn_sequenceof"></span><dl> <span data-ttu-id="52d8f-112"><dt>**\_SEQUENCEOF ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="52d8f-112"><dt>**ASN\_SEQUENCEOF**</dt></span></span> </dl> | <span data-ttu-id="52d8f-113">Consulte a \_ sequência ASN.</span><span class="sxs-lookup"><span data-stu-id="52d8f-113">See ASN\_SEQUENCE.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="52d8f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52d8f-114">Requirements</span></span>



| <span data-ttu-id="52d8f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="52d8f-115">Requirement</span></span> | <span data-ttu-id="52d8f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="52d8f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="52d8f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52d8f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="52d8f-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52d8f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="52d8f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52d8f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="52d8f-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52d8f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="52d8f-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="52d8f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="52d8f-122"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="52d8f-122"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52d8f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="52d8f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52d8f-124">Visão geral do Protocolo SNMP</span><span class="sxs-lookup"><span data-stu-id="52d8f-124">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="52d8f-125">Referência de SNMP</span><span class="sxs-lookup"><span data-stu-id="52d8f-125">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="52d8f-126">Constantes SNMP</span><span class="sxs-lookup"><span data-stu-id="52d8f-126">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

