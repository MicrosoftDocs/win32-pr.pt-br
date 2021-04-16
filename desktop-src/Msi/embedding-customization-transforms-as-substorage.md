---
description: Você pode armazenar a transformação personalização em um armazenamento do pacote de Windows Installer para garantir que a transformação esteja sempre disponível quando o pacote de instalação estiver disponível.
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: Incorporando transformações de personalização como subarmazenamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd275d36b37b2e29ae166a2a464a62495d2ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750245"
---
# <a name="embedding-customization-transforms-as-substorage"></a><span data-ttu-id="177cf-103">Incorporando transformações de personalização como subarmazenamento</span><span class="sxs-lookup"><span data-stu-id="177cf-103">Embedding Customization Transforms as Substorage</span></span>

<span data-ttu-id="177cf-104">Você pode armazenar a transformação personalização em um armazenamento do pacote de Windows Installer para garantir que a transformação esteja sempre disponível quando o pacote de instalação estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="177cf-104">You may store the customization transform in a storage of the Windows Installer package to guarantee that the transform is always available when the installation package is available.</span></span> <span data-ttu-id="177cf-105">Consulte [transformações incorporadas](embedded-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="177cf-105">See [Embedded Transforms](embedded-transforms.md).</span></span> <span data-ttu-id="177cf-106">Um exemplo disso é fornecido no SDK do Windows Installer como o WiSubStg.vbs do utilitário.</span><span class="sxs-lookup"><span data-stu-id="177cf-106">An example of this is provided in the Windows Installer SDK as the utility WiSubStg.vbs.</span></span> <span data-ttu-id="177cf-107">O trecho a seguir, Emb.vbs, também ilustra o uso da [tabela de armazenamentos](-storages-table.md) para adicionar uma transformação inserida e é para uso com o Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="177cf-107">The following snippet, Emb.vbs, also illustrates the use of the [Storages table](-storages-table.md) to add an embedded transform and is for use with Windows Script Host.</span></span>


```VB
'Emb.vbs. Argument(0) is the original database. Argument(1) is the
'    path to the transform file. Argument(2) is the name of the storage.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
 WScript.Echo "Usage is emb.vbs [original database] [transform] [storage name]"
 WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
 
' Evaluate command-line arguments and set open and update modes
Dim databasePath: databasePath = Wscript.Arguments(0)
Dim importPath  : importPath = Wscript.Arguments(1)
Dim storageName : storageName = Wscript.Arguments(2)
 
' Open database and create a view on the _Storages table
Dim sqlQuery : sqlQuery = "SELECT `Name`,`Data` FROM _Storages"
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim view     : Set view = database.OpenView(sqlQuery)
 
'Create and Insert the row.
Dim record   : Set record = installer.CreateRecord(2)
record.StringData(1) = storageName
view.Execute record
 
'Insert storage - copy data into stream
record.SetStream 2, importPath
view.Modify 3, record
database.Commit
Set view = Nothing
Set database = Nothing
```



<span data-ttu-id="177cf-108">Para adicionar um armazenamento chamado MNPtrans1 ao MNP2000.msi e que contém a transformação criada na [adição de informações resumidas à transformação personalização](adding-summary-information-to-customization-transform.md), altere os diretórios para a pasta que contém Emb.vbs, o banco de dados original e o arquivo de transformação e, em seguida, insira a linha de comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="177cf-108">To add a storage named MNPtrans1 to MNP2000.msi, and containing the transform you created in [Adding Summary Information to Customization Transform](adding-summary-information-to-customization-transform.md), change directories to the folder containing Emb.vbs, the original database, and the transform file, then enter the following command line.</span></span>

<span data-ttu-id="177cf-109">**Cscript.exe Emb.vbs MNP2000.msi MNPtrans. MST MNPtrans1**</span><span class="sxs-lookup"><span data-stu-id="177cf-109">**Cscript.exe Emb.vbs MNP2000.msi MNPtrans.mst MNPtrans1**</span></span>

<span data-ttu-id="177cf-110">Isso conclui o exemplo de transformação personalização.</span><span class="sxs-lookup"><span data-stu-id="177cf-110">This completes the customization transform example.</span></span> <span data-ttu-id="177cf-111">Depois de inserir a transformação em MNPtrans. MST, a transformação estará sempre disponível com o pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="177cf-111">After embedding the transform in MNPtrans.mst, the transform is always available with the installation package.</span></span> <span data-ttu-id="177cf-112">O arquivo MNPtrans. MST não precisa estar localizado na origem para aplicar a transformação.</span><span class="sxs-lookup"><span data-stu-id="177cf-112">The file MNPtrans.mst does not need to be located at the source to apply the transform.</span></span>

<span data-ttu-id="177cf-113">Remova MNPtrans. MST da pasta que contém o pacote de instalação de exemplo.</span><span class="sxs-lookup"><span data-stu-id="177cf-113">Remove MNPtrans.mst from the folder containing the sample installation package.</span></span> <span data-ttu-id="177cf-114">Clique no ícone de MNP2000.msi para iniciar uma instalação ou use a seguinte linha de comando.</span><span class="sxs-lookup"><span data-stu-id="177cf-114">Click the MNP2000.msi icon to launch an install or use the following command line.</span></span>

<span data-ttu-id="177cf-115">**msiexec/i MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="177cf-115">**msiexec /i MNP2000.msi**</span></span>

<span data-ttu-id="177cf-116">Observe que isso instala o produto sem as personalizações.</span><span class="sxs-lookup"><span data-stu-id="177cf-116">Note that this installs the product without the customizations.</span></span> <span data-ttu-id="177cf-117">Para instalar o com as personalizações, insira a linha de comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="177cf-117">To install with the customizations, enter the following command line.</span></span> <span data-ttu-id="177cf-118">Use dois-pontos para indicar que o valor da propriedade [**TRANSformações**](transforms.md) se refere a uma transformação inserida.</span><span class="sxs-lookup"><span data-stu-id="177cf-118">Use a colon to indicate that the value of the [**TRANSFORMS**](transforms.md) Property refers to an embedded transform.</span></span>

<span data-ttu-id="177cf-119">msiexec/i MNP2000.msi transformações =: MNPtrans1</span><span class="sxs-lookup"><span data-stu-id="177cf-119">msiexec /i MNP2000.msi TRANSFORMS=:MNPtrans1</span></span>

<span data-ttu-id="177cf-120">Observe que o recurso de portão não aparece na árvore de seleção de recursos e que os componentes do recurso de portão não são instalados mesmo que um tipo completo de instalação seja selecionado na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="177cf-120">Note that the Gate feature does not appear in the feature selection tree and that the components of the Gate feature are not installed even if a Complete type of installation is selected in the user interface.</span></span>

## <a name="next-example"></a><span data-ttu-id="177cf-121">Próximo exemplo</span><span class="sxs-lookup"><span data-stu-id="177cf-121">Next example</span></span>

[<span data-ttu-id="177cf-122">Um exemplo de aplicação de patch de atualização pequena</span><span class="sxs-lookup"><span data-stu-id="177cf-122">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)

 

 



