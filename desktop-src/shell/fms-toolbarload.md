---
description: Contém informações sobre os botões personalizados a serem adicionados à barra de ferramentas do Gerenciador de arquivos. Os botões são fornecidos por uma DLL de extensão do Gerenciador de arquivos.
title: Estrutura de FMS_TOOLBARLOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 7185f9e5-10c6-43cc-b85b-cd077378338f
ms.openlocfilehash: 8e123c759a827adddf5fd00eaf33193ebca0dbf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967936"
---
# <a name="fms_toolbarload-structure"></a><span data-ttu-id="e07e4-104">\_Estrutura TOOLBARLOAD do FMS</span><span class="sxs-lookup"><span data-stu-id="e07e4-104">FMS\_TOOLBARLOAD structure</span></span>

<span data-ttu-id="e07e4-105">Contém informações sobre os botões personalizados a serem adicionados à barra de ferramentas do Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e07e4-105">Contains information about custom buttons to be added to the File Manager toolbar.</span></span> <span data-ttu-id="e07e4-106">Os botões são fornecidos por uma DLL de extensão do Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e07e4-106">The buttons are provided by a File Manager extension DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="e07e4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e07e4-107">Syntax</span></span>


```C++
typedef struct _FMS_TOOLBARLOAD {
  DWORD        dwSize;
  LPEXT_BUTTON lpButtons;
  WORD         cButtons;
  WORD         cBitmaps;
  WORD         idBitmap;
  HBITMAP      hBitmap;
} FMS_TOOLBARLOAD;
```



## <a name="members"></a><span data-ttu-id="e07e4-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e07e4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e07e4-109">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="e07e4-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="e07e4-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e07e4-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e07e4-111">O tamanho, em bytes, da estrutura.</span><span class="sxs-lookup"><span data-stu-id="e07e4-111">The size, in bytes, of the structure.</span></span> <span data-ttu-id="e07e4-112">O Gerenciador de arquivos define o tamanho antes de chamar a extensão e verifica o tamanho após o retorno do procedimento de extensão.</span><span class="sxs-lookup"><span data-stu-id="e07e4-112">File Manager sets the size before calling the extension and checks the size after the extension procedure returns.</span></span>

</dd> <dt>

<span data-ttu-id="e07e4-113">**lpButtons**</span><span class="sxs-lookup"><span data-stu-id="e07e4-113">**lpButtons**</span></span>
</dt> <dd>

<span data-ttu-id="e07e4-114">Tipo: **\_ botão LPEXT**</span><span class="sxs-lookup"><span data-stu-id="e07e4-114">Type: **LPEXT\_BUTTON**</span></span>

</dd> <dd>

<span data-ttu-id="e07e4-115">O endereço de uma matriz de estruturas de [**\_ botão de ext**](ext-button.md) .</span><span class="sxs-lookup"><span data-stu-id="e07e4-115">The address of an array of [**EXT\_BUTTON**](ext-button.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="e07e4-116">**cButtons**</span><span class="sxs-lookup"><span data-stu-id="e07e4-116">**cButtons**</span></span>
</dt> <dd>

<span data-ttu-id="e07e4-117">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e07e4-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e07e4-118">O número de estruturas de [**\_ botão de ext**](ext-button.md) na matriz apontadas pelo membro **lpButtons** .</span><span class="sxs-lookup"><span data-stu-id="e07e4-118">The number of [**EXT\_BUTTON**](ext-button.md) structures in the array pointed to by the **lpButtons** member.</span></span> <span data-ttu-id="e07e4-119">Esse número é igual ao número de botões e separadores a serem adicionados à barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="e07e4-119">This number equals the number of buttons and separators to add to the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="e07e4-120">**cBitmaps**</span><span class="sxs-lookup"><span data-stu-id="e07e4-120">**cBitmaps**</span></span>
</dt> <dd>

<span data-ttu-id="e07e4-121">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e07e4-121">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e07e4-122">O número de botões representados pelo bitmap fornecido.</span><span class="sxs-lookup"><span data-stu-id="e07e4-122">The number of buttons represented by the given bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="e07e4-123">**idBitmap**</span><span class="sxs-lookup"><span data-stu-id="e07e4-123">**idBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="e07e4-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e07e4-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e07e4-125">O identificador de um recurso de bitmap no arquivo executável para a extensão DLL.</span><span class="sxs-lookup"><span data-stu-id="e07e4-125">The identifier of a bitmap resource in the executable file for the extension DLL.</span></span> <span data-ttu-id="e07e4-126">O recurso de bitmap contém imagens para o número de botões especificados por **cBitmaps**.</span><span class="sxs-lookup"><span data-stu-id="e07e4-126">The bitmap resource contains images for the number of buttons specified by **cBitmaps**.</span></span> <span data-ttu-id="e07e4-127">O Gerenciador de arquivos carrega o recurso de bitmap e, em seguida, o usa para exibir os botões.</span><span class="sxs-lookup"><span data-stu-id="e07e4-127">File Manager loads the bitmap resource and then uses it to display the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="e07e4-128">**hBitmap**</span><span class="sxs-lookup"><span data-stu-id="e07e4-128">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="e07e4-129">Tipo: **HBITMAP**</span><span class="sxs-lookup"><span data-stu-id="e07e4-129">Type: **HBITMAP**</span></span>

</dd> <dd>

<span data-ttu-id="e07e4-130">Um identificador para um bitmap que o Gerenciador de arquivos usará para obter e exibir imagens de botão se **idBitmap** for 0.</span><span class="sxs-lookup"><span data-stu-id="e07e4-130">A handle to a bitmap that File Manager will use to obtain and display button images if **idBitmap** is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e07e4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e07e4-131">Requirements</span></span>



| <span data-ttu-id="e07e4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e07e4-132">Requirement</span></span> | <span data-ttu-id="e07e4-133">Valor</span><span class="sxs-lookup"><span data-stu-id="e07e4-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e07e4-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e07e4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e07e4-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e07e4-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e07e4-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e07e4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e07e4-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e07e4-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e07e4-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e07e4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e07e4-139"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="e07e4-139"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e07e4-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="e07e4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07e4-141">**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="e07e4-141">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> </dl>

 

 




