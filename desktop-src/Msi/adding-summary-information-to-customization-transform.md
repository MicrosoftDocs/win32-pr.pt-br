---
description: Para aplicar a transformação de personalização durante uma instalação do produto, você deve adicionar um fluxo de informações de resumo ao arquivo de transformação MNPtrans. MST gerado na geração de uma transformação de personalização.
ms.assetid: 586f6c43-7449-4d06-9201-9b4b4919871e
title: Adicionando informações resumidas à transformação de personalização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64957fcf8f29ab8793517015c7018292ba9a6e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751212"
---
# <a name="adding-summary-information-to-customization-transform"></a>Adicionando informações resumidas à transformação de personalização

Para aplicar a transformação de personalização durante uma instalação do produto, você deve adicionar um [fluxo de informações de resumo](summary-information-stream.md) ao arquivo de transformação MNPtrans. MST gerado na [geração de uma transformação de personalização](generating-a-customization-transform.md).

Você pode gerar informações resumidas para uma transformação usando [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) ou o [**método CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md). O trecho a seguir, Sum.vbs, ilustra o [**método CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) e é para uso com o Windows Script Host. Observe que este exemplo não executa nenhuma validação e suprime nenhuma condição de erro.


```VB
'Sum.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is sum.vbs [original database] [customized database] [transform]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
 
' Open databases and transform 
Dim database1 : Set database1 =
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 =
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
Dim transform : transform = Wscript.Arguments(2)
 
' Create and add Summary Information
Dim transinfo : transinfo =
    Database2.CreateTransformSummaryInfo(Database1, transform,0,0)
```



Para criar e adicionar informações resumidas ao arquivo de transformação MNPtrans. MST criado na [geração de uma transformação de personalização](generating-a-customization-transform.md), altere os diretórios para a pasta que contém Gen.vbs, o banco de dados original, o banco de dados atualizado e a transformação e insira a linha de comando a seguir.

**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans. MST**

Clique no ícone de MNP2000.msi para iniciar uma instalação ou use a seguinte linha de comando.

**msiexec/i MNP2000.msi**

Isso instala o produto sem as personalizações. Para instalar com a personalização, insira a linha de comando a seguir. Observe que o valor da propriedade [**TRANSFORMS**](transforms.md) refere-se ao arquivo de transformação localizado na origem.

**msiexec/i MNP2000.msi transformações = MNPtrans. MST**

O recurso de portão não aparece na árvore de seleção de recursos e os componentes do recurso de portão não são instalados mesmo que um tipo completo de instalação seja selecionado na interface do usuário.

[Continuar](embedding-customization-transforms-as-substorage.md)

 

 



