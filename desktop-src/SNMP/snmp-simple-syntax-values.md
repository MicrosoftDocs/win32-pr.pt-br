---
title: Valores de sintaxe simples SNMP (SNMP. h)
description: Os valores de sintaxe simples do SNMP são usados para indicar um tipo de variável SNMP.
ms.assetid: 42b681e5-721d-4d41-bc1a-c9f0005cde87
topic_type:
- apiref
api_name:
- ASN_INTEGER
- ASN_BITS
- ASN_OCTETSTRING
- ASN_NULL
- ASN_OBJECTIDENTIFIER
- ASN_INTEGER32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee6a40b4f63b7ce701b8232b310b2f73bac42d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085787"
---
# <a name="snmp-simple-syntax-values"></a><span data-ttu-id="c2b3f-103">Valores de sintaxe simples SNMP</span><span class="sxs-lookup"><span data-stu-id="c2b3f-103">SNMP Simple Syntax Values</span></span>

<span data-ttu-id="c2b3f-104">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="c2b3f-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c2b3f-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c2b3f-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c2b3f-106">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="c2b3f-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="c2b3f-107">Os valores de sintaxe simples do SNMP são usados para indicar um tipo de variável SNMP.</span><span class="sxs-lookup"><span data-stu-id="c2b3f-107">The SNMP Simple Syntax Values are used to indicate an SNMP variable type.</span></span>



| <span data-ttu-id="c2b3f-108">Constante</span><span class="sxs-lookup"><span data-stu-id="c2b3f-108">Constant</span></span>                                                                                                                                                                           | <span data-ttu-id="c2b3f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2b3f-109">Description</span></span>                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="ASN_INTEGER"></span><span id="asn_integer"></span><dl> <span data-ttu-id="c2b3f-110"><dt>**\_inteiro ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="c2b3f-110"><dt>**ASN\_INTEGER**</dt></span></span> </dl>                            | <span data-ttu-id="c2b3f-111">Indica uma variável de inteiro com sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c2b3f-111">Indicates a 32-bit signed integer variable.</span></span><br/>                |
| <span id="ASN_BITS"></span><span id="asn_bits"></span><dl> <span data-ttu-id="c2b3f-112"><dt>**\_bits ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="c2b3f-112"><dt>**ASN\_BITS**</dt></span></span> </dl>                                     | <span data-ttu-id="c2b3f-113">Indica uma variável que é uma enumeração de bits nomeados.</span><span class="sxs-lookup"><span data-stu-id="c2b3f-113">Indicates a variable that is an enumeration of named bits.</span></span><br/> |
| <span id="ASN_OCTETSTRING"></span><span id="asn_octetstring"></span><dl> <span data-ttu-id="c2b3f-114"><dt>**\_octetstring ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="c2b3f-114"><dt>**ASN\_OCTETSTRING**</dt></span></span> </dl>                | <span data-ttu-id="c2b3f-115">Indica uma variável de cadeia de caracteres de octeto.</span><span class="sxs-lookup"><span data-stu-id="c2b3f-115">Indicates an octet string variable.</span></span><br/>                        |
| <span id="ASN_NULL"></span><span id="asn_null"></span><dl> <span data-ttu-id="c2b3f-116"><dt>**ASN ( \_ nulo)**</dt></span><span class="sxs-lookup"><span data-stu-id="c2b3f-116"><dt>**ASN\_NULL**</dt></span></span> </dl>                                     | <span data-ttu-id="c2b3f-117">Indica um valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="c2b3f-117">Indicates a **NULL** value.</span></span><br/>                                |
| <span id="ASN_OBJECTIDENTIFIER"></span><span id="asn_objectidentifier"></span><dl> <span data-ttu-id="c2b3f-118"><dt>**objectidentifier ASN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2b3f-118"><dt>**ASN\_OBJECTIDENTIFIER**</dt></span></span> </dl> | <span data-ttu-id="c2b3f-119">Indica uma variável de identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="c2b3f-119">Indicates an object identifier variable.</span></span><br/>                   |
| <span id="ASN_INTEGER32"></span><span id="asn_integer32"></span><dl> <span data-ttu-id="c2b3f-120"><dt>**\_INTEGER32 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="c2b3f-120"><dt>**ASN\_INTEGER32**</dt></span></span> </dl>                      | <span data-ttu-id="c2b3f-121">Indica um valor inteiro com sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c2b3f-121">Indicates a 32-bit signed integer value.</span></span><br/>                   |



## <a name="requirements"></a><span data-ttu-id="c2b3f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2b3f-122">Requirements</span></span>



| <span data-ttu-id="c2b3f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2b3f-123">Requirement</span></span> | <span data-ttu-id="c2b3f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c2b3f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c2b3f-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2b3f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c2b3f-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2b3f-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="c2b3f-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2b3f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c2b3f-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2b3f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c2b3f-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c2b3f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2b3f-130"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2b3f-130"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2b3f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2b3f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2b3f-132">Visão geral do Protocolo SNMP</span><span class="sxs-lookup"><span data-stu-id="c2b3f-132">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="c2b3f-133">Referência de SNMP</span><span class="sxs-lookup"><span data-stu-id="c2b3f-133">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="c2b3f-134">Constantes SNMP</span><span class="sxs-lookup"><span data-stu-id="c2b3f-134">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

