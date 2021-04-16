---
description: Representa os recursos e o gerenciamento de um dispositivo de porta Fibre Channel (FC).
ms.assetid: 32a11971-9e18-410d-a3cd-4921a7e986f0
title: Classe CIM_FCPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FCPort
- CIM_FCPort.PortType
- CIM_FCPort.SupportedCOS
- CIM_FCPort.ActiveCOS
- CIM_FCPort.SupportedFC4Types
- CIM_FCPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6a858cbb4603743e1ddd11cac71500a9e39325a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787114"
---
# <a name="cim_fcport-class"></a><span data-ttu-id="2b120-103">\_Classe CIM FCPort</span><span class="sxs-lookup"><span data-stu-id="2b120-103">CIM\_FCPort class</span></span>

> [!NOTE]
> <span data-ttu-id="2b120-104">Este artigo contém referências ao termo "servidor subordinado", um termo que a Microsoft não usa mais.</span><span class="sxs-lookup"><span data-stu-id="2b120-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="2b120-105">Quando o termo for removido do software, também o removeremos deste artigo.</span><span class="sxs-lookup"><span data-stu-id="2b120-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="2b120-106">Representa os recursos e o gerenciamento de um dispositivo de porta Fibre Channel (FC).</span><span class="sxs-lookup"><span data-stu-id="2b120-106">Represents the capabilities and management of a fibre channel (FC) port device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b120-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b120-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::FC"), AMENDMENT]
class CIM_FCPort : CIM_NetworkPort
{
  uint16 PortType;
  uint16 SupportedCOS[];
  uint16 ActiveCOS[];
  uint16 SupportedFC4Types[];
  uint16 ActiveFC4Types[];
};
```

## <a name="members"></a><span data-ttu-id="2b120-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2b120-108">Members</span></span>

> [!NOTE]
> <span data-ttu-id="2b120-109">Este artigo contém referências ao termo "servidor subordinado", um termo que a Microsoft não usa mais.</span><span class="sxs-lookup"><span data-stu-id="2b120-109">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="2b120-110">Quando o termo for removido do software, também o removeremos deste artigo.</span><span class="sxs-lookup"><span data-stu-id="2b120-110">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="2b120-111">A classe **CIM \_ FCPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2b120-111">The **CIM\_FCPort** class has these types of members:</span></span>

-   [<span data-ttu-id="2b120-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2b120-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b120-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2b120-113">Properties</span></span>

<span data-ttu-id="2b120-114">A classe **CIM \_ FCPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2b120-114">The **CIM\_FCPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b120-115">**ActiveCOS**</span><span class="sxs-lookup"><span data-stu-id="2b120-115">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b120-116">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b120-116">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2b120-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2b120-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b120-118">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ FCPort**.**SupportedCOS**")</span><span class="sxs-lookup"><span data-stu-id="2b120-118">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_FCPort**.**SupportedCOS**")</span></span>
</dt> </dl>

<span data-ttu-id="2b120-119">As configurações de classe de serviço (COS) ativas para o Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="2b120-119">The active class of service (COS) settings for the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2b120-120">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2b120-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="1"></span>

<span data-ttu-id="2b120-121">**1** (1)</span><span class="sxs-lookup"><span data-stu-id="2b120-121">**1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="2b120-122">**2** (2)</span><span class="sxs-lookup"><span data-stu-id="2b120-122">**2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="2b120-123">**3** (3)</span><span class="sxs-lookup"><span data-stu-id="2b120-123">**3** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="2b120-124">**4** (4)</span><span class="sxs-lookup"><span data-stu-id="2b120-124">**4** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="5"></span>

<span data-ttu-id="2b120-125">**5** (5)</span><span class="sxs-lookup"><span data-stu-id="2b120-125">**5** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="6"></span>

<span data-ttu-id="2b120-126">**6** (6)</span><span class="sxs-lookup"><span data-stu-id="2b120-126">**6** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="2b120-127">**F** (7)</span><span class="sxs-lookup"><span data-stu-id="2b120-127">**F** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2b120-128">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="2b120-128">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b120-129">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b120-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2b120-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2b120-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b120-131">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ FCPort**.**SupportedFC4Types**")</span><span class="sxs-lookup"><span data-stu-id="2b120-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_FCPort**.**SupportedFC4Types**")</span></span>
</dt> </dl>

<span data-ttu-id="2b120-132">Os protocolos FC-4 que estão em execução no Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="2b120-132">The FC-4 protocols that are running on the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2b120-133">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2b120-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2b120-134">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="2b120-134">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

<span data-ttu-id="2b120-135">**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="2b120-135">**ISO/IEC 8802 - 2 LLC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

<span data-ttu-id="2b120-136">**IP sobre FC** (5)</span><span class="sxs-lookup"><span data-stu-id="2b120-136">**IP over FC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

<span data-ttu-id="2b120-137">**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="2b120-137">**SCSI - FCP** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

<span data-ttu-id="2b120-138">**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="2b120-138">**SCSI - GPP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

<span data-ttu-id="2b120-139">**IPI-3 mestre** (17)</span><span class="sxs-lookup"><span data-stu-id="2b120-139">**IPI - 3 Master** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

<span data-ttu-id="2b120-140">**IPI-3 escravo** (18)</span><span class="sxs-lookup"><span data-stu-id="2b120-140">**IPI - 3 Slave** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

<span data-ttu-id="2b120-141">**IPI-3 par** (19)</span><span class="sxs-lookup"><span data-stu-id="2b120-141">**IPI - 3 Peer** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

<span data-ttu-id="2b120-142">**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="2b120-142">**CP IPI - 3 Master** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

<span data-ttu-id="2b120-143">**CP IPI-3 escravo** (22)</span><span class="sxs-lookup"><span data-stu-id="2b120-143">**CP IPI - 3 Slave** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

<span data-ttu-id="2b120-144">**CP IPI-3 par** (23)</span><span class="sxs-lookup"><span data-stu-id="2b120-144">**CP IPI - 3 Peer** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

<span data-ttu-id="2b120-145">**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="2b120-145">**SBCCS Channel** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

<span data-ttu-id="2b120-146">**Unidade de controle SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="2b120-146">**SBCCS Control Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

<span data-ttu-id="2b120-147">**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="2b120-147">**FC-SB-2 Channel** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

<span data-ttu-id="2b120-148">**Unidade de controle FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="2b120-148">**FC-SB-2 Control Unit** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

<span data-ttu-id="2b120-149">**Serviços de Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="2b120-149">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

<span data-ttu-id="2b120-150">**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="2b120-150">**FC-SW** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

<span data-ttu-id="2b120-151">**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="2b120-151">**FC - SNMP** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

<span data-ttu-id="2b120-152">**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="2b120-152">**HIPPI - FP** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

<span data-ttu-id="2b120-153">**Controle bbl** (80)</span><span class="sxs-lookup"><span data-stu-id="2b120-153">**BBL Control** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="2b120-154">**PDU de LAN encapsulada bbl FDDI** (81)</span><span class="sxs-lookup"><span data-stu-id="2b120-154">**BBL FDDI Encapsulated LAN PDU** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="2b120-155">**PDU de LAN encapsulada BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="2b120-155">**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

<span data-ttu-id="2b120-156">**FC-vi** (88)</span><span class="sxs-lookup"><span data-stu-id="2b120-156">**FC - VI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

<span data-ttu-id="2b120-157">**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="2b120-157">**FC - AV** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

<span data-ttu-id="2b120-158">**Exclusivo do fornecedor** (255)</span><span class="sxs-lookup"><span data-stu-id="2b120-158">**Vendor Unique** (255)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2b120-159">**PortType**</span><span class="sxs-lookup"><span data-stu-id="2b120-159">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b120-160">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b120-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b120-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2b120-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b120-162">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span><span class="sxs-lookup"><span data-stu-id="2b120-162">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="2b120-163">O modo habilitado para a porta.</span><span class="sxs-lookup"><span data-stu-id="2b120-163">The enabled mode for the port.</span></span> <span data-ttu-id="2b120-164">Os modos de porta são definidos por padrões do ANSI X3.</span><span class="sxs-lookup"><span data-stu-id="2b120-164">The port modes are defined by ANSI X3 standards.</span></span> <span data-ttu-id="2b120-165">Se a porta estiver conectada, esse será o tipo de porta negociada, caso contrário, o tipo de porta configurado será relatado.</span><span class="sxs-lookup"><span data-stu-id="2b120-165">If the port is logged in, this will be the negotiated port type, otherwise the configured port type will be reported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2b120-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2b120-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2b120-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="2b120-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2b120-168">A propriedade relacionada **OtherPortType** contém uma descrição de cadeia de caracteres do tipo de porta</span><span class="sxs-lookup"><span data-stu-id="2b120-168">The related property **OtherPortType** contains a string description of the type of port</span></span>

</dd> <dt>

<span id="N"></span><span id="n"></span>

<span data-ttu-id="2b120-169"><span id="N"></span><span id="n"></span>**N** (10)</span><span class="sxs-lookup"><span data-stu-id="2b120-169"><span id="N"></span><span id="n"></span>**N** (10)</span></span>


</dt> <dd>

<span data-ttu-id="2b120-170">Porta do nó</span><span class="sxs-lookup"><span data-stu-id="2b120-170">Node Port</span></span>

</dd> <dt>

<span id="NL"></span><span id="nl"></span>

<span data-ttu-id="2b120-171"><span id="NL"></span><span id="nl"></span>**Nl** (11)</span><span class="sxs-lookup"><span data-stu-id="2b120-171"><span id="NL"></span><span id="nl"></span>**NL** (11)</span></span>


</dt> <dd>

<span data-ttu-id="2b120-172">Porta de nó com suporte para Loop arbitrado FC</span><span class="sxs-lookup"><span data-stu-id="2b120-172">Node Port supporting FC arbitrated loop</span></span>

</dd> <dt>

<span id="F_NL"></span><span id="f_nl"></span>

<span data-ttu-id="2b120-173"><span id="F_NL"></span><span id="f_nl"></span>**F/NL** (12)</span><span class="sxs-lookup"><span data-stu-id="2b120-173"><span id="F_NL"></span><span id="f_nl"></span>**F/NL** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Nx"></span><span id="nx"></span><span id="NX"></span>

<span data-ttu-id="2b120-174"><span id="Nx"></span><span id="nx"></span><span id="NX"></span>**NX** (13)</span><span class="sxs-lookup"><span data-stu-id="2b120-174"><span id="Nx"></span><span id="nx"></span><span id="NX"></span>**Nx** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2b120-175">A porta pode negociar para se tornar uma porta de nó (N) ou uma porta de nó com suporte a Loop arbitrado FC (NL)</span><span class="sxs-lookup"><span data-stu-id="2b120-175">Port may negotiate to become either a node port (N) or a node port supporting FC arbitrated loop (NL)</span></span>

</dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="2b120-176"><span id="E"></span><span id="e"></span>**E** (14)</span><span class="sxs-lookup"><span data-stu-id="2b120-176"><span id="E"></span><span id="e"></span>**E** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2b120-177">Porta de expansão conectando elementos da malha (por exemplo, comutadores FC)</span><span class="sxs-lookup"><span data-stu-id="2b120-177">Expansion Port connecting fabric elements (for example, FC switches)</span></span>

</dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="2b120-178"><span id="F"></span><span id="f"></span>**F** (15)</span><span class="sxs-lookup"><span data-stu-id="2b120-178"><span id="F"></span><span id="f"></span>**F** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2b120-179">Porta de malha (elemento)</span><span class="sxs-lookup"><span data-stu-id="2b120-179">Fabric (element) Port</span></span>

</dd> <dt>

<span id="FL"></span><span id="fl"></span>

<span data-ttu-id="2b120-180"><span id="FL"></span><span id="fl"></span>**Fl** (16)</span><span class="sxs-lookup"><span data-stu-id="2b120-180"><span id="FL"></span><span id="fl"></span>**FL** (16)</span></span>


</dt> <dd>

<span data-ttu-id="2b120-181">Porta de malha (elemento) com suporte para Loop arbitrado FC</span><span class="sxs-lookup"><span data-stu-id="2b120-181">Fabric (element) Port supporting FC arbitrated loop</span></span>

</dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="2b120-182"><span id="B"></span><span id="b"></span>**B** (17)</span><span class="sxs-lookup"><span data-stu-id="2b120-182"><span id="B"></span><span id="b"></span>**B** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2b120-183">Porta de ponte</span><span class="sxs-lookup"><span data-stu-id="2b120-183">Bridge port</span></span>

</dd> <dt>

<span id="G"></span><span id="g"></span>

<span data-ttu-id="2b120-184"><span id="G"></span><span id="g"></span>**G** (18)</span><span class="sxs-lookup"><span data-stu-id="2b120-184"><span id="G"></span><span id="g"></span>**G** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2b120-185">A porta pode negociar para se tornar uma porta de expansão (E) ou uma porta de malha (F)</span><span class="sxs-lookup"><span data-stu-id="2b120-185">Port may negotiate to become either an expansion port (E), or a fabric port (F)</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2b120-186"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="2b120-186"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2b120-187">**SupportedCOS**</span><span class="sxs-lookup"><span data-stu-id="2b120-187">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b120-188">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b120-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2b120-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2b120-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b120-190">As configurações de COS (classe de serviço) com suporte do Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="2b120-190">The class of service (COS) settings that are supported by the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2b120-191">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2b120-191">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="1"></span>

<span data-ttu-id="2b120-192">**1** (1)</span><span class="sxs-lookup"><span data-stu-id="2b120-192">**1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="2b120-193">**2** (2)</span><span class="sxs-lookup"><span data-stu-id="2b120-193">**2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="2b120-194">**3** (3)</span><span class="sxs-lookup"><span data-stu-id="2b120-194">**3** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="2b120-195">**4** (4)</span><span class="sxs-lookup"><span data-stu-id="2b120-195">**4** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="5"></span>

<span data-ttu-id="2b120-196">**5** (5)</span><span class="sxs-lookup"><span data-stu-id="2b120-196">**5** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="6"></span>

<span data-ttu-id="2b120-197">**6** (6)</span><span class="sxs-lookup"><span data-stu-id="2b120-197">**6** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="2b120-198">**F** (7)</span><span class="sxs-lookup"><span data-stu-id="2b120-198">**F** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2b120-199">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="2b120-199">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b120-200">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b120-200">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2b120-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2b120-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b120-202">Os protocolos FC-4 com suporte do Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="2b120-202">The FC-4 protocols that are supported by the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2b120-203">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2b120-203">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2b120-204">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="2b120-204">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

<span data-ttu-id="2b120-205">**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="2b120-205">**ISO/IEC 8802 - 2 LLC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

<span data-ttu-id="2b120-206">**IP sobre FC** (5)</span><span class="sxs-lookup"><span data-stu-id="2b120-206">**IP over FC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

<span data-ttu-id="2b120-207">**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="2b120-207">**SCSI - FCP** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

<span data-ttu-id="2b120-208">**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="2b120-208">**SCSI - GPP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

<span data-ttu-id="2b120-209">**IPI-3 mestre** (17)</span><span class="sxs-lookup"><span data-stu-id="2b120-209">**IPI - 3 Master** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

<span data-ttu-id="2b120-210">**IPI-3 escravo** (18)</span><span class="sxs-lookup"><span data-stu-id="2b120-210">**IPI - 3 Slave** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

<span data-ttu-id="2b120-211">**IPI-3 par** (19)</span><span class="sxs-lookup"><span data-stu-id="2b120-211">**IPI - 3 Peer** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

<span data-ttu-id="2b120-212">**CP IPI-3 Master** (21)</span><span class="sxs-lookup"><span data-stu-id="2b120-212">**CP IPI - 3 Master** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

<span data-ttu-id="2b120-213">**CP IPI-3 escravo** (22)</span><span class="sxs-lookup"><span data-stu-id="2b120-213">**CP IPI - 3 Slave** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

<span data-ttu-id="2b120-214">**CP IPI-3 par** (23)</span><span class="sxs-lookup"><span data-stu-id="2b120-214">**CP IPI - 3 Peer** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

<span data-ttu-id="2b120-215">**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="2b120-215">**SBCCS Channel** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

<span data-ttu-id="2b120-216">**Unidade de controle SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="2b120-216">**SBCCS Control Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

<span data-ttu-id="2b120-217">**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="2b120-217">**FC-SB-2 Channel** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

<span data-ttu-id="2b120-218">**Unidade de controle FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="2b120-218">**FC-SB-2 Control Unit** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

<span data-ttu-id="2b120-219">**Serviços de Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="2b120-219">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

<span data-ttu-id="2b120-220">**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="2b120-220">**FC-SW** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

<span data-ttu-id="2b120-221">**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="2b120-221">**FC - SNMP** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

<span data-ttu-id="2b120-222">**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="2b120-222">**HIPPI - FP** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

<span data-ttu-id="2b120-223">**Controle bbl** (80)</span><span class="sxs-lookup"><span data-stu-id="2b120-223">**BBL Control** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="2b120-224">**PDU de LAN encapsulada bbl FDDI** (81)</span><span class="sxs-lookup"><span data-stu-id="2b120-224">**BBL FDDI Encapsulated LAN PDU** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="2b120-225">**PDU de LAN encapsulada BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="2b120-225">**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

<span data-ttu-id="2b120-226">**FC-vi** (88)</span><span class="sxs-lookup"><span data-stu-id="2b120-226">**FC - VI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

<span data-ttu-id="2b120-227">**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="2b120-227">**FC - AV** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

<span data-ttu-id="2b120-228">**Exclusivo do fornecedor** (255)</span><span class="sxs-lookup"><span data-stu-id="2b120-228">**Vendor Unique** (255)</span></span>


<span data-ttu-id="2b120-229"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2b120-229"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2b120-230">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b120-230">Requirements</span></span>



| <span data-ttu-id="2b120-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b120-231">Requirement</span></span> | <span data-ttu-id="2b120-232">Valor</span><span class="sxs-lookup"><span data-stu-id="2b120-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b120-233">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b120-233">Minimum supported client</span></span><br/> | <span data-ttu-id="2b120-234">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2b120-234">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2b120-235">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b120-235">Minimum supported server</span></span><br/> | <span data-ttu-id="2b120-236">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2b120-236">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2b120-237">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b120-237">Namespace</span></span><br/>                | <span data-ttu-id="2b120-238">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="2b120-238">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2b120-239">MOF</span><span class="sxs-lookup"><span data-stu-id="2b120-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b120-240"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b120-240"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b120-241">DLL</span><span class="sxs-lookup"><span data-stu-id="2b120-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b120-242"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2b120-242"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2b120-243">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b120-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b120-244">**\_NETWORKPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="2b120-244">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

