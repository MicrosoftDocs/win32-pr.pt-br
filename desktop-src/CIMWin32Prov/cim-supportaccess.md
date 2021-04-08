---
description: A \_ classe CIM SupportAccess define como obter assistência para um produto.
ms.assetid: f42a793f-d71e-498e-9c6b-581aa029a0dd
ms.tgt_platform: multiple
title: Classe CIM_SupportAccess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SupportAccess
- CIM_SupportAccess.CommunicationInfo
- CIM_SupportAccess.CommunicationMode
- CIM_SupportAccess.Description
- CIM_SupportAccess.Locale
- CIM_SupportAccess.SupportAccessId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db5f1dc4331bd50e2fc61899f9d45fe2cdb0eca0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089232"
---
# <a name="cim_supportaccess-class"></a><span data-ttu-id="2bd13-103">\_Classe CIM SupportAccess</span><span class="sxs-lookup"><span data-stu-id="2bd13-103">CIM\_SupportAccess class</span></span>

<span data-ttu-id="2bd13-104">A classe **CIM \_ SupportAccess** define como obter assistência para um produto.</span><span class="sxs-lookup"><span data-stu-id="2bd13-104">The **CIM\_SupportAccess** class defines how to obtain assistance for a product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2bd13-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="2bd13-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2bd13-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2bd13-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2bd13-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2bd13-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2bd13-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="2bd13-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bd13-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2bd13-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{80321714-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_SupportAccess
{
  string CommunicationInfo;
  uint16 CommunicationMode;
  string Description;
  string Locale;
  string SupportAccessId;
};
```

## <a name="members"></a><span data-ttu-id="2bd13-110">Membros</span><span class="sxs-lookup"><span data-stu-id="2bd13-110">Members</span></span>

<span data-ttu-id="2bd13-111">A classe **CIM \_ SupportAccess** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2bd13-111">The **CIM\_SupportAccess** class has these types of members:</span></span>

-   [<span data-ttu-id="2bd13-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2bd13-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2bd13-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2bd13-113">Properties</span></span>

<span data-ttu-id="2bd13-114">A classe **CIM \_ SupportAccess** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2bd13-114">The **CIM\_SupportAccess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2bd13-115">**CommunicationInfo**</span><span class="sxs-lookup"><span data-stu-id="2bd13-115">**CommunicationInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd13-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bd13-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd13-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2bd13-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd13-118">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 2,11 "," MIF. DMTF \| FRU \| 2,12 ")</span><span class="sxs-lookup"><span data-stu-id="2bd13-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.11", "MIF.DMTF\|FRU\|002.12")</span></span>
</dt> </dl>

<span data-ttu-id="2bd13-119">Detalhes do modo de comunicação.</span><span class="sxs-lookup"><span data-stu-id="2bd13-119">Details of the communication mode.</span></span> <span data-ttu-id="2bd13-120">Por exemplo, se a propriedade **communicationmode** é "Phone", essa propriedade especifica o número de telefone a ser chamado.</span><span class="sxs-lookup"><span data-stu-id="2bd13-120">For example, if the **CommunicationMode** property is "Phone", then this property specifies the phone number to call.</span></span>

</dd> <dt>

<span data-ttu-id="2bd13-121">**Communicationmode**</span><span class="sxs-lookup"><span data-stu-id="2bd13-121">**CommunicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd13-122">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2bd13-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2bd13-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2bd13-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd13-124">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Suporte a DMTF \| \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="2bd13-124">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="2bd13-125">Forma de comunicação a ser usada para obter suporte.</span><span class="sxs-lookup"><span data-stu-id="2bd13-125">Form of communication to use to obtain support.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2bd13-126"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="2bd13-126"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>

<span data-ttu-id="2bd13-127"><span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Telefone** (2)</span><span class="sxs-lookup"><span data-stu-id="2bd13-127"><span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Phone** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Fax"></span><span id="fax"></span><span id="FAX"></span>

<span data-ttu-id="2bd13-128"><span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**Fax** (3)</span><span class="sxs-lookup"><span data-stu-id="2bd13-128"><span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**Fax** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="BBS"></span><span id="bbs"></span>

<span data-ttu-id="2bd13-129"><span id="BBS"></span><span id="bbs"></span>**BBS** (4)</span><span class="sxs-lookup"><span data-stu-id="2bd13-129"><span id="BBS"></span><span id="bbs"></span>**BBS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>

<span data-ttu-id="2bd13-130"><span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Serviço online** (5)</span><span class="sxs-lookup"><span data-stu-id="2bd13-130"><span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Online Service** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>

<span data-ttu-id="2bd13-131"><span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**Página da Web** (6)</span><span class="sxs-lookup"><span data-stu-id="2bd13-131"><span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**Web Page** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2bd13-132">Página da web</span><span class="sxs-lookup"><span data-stu-id="2bd13-132">Webpage</span></span>

</dd> <dt>

<span id="FTP"></span><span id="ftp"></span>

<span data-ttu-id="2bd13-133"><span id="FTP"></span><span id="ftp"></span>**FTP** (7)</span><span class="sxs-lookup"><span data-stu-id="2bd13-133"><span id="FTP"></span><span id="ftp"></span>**FTP** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>

<span data-ttu-id="2bd13-134"><span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**Email** (8)</span><span class="sxs-lookup"><span data-stu-id="2bd13-134"><span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**E-mail** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2bd13-135">Email</span><span class="sxs-lookup"><span data-stu-id="2bd13-135">Email</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2bd13-136">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2bd13-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd13-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bd13-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd13-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2bd13-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd13-139">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Suporte a DMTF \| \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="2bd13-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="2bd13-140">Descrição textual do tipo de suporte fornecido.</span><span class="sxs-lookup"><span data-stu-id="2bd13-140">Textual description of the type of support provided.</span></span>

</dd> <dt>

<span data-ttu-id="2bd13-141">**Localidade**</span><span class="sxs-lookup"><span data-stu-id="2bd13-141">**Locale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd13-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bd13-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd13-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2bd13-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd13-144">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Suporte para DMTF \| 1,2 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2bd13-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.2"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2bd13-145">Região geográfica ou dialeto de idioma ao qual esse recurso de suporte pertence.</span><span class="sxs-lookup"><span data-stu-id="2bd13-145">Geographic region or language dialect to which this support resource pertains.</span></span>

</dd> <dt>

<span data-ttu-id="2bd13-146">**SupportAccessId**</span><span class="sxs-lookup"><span data-stu-id="2bd13-146">**SupportAccessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bd13-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bd13-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bd13-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2bd13-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bd13-149">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2bd13-149">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2bd13-150">Cadeia de caracteres de forma livre arbitrária definida pelo fornecedor do produto ou pela organização que implanta o produto.</span><span class="sxs-lookup"><span data-stu-id="2bd13-150">Arbitrary free-form string defined by the product vendor or by the organization that deploys the product.</span></span> <span data-ttu-id="2bd13-151">Essa propriedade, já que é uma chave, deve ser exclusiva em toda a empresa.</span><span class="sxs-lookup"><span data-stu-id="2bd13-151">This property, since it is a key, should be unique throughout the enterprise.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2bd13-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="2bd13-152">Remarks</span></span>

<span data-ttu-id="2bd13-153">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="2bd13-153">WMI does not implement this class.</span></span>

<span data-ttu-id="2bd13-154">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="2bd13-154">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2bd13-155">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="2bd13-155">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bd13-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bd13-156">Requirements</span></span>



| <span data-ttu-id="2bd13-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bd13-157">Requirement</span></span> | <span data-ttu-id="2bd13-158">Valor</span><span class="sxs-lookup"><span data-stu-id="2bd13-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd13-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2bd13-159">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd13-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bd13-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2bd13-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2bd13-161">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd13-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2bd13-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2bd13-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="2bd13-163">Namespace</span></span><br/>                | <span data-ttu-id="2bd13-164">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2bd13-164">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2bd13-165">MOF</span><span class="sxs-lookup"><span data-stu-id="2bd13-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bd13-166"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2bd13-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2bd13-167">DLL</span><span class="sxs-lookup"><span data-stu-id="2bd13-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bd13-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bd13-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

