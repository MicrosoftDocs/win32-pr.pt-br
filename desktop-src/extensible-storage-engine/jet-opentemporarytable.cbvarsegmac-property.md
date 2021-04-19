---
description: 'Saiba mais sobre a propriedade: JET_OPENTEMPORARYTABLE. cbVarSegMac'
title: Propriedade JET_OPENTEMPORARYTABLE. cbVarSegMac (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'cbVarSegMac property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbvarsegmac(v=EXCHG.10)
ms:contentKeyID: 55104115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbVarSegMac
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbVarSegMac
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37fe218a9741235410d2452f04f082dc6673eaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782632"
---
# <a name="jet_opentemporarytablecbvarsegmac-property"></a><span data-ttu-id="83d9c-103">Propriedade JET_OPENTEMPORARYTABLE. cbVarSegMac</span><span class="sxs-lookup"><span data-stu-id="83d9c-103">JET_OPENTEMPORARYTABLE.cbVarSegMac property</span></span>

<span data-ttu-id="83d9c-104">Obtém ou define a quantidade máxima de dados que serão usados de qualquer variável lengthcolumn para construir uma chave para uma determinada linha.</span><span class="sxs-lookup"><span data-stu-id="83d9c-104">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="83d9c-105">Esse parâmetro pode ser usado para controlar a quantidade de espaço de chave consumida por qualquer coluna de chave fornecida.</span><span class="sxs-lookup"><span data-stu-id="83d9c-105">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="83d9c-106">Esse limite está em bytes.</span><span class="sxs-lookup"><span data-stu-id="83d9c-106">This limit is in bytes.</span></span> <span data-ttu-id="83d9c-107">Se esse parâmetro for zero ou for o mesmo que a propriedade [cbKeyMost](./jet-opentemporarytable.cbkeymost-property.md) , nenhum limite estará em vigor.</span><span class="sxs-lookup"><span data-stu-id="83d9c-107">If this parameter is zero or is the same as the [cbKeyMost](./jet-opentemporarytable.cbkeymost-property.md) property then no limit is in effect.</span></span>

<span data-ttu-id="83d9c-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="83d9c-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="83d9c-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="83d9c-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="83d9c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83d9c-110">Syntax</span></span>

``` vb
'Declaration
Public Property cbVarSegMac As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbVarSegMac

instance.cbVarSegMac = value
```

``` csharp
public int cbVarSegMac { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="83d9c-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="83d9c-111">Property value</span></span>

<span data-ttu-id="83d9c-112">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="83d9c-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="83d9c-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="83d9c-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="83d9c-114">Referência</span><span class="sxs-lookup"><span data-stu-id="83d9c-114">Reference</span></span>

[<span data-ttu-id="83d9c-115">Classe JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="83d9c-115">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="83d9c-116">Membros do JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="83d9c-116">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="83d9c-117">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="83d9c-117">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
