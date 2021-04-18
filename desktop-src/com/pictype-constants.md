---
title: Constantes PICTYPE (OleCtl. h)
description: Descreva o tipo de um objeto de imagem como retornado pelo tipo Get IPicture \_ , bem como para descrever o tipo de imagem no membro picType da estrutura PICTDESC que é passada para OleCreatePictureIndirect.
ms.assetid: 79f10687-f0eb-4b5e-a1a9-9186dbd0b51f
topic_type:
- apiref
api_name:
- PICTYPE_UNINITIALIZED
- PICTYPE_NONE
- PICTYPE_BITMAP
- PICTYPE_METAFILE
- PICTYPE_ICON
- PICTYPE_ENHMETAFILE
api_location:
- OleCtl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebf8ad8f678e9b6e463ade9f149b2e1d4bab529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105807195"
---
# <a name="pictype-constants"></a><span data-ttu-id="82766-103">Constantes PICTYPE</span><span class="sxs-lookup"><span data-stu-id="82766-103">PICTYPE Constants</span></span>

<span data-ttu-id="82766-104">Descreva o tipo de um objeto de imagem como retornado [**por IPicture:: \_ Get Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), bem como para descrever o tipo de imagem no membro **picType** da estrutura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) que é passada para [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span><span class="sxs-lookup"><span data-stu-id="82766-104">Describe the type of a picture object as returned by [**IPicture::get\_Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), as well as to describe the type of picture in the **picType** member of the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure that is passed to [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span></span>



| <span data-ttu-id="82766-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="82766-105">Constant/value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="82766-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="82766-106">Description</span></span>                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <span data-ttu-id="82766-107"><dt>**PICTYPE \_ Não INICIALIZAdo**</dt> <dt>(-1)</dt></span><span class="sxs-lookup"><span data-stu-id="82766-107"><dt>**PICTYPE\_UNINITIALIZED**</dt> <dt>(-1)</dt></span></span> </dl> | <span data-ttu-id="82766-108">O objeto de imagem não foi inicializado no momento.</span><span class="sxs-lookup"><span data-stu-id="82766-108">The picture object is currently uninitialized.</span></span> <span data-ttu-id="82766-109">Esse valor só é válido como um valor de retorno de [**IPicture:: get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) e não é válido com a estrutura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) .</span><span class="sxs-lookup"><span data-stu-id="82766-109">This value is only valid as a return value from [**IPicture::get\_Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) and is not valid with the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure.</span></span><br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <span data-ttu-id="82766-110"><dt>**PICTYPE \_ NENHUM**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="82766-110"><dt>**PICTYPE\_NONE**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="82766-111">Um novo objeto de imagem deve ser criado sem um estado inicializado.</span><span class="sxs-lookup"><span data-stu-id="82766-111">A new picture object is to be created without an initialized state.</span></span> <span data-ttu-id="82766-112">Esse valor é válido somente na estrutura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) .</span><span class="sxs-lookup"><span data-stu-id="82766-112">This value is valid only in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure.</span></span><br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <span data-ttu-id="82766-113"><dt>**PICTYPE \_ BITMAP**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="82766-113"><dt>**PICTYPE\_BITMAP**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="82766-114">O tipo de imagem é um bitmap.</span><span class="sxs-lookup"><span data-stu-id="82766-114">The picture type is a bitmap.</span></span> <span data-ttu-id="82766-115">Quando esse valor ocorre na estrutura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , isso significa que o campo **BMP** dessa estrutura contém os parâmetros de inicialização relevantes.</span><span class="sxs-lookup"><span data-stu-id="82766-115">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **bmp** field of that structure contains the relevant initialization parameters.</span></span><br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <span data-ttu-id="82766-116"><dt>**PICTYPE \_ METARQUIVO**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="82766-116"><dt>**PICTYPE\_METAFILE**</dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="82766-117">O tipo de imagem é um metarquivo.</span><span class="sxs-lookup"><span data-stu-id="82766-117">The picture type is a metafile.</span></span> <span data-ttu-id="82766-118">Quando esse valor ocorre na estrutura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , isso significa que o campo **WMF** dessa estrutura contém os parâmetros de inicialização relevantes.</span><span class="sxs-lookup"><span data-stu-id="82766-118">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **wmf** field of that structure contains the relevant initialization parameters.</span></span><br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <span data-ttu-id="82766-119"><dt>**PICTYPE \_ ÍCONE**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="82766-119"><dt>**PICTYPE\_ICON**</dt> <dt>3</dt></span></span> </dl>                               | <span data-ttu-id="82766-120">O tipo de imagem é um ícone.</span><span class="sxs-lookup"><span data-stu-id="82766-120">The picture type is an icon.</span></span> <span data-ttu-id="82766-121">Quando esse valor ocorre na estrutura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , isso significa que o campo de **ícone** dessa estrutura contém os parâmetros de inicialização relevantes.</span><span class="sxs-lookup"><span data-stu-id="82766-121">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **icon** field of that structure contains the relevant initialization parameters.</span></span><br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <span data-ttu-id="82766-122"><dt>**PICTYPE \_ ENHMETAFILE**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="82766-122"><dt>**PICTYPE\_ENHMETAFILE**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="82766-123">O tipo de imagem é um metarquivo avançado.</span><span class="sxs-lookup"><span data-stu-id="82766-123">The picture type is an enhanced metafile.</span></span> <span data-ttu-id="82766-124">Quando esse valor ocorre na estrutura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , isso significa que o campo **EMF** dessa estrutura contém os parâmetros de inicialização relevantes.</span><span class="sxs-lookup"><span data-stu-id="82766-124">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **emf** field of that structure contains the relevant initialization parameters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="82766-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82766-125">Requirements</span></span>



| <span data-ttu-id="82766-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="82766-126">Requirement</span></span> | <span data-ttu-id="82766-127">Valor</span><span class="sxs-lookup"><span data-stu-id="82766-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="82766-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82766-128">Minimum supported client</span></span><br/> | <span data-ttu-id="82766-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="82766-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="82766-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82766-130">Minimum supported server</span></span><br/> | <span data-ttu-id="82766-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="82766-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="82766-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="82766-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="82766-133"><dt>OleCtl. h</dt></span><span class="sxs-lookup"><span data-stu-id="82766-133"><dt>OleCtl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82766-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="82766-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82766-135">**IPicture:: obter \_ tipo**</span><span class="sxs-lookup"><span data-stu-id="82766-135">**IPicture::get\_Type**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[<span data-ttu-id="82766-136">**OleCreatePictureIndirect**</span><span class="sxs-lookup"><span data-stu-id="82766-136">**OleCreatePictureIndirect**</span></span>](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[<span data-ttu-id="82766-137">**PICTDESC**</span><span class="sxs-lookup"><span data-stu-id="82766-137">**PICTDESC**</span></span>](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





