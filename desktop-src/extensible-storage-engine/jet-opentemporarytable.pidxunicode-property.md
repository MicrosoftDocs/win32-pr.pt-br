---
description: 'Saiba mais sobre a propriedade: JET_OPENTEMPORARYTABLE. pidxunicode'
title: Propriedade JET_OPENTEMPORARYTABLE. pidxunicode (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'pidxunicode property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.pidxunicode(v=EXCHG.10)
ms:contentKeyID: 55104227
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 98e5beb4f4523f5e6a6da37a999b6c0a2ab7b4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762348"
---
# <a name="jet_opentemporarytablepidxunicode-property"></a><span data-ttu-id="745c9-103">Propriedade JET_OPENTEMPORARYTABLE. pidxunicode</span><span class="sxs-lookup"><span data-stu-id="745c9-103">JET_OPENTEMPORARYTABLE.pidxunicode property</span></span>

<span data-ttu-id="745c9-104">Obtém ou define os sinalizadores de ID de localidade e normalização a serem usados para comparar quaisquer dados de coluna de chave Unicode na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="745c9-104">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="745c9-105">Quando esse parâmetro for NULL, o LCID padrão será usado para comparar todas as colunas de chave Unicode na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="745c9-105">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="745c9-106">O LCID padrão é a localidade inglês dos EUA.</span><span class="sxs-lookup"><span data-stu-id="745c9-106">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="745c9-107">Quando esse parâmetro é nulo, os sinalizadores de normalização padrão serão usados para comparar quaisquer dados de coluna de chave Unicode na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="745c9-107">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="745c9-108">Os sinalizadores de normalização padrão são: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="745c9-108">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="745c9-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="745c9-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="745c9-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="745c9-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="745c9-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="745c9-111">Syntax</span></span>

``` vb
'Declaration
Public Property pidxunicode As JET_UNICODEINDEX
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_UNICODEINDEX

value = instance.pidxunicode

instance.pidxunicode = value
```

``` csharp
public JET_UNICODEINDEX pidxunicode { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="745c9-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="745c9-112">Property value</span></span>

<span data-ttu-id="745c9-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span><span class="sxs-lookup"><span data-stu-id="745c9-113">Type: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="745c9-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="745c9-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="745c9-115">Referência</span><span class="sxs-lookup"><span data-stu-id="745c9-115">Reference</span></span>

[<span data-ttu-id="745c9-116">Classe JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="745c9-116">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="745c9-117">Membros do JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="745c9-117">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="745c9-118">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="745c9-118">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
