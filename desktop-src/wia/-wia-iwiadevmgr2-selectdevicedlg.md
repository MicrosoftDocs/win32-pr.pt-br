---
description: Exibe uma caixa de diálogo que permite ao usuário selecionar um dispositivo de hardware para aquisição de imagem.
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: 'Método IWiaDevMgr2:: SelectDeviceDlg (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: cb41ec8e94782ee4d7408c53e2d4e098d986fe83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812104"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a><span data-ttu-id="b3908-103">Método IWiaDevMgr2:: SelectDeviceDlg</span><span class="sxs-lookup"><span data-stu-id="b3908-103">IWiaDevMgr2::SelectDeviceDlg method</span></span>

<span data-ttu-id="b3908-104">Exibe uma caixa de diálogo que permite ao usuário selecionar um dispositivo de hardware para aquisição de imagem.</span><span class="sxs-lookup"><span data-stu-id="b3908-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3908-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3908-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
);
```



## <a name="parameters"></a><span data-ttu-id="b3908-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3908-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3908-107">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3908-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3908-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="b3908-108">Type: **HWND**</span></span>

<span data-ttu-id="b3908-109">Especifica a janela pai da caixa de diálogo **selecionar dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="b3908-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b3908-110">*lDeviceType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3908-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3908-111">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="b3908-111">Type: **LONG**</span></span>

<span data-ttu-id="b3908-112">Especifica o tipo de dispositivo WIA 2,0 a ser usado.</span><span class="sxs-lookup"><span data-stu-id="b3908-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="b3908-113">Consulte [especificadores de tipo de dispositivo WIA](-wia-wia-device-type-specifiers.md) para obter uma lista de valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="b3908-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="b3908-114">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3908-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3908-115">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="b3908-115">Type: **LONG**</span></span>

<span data-ttu-id="b3908-116">Especifica o comportamento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b3908-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="b3908-117">O valor pode ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="b3908-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="b3908-118"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="b3908-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="b3908-119">Use o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="b3908-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="b3908-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ selecionar \_ dispositivo \_ padrão**</span><span class="sxs-lookup"><span data-stu-id="b3908-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="b3908-121">Exibir a caixa de diálogo mesmo que haja apenas um dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="b3908-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b3908-122">*pbstrDeviceID* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b3908-122">*pbstrDeviceID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3908-123">Tipo: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="b3908-123">Type: \**BSTR\** _</span></span>

<span data-ttu-id="b3908-124">Na saída, recebe uma cadeia de caracteres que contém a cadeia de caracteres do identificador do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3908-124">On output, receives a string which contains the device's identifier string.</span></span> <span data-ttu-id="b3908-125">Na entrada, passe o endereço de um ponteiro se essas informações forem necessárias ou _ *NULL*\* se não for necessário.</span><span class="sxs-lookup"><span data-stu-id="b3908-125">On input, pass the address of a pointer if this information is needed, or _ *NULL*\* if it is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="b3908-126">*ppItemRoot* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b3908-126">*ppItemRoot* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b3908-127">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b3908-127">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="b3908-128">Recebe o endereço de um ponteiro para a interface [**IWiaItem2**](-wia-iwiaitem2.md) do item raiz da árvore hierárquica que representa o dispositivo WIA 2,0 selecionado.</span><span class="sxs-lookup"><span data-stu-id="b3908-128">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item of the hierarchical tree that represents the selected WIA 2.0 device.</span></span> <span data-ttu-id="b3908-129">Se nenhum dispositivo for encontrado, ele receberá **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b3908-129">If no device is found, it receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3908-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3908-130">Return value</span></span>

<span data-ttu-id="b3908-131">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b3908-131">Type: **HRESULT**</span></span>

<span data-ttu-id="b3908-132">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b3908-132">This method can return one of these values.</span></span>



| <span data-ttu-id="b3908-133">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b3908-133">Return code</span></span>                                                                                                  | <span data-ttu-id="b3908-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3908-134">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3908-135"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b3908-135"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="b3908-136">O dispositivo foi selecionado com êxito.</span><span class="sxs-lookup"><span data-stu-id="b3908-136">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="b3908-137"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="b3908-137"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="b3908-138">O usuário cancelou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b3908-138">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="b3908-139"><dt>**WIA \_ S \_ nenhum \_ dispositivo \_ disponível**</dt></span><span class="sxs-lookup"><span data-stu-id="b3908-139"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="b3908-140">Nenhum dispositivo de hardware WIA 2,0 corresponde às especificações fornecidas no parâmetro *lDeviceType* .</span><span class="sxs-lookup"><span data-stu-id="b3908-140">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="b3908-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3908-141">Remarks</span></span>

<span data-ttu-id="b3908-142">Esse método cria e exibe a caixa de diálogo **selecionar dispositivo** para que o usuário possa selecionar um dispositivo WIA 2,0 para aquisição de imagem.</span><span class="sxs-lookup"><span data-stu-id="b3908-142">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="b3908-143">Se um dispositivo for selecionado com êxito, o método **IWiaDevMgr2:: SelectDeviceDlg** criará uma árvore hierárquica de objetos [**IWiaItem2**](-wia-iwiaitem2.md) para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3908-143">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlg** method creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for the device.</span></span> <span data-ttu-id="b3908-144">Ele armazena um ponteiro para a interface **IWiaItem2** do item raiz no parâmetro *ppItemRoot*.</span><span class="sxs-lookup"><span data-stu-id="b3908-144">It stores a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span>

<span data-ttu-id="b3908-145">O aplicativo pode restringir os dispositivos exibidos ao usuário para tipos específicos especificando os tipos de dispositivo por meio do parâmetro *lDeviceType* .</span><span class="sxs-lookup"><span data-stu-id="b3908-145">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="b3908-146">Se apenas um dispositivo atender à especificação, **IWiaDevMgr2:: SelectDeviceDlg** não exibirá a caixa de diálogo **selecionar dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="b3908-146">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlg** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="b3908-147">Em vez disso, ele cria a árvore [**IWiaItem2**](-wia-iwiaitem2.md) para o dispositivo e armazena um ponteiro para a interface **IWiaItem2** do item raiz no parâmetro *ppItemRoot*.</span><span class="sxs-lookup"><span data-stu-id="b3908-147">Instead it creates the [**IWiaItem2**](-wia-iwiaitem2.md) tree for the device and store a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span> <span data-ttu-id="b3908-148">Você pode substituir esse comportamento e forçar **IWiaDevMgr2:: SelectDeviceDlg** a exibir a caixa de diálogo ESPECIFICANDO o WIA \_ selecionar \_ dispositivo \_ como o valor para o parâmetro *lFlags* .</span><span class="sxs-lookup"><span data-stu-id="b3908-148">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlg** to display the dialog box by specifying WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="b3908-149">Se mais de um dispositivo WIA 2,0 corresponder à especificação, todos os dispositivos correspondentes serão exibidos na caixa de diálogo **selecionar dispositivo** para que o usuário possa escolher um.</span><span class="sxs-lookup"><span data-stu-id="b3908-149">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the **Select Device** dialog box so the user may choose one.</span></span>

<span data-ttu-id="b3908-150">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppItemRoot* .</span><span class="sxs-lookup"><span data-stu-id="b3908-150">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppItemRoot* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="b3908-151">É recomendável que os aplicativos tornem a seleção de dispositivo e imagem disponível por meio de um item de menu chamado **de scanner** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="b3908-151">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b3908-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3908-152">Requirements</span></span>



| <span data-ttu-id="b3908-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3908-153">Requirement</span></span> | <span data-ttu-id="b3908-154">Valor</span><span class="sxs-lookup"><span data-stu-id="b3908-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3908-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3908-155">Minimum supported client</span></span><br/> | <span data-ttu-id="b3908-156">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3908-156">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b3908-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3908-157">Minimum supported server</span></span><br/> | <span data-ttu-id="b3908-158">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3908-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b3908-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3908-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3908-160"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3908-160"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3908-161">INSERI</span><span class="sxs-lookup"><span data-stu-id="b3908-161">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3908-162"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3908-162"><dt>Wia.idl</dt></span></span> </dl> |



 

 
