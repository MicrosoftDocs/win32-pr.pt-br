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
# <a name="adding-summary-information-to-customization-transform"></a><span data-ttu-id="d0323-103">Adicionando informações resumidas à transformação de personalização</span><span class="sxs-lookup"><span data-stu-id="d0323-103">Adding Summary Information to Customization Transform</span></span>

<span data-ttu-id="d0323-104">Para aplicar a transformação de personalização durante uma instalação do produto, você deve adicionar um [fluxo de informações de resumo](summary-information-stream.md) ao arquivo de transformação MNPtrans. MST gerado na [geração de uma transformação de personalização](generating-a-customization-transform.md).</span><span class="sxs-lookup"><span data-stu-id="d0323-104">To apply the customization transform during an installation of the product, you must add a [Summary Information Stream](summary-information-stream.md) to the transform file MNPtrans.mst generated in [Generating a Customization Transform](generating-a-customization-transform.md).</span></span>

<span data-ttu-id="d0323-105">Você pode gerar informações resumidas para uma transformação usando [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) ou o [**método CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md).</span><span class="sxs-lookup"><span data-stu-id="d0323-105">You may generate summary information for a transform using [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) or the [**CreateTransformSummaryInfo Method**](database-createtransformsummaryinfo.md).</span></span> <span data-ttu-id="d0323-106">O trecho a seguir, Sum.vbs, ilustra o [**método CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) e é para uso com o Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="d0323-106">The following snippet, Sum.vbs, illustrates the [**CreateTransformSummaryInfo Method**](database-createtransformsummaryinfo.md) and is for use with Windows Script Host.</span></span> <span data-ttu-id="d0323-107">Observe que este exemplo não executa nenhuma validação e suprime nenhuma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="d0323-107">Note that this example performs no validation and suppresses no error conditions.</span></span>


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



<span data-ttu-id="d0323-108">Para criar e adicionar informações resumidas ao arquivo de transformação MNPtrans. MST criado na [geração de uma transformação de personalização](generating-a-customization-transform.md), altere os diretórios para a pasta que contém Gen.vbs, o banco de dados original, o banco de dados atualizado e a transformação e insira a linha de comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="d0323-108">To create and add summary information to the transform file MNPtrans.mst you created in [Generating a Customization Transform](generating-a-customization-transform.md), change directories to the folder containing Gen.vbs, the original database, the updated database, and the transform, and enter the following command line.</span></span>

<span data-ttu-id="d0323-109">**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans. MST**</span><span class="sxs-lookup"><span data-stu-id="d0323-109">**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans.mst**</span></span>

<span data-ttu-id="d0323-110">Clique no ícone de MNP2000.msi para iniciar uma instalação ou use a seguinte linha de comando.</span><span class="sxs-lookup"><span data-stu-id="d0323-110">Click the MNP2000.msi icon to launch an install or use the following command line.</span></span>

<span data-ttu-id="d0323-111">**msiexec/i MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="d0323-111">**msiexec /i MNP2000.msi**</span></span>

<span data-ttu-id="d0323-112">Isso instala o produto sem as personalizações.</span><span class="sxs-lookup"><span data-stu-id="d0323-112">This installs the product without the customizations.</span></span> <span data-ttu-id="d0323-113">Para instalar com a personalização, insira a linha de comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="d0323-113">To install with the customization, enter the following command line.</span></span> <span data-ttu-id="d0323-114">Observe que o valor da propriedade [**TRANSFORMS**](transforms.md) refere-se ao arquivo de transformação localizado na origem.</span><span class="sxs-lookup"><span data-stu-id="d0323-114">Note that the value of the [**TRANSFORMS**](transforms.md) Property refers to transform file located at the source.</span></span>

<span data-ttu-id="d0323-115">**msiexec/i MNP2000.msi transformações = MNPtrans. MST**</span><span class="sxs-lookup"><span data-stu-id="d0323-115">**msiexec /i MNP2000.msi TRANSFORMS=MNPtrans.mst**</span></span>

<span data-ttu-id="d0323-116">O recurso de portão não aparece na árvore de seleção de recursos e os componentes do recurso de portão não são instalados mesmo que um tipo completo de instalação seja selecionado na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="d0323-116">The Gate feature does not appear in the feature selection tree and the components of the Gate feature are not installed even if a Complete type of installation is selected in the user interface.</span></span>

[<span data-ttu-id="d0323-117">Continuar</span><span class="sxs-lookup"><span data-stu-id="d0323-117">Continue</span></span>](embedding-customization-transforms-as-substorage.md)

 

 



