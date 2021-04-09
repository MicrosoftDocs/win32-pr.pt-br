---
description: Exibe uma caixa de diálogo para o usuário se preparar para a aquisição de imagem.
ms.assetid: 2d7246ec-fb90-4538-b717-b9e3813c1696
title: 'IWiaItem2: método eviceDlg de:D (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3337e74a621b6431b5bbfa429692717def447c82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090511"
---
# <a name="iwiaitem2devicedlg-method"></a><span data-ttu-id="f77c7-103">IWiaItem2: método eviceDlg de:D</span><span class="sxs-lookup"><span data-stu-id="f77c7-103">IWiaItem2::DeviceDlg method</span></span>

<span data-ttu-id="f77c7-104">Exibe uma caixa de diálogo para o usuário se preparar para a aquisição de imagem.</span><span class="sxs-lookup"><span data-stu-id="f77c7-104">Displays a dialog box to the user to prepare for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="f77c7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f77c7-105">Syntax</span></span>


```C++
HRESULT DeviceDlg(
  [in]      LONG      lFlags,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in, out] BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="f77c7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f77c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f77c7-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f77c7-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f77c7-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="f77c7-108">Type: **LONG**</span></span>

<span data-ttu-id="f77c7-109">Especifica um conjunto de sinalizadores que controlam a operação da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f77c7-109">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="f77c7-110">O valor pode ser 0 para representar o comportamento padrão ou qualquer um dos sinalizadores de \_ caixa de diálogo do dispositivo WIA \_ descritos em [**WiaFlag**](-wia-wiaflag.md).</span><span class="sxs-lookup"><span data-stu-id="f77c7-110">The value can be either 0 to represent the default behavior or any of the WIA\_DEVICE\_DIALOG flags described in [**WiaFlag**](-wia-wiaflag.md).</span></span>

</dd> <dt>

<span data-ttu-id="f77c7-111">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f77c7-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f77c7-112">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="f77c7-112">Type: **HWND**</span></span>

<span data-ttu-id="f77c7-113">Um identificador para a janela pai.</span><span class="sxs-lookup"><span data-stu-id="f77c7-113">A handle to the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="f77c7-114">*bstrFolderName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f77c7-114">*bstrFolderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f77c7-115">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f77c7-115">Type: **BSTR**</span></span>

<span data-ttu-id="f77c7-116">Especifica o nome da pasta onde os arquivos devem ser transferidos.</span><span class="sxs-lookup"><span data-stu-id="f77c7-116">Specifies the folder name where the files are to be transferred.</span></span>

</dd> <dt>

<span data-ttu-id="f77c7-117">*bstrFilename* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f77c7-117">*bstrFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f77c7-118">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f77c7-118">Type: **BSTR**</span></span>

<span data-ttu-id="f77c7-119">Especifica o nome do arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="f77c7-119">Specifies the template file name.</span></span>

</dd> <dt>

<span data-ttu-id="f77c7-120">*plNumFiles* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f77c7-120">*plNumFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f77c7-121">Tipo: \**Long \** _</span><span class="sxs-lookup"><span data-stu-id="f77c7-121">Type: \**LONG\** _</span></span>

<span data-ttu-id="f77c7-122">Um ponteiro para o número de itens na matriz _ppbstrFilePaths \*.</span><span class="sxs-lookup"><span data-stu-id="f77c7-122">A pointer to the number of items in the _ppbstrFilePaths\* array.</span></span>

</dd> <dt>

<span data-ttu-id="f77c7-123">*ppbstrFilePaths* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f77c7-123">*ppbstrFilePaths* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f77c7-124">Tipo: **BSTR \* \***</span><span class="sxs-lookup"><span data-stu-id="f77c7-124">Type: **BSTR\*\***</span></span>

<span data-ttu-id="f77c7-125">O endereço de um ponteiro para uma matriz de caminhos para os arquivos digitalizados.</span><span class="sxs-lookup"><span data-stu-id="f77c7-125">The address of a pointer to an array of paths for the scanned files.</span></span> <span data-ttu-id="f77c7-126">Inicialize o ponteiro para apontar para uma matriz de tamanho zero (0) antes de **IWiaItem2::D evicedlg** é chamado.</span><span class="sxs-lookup"><span data-stu-id="f77c7-126">Initialize the pointer to point to an array of size zero (0) before **IWiaItem2::DeviceDlg** is called.</span></span>

</dd> <dt>

<span data-ttu-id="f77c7-127">*ppIWiaItem2* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f77c7-127">*ppIWiaItem2* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f77c7-128">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f77c7-128">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="f77c7-129">O endereço de uma matriz de ponteiros para interfaces [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="f77c7-129">The address of an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f77c7-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f77c7-130">Return value</span></span>

<span data-ttu-id="f77c7-131">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f77c7-131">Type: **HRESULT**</span></span>

<span data-ttu-id="f77c7-132">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f77c7-132">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f77c7-133">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f77c7-133">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f77c7-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="f77c7-134">Remarks</span></span>

<span data-ttu-id="f77c7-135">Esse método exibe uma caixa de diálogo para o usuário que um aplicativo usa para reunir todas as informações necessárias para a aquisição de imagem.</span><span class="sxs-lookup"><span data-stu-id="f77c7-135">This method displays a dialog box to the user that an application uses to gather all the information required for image acquisition.</span></span> <span data-ttu-id="f77c7-136">Ele também é usado para especificar propriedades de verificação de imagem, como brilho e contraste.</span><span class="sxs-lookup"><span data-stu-id="f77c7-136">It is also used to specify image scan properties such as brightness and contrast.</span></span>

<span data-ttu-id="f77c7-137">Depois que esse método retornar, o aplicativo poderá usar a interface [**IWiaTransfer**](-wia-iwiatransfer.md) para adquirir a imagem.</span><span class="sxs-lookup"><span data-stu-id="f77c7-137">After this method returns, the application can use the [**IWiaTransfer**](-wia-iwiatransfer.md) interface to acquire the image.</span></span>

<span data-ttu-id="f77c7-138">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para cada elemento na matriz de ponteiros de interface recebidos por meio do parâmetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="f77c7-138">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method for each element in the array of interface pointers they receive through the *ppIWiaItem2* parameter.</span></span> <span data-ttu-id="f77c7-139">Os aplicativos também devem liberar a matriz usando [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="f77c7-139">Applications must also free the array using [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="f77c7-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f77c7-140">Requirements</span></span>



| <span data-ttu-id="f77c7-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="f77c7-141">Requirement</span></span> | <span data-ttu-id="f77c7-142">Valor</span><span class="sxs-lookup"><span data-stu-id="f77c7-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f77c7-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f77c7-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f77c7-144">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f77c7-144">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f77c7-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f77c7-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f77c7-146">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f77c7-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f77c7-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f77c7-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="f77c7-148"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="f77c7-148"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="f77c7-149">INSERI</span><span class="sxs-lookup"><span data-stu-id="f77c7-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f77c7-150"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f77c7-150"><dt>Wia.idl</dt></span></span> </dl> |



 

 
