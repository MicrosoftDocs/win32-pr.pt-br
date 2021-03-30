---
title: Modificando um objeto ADSI do ADO
description: O ADSI para o Windows 2000 e o DS Client inclui um provedor de OLE DB somente leitura. Isso significa que você não pode, no momento, emitir a instrução UPDATE no dialeto SQL.
ms.assetid: b0a107ed-0271-45ab-b971-f589f34472e2
ms.tgt_platform: multiple
keywords:
- Modificando um objeto ADSI do ADO ADSI
- ADSI do objeto de dados ActiveX, modificando um objeto ADSI do ADO
- ADSI ADSI, código de exemplo C/C++, modificando um objeto ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7291088915a537231077e1d75161b57684caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634871"
---
# <a name="modifying-an-adsi-object-from-ado"></a><span data-ttu-id="7279f-107">Modificando um objeto ADSI do ADO</span><span class="sxs-lookup"><span data-stu-id="7279f-107">Modifying an ADSI Object from ADO</span></span>

<span data-ttu-id="7279f-108">O ADSI para o Windows 2000 e o DS Client inclui um provedor de OLE DB somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7279f-108">ADSI for Windows 2000 and DS Client includes a read-only OLE DB provider.</span></span> <span data-ttu-id="7279f-109">Isso significa que você não pode, no momento, emitir a instrução UPDATE no dialeto SQL.</span><span class="sxs-lookup"><span data-stu-id="7279f-109">This means that you cannot, at present, issue the UPDATE statement in the SQL dialect.</span></span>

<span data-ttu-id="7279f-110">**Para modificar um objeto retornado de uma consulta ADO**</span><span class="sxs-lookup"><span data-stu-id="7279f-110">**To modify an object returned from an ADO query**</span></span>

1.  <span data-ttu-id="7279f-111">Solicite o **ADsPath** ao especificar um nome de atributo, como em "Select ADsPath,..."</span><span class="sxs-lookup"><span data-stu-id="7279f-111">Request the **ADsPath** when specifying an attribute name, as in "SELECT ADsPath, ..."</span></span>
2.  <span data-ttu-id="7279f-112">Execute a consulta e obtenha o atributo **ADsPath** .</span><span class="sxs-lookup"><span data-stu-id="7279f-112">Execute the query and get the **ADsPath** attribute.</span></span>
3.  <span data-ttu-id="7279f-113">Associe-se ao conjunto de registros usando **ADsPath** e modifique os atributos.</span><span class="sxs-lookup"><span data-stu-id="7279f-113">Bind to the record set using **ADsPath**, and modify the attributes.</span></span>

<span data-ttu-id="7279f-114">O exemplo de código a seguir mostra como modificar um objeto ADSI depois de executar as etapas descritas no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="7279f-114">The following code example shows how to modify an ADSI object after performing the steps outlined in the preceding example.</span></span>


```VB
Dim Con As New Connection
Dim rs As New Recordset
Dim command As New Command
Dim usr As IADsUser

' Replace department for all users in OU=sales.
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
 
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = con
 
command.CommandText = "SELECT AdsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=com' WHERE objectClass = 'user'"
 
command.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Set rs = command.Execute
While Not rs.EOF
    Set usr = GetObject(rs.Fields("AdsPath").Value)
    usr.Put "department", "1001"
    usr.SetInfo
    rs.MoveNext
Wend
```



 

 




