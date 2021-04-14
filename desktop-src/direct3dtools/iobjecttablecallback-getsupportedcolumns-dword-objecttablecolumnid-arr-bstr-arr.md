---
description: Obtém informações sobre quais colunas (tipos de dados de objeto) têm suporte na tabela de objetos.
MS-HAID: vspixengine.IObjectTableCallback\_GetSupportedColumns\_DWORD\_ObjectTableColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IObjectTableCallback:: GetSupportedColumns'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 148AB80D-9833-4B57-9F34-CEDFFF8E905A
api_name:
- IObjectTableCallback.GetSupportedColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ed077e0921043245e4ff3dda4b1c33dd4e3f20d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456513"
---
# <a name="span-idvspixengineiobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arrspaniobjecttablecallbackgetsupportedcolumns-method"></a><span data-ttu-id="a9f52-103"><span id="vspixengine.iobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arr"></span>Método IObjectTableCallback:: GetSupportedColumns</span><span class="sxs-lookup"><span data-stu-id="a9f52-103"><span id="vspixengine.iobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arr"></span>IObjectTableCallback::GetSupportedColumns method</span></span>

<span data-ttu-id="a9f52-104">Obtém informações sobre quais colunas (tipos de dados de objeto) têm suporte na tabela de objetos.</span><span class="sxs-lookup"><span data-stu-id="a9f52-104">Gets information about which columns (types of object data) are supported by the object table.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9f52-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9f52-105">Syntax</span></span>


```C++
HRESULT GetSupportedColumns(
   DWORD                  numColumns,
   ObjectTableColumnID [] count0_pIDs,
   BSTR []                count0_pBstrNames
);
```

## <a name="parameters"></a><span data-ttu-id="a9f52-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9f52-106">Parameters</span></span>

<span data-ttu-id="a9f52-107">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="a9f52-107">*numColumns* </span></span>  
<span data-ttu-id="a9f52-108">O número de colunas com suporte na tabela de objetos.</span><span class="sxs-lookup"><span data-stu-id="a9f52-108">The number of columns supported by the object table.</span></span>

<span data-ttu-id="a9f52-109">*count0_pIDs* </span><span class="sxs-lookup"><span data-stu-id="a9f52-109">*count0_pIDs* </span></span>  
<span data-ttu-id="a9f52-110">As IDs de cada coluna com suporte na tabela de objetos.</span><span class="sxs-lookup"><span data-stu-id="a9f52-110">The IDs of each column supported by the object table.</span></span>

<span data-ttu-id="a9f52-111">*count0_pBstrNames* </span><span class="sxs-lookup"><span data-stu-id="a9f52-111">*count0_pBstrNames* </span></span>  
<span data-ttu-id="a9f52-112">Os nomes de cada coluna, como uma cadeia de caracteres COM, com suporte da tabela de objetos.</span><span class="sxs-lookup"><span data-stu-id="a9f52-112">The names of each column, as a COM string, supported by the object table.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9f52-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9f52-113">Return value</span></span>

<span data-ttu-id="a9f52-114">Se esse método tiver sucesso, ele retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="a9f52-114">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="a9f52-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a9f52-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9f52-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9f52-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a9f52-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9f52-117">Header</span></span></p></td><td><span data-ttu-id="a9f52-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a9f52-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a9f52-119"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="a9f52-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a9f52-120">**IObjectTableCallback**</span><span class="sxs-lookup"><span data-stu-id="a9f52-120">**IObjectTableCallback**</span></span>](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
