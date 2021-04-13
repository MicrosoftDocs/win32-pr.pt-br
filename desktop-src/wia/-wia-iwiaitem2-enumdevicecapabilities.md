---
description: Cria um enumerador que é usado para verificar os comandos e eventos aos quais um dispositivo de aquisição de imagem do Windows (WIA) 2,0 dá suporte.
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: 'Método IWiaItem2:: EnumDeviceCapabilities (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumDeviceCapabilities
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3e771aa636b42d9cd7e4024a1684ebe3edf02eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501794"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a><span data-ttu-id="d91ec-103">Método IWiaItem2:: EnumDeviceCapabilities</span><span class="sxs-lookup"><span data-stu-id="d91ec-103">IWiaItem2::EnumDeviceCapabilities method</span></span>

<span data-ttu-id="d91ec-104">Cria um enumerador que é usado para verificar os comandos e eventos aos quais um dispositivo de aquisição de imagem do Windows (WIA) 2,0 dá suporte.</span><span class="sxs-lookup"><span data-stu-id="d91ec-104">Creates an enumerator that is used to ascertain the commands and events a Windows Image Acquisition (WIA) 2.0 device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="d91ec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d91ec-105">Syntax</span></span>


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a><span data-ttu-id="d91ec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d91ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d91ec-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d91ec-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d91ec-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="d91ec-108">Type: **LONG**</span></span>

<span data-ttu-id="d91ec-109">Especifica um sinalizador que seleciona o tipo de recursos a serem enumerados.</span><span class="sxs-lookup"><span data-stu-id="d91ec-109">Specifies a flag that selects the type of capabilities to enumerate.</span></span> <span data-ttu-id="d91ec-110">É um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d91ec-110">It is one of the following values.</span></span>

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span data-ttu-id="d91ec-111"><span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**\_comandos do dispositivo WIA \_**</span><span class="sxs-lookup"><span data-stu-id="d91ec-111"><span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**WIA\_DEVICE\_COMMANDS**</span></span>


</dt> <dd>

<span data-ttu-id="d91ec-112">Enumere os comandos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d91ec-112">Enumerate device commands.</span></span>

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span data-ttu-id="d91ec-113"><span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**\_eventos do dispositivo WIA \_**</span><span class="sxs-lookup"><span data-stu-id="d91ec-113"><span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**WIA\_DEVICE\_EVENTS**</span></span>


</dt> <dd>

<span data-ttu-id="d91ec-114">Enumerar eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d91ec-114">Enumerate device events.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d91ec-115">*ppIEnumWIA \_ \_* Desativação de desenvolvimento \[\]</span><span class="sxs-lookup"><span data-stu-id="d91ec-115">*ppIEnumWIA\_DEV\_CAPS* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d91ec-116">Tipo: **[ **IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span><span class="sxs-lookup"><span data-stu-id="d91ec-116">Type: **[**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span></span>

<span data-ttu-id="d91ec-117">Recebe um ponteiro para a interface [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) criada por esse método.</span><span class="sxs-lookup"><span data-stu-id="d91ec-117">Receives a pointer to the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface created by this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d91ec-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d91ec-118">Return value</span></span>

<span data-ttu-id="d91ec-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d91ec-119">Type: **HRESULT**</span></span>

<span data-ttu-id="d91ec-120">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d91ec-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d91ec-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d91ec-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d91ec-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="d91ec-122">Remarks</span></span>

<span data-ttu-id="d91ec-123">Esse método é usado para criar um objeto de enumerador para obter o conjunto de comandos e eventos aos quais um dispositivo WIA 2,0 dá suporte.</span><span class="sxs-lookup"><span data-stu-id="d91ec-123">This method is used to create an enumerator object to obtain the set of commands and events that a WIA 2.0 device supports.</span></span> <span data-ttu-id="d91ec-124">O parâmetro *lFlags* é usado para especificar quais tipos de recursos de dispositivo serão enumerados.</span><span class="sxs-lookup"><span data-stu-id="d91ec-124">The *lFlags* parameter is used to specify which kinds of device capabilities to enumerate.</span></span> <span data-ttu-id="d91ec-125">O método **IWiaItem2:: EnumDeviceCapabilities** armazena o endereço da interface do objeto enumerador no parâmetro *ppIEnumWIA \_ dev \_ Caps* .</span><span class="sxs-lookup"><span data-stu-id="d91ec-125">The **IWiaItem2::EnumDeviceCapabilities** method stores the address of the interface of the enumerator object in the *ppIEnumWIA\_DEV\_CAPS* parameter.</span></span>

<span data-ttu-id="d91ec-126">Esse método só pode ser chamado no item raiz dos objetos [**IWiaItem2**](-wia-iwiaitem2.md) de uma árvore de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d91ec-126">This method can only be called on the root item of [**IWiaItem2**](-wia-iwiaitem2.md) objects of a device tree.</span></span>

<span data-ttu-id="d91ec-127">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIEnumWIA \_ dev \_ Caps* .</span><span class="sxs-lookup"><span data-stu-id="d91ec-127">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnumWIA\_DEV\_CAPS* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="d91ec-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d91ec-128">Requirements</span></span>



| <span data-ttu-id="d91ec-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d91ec-129">Requirement</span></span> | <span data-ttu-id="d91ec-130">Valor</span><span class="sxs-lookup"><span data-stu-id="d91ec-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d91ec-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d91ec-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d91ec-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d91ec-132">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d91ec-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d91ec-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d91ec-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d91ec-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d91ec-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d91ec-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d91ec-136"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="d91ec-136"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="d91ec-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="d91ec-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d91ec-138"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d91ec-138"><dt>Wia.idl</dt></span></span> </dl> |



 

 
