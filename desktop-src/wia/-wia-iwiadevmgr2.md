---
description: A interface IWiaDevMgr2 é usada para criar e gerenciar dispositivos de aquisição de imagem e para se registrar para receber eventos de dispositivo.
ms.assetid: 0e9fb3a1-bbe3-4dba-ba8c-b79f202d5a38
title: Interface IWiaDevMgr2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1dd73733d77c80ba4f3880464000f823e0e35092
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828453"
---
# <a name="iwiadevmgr2-interface"></a><span data-ttu-id="decef-103">Interface IWiaDevMgr2</span><span class="sxs-lookup"><span data-stu-id="decef-103">IWiaDevMgr2 interface</span></span>

<span data-ttu-id="decef-104">A interface **IWiaDevMgr2** é usada para criar e gerenciar dispositivos de aquisição de imagem e para se registrar para receber eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="decef-104">The **IWiaDevMgr2** interface is used to create and manage image acquisition devices and to register to receive device events.</span></span>

## <a name="members"></a><span data-ttu-id="decef-105">Membros</span><span class="sxs-lookup"><span data-stu-id="decef-105">Members</span></span>

<span data-ttu-id="decef-106">A interface **IWiaDevMgr2** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="decef-106">The **IWiaDevMgr2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="decef-107">**IWiaDevMgr2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="decef-107">**IWiaDevMgr2** also has these types of members:</span></span>

-   [<span data-ttu-id="decef-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="decef-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="decef-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="decef-109">Methods</span></span>

<span data-ttu-id="decef-110">A interface **IWiaDevMgr2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="decef-110">The **IWiaDevMgr2** interface has these methods.</span></span>



| <span data-ttu-id="decef-111">Método</span><span class="sxs-lookup"><span data-stu-id="decef-111">Method</span></span>                                                                                    | <span data-ttu-id="decef-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="decef-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="decef-113">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="decef-113">**CreateDevice**</span></span>](-wia-iwiadevmgr2-createdevice.md)                                     | <span data-ttu-id="decef-114">Cria uma árvore hierárquica de objetos [**IWiaItem2**](-wia-iwiaitem2.md) para um dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="decef-114">Creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for a WIA 2.0 device.</span></span> <br/>                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="decef-115">**EnumDeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="decef-115">**EnumDeviceInfo**</span></span>](-wia-iwiadevmgr2-enumdeviceinfo.md)                                 | <span data-ttu-id="decef-116">Cria um enumerador de informações de propriedade para cada dispositivo WIA 2,0 disponível.</span><span class="sxs-lookup"><span data-stu-id="decef-116">Creates an enumerator of property information for each available WIA 2.0 device.</span></span> <br/>                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="decef-117">**GetImageDlg**</span><span class="sxs-lookup"><span data-stu-id="decef-117">**GetImageDlg**</span></span>](-wia-iwiadevmgr2-getimagedlg.md)                                       | <span data-ttu-id="decef-118">O método [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) exibe uma ou mais caixas de diálogo que permitem que um usuário adquira uma imagem de um dispositivo WIA 2,0 e grave a imagem em um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="decef-118">The [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) method displays one or more dialog boxes that enable a user to acquire an image from a WIA 2.0 device and write the image to a specified file.</span></span> <span data-ttu-id="decef-119">Esse método estende a funcionalidade de [**IWiaDevMgr2:: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) para encapsular a aquisição de imagem em uma única chamada à API.</span><span class="sxs-lookup"><span data-stu-id="decef-119">This method extends the functionality of [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) to encapsulate image acquisition within a single API call.</span></span> <br/> |
| [<span data-ttu-id="decef-120">**RegisterEventCallbackCLSID**</span><span class="sxs-lookup"><span data-stu-id="decef-120">**RegisterEventCallbackCLSID**</span></span>](-wia-iwiadevmgr2-registereventcallbackclsid.md)         | <span data-ttu-id="decef-121">O método [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) registra um aplicativo para receber eventos, mesmo que o aplicativo não esteja em execução.</span><span class="sxs-lookup"><span data-stu-id="decef-121">The [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) method registers an application to receive events even if the application is not running.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="decef-122">**RegisterEventCallbackInterface**</span><span class="sxs-lookup"><span data-stu-id="decef-122">**RegisterEventCallbackInterface**</span></span>](-wia-iwiadevmgr2-registereventcallbackinterface.md) | <span data-ttu-id="decef-123">Registra um aplicativo em execução para notificação de eventos WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="decef-123">Registers a running application for WIA 2.0 event notification.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="decef-124">**RegisterEventCallbackProgram**</span><span class="sxs-lookup"><span data-stu-id="decef-124">**RegisterEventCallbackProgram**</span></span>](-wia-iwiadevmgr2-registereventcallbackprogram.md)     | <span data-ttu-id="decef-125">O método [**IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) registra um aplicativo para receber eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="decef-125">The [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) method registers an application to receive device events.</span></span> <span data-ttu-id="decef-126">Ele é fornecido principalmente para compatibilidade com versões anteriores com aplicativos que não foram escritos para o WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="decef-126">It is primarily provided for backward compatibility with applications that were not written for WIA 2.0.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="decef-127">**SelectDeviceDlg**</span><span class="sxs-lookup"><span data-stu-id="decef-127">**SelectDeviceDlg**</span></span>](-wia-iwiadevmgr2-selectdevicedlg.md)                               | <span data-ttu-id="decef-128">Exibe uma caixa de diálogo que permite ao usuário selecionar um dispositivo de hardware para aquisição de imagem.</span><span class="sxs-lookup"><span data-stu-id="decef-128">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span> <br/>                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="decef-129">**SelectDeviceDlgID**</span><span class="sxs-lookup"><span data-stu-id="decef-129">**SelectDeviceDlgID**</span></span>](-wia-iwiadevmgr2-selectdevicedlgid.md)                           | <span data-ttu-id="decef-130">Exibe uma caixa de diálogo que permite ao usuário selecionar um dispositivo de hardware para aquisição de imagem.</span><span class="sxs-lookup"><span data-stu-id="decef-130">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span> <br/>                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="decef-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="decef-131">Remarks</span></span>

<span data-ttu-id="decef-132">A interface **IWiaDevMgr2** , como todas as interfaces de Component Object Model (com), herda os métodos de interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="decef-132">The **IWiaDevMgr2** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="decef-133">Métodos IUnknown</span><span class="sxs-lookup"><span data-stu-id="decef-133">IUnknown Methods</span></span>                                        | <span data-ttu-id="decef-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="decef-134">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="decef-135">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="decef-135">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="decef-136">Retorna ponteiros para interfaces com suporte.</span><span class="sxs-lookup"><span data-stu-id="decef-136">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="decef-137">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="decef-137">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="decef-138">Incrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="decef-138">Increments reference count.</span></span>               |
| [<span data-ttu-id="decef-139">IUnknown:: versão</span><span class="sxs-lookup"><span data-stu-id="decef-139">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="decef-140">Decrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="decef-140">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="decef-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="decef-141">Requirements</span></span>



| <span data-ttu-id="decef-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="decef-142">Requirement</span></span> | <span data-ttu-id="decef-143">Valor</span><span class="sxs-lookup"><span data-stu-id="decef-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="decef-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="decef-144">Minimum supported client</span></span><br/> | <span data-ttu-id="decef-145">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="decef-145">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="decef-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="decef-146">Minimum supported server</span></span><br/> | <span data-ttu-id="decef-147">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="decef-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="decef-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="decef-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="decef-149"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="decef-149"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="decef-150">INSERI</span><span class="sxs-lookup"><span data-stu-id="decef-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="decef-151"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="decef-151"><dt>Wia.idl</dt></span></span> </dl> |



 

 
