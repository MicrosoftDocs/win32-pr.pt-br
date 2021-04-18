---
description: Exibe uma caixa de diálogo que permite ao usuário selecionar um dispositivo de hardware para aquisição de imagem.
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: 'Método IWiaDevMgr2:: SelectDeviceDlgID (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlgID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bad749eb48e72b362070ea4951d4e9eac380e737
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810832"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a><span data-ttu-id="83c1c-103">Método IWiaDevMgr2:: SelectDeviceDlgID</span><span class="sxs-lookup"><span data-stu-id="83c1c-103">IWiaDevMgr2::SelectDeviceDlgID method</span></span>

<span data-ttu-id="83c1c-104">Exibe uma caixa de diálogo que permite ao usuário selecionar um dispositivo de hardware para aquisição de imagem.</span><span class="sxs-lookup"><span data-stu-id="83c1c-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="83c1c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83c1c-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlgID(
  [in]          HWND hwndParent,
  [in]          LONG lDeviceType,
  [in]          LONG lFlags,
  [out, retval] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="83c1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83c1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83c1c-107">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83c1c-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83c1c-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="83c1c-108">Type: **HWND**</span></span>

<span data-ttu-id="83c1c-109">Especifica a janela pai da caixa de diálogo **selecionar dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="83c1c-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="83c1c-110">*lDeviceType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83c1c-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83c1c-111">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="83c1c-111">Type: **LONG**</span></span>

<span data-ttu-id="83c1c-112">Especifica o tipo de dispositivo WIA 2,0 a ser usado.</span><span class="sxs-lookup"><span data-stu-id="83c1c-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="83c1c-113">Consulte [especificadores de tipo de dispositivo WIA](-wia-wia-device-type-specifiers.md) para obter uma lista de valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="83c1c-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="83c1c-114">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83c1c-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83c1c-115">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="83c1c-115">Type: **LONG**</span></span>

<span data-ttu-id="83c1c-116">Especifica o comportamento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="83c1c-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="83c1c-117">O valor pode ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="83c1c-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="83c1c-118"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="83c1c-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="83c1c-119">Use o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="83c1c-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="83c1c-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ selecionar \_ dispositivo \_ padrão**</span><span class="sxs-lookup"><span data-stu-id="83c1c-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="83c1c-121">Exibir a caixa de diálogo mesmo que haja apenas um dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="83c1c-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="83c1c-122">*pbstrDeviceID* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="83c1c-122">*pbstrDeviceID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="83c1c-123">Tipo: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="83c1c-123">Type: \**BSTR\** _</span></span>

<span data-ttu-id="83c1c-124">Ponteiro para uma cadeia de caracteres que recebe a cadeia de caracteres do identificador do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83c1c-124">Pointer to a string that receives the identifier string of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83c1c-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83c1c-125">Return value</span></span>

<span data-ttu-id="83c1c-126">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="83c1c-126">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="83c1c-127">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="83c1c-127">This method can return one of these values.</span></span>



| <span data-ttu-id="83c1c-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="83c1c-128">Return code</span></span>                                                                                                  | <span data-ttu-id="83c1c-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="83c1c-129">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="83c1c-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="83c1c-130"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="83c1c-131">O dispositivo foi selecionado com êxito.</span><span class="sxs-lookup"><span data-stu-id="83c1c-131">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="83c1c-132"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="83c1c-132"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="83c1c-133">O usuário cancelou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="83c1c-133">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="83c1c-134"><dt>**WIA \_ S \_ nenhum \_ dispositivo \_ disponível**</dt></span><span class="sxs-lookup"><span data-stu-id="83c1c-134"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="83c1c-135">Nenhum dispositivo de hardware WIA 2,0 corresponde às especificações fornecidas no parâmetro *lDeviceType* .</span><span class="sxs-lookup"><span data-stu-id="83c1c-135">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="83c1c-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="83c1c-136">Remarks</span></span>

<span data-ttu-id="83c1c-137">Esse método cria e exibe a caixa de diálogo **selecionar dispositivo** para que o usuário possa selecionar um dispositivo WIA 2,0 para aquisição de imagem.</span><span class="sxs-lookup"><span data-stu-id="83c1c-137">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="83c1c-138">Se um dispositivo for selecionado com êxito, o método **IWiaDevMgr2:: SelectDeviceDlgID** passará sua cadeia de caracteres de identificador para o aplicativo por meio de seu parâmetro *pbstrDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="83c1c-138">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlgID** method passes its identifier string to the application through its *pbstrDeviceID* parameter.</span></span>

<span data-ttu-id="83c1c-139">O aplicativo pode restringir os dispositivos exibidos ao usuário para tipos específicos especificando os tipos de dispositivo por meio do parâmetro *lDeviceType* .</span><span class="sxs-lookup"><span data-stu-id="83c1c-139">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="83c1c-140">Se apenas um dispositivo atender à especificação, **IWiaDevMgr2:: SelectDeviceDlgID** não exibirá a caixa de diálogo **selecionar dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="83c1c-140">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlgID** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="83c1c-141">Em vez disso, ele passa a cadeia de caracteres do identificador do dispositivo para o aplicativo sem exibir a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="83c1c-141">Instead it passes the device's identifier string to the application without displaying the dialog box.</span></span> <span data-ttu-id="83c1c-142">Você pode substituir esse comportamento e forçar **IWiaDevMgr2:: SelectDeviceDlgID** a exibir a caixa de diálogo passando o \_ WIA \_ selecione \_ o dispositivo como o valor para o parâmetro *lFlags* .</span><span class="sxs-lookup"><span data-stu-id="83c1c-142">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlgID** to display the dialog box by passing WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="83c1c-143">Se mais de um dispositivo WIA 2,0 corresponder à especificação, todos os dispositivos correspondentes serão exibidos na caixa de diálogo SelectDevice para que o usuário possa escolher um.</span><span class="sxs-lookup"><span data-stu-id="83c1c-143">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the SelectDevice dialog box so the user may choose one.</span></span>

> [!Note]  
> <span data-ttu-id="83c1c-144">É recomendável que os aplicativos tornem a seleção de dispositivo e imagem disponível por meio de um item de menu chamado **de scanner** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="83c1c-144">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="83c1c-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83c1c-145">Requirements</span></span>



| <span data-ttu-id="83c1c-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="83c1c-146">Requirement</span></span> | <span data-ttu-id="83c1c-147">Valor</span><span class="sxs-lookup"><span data-stu-id="83c1c-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="83c1c-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83c1c-148">Minimum supported client</span></span><br/> | <span data-ttu-id="83c1c-149">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83c1c-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="83c1c-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83c1c-150">Minimum supported server</span></span><br/> | <span data-ttu-id="83c1c-151">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="83c1c-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="83c1c-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="83c1c-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="83c1c-153"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="83c1c-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="83c1c-154">INSERI</span><span class="sxs-lookup"><span data-stu-id="83c1c-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="83c1c-155"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="83c1c-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 




