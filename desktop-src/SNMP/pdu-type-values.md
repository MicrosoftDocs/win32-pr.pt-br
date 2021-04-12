---
title: Valores de tipo de PDU (SNMP. h)
description: Os valores do tipo PDU são usados no \_ campo tipo PDU da PDU para descrever seu tipo.
ms.assetid: 9d7a3f1c-7940-428b-a4e0-3c9e61dd755f
topic_type:
- apiref
api_name:
- SNMP_PDU_GET
- SNMP_PDU_GETNEXT
- SNMP_PDU_RESPONSE
- SNMP_PDU_SET
- SNMP_PDU_V1TRAP
- SNMP_PDU_GETBULK
- SNMP_PDU_INFORM
- SNMP_PDU_TRAP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90086de73e53eb89b1f3e3925ae7669777a6a088
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455718"
---
# <a name="pdu-type-values"></a><span data-ttu-id="4ed18-103">Valores de tipo de PDU</span><span class="sxs-lookup"><span data-stu-id="4ed18-103">PDU Type Values</span></span>

<span data-ttu-id="4ed18-104">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="4ed18-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4ed18-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="4ed18-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="4ed18-106">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="4ed18-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="4ed18-107">Os valores do tipo PDU são usados no **campo \_ tipo PDU** da PDU para descrever seu tipo.</span><span class="sxs-lookup"><span data-stu-id="4ed18-107">The PDU type values are used in the **pdu\_type** field of the PDU to describe its type.</span></span>



| <span data-ttu-id="4ed18-108">Constante</span><span class="sxs-lookup"><span data-stu-id="4ed18-108">Constant</span></span>                                                                                                                                                                   | <span data-ttu-id="4ed18-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ed18-109">Description</span></span>                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <span data-ttu-id="4ed18-110"><dt>**\_Get SNMP PDU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4ed18-110"><dt>**SNMP\_PDU\_GET**</dt></span></span> </dl>                | <span data-ttu-id="4ed18-111">Pesquisar e recuperar um valor de uma variável SNMP especificada.</span><span class="sxs-lookup"><span data-stu-id="4ed18-111">Search and retrieve a value from a specified SNMP variable.</span></span><br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <span data-ttu-id="4ed18-112"><dt>**o SNMP \_ PDU \_ GetNext**</dt></span><span class="sxs-lookup"><span data-stu-id="4ed18-112"><dt>**SNMP\_PDU\_GETNEXT**</dt></span></span> </dl>    | <span data-ttu-id="4ed18-113">Pesquise e recupere o valor de uma variável SNMP sem saber o nome exato da variável.</span><span class="sxs-lookup"><span data-stu-id="4ed18-113">Search and retrieve the value of an SNMP variable without knowing the exact name of the variable.</span></span><br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <span data-ttu-id="4ed18-114"><dt>**\_resposta de PDU de SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4ed18-114"><dt>**SNMP\_PDU\_RESPONSE**</dt></span></span> </dl> | <span data-ttu-id="4ed18-115">Responder a uma solicitação do SNMP \_ PDU \_ Get ou SNMP \_ PDU \_ GetNext.</span><span class="sxs-lookup"><span data-stu-id="4ed18-115">Reply to an SNMP\_PDU\_GET or an SNMP\_PDU\_GETNEXT request.</span></span><br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <span data-ttu-id="4ed18-116"><dt>**\_conjunto de PDU SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4ed18-116"><dt>**SNMP\_PDU\_SET**</dt></span></span> </dl>                | <span data-ttu-id="4ed18-117">Armazene um valor em uma variável SNMP especificada.</span><span class="sxs-lookup"><span data-stu-id="4ed18-117">Store a value in a specified SNMP variable.</span></span><br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <span data-ttu-id="4ed18-118"><dt>**\_V1TRAP de PDU SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4ed18-118"><dt>**SNMP\_PDU\_V1TRAP**</dt></span></span> </dl>       | <span data-ttu-id="4ed18-119">Indica que a interceptação de PDU está formatada para estar em conformidade com o padrão SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="4ed18-119">Indicates that the PDU trap is formatted to conform with the SNMPv1 standard.</span></span><br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <span data-ttu-id="4ed18-120"><dt>**SNMP \_ PDU \_ GetBulk**</dt></span><span class="sxs-lookup"><span data-stu-id="4ed18-120"><dt>**SNMP\_PDU\_GETBULK**</dt></span></span> </dl>    | <span data-ttu-id="4ed18-121">Pesquise e recupere vários valores com uma única solicitação.</span><span class="sxs-lookup"><span data-stu-id="4ed18-121">Search and retrieve multiple values with a single request.</span></span><br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <span data-ttu-id="4ed18-122"><dt>**informar sobre o SNMP \_ PDU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4ed18-122"><dt>**SNMP\_PDU\_INFORM**</dt></span></span> </dl>       | <span data-ttu-id="4ed18-123">Indica uma PDU de solicitação de informe.</span><span class="sxs-lookup"><span data-stu-id="4ed18-123">Indicates an inform request PDU.</span></span><br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <span data-ttu-id="4ed18-124"><dt>**\_interceptação de PDU SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4ed18-124"><dt>**SNMP\_PDU\_TRAP**</dt></span></span> </dl>             | <span data-ttu-id="4ed18-125">Alerta o sistema de gerenciamento para um evento extraordinário sob o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="4ed18-125">Alerts the management system to an extraordinary event under SNMPv2C.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="4ed18-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ed18-126">Requirements</span></span>



| <span data-ttu-id="4ed18-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ed18-127">Requirement</span></span> | <span data-ttu-id="4ed18-128">Valor</span><span class="sxs-lookup"><span data-stu-id="4ed18-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4ed18-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ed18-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4ed18-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4ed18-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="4ed18-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ed18-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4ed18-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4ed18-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4ed18-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4ed18-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ed18-134"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ed18-134"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ed18-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ed18-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ed18-136">Visão geral do Protocolo SNMP</span><span class="sxs-lookup"><span data-stu-id="4ed18-136">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="4ed18-137">Referência de SNMP</span><span class="sxs-lookup"><span data-stu-id="4ed18-137">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="4ed18-138">Constantes SNMP</span><span class="sxs-lookup"><span data-stu-id="4ed18-138">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

