---
description: Emite um comando para um dispositivo de hardware de aquisição de imagem do Windows (WIA) 2,0.
ms.assetid: a077448f-2029-4fd3-8bce-c0291afd0b79
title: 'IWiaItem2: método eviceCommand de:D (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceCommand
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2961a3c0e0d1b75a487b9bf112e76bee8c937a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788661"
---
# <a name="iwiaitem2devicecommand-method"></a><span data-ttu-id="6b81d-103">IWiaItem2: método eviceCommand de:D</span><span class="sxs-lookup"><span data-stu-id="6b81d-103">IWiaItem2::DeviceCommand method</span></span>

<span data-ttu-id="6b81d-104">Emite um comando para um dispositivo de hardware de aquisição de imagem do Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="6b81d-104">Issues a command to a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b81d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b81d-105">Syntax</span></span>


```C++
HRESULT DeviceCommand(
  [in]            LONG      lFlags,
  [in]      const GUID      *pCmdGUID,
  [in, out]       IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="6b81d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b81d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b81d-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b81d-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b81d-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="6b81d-108">Type: **LONG**</span></span>

<span data-ttu-id="6b81d-109">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="6b81d-109">Currently unused.</span></span> <span data-ttu-id="6b81d-110">Deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="6b81d-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6b81d-111">*pCmdGUID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b81d-111">*pCmdGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b81d-112">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="6b81d-112">Type: \**const GUID\** _</span></span>

<span data-ttu-id="6b81d-113">Especifica o comando a ser enviado para o dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6b81d-113">Specifies the command to send to the WIA 2.0 device.</span></span> <span data-ttu-id="6b81d-114">Consulte [_ *comandos* \* do dispositivo WIA](-wia-wia-device-commands.md).</span><span class="sxs-lookup"><span data-stu-id="6b81d-114">See [_ *WIA Device Commands*\*](-wia-wia-device-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b81d-115">*ppIWiaItem2* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6b81d-115">*ppIWiaItem2* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b81d-116">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6b81d-116">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="6b81d-117">Recebe o endereço de um ponteiro para o item [**IWiaItem2**](-wia-iwiaitem2.md) criado pelo comando, se houver.</span><span class="sxs-lookup"><span data-stu-id="6b81d-117">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) item created by the command, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b81d-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6b81d-118">Return value</span></span>

<span data-ttu-id="6b81d-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6b81d-119">Type: **HRESULT**</span></span>

<span data-ttu-id="6b81d-120">Além dos códigos de erro COM padrão, o método pode retornar o valor a seguir.</span><span class="sxs-lookup"><span data-stu-id="6b81d-120">In addition to the standard COM error codes, the method may return the following value.</span></span>



| <span data-ttu-id="6b81d-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6b81d-121">Return code</span></span>                                                                                       | <span data-ttu-id="6b81d-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b81d-122">Description</span></span>                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b81d-123"><dt>**E \_ CMDNOTSUPPORTED**</dt></span><span class="sxs-lookup"><span data-stu-id="6b81d-123"><dt>**E\_CMDNOTSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="6b81d-124">O comando não é implementado para a interface [**IWiaItem2**](-wia-iwiaitem2.md) na qual o método é chamado.</span><span class="sxs-lookup"><span data-stu-id="6b81d-124">The command is not implemented for the [**IWiaItem2**](-wia-iwiaitem2.md) interface on which the method is called.</span></span> <span data-ttu-id="6b81d-125">O valor numérico para esse erro ainda não foi definido.</span><span class="sxs-lookup"><span data-stu-id="6b81d-125">The numeric value for this error is not yet defined.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="6b81d-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b81d-126">Remarks</span></span>

<span data-ttu-id="6b81d-127">O comportamento desse método é diferente dependendo da categoria do nó no qual o método é chamado.</span><span class="sxs-lookup"><span data-stu-id="6b81d-127">The behavior of this method is different depending on the category of the node on which the method is called.</span></span>

<span data-ttu-id="6b81d-128">Quando o aplicativo envia o comando do [**WIA \_ cmd \_ Take \_ Picture**](-wia-wia-device-commands.md) para o dispositivo usando o método **IWiaItem2::D evicecommand** , o sistema de tempo de execução WIA 2,0 cria um objeto [**IWiaItem2**](-wia-iwiaitem2.md) para representar a imagem.</span><span class="sxs-lookup"><span data-stu-id="6b81d-128">When the application sends the [**WIA\_CMD\_TAKE\_PICTURE**](-wia-wia-device-commands.md) command to the device using the **IWiaItem2::DeviceCommand** method, the WIA 2.0 run-time system creates an [**IWiaItem2**](-wia-iwiaitem2.md) object to represent the image.</span></span> <span data-ttu-id="6b81d-129">O método **IWiaItem2::D evicecommand** armazena o endereço da interface no parâmetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="6b81d-129">The **IWiaItem2::DeviceCommand** method stores the address of the interface in the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="6b81d-130">Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="6b81d-130">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b81d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b81d-131">Requirements</span></span>



| <span data-ttu-id="6b81d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b81d-132">Requirement</span></span> | <span data-ttu-id="6b81d-133">Valor</span><span class="sxs-lookup"><span data-stu-id="6b81d-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b81d-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b81d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6b81d-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6b81d-135">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6b81d-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b81d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6b81d-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6b81d-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6b81d-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b81d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b81d-139"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b81d-139"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b81d-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="6b81d-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6b81d-141"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6b81d-141"><dt>Wia.idl</dt></span></span> </dl> |



 

 
