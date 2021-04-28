---
description: 'Método IWiaDevMgr2:: SelectDeviceDlg – exibe uma caixa de diálogo que permite ao usuário selecionar um dispositivo de hardware para aquisição de imagem.'
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
ms.openlocfilehash: 60ec24f264b8fe0424f17fc32deaf803e55c3346
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091254"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a><span data-ttu-id="43ca4-103">Método IWiaDevMgr2:: SelectDeviceDlg</span><span class="sxs-lookup"><span data-stu-id="43ca4-103">IWiaDevMgr2::SelectDeviceDlg method</span></span>

<span data-ttu-id="43ca4-104">Exibe uma caixa de diálogo que permite ao usuário selecionar um dispositivo de hardware para aquisição de imagem.</span><span class="sxs-lookup"><span data-stu-id="43ca4-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="43ca4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43ca4-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
);
```



## <a name="parameters"></a><span data-ttu-id="43ca4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43ca4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43ca4-107">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43ca4-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ca4-108">Digite: **HWND**</span><span class="sxs-lookup"><span data-stu-id="43ca4-108">Type: **HWND**</span></span>

<span data-ttu-id="43ca4-109">Especifica a janela pai da caixa de diálogo **selecionar dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="43ca4-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="43ca4-110">*lDeviceType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43ca4-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ca4-111">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="43ca4-111">Type: **LONG**</span></span>

<span data-ttu-id="43ca4-112">Especifica o tipo de dispositivo WIA 2,0 a ser usado.</span><span class="sxs-lookup"><span data-stu-id="43ca4-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="43ca4-113">Consulte [especificadores de tipo de dispositivo WIA](-wia-wia-device-type-specifiers.md) para obter uma lista de valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="43ca4-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="43ca4-114">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43ca4-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43ca4-115">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="43ca4-115">Type: **LONG**</span></span>

<span data-ttu-id="43ca4-116">Especifica o comportamento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="43ca4-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="43ca4-117">O valor pode ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="43ca4-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="43ca4-118"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="43ca4-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="43ca4-119">Use o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="43ca4-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="43ca4-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ selecionar \_ dispositivo \_ padrão**</span><span class="sxs-lookup"><span data-stu-id="43ca4-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="43ca4-121">Exibir a caixa de diálogo mesmo que haja apenas um dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="43ca4-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="43ca4-122">*pbstrDeviceID* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="43ca4-122">*pbstrDeviceID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="43ca4-123">Tipo: **BSTR \***</span><span class="sxs-lookup"><span data-stu-id="43ca4-123">Type: **BSTR\***</span></span>

<span data-ttu-id="43ca4-124">Na saída, recebe uma cadeia de caracteres que contém a cadeia de caracteres do identificador do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43ca4-124">On output, receives a string which contains the device's identifier string.</span></span> <span data-ttu-id="43ca4-125">Na entrada, passe o endereço de um ponteiro se essas informações forem necessárias, ou **NULL** se não for necessário.</span><span class="sxs-lookup"><span data-stu-id="43ca4-125">On input, pass the address of a pointer if this information is needed, or **NULL** if it is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="43ca4-126">*ppItemRoot* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="43ca4-126">*ppItemRoot* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="43ca4-127">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="43ca4-127">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="43ca4-128">Recebe o endereço de um ponteiro para a interface [**IWiaItem2**](-wia-iwiaitem2.md) do item raiz da árvore hierárquica que representa o dispositivo WIA 2,0 selecionado.</span><span class="sxs-lookup"><span data-stu-id="43ca4-128">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item of the hierarchical tree that represents the selected WIA 2.0 device.</span></span> <span data-ttu-id="43ca4-129">Se nenhum dispositivo for encontrado, ele receberá **NULL**.</span><span class="sxs-lookup"><span data-stu-id="43ca4-129">If no device is found, it receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43ca4-130">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="43ca4-130">Return value</span></span>

<span data-ttu-id="43ca4-131">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="43ca4-131">Type: **HRESULT**</span></span>

<span data-ttu-id="43ca4-132">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="43ca4-132">This method can return one of these values.</span></span>



| <span data-ttu-id="43ca4-133">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="43ca4-133">Return code</span></span>                                                                                                  | <span data-ttu-id="43ca4-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="43ca4-134">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43ca4-135"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="43ca4-135"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="43ca4-136">O dispositivo foi selecionado com êxito.</span><span class="sxs-lookup"><span data-stu-id="43ca4-136">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="43ca4-137"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="43ca4-137"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="43ca4-138">O usuário cancelou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="43ca4-138">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="43ca4-139"><dt>**WIA \_ S \_ nenhum \_ dispositivo \_ disponível**</dt></span><span class="sxs-lookup"><span data-stu-id="43ca4-139"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="43ca4-140">Nenhum dispositivo de hardware WIA 2,0 corresponde às especificações fornecidas no parâmetro *lDeviceType* .</span><span class="sxs-lookup"><span data-stu-id="43ca4-140">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="43ca4-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="43ca4-141">Remarks</span></span>

<span data-ttu-id="43ca4-142">Esse método cria e exibe a caixa de diálogo **selecionar dispositivo** para que o usuário possa selecionar um dispositivo WIA 2,0 para aquisição de imagem.</span><span class="sxs-lookup"><span data-stu-id="43ca4-142">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="43ca4-143">Se um dispositivo for selecionado com êxito, o método **IWiaDevMgr2:: SelectDeviceDlg** criará uma árvore hierárquica de objetos [**IWiaItem2**](-wia-iwiaitem2.md) para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43ca4-143">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlg** method creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for the device.</span></span> <span data-ttu-id="43ca4-144">Ele armazena um ponteiro para a interface **IWiaItem2** do item raiz no parâmetro *ppItemRoot*.</span><span class="sxs-lookup"><span data-stu-id="43ca4-144">It stores a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span>

<span data-ttu-id="43ca4-145">O aplicativo pode restringir os dispositivos exibidos ao usuário para tipos específicos especificando os tipos de dispositivo por meio do parâmetro *lDeviceType* .</span><span class="sxs-lookup"><span data-stu-id="43ca4-145">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="43ca4-146">Se apenas um dispositivo atender à especificação, **IWiaDevMgr2:: SelectDeviceDlg** não exibirá a caixa de diálogo **selecionar dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="43ca4-146">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlg** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="43ca4-147">Em vez disso, ele cria a árvore [**IWiaItem2**](-wia-iwiaitem2.md) para o dispositivo e armazena um ponteiro para a interface **IWiaItem2** do item raiz no parâmetro *ppItemRoot*.</span><span class="sxs-lookup"><span data-stu-id="43ca4-147">Instead it creates the [**IWiaItem2**](-wia-iwiaitem2.md) tree for the device and store a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span> <span data-ttu-id="43ca4-148">Você pode substituir esse comportamento e forçar **IWiaDevMgr2:: SelectDeviceDlg** a exibir a caixa de diálogo ESPECIFICANDO o WIA \_ selecionar \_ dispositivo \_ como o valor para o parâmetro *lFlags* .</span><span class="sxs-lookup"><span data-stu-id="43ca4-148">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlg** to display the dialog box by specifying WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="43ca4-149">Se mais de um dispositivo WIA 2,0 corresponder à especificação, todos os dispositivos correspondentes serão exibidos na caixa de diálogo **selecionar dispositivo** para que o usuário possa escolher um.</span><span class="sxs-lookup"><span data-stu-id="43ca4-149">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the **Select Device** dialog box so the user may choose one.</span></span>

<span data-ttu-id="43ca4-150">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppItemRoot* .</span><span class="sxs-lookup"><span data-stu-id="43ca4-150">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppItemRoot* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="43ca4-151">É recomendável que os aplicativos tornem a seleção de dispositivo e imagem disponível por meio de um item de menu chamado **de scanner** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="43ca4-151">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="43ca4-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43ca4-152">Requirements</span></span>



| <span data-ttu-id="43ca4-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="43ca4-153">Requirement</span></span> | <span data-ttu-id="43ca4-154">Valor</span><span class="sxs-lookup"><span data-stu-id="43ca4-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43ca4-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43ca4-155">Minimum supported client</span></span><br/> | <span data-ttu-id="43ca4-156">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43ca4-156">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="43ca4-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43ca4-157">Minimum supported server</span></span><br/> | <span data-ttu-id="43ca4-158">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="43ca4-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="43ca4-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43ca4-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="43ca4-160"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="43ca4-160"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="43ca4-161">INSERI</span><span class="sxs-lookup"><span data-stu-id="43ca4-161">IDL</span></span><br/>                      | <dl> <span data-ttu-id="43ca4-162"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="43ca4-162"><dt>Wia.idl</dt></span></span> </dl> |



 

 
