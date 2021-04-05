---
description: 'Saiba mais sobre: método API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, Cadeia de caracteres, Int32)'
title: Método API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, Cadeia de caracteres, Int32)
TOCTitle: JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.IntPtr@,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100731
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 25e8430931cbf45c84d65fb68ae877ed96e7cea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826943"
---
# <a name="apijetgetsystemparameter-method-jet_instance-jet_sesid-jet_param-intptr-string-int32"></a><span data-ttu-id="d2637-103">Método API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, Cadeia de caracteres, Int32)</span><span class="sxs-lookup"><span data-stu-id="d2637-103">Api.JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)</span></span>

<span data-ttu-id="d2637-104">Obtém as opções de configuração do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d2637-104">Gets database configuration options.</span></span>

<span data-ttu-id="d2637-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d2637-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d2637-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d2637-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d2637-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2637-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetGetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    ByRef paramValue As IntPtr, _
    <OutAttribute> ByRef paramString As String, _
    maxParam As Integer _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As IntPtr
Dim paramString As String
Dim maxParam As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetGetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString, _
    maxParam)
```

``` csharp
public static JET_wrn JetGetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    ref IntPtr paramValue,
    out string paramString,
    int maxParam
)
```

#### <a name="parameters"></a><span data-ttu-id="d2637-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2637-108">Parameters</span></span>

  - <span data-ttu-id="d2637-109">instance</span><span class="sxs-lookup"><span data-stu-id="d2637-109">instance</span></span>  
    <span data-ttu-id="d2637-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d2637-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="d2637-111">A instância da qual as opções são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="d2637-111">The instance to retrieve the options from.</span></span>

<!-- end list -->

  - <span data-ttu-id="d2637-112">sesid</span><span class="sxs-lookup"><span data-stu-id="d2637-112">sesid</span></span>  
    <span data-ttu-id="d2637-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d2637-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d2637-114">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="d2637-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d2637-115">paramid</span><span class="sxs-lookup"><span data-stu-id="d2637-115">paramid</span></span>  
    <span data-ttu-id="d2637-116">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_param](./jet-param-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d2637-116">Type: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span></span>  
    
    <span data-ttu-id="d2637-117">O parâmetro a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="d2637-117">The parameter to get.</span></span>

<!-- end list -->

  - <span data-ttu-id="d2637-118">paramValue</span><span class="sxs-lookup"><span data-stu-id="d2637-118">paramValue</span></span>  
    <span data-ttu-id="d2637-119">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="d2637-119">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="d2637-120">Retorna o valor do parâmetro, se o valor for um inteiro.</span><span class="sxs-lookup"><span data-stu-id="d2637-120">Returns the value of the parameter, if the value is an integer.</span></span>

<!-- end list -->

  - <span data-ttu-id="d2637-121">paramstring</span><span class="sxs-lookup"><span data-stu-id="d2637-121">paramString</span></span>  
    <span data-ttu-id="d2637-122">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d2637-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d2637-123">Retorna o valor do parâmetro, se o valor for uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d2637-123">Returns the value of the parameter, if the value is a string.</span></span>

<!-- end list -->

  - <span data-ttu-id="d2637-124">maxParam</span><span class="sxs-lookup"><span data-stu-id="d2637-124">maxParam</span></span>  
    <span data-ttu-id="d2637-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d2637-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d2637-126">O tamanho máximo da cadeia de caracteres do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d2637-126">The maximum size of the parameter string.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d2637-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2637-127">Return value</span></span>

<span data-ttu-id="d2637-128">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d2637-128">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="d2637-129">Um código de aviso de ESENT.</span><span class="sxs-lookup"><span data-stu-id="d2637-129">An ESENT warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="d2637-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2637-130">Remarks</span></span>

<span data-ttu-id="d2637-131">[ErrorToString](./jet-param-enumeration.md) passa o número do erro no ParamValue, que é o motivo pelo qual ele é um parâmetro ref e não um parâmetro out.</span><span class="sxs-lookup"><span data-stu-id="d2637-131">[ErrorToString](./jet-param-enumeration.md) passes in the error number in the paramValue, which is why it is a ref parameter and not an out parameter.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2637-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2637-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d2637-133">Referência</span><span class="sxs-lookup"><span data-stu-id="d2637-133">Reference</span></span>

[<span data-ttu-id="d2637-134">Classe de API</span><span class="sxs-lookup"><span data-stu-id="d2637-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d2637-135">Membros da API</span><span class="sxs-lookup"><span data-stu-id="d2637-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d2637-136">Sobrecarga de JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="d2637-136">JetGetSystemParameter overload</span></span>](./api.jetgetsystemparameter-method.md)

[<span data-ttu-id="d2637-137">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d2637-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
