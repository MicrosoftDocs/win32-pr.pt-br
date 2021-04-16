---
description: 'Saiba mais sobre a propriedade: JET_OPENTEMPORARYTABLE. cbKeyMost'
title: Propriedade JET_OPENTEMPORARYTABLE. cbKeyMost (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55104228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbKeyMost
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8e608d1419cd381c507874bf1f1c334d192ae2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772631"
---
# <a name="jet_opentemporarytablecbkeymost-property"></a><span data-ttu-id="4048b-103">Propriedade JET_OPENTEMPORARYTABLE. cbKeyMost</span><span class="sxs-lookup"><span data-stu-id="4048b-103">JET_OPENTEMPORARYTABLE.cbKeyMost property</span></span>

<span data-ttu-id="4048b-104">Obtém ou define o tamanho máximo de uma chave que representa uma determinada linha.</span><span class="sxs-lookup"><span data-stu-id="4048b-104">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="4048b-105">O tamanho máximo da chave pode ser definido para controlar como as chaves são truncadas.</span><span class="sxs-lookup"><span data-stu-id="4048b-105">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="4048b-106">O truncamento de chave é importante porque pode afetar quando as linhas são consideradas distintas.</span><span class="sxs-lookup"><span data-stu-id="4048b-106">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="4048b-107">Se esse parâmetro for definido como 0 ou 255, o tamanho máximo da chave e sua semântica permanecerão idênticos ao tamanho máximo da chave com suporte do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4048b-107">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="4048b-108">Esse parâmetro também pode ser definido como um valor maior como uma função do tamanho da página do banco de dados para a instância [DatabasePageSize](./jet-param-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="4048b-108">This parameter may also be set to a larger value as a function of the database page size for the instance [DatabasePageSize](./jet-param-enumeration.md).</span></span> <span data-ttu-id="4048b-109">Confira o [melhor](./vistaparam.keymost-field.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="4048b-109">See [KeyMost](./vistaparam.keymost-field.md) for more information.</span></span>

<span data-ttu-id="4048b-110">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4048b-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="4048b-111">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4048b-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4048b-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="4048b-112">Syntax</span></span>

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="4048b-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4048b-113">Property value</span></span>

<span data-ttu-id="4048b-114">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4048b-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="4048b-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="4048b-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4048b-116">Referência</span><span class="sxs-lookup"><span data-stu-id="4048b-116">Reference</span></span>

[<span data-ttu-id="4048b-117">Classe JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="4048b-117">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="4048b-118">Membros do JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="4048b-118">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="4048b-119">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="4048b-119">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
