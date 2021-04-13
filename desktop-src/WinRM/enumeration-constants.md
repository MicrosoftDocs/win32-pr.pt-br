---
title: Constantes de enumeração (WSManDisp. h)
description: A enumeração contém constantes, conforme listado na lista a seguir, usada no parâmetro flags por chamadas para a enumeração Session. Enumerate e IWSManSession.
ms.assetid: c0f2763b-a549-43d5-84a6-8cebf33a1ea2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagReturnObject
- WSManFlagNonXmlText
- EnumerationFlagReturnEPR
- WSManFlagReturnObjectAndEPR
- WSManFlagHierarchyDeep
- WSManFlagHierarchyShallow
- WSManFlagHierarchyDeepBasePropsOnly
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422f688fea992ee2d9b1d0d25af00a1d24ad798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369420"
---
# <a name="enumeration-constants"></a><span data-ttu-id="a8b11-103">Constantes de enumeração</span><span class="sxs-lookup"><span data-stu-id="a8b11-103">Enumeration Constants</span></span>

<span data-ttu-id="a8b11-104">A enumeração **\_ \_ WSManEnumFlags** contém constantes, conforme listado na lista a seguir, usada no parâmetro *flags* por chamadas para [**Session. Enumerate**](session-enumerate.md) e [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="a8b11-104">The **\_\_WSManEnumFlags** enumeration contains constants, as listed in the following list, used in the *flags* parameter by calls to [**Session.Enumerate**](session-enumerate.md) and [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

<span data-ttu-id="a8b11-105">Lembre-se de que **WSManFlagReturnObject** e **WSManFlagHierarchyDeep** são o padrão se o parâmetro *flags* não for especificado.</span><span class="sxs-lookup"><span data-stu-id="a8b11-105">Be aware that **WSManFlagReturnObject** and **WSManFlagHierarchyDeep** are the default if the *flags* parameter is not specified.</span></span>

<dl> <dt>

<span data-ttu-id="a8b11-106"><span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**</span><span class="sxs-lookup"><span data-stu-id="a8b11-106"><span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b11-107">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="a8b11-107">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="a8b11-108">Os lotes contêm as instâncias XML solicitadas.</span><span class="sxs-lookup"><span data-stu-id="a8b11-108">Batches contain the requested XML instances.</span></span> <span data-ttu-id="a8b11-109">Esse é o valor padrão para o parâmetro Flag.</span><span class="sxs-lookup"><span data-stu-id="a8b11-109">This is the default value for the flag parameter.</span></span>

<span data-ttu-id="a8b11-110">O método de script associado é [**WSMan. EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) e o método C++ é [**IWSManEx. EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).</span><span class="sxs-lookup"><span data-stu-id="a8b11-110">The associated scripting method is [**WSMan.EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b11-111"><span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**</span><span class="sxs-lookup"><span data-stu-id="a8b11-111"><span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b11-112">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="a8b11-112">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="a8b11-113">Esse sinalizador controla como o parâmetro de *filtro* na chamada para [**Session. Enumerate**](session-enumerate.md) é interpretado pelo WinRM.</span><span class="sxs-lookup"><span data-stu-id="a8b11-113">This flag controls how the *filter* parameter in the call to [**Session.Enumerate**](session-enumerate.md) is interpreted by WinRM.</span></span>

<span data-ttu-id="a8b11-114">O formato do filtro pode ser um fragmento XML ou uma cadeia de caracteres de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="a8b11-114">The format of the filter may be an XML fragment or a string of plain text.</span></span> <span data-ttu-id="a8b11-115">O formato é determinado pelo [*dialeto de filtro*](windows-remote-management-glossary.md) do [*filtro*](windows-remote-management-glossary.md) usado na chamada para [**Session. enumerar**](session-enumerate.md) ou [**IWSManSession:: enumerar**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), que é específica para a operação executada.</span><span class="sxs-lookup"><span data-stu-id="a8b11-115">The format is determined by the [*filter dialect*](windows-remote-management-glossary.md) of the [*filter*](windows-remote-management-glossary.md) used in the call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), which is specific to the operation performed.</span></span>

<span data-ttu-id="a8b11-116">Se o parâmetro *dialeto* não for especificado, o WinRM tentará determinar o dialeto com base no primeiro caractere do filtro.</span><span class="sxs-lookup"><span data-stu-id="a8b11-116">If the *dialect* parameter is not specified, WinRM attempts to determine the dialect based on the first character of the filter.</span></span> <span data-ttu-id="a8b11-117">Se o primeiro caractere for <, mas o filtro não for, na verdade, um fragmento XML, esse sinalizador deverá ser definido.</span><span class="sxs-lookup"><span data-stu-id="a8b11-117">If the first character is <, but the filter is not actually an XML fragment, then this flag should be set.</span></span> <span data-ttu-id="a8b11-118">Por exemplo, um filtro no formato a seguir requer que você defina **WSManFlagNonXmlText** para que o filtro seja interpretado corretamente:</span><span class="sxs-lookup"><span data-stu-id="a8b11-118">For example, a filter in the following format requires that you set **WSManFlagNonXmlText** so that the filter is correctly interpreted:</span></span>

`<25 && > 1`

<span data-ttu-id="a8b11-119">Se o filtro for um fragmento XML, esse sinalizador não será necessário porque o fragmento começa com <, que o WinRM interpreta corretamente como XML.</span><span class="sxs-lookup"><span data-stu-id="a8b11-119">If the filter is an XML fragment, then this flag is not required because the fragment starts with <, which WinRM correctly interprets as XML.</span></span> <span data-ttu-id="a8b11-120">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="a8b11-120">For example,</span></span>

`<filter>select * from aDataStructure</filter>`

<span data-ttu-id="a8b11-121">Se o filtro estiver em texto sem formatação que não comece com <, esse sinalizador não será necessário.</span><span class="sxs-lookup"><span data-stu-id="a8b11-121">If the filter is in plain text that does not start with <, then this flag is not required.</span></span> <span data-ttu-id="a8b11-122">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="a8b11-122">For example,</span></span>

`select * from aDataStructure`

<span data-ttu-id="a8b11-123">O método de script associado é [**WSMan. EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) e o método C++ é [**IWSManEx. EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).</span><span class="sxs-lookup"><span data-stu-id="a8b11-123">The associated scripting method is [**WSMan.EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) and the C++ method is [**IWSManEx.EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b11-124"><span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**</span><span class="sxs-lookup"><span data-stu-id="a8b11-124"><span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b11-125">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="a8b11-125">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="a8b11-126">Os lotes contêm referências de ponto de extremidade (EPRs) para as instâncias XML correspondentes, mas não as instâncias reais.</span><span class="sxs-lookup"><span data-stu-id="a8b11-126">Batches contain endpoint references (EPRs) for the corresponding XML instances, but not the actual instances.</span></span>

<span data-ttu-id="a8b11-127">O método de script associado é [**WSMan. EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) e o método C++ é [**IWSManEx. EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).</span><span class="sxs-lookup"><span data-stu-id="a8b11-127">The associated scripting method is [**WSMan.EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b11-128"><span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**</span><span class="sxs-lookup"><span data-stu-id="a8b11-128"><span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b11-129">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="a8b11-129">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="a8b11-130">Os lotes contêm as instâncias XML solicitadas e os EPRs correspondentes contidos em um elemento [*WSMan: Items*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="a8b11-130">Batches contain both the requested XML instances and the corresponding EPRs contained in a [*wsman:Items*](windows-remote-management-glossary.md) element.</span></span>

<span data-ttu-id="a8b11-131">O método de script associado é [**WSMan. EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) e o método C++ é [**IWSManEx. EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).</span><span class="sxs-lookup"><span data-stu-id="a8b11-131">The associated scripting method is [**WSMan.EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b11-132"><span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**</span><span class="sxs-lookup"><span data-stu-id="a8b11-132"><span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b11-133">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="a8b11-133">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="a8b11-134">As instâncias de classe derivadas são incluídas e são representadas de acordo com seus esquemas reais.</span><span class="sxs-lookup"><span data-stu-id="a8b11-134">Derived class instances are included and are represented according to their actual schemas.</span></span>

<span data-ttu-id="a8b11-135">O método de script associado é [**WSMan. EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) e o método C++ é [**IWSManEx. EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).</span><span class="sxs-lookup"><span data-stu-id="a8b11-135">The associated scripting method is [**WSMan.EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b11-136"><span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**</span><span class="sxs-lookup"><span data-stu-id="a8b11-136"><span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b11-137">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="a8b11-137">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="a8b11-138">As instâncias de classe derivadas são excluídas.</span><span class="sxs-lookup"><span data-stu-id="a8b11-138">Derived class instances are excluded.</span></span> <span data-ttu-id="a8b11-139">Somente as instâncias do tipo solicitado são mostradas.</span><span class="sxs-lookup"><span data-stu-id="a8b11-139">Only instances of the requested type are shown.</span></span>

<span data-ttu-id="a8b11-140">O método de script associado é [**WSMan. EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) e o método C++ é [**IWSManEx. EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).</span><span class="sxs-lookup"><span data-stu-id="a8b11-140">The associated scripting method is [**WSMan.EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8b11-141"><span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**</span><span class="sxs-lookup"><span data-stu-id="a8b11-141"><span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b11-142">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="a8b11-142">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="a8b11-143">As instâncias de classe derivadas são incluídas e são representadas de acordo com o esquema de classe base.</span><span class="sxs-lookup"><span data-stu-id="a8b11-143">Derived class instances are included and are represented according to the base class schema.</span></span> <span data-ttu-id="a8b11-144">As propriedades definidas na classe derivada não são mostradas.</span><span class="sxs-lookup"><span data-stu-id="a8b11-144">Properties defined in the derived class are not shown.</span></span>

<span data-ttu-id="a8b11-145">O método de script associado é [**WSMan. EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) e o método C++ é [**IWSManEx. EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).</span><span class="sxs-lookup"><span data-stu-id="a8b11-145">The associated scripting method is [**WSMan.EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8b11-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8b11-146">Requirements</span></span>



| <span data-ttu-id="a8b11-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8b11-147">Requirement</span></span> | <span data-ttu-id="a8b11-148">Valor</span><span class="sxs-lookup"><span data-stu-id="a8b11-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b11-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8b11-149">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b11-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8b11-150">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a8b11-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8b11-151">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b11-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8b11-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a8b11-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8b11-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8b11-154"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b11-154"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8b11-155">INSERI</span><span class="sxs-lookup"><span data-stu-id="a8b11-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a8b11-156"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8b11-156"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b11-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8b11-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b11-158">Constantes e enumerações do WinRM</span><span class="sxs-lookup"><span data-stu-id="a8b11-158">WinRM Constants and Enumerations</span></span>](winrm-constants-and-enumerations.md)
</dt> <dt>

[<span data-ttu-id="a8b11-159">Enumerando ou listando todas as instâncias de um recurso</span><span class="sxs-lookup"><span data-stu-id="a8b11-159">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="a8b11-160">Consultando instâncias específicas de um recurso</span><span class="sxs-lookup"><span data-stu-id="a8b11-160">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 





