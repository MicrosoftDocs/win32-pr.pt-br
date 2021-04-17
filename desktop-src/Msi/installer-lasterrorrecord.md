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
# <a name="installerlasterrorrecord-method"></a>Método Installer. LastErrorRecord

O método **LastErrorRecord** do objeto do [**instalador**](installer-object.md) retorna um objeto de [**registro**](record-object.md) que contém parâmetros de erro para o erro mais recente da função que produziu o registro de erro.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O objeto de [**registro**](record-object.md) é redefinido após a execução dessa função de qualquer função que gera um registro de erro.

Somente as seguintes funções designadas geram um registro de erro:

-   [**Método OpenDatabase (objeto instalador)**](installer-opendatabase.md)
-   [**Compromisso**](database-commit.md)
-   [**AbrirModoDeExibição**](database-openview.md)
-   [**Importar**](database-import.md)
-   [**Exportação**](database-export.md)
-   [**Mescle**](database-merge.md)
-   [**GenerateTransform**](database-generatetransform.md)
-   [**ApplyTransform**](database-applytransform.md)
-   [**Executados**](view-execute.md)
-   [**Modificar**](view-modify.md)
-   [**SetStream**](record-setstream.md)
-   [**SummaryInformation**](database-summaryinformation.md)
-   [**SourcePath**](session-sourcepath.md)
-   [**TargetPath**](session-targetpath.md)
-   [**ComponentCurrentState**](session-componentcurrentstate.md)
-   [**ComponentRequestState**](session-componentrequeststate.md)
-   [**FeatureCurrentState**](session-featurecurrentstate.md)
-   [**FeatureRequestState**](session-featurerequeststate.md)
-   [**FeatureCost**](session-featurecost.md)
-   [**FeatureValidStates**](session-featurevalidstates.md)
-   [**SetInstallLevel**](session-setinstalllevel.md)

O exemplo a seguir no VBScript usa uma chamada para [**OpenDatabase**](installer-opendatabase.md) para mostrar como obter informações de erro estendidas de um dos métodos ou propriedades que dão suporte ao método **LastErrorRecord** . O exemplo constrói uma mensagem de erro quando o método **OpenDatabase** falha. O objeto **Err** é usado para determinar se um erro foi encontrado.


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




