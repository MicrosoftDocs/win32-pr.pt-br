---
description: Cria um objeto salvar. Preterido.
ms.assetid: 50a7dbde-1dd4-4aae-a9ab-97d6f99618c0
title: 'Método IDirectXFile:: createsaveobject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 848010a1f701b39f5cc77a126272bc019ed01f4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105749418"
---
# <a name="idirectxfilecreatesaveobject-method"></a><span data-ttu-id="4e540-104">Método IDirectXFile:: createsaveobject</span><span class="sxs-lookup"><span data-stu-id="4e540-104">IDirectXFile::CreateSaveObject method</span></span>

<span data-ttu-id="4e540-105">Cria um objeto salvar.</span><span class="sxs-lookup"><span data-stu-id="4e540-105">Creates a save object.</span></span> <span data-ttu-id="4e540-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="4e540-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e540-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e540-107">Syntax</span></span>


```C++
HRESULT CreateSaveObject(
  [in]          LPCSTR                  szFileName,
  [in]          DXFILEFORMAT            dwFileFormat,
  [out, retval] LPDIRECTXFILESAVEOBJECT *ppSaveObj
);
```



## <a name="parameters"></a><span data-ttu-id="4e540-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e540-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e540-109">*szFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4e540-109">*szFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e540-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e540-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e540-111">Ponteiro para o nome do arquivo a ser usado para salvar dados.</span><span class="sxs-lookup"><span data-stu-id="4e540-111">Pointer to the name of the file to use for saving data.</span></span>

</dd> <dt>

<span data-ttu-id="4e540-112">*dwFileFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4e540-112">*dwFileFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e540-113">Tipo: **[ **DXFILEFORMAT**](dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="4e540-113">Type: **[**DXFILEFORMAT**](dxfile.md)**</span></span>

<span data-ttu-id="4e540-114">Indica o formato a ser usado ao salvar o arquivo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="4e540-114">Indicates the format to use when saving the DirectX file.</span></span> <span data-ttu-id="4e540-115">Esse valor pode ser um dos sinalizadores DXFILEFORMAT \_ XXX em [constantes DXFILE](dxfile.md).</span><span class="sxs-lookup"><span data-stu-id="4e540-115">This value can be one of the DXFILEFORMAT\_xxx flags in [DXFILE Constants](dxfile.md).</span></span> <span data-ttu-id="4e540-116">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="4e540-116">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4e540-117">*ppSaveObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4e540-117">*ppSaveObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4e540-118">Tipo: **[ **LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e540-118">Type: **[**LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***</span></span>

<span data-ttu-id="4e540-119">Endereço de um ponteiro para uma interface [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) , que representa o objeto salvar criado.</span><span class="sxs-lookup"><span data-stu-id="4e540-119">Address of a pointer to an [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interface, representing the created save object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e540-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e540-120">Return value</span></span>

<span data-ttu-id="4e540-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4e540-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4e540-122">Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e540-122">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="4e540-123">Se o método falhar, o valor de retorno poderá ser um dos seguintes: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILE, DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="4e540-123">If the method fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADFILE, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e540-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e540-124">Remarks</span></span>

<span data-ttu-id="4e540-125">Depois de usar esse método, use métodos da interface [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) para criar objetos de dados e para salvar modelos ou dados.</span><span class="sxs-lookup"><span data-stu-id="4e540-125">After using this method, use methods of the [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interface to create data objects and to save templates or data.</span></span>

<span data-ttu-id="4e540-126">O valor padrão para o formato de arquivo é DXFILEFORMAT \_ binário.</span><span class="sxs-lookup"><span data-stu-id="4e540-126">The default value for the file format is DXFILEFORMAT\_BINARY.</span></span> <span data-ttu-id="4e540-127">Os valores de formato de arquivo podem ser combinados em uma lógica ou para criar texto compactado ou arquivos binários compactados.</span><span class="sxs-lookup"><span data-stu-id="4e540-127">The file format values can be combined in a logical OR to create compressed text or compressed binary files.</span></span> <span data-ttu-id="4e540-128">Se um arquivo for especificado como binário (0) e texto (1), ele será salvo como um arquivo de texto porque o valor será indistinguíveis do valor de formato de arquivo de texto (0 + 1 = 1).</span><span class="sxs-lookup"><span data-stu-id="4e540-128">If a file is specified as both binary (0) and text (1), it will be saved as a text file because the value will be indistinguishable from the text file format value (0 + 1 = 1).</span></span> <span data-ttu-id="4e540-129">Se você indicar que o formato de arquivo deve ser texto e compactado, o arquivo será gravado primeiro como texto e, em seguida, compactado.</span><span class="sxs-lookup"><span data-stu-id="4e540-129">If you indicate that the file format should be text and compressed, the file will first be written out as text and then compressed.</span></span> <span data-ttu-id="4e540-130">No entanto, arquivos de texto compactados não são tão eficientes quanto arquivos de texto binários, portanto, na maioria dos casos, você desejará indicar binário e compactado.</span><span class="sxs-lookup"><span data-stu-id="4e540-130">However, compressed text files are not as efficient as binary text files, so in most cases you will want to indicate binary and compressed.</span></span> <span data-ttu-id="4e540-131">Definir um arquivo a ser compactado sem especificar um formato resultará em um arquivo binário e compactado.</span><span class="sxs-lookup"><span data-stu-id="4e540-131">Setting a file to be compressed without specifying a format will result in a binary, compressed file.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e540-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e540-132">Requirements</span></span>



| <span data-ttu-id="4e540-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e540-133">Requirement</span></span> | <span data-ttu-id="4e540-134">Valor</span><span class="sxs-lookup"><span data-stu-id="4e540-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e540-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e540-135">Header</span></span><br/>  | <dl> <span data-ttu-id="4e540-136"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e540-136"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e540-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e540-137">Library</span></span><br/> | <dl> <span data-ttu-id="4e540-138"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e540-138"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e540-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e540-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e540-140">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="4e540-140">IDirectXFile</span></span>](idirectxfile.md)
</dt> <dt>

[<span data-ttu-id="4e540-141">**IDirectXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="4e540-141">**IDirectXFileSaveObject**</span></span>](idirectxfilesaveobject.md)
</dt> </dl>

 

 
