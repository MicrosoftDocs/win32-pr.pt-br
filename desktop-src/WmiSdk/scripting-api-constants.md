---
description: A API de script para WMI contém sinalizadores, valores comuns e códigos de erro.
ms.assetid: feaab757-3167-420b-8f42-edced4cd4c53
ms.tgt_platform: multiple
title: Constantes de API de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8576d4c7ab5b6103efca4491bc00b2fcf4649ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796185"
---
# <a name="scripting-api-constants"></a><span data-ttu-id="0e01b-103">Constantes de API de script</span><span class="sxs-lookup"><span data-stu-id="0e01b-103">Scripting API Constants</span></span>

<span data-ttu-id="0e01b-104">O WMI usa vários tipos de constantes no parâmetro *iFlags* de chamadas de método na [API de script para o WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="0e01b-104">WMI uses several types of constants in the *iflags* parameter of method calls in the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

<span data-ttu-id="0e01b-105">Visual Basic aplicativos podem incluir a biblioteca de tipos para a API de script, Wbemdisp. tlb.</span><span class="sxs-lookup"><span data-stu-id="0e01b-105">Visual Basic applications can include the type library for the scripting API, Wbemdisp.tlb.</span></span> <span data-ttu-id="0e01b-106">Os scripts não podem acessar constantes na biblioteca de tipos, a menos que usem as <REFERENCE> <OBJECT> marcas ou do formato de arquivo XML do WSH (Windows Script Host), conforme descrito em [usando a biblioteca de tipos de script do WMI](using-the-wmi-scripting-type-library.md).</span><span class="sxs-lookup"><span data-stu-id="0e01b-106">Scripts are unable to access constants in the type library unless they use the <REFERENCE> or <OBJECT> tags from the Windows Script Host (WSH) XML file format as described in [Using the WMI Scripting Type Library](using-the-wmi-scripting-type-library.md).</span></span> <span data-ttu-id="0e01b-107">Caso contrário, um script deve usar o valor da constante.</span><span class="sxs-lookup"><span data-stu-id="0e01b-107">Otherwise, a script must use the value of the constant.</span></span>

## <a name="constants"></a><span data-ttu-id="0e01b-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="0e01b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0e01b-109"><span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)</span><span class="sxs-lookup"><span data-stu-id="0e01b-109"><span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)</span></span>
</dt> <dd>

<span data-ttu-id="0e01b-110">Defina os níveis de autenticação de segurança.</span><span class="sxs-lookup"><span data-stu-id="0e01b-110">Define the security authentication levels.</span></span>

</dd> <dt>

<span data-ttu-id="0e01b-111"><span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)</span><span class="sxs-lookup"><span data-stu-id="0e01b-111"><span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="0e01b-112">Defina como uma operação de gravação para uma classe ou uma instância é executada.</span><span class="sxs-lookup"><span data-stu-id="0e01b-112">Define how a write operation to a class or an instance is carried out.</span></span>

</dd> <dt>

<span data-ttu-id="0e01b-113"><span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)</span><span class="sxs-lookup"><span data-stu-id="0e01b-113"><span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)</span></span>
</dt> <dd>

<span data-ttu-id="0e01b-114">Defina os tipos CIM válidos de um valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="0e01b-114">Define the valid CIM types of a property value.</span></span>

</dd> <dt>

<span data-ttu-id="0e01b-115"><span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)</span><span class="sxs-lookup"><span data-stu-id="0e01b-115"><span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="0e01b-116">Defina as configurações para comparação de objeto e são usadas por [**SWbemObject. \_ CompareTo**](swbemobject-compareto-.md).</span><span class="sxs-lookup"><span data-stu-id="0e01b-116">Define the settings for object comparison and are used by [**SWbemObject.CompareTo\_**](swbemobject-compareto-.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e01b-117"><span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)</span><span class="sxs-lookup"><span data-stu-id="0e01b-117"><span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)</span></span>
</dt> <dd>

<span data-ttu-id="0e01b-118">Define um sinalizador de segurança que é usado como um parâmetro em chamadas para o método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) quando uma conexão com o WMI em um computador remoto está falhando.</span><span class="sxs-lookup"><span data-stu-id="0e01b-118">Defines a security flag that is used as a parameter in calls to the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method when a connection to WMI on a remote machine is failing.</span></span>

</dd> <dt>

<span data-ttu-id="0e01b-119"><span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="0e01b-119"><span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)</span></span>
</dt> <dd>

<span data-ttu-id="0e01b-120">Defina os erros que podem ser retornados pela [API de script para chamadas WMI](scripting-api-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="0e01b-120">Define the errors that may be returned by [Scripting API for WMI](scripting-api-for-wmi.md) calls.</span></span>

</dd> <dt>

<span data-ttu-id="0e01b-121"><span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)</span><span class="sxs-lookup"><span data-stu-id="0e01b-121"><span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="0e01b-122">Define constantes que são usadas por [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)e [**SWbemServices. InstancesOf**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="0e01b-122">Defines constants that are used by [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md), and [**SWbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e01b-123"><span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)</span><span class="sxs-lookup"><span data-stu-id="0e01b-123"><span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)</span></span>
</dt> <dd>

<span data-ttu-id="0e01b-124">Defina os níveis de representação de segurança.</span><span class="sxs-lookup"><span data-stu-id="0e01b-124">Define the security impersonation levels.</span></span> <span data-ttu-id="0e01b-125">Essas constantes são usadas com [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="0e01b-125">These constants are used with [**SWbemSecurity**](swbemsecurity.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e01b-126"><span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)</span><span class="sxs-lookup"><span data-stu-id="0e01b-126"><span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)</span></span>
</dt> <dd>

<span data-ttu-id="0e01b-127">Defina os formatos de texto de objeto válidos a serem usados por [**SWbemObjectEx. \_ gettext**](swbemobjectex-gettext-.md).</span><span class="sxs-lookup"><span data-stu-id="0e01b-127">Define the valid object text formats to be used by [**SWbemObjectEx.GetText\_**](swbemobjectex-gettext-.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e01b-128"><span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span><span class="sxs-lookup"><span data-stu-id="0e01b-128"><span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span></span>
</dt> <dd>

<span data-ttu-id="0e01b-129">Definir privilégios.</span><span class="sxs-lookup"><span data-stu-id="0e01b-129">Define privileges.</span></span> <span data-ttu-id="0e01b-130">Essas constantes são usadas com [**SWbemSecurity**](swbemsecurity.md) para conceder os privilégios necessários para algumas operações.</span><span class="sxs-lookup"><span data-stu-id="0e01b-130">These constants are used with [**SWbemSecurity**](swbemsecurity.md) to grant the privileges required for some operations.</span></span>

</dd> <dt>

<span data-ttu-id="0e01b-131"><span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)</span><span class="sxs-lookup"><span data-stu-id="0e01b-131"><span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="0e01b-132">Defina a profundidade da enumeração ou da consulta, que determina quantos objetos são retornados por uma chamada.</span><span class="sxs-lookup"><span data-stu-id="0e01b-132">Define the depth of enumeration or query, which determines how many objects are returned by a call.</span></span>

</dd> <dt>

<span data-ttu-id="0e01b-133"><span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)</span><span class="sxs-lookup"><span data-stu-id="0e01b-133"><span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="0e01b-134">Define o conteúdo do texto de objeto gerado e é usado por [**SWbemObject. \_ GetObjectText**](swbemobject-getobjecttext-.md).</span><span class="sxs-lookup"><span data-stu-id="0e01b-134">Defines the content of generated object text and is used by [**SWbemObject.GetObjectText\_**](swbemobject-getobjecttext-.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e01b-135"><span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)</span><span class="sxs-lookup"><span data-stu-id="0e01b-135"><span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)</span></span>
</dt> <dd>

<span data-ttu-id="0e01b-136">Define as constantes de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="0e01b-136">Defines the time-out constants.</span></span> <span data-ttu-id="0e01b-137">Essa constante é usada por [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md).</span><span class="sxs-lookup"><span data-stu-id="0e01b-137">This constant is used by [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md).</span></span>

</dd> </dl>

## <a name="combining-flags"></a><span data-ttu-id="0e01b-138">Combinando sinalizadores</span><span class="sxs-lookup"><span data-stu-id="0e01b-138">Combining Flags</span></span>

<span data-ttu-id="0e01b-139">Você pode combinar sinalizadores para afetar mais de um aspecto da chamada à API.</span><span class="sxs-lookup"><span data-stu-id="0e01b-139">You can combine flags to affect more than one aspect of the API call.</span></span>

<span data-ttu-id="0e01b-140">Por exemplo, para criar uma chamada [*semisynchronous*](gloss-s.md) , o parâmetro *iFlags* em uma [**SWbemServices.Exechamada \_ CQuery**](swbemservices-execquery.md) deve conter dois sinalizadores: **WbemFlagReturnImmediately** e **WbemFlagForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="0e01b-140">For example, to create a [*semisynchronous*](gloss-s.md) call, the *iFlags* parameter in an [**SWbemServices.ExecQuery\_**](swbemservices-execquery.md) call must contain two flags: **WbemFlagReturnImmediately** and **WbemFlagForwardOnly**.</span></span> <span data-ttu-id="0e01b-141">O valor de **WbemFlagReturnImmediately** é 16 e o valor de **WbemFlagForwardOnly** é 32.</span><span class="sxs-lookup"><span data-stu-id="0e01b-141">The value of **WbemFlagReturnImmediately** is 16 and the value of **WbemFlagForwardOnly** is 32.</span></span> <span data-ttu-id="0e01b-142">Como as constantes não podem ser acessadas pelo nome, os valores desses sinalizadores são combinados, produzindo um valor *iFlags* de 48.</span><span class="sxs-lookup"><span data-stu-id="0e01b-142">Because the constants cannot be accessed by name, the values of these flags are combined, producing an *iFlags* value of 48.</span></span>

<span data-ttu-id="0e01b-143">O exemplo de script a seguir mostra a chamada.</span><span class="sxs-lookup"><span data-stu-id="0e01b-143">The following script example shows the call.</span></span>


```VB
On Error Resume Next
For Each obj in GetObject("WinMgmts:").ExecQuery _
("SELECT * FROM Win32_NTLogEvent WHERE _ LogFile='Application'",,48)
    count  = count + 1
Next
```



<span data-ttu-id="0e01b-144">Nem todos os sinalizadores podem ser combinados, pois muitos são mutuamente exclusivos e podem produzir resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="0e01b-144">Not all flags can be combined since many are mutually exclusive and may produce unpredictable results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e01b-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e01b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e01b-146">API de script para WMI</span><span class="sxs-lookup"><span data-stu-id="0e01b-146">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 



