---
title: Tipo simples de processTokenSidType
description: Define os valores possíveis para o elemento ProcessTokenSidType (PrincipalType).
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- Agendador de Tarefas tipo simples de processTokenSidType
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13cf70534510e1aed8def9005d0c2d1eafab2a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369464"
---
# <a name="processtokensidtype-simple-type"></a><span data-ttu-id="c636e-104">Tipo simples de processTokenSidType</span><span class="sxs-lookup"><span data-stu-id="c636e-104">processTokenSidType Simple Type</span></span>

<span data-ttu-id="c636e-105">Define os valores possíveis para o elemento [**ProcessTokenSidType (PrincipalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c636e-105">Defines the possible values for the [**ProcessTokenSidType (principalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="processTokenSidType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="None"
         />
        <xs:enumeration
            value="Unrestricted"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="c636e-106">Valores de enumeração</span><span class="sxs-lookup"><span data-stu-id="c636e-106">Enumeration values</span></span>

<span data-ttu-id="c636e-107">O tipo simples **processTokenSidType** define os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c636e-107">The **processTokenSidType** simple type defines the following values.</span></span>



| <span data-ttu-id="c636e-108">Valor</span><span class="sxs-lookup"><span data-stu-id="c636e-108">Value</span></span>        | <span data-ttu-id="c636e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c636e-109">Description</span></span>                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c636e-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c636e-110">None</span></span>         | <span data-ttu-id="c636e-111">As tarefas são executadas em um processo que não contém um SID de token de processo (nenhuma alteração será feita na lista de grupos de tokens de processo).</span><span class="sxs-lookup"><span data-stu-id="c636e-111">Tasks are run in a process that does not contain a process token SID (no changes will be made to the process token groups list).</span></span><br/> |
| <span data-ttu-id="c636e-112">Irrestrito</span><span class="sxs-lookup"><span data-stu-id="c636e-112">Unrestricted</span></span> | <span data-ttu-id="c636e-113">Um SID de tarefa será derivado do caminho completo da tarefa e será adicionado à lista de grupos de tokens de processo.</span><span class="sxs-lookup"><span data-stu-id="c636e-113">A task SID will be derived from the full task path and will be added to the process token groups list.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="c636e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c636e-114">Requirements</span></span>



| <span data-ttu-id="c636e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c636e-115">Requirement</span></span> | <span data-ttu-id="c636e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c636e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c636e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c636e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c636e-118">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c636e-118">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c636e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c636e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c636e-120">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="c636e-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





