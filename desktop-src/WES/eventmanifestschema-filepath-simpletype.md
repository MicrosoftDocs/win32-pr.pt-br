---
title: Tipo simples de filePath
description: Define uma cadeia de caracteres que contém um caminho totalmente qualificado para um arquivo.
ms.assetid: a9b8f40a-fecd-4325-b068-a5aca3133134
keywords:
- Caminho de log de tipo simples de filePath
topic_type:
- apiref
api_name:
- filePath
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 492580634c1a48c88df6f50de2582c215ec7ecb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454777"
---
# <a name="filepath-simple-type"></a><span data-ttu-id="acb5c-104">Tipo simples de filePath</span><span class="sxs-lookup"><span data-stu-id="acb5c-104">filePath Simple Type</span></span>

<span data-ttu-id="acb5c-105">Define uma cadeia de caracteres que contém um caminho totalmente qualificado para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="acb5c-105">Defines a string that contains a fully qualified path to a file.</span></span> <span data-ttu-id="acb5c-106">O caminho pode conter variáveis de ambiente.</span><span class="sxs-lookup"><span data-stu-id="acb5c-106">The path may contain environment variables.</span></span>

``` syntax
<xs:simpleType name="filePath">
    <xs:restriction
        base="xs:string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="acb5c-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acb5c-107">Requirements</span></span>



| <span data-ttu-id="acb5c-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="acb5c-108">Requirement</span></span> | <span data-ttu-id="acb5c-109">Valor</span><span class="sxs-lookup"><span data-stu-id="acb5c-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="acb5c-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acb5c-110">Minimum supported client</span></span><br/> | <span data-ttu-id="acb5c-111">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="acb5c-111">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="acb5c-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acb5c-112">Minimum supported server</span></span><br/> | <span data-ttu-id="acb5c-113">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="acb5c-113">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





