---
title: Usando um objeto de dados ActiveX para ligar a provedores ADSI
description: Como a ADSI também é um provedor de OLE DB, você pode usar um ADO (ActiveX Data Object) para se conectar a provedores ADSI.
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- ADSI do objeto de dados ActiveX
- ADSI do objeto de dados ActiveX, usando o ADO para ligar a provedores ADSI
- ADSI de provedores de serviço, usando o objeto de dados ActiveX para associar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efb64da28d5c4c2596fcf889e3b3db88b77205c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004851"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a><span data-ttu-id="73f65-106">Usando um objeto de dados ActiveX para ligar a provedores ADSI</span><span class="sxs-lookup"><span data-stu-id="73f65-106">Using an ActiveX Data Object to Bind to ADSI Providers</span></span>

<span data-ttu-id="73f65-107">Como a ADSI também é um provedor de OLE DB, você pode usar um ADO (ActiveX Data Object) para se conectar a provedores ADSI.</span><span class="sxs-lookup"><span data-stu-id="73f65-107">Since ADSI is also an OLE DB provider, you can use an ActiveX Data Object (ADO) to connect to ADSI providers.</span></span> <span data-ttu-id="73f65-108">Assim como ocorre com outros provedores de ADO, para se conectar a um provedor de OLE DB, você deve criar um novo objeto de conexão e, opcionalmente, especificar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="73f65-108">As with other ADO providers, to connect to an OLE DB provider, you must create a new connection object and, optionally, specify the credentials.</span></span> <span data-ttu-id="73f65-109">O nome do provedor de OLE DB ADSI é **ADsDSOObject**.</span><span class="sxs-lookup"><span data-stu-id="73f65-109">The name of the ADSI OLE DB provider is **ADsDSOObject**.</span></span>

<span data-ttu-id="73f65-110">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="73f65-110">For example:</span></span>


```VB
Dim con As New Connection 
'VBScript use: con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
con.Open "YourDescriptionHere"
```



<span data-ttu-id="73f65-111">No exemplo anterior, você está conectado em nome do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="73f65-111">In the previous example, you are connected on behalf of the current user.</span></span> <span data-ttu-id="73f65-112">Para especificar credenciais diferentes, use as propriedades de conexão:</span><span class="sxs-lookup"><span data-stu-id="73f65-112">To specify different credentials, use connection properties:</span></span>


```VB
con.Provider = "ADsDSOObject"
con.Properties("User ID") = "jeffsmith"
con.Properties("Password") = "guesswhat?"
con.Properties("Encrypt Password") = True
con.Open "YourDescriptionHere"
```



<span data-ttu-id="73f65-113">O OLE DB ADSI define as propriedades de conexão a seguir.</span><span class="sxs-lookup"><span data-stu-id="73f65-113">ADSI OLE DB defines the following connection properties.</span></span>



| <span data-ttu-id="73f65-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="73f65-114">Property</span></span>           | <span data-ttu-id="73f65-115">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="73f65-115">Data type</span></span>   | <span data-ttu-id="73f65-116">Padrão</span><span class="sxs-lookup"><span data-stu-id="73f65-116">Default</span></span>   |
|--------------------|-------------|-----------|
| <span data-ttu-id="73f65-117">"ID de usuário"</span><span class="sxs-lookup"><span data-stu-id="73f65-117">"User ID"</span></span>          | <span data-ttu-id="73f65-118">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="73f65-118">**BSTR**</span></span>    | <span data-ttu-id="73f65-119">**NULL**</span><span class="sxs-lookup"><span data-stu-id="73f65-119">**NULL**</span></span>  |
| <span data-ttu-id="73f65-120">"Password"</span><span class="sxs-lookup"><span data-stu-id="73f65-120">"Password"</span></span>         | <span data-ttu-id="73f65-121">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="73f65-121">**BSTR**</span></span>    | <span data-ttu-id="73f65-122">**NULL**</span><span class="sxs-lookup"><span data-stu-id="73f65-122">**NULL**</span></span>  |
| <span data-ttu-id="73f65-123">"Criptografar senha"</span><span class="sxs-lookup"><span data-stu-id="73f65-123">"Encrypt Password"</span></span> | <span data-ttu-id="73f65-124">**BOOLEAN**</span><span class="sxs-lookup"><span data-stu-id="73f65-124">**BOOLEAN**</span></span> | <span data-ttu-id="73f65-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="73f65-125">**FALSE**</span></span> |
| <span data-ttu-id="73f65-126">"Sinalizador ADSI"</span><span class="sxs-lookup"><span data-stu-id="73f65-126">"ADSI Flag"</span></span>        | <span data-ttu-id="73f65-127">**Long**</span><span class="sxs-lookup"><span data-stu-id="73f65-127">**Long**</span></span>    | <span data-ttu-id="73f65-128">0</span><span class="sxs-lookup"><span data-stu-id="73f65-128">0</span></span>         |



 

<span data-ttu-id="73f65-129">Usando OLE DB ADO, não é possível associar a um objeto específico.</span><span class="sxs-lookup"><span data-stu-id="73f65-129">Using OLE DB ADO, you cannot bind to a specific object.</span></span> <span data-ttu-id="73f65-130">No entanto, você pode consultar um objeto específico e obter um conjunto de resultados de volta.</span><span class="sxs-lookup"><span data-stu-id="73f65-130">You can, however, query a specific object and get a result set back.</span></span> <span data-ttu-id="73f65-131">Somente os provedores ADSI que dão suporte ao [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) se beneficiam de ter o ADO como um modelo de programação.</span><span class="sxs-lookup"><span data-stu-id="73f65-131">Only ADSI providers that support [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) benefit from having ADO as a programming model.</span></span>

<span data-ttu-id="73f65-132">A propriedade de sinalizador ADSI é usada para especificar a opção de autenticação de associação.</span><span class="sxs-lookup"><span data-stu-id="73f65-132">The ADSI Flag property is used to specify the binding authentication option.</span></span> <span data-ttu-id="73f65-133">Essa propriedade pode ser uma combinação de sinalizadores da enumeração de enumeração de [**\_ \_ autenticação do ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) .</span><span class="sxs-lookup"><span data-stu-id="73f65-133">This property can be a combination of flags from the [**ADS\_AUTHENTICATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) enumeration.</span></span>

 

 




