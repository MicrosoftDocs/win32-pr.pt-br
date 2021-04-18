---
title: Enumeração de WMDM_TAG_DATATYPE
description: O \_ tipo de enumeração de DataType da marca WMDM \_ define um tipo de dados.
ms.assetid: 9c300814-5610-4e46-b441-e7f2fc78a47b
keywords:
- WMDM_TAG_DATATYPE de enumeração do Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_TAG_DATATYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad04f0d220809f6bd13d8ae29cc36d52ff6e599
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796453"
---
# <a name="wmdm_tag_datatype-enumeration"></a><span data-ttu-id="1a527-104">\_Enumeração de tipo de dados de marca WMDM \_</span><span class="sxs-lookup"><span data-stu-id="1a527-104">WMDM\_TAG\_DATATYPE enumeration</span></span>

<span data-ttu-id="1a527-105">O tipo de enumeração de **\_ \_ DataType da marca WMDM** define um tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1a527-105">The **WMDM\_TAG\_DATATYPE** enumeration type defines a data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a527-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a527-106">Syntax</span></span>


```C++
typedef enum tagWMDM_TAG_DATATYPE { 
  WMDM_TYPE_DWORD,
  WMDM_TYPE_STRING,
  WMDM_TYPE_BINARY,
  WMDM_TYPE_BOOL,
  WMDM_TYPE_QWORD,
  WMDM_TYPE_WORD,
  WMDM_TYPE_GUID,
  WMDM_TYPE_DATE
} WMDM_TAG_DATATYPE;
```



## <a name="constants"></a><span data-ttu-id="1a527-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="1a527-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1a527-108"><span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**tipo de WMDM \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1a527-108"><span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**WMDM\_TYPE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="1a527-109">Especifica um valor **DWORD** de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="1a527-109">Specifies a 4-byte **DWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="1a527-110"><span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**Cadeia de caracteres do \_ tipo WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="1a527-110"><span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**WMDM\_TYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="1a527-111">Especifica uma cadeia de caracteres Unicode terminada em nulo (2 bytes por caractere).</span><span class="sxs-lookup"><span data-stu-id="1a527-111">Specifies a null-terminated Unicode string (2 bytes per character).</span></span>

</dd> <dt>

<span data-ttu-id="1a527-112"><span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**\_tipo de \_ binário do WMDM**</span><span class="sxs-lookup"><span data-stu-id="1a527-112"><span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**WMDM\_TYPE\_BINARY**</span></span>
</dt> <dd>

<span data-ttu-id="1a527-113">Especifica uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="1a527-113">Specifies an array of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1a527-114"><span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**tipo de WMDM \_ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="1a527-114"><span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**WMDM\_TYPE\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="1a527-115">Especifica um valor booliano de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="1a527-115">Specifies a 4-byte Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="1a527-116"><span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**WMDM \_ tipo \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="1a527-116"><span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**WMDM\_TYPE\_QWORD**</span></span>
</dt> <dd>

<span data-ttu-id="1a527-117">Especifica um valor **QWORD** de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="1a527-117">Specifies an 8-byte **QWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="1a527-118"><span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**tipo de WMDM \_ \_ Word**</span><span class="sxs-lookup"><span data-stu-id="1a527-118"><span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM\_TYPE\_WORD**</span></span>
</dt> <dd>

<span data-ttu-id="1a527-119">Especifica um valor de **palavra** de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="1a527-119">Specifies a 2-byte **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="1a527-120"><span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**\_GUID do tipo WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="1a527-120"><span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**WMDM\_TYPE\_GUID**</span></span>
</dt> <dd>

<span data-ttu-id="1a527-121">Especifica um GUID de 128 bits (16 bytes).</span><span class="sxs-lookup"><span data-stu-id="1a527-121">Specifies a 128-bit (16-byte) GUID.</span></span>

</dd> <dt>

<span data-ttu-id="1a527-122"><span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**\_data do tipo WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="1a527-122"><span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**WMDM\_TYPE\_DATE**</span></span>
</dt> <dd>

<span data-ttu-id="1a527-123">Especifica uma data.</span><span class="sxs-lookup"><span data-stu-id="1a527-123">Specifies a date.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1a527-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a527-124">Requirements</span></span>



| <span data-ttu-id="1a527-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a527-125">Requirement</span></span> | <span data-ttu-id="1a527-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1a527-126">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1a527-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a527-127">Header</span></span><br/> | <dl> <span data-ttu-id="1a527-128"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1a527-128"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a527-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a527-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a527-130">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="1a527-130">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





