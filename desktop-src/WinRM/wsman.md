---
title: Objeto WSMan (WSManDisp. h)
description: Fornece métodos e propriedades usados para criar uma sessão, representada por um objeto de sessão.
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows de objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, descrito
topic_type:
- apiref
api_name:
- WSMan
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02cb92b2d72d657791d4a16bd1e999b77645a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369288"
---
# <a name="wsman-object"></a><span data-ttu-id="d35c8-105">Objeto WSMan</span><span class="sxs-lookup"><span data-stu-id="d35c8-105">WSMan object</span></span>

<span data-ttu-id="d35c8-106">Fornece métodos e propriedades usados para criar uma sessão, representada por um objeto de [**sessão**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="d35c8-106">Provides methods and properties used to create a session, represented by a [**Session**](session.md) object.</span></span> <span data-ttu-id="d35c8-107">Todas as operações de Gerenciamento Remoto do Windows exigem a criação de uma [**sessão**](session.md) que se conecta a um computador remoto, BMC ( [*controlador de gerenciamento base*](windows-remote-management-glossary.md) ) ou o computador local.</span><span class="sxs-lookup"><span data-stu-id="d35c8-107">Any Windows Remote Management operations require creation of a [**Session**](session.md) that connects to a remote computer, [*base management controller*](windows-remote-management-glossary.md) (BMC), or the local computer.</span></span> <span data-ttu-id="d35c8-108">As operações incluem obter, gravar, enumerar dados ou invocar métodos.</span><span class="sxs-lookup"><span data-stu-id="d35c8-108">Operations include getting, writing, enumerating data, or invoking methods.</span></span>

## <a name="members"></a><span data-ttu-id="d35c8-109">Membros</span><span class="sxs-lookup"><span data-stu-id="d35c8-109">Members</span></span>

<span data-ttu-id="d35c8-110">O objeto **WSMan** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d35c8-110">The **WSMan** object has these types of members:</span></span>

-   [<span data-ttu-id="d35c8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d35c8-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d35c8-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d35c8-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d35c8-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="d35c8-113">Methods</span></span>

<span data-ttu-id="d35c8-114">O objeto **WSMan** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d35c8-114">The **WSMan** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="d35c8-115">Método</span><span class="sxs-lookup"><span data-stu-id="d35c8-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="d35c8-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d35c8-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d35c8-117"><a href="wsman-createconnectionoptions.md"><strong>Createconnectoptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-117"><a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-118">Cria um objeto <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> que especifica o nome de usuário e a senha usados ao criar uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="d35c8-118">Creates a <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> object that specifies the user name and password used when creating a remote session.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d35c8-119"><a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-119"><a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-120">Cria um objeto <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> que pode especificar:</span><span class="sxs-lookup"><span data-stu-id="d35c8-120">Creates a <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> object that can specify:</span></span><br/>
<ul>
<li><span data-ttu-id="d35c8-121">O caminho completo para um <a href="windows-remote-management-glossary.md"><em>recurso</em></a> ou um único dado.</span><span class="sxs-lookup"><span data-stu-id="d35c8-121">The complete path to a <a href="windows-remote-management-glossary.md"><em>resource</em></a> or a single piece of data.</span></span></li>
<li><span data-ttu-id="d35c8-122">Um <a href="windows-remote-management-glossary.md"><em>seletor</em></a> para uma instância específica de um recurso.</span><span class="sxs-lookup"><span data-stu-id="d35c8-122">A <a href="windows-remote-management-glossary.md"><em>selector</em></a> for a specific instance of a resource.</span></span></li>
<li><span data-ttu-id="d35c8-123">Uma <a href="windows-remote-management-glossary.md"><em>opção</em></a> que fornece dados adicionais para o provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="d35c8-123">An <a href="windows-remote-management-glossary.md"><em>option</em></a> that supplies additional data to the resource provider.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d35c8-124"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-124"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-125">Cria um objeto de <a href="session.md"><strong>sessão</strong></a> que pode ser usado para operações de rede subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d35c8-125">Creates a <a href="session.md"><strong>Session</strong></a> object that can then be used for subsequent network operations.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d35c8-126"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan. EnumerationFlagHierarchyDeep</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-126"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan.EnumerationFlagHierarchyDeep</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-127">Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagHierarchyDeep</strong> para uso no parâmetro <em>flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-127">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyDeep</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d35c8-128"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan. EnumerationFlagHierarchyDeepBasePropsOnly</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-128"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan.EnumerationFlagHierarchyDeepBasePropsOnly</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-129">Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> para uso no parâmetro <em>flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-129">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d35c8-130"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan. EnumerationFlagHierarchyShallow</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-130"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan.EnumerationFlagHierarchyShallow</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-131">Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagHierarchyShallow</strong> para uso no parâmetro <em>flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-131">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyShallow</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d35c8-132"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan. EnumerationFlagNonXmlText</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-132"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan.EnumerationFlagNonXmlText</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-133">Retorna o valor da constante de enumeração <strong>WSManFlagNonXmlText</strong> para uso no parâmetro <em>flags</em> do método <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d35c8-133">Returns the value of the enumeration constant <strong>WSManFlagNonXmlText</strong> for use in the <em>flags</em> parameter of the <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a> method.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d35c8-134"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan. EnumerationFlagReturnEPR</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-134"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan.EnumerationFlagReturnEPR</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-135">Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagReturnEPR</strong> para uso no parâmetro <em>flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-135">Returns the value of the enumeration flag <strong>EnumerationFlagReturnEPR</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d35c8-136"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan. EnumerationFlagReturnObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-136"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan.EnumerationFlagReturnObject</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-137">Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagReturnObject</strong> para uso no parâmetro <em>flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-137">Returns the value of the enumeration flag <strong>EnumerationFlagReturnObject</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d35c8-138"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan. EnumerationFlagReturnObjectAndEPR</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-138"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan.EnumerationFlagReturnObjectAndEPR</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-139">Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagReturnObjectAndEPR</strong> para uso no parâmetro <em>flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-139">Returns the value of the enumeration flag <strong>EnumerationFlagReturnObjectAndEPR</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d35c8-140"><a href="wsman-geterrormessage.md"><strong>WSMan. GetErrorMessage</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-140"><a href="wsman-geterrormessage.md"><strong>WSMan.GetErrorMessage</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-141">Retorna uma cadeia de caracteres formatada que contém o texto de um número de erro.</span><span class="sxs-lookup"><span data-stu-id="d35c8-141">Returns a formatted string containing the text of an error number.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d35c8-142"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan. SessionFlagCredUsernamePassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-142"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan.SessionFlagCredUsernamePassword</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-143">Retorna o valor do sinalizador de autenticação <strong>WSManFlagCredUsernamePassword</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-143">Returns the value of the authentication flag <strong>WSManFlagCredUsernamePassword</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d35c8-144"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan. SessionFlagEnableSPNServerPort</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-144"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan.SessionFlagEnableSPNServerPort</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-145">Retorna o valor do sinalizador de autenticação <strong>WSManFlagEnableSPNServerPort</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-145">Returns the value of the authentication flag <strong>WSManFlagEnableSPNServerPort</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d35c8-146"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan. SessionFlagNoEncryption</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-146"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan.SessionFlagNoEncryption</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-147">Retorna o valor do sinalizador de autenticação <strong>WSManFlagNoEncryption</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-147">Returns the value of the authentication flag <strong>WSManFlagNoEncryption</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d35c8-148"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan. SessionFlagSkipCACheck</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-148"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan.SessionFlagSkipCACheck</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-149">Retorna o valor do sinalizador de autenticação <strong>WSManFlagSkipCACheck</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-149">Returns the value of the <strong>WSManFlagSkipCACheck</strong> authentication flag for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d35c8-150"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan. SessionFlagSkipCNCheck</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-150"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan.SessionFlagSkipCNCheck</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-151">Retorna o valor do sinalizador de autenticação <strong>WSManFlagSkipCNCheck</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-151">Returns the value of the authentication flag <strong>WSManFlagSkipCNCheck</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d35c8-152"><a href="wsman-sessionflagusebasic.md"><strong>WSMan. SessionFlagUseBasic</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-152"><a href="wsman-sessionflagusebasic.md"><strong>WSMan.SessionFlagUseBasic</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-153">Retorna o valor do sinalizador de autenticação <strong>WSManFlagUseBasic</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-153">Returns the value of the authentication flag <strong>WSManFlagUseBasic</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d35c8-154"><a href="wsman-sessionflagusedigest.md"><strong>WSMan. SessionFlagUseDigest</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-154"><a href="wsman-sessionflagusedigest.md"><strong>WSMan.SessionFlagUseDigest</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-155">Retorna o valor do sinalizador de autenticação <strong>WSManFlagUseDigest</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-155">Returns the value of the authentication flag <strong>WSManFlagUseDigest</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d35c8-156"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan. SessionFlagUseKerberos</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-156"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan.SessionFlagUseKerberos</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-157">Retorna o valor do sinalizador de autenticação <strong>WSManFlagUseKerberos</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-157">Returns the value of the authentication flag <strong>WSManFlagUseKerberos</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d35c8-158"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan. SessionFlagUseNegotiate</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-158"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan.SessionFlagUseNegotiate</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-159">Retorna o valor do sinalizador de autenticação <strong>WSManFlagUseNegotiate</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-159">Returns the value of the authentication flag <strong>WSManFlagUseNegotiate</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d35c8-160"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan. SessionFlagUseNoAuthentication</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-160"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan.SessionFlagUseNoAuthentication</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-161">Retorna o valor do sinalizador de autenticação <strong>WSManFlagUseNoAuthentication</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-161">Returns the value of the authentication flag <strong>WSManFlagUseNoAuthentication</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d35c8-162"><a href="wsman-sessionflagutf8.md"><strong>WSMan. SessionFlagUTF8</strong></a></span><span class="sxs-lookup"><span data-stu-id="d35c8-162"><a href="wsman-sessionflagutf8.md"><strong>WSMan.SessionFlagUTF8</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d35c8-163">Retorna o valor do sinalizador de autenticação <strong>WSManFlagUTF8</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d35c8-163">Returns the value of the authentication flag <strong>WSManFlagUTF8</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="d35c8-164">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d35c8-164">Properties</span></span>

<span data-ttu-id="d35c8-165">O objeto **WSMan** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d35c8-165">The **WSMan** object has these properties.</span></span>



| <span data-ttu-id="d35c8-166">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d35c8-166">Property</span></span>                                            | <span data-ttu-id="d35c8-167">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="d35c8-167">Access type</span></span>          | <span data-ttu-id="d35c8-168">Descrição</span><span class="sxs-lookup"><span data-stu-id="d35c8-168">Description</span></span>                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="d35c8-169">**CommandLine**</span><span class="sxs-lookup"><span data-stu-id="d35c8-169">**CommandLine**</span></span>](wsman-commandline.md)<br/> | <span data-ttu-id="d35c8-170">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d35c8-170">Read-only</span></span><br/> | <span data-ttu-id="d35c8-171">Obtém a linha de comando não processada para o processo de hospedagem atual.</span><span class="sxs-lookup"><span data-stu-id="d35c8-171">Gets the unprocessed command line for the current hosting process.</span></span><br/> |
| [<span data-ttu-id="d35c8-172">**Erro**</span><span class="sxs-lookup"><span data-stu-id="d35c8-172">**Error**</span></span>](wsman-error.md)<br/>             | <span data-ttu-id="d35c8-173">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d35c8-173">Read-only</span></span><br/> | <span data-ttu-id="d35c8-174">Obtém informações de erro.</span><span class="sxs-lookup"><span data-stu-id="d35c8-174">Gets error information.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="d35c8-175">Comentários</span><span class="sxs-lookup"><span data-stu-id="d35c8-175">Remarks</span></span>

<span data-ttu-id="d35c8-176">O objeto **WSMan** corresponde às interfaces [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) e [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) .</span><span class="sxs-lookup"><span data-stu-id="d35c8-176">The **WSMan** object corresponds to the [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) and [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) interfaces.</span></span> <span data-ttu-id="d35c8-177">**WSMan** é o único objeto que pode ser criado diretamente usando [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d35c8-177">**WSMan** is the only object that can be created directly using [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span>

## <a name="examples"></a><span data-ttu-id="d35c8-178">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d35c8-178">Examples</span></span>

<span data-ttu-id="d35c8-179">O exemplo de código a seguir mostra como criar uma instância de um objeto **WSMan** .</span><span class="sxs-lookup"><span data-stu-id="d35c8-179">The following code example shows how to instantiate a **WSMan** object.</span></span>


```VB
Dim objWsman
Dim Session, Resource 
Set objWsman = CreateObject( "WSMAN.Automation" )
Set Session = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/Root/CIMv2/Win32_OperatingSystem"
```



## <a name="requirements"></a><span data-ttu-id="d35c8-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d35c8-180">Requirements</span></span>



| <span data-ttu-id="d35c8-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="d35c8-181">Requirement</span></span> | <span data-ttu-id="d35c8-182">Valor</span><span class="sxs-lookup"><span data-stu-id="d35c8-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d35c8-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d35c8-183">Minimum supported client</span></span><br/> | <span data-ttu-id="d35c8-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d35c8-184">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="d35c8-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d35c8-185">Minimum supported server</span></span><br/> | <span data-ttu-id="d35c8-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d35c8-186">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d35c8-187">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d35c8-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="d35c8-188"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d35c8-188"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d35c8-189">INSERI</span><span class="sxs-lookup"><span data-stu-id="d35c8-189">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d35c8-190"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d35c8-190"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="d35c8-191">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d35c8-191">Library</span></span><br/>                  | <dl> <span data-ttu-id="d35c8-192"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d35c8-192"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d35c8-193">DLL</span><span class="sxs-lookup"><span data-stu-id="d35c8-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d35c8-194"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d35c8-194"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d35c8-195">Confira também</span><span class="sxs-lookup"><span data-stu-id="d35c8-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d35c8-196">API de script do WinRM</span><span class="sxs-lookup"><span data-stu-id="d35c8-196">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="d35c8-197">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="d35c8-197">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="d35c8-198">Usando Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="d35c8-198">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="d35c8-199">Criando scripts no Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="d35c8-199">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="d35c8-200">Obtendo dados do computador local</span><span class="sxs-lookup"><span data-stu-id="d35c8-200">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="d35c8-201">Obtendo dados de um computador remoto</span><span class="sxs-lookup"><span data-stu-id="d35c8-201">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

