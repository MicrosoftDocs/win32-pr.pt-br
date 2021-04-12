---
description: Representa o tipo de caminho que está sendo usado como um argumento.
ms.assetid: f308c638-b383-432e-9dd3-edc33b792139
title: Enumeração de PATH_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATH_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1e5602aa7384c8de6c33b407e9a536141d8d002b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500775"
---
# <a name="path_type-enumeration"></a><span data-ttu-id="5e42f-103">Enumeração de tipo de caminho \_</span><span class="sxs-lookup"><span data-stu-id="5e42f-103">PATH\_TYPE enumeration</span></span>

<span data-ttu-id="5e42f-104">Representa o tipo de caminho que está sendo usado como um argumento.</span><span class="sxs-lookup"><span data-stu-id="5e42f-104">Represents the type of path being used as an argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e42f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e42f-105">Syntax</span></span>


```C++
typedef enum _PATH_TYPE { 
  DOS_PATH,
  NT_PATH
} PATH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="5e42f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="5e42f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5e42f-107"><span id="DOS_PATH"></span><span id="dos_path"></span>**\_caminho dos**</span><span class="sxs-lookup"><span data-stu-id="5e42f-107"><span id="DOS_PATH"></span><span id="dos_path"></span>**DOS\_PATH**</span></span>
</dt> <dd>

<span data-ttu-id="5e42f-108">Caminho padrão.</span><span class="sxs-lookup"><span data-stu-id="5e42f-108">Standard path.</span></span>

</dd> <dt>

<span data-ttu-id="5e42f-109"><span id="NT_PATH"></span><span id="nt_path"></span>**caminho do NT \_**</span><span class="sxs-lookup"><span data-stu-id="5e42f-109"><span id="NT_PATH"></span><span id="nt_path"></span>**NT\_PATH**</span></span>
</dt> <dd>

<span data-ttu-id="5e42f-110">Caminho interno.</span><span class="sxs-lookup"><span data-stu-id="5e42f-110">Internal path.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e42f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e42f-111">Requirements</span></span>



| <span data-ttu-id="5e42f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e42f-112">Requirement</span></span> | <span data-ttu-id="5e42f-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5e42f-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e42f-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e42f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5e42f-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e42f-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e42f-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e42f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5e42f-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e42f-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e42f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e42f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e42f-119">**SdbCreateDatabase**</span><span class="sxs-lookup"><span data-stu-id="5e42f-119">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
</dt> <dt>

[<span data-ttu-id="5e42f-120">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="5e42f-120">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




