---
description: 'O método IWiaDevMgr2:: GetImageDlg exibe uma ou mais caixas de diálogo que permitem que um usuário adquira uma imagem de um dispositivo WIA (Windows Image Acquisition) 2,0 e grave a imagem em um arquivo especificado.'
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: 'Método IWiaDevMgr2:: GetImageDlg (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.GetImageDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6777b839beeb809383e524960e8882392be4bd24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790396"
---
# <a name="iwiadevmgr2getimagedlg-method"></a><span data-ttu-id="4a81a-103">Método IWiaDevMgr2:: GetImageDlg</span><span class="sxs-lookup"><span data-stu-id="4a81a-103">IWiaDevMgr2::GetImageDlg method</span></span>

<span data-ttu-id="4a81a-104">O método **IWiaDevMgr2:: GetImageDlg** exibe uma ou mais caixas de diálogo que permitem que um usuário adquira uma imagem de um dispositivo WIA (Windows Image Acquisition) 2,0 e grave a imagem em um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="4a81a-104">The **IWiaDevMgr2::GetImageDlg** method displays one or more dialog boxes that enable a user to acquire an image from a Windows Image Acquisition (WIA) 2.0 device and write the image to a specified file.</span></span> <span data-ttu-id="4a81a-105">Esse método estende a funcionalidade de [**IWiaDevMgr2:: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) para encapsular a aquisição de imagem em uma única chamada à API.</span><span class="sxs-lookup"><span data-stu-id="4a81a-105">This method extends the functionality of [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) to encapsulate image acquisition within a single API call.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a81a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a81a-106">Syntax</span></span>


```C++
HRESULT GetImageDlg(
  [in]      LONG      lFlags,
  [in]      BSTR      bstrDeviceID,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in]      BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppItem
);
```



## <a name="parameters"></a><span data-ttu-id="4a81a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a81a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a81a-108">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4a81a-108">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a81a-109">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="4a81a-109">Type: **LONG**</span></span>

<span data-ttu-id="4a81a-110">Especifica o comportamento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4a81a-110">Specifies dialog box behavior.</span></span> <span data-ttu-id="4a81a-111">Pode ser definido com os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="4a81a-111">Can be set to the following values:</span></span>



| <span data-ttu-id="4a81a-112">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="4a81a-112">Flag</span></span>                                 | <span data-ttu-id="4a81a-113">Significado</span><span class="sxs-lookup"><span data-stu-id="4a81a-113">Meaning</span></span>                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a81a-114">0</span><span class="sxs-lookup"><span data-stu-id="4a81a-114">0</span></span>                                    | <span data-ttu-id="4a81a-115">Comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="4a81a-115">Default behavior.</span></span>                                                                                                                                                           |
| <span data-ttu-id="4a81a-116">\_caixa de \_ diálogo do dispositivo WIA \_ usar \_ \_ interface do usuário comum</span><span class="sxs-lookup"><span data-stu-id="4a81a-116">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="4a81a-117">Use a interface do usuário do sistema em vez da interface do usuário fornecida pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="4a81a-117">Use the system UI instead of the vendor-supplied UI.</span></span> <span data-ttu-id="4a81a-118">Se a interface do usuário do sistema não estiver disponível, a interface do usuário do fornecedor será usada.</span><span class="sxs-lookup"><span data-stu-id="4a81a-118">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="4a81a-119">Se nenhuma interface do usuário estiver disponível, a função retornará E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="4a81a-119">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="4a81a-120">*bstrDeviceID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4a81a-120">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a81a-121">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4a81a-121">Type: **BSTR**</span></span>

<span data-ttu-id="4a81a-122">Especifica o scanner a ser usado.</span><span class="sxs-lookup"><span data-stu-id="4a81a-122">Specifies the scanner to use.</span></span>

</dd> <dt>

<span data-ttu-id="4a81a-123">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4a81a-123">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a81a-124">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="4a81a-124">Type: **HWND**</span></span>

<span data-ttu-id="4a81a-125">Um identificador da janela que é proprietária da caixa de diálogo **obter imagem** .</span><span class="sxs-lookup"><span data-stu-id="4a81a-125">A handle of the window that owns the **Get Image** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="4a81a-126">*bstrFolderName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4a81a-126">*bstrFolderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a81a-127">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4a81a-127">Type: **BSTR**</span></span>

<span data-ttu-id="4a81a-128">Especifica o nome da pasta que Ito armazena os arquivos digitalizados.</span><span class="sxs-lookup"><span data-stu-id="4a81a-128">Specifies the name of the folder ito store the scanned files in.</span></span>

</dd> <dt>

<span data-ttu-id="4a81a-129">*bstrFilename* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4a81a-129">*bstrFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a81a-130">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4a81a-130">Type: **BSTR**</span></span>

<span data-ttu-id="4a81a-131">Especifica o nome do arquivo no qual gravar os dados da imagem.</span><span class="sxs-lookup"><span data-stu-id="4a81a-131">Specifies the name of the file to write the image data to.</span></span>

</dd> <dt>

<span data-ttu-id="4a81a-132">*plNumFiles* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4a81a-132">*plNumFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a81a-133">Tipo: \**Long \** _</span><span class="sxs-lookup"><span data-stu-id="4a81a-133">Type: \**LONG\** _</span></span>

<span data-ttu-id="4a81a-134">Um ponteiro para o número de arquivos a serem verificados.</span><span class="sxs-lookup"><span data-stu-id="4a81a-134">A pointer to the number of files to scan.</span></span>

</dd> <dt>

<span data-ttu-id="4a81a-135">_ppbstrFilePaths \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a81a-135">_ppbstrFilePaths\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a81a-136">Tipo: **BSTR \* \***</span><span class="sxs-lookup"><span data-stu-id="4a81a-136">Type: **BSTR\*\***</span></span>

<span data-ttu-id="4a81a-137">O endereço de um ponteiro para uma matriz de caminhos para os arquivos digitalizados.</span><span class="sxs-lookup"><span data-stu-id="4a81a-137">The address of a pointer to an array of paths for the scanned files.</span></span> <span data-ttu-id="4a81a-138">Inicialize o ponteiro para apontar para uma matriz de tamanho zero (0) antes de **IWiaDevMgr2:: GetImageDlg** ser chamado.</span><span class="sxs-lookup"><span data-stu-id="4a81a-138">Initialize the pointer to point to an array of size zero (0) before **IWiaDevMgr2::GetImageDlg** is called.</span></span> <span data-ttu-id="4a81a-139">Consulte **comentários**.</span><span class="sxs-lookup"><span data-stu-id="4a81a-139">See **Remarks**.</span></span>

</dd> <dt>

<span data-ttu-id="4a81a-140">*ppItem* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4a81a-140">*ppItem* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a81a-141">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="4a81a-141">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="4a81a-142">O endereço de um ponteiro para o [**IWiaItem2**](-wia-iwiaitem2.md) do qual as imagens foram examinadas.</span><span class="sxs-lookup"><span data-stu-id="4a81a-142">The address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) that the images were scanned from.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a81a-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a81a-143">Return value</span></span>

<span data-ttu-id="4a81a-144">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4a81a-144">Type: **HRESULT**</span></span>

<span data-ttu-id="4a81a-145">**IWiaDevMgr2:: GetImageDlg** retornará s \_ OK se os dados forem transferidos com êxito, retornará s \_ false se o usuário cancelar a caixa de diálogo ou retornar um erro com padrão.</span><span class="sxs-lookup"><span data-stu-id="4a81a-145">**IWiaDevMgr2::GetImageDlg** returns S\_OK if the data is transferred successfully, returns S\_FALSE if the user cancels the dialog box, or returns a standard COM error.</span></span>

> [!Note]  
> <span data-ttu-id="4a81a-146">O parâmetro *ppbstrFilePaths* não está necessariamente vazio, se a função retornar S \_ false.</span><span class="sxs-lookup"><span data-stu-id="4a81a-146">The *ppbstrFilePaths* parameter is not necessarily empty, if the function returns S\_FALSE.</span></span> <span data-ttu-id="4a81a-147">Se o usuário cancelar, as páginas que concluíram a verificação serão processadas e retornadas em *ppbstrFilePaths*.</span><span class="sxs-lookup"><span data-stu-id="4a81a-147">If the user cancels, the pages that have completed scanning are processed and returned in *ppbstrFilePaths*.</span></span> <span data-ttu-id="4a81a-148">Mesmo que eles não sejam usados, você deve liberar a matriz.</span><span class="sxs-lookup"><span data-stu-id="4a81a-148">Even if they are not used, you must free the array.</span></span> <span data-ttu-id="4a81a-149">Consulte **comentários**.</span><span class="sxs-lookup"><span data-stu-id="4a81a-149">See **Remarks**.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="4a81a-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a81a-150">Remarks</span></span>

<span data-ttu-id="4a81a-151">Se o aplicativo passar **nulo** para o valor do parâmetro *bstrDeviceID* , **IWiaDevMgr2:: GetImageDlg** exibirá a caixa de diálogo **selecionar dispositivo** para que o usuário possa selecionar o dispositivo de entrada WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4a81a-151">If the application passes **NULL** for the value of the *bstrDeviceID* parameter, **IWiaDevMgr2::GetImageDlg** displays the **Select Device** dialog box so that the user can select the WIA 2.0 input device.</span></span>

<span data-ttu-id="4a81a-152">Use um item de menu chamado **de scanner** no menu **arquivo** para que as seleções de dispositivo e imagem estejam disponíveis em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4a81a-152">Use a menu item named **From scanner** on the **File** menu so that device and image selections are available in your application.</span></span>

<span data-ttu-id="4a81a-153">Chame [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) em cada BSTR na matriz à qual o *ppbstrFilePaths* \[ \] aponta e chame [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) na matriz em si para liberar a memória associada.</span><span class="sxs-lookup"><span data-stu-id="4a81a-153">Call [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) on each BSTR in the array that *ppbstrFilePaths*\[i\] points to, and call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) on the array itself to free associated memory.</span></span> <span data-ttu-id="4a81a-154">Se S \_ false for retornado, verifique se o valor que *plNumFiles* aponta para não é zero.</span><span class="sxs-lookup"><span data-stu-id="4a81a-154">If S\_FALSE is returned, check to see if the value that *plNumFiles* points to is not zero.</span></span> <span data-ttu-id="4a81a-155">Se o valor não for zero, libere os  \[ recursos ppbstrFilePaths i \] no aplicativo, pois o usuário pode cancelar após a verificação de uma ou mais páginas.</span><span class="sxs-lookup"><span data-stu-id="4a81a-155">If the value is not zero, free the *ppbstrFilePaths*\[i\] resources in the application, because the user might cancel after scanning one or more pages.</span></span> <span data-ttu-id="4a81a-156">Inicialize *plNumFiles* para zero antes de chamar **IWiaDevMgr2:: GetImageDlg**.</span><span class="sxs-lookup"><span data-stu-id="4a81a-156">Initialize *plNumFiles* to zero before you call **IWiaDevMgr2::GetImageDlg**.</span></span> <span data-ttu-id="4a81a-157">Se *plNumFiles* não for inicializado como zero e uma falha na infraestrutura com fizer com que a função retorne S \_ false antes de **IWiaDevMgr2:: GetImageDlg** for chamado, *plNumFiles* terá um valor de lixo enganoso.</span><span class="sxs-lookup"><span data-stu-id="4a81a-157">If *plNumFiles* is not initialized to zero and a failure in the COM infrastructure causes the function to return S\_FALSE before **IWiaDevMgr2::GetImageDlg** is called, then *plNumFiles* will have a misleading garbage value.</span></span>

<span data-ttu-id="4a81a-158">A caixa de diálogo deve ter direitos suficientes para *bstrFolderName* para que possa salvar os arquivos com nomes de arquivo exclusivos.</span><span class="sxs-lookup"><span data-stu-id="4a81a-158">The dialog box must have sufficient rights to *bstrFolderName* so that it can save the files with unique file names.</span></span> <span data-ttu-id="4a81a-159">Proteja a pasta com uma ACL (lista de controle de acesso) porque ela contém dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="4a81a-159">Protect the folder with an access control list (ACL) because it contains user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a81a-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a81a-160">Requirements</span></span>



| <span data-ttu-id="4a81a-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a81a-161">Requirement</span></span> | <span data-ttu-id="4a81a-162">Valor</span><span class="sxs-lookup"><span data-stu-id="4a81a-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4a81a-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a81a-163">Minimum supported client</span></span><br/> | <span data-ttu-id="4a81a-164">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a81a-164">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4a81a-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a81a-165">Minimum supported server</span></span><br/> | <span data-ttu-id="4a81a-166">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4a81a-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4a81a-167">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a81a-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a81a-168"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a81a-168"><dt>Wia.h</dt></span></span> </dl> |



 

 
