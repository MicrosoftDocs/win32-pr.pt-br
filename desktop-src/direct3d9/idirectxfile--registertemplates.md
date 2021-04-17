---
description: Registra modelos personalizados. Preterido.
ms.assetid: f9b24800-83a5-45bf-b19f-b247c88a2c2c
title: 'Método IDirectXFile:: RegisterTemplates (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 683a495398e7fe0718ee0642c7760b0a8590538c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105754916"
---
# <a name="idirectxfileregistertemplates-method"></a><span data-ttu-id="ce472-104">Método IDirectXFile:: RegisterTemplates</span><span class="sxs-lookup"><span data-stu-id="ce472-104">IDirectXFile::RegisterTemplates method</span></span>

<span data-ttu-id="ce472-105">Registra modelos personalizados.</span><span class="sxs-lookup"><span data-stu-id="ce472-105">Registers custom templates.</span></span> <span data-ttu-id="ce472-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="ce472-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce472-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce472-107">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPVOID pvData,
  [in] DWORD  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="ce472-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce472-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce472-109">*pvData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce472-109">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce472-110">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce472-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce472-111">Ponteiro para um buffer que consiste em um arquivo do DirectX em formato de texto ou binário que contém modelos.</span><span class="sxs-lookup"><span data-stu-id="ce472-111">Pointer to a buffer consisting of a DirectX file in text or binary format that contains templates.</span></span>

</dd> <dt>

<span data-ttu-id="ce472-112">*cbSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce472-112">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce472-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce472-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce472-114">Tamanho do buffer apontado por pvData, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ce472-114">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce472-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce472-115">Return value</span></span>

<span data-ttu-id="ce472-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce472-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce472-117">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ce472-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="ce472-118">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: DXFILEERR \_ BADFILEFLOATSIZE, DXFILEERR \_ BADFILETYPE, DXFILEERR \_ BADFILEVERSION, DXFILEERR \_ BADVALUE, DXFILEERR \_ PARSEERROR.</span><span class="sxs-lookup"><span data-stu-id="ce472-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADFILEFLOATSIZE, DXFILEERR\_BADFILETYPE, DXFILEERR\_BADFILEVERSION, DXFILEERR\_BADVALUE, DXFILEERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce472-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce472-119">Remarks</span></span>

<span data-ttu-id="ce472-120">O fragmento de código a seguir fornece uma chamada de exemplo para **RegisterTemplates** e conteúdo de exemplo para o buffer para o qual pvData Aponta.</span><span class="sxs-lookup"><span data-stu-id="ce472-120">The following code fragment provides an example call to **RegisterTemplates** And example contents for the buffer to which pvData points.</span></span>


```
    TIDirectXFile * pDXFile;
    char *szTemplates = "xof 0303txt 0032\
        template SimpleData { \
            <2b934580-9e9a-11cf-ab39-0020af71e433> \
            DWORD item1;DWORD item2;DWORD item3;} \
        template ArrayData { \
            <2b934581-9e9a-11cf-ab39-0020af71e433> \
            DWORD cItems; array DWORD aItem[2][cItems]; [...] } \
        template RestrictedData { \
            <2b934582-9e9a-11cf-ab39-0020af71e433> \
            DWORD item; [SimpleData]}";
    hr = pDXFile->RegisterTemplates(szTemplates, strlen(szTemplates));
    
    
```



<span data-ttu-id="ce472-121">Todos os modelos devem especificar um nome e um UUID (identificador universal exclusivo).</span><span class="sxs-lookup"><span data-stu-id="ce472-121">All templates must specify a name and a Universally Unique Identifier (UUID).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce472-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce472-122">Requirements</span></span>



| <span data-ttu-id="ce472-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce472-123">Requirement</span></span> | <span data-ttu-id="ce472-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ce472-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce472-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce472-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ce472-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce472-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="ce472-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce472-127">Library</span></span><br/> | <dl> <span data-ttu-id="ce472-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce472-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce472-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce472-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce472-130">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="ce472-130">IDirectXFile</span></span>](idirectxfile.md)
</dt> </dl>

 

 
