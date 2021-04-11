---
description: 'Saiba mais sobre: método API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, Cadeia de caracteres)'
title: Método API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, Cadeia de caracteres)
TOCTitle: JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,Microsoft.Isam.Esent.Interop.JET_CALLBACK,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100819
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d8d9d65af803a011c0a6a79fdaec2fb0a44755b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172298"
---
# <a name="apijetsetsystemparameter-method-jet_instance-jet_sesid-jet_param-jet_callback-string"></a><span data-ttu-id="4a4ed-103">Método API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, Cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="4a4ed-103">Api.JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)</span></span>

<span data-ttu-id="4a4ed-104">Define opções de configuração do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4a4ed-104">Sets database configuration options.</span></span>

<span data-ttu-id="4a4ed-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4a4ed-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4a4ed-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4a4ed-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4a4ed-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a4ed-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    paramValue As JET_CALLBACK, _
    paramString As String _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As JET_CALLBACK
Dim paramString As String
Dim returnValue As JET_wrn

returnValue = Api.JetSetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString)
```

``` csharp
public static JET_wrn JetSetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    JET_CALLBACK paramValue,
    string paramString
)
```

#### <a name="parameters"></a><span data-ttu-id="4a4ed-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a4ed-108">Parameters</span></span>

  - <span data-ttu-id="4a4ed-109">instance</span><span class="sxs-lookup"><span data-stu-id="4a4ed-109">instance</span></span>  
    <span data-ttu-id="4a4ed-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4a4ed-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="4a4ed-111">A instância na qual definir a opção ou [nil](./jet-instance.nil-property.md) para definir a opção em todas as instâncias.</span><span class="sxs-lookup"><span data-stu-id="4a4ed-111">The instance to set the option on or [Nil](./jet-instance.nil-property.md) to set the option on all instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a4ed-112">sesid</span><span class="sxs-lookup"><span data-stu-id="4a4ed-112">sesid</span></span>  
    <span data-ttu-id="4a4ed-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4a4ed-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4a4ed-114">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="4a4ed-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a4ed-115">paramid</span><span class="sxs-lookup"><span data-stu-id="4a4ed-115">paramid</span></span>  
    <span data-ttu-id="4a4ed-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_param](./jet-param-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4a4ed-116">Type: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span></span>  
    
    <span data-ttu-id="4a4ed-117">O parâmetro a ser definido.</span><span class="sxs-lookup"><span data-stu-id="4a4ed-117">The parameter to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a4ed-118">paramValue</span><span class="sxs-lookup"><span data-stu-id="4a4ed-118">paramValue</span></span>  
    <span data-ttu-id="4a4ed-119">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="4a4ed-119">Type: [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span></span>  
    
    <span data-ttu-id="4a4ed-120">O valor do parâmetro a ser definido, se o parâmetro for um JET_CALLBACK.</span><span class="sxs-lookup"><span data-stu-id="4a4ed-120">The value of the parameter to set, if the parameter is a JET_CALLBACK.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a4ed-121">paramstring</span><span class="sxs-lookup"><span data-stu-id="4a4ed-121">paramString</span></span>  
    <span data-ttu-id="4a4ed-122">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4a4ed-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4a4ed-123">O valor do parâmetro a ser definido, se o parâmetro for um tipo de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4a4ed-123">The value of the parameter to set, if the parameter is a string type.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4a4ed-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a4ed-124">Return value</span></span>

<span data-ttu-id="4a4ed-125">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4a4ed-125">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="4a4ed-126">Um código de aviso de ESENT.</span><span class="sxs-lookup"><span data-stu-id="4a4ed-126">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4a4ed-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a4ed-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4a4ed-128">Referência</span><span class="sxs-lookup"><span data-stu-id="4a4ed-128">Reference</span></span>

[<span data-ttu-id="4a4ed-129">Classe de API</span><span class="sxs-lookup"><span data-stu-id="4a4ed-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4a4ed-130">Membros da API</span><span class="sxs-lookup"><span data-stu-id="4a4ed-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4a4ed-131">Sobrecarga de JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="4a4ed-131">JetSetSystemParameter overload</span></span>](./api.jetsetsystemparameter-method.md)

[<span data-ttu-id="4a4ed-132">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4a4ed-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
