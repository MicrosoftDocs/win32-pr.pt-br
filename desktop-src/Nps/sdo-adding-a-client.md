---
title: Adicionando um cliente
description: Adicionando um cliente
ms.assetid: 7e9e25af-e3b9-40ba-a89d-50b3874e3e68
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ccb2ecc6d92a387107dc473bc7c7844c106da43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366387"
---
# <a name="adding-a-client"></a><span data-ttu-id="cc44f-103">Adicionando um cliente</span><span class="sxs-lookup"><span data-stu-id="cc44f-103">Adding a Client</span></span>

<span data-ttu-id="cc44f-104">O código de Visual Basic a seguir adiciona um novo cliente RADIUS e define o endereço e o segredo compartilhado para o cliente.</span><span class="sxs-lookup"><span data-stu-id="cc44f-104">The following Visual Basic code adds a new RADIUS client, and sets the address and shared secret for the client.</span></span>

> [!Note]  
> <span data-ttu-id="cc44f-105">Uma referência COM deve ser adicionada ao projeto Visual Basic para que seja criada corretamente.</span><span class="sxs-lookup"><span data-stu-id="cc44f-105">A COM reference must be added to the Visual Basic project in order for it to build properly.</span></span> <span data-ttu-id="cc44f-106">Um exemplo da sequência de comandos do VB tem esta aparência: Add Reference-> COM-> "IAS SDO 1,0 tipo Library".</span><span class="sxs-lookup"><span data-stu-id="cc44f-106">An example of the VB command sequence looks like this: Add reference -> COM -> "IAS SDO 1.0 Type Library".</span></span> <span data-ttu-id="cc44f-107">Isso varia de acordo com sua versão do VB.</span><span class="sxs-lookup"><span data-stu-id="cc44f-107">This varies based on your version of VB.</span></span>

 

> [!Note]  
> <span data-ttu-id="cc44f-108">Este exemplo não funciona como código VBScript.</span><span class="sxs-lookup"><span data-stu-id="cc44f-108">This example does not work as VBScript code.</span></span>

 


```VB
Option Explicit On 

Public Class Form1
   Inherits System.Windows.Forms.Form


#Region " Windows Form Designer generated code "

   Public Sub New()
      MyBase.New()

      'This call is required by the Windows Form Designer.
      InitializeComponent()

      'Add any initialization after the InitializeComponent() call

   End Sub

   'Form overrides dispose to clean up the component list.
   Protected Overloads Overrides Sub Dispose(ByVal disposing As Boolean)
      If disposing Then
         If Not (components Is Nothing) Then
            components.Dispose()
         End If
      End If
      MyBase.Dispose(disposing)
   End Sub

   'Required by the Windows Form Designer
   Private components As System.ComponentModel.IContainer

   'NOTE: The following procedure is required by the Windows Form Designer
   'It can be modified using the Windows Form Designer.  
   'Do not modify it using the code editor.
   Friend WithEvents Button1 As System.Windows.Forms.Button
   <System.Diagnostics.DebuggerStepThrough()> Private Sub InitializeComponent()
      Me.Button1 = New System.Windows.Forms.Button()
      Me.SuspendLayout()
      '
      'Button1
      '
      Me.Button1.Location = New System.Drawing.Point(80, 24)
      Me.Button1.Name = "Button1"
      Me.Button1.TabIndex = 0
      Me.Button1.Text = "Add Client"
      '
      'Form1
      '
      Me.AutoScaleBaseSize = New System.Drawing.Size(5, 13)
      Me.ClientSize = New System.Drawing.Size(248, 85)
      Me.Controls.AddRange(New System.Windows.Forms.Control() {Me.Button1})
      Me.Name = "Form1"
      Me.Text = "SDO Sample code: Add Client"
      Me.ResumeLayout(False)

   End Sub

#End Region

   Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click
      On Error GoTo ErrorHandler ' Enable error-handling routine.

      '
      ' Attach to the local computer
      '
      Dim sdomachine As New SDOIASLib.SdoMachine()
      sdomachine.Attach(vbNullString)  'local

      '
      ' Retrieve a service SDO
      '
      Dim ServiceSdo As SDOIASLib.ISdo
      ServiceSdo = sdomachine.GetServiceSDO(SDOIASLib.IASDATASTORE.DATA_STORE_LOCAL, "IAS")

      '
      ' Retrieve the protocols collection
      '
      Dim ProtocolsCollection As SDOIASLib.ISdoCollection
      ProtocolsCollection = ServiceSdo.GetProperty(SDOIASLib.IASPROPERTIES.PROPERTY_IAS_PROTOCOLS_COLLECTION)

      '
      ' Retrieve the RADIUS protocol
      '
      Dim SdoRADIUS As SDOIASLib.ISdo
      SdoRADIUS = ProtocolsCollection.Item("Microsoft Radius Protocol")

      '
      ' Retrieve the clients collection
      '
      Dim ClientsCollection As SDOIASLib.ISdoCollection
      ClientsCollection = SdoRADIUS.GetProperty(SDOIASLib.RADIUSPROPERTIES.PROPERTY_RADIUS_CLIENTS_COLLECTION)

      Dim ClientName
      ClientName = InputBox("Enter client's name:", "Client's Name")
      If (ClientName = "") Then Exit Sub

      '
      ' Verify that the name is unique
      '
      If Not ClientsCollection.IsNameUnique(ClientName) Then
         Dim Answer
         Answer = MsgBox("Client already exists", vbExclamation + vbOKOnly, "Add client Error")
         Exit Sub
      End If

      '
      ' Add the client
      '
      Dim ClientSdo As SDOIASLib.ISdo
      Call ClientsCollection.Add(ClientName, ClientSdo)

      '
      ' Set the address for the client
      '
      Dim ClientAddress
      ClientAddress = InputBox("Enter the client's address (IP or DNS):", "Client's Address")
      Call ClientSdo.PutProperty(SDOIASLib.CLIENTPROPERTIES.PROPERTY_CLIENT_ADDRESS, ClientAddress)

      '
      ' Set the shared secret for the client
      '                                    
      Dim ClientSecret
      ClientSecret = InputBox("Enter the client's shared secret:", "Client's shared Secret")
      Call ClientSdo.PutProperty(SDOIASLib.CLIENTPROPERTIES.PROPERTY_CLIENT_SHARED_SECRET, ClientSecret)

      '
      ' Apply the changes
      '  
      Call ClientSdo.Apply()

      Exit Sub

ErrorHandler:
      ' Insert code to handle the error here
      Resume Next

   End Sub
End Class

```



## <a name="related-topics"></a><span data-ttu-id="cc44f-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc44f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc44f-110">**CLIENTproperties**</span><span class="sxs-lookup"><span data-stu-id="cc44f-110">**CLIENTPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-clientproperties)
</dt> <dt>

[<span data-ttu-id="cc44f-111">Enumerando objetos em uma coleção</span><span class="sxs-lookup"><span data-stu-id="cc44f-111">Enumerating Objects in a Collection</span></span>](/windows/desktop/Nps/sdo-enumerating-objects-in-a-collection)
</dt> <dt>

[<span data-ttu-id="cc44f-112">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="cc44f-112">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[<span data-ttu-id="cc44f-113">**ISdo**</span><span class="sxs-lookup"><span data-stu-id="cc44f-113">**ISdo**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[<span data-ttu-id="cc44f-114">**ISdoMachine**</span><span class="sxs-lookup"><span data-stu-id="cc44f-114">**ISdoMachine**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdomachine)
</dt> <dt>

[<span data-ttu-id="cc44f-115">**RADIUSproperties**</span><span class="sxs-lookup"><span data-stu-id="cc44f-115">**RADIUSPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)
</dt> </dl>

 

 