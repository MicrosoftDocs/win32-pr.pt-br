---
description: 'Saiba mais sobre: JET_SESID. Método ToString (String, IFormatProvider)'
title: JET_SESID. Método ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.tostring(v=EXCHG.10)
ms:contentKeyID: 39512468
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5565e67cc0f91fd1c2edb0d9c0aa421211c57c2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748348"
---
# <a name="jet_sesidtostring-method-string-iformatprovider"></a><span data-ttu-id="afefc-103">JET_SESID. Método ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="afefc-103">JET_SESID.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="afefc-104">Formata o valor da instância atual usando o formato especificado.</span><span class="sxs-lookup"><span data-stu-id="afefc-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="afefc-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="afefc-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="afefc-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="afefc-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="afefc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afefc-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_SESID
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

#### <a name="parameters"></a><span data-ttu-id="afefc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="afefc-108">Parameters</span></span>

  - <span data-ttu-id="afefc-109">format</span><span class="sxs-lookup"><span data-stu-id="afefc-109">format</span></span>  
    <span data-ttu-id="afefc-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="afefc-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="afefc-111">A [cadeia de caracteres](/dotnet/api/system.string) que especifica o formato a ser usado; ou NULL para usar o formato padrão definido para o tipo da implementação de [IFormattable](/dotnet/api/system.iformattable) .</span><span class="sxs-lookup"><span data-stu-id="afefc-111">The [String](/dotnet/api/system.string) specifying the format to use; or, null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="afefc-112">formatProvider</span><span class="sxs-lookup"><span data-stu-id="afefc-112">formatProvider</span></span>  
    <span data-ttu-id="afefc-113">Tipo: [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="afefc-113">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="afefc-114">O [IFormatProvider](/dotnet/api/system.iformatprovider) a ser usado para formatar o valor; ou, NULL para obter as informações de formato numérico da configuração de localidade atual do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="afefc-114">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value; or, null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="afefc-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="afefc-115">Return value</span></span>

<span data-ttu-id="afefc-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="afefc-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="afefc-117">Uma [cadeia de caracteres](/dotnet/api/system.string) que contém o valor da instância atual no formato especificado.</span><span class="sxs-lookup"><span data-stu-id="afefc-117">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="afefc-118">Implementações</span><span class="sxs-lookup"><span data-stu-id="afefc-118">Implements</span></span>

[<span data-ttu-id="afefc-119">IFormattable. ToString (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="afefc-119">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="afefc-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="afefc-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="afefc-121">Referência</span><span class="sxs-lookup"><span data-stu-id="afefc-121">Reference</span></span>

[<span data-ttu-id="afefc-122">Estrutura de JET_SESID</span><span class="sxs-lookup"><span data-stu-id="afefc-122">JET_SESID structure</span></span>](./jet-sesid-structure.md)

[<span data-ttu-id="afefc-123">Membros do JET_SESID</span><span class="sxs-lookup"><span data-stu-id="afefc-123">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="afefc-124">Sobrecarga de ToString</span><span class="sxs-lookup"><span data-stu-id="afefc-124">ToString overload</span></span>](./jet-sesid.tostring-method2.md)

[<span data-ttu-id="afefc-125">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="afefc-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
