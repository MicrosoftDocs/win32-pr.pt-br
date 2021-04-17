---
description: O método LastErrorRecord do objeto do instalador retorna um objeto de registro que contém parâmetros de erro para o erro mais recente da função que produziu o registro de erro.
ms.assetid: 48fe46bc-6c10-4bd5-89bc-013e650a44e6
title: Método Installer. LastErrorRecord
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.LastErrorRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b368f30b04734b2d253a7d5f2aa64f0d61c930e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747763"
---
# <a name="installerlasterrorrecord-method"></a><span data-ttu-id="53c76-103">Método Installer. LastErrorRecord</span><span class="sxs-lookup"><span data-stu-id="53c76-103">Installer.LastErrorRecord method</span></span>

<span data-ttu-id="53c76-104">O método **LastErrorRecord** do objeto do [**instalador**](installer-object.md) retorna um objeto de [**registro**](record-object.md) que contém parâmetros de erro para o erro mais recente da função que produziu o registro de erro.</span><span class="sxs-lookup"><span data-stu-id="53c76-104">The **LastErrorRecord** method of the [**Installer**](installer-object.md) object returns a [**Record**](record-object.md) object that contains error parameters for the most recent error from the function that produced the error record.</span></span>

## <a name="syntax"></a><span data-ttu-id="53c76-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53c76-105">Syntax</span></span>


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a><span data-ttu-id="53c76-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53c76-106">Parameters</span></span>

<span data-ttu-id="53c76-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="53c76-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="53c76-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="53c76-108">Return value</span></span>

<span data-ttu-id="53c76-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="53c76-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53c76-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="53c76-110">Remarks</span></span>

<span data-ttu-id="53c76-111">O objeto de [**registro**](record-object.md) é redefinido após a execução dessa função de qualquer função que gera um registro de erro.</span><span class="sxs-lookup"><span data-stu-id="53c76-111">The [**Record**](record-object.md) object is reset after the execution of this function of any function that generates an error record.</span></span>

<span data-ttu-id="53c76-112">Somente as seguintes funções designadas geram um registro de erro:</span><span class="sxs-lookup"><span data-stu-id="53c76-112">Only the following designated functions generate an error record:</span></span>

-   [<span data-ttu-id="53c76-113">**Método OpenDatabase (objeto instalador)**</span><span class="sxs-lookup"><span data-stu-id="53c76-113">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="53c76-114">**Compromisso**</span><span class="sxs-lookup"><span data-stu-id="53c76-114">**Commit**</span></span>](database-commit.md)
-   [<span data-ttu-id="53c76-115">**AbrirModoDeExibição**</span><span class="sxs-lookup"><span data-stu-id="53c76-115">**OpenView**</span></span>](database-openview.md)
-   [<span data-ttu-id="53c76-116">**Importar**</span><span class="sxs-lookup"><span data-stu-id="53c76-116">**Import**</span></span>](database-import.md)
-   [<span data-ttu-id="53c76-117">**Exportação**</span><span class="sxs-lookup"><span data-stu-id="53c76-117">**Export**</span></span>](database-export.md)
-   [<span data-ttu-id="53c76-118">**Mescle**</span><span class="sxs-lookup"><span data-stu-id="53c76-118">**Merge**</span></span>](database-merge.md)
-   [<span data-ttu-id="53c76-119">**GenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="53c76-119">**GenerateTransform**</span></span>](database-generatetransform.md)
-   [<span data-ttu-id="53c76-120">**ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="53c76-120">**ApplyTransform**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="53c76-121">**Executados**</span><span class="sxs-lookup"><span data-stu-id="53c76-121">**Execute**</span></span>](view-execute.md)
-   [<span data-ttu-id="53c76-122">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="53c76-122">**Modify**</span></span>](view-modify.md)
-   [<span data-ttu-id="53c76-123">**SetStream**</span><span class="sxs-lookup"><span data-stu-id="53c76-123">**SetStream**</span></span>](record-setstream.md)
-   [<span data-ttu-id="53c76-124">**SummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="53c76-124">**SummaryInformation**</span></span>](database-summaryinformation.md)
-   [<span data-ttu-id="53c76-125">**SourcePath**</span><span class="sxs-lookup"><span data-stu-id="53c76-125">**SourcePath**</span></span>](session-sourcepath.md)
-   [<span data-ttu-id="53c76-126">**TargetPath**</span><span class="sxs-lookup"><span data-stu-id="53c76-126">**TargetPath**</span></span>](session-targetpath.md)
-   [<span data-ttu-id="53c76-127">**ComponentCurrentState**</span><span class="sxs-lookup"><span data-stu-id="53c76-127">**ComponentCurrentState**</span></span>](session-componentcurrentstate.md)
-   [<span data-ttu-id="53c76-128">**ComponentRequestState**</span><span class="sxs-lookup"><span data-stu-id="53c76-128">**ComponentRequestState**</span></span>](session-componentrequeststate.md)
-   [<span data-ttu-id="53c76-129">**FeatureCurrentState**</span><span class="sxs-lookup"><span data-stu-id="53c76-129">**FeatureCurrentState**</span></span>](session-featurecurrentstate.md)
-   [<span data-ttu-id="53c76-130">**FeatureRequestState**</span><span class="sxs-lookup"><span data-stu-id="53c76-130">**FeatureRequestState**</span></span>](session-featurerequeststate.md)
-   [<span data-ttu-id="53c76-131">**FeatureCost**</span><span class="sxs-lookup"><span data-stu-id="53c76-131">**FeatureCost**</span></span>](session-featurecost.md)
-   [<span data-ttu-id="53c76-132">**FeatureValidStates**</span><span class="sxs-lookup"><span data-stu-id="53c76-132">**FeatureValidStates**</span></span>](session-featurevalidstates.md)
-   [<span data-ttu-id="53c76-133">**SetInstallLevel**</span><span class="sxs-lookup"><span data-stu-id="53c76-133">**SetInstallLevel**</span></span>](session-setinstalllevel.md)

<span data-ttu-id="53c76-134">O exemplo a seguir no VBScript usa uma chamada para [**OpenDatabase**](installer-opendatabase.md) para mostrar como obter informações de erro estendidas de um dos métodos ou propriedades que dão suporte ao método **LastErrorRecord** .</span><span class="sxs-lookup"><span data-stu-id="53c76-134">The following sample in VBScript uses a call to [**OpenDatabase**](installer-opendatabase.md) to show how to obtain extended error information from one of the methods or properties that support the **LastErrorRecord** method.</span></span> <span data-ttu-id="53c76-135">O exemplo constrói uma mensagem de erro quando o método **OpenDatabase** falha.</span><span class="sxs-lookup"><span data-stu-id="53c76-135">The sample constructs an error message when the **OpenDatabase** method fails.</span></span> <span data-ttu-id="53c76-136">O objeto **Err** é usado para determinar se um erro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="53c76-136">The **Err** object is used to determine whether an error was encountered.</span></span>


```VB
Const msiOpenDatabaseModeReadOnly     = 0

On Error Resume Next ' defer error handling

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' attempt to open the non-existent MSI database
Dim database
Set database = installer.OpenDatabase("c:\nonexistent.msi", msiOpenDatabaseModeReadOnly)

' test for error
If Err.Number <> 0 Then
    Dim message, errorRec
    message = Err.Source & " " & Hex(Err.Number) & ": " & Err.Description
    If Not installer Is Nothing Then
        ' try to obtain extended error info
        Set errorRec = installer.LastErrorRecord
        If Not errorRec Is Nothing Then message = message & vbNewLine & errorRec.FormatText
    End If

    MsgBox message

    ' PLACE ADDITIONAL SCRIPTING CODE HERE TO LOG AND/OR DISPLAY THE MESSAGE AND
    ' DETERMINE WHETHER TO CONTINUE PROCESSING ANYTHING ELSE
End If
```



## <a name="requirements"></a><span data-ttu-id="53c76-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53c76-137">Requirements</span></span>



| <span data-ttu-id="53c76-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="53c76-138">Requirement</span></span> | <span data-ttu-id="53c76-139">Valor</span><span class="sxs-lookup"><span data-stu-id="53c76-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53c76-140">Versão</span><span class="sxs-lookup"><span data-stu-id="53c76-140">Version</span></span><br/> | <span data-ttu-id="53c76-141">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="53c76-141">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="53c76-142">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="53c76-142">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="53c76-143">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="53c76-143">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="53c76-144">DLL</span><span class="sxs-lookup"><span data-stu-id="53c76-144">DLL</span></span><br/>     | <dl> <span data-ttu-id="53c76-145"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53c76-145"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="53c76-146">IID</span><span class="sxs-lookup"><span data-stu-id="53c76-146">IID</span></span><br/>     | <span data-ttu-id="53c76-147">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="53c76-147">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




