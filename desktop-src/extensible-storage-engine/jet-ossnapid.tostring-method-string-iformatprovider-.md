---
description: 'Saiba mais sobre: JET_OSSNAPID. Método ToString (String, IFormatProvider)'
title: JET_OSSNAPID. Método ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_OSSNAPID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ossnapid.tostring(v=EXCHG.10)
ms:contentKeyID: 39512151
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 95e93fd3a6bbf7f2fa3505fcb9480367b780ecc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788971"
---
# <a name="jet_ossnapidtostring-method-string-iformatprovider"></a><span data-ttu-id="0cb94-103">JET_OSSNAPID. Método ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="0cb94-103">JET_OSSNAPID.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="0cb94-104">Formata o valor da instância atual usando o formato especificado.</span><span class="sxs-lookup"><span data-stu-id="0cb94-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="0cb94-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0cb94-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0cb94-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0cb94-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb94-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cb94-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_OSSNAPID
Dim format As String
Dim formatProvider As IFormatProvider
Dim returnValue As String

returnValue = instance.ToString(format, _
    formatProvider)
```

``` csharp
public string ToString(
    string format,
    IFormatProvider formatProvider
)
```

#### <a name="parameters"></a><span data-ttu-id="0cb94-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0cb94-108">Parameters</span></span>

  - <span data-ttu-id="0cb94-109">format</span><span class="sxs-lookup"><span data-stu-id="0cb94-109">format</span></span>  
    <span data-ttu-id="0cb94-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="0cb94-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="0cb94-111">A [cadeia de caracteres](/dotnet/api/system.string) que especifica o formato a ser usado.</span><span class="sxs-lookup"><span data-stu-id="0cb94-111">The [String](/dotnet/api/system.string) specifying the format to use.</span></span> <span data-ttu-id="0cb94-112">-ou-NULL para usar o formato padrão definido para o tipo da implementação de [IFormattable](/dotnet/api/system.iformattable) .</span><span class="sxs-lookup"><span data-stu-id="0cb94-112">-or- null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="0cb94-113">formatProvider</span><span class="sxs-lookup"><span data-stu-id="0cb94-113">formatProvider</span></span>  
    <span data-ttu-id="0cb94-114">Tipo: [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="0cb94-114">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="0cb94-115">O [IFormatProvider](/dotnet/api/system.iformatprovider) a ser usado para formatar o valor.</span><span class="sxs-lookup"><span data-stu-id="0cb94-115">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value.</span></span> <span data-ttu-id="0cb94-116">-ou-NULL para obter as informações de formato numérico da configuração de localidade atual do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0cb94-116">-or- null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0cb94-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0cb94-117">Return value</span></span>

<span data-ttu-id="0cb94-118">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="0cb94-118">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="0cb94-119">Uma [cadeia de caracteres](/dotnet/api/system.string) que contém o valor da instância atual no formato especificado.</span><span class="sxs-lookup"><span data-stu-id="0cb94-119">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="0cb94-120">Implementações</span><span class="sxs-lookup"><span data-stu-id="0cb94-120">Implements</span></span>

[<span data-ttu-id="0cb94-121">IFormattable. ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="0cb94-121">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="0cb94-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0cb94-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0cb94-123">Referência</span><span class="sxs-lookup"><span data-stu-id="0cb94-123">Reference</span></span>

[<span data-ttu-id="0cb94-124">Estrutura de JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="0cb94-124">JET_OSSNAPID structure</span></span>](./jet-ossnapid-structure.md)

[<span data-ttu-id="0cb94-125">Membros do JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="0cb94-125">JET_OSSNAPID members</span></span>](./jet-ossnapid-members.md)

[<span data-ttu-id="0cb94-126">Sobrecarga de ToString</span><span class="sxs-lookup"><span data-stu-id="0cb94-126">ToString overload</span></span>](./jet-ossnapid.tostring-method.md)

[<span data-ttu-id="0cb94-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0cb94-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
