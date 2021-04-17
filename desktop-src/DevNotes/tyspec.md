---
description: Define maneiras de mapear para uma ID de classe.
ms.assetid: 1af170e3-1edd-411f-acba-d4b244107996
title: Enumeração TYSPEC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TYSPEC
api_type:
- IDLDef
api_location:
- Wtypes.idl
ms.openlocfilehash: b4c8cf38a8f99458e76cabc726aa39ad01a71ebc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747289"
---
# <a name="tyspec-enumeration"></a><span data-ttu-id="c7721-103">Enumeração TYSPEC</span><span class="sxs-lookup"><span data-stu-id="c7721-103">TYSPEC enumeration</span></span>

<span data-ttu-id="c7721-104">Define maneiras de mapear para uma ID de classe.</span><span class="sxs-lookup"><span data-stu-id="c7721-104">Defines ways of mapping to a class ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7721-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7721-105">Syntax</span></span>


```C++
typedef enum tagTYSPEC { 
  TYSPEC_CLSID,
  TYSPEC_FILEEXT,
  TYSPEC_MIMETYPE,
  TYSPEC_FILENAME,
  TYSPEC_PROGID,
  TYSPEC_PACKAGENAME,
  TYSPEC_OBJECTID
} TYSPEC;
```



## <a name="constants"></a><span data-ttu-id="c7721-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c7721-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c7721-107"><span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**TYSPEC \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="c7721-107"><span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**TYSPEC\_CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="c7721-108">UM CLSID.</span><span class="sxs-lookup"><span data-stu-id="c7721-108">A CLSID.</span></span>

</dd> <dt>

<span data-ttu-id="c7721-109"><span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**TYSPEC \_ FILEEXT**</span><span class="sxs-lookup"><span data-stu-id="c7721-109"><span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**TYSPEC\_FILEEXT**</span></span>
</dt> <dd>

<span data-ttu-id="c7721-110">Uma extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c7721-110">A file name extension.</span></span> <span data-ttu-id="c7721-111">Não há suporte para esse valor no momento.</span><span class="sxs-lookup"><span data-stu-id="c7721-111">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="c7721-112"><span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**\_MIMETYPE TYSPEC**</span><span class="sxs-lookup"><span data-stu-id="c7721-112"><span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**TYSPEC\_MIMETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="c7721-113">Um tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="c7721-113">A MIME type.</span></span> <span data-ttu-id="c7721-114">Não há suporte para esse valor no momento.</span><span class="sxs-lookup"><span data-stu-id="c7721-114">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="c7721-115"><span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**\_nome de arquivo TYSPEC**</span><span class="sxs-lookup"><span data-stu-id="c7721-115"><span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**TYSPEC\_FILENAME**</span></span>
</dt> <dd>

<span data-ttu-id="c7721-116">Um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c7721-116">A file name.</span></span> <span data-ttu-id="c7721-117">Não há suporte para esse valor no momento.</span><span class="sxs-lookup"><span data-stu-id="c7721-117">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="c7721-118"><span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**ProgID do TYSPEC \_**</span><span class="sxs-lookup"><span data-stu-id="c7721-118"><span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**TYSPEC\_PROGID**</span></span>
</dt> <dd>

<span data-ttu-id="c7721-119">UM PROGID.</span><span class="sxs-lookup"><span data-stu-id="c7721-119">A PROGID.</span></span> <span data-ttu-id="c7721-120">Não há suporte para esse valor no momento.</span><span class="sxs-lookup"><span data-stu-id="c7721-120">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="c7721-121"><span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC \_ PackageName**</span><span class="sxs-lookup"><span data-stu-id="c7721-121"><span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC\_PACKAGENAME**</span></span>
</dt> <dd>

<span data-ttu-id="c7721-122">Um nome de pacote.</span><span class="sxs-lookup"><span data-stu-id="c7721-122">A package name.</span></span> <span data-ttu-id="c7721-123">Não há suporte para esse valor no momento.</span><span class="sxs-lookup"><span data-stu-id="c7721-123">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="c7721-124"><span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**\_OBJECTID TYSPEC**</span><span class="sxs-lookup"><span data-stu-id="c7721-124"><span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**TYSPEC\_OBJECTID**</span></span>
</dt> <dd>

<span data-ttu-id="c7721-125">Uma ID do objeto.</span><span class="sxs-lookup"><span data-stu-id="c7721-125">An object ID.</span></span> <span data-ttu-id="c7721-126">Não há suporte para esse valor no momento.</span><span class="sxs-lookup"><span data-stu-id="c7721-126">This value is not currently supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7721-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7721-127">Remarks</span></span>

<span data-ttu-id="c7721-128">A União **uCLSSPEC** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c7721-128">The **uCLSSPEC** union is defined as follows:</span></span>

``` syntax
typedef union switch(DWORD tyspec) {
    case TYSPEC_CLSID:
        CLSID clsid;
    case TYSPEC_FILEEXT:
        LPOLESTR pFileExt;
    case TYSPEC_MIMETYPE:
        LPOLESTR pMimeType;
    case TYSPEC_PROGID:
        LPOLESTR pProgId;
    case TYSPEC_FILENAME:
        LPOLESTR pFileName;
    case TYSPEC_PACKAGENAME:
        struct {
        LPOLESTR pPackageName;
        GUID PolicyId;
        } ByName;
    case TYSPEC_OBJECTID:
        struct {
        GUID ObjectId;
        GUID PolicyId;
        } ByObjectId;
} uCLSSPEC;
```

## <a name="requirements"></a><span data-ttu-id="c7721-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7721-129">Requirements</span></span>



| <span data-ttu-id="c7721-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7721-130">Requirement</span></span> | <span data-ttu-id="c7721-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c7721-131">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7721-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="c7721-132">IDL</span></span><br/> | <dl> <span data-ttu-id="c7721-133"><dt>Wtypes. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7721-133"><dt>Wtypes.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7721-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7721-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7721-135">**Instalar**</span><span class="sxs-lookup"><span data-stu-id="c7721-135">**CoInstall**</span></span>](/windows/win32/api/objbase/nf-objbase-coinstall)
</dt> </dl>

 

 
