---
description: Estrutura DEVICEDIALOGDATA2 – define os dados necessários para chamar uma caixa de diálogo de dispositivo.
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: Estrutura DEVICEDIALOGDATA2 (Wiadefd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA2
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: 82ca6cba81101e577eed882ad45272ab81546fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089795"
---
# <a name="devicedialogdata2-structure"></a><span data-ttu-id="ff313-103">Estrutura DEVICEDIALOGDATA2</span><span class="sxs-lookup"><span data-stu-id="ff313-103">DEVICEDIALOGDATA2 structure</span></span>

<span data-ttu-id="ff313-104">Define os dados necessários para chamar uma caixa de diálogo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ff313-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff313-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff313-105">Syntax</span></span>


```C++
typedef struct {
  DWORD     cbSize;
  IWiaItem2 *pIWiaItemRoot;
  DWORD     dwFlags;
  HWND      hwndParent;
  BSTR      bstrFolderName;
  BSTR      bstrFilename;
  LONG      lNumFiles;
  BSTR      *pbstrFilePaths;
  IWiaItem2 *ppWiaItem;
} DEVICEDIALOGDATA2;
```



## <a name="members"></a><span data-ttu-id="ff313-106">Membros</span><span class="sxs-lookup"><span data-stu-id="ff313-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ff313-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="ff313-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="ff313-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ff313-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ff313-109">Especifica o tamanho dessa estrutura em bytes.</span><span class="sxs-lookup"><span data-stu-id="ff313-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ff313-110">**pIWiaItemRoot**</span><span class="sxs-lookup"><span data-stu-id="ff313-110">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="ff313-111">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***</span><span class="sxs-lookup"><span data-stu-id="ff313-111">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="ff313-112">Aponta para uma interface [**IWiaItem2**](-wia-iwiaitem2.md) que representa o item raiz válido na árvore de itens de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ff313-112">Points to an [**IWiaItem2**](-wia-iwiaitem2.md) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="ff313-113">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="ff313-113">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="ff313-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ff313-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ff313-115">Especifica um conjunto de sinalizadores que controlam a operação da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ff313-115">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="ff313-116">Pode ser definido como qualquer um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="ff313-116">Can be set to any of the following values:</span></span>



| <span data-ttu-id="ff313-117">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="ff313-117">Flag</span></span>                                 | <span data-ttu-id="ff313-118">Significado</span><span class="sxs-lookup"><span data-stu-id="ff313-118">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff313-119">0</span><span class="sxs-lookup"><span data-stu-id="ff313-119">0</span></span>                                    | <span data-ttu-id="ff313-120">Comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="ff313-120">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="ff313-121">\_ \_ imagem única da caixa de diálogo do dispositivo WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="ff313-121">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="ff313-122">Restringir a seleção de imagem a uma única imagem na caixa de diálogo aquisição de imagem de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ff313-122">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="ff313-123">\_caixa de \_ diálogo do dispositivo WIA \_ usar \_ \_ interface do usuário comum</span><span class="sxs-lookup"><span data-stu-id="ff313-123">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="ff313-124">Use a interface do usuário do sistema, se disponível, em vez da interface do usuário fornecida pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="ff313-124">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="ff313-125">Se a interface do usuário do sistema não estiver disponível, a interface do usuário do fornecedor será usada.</span><span class="sxs-lookup"><span data-stu-id="ff313-125">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="ff313-126">Se nenhuma interface do usuário estiver disponível, a função retornará E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="ff313-126">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="ff313-127">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="ff313-127">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="ff313-128">Digite: **HWND**</span><span class="sxs-lookup"><span data-stu-id="ff313-128">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="ff313-129">Especifica o identificador para a janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ff313-129">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="ff313-130">**bstrFolderName**</span><span class="sxs-lookup"><span data-stu-id="ff313-130">**bstrFolderName**</span></span>
</dt> <dd>

<span data-ttu-id="ff313-131">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ff313-131">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="ff313-132">Especifica o nome da pasta onde os arquivos são transferidos.</span><span class="sxs-lookup"><span data-stu-id="ff313-132">Specifies the folder name where the files are transferred.</span></span>

</dd> <dt>

<span data-ttu-id="ff313-133">**bstrFilename**</span><span class="sxs-lookup"><span data-stu-id="ff313-133">**bstrFilename**</span></span>
</dt> <dd>

<span data-ttu-id="ff313-134">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ff313-134">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="ff313-135">Especifica o modelo de nome de arquivo a ser usado para arquivos transferidos de itens WIA para a pasta de destino designada por **bstrFolderName**.</span><span class="sxs-lookup"><span data-stu-id="ff313-135">Specifies the filename template to be used for files transferred from WIA items to the destination folder designated by **bstrFolderName**.</span></span> <span data-ttu-id="ff313-136">Um número arbitrário de nomes de arquivo exclusivos pode ser criado acrescentando-se caracteres adicionais ao modelo de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ff313-136">An arbitrary number of unique file names can be created by appending additional characters to the file name template.</span></span>

</dd> <dt>

<span data-ttu-id="ff313-137">**lNumFiles**</span><span class="sxs-lookup"><span data-stu-id="ff313-137">**lNumFiles**</span></span>
</dt> <dd>

<span data-ttu-id="ff313-138">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="ff313-138">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="ff313-139">Recebe o número de cadeias de caracteres gravadas na matriz **pbstrFilePaths** .</span><span class="sxs-lookup"><span data-stu-id="ff313-139">Receives the number of strings written to the **pbstrFilePaths** array.</span></span>

</dd> <dt>

<span data-ttu-id="ff313-140">**pbstrFilePaths**</span><span class="sxs-lookup"><span data-stu-id="ff313-140">**pbstrFilePaths**</span></span>
</dt> <dd>

<span data-ttu-id="ff313-141">Tipo: **BSTR \***</span><span class="sxs-lookup"><span data-stu-id="ff313-141">Type: **BSTR\***</span></span>

</dd> <dd>

<span data-ttu-id="ff313-142">Ponteiro para uma matriz de ponteiros BSTR.</span><span class="sxs-lookup"><span data-stu-id="ff313-142">Pointer to an array of BSTR pointers.</span></span> <span data-ttu-id="ff313-143">Cada elemento de matriz aponta para um BSTR que contém o nome de destino de um arquivo que foi transferido com êxito para a pasta identificada por bstrFolderName.</span><span class="sxs-lookup"><span data-stu-id="ff313-143">Each array element points to a BSTR that contains the destination name of a file that was successfully transferred to the folder identified by bstrFolderName.</span></span> <span data-ttu-id="ff313-144">O método deve alocar o armazenamento para esse membro.</span><span class="sxs-lookup"><span data-stu-id="ff313-144">The method must allocate the storage for this member.</span></span>

</dd> <dt>

<span data-ttu-id="ff313-145">**ppWiaItem**</span><span class="sxs-lookup"><span data-stu-id="ff313-145">**ppWiaItem**</span></span>
</dt> <dd>

<span data-ttu-id="ff313-146">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***</span><span class="sxs-lookup"><span data-stu-id="ff313-146">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="ff313-147">Ponteiro para a interface [**IWiaItem2**](-wia-iwiaitem2.md) do item WIA que transfere dados para o arquivo ou arquivos nomeados na matriz **pbstrFilePaths** .</span><span class="sxs-lookup"><span data-stu-id="ff313-147">Pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the WIA item that transfers data to the file or files named in the **pbstrFilePaths** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff313-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff313-148">Requirements</span></span>



| <span data-ttu-id="ff313-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff313-149">Requirement</span></span> | <span data-ttu-id="ff313-150">Valor</span><span class="sxs-lookup"><span data-stu-id="ff313-150">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ff313-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff313-151">Minimum supported client</span></span><br/> | <span data-ttu-id="ff313-152">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff313-152">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ff313-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff313-153">Minimum supported server</span></span><br/> | <span data-ttu-id="ff313-154">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff313-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ff313-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff313-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff313-156"><dt>Wiadefd. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff313-156"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




