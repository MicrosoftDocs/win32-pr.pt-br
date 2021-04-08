---
description: Cria uma árvore hierárquica de objetos IWiaItem2 para um dispositivo de aquisição de imagem do Windows (WIA) 2,0.
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: 'Método IWiaDevMgr2:: CreateDevice (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.CreateDevice
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a548a0ef43c2621b77c4ed10acde393af21d596d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828456"
---
# <a name="iwiadevmgr2createdevice-method"></a><span data-ttu-id="7b83a-103">Método IWiaDevMgr2:: CreateDevice</span><span class="sxs-lookup"><span data-stu-id="7b83a-103">IWiaDevMgr2::CreateDevice method</span></span>

<span data-ttu-id="7b83a-104">Cria uma árvore hierárquica de objetos [**IWiaItem2**](-wia-iwiaitem2.md) para um dispositivo de aquisição de imagem do Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="7b83a-104">Creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for a Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b83a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b83a-105">Syntax</span></span>


```C++
HRESULT CreateDevice(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrDeviceID,
  [out] IWiaItem2 **ppWiaItem2Root
);
```



## <a name="parameters"></a><span data-ttu-id="7b83a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b83a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b83a-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b83a-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b83a-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="7b83a-108">Type: **LONG**</span></span>

<span data-ttu-id="7b83a-109">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="7b83a-109">Currently unused.</span></span> <span data-ttu-id="7b83a-110">Deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="7b83a-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7b83a-111">*bstrDeviceID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b83a-111">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b83a-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7b83a-112">Type: **BSTR**</span></span>

<span data-ttu-id="7b83a-113">Especifica o identificador exclusivo do dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="7b83a-113">Specifies the unique identifier of the WIA 2.0 device.</span></span>

</dd> <dt>

<span data-ttu-id="7b83a-114">*ppWiaItem2Root* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7b83a-114">*ppWiaItem2Root* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b83a-115">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="7b83a-115">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="7b83a-116">Recebe o endereço de um ponteiro para a interface [**IWiaItem2**](-wia-iwiaitem2.md) do item raiz na árvore hierárquica do dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="7b83a-116">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item in the hierarchical tree for the WIA 2.0 device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b83a-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b83a-117">Return value</span></span>

<span data-ttu-id="7b83a-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7b83a-118">Type: **HRESULT**</span></span>

<span data-ttu-id="7b83a-119">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7b83a-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7b83a-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7b83a-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b83a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b83a-121">Remarks</span></span>

<span data-ttu-id="7b83a-122">Os aplicativos usam o método **IWiaDevMgr2:: CreateDevice** para criar um objeto de dispositivo para os dispositivos WIA 2,0 especificados pelo parâmetro bstrDeviceID.</span><span class="sxs-lookup"><span data-stu-id="7b83a-122">Applications use the **IWiaDevMgr2::CreateDevice** method to create a device object for the WIA 2.0 devices specified by the bstrDeviceID parameter.</span></span> <span data-ttu-id="7b83a-123">Quando ele retorna, o método **IWiaDevMgr2:: CreateDevice** armazena um endereço de um ponteiro no parâmetro *ppWiaItem2Root*, que aponta para o item raiz da árvore de objetos [**IWiaItem2**](-wia-iwiaitem2.md) criados por **IWiaDevMgr2:: CreateDevice**.</span><span class="sxs-lookup"><span data-stu-id="7b83a-123">When it returns, the **IWiaDevMgr2::CreateDevice** method stores an address of a pointer in the parameter *ppWiaItem2Root*, which points to the root item of the tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects created by **IWiaDevMgr2::CreateDevice**.</span></span> <span data-ttu-id="7b83a-124">Os aplicativos podem usar essa árvore de objetos para controlar e recuperar dados do dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="7b83a-124">Applications can use this tree of objects to control and retrieve data from the WIA 2.0 device.</span></span>

<span data-ttu-id="7b83a-125">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros recebidos por meio do parâmetro *ppWiaItem2Root* .</span><span class="sxs-lookup"><span data-stu-id="7b83a-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the pointers they receive through the *ppWiaItem2Root* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b83a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b83a-126">Requirements</span></span>



| <span data-ttu-id="7b83a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b83a-127">Requirement</span></span> | <span data-ttu-id="7b83a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="7b83a-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b83a-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b83a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7b83a-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b83a-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7b83a-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b83a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7b83a-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7b83a-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7b83a-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b83a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b83a-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b83a-134"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="7b83a-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="7b83a-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7b83a-136"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7b83a-136"><dt>Wia.idl</dt></span></span> </dl> |



 

 
