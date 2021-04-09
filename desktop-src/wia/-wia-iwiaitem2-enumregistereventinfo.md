---
description: 'O método IWiaItem2:: EnumRegisterEventInfo cria um enumerador que você pode usar para obter informações sobre eventos para os quais um aplicativo está registrado.'
ms.assetid: 9c25e9ae-bd3e-46a6-b4c2-c0bbcd265d51
title: 'Método IWiaItem2:: EnumRegisterEventInfo (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumRegisterEventInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b5899b629267f74724129aeae3f66801953d8cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090510"
---
# <a name="iwiaitem2enumregistereventinfo-method"></a><span data-ttu-id="477f2-103">Método IWiaItem2:: EnumRegisterEventInfo</span><span class="sxs-lookup"><span data-stu-id="477f2-103">IWiaItem2::EnumRegisterEventInfo method</span></span>

<span data-ttu-id="477f2-104">O método **IWiaItem2:: EnumRegisterEventInfo** cria um enumerador que você pode usar para obter informações sobre eventos para os quais um aplicativo está registrado.</span><span class="sxs-lookup"><span data-stu-id="477f2-104">The **IWiaItem2::EnumRegisterEventInfo** method creates an enumerator that you can use to obtain information about events for which an application is registered.</span></span>

## <a name="syntax"></a><span data-ttu-id="477f2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="477f2-105">Syntax</span></span>


```C++
HRESULT EnumRegisterEventInfo(
  [in]        LONG              lFlags,
  [in]  const GUID              *pEventGUID,
  [out]       IEnumWIA_DEV_CAPS **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="477f2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="477f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="477f2-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="477f2-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="477f2-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="477f2-108">Type: **LONG**</span></span>

<span data-ttu-id="477f2-109">Não usado.</span><span class="sxs-lookup"><span data-stu-id="477f2-109">Not used.</span></span> <span data-ttu-id="477f2-110">Defina como 0.</span><span class="sxs-lookup"><span data-stu-id="477f2-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="477f2-111">*pEventGUID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="477f2-111">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="477f2-112">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="477f2-112">Type: \**const GUID\** _</span></span>

<span data-ttu-id="477f2-113">Ponteiro para um identificador que especifica o evento de hardware para o qual você deseja obter informações de registro.</span><span class="sxs-lookup"><span data-stu-id="477f2-113">Pointer to an identifier that specifies the hardware event for which you want to obtain registration information.</span></span>

</dd> <dt>

<span data-ttu-id="477f2-114">_ppIEnum \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="477f2-114">_ppIEnum\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="477f2-115">Tipo: **[ **IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span><span class="sxs-lookup"><span data-stu-id="477f2-115">Type: **[**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span></span>

<span data-ttu-id="477f2-116">O endereço de um ponteiro para a interface [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) .</span><span class="sxs-lookup"><span data-stu-id="477f2-116">The address of a pointer to the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="477f2-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="477f2-117">Return value</span></span>

<span data-ttu-id="477f2-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="477f2-118">Type: **HRESULT**</span></span>

<span data-ttu-id="477f2-119">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="477f2-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="477f2-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="477f2-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="477f2-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="477f2-121">Remarks</span></span>

<span data-ttu-id="477f2-122">Um aplicativo chama esse método para criar um objeto enumerador para as informações do evento.</span><span class="sxs-lookup"><span data-stu-id="477f2-122">An application calls this method to create an enumerator object for the event information.</span></span> <span data-ttu-id="477f2-123">**IWiaItem2:: EnumRegisterEventInfo** armazena o endereço da interface [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) do objeto enumerador no parâmetro *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="477f2-123">**IWiaItem2::EnumRegisterEventInfo** stores the address of the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface of the enumerator object in the *ppIEnum* parameter.</span></span> <span data-ttu-id="477f2-124">Em seguida, o programa usa o ponteiro de interface para enumerar as propriedades do evento para o qual ele está registrado.</span><span class="sxs-lookup"><span data-stu-id="477f2-124">The program then uses the interface pointer to enumerate the properties of the event for which it is registered.</span></span>

<span data-ttu-id="477f2-125">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="477f2-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers that they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="477f2-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="477f2-126">Requirements</span></span>



| <span data-ttu-id="477f2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="477f2-127">Requirement</span></span> | <span data-ttu-id="477f2-128">Valor</span><span class="sxs-lookup"><span data-stu-id="477f2-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="477f2-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="477f2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="477f2-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="477f2-130">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="477f2-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="477f2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="477f2-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="477f2-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="477f2-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="477f2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="477f2-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="477f2-134"><dt>Wia.h</dt></span></span> </dl> |



 

 
