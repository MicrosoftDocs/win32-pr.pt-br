---
description: Cria um enumerador de informações de propriedade para cada dispositivo disponível de aquisição de imagem do Windows (WIA) 2,0.
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: 'Método IWiaDevMgr2:: EnumDeviceInfo (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.EnumDeviceInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bd9e9281b625f4cec5377537d82a304045b95a3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647484"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a><span data-ttu-id="5e768-103">Método IWiaDevMgr2:: EnumDeviceInfo</span><span class="sxs-lookup"><span data-stu-id="5e768-103">IWiaDevMgr2::EnumDeviceInfo method</span></span>

<span data-ttu-id="5e768-104">Cria um enumerador de informações de propriedade para cada dispositivo disponível de aquisição de imagem do Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="5e768-104">Creates an enumerator of property information for each available Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e768-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e768-105">Syntax</span></span>


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="5e768-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e768-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e768-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e768-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e768-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="5e768-108">Type: **LONG**</span></span>

<span data-ttu-id="5e768-109">Especifica o tipo de dispositivos WIA 2,0 a serem enumerados.</span><span class="sxs-lookup"><span data-stu-id="5e768-109">Specifies the type of WIA 2.0 devices to enumerate.</span></span>

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span data-ttu-id="5e768-110"><span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**\_local de \_ enumeração \_ DevInfo do WIA**</span><span class="sxs-lookup"><span data-stu-id="5e768-110"><span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA\_DEVINFO\_ENUM\_LOCAL**</span></span>


</dt> <dd>

<span data-ttu-id="5e768-111">Somente dispositivos de scanner ativos conectados localmente são enumerados.</span><span class="sxs-lookup"><span data-stu-id="5e768-111">Only locally connected active scanner devices are enumerated.</span></span>

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span data-ttu-id="5e768-112"><span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**\_Enumeração DevInfo do WIA \_ \_ All**</span><span class="sxs-lookup"><span data-stu-id="5e768-112"><span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA\_DEVINFO\_ENUM\_ALL**</span></span>


</dt> <dd>

<span data-ttu-id="5e768-113">Todos os dispositivos são enumerados, localmente e remoto, incluindo dispositivos inativos (desconectados) e dispositivos STI herdados.</span><span class="sxs-lookup"><span data-stu-id="5e768-113">All devices are enumerated, both locally and remote, including inactive (disconnected) devices and legacy STI-only devices.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5e768-114">*ppIEnum* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5e768-114">*ppIEnum* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5e768-115">Tipo: **[ **\_ \_ informações de desenvolvimento de IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***</span><span class="sxs-lookup"><span data-stu-id="5e768-115">Type: **[**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***</span></span>

<span data-ttu-id="5e768-116">Recebe o endereço de um ponteiro para a interface de [**\_ \_ informações de dev IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="5e768-116">Receives the address of a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e768-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e768-117">Return value</span></span>

<span data-ttu-id="5e768-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5e768-118">Type: **HRESULT**</span></span>

<span data-ttu-id="5e768-119">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5e768-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5e768-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5e768-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e768-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e768-121">Remarks</span></span>

<span data-ttu-id="5e768-122">O método **IWiaDevMgr2:: EnumDeviceInfo** cria um objeto enumerador que dá suporte à interface [**\_ \_ informações de desenvolvimento IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="5e768-122">The **IWiaDevMgr2::EnumDeviceInfo** method creates an enumerator object that supports the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span> <span data-ttu-id="5e768-123">O método armazena um ponteiro para a interface de **\_ \_ informações de dev IEnumWIA** no parâmetro *ppIEnum*.</span><span class="sxs-lookup"><span data-stu-id="5e768-123">The method stores a pointer to the **IEnumWIA\_DEV\_INFO** interface in the parameter *ppIEnum*.</span></span> <span data-ttu-id="5e768-124">Os aplicativos podem usar o ponteiro de interface de **\_ \_ informações de desenvolvimento IEnumWIA** para enumerar as propriedades de cada dispositivo WIA 2,0 conectado ao computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="5e768-124">Applications can use the **IEnumWIA\_DEV\_INFO** interface pointer to enumerate the properties of each WIA 2.0 device attached to the user's computer.</span></span>

<span data-ttu-id="5e768-125">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="5e768-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e768-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e768-126">Requirements</span></span>



| <span data-ttu-id="5e768-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e768-127">Requirement</span></span> | <span data-ttu-id="5e768-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5e768-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e768-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e768-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5e768-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e768-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5e768-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e768-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5e768-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e768-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5e768-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e768-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e768-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e768-134"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e768-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="5e768-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e768-136"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e768-136"><dt>Wia.idl</dt></span></span> </dl> |



 

 
