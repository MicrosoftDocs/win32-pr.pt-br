---
description: 'Saiba mais sobre: CimMofDeserializer. GetIncludedFileContent delegate (cadeia de caracteres)'
title: Delegado CimMofDeserializer. GetIncludedFileContent (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.GetIncludedFileContent delegate (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: T:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent
ms.date: 11/13/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent
- Microsoft::Management::Infrastructure::Serialization::CimMofDeserializer::GetIncludedFileContent
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent..ctor
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent.BeginInvoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent.Invoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent.EndInvoke
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: cb922d785da7d01de93adec56cefee29785210d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105802161"
---
# <a name="cimmofdeserializergetincludedfilecontent-delegate-string"></a><span data-ttu-id="6f2b0-103">CimMofDeserializer. GetIncludedFileContent delegate (cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="6f2b0-103">CimMofDeserializer.GetIncludedFileContent delegate (String)</span></span>

<span data-ttu-id="6f2b0-104">Representa um retorno de chamada para recuperar o conteúdo do arquivo na forma de uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="6f2b0-104">Represents a callback to retrieve the file's contents in the form of a byte array.</span></span>

<span data-ttu-id="6f2b0-105">**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6f2b0-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="6f2b0-106">**Assembly:**  Microsoft. Management. Infrastructure (em Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="6f2b0-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="6f2b0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f2b0-107">Syntax</span></span>

``` csharp
public delegate byte[] GetIncludedFileContent(
    string fileName
)
```

``` c++
public delegate array<unsigned char>^ GetIncludedFileContent(
    String^ fileName
)
```

``` fsharp
type GetIncludedFileContent = 
    delegate of 
        fileName:string -> byte[]
```

``` vb
Public Delegate Function GetIncludedFileContent (
    fileName As String
) As Byte()
```

#### <a name="parameters"></a><span data-ttu-id="6f2b0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f2b0-108">Parameters</span></span>

  - <span data-ttu-id="6f2b0-109">fileName</span><span class="sxs-lookup"><span data-stu-id="6f2b0-109">fileName</span></span>  
    <span data-ttu-id="6f2b0-110">Tipo: [System. String](/dotnet/api/system.string?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="6f2b0-110">Type: [System.String](/dotnet/api/system.string?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="6f2b0-111">Nome do arquivo, incluindo o caminho.</span><span class="sxs-lookup"><span data-stu-id="6f2b0-111">File name, including path.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6f2b0-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6f2b0-112">Return Value</span></span>

<span data-ttu-id="6f2b0-113">Tipo: [System. byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="6f2b0-113">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>

<span data-ttu-id="6f2b0-114">Retorna o conteúdo do arquivo na forma de uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="6f2b0-114">Returns the file's contents in the form of a byte array.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f2b0-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6f2b0-115">See Also</span></span>

<span data-ttu-id="6f2b0-116">[Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6f2b0-116">[Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
