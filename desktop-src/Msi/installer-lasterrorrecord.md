---
description: O método LastErrorRecord do objeto Installer retorna um objeto Record que contém parâmetros de erro para o erro mais recente da função que produziu o registro de erro.
ms.assetid: 48fe46bc-6c10-4bd5-89bc-013e650a44e6
title: Método Installer.LastErrorRecord
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
ms.openlocfilehash: bb9dad1962cace623a4a52991d3650451a0a6d5f660aad88e46c4fe393ce4e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142105"
---
# <a name="installerlasterrorrecord-method"></a>Método Installer.LastErrorRecord

O **método LastErrorRecord** do objeto [**Installer**](installer-object.md) retorna um objeto [**Record**](record-object.md) que contém parâmetros de erro para o erro mais recente da função que produziu o registro de erro.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O [**objeto**](record-object.md) Record é redefinido após a execução dessa função de qualquer função que gere um registro de erro.

Somente as seguintes funções designadas geram um registro de erro:

-   [**Método OpenDatabase (Objeto do Instalador)**](installer-opendatabase.md)
-   [**Commit**](database-commit.md)
-   [**Openview**](database-openview.md)
-   [**Importar**](database-import.md)
-   [**Exportação**](database-export.md)
-   [**Mesclagem**](database-merge.md)
-   [**GenerateTransform**](database-generatetransform.md)
-   [**ApplyTransform**](database-applytransform.md)
-   [**Executar**](view-execute.md)
-   [**Modificar**](view-modify.md)
-   [**SetStream**](record-setstream.md)
-   [**SummaryInformation**](database-summaryinformation.md)
-   [**Sourcepath**](session-sourcepath.md)
-   [**TargetPath**](session-targetpath.md)
-   [**ComponentCurrentState**](session-componentcurrentstate.md)
-   [**ComponentRequestState**](session-componentrequeststate.md)
-   [**FeatureCurrentState**](session-featurecurrentstate.md)
-   [**FeatureRequestState**](session-featurerequeststate.md)
-   [**FeatureCost**](session-featurecost.md)
-   [**FeatureValidStates**](session-featurevalidstates.md)
-   [**SetInstallLevel**](session-setinstalllevel.md)

O exemplo a seguir no VBScript usa uma chamada para [**OpenDatabase**](installer-opendatabase.md) para mostrar como obter informações de erro estendidas de um dos métodos ou propriedades que suportam o **método LastErrorRecord.** O exemplo constrói uma mensagem de erro quando **o método OpenDatabase** falha. O **objeto Err** é usado para determinar se um erro foi encontrado.


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
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




