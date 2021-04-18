---
description: Cria um objeto salvar que será usado para salvar dados em um arquivo. x.
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: 'Método ID3DXFile:: createsaveobject (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d7c5b3de020ad50abfd8834aabbdc8e6e848d71d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771394"
---
# <a name="id3dxfilecreatesaveobject-method"></a><span data-ttu-id="db8f7-103">Método ID3DXFile:: createsaveobject</span><span class="sxs-lookup"><span data-stu-id="db8f7-103">ID3DXFile::CreateSaveObject method</span></span>

<span data-ttu-id="db8f7-104">Cria um objeto salvar que será usado para salvar dados em um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="db8f7-104">Creates a save object that will be used to save data to a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="db8f7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db8f7-105">Syntax</span></span>


```C++
HRESULT CreateSaveObject(
  [in]  LPCVOID               pData,
  [in]  D3DXF_FILESAVEOPTIONS flags,
  [in]  D3DXF_FILEFORMAT      dwFileFormat,
  [out] ID3DXFileSaveObject   **ppSaveObj
);
```



## <a name="parameters"></a><span data-ttu-id="db8f7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db8f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db8f7-107">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db8f7-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db8f7-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db8f7-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db8f7-109">Ponteiro para o nome do arquivo a ser usado para salvar dados.</span><span class="sxs-lookup"><span data-stu-id="db8f7-109">Pointer to the name of the file to use for saving data.</span></span>

</dd> <dt>

<span data-ttu-id="db8f7-110">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="db8f7-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db8f7-111">Tipo: **[D3DXF \_ filesaveoptions](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="db8f7-111">Type: **[D3DXF\_FILESAVEOPTIONS](d3dxf.md)**</span></span>

<span data-ttu-id="db8f7-112">Valor que especifica o nome do arquivo no qual os dados serão salvos.</span><span class="sxs-lookup"><span data-stu-id="db8f7-112">Value that specifies the name of the file to which data is to be saved.</span></span> <span data-ttu-id="db8f7-113">Esse valor pode ser um dos sinalizadores de [Opções de salvamento de arquivo](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="db8f7-113">This value can be one of the [File Save Options](d3dxf.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="db8f7-114">*dwFileFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db8f7-114">*dwFileFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db8f7-115">Tipo: **[D3DXF \_ FileFormat](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="db8f7-115">Type: **[D3DXF\_FILEFORMAT](d3dxf.md)**</span></span>

<span data-ttu-id="db8f7-116">Indica o formato a ser usado ao salvar o arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="db8f7-116">Indicates the format to use when saving the .x file.</span></span> <span data-ttu-id="db8f7-117">Esse valor pode ser um dos sinalizadores de [formatos de arquivo](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="db8f7-117">This value can be one of the [File Formats](d3dxf.md) flags.</span></span> <span data-ttu-id="db8f7-118">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="db8f7-118">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="db8f7-119">*ppSaveObj* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="db8f7-119">*ppSaveObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db8f7-120">Tipo: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="db8f7-120">Type: **[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span></span>

<span data-ttu-id="db8f7-121">Endereço de um ponteiro para uma interface [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) , que representa o objeto salvar criado.</span><span class="sxs-lookup"><span data-stu-id="db8f7-121">Address of a pointer to an [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface, representing the created save object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db8f7-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db8f7-122">Return value</span></span>

<span data-ttu-id="db8f7-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db8f7-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db8f7-124">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="db8f7-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="db8f7-125">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.</span><span class="sxs-lookup"><span data-stu-id="db8f7-125">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="db8f7-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="db8f7-126">Remarks</span></span>

<span data-ttu-id="db8f7-127">Depois de usar esse método, use métodos da interface [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) para criar objetos de dados e para salvar modelos ou dados.</span><span class="sxs-lookup"><span data-stu-id="db8f7-127">After using this method, use methods of the [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface to create data objects and to save templates or data.</span></span>

<span data-ttu-id="db8f7-128">Para o formato de arquivo salvo *dwFileFormat*, um dos sinalizadores binário, binário herdado ou de texto nos [formatos de arquivo](d3dxf.md) deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="db8f7-128">For the saved file format *dwFileFormat*, one of the binary, legacy binary, or text flags in [File Formats](d3dxf.md) must be specified.</span></span> <span data-ttu-id="db8f7-129">O arquivo pode ser compactado usando o \_ sinalizador compactado FileFormat opcional D3DXF \_ .</span><span class="sxs-lookup"><span data-stu-id="db8f7-129">The file can be compressed by using the optional D3DXF\_FILEFORMAT\_COMPRESSED flag.</span></span>

<span data-ttu-id="db8f7-130">Os valores de formato de arquivo podem ser combinados em uma lógica ou para criar texto compactado ou arquivos binários compactados.</span><span class="sxs-lookup"><span data-stu-id="db8f7-130">The file format values can be combined in a logical OR to create compressed text or compressed binary files.</span></span> <span data-ttu-id="db8f7-131">Se você indicar que o formato do arquivo deve ser texto e compactado, o arquivo será gravado primeiro como texto e, em seguida, compactado.</span><span class="sxs-lookup"><span data-stu-id="db8f7-131">If you indicate that the file format should be text and compressed, the file will be written out first as text and then compressed.</span></span> <span data-ttu-id="db8f7-132">No entanto, arquivos de texto compactados não são tão eficientes quanto arquivos de texto binários; na maioria dos casos, portanto, você desejará indicar binário e compactado.</span><span class="sxs-lookup"><span data-stu-id="db8f7-132">However, compressed text files are not as efficient as binary text files; in most cases, therefore, you will want to indicate binary and compressed.</span></span>

## <a name="requirements"></a><span data-ttu-id="db8f7-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db8f7-133">Requirements</span></span>



| <span data-ttu-id="db8f7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="db8f7-134">Requirement</span></span> | <span data-ttu-id="db8f7-135">Valor</span><span class="sxs-lookup"><span data-stu-id="db8f7-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db8f7-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db8f7-136">Header</span></span><br/>  | <dl> <span data-ttu-id="db8f7-137"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="db8f7-137"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="db8f7-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db8f7-138">Library</span></span><br/> | <dl> <span data-ttu-id="db8f7-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db8f7-139"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="db8f7-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="db8f7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db8f7-141">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="db8f7-141">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="db8f7-142">**ID3DXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="db8f7-142">**ID3DXFileSaveObject**</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 
